# Design decision framework

Use this as a decision process for a new screen. Its design rules are inferred from the visible Petal and BR10 outputs and their measured styles.

## 1. Allocate attention before allocating components

Write a sentence of the form “The user is here to [act or understand], and must see [current state] before doing it.” Pull out the entity, one primary result, any immediate choices, and the details needed for confidence. Number the actual steps on paper if that helps you sort them.

Sketch three layers on a blank page.

1. At the orientation layer, name the current object or scope and expose the top-level ways to change it.
2. At the working layer, give the main object enough continuous area for the dominant reading pattern. Select and compare on a shared lane. Read a result top to bottom. Scan a board on meaningful axes.
3. At the commitment layer, place the next action in reach of the facts that explain it. Move low-priority actions into a clear secondary row, a small utility circle, or deeper disclosure.

Scan the sketch before adding detail. The main object should be identifiable by area and placement alone. If the layout consists of equally important modules, combine related elements until one visible structure can lead.

## 2. Choose density from the task

Start with the desired unit of reading. A booking chooser should make the row easy to select and name. A confirmation should make the ticket easy to recount. An operations board should make its axes and states easy to compare. Dedicate space to the limiting unit early.

- For catalog or transaction tasks, allow short periods of playful emphasis. Lead with the identity or result. Use broad pastel clusters for complete subtasks and white for the record or hero.
- For monitoring, keep the operational background white and align time and resource columns. Save broad gradients and large illustrations for contexts with real narrative space. Use small repeated accents or patterns and group controls by how they change the view.
- For a narrow view, keep the important action in reach if it depends on choices above or below it. Collapse a two-column recap into a compact dock and detailed sheet when doing so clarifies the task.
- When the first fold contains only chrome, check whether the date or scope rows can share a surface, whether parent context can move into a smaller label, and whether a preview of the working unit can come sooner.

Allow each new screen to keep its own dominant geometry. Repeat the alignment and state rules across the product.

## 3. Assign each color a job

Start from lavender, white and near-black. Assign white to whichever surface carries the main work. Add pastel after the grayscale hierarchy reads.

For each colored area, write its role in one phrase, such as “time availability,” “selected service family,” “completed inventory” or “transaction details.” Choose the light fill by the local task. Give a deeper accent the smaller accompanying marks. Every state should also be read through text, icon, shape, order or position. Place the compact legend close to repeated states when labels would crowd the units.

Reserve ink fill for the next action, the active member of a group or another specifically named high-salience state. If using ink at the top of an ordinal scale, show the scale label and numeric value, and give the actual selection an additional boundary treatment. If two nearby elements compete, preserve the higher-priority ink surface and mute or move the other action.

Count color roles during review. One hue can have different semantic roles on unrelated screens, such as peach for contextual detail in a receipt and medium occupancy in a calendar. Make each assignment coherent within its screen and any flow where users compare the same states.

## 4. Build hierarchy with text and measurable spacing

Use the lightest weight that maintains the intended hierarchy. Load Plus Jakarta Sans before assessing wrapping. Use 800 with tight tracking for the biggest identity, result and important numbers. Use 600–700 for decision labels and other strong names, 400 for explanatory copy, and a larger line-height ratio for prose than for display. Add tabular digits wherever units must align or update.

Start with 16 px mobile outer gutters and 16–20 px internal panel padding. Use about 2–4 px inside the label/value pair, 6–12 px between inline pieces, 12–16 px between local subgroups and 24–28 px between stages. Increase or decrease spacing at the specific relationship that needs clarification. Look at the resulting column baselines before adding more wrappers.

Use contextual rounding. An outer surface can use 28–32 px, an inner block 16–22 px and a pill its full radius. Tight timeline or matrix cells use about 10–12 px. Check that shape differences mirror information roles at a glance.

## 5. Choose the right visual carrier for a fact

Choose by what the user compares.

- **Magnitude over choices.** Embed a shared-baseline strip or bar inside the chooser. Give it a quiet track, proportional fill and a visible selected state. Provide a direct reading of the key value.
- **Parts of a total.** Use a short segmented, horizontal track whose widths reflect the parts. Make the segment order correspond to the line items or legend. Label the whole duration or value.
- **One measure per person or entity.** Use a halo around its avatar or mark when that makes a relationship immediate. Keep air between the picture and the arc. Pair it with a printed value and useful category.
- **Temporal or positional states.** Let the grid position and the axes carry the main meaning. Use tone, small rails, texture and labels to distinguish what position alone cannot.
- **Identity or trust.** Use a face, illustration, review or badge when it supports a decision. Give it a bounded place in the established grid and reserve clear space around its subject.

Write what each visual mark is derived from. If there is no real comparison or data relationship, keep the text label by itself.

## 6. Escalate emphasis in steps

First adjust position and grouping. Then strengthen text or add space. Then use a bigger silhouette, a pastel area, an ink state or a ring. Apply stronger shadow only where layers actually need to separate. Leave the strongest dark fill for the most important action in that area.

Keep one local asymmetric detail if it helps the user notice something in context. A rotated rating seal on art, a small labeled overlay at its opposite edge, or a ticket notch is enough for many layouts. At mobile width give the detail less room and choose the best anchor. Keep decorative paths behind labels and choices.

Decide what the user sees after the action. For success, give the outcome a brief visual beat and follow with the durable record. For an error or exception, specify what happened and how to recover. For an empty work area, use the shared shell and a task-specific reset. For data-heavy states, build the full detail into an accessible surface and retain the inline context that led there.

## 7. Evaluate with three scans and two stress tests

1. **Distance scan.** At a small scale, find the main object and deepest fill in each zone. They should match the intended reading order. Equal silhouettes or competing fills indicate where to regroup.
2. **State scan.** Read active, available, selected, disabled and destructive treatments with hue reduced. The key differences should persist in shape, labels, checks, position or contrast.
3. **Optical scan.** At normal size, check the center of each circle, alignment of numeric baselines, space between label and value, contrast of metadata, sticker clearance, crop boundaries and rail endpoints.
4. **Density stress.** Try long translated names, larger type, an earlier and later time, a short event, an overlap, and a keyboard focus indicator. Verify that the core selection and reading order remain possible.
5. **Interaction stress.** Scroll to the actual end, expand the sheet, switch a meaningful status, recover the empty state, and check whether data updates in both the working and summary areas. Use an equivalent local or conceptual test where a feature is beyond scope.

Review the final output with the [quality checklist](DESIGN_QUALITY_CHECKLIST.md). Use its corrective actions before changing the core style.

## Evidence behind the decision rules

The booking comparison shows that color and geometry can remain recognizable through a shift from a desktop rail to a mobile dock and summary sheet. The confirmation revisions show how a brand wordmark can change while the composition and interaction cues read as the same design. The held-out calendar shows that data density can replace the large illustration and that black can carry high utilization when a legend and selection outline preserve the distinction. The resulting rules favor recurring roles and relationships, with task-specific choices for ornament, density and layout. [Cross-screen validation](ANALYSIS_EVIDENCE.md#held-out-validation)
