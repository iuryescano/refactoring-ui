# UI Refactoring Examples

These examples are original calibration patterns inspired by the visual refactoring mindset behind this skill. They are not copied from the book. Use them to translate abstract guidance into small, practical UI changes.

## Hierarchy And Action Priority

Before:

- A settings screen has three equally bright buttons: "Save", "Cancel", and "Delete workspace".
- The page title, plan name, billing note, and warning banner all use similar weight and contrast.
- The destructive action appears beside the primary action with the same visual treatment.

After:

- Make "Save changes" the only filled primary button.
- Move "Cancel" to a quiet text or ghost button.
- Move "Delete workspace" into a lower-priority danger zone or confirmation flow.
- Make the workspace name and current plan the main content, with billing notes in softer supporting text.

Implementation pattern:

```text
Primary action: filled, high contrast
Secondary action: ghost or text
Destructive action: visually quiet until confirmation
Supporting metadata: smaller, softer, closer to the object it describes
```

## Spacing And Grouping

Before:

- A profile panel uses the same 16px gap between every label, field, section title, and footer action.
- Related fields feel disconnected, while unrelated sections feel crowded together.
- Borders are used between nearly every row to compensate for weak spacing.

After:

- Use smaller gaps inside a field group and larger gaps between groups.
- Remove borders that repeat what spacing already communicates.
- Put each section title closer to its own content than to the previous section.
- Keep footer actions separated from form fields with a clear outer gap.

Implementation pattern:

```text
Inside a group: tight spacing
Between groups: noticeably larger spacing
Between page regions: largest spacing
Borders: only where precision or interaction needs them
```

## Form Design

Before:

- A checkout form stretches every input to full width, including short values like ZIP code and CVC.
- Labels are bold and darker than the entered values.
- Error text appears far from the field and focus states are browser defaults.

After:

- Keep short inputs visually short, or group them with related fields on the same row when space allows.
- Make labels readable but quieter than the values users need to verify.
- Place helper and error text directly below the relevant field.
- Give focus, error, disabled, and loading states intentional visual treatment using the local design system.

Implementation pattern:

```text
Input width follows expected value length
Label supports scanning, value carries emphasis
Field state appears next to the field
Important choices can become option cards with clear selected state
```

## Dashboard Or Table Polish

Before:

- A dashboard table gives every column equal weight and left-aligns all numbers.
- Status badges, row actions, timestamps, and secondary metadata compete with the record title.
- Heavy grid lines make the table look busy without improving scanning.

After:

- Make the record title the strongest element in each row.
- Right-align comparable numeric columns.
- Soften repeated labels, timestamps, and secondary metadata.
- Use subtle row separation, hover states, or background contrast instead of heavy grid lines.
- Keep filters and primary actions easier to find than table utilities.

Implementation pattern:

```text
Primary cell: title plus one supporting line
Numbers: tabular and right-aligned when compared
Status: clear but not louder than the row object
Utilities: available, but visually lower priority than task actions
```
