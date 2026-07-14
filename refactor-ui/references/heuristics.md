# UI Refactoring Heuristics

Use this checklist when reviewing a UI screen, component, or screenshot. Start at the top; later categories should support earlier decisions.

## 1. Product Intent

- Name the screen's job in one sentence.
- Identify the primary user decision or action.
- Identify the main object: record, property, audit, message, chart, task, search result, profile, plan, or document.
- Remove or defer UI that implies unbuilt behavior.
- Prefer building and iterating on a usable simple version over polishing a speculative full version.
- Pick a personality before styling: calm/professional, playful, editorial, premium, technical, operational, or utilitarian.

## 2. Visual Hierarchy

- Rank content into primary, secondary, tertiary, and background information.
- Use size, weight, contrast, color, spacing, and placement to express that rank.
- If everything feels loud, de-emphasize supporting elements before making the main element louder.
- Avoid relying on font size alone. Softer color and lighter weight often communicate support while preserving readability.
- Treat labels as supporting content. Prefer self-explanatory values when possible, such as "12 left in stock" over a rigid label/value pair.
- Keep labels visible when users need to scan categories or compare similar values.
- Style headings by visual role, not by HTML tag. Keep semantic headings for document structure.
- Actions should form a priority pyramid: one true primary action, a few secondary actions, and lower-priority actions as links, ghost buttons, or menus.
- Do not make a destructive action visually primary until the confirmation step where it is the focused decision.

## 3. Layout And Spacing

- Start with more whitespace than feels necessary, then remove space deliberately.
- Use a spacing and sizing scale. Small steps should be close together; large steps should spread out more.
- Do not fill the full viewport just because space exists. Use max widths, columns, and content-sized panels.
- Let components keep their useful intrinsic width until the viewport forces them to shrink.
- Avoid proportional scaling across breakpoints. Tune headline sizes, padding, gaps, and controls independently for each context.
- Make group relationships obvious: space inside a group must be smaller than space around the group.
- If spacing alone cannot communicate grouping, use background contrast before borders.
- Use grids as tools, not masters. Fixed sidebars, max-width content, and internal grids are often cleaner than making every child fluid.
- In dense enterprise screens, reduce whitespace intentionally but keep group separation and scan paths clear.

## 4. Typography

- Use a constrained type scale. Avoid a trail of one-off pixel sizes.
- Prefer local typography tokens. If none exist, create a small set for body, small text, labels, section titles, page titles, and display text.
- Use fonts with enough weights for hierarchy and legibility.
- Avoid condensed or display fonts for small UI text.
- Keep paragraph line length comfortable. Narrow text can use tighter line-height; wide text needs more line-height.
- Large headings usually need shorter line-height than body copy.
- Align mixed font sizes by baseline when they sit on the same row.
- Left-align long text in left-to-right languages. Center short text only when the line length stays short.
- Right-align tabular numbers when comparing magnitudes in columns.
- Links inside prose need visible affordance; link-heavy interfaces can rely on context, hover, or lower-key styling.
- Use letter spacing sparingly. Tighten large headlines only when the font feels loose; increase spacing for short all-caps labels.

## 5. Color

- Use HSL or another perceptual workflow while choosing colors, even if implementation uses hex tokens.
- Build palettes as shade scales, not as isolated swatches.
- Include neutral shades, primary shades, and accent/semantic shades. Complex products usually need more shades than early mockups suggest.
- Pick base, dark, and light shades first, then fill the gaps.
- Avoid generating endless variants with lighten/darken functions. Use named tokens or a constrained palette.
- As colors get very light or dark, adjust saturation so shades do not look washed out.
- Warm or cool greys can make an interface feel more intentional than pure neutral grey.
- Meet contrast requirements without making every supporting element visually dominant. Try tinted text, flipped contrast, or hue shifts.
- Never rely on color alone for status. Add labels, icons, shape, position, contrast, or text.

## 6. Depth And Layering

- Add depth to communicate elevation, interactivity, focus, or physical grouping.
- Keep the light source consistent. Raised elements usually have a lighter top edge and a shadow below.
- Inset elements can use inner shadows or edge highlights to suggest depth.
- Use an elevation scale instead of arbitrary shadows. Small shadows for subtle lift, medium for dropdowns/popovers, large for modals.
- Two-part shadows can feel more natural: one broad soft shadow and one tighter contact shadow.
- Flat designs still need depth. Use background contrast, lighter/darker surfaces, offset solid shadows, and overlap.
- Overlap elements to create layers when it improves composition, but protect readability and avoid collision.

## 7. Images And Media

- Bad imagery can weaken an otherwise good UI. Use real, high-quality, appropriately cropped images when the product depends on visuals.
- Text over photos needs consistent contrast across the whole text area.
- Improve photo text contrast with overlays, reduced image contrast, desaturation/colorization, or a subtle glow-like text shadow.
- Do not upscale small icons. Put small icons inside a larger colored shape if they need more visual weight.
- Do not shrink detailed screenshots until text becomes unreadable. Crop, simplify, or show a smaller viewport instead.
- Render user-uploaded images inside fixed aspect-ratio containers with cropping rules.
- Prevent image/background bleed with subtle inner shadows or translucent inner borders instead of heavy outlines.

## 8. Finishing Touches

- Enhance existing defaults before adding new decoration: bullets, links, selected controls, checkboxes, radio buttons, tabs, and active states.
- Use accent borders or short color bars to add controlled energy.
- Decorate backgrounds with low-contrast section color, subtle patterns, or simple shapes only when hierarchy and readability are already solid.
- Design empty states as first-run experiences. Include context, a useful next action, and optionally an illustration or icon.
- Use fewer borders. Try shadow, background contrast, or extra spacing first.
- Reconsider default component shapes. Tables, dropdowns, radio groups, and forms can combine related fields, add supporting text, or use richer option cards when the decision matters.

## 9. Verification

- Check desktop and mobile.
- Confirm no text is clipped, overlapping, or too small.
- Confirm primary action is visually obvious.
- Confirm groups are understandable at a glance.
- Confirm contrast works for text, statuses, disabled states, and text over media.
- Confirm hover, focus, selected, disabled, loading, empty, error, and success states are styled.
- Confirm the UI still fits the product personality and local design system.
