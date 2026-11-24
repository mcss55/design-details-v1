# Design quality checklist

Review the rendered screen at the target size and at a narrow or high-density size when applicable. Use real labels, prices or quantities and at least one changed state. Include the end of the scroll and any sheet the main task requires. A paper exercise can be reviewed for concept and hierarchy. Scores that depend on rendered behavior or contrast become pending until there is a render.

## Pass conditions

Treat each applicable failure below as a release blocker even when the weighted score is high.

- The primary action and current selection can be identified in their own context. Users can also distinguish them through text, shape, position or a state indicator.
- The main task fits or scrolls through. Fixed layers, dense units and sheets leave an available path to required data and controls.
- Essential fine text and large text have readable contrast against their actual surfaces. Use 4.5:1 for normal text as a practical target, and use a visible focus outline and an adequate target for meaningful actions.
- Encoded values agree with their labels and underlying data. A repeated color is consistent within its local legend. Important identifiers remain available as text.
- The user can dismiss overlays and recover important empty or failed states. The next action reflects the current scope and selected data.

## Score from 0 to 4 per criterion

- **4** means the principle is evident, precise and robust in the checked states.
- **3** means it works in the primary state with a minor, localized deviation.
- **2** means it reads partly or depends on a narrow set of content or states.
- **1** means treatment is present but substantially weakens clarity or family resemblance.
- **0** means the trait is absent or undermines the user job.

For each row below, multiply its weight by the score divided by 4. Sum to 100. Use **90–100** and all applicable pass conditions for a handoff candidate. **78–89** asks for targeted fixes and a second pass. **Below 78** calls for revisiting screen composition and state rules. A product can score 4 on a criterion with a purposeful equivalent to any optional motif.

### 1. Composition and visual priority · 16 points

- The user's immediate job has an identifiable focal object. The area, first heading and action reinforce a coherent reading order.
- Related controls share boundaries or an edge. The main object has room. The screen has a reason for any uneven split, empty interval or sticky recap.
- **Repair.** Start with a grayscale view. Combine redundant cards and reallocate width or height to the primary object. Put the action beside the consequence or after the record.

### 2. Family resemblance · 14 points

- A cool field, white anchors, soft panels, tight heavy type and small precise marks work together.
- A screen from another domain would still share the ink decision state, pastel relationship and layered shape logic.
- **Repair.** Restore the core palette roles, vary the shape scale by function and add one meaningful data or object cue in the main workflow.

### 3. Color and state hierarchy · 12 points

- Broad light color groups information. Deep accent indicates status or data in a smaller area. Ink remains the most decisive fill in action zones.
- Selected, default, disabled, in-progress and destructive labels are legible with hue reduced. A dark high-value matrix cell has a separate selection cue.
- **Repair.** Lower chroma or move accents into rails and marks. Use shape, ink/check or a clear label to disambiguate. Consolidate adjacent hues that represent the same job.

### 4. Typography and number treatment · 12 points

- Display has a distinctly heavier and tighter register than text. Important labels, values, notes and fine details form clear tiers.
- Numbers align across rows and updates where needed. Long, localized labels and accents render well.
- **Repair.** Load the typeface before measuring. Strengthen weight or space around important values. Use tabular numbers, consistent units and common trailing edges. Wrap or reflow text when it needs width.

### 5. Spacing and surface geometry · 10 points

- The rhythm is tight within clusters, wider between steps and consistent among peers. Gutter and alignments carry across modules.
- Controls, cards, insets and dense cells have appropriate radii and inner margins for their roles.
- **Repair.** Set the outer and inner edges before tuning the gaps. Reduce large rounding on small cells. Use separators inside one surface where repeated nested cards waste width.

### 6. Components and interaction · 10 points

- Variants share the same anatomy. Buttons and selection controls communicate purpose, weight and state clearly.
- Disclosures keep their context. Interactive targets work through touch and keyboard where appropriate.
- **Repair.** Put row name, value and action on repeatable axes. Make the entire selection row actionable where suitable. Give each icon-only action a name. Restore context and focus when dismissing an overlay.

### 7. Data and information integrity · 8 points

- Charts, rings, ranges and time or count tracks have an understandable scale. Labels align to real boundaries and selected states update the working surface and recap.
- Dense units expose needed details and distinguish patterns with words or glyphs.
- **Repair.** Derive positions and lengths from the same data as labels. Bound the data area. Add a short key, explicit overlap count or an accessible detail path.

### 8. Micro-level finish · 8 points

- Text and icon centers read as optically aligned. Rings clear portraits. Sticker and badge overlaps have a specific role. A ticket's dashed divider and notches line up.
- Hairlines, opacity and elevation create quiet edges. The hierarchy is clear at both a glance and full size.
- **Repair.** Inspect at native scale. Shift based on content, trim conflicting decoration and give a centered mark real clearance. Increase contrast for meaningful fine print.

### 9. Responsive and dense states · 5 points

- The main layout recomposes with purpose. Titles, actions and current values stay reachable at narrow width and larger text.
- The page and any sheet can scroll to their end. Long or overlapping content still has a readable path.
- **Repair.** Move metadata under names, reduce simultaneous columns, add an intentional scroller or disclose details. Reserve actual space above the dock and respect the safe area.

### 10. Restraint and originality · 5 points

- Any illustration, flourish, badge, ticket or unusual chart answers a real need. It earns its area and leaves the work clear.
- The design applies the language to its own content and introduces specific aesthetic decisions beyond framework defaults.
- **Repair.** Remove filler copy, unnecessary status pucks and gratuitous visual effects. Replace inherited decorative assets with one relevant content or data device.

## Review record

For each criterion, write the score and the concrete evidence behind it. Name the screen size and state. Order corrections by the pass conditions, then by score impact. Check the revised render again at the sizes and states where the failure appeared. Record any pending implementation or measurement alongside the result. [Decision framework](DESIGN_DECISION_FRAMEWORK.md)
