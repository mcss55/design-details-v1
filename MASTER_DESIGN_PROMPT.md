# Master prompt for generating a new screen

## Your assignment

Design an original digital interface for the product, audience, task and form factor in my brief. Use the visual language below to decide how the screen should work, look and respond. Apply it to the actual content and workflow. Preserve the hierarchy and state relationships through changes in product domain, copy, navigation, imagery and components.

Begin by identifying the immediate job and the state a user needs to understand before acting. Choose the number of screens and depth of detail requested in the brief. Design them with believable content and space for realistic lengths. Deliver the requested screen or implementation. Where the brief leaves a routine choice open, choose a reversible default that supports the job.

## Target character

Make the interface soft in its surroundings and decisive where people act. Use a cool, light lavender field, clean white objects, pale color in coherent areas and near-black for the most important choices. Give important words and numbers a tight, confident weight. Make a single title, record, instrument or area of work lead each screen.

The family can support a generous editorial introduction or a dense operating view. In an expressive screen, use one clear subject or outcome as the visual anchor. In an operational screen, let a date, board, row alignment or comparison take the same role. Use rounded outer surfaces, clear internal axes and crisp, small indicators. Add a tactile detail only when its object or meaning is immediate, such as a perforation on a receipt, a ring around a measured entity, or a small label that attaches to an illustration.

## Compose from the job

Start with a single sentence describing what the user came to understand or do. Sketch the screen with three areas. Orient the user with the current entity or scope. Give the work one main region with a clear reading order. Place the next action alongside or just after its consequence.

Choose the arrangement that matches the content.

- **Select and commit.** On wide screens, pair a dominant chooser with a narrower, top-aligned live recap. Use roughly 67–72% for the chooser if the content supports it. A starting point at 1440 px is a 1360 px centered wrapper, 24 px inner gutters, a 24 px grid gap, about 908 px for choices and 380 px for the recap. The working lane may itself contain a split hero, a narrow bundle beside a wider list and an unequal pair of related selectors. Keep the outer edge common. Let the rail end naturally. For mobile, reorder related content and move recap details into an expandable layer when a short fixed summary helps keep the decision in reach.
- **Resolve and orient.** Use a brief centered success or completion moment, then return to a left-aligned white record. Group the entity, state, time or key context, line items and totals in the order a person would recount them. Place one decisive next action directly after the record. Pair lower-priority actions on the next line. Separate independent follow-up jobs into a few quiet, colored modules. Show the exit and material policy at the edge of the flow.
- **Monitor and act.** Open with a compact title and scope. Put wide lenses such as location, date or range before narrow status filters. Give the board or work list the broadest continuous white area. Align the axes, labels and repeated units. Put pastels inside events, chips and data marks to preserve the white reading plane. A relevant floating action or tab rail may stay within reach. Use a white sheet to handle deeper configuration or work on one selected record.
- **Browse or compare.** Group related items in one shared surface. Lead each row with its identity and let fixed trailing columns hold the values people compare. Use tone, a rail, a status chip or a selection control to add distinctions. Keep repeated units consistent where the user is comparing them. Allocate more area to the featured object only when the task makes it more important.

Use 16 px mobile outer gutters as a starting point, about 343 px usable at 375 px viewport width. A dense board or floating dock can use 12 px gutters for extra room and purposeful separation from the content edge. A reference mobile shell caps near 480 px. Recompose at the point where the longest useful label, numeric columns and actions can no longer coexist in the wide layout. Test the fold at the actual target size, and keep bottom layers clear of final content and safe areas.

Give each zone a reading direction. Stack qualifiers directly above or below what they qualify. Align values to the same edge. A heading can anchor the start of a stage. Number stages only when order matters. Preserve more space between task transitions than between related values.

## Palette and visual emphasis

Use these sRGB colors as the default. They work as relationships that can be carried into a product palette.

- Canvas `#F1EEF6`, white surface `#FFFFFF`, near-black ink `#151515`.
- Lilac `#E8DCF8` with deep violet `#A46CE6`.
- Peach `#FBE2CA` with orange `#EE9757`.
- Sky `#CDEFF6` with cyan `#3FBAD6`.
- Lime `#DFF3C6` with green `#79B443`.

Use white to clarify the main object, raised controls and information-dense reading surfaces. Let the canvas appear in the gaps and around outer corners. Make most pastel surfaces flat. Spend a pastel on a meaningful functional group or repeated state. Spend its deep accent in a much smaller rail, dot, stroke, arc or fill. Keep the text ink so light surfaces share a coherent foreground.

Choose hue assignments for the actual job. Lilac can orient a choice family or a pending state. Sky works for availability or in-progress work. Lime works for readiness, completed work or a positive measure. Peach adds warmth to transactional context and can mark medium load, an exception or a live time marker. Use one clear legend when the same scale is repeated. In a single flow, color for the same state should travel with its associated label and icon.

Use ink fill with white content for selected items and primary actions. More than one ink shape can coexist if each belongs to a distinct selection or action group. Make the final commitment visually strongest in its zone. An already dark dock can use a nested white action with an ink icon well. A high-value position in a labeled matrix can use ink independently of selection. Show a numeric scale and use a ring or boundary to indicate the cell currently in focus. Differentiate meaning with a label, icon, position, check or pattern as well as color.

Use full ink for essential content. Secondary text may use softened ink. For meaningful small labels use roughly 65–70% ink on the specified lights as a starting point and measure contrast against the actual backdrop. Target at least 4.5:1 for essential normal-size text. Very faint marks can support context when the same information has a legible path. Avoid using the brighter accents as the only carrier of small important text.

## Type and number treatment

Start with **Plus Jakarta Sans**, then `ui-sans-serif, system-ui` as fallbacks. Use weights 400, 500, 600, 700 and 800. Match the proportions and weight contrast if a different face is required.

- **Main identity or outcome.** Use 46/46 at 800 for a large desktop identity. Mobile identity can use 32/32 at 800 and short mobile outcomes 30/31.5 at 800. Practical operating titles use about 24/24 at 800. Track large display text tightly, about −0.03 to −0.035 em.
- **Section entry.** Use about 21/31.5 mobile or 24/32 desktop at 700 with roughly −0.025 em tracking for prominent stages. Use about 16–20 px at 700–800 for utility group and sheet headings as appropriate.
- **Focusable row title.** Use 14–15 px at 600–700. Add a stronger 12–16 px price or quantity where it is compared across rows. Use 11–13 px supporting copy with a more open line height and consistent spacing. Hero prose can be 13.5–15 px with about 1.6 line height.
- **Short labels.** Use 10–11 px with stronger tracking and 600–700 for field-eyebrow labels such as DATE, STATUS or TOTAL TIME. Keep normal labels in natural case and within easy eye distance of the value.
- **Numbers.** Use tabular numbers in repeating prices, dates, times, duration, counters and instrument readouts where alignment matters. Prominent totals can use 28–34 px at 800. A persistent dock can carry a 20 px weight-800 value. Use bold values, lighter labels, consistent units and a stable shared edge.
- **Dense cells.** When a narrow matrix forces compact type, keep the leading identity and time readable and disclose full details on activation. A time at 10 px and name at 11.5 px are ancestor examples of compact schedule-cell type. Use larger type if the actual width allows, and test with localization and large text.

If a phrase wraps, preserve its shape and grouping through sensible line breaks and adjacent space. Adjust the hierarchy before reducing legibility to fit one line.

## Spacing, geometry and depth

Use a 4 px-derived cadence with intermediate 6, 10 and 14 px steps where the relationship calls for them. Use about 2–4 px for label/value gaps, 6–12 px inside rows and chip groups, 12–20 px for component padding, 12–16 px between closely related modules, and 24–28 px to signal a change in stage. A large desktop hero copy inset can use 32–36 px.

Use outer corners of 28–32 px on the main white or softly filled cards, 24–28 px on ordinary colored modules, 16–22 px on important insets and 10–12 px on dense data cells. Use full radius for pills, user photos and circular controls. Keep the shapes aligned and let a shared surface enclose multiple rows where the rows are related. Reserve a 4 × 40 px stripe or a 3 px event rail for a small, repeatable accent.

Use two soft shadows as needed:

- Ordinary white layer uses `0 1px 2px rgba(21,21,21,.04), 0 12px 32px -12px rgba(76,52,120,.18)`.
- Floating layer uses `0 18px 40px -16px rgba(21,21,21,.35)`.

Leave flat pastel modules close to the canvas. Where rows need division, use a 1 px ink rule at about 6–10% alpha. Use clear focus outlines on interactive elements. Keep visual button shape independent from hit area, especially for a compact icon inside a larger row.

## Design the components together

**Primary action.** A pill about 56–60 px high can carry a left-set semibold label with 24–28 px leading padding and a 44 px contrasting icon circle near the trailing edge. Use this larger treatment on a meaningful continuing or committing action. A smaller 36 px companion action can sit on a related promo or card. Put equal-priority secondaries in white or lightly filled 44–48 px pills, with short labels and aligned icons.

**Pills, tabs and status.** Use pale or white containers with 4–6 px inset for a segmented control and fill the active selection with ink. On mobile, spaced individual pills work when labels need horizontal scroll. Use compact 6–8 px dots and count badges to supplement an actual label. Distinguish the active filter's shape or fill from the data status hues. Keep controls within the scroller and give the row an obvious continuation when more options exist.

**Choice and record rows.** Place a small deep-color rail, name, supporting text and a stable trailing affordance from left to right. Use 14–15 px semibold titles and a compact metadata tier. Shift supporting values below the name on narrow screens. Use a shared tinted list bed, transparent normal rows and a selected row on about 80% white with a black check disc. An add state can use a white disc with an ink plus. For line items inside a white record, simplify the row to name, note and tabular value. Use the same accent order if a related chart shows the parts.

**Progress and selection instruments.** Use a pale track that makes the maximum visible, then a connected rounded fill for the actual value. Place the count or units where the user reads the mark. For selections across hours or other ordered choices, share scale and baseline, encode capacity in length or height, show quiet disabled marks, and put an ink fill on the active option. A 10–12 px horizontal segment track with 4 px gaps can encode parts of a whole. A thin round-capped progress ring can sit around a photo or mark, with a visible gap to the subject and a printed percentage. Keep data labels and markers anchored to the actual positions they describe.

**Record or ticket.** Give the subject a compact header. Place the most important context in a 22 px radius tinted inset with about 16 px padding. Put details and any meter on the main white surface. If a literal receipt is appropriate, use a 2 px low-contrast dashed line and two 20–24 px canvas-colored discs centered at its ends. The discs should appear cut out of the card edge. Put the total in an obvious place below. Show the actual reference identifier in text. Use decorative codes or other ornaments only when they reinforce a real identification or retrieval step.

**Dock and sheet.** For a long choice flow, pair a 64 px dark dock about 12 px from the edge with concise selection context and a 48 px nested action. Expand a white summary above it when the user needs detail. For modal editing or settings, use a white bottom sheet with about 32 px upper corners, a 40 × 4 px handle, helpful title and visible close, about 20 px side padding, and a light scrim. Separate form groups with pale neutral wells, short labels and subtle dividers. Give the scrollable sheet enough space to reach its last control. Ensure dismissal, keyboard navigation and focus return work.

**Date pickers.** Put a month label and paired 40 px navigation circles above a regular seven-column grid. At mobile width use approximately 48 px cell height, 4 px gaps and 16 px corners. Select the day with an ink surface. Where dates include a load indicator, put a small dot or bar under the date and explain the scale in the picker. Provide a direct return to the current date.

**Inputs and settings.** Use a pale canvas-colored pill or softer rounded field to express input. Put a useful label above it and a compact icon inside when meaningful. A source-style search field is roughly 48 px tall with a 12–14 px leading glyph. Independent settings can use a 48 × 28 px switch with a 20 px white thumb, dark on and pale off. A checklist can use 44 px light rows and a 24 px round check indicator. Use plain language for unavailable options and keep action visibility separate from validation state.

**Operational cells and empty state.** Use the base plane and shared axes for scanning. Use a pastel status fill and deeper rail where repeated items need quick recognition. Use simple texture for structurally different states, such as faint hatching for outside scope, dots for a break, and ink hatch for a blocked region. Pair each with text or an icon and show a short key. Show important current position with a labeled line or distinct marker. An empty state belongs inside the same work area and gives one clear reason and, when applicable, one bounded recovery action.

## Imagery, icons and restrained richness

Use one primary image or illustration only when it serves the story. For a friendly identity hero, choose a flat editorial subject with soft shapes, a clear dark contour, restrained palette and room around the face or action. Place it in a rounded, bounded panel and keep its subject readable on mobile. A soft lilac-to-peach gradient fits that panel. Anchor small data overlays at opposite corners and leave the middle for the artwork. A single circular rating seal may tilt around 6° if its tiny supporting label remains readable. Portraits use a circular crop, a narrow white keyline when needed, and enough margin for a ring or badge.

Use one consistent icon vocabulary with small solid and regular glyphs. Font Awesome 6 Free is a strong starting point for these proportions. Use mostly 10–18 px utility glyphs centered in 36–44 px control wells. Put bold state glyphs in dark or colored shapes only where they reinforce meaning. A restrained native emoji can accompany a genuine milestone, section or tone cue. Keep utilitarian screens focused on their labels and data.

A background may carry one or a few wide, low-contrast lavender contours in `#DED2F1`, `#E3D9F3` or `#E6DDF4`. Keep stroke around 1.5–2 px and visible primarily in the open canvas. Use flat colors everywhere the content needs predictable contrast. Localize any motion to a real entrance, expansion or status change. A small success animation can settle into a clearly readable static frame. Honor reduced motion.

## Review and revise

Before delivering the screen, check it at the intended width, at a narrow width and in a high-density case. Inspect default, selected, disabled, keyboard-focus and relevant empty states. Confirm that numbers and labels still read correctly after a state change and that fixed layers leave the end of the content reachable.

- When every area looks equally important, give one object clearer area and position. Combine neighboring controls that share a job and quiet duplicated elevation.
- When the work starts to look like a generic dashboard, remove decorative badges or repeated panel titles. Give the distinct task a useful visual structure such as a labeled track, asymmetric choice-plus-recap composition or aligned working board.
- When color is loud, bring back a continuous white or lavender plane. Shrink deep hues to rails, icons, dots or fills. Restore the ink anchor for the active choice and primary action.
- When a data mark works only through hue, add a useful label, shape, glyph, scale or pattern. Verify that its position or proportion matches the value.
- When the screen feels cramped, tighten the low-priority cluster or disclose it on demand. Protect the main label, value and action. When there is too much empty space, use the space to clarify grouping and affordance before adding content.
- When the composition feels vague at a glance, check where the largest text, largest surface and darkest action are. Give each a concrete role in the same user journey.
- When small details look unresolved, check the optical alignment of dots, icons and numbers, the spacing around the subject, the width of the last choice, the position of boundary labels and the spacing of the ticket notches.

Honor the product's own content, language and decisions. The newly designed interface should read as one coherent original screen, with a clear user task, precise state treatment and local visual character.
