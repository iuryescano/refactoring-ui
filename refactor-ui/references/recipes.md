# UI Refactoring Recipes

Use these recipes when you recognize a common UI weakness. Combine only the moves that fit the local product and component system.

## Screen Feels Generic

- Define the screen's main object and make it the visual anchor.
- Replace evenly weighted cards with a clear primary section and quieter supporting sections.
- Add one restrained brand signal: accent border, active navigation treatment, selected state color, or section background.
- Upgrade empty/default states before adding decorative surfaces.
- Remove placeholder-like copy and use specific domain language.

## Everything Competes

- Pick one primary action and one primary content block.
- Reduce contrast, weight, or background treatment on secondary content.
- Convert secondary buttons to outline, ghost, link, or menu actions.
- Move metadata into smaller type, softer color, or a secondary row.
- Remove icon color unless color is carrying useful state.

## UI Feels Cramped

- Increase padding and gaps first, then remove space where density is truly needed.
- Separate groups with larger outer gaps than inner gaps.
- Increase card or panel padding only if content relationships remain clear.
- Avoid cramming a narrow form across a wide row; use columns only when fields are naturally related.
- For dense dashboards, keep row height efficient but add section spacing and clear scan anchors.

## UI Feels Too Sparse

- Check whether the content is too wide or too evenly distributed.
- Add max widths to paragraphs, forms, and controls.
- Use columns to balance a narrow workflow in a wide area.
- Bring related metadata closer to its object.
- Add useful secondary content rather than decorative filler.

## Weak Form Design

- Group related fields and make group spacing unambiguous.
- Use labels for accessibility and scanning, but avoid making labels visually heavier than values or inputs.
- Put helper text near the field it explains.
- Use clear selected, focus, error, disabled, and loading states.
- Avoid full-width inputs when the expected value is short.
- For important radio or checkbox decisions, consider option cards with title, description, and selected state.

## Weak Dashboard Or Table

- Right-align comparable numeric columns.
- De-emphasize repeated labels and emphasize the changing values.
- Combine columns when the relationship matters more than independent sorting.
- Add visual hierarchy inside cells: title, supporting metadata, status, action.
- Use subtle row separation. Try whitespace, background changes, or hover states before heavy grid borders.
- Make filters and primary actions easier to find than table utilities.

## Weak Card Or List Item

- Identify the card's primary fact or action.
- Use one strong title, one supporting line, and optional metadata.
- Keep icon/avatar/image size intentional and consistent.
- Do not let badges, timestamps, or tertiary actions overpower the title.
- Align repeated elements consistently across cards.
- Make selected, hover, focus, and disabled states visible.

## Weak Hero Or Marketing Section

- Make the product, offer, person, or place visible immediately.
- Keep headline content specific; do not hide the actual object behind vague value language.
- Use real or generated visual assets that reveal the subject.
- Protect text contrast over imagery with overlays or image treatment.
- Keep a hint of the next section visible on common viewport heights.
- Avoid turning the hero into a floating card unless the product itself is a framed tool.

## Weak Typography

- Collapse one-off sizes into a small type scale.
- Use weight and color before shrinking text below readable size.
- Shorten line length for paragraphs rather than stretching text across the layout.
- Reduce line-height for large headings; increase line-height for small or wide text.
- Align mixed-size inline text by baseline.
- Add letter spacing only to short all-caps labels or loose large headings.

## Weak Color

- Replace isolated colors with palette tokens.
- Create or reuse shade scales for neutrals, primary, accents, and semantic states.
- Use color to support existing structure, not to create the only distinction.
- Use softer backgrounds with darker text for secondary colored UI instead of saturated blocks everywhere.
- Add icons, labels, or contrast changes for status states.
- Check contrast after every color change.

## Weak Depth

- Decide whether the element is flat, raised, inset, overlaying, or modal.
- Pick a shadow from an elevation scale.
- Use lower elevation for cards and buttons, medium for menus, high for dialogs.
- Add contact shadow only when the element should feel close to the surface.
- Use background contrast or overlap for flat depth.
- Remove shadows that do not communicate layering or interaction.

## Weak Image Handling

- Replace placeholders with real, representative imagery.
- Use fixed aspect-ratio containers for unpredictable uploads.
- Set `object-fit: cover` or equivalent crop behavior where layout consistency matters.
- Avoid scaling icons outside their intended range.
- Crop screenshots or show partial screenshots when full screenshots become unreadable.
- Add overlay, colorization, or text shadow for text over images.

## Too Many Borders

- Remove borders that duplicate spacing or background contrast.
- Use subtle shadow when a surface needs separation from a different background.
- Use slight background differences for adjacent regions.
- Increase spacing between groups instead of drawing another line.
- Keep borders for controls, data grids, and separators where precision matters.

## Before Finishing

- Compare the result to the original at the same viewport.
- Ask whether the primary action, main object, and group structure became easier to see.
- Check whether the UI now uses fewer arbitrary values.
- Verify that polish did not reduce accessibility, responsiveness, or product density.
