# Design DNA

## Identity

A cool lavender canvas, white anchor surfaces and pale color groups frame high-contrast controls. Lavender surrounds the content, white defines the object the user is working on, and warm or cool pastels identify related blocks of information. A near-black pill, circle or inset marks the current choice, the next action or an outcome that deserves immediate recognition. The strongest text is compact, heavy and dark.

The family handles two kinds of attention. The booking and confirmation screens make room for a human subject, an illustration or a moment of reassurance. The operations calendar spends that room on a legible board. In both cases the interface has visible axes and repeatable controls. Its expressive details live inside bounded areas or in the gaps around them.

The five saved designs cover four compositions. Petal has a desktop booking screen, a separately authored mobile booking screen and a mobile confirmation with two wordmarks. BR10 Business uses the same language for a mobile staff calendar. The mobile calendar also exposes week, empty, filter, create and appointment detail states. Source screen IDs P1–P4 and B1 refer to the [evidence register](ANALYSIS_EVIDENCE.md).

## The fingerprint

Preserve this combination when changing product, content or layout.

1. **A cool, lightly colored field remains visible.** Lavender gives sections breathing room and makes white surfaces legible by silhouette. On a schedule, white takes more area and carries the grid.
2. **Black signals agency.** Selected categories, times and ranges go ink/white. The commit action gets the most substantial ink shape in its action zone. A confirmation check may own the ink focal point before the next action comes into view.
3. **Pastel and deeper accent work in pairs.** A broad fill declares a module or state family. A thin bar, dot, arc or fill repeats that relationship with much less area. A label, glyph or position explains what it means.
4. **Type changes register sharply.** Dense, tightly tracked 800-weight display type sits next to lighter, longer-legged support text. Values carry weight independently of their labels. Aligned numeric comparisons use tabular digits.
5. **Geometry expresses function.** Outer surfaces are soft, inner surfaces step down, and controls collapse into pills or circles. Calendar items and matrix cells have smaller corners so the grid stays visible.
6. **Some data is part of the control itself.** Time capacity sits inside the hour picker, occupancy inside employee rings and date strips, and duration inside the recap. Marks have a visible baseline, reference track or endpoint.
7. **Each layout has a dominant object.** Lead with identity and a paired live receipt, with a celebratory result and its ticket, or with a date context and its board. Unequal areas let the task decide the shape of the page.

A perforated ticket, a rotated rating seal, a background curve and a small emoji can reinforce the family. Use each where it serves the story or the task. The exact illustration, flower mark, wordmark, booking copy and service category names belong to their source screens. The family survives their replacement.

The craft comes from relationships among familiar primitives. Tailwind utilities and Font Awesome were used inside the source previews. A build in Tailwind, Material, Bootstrap or shadcn/ui will feel like this family when it reproduces the color roles, uneven visual weight, optical details and state grammar. Generic defaults give components familiar shapes and leave those relationships unresolved.

## Composition

### Shared rules

- Establish a strong content edge. Align outer surfaces and section titles to it, then use a smaller internal inset for rows and values. Let an explicitly scrollable strip cross the outer edge when seeing the next item helps discover more choices.
- Give the main object the largest continuous surface. Cluster the most important values and actions inside that object or in its adjacent recap.
- Use a quieter background interval between separate jobs. Limit density within a job through alignment, matching row baselines and compact supporting labels.
- Follow context → focus → choices or data → commitment or next step. A desktop recap may sit beside the first three phases. On mobile its compact version can stay in reach while the detailed record opens on demand.
- Pair one visually distinctive structure with familiar controls. A time strip can become a chart or a record can become a ticket. The frame around it can stay predictable.

### Desktop booking

At 1440 CSS px, the header, main and footer have a 1360 px maximum wrapper with 24 px inner gutters. The usable lane is 1312 px wide and begins at x = 64. The main grid is 908 / 380 px with a 24 px gap. The narrower rail starts level with the hero, holds the ticket and review, and sticks 24 px from the top where space permits. In this implementation the two-column body starts at 1280 px. At 1279 the summary returns to normal flow.

The 330 px hero uses a 1.1:1 copy-to-art grid. A 36 px copy inset frames tiny status badges, an oversized title and a short description. Four values share a baseline toward the bottom, leaving a deliberate band of air after the description. The inset illustration has a white perimeter and two asymmetric overlay anchors, one at the upper trailing corner and one at the lower leading corner.

The next modules change proportions inside the same left edge. A 210 px bundle sits beside a wider service list, then a specialist card and time picker share a roughly 5:7 split. The review rail ends early. The open area under it gives the last chooser stage more visual weight.

### Mobile booking and confirmation

The mobile compositions use a 480 px maximum shell and a 375 px reference canvas. A 16 px main gutter leaves 343 px for the primary column. Floating layers may sit 12 px off the viewport edge and therefore reach slightly wider than the content.

P2 places the illustration above the studio copy, encloses the metrics in a light inset, turns the bundle into a horizontal strip, and moves duration and price below row descriptions. Specialist and time modules stack. The 64 px bottom dock holds time and total on the left and the action on the right. Expanding the amount side reveals a compact ticket above the dock and leaves the current point in the chooser visible.

P3/P4 build a centered reveal above a left-aligned record. A short outcome headline sits under the success badge. The white ticket carries identity, when, who, duration, price and code. The largest action follows the ticket. A pair of equal white buttons follows the primary action, then three colored utility modules, policy and exit. The contrast shifts from the result to the receipt, then settles into a lighter sequence of supporting cards.

### Operational screens

B1 places the date header and the staff board on white surfaces. Branch, date, range and filter controls progressively narrow the scope. The calendar margin is 12 px so the grid gains 8 px of extra width versus the 16 px top sections. The time gutter and employee columns keep the same alignment as the staff header. An hour is 72 px tall at the default setting. Event heights follow duration and neighboring items share an axis.

The board uses three visual channels at once. Position encodes time and employee. Fill and rail encode status. Pattern distinguishes blocked, break, off-hours and available space. A labeled peach rule marks the current time. The seven-day view turns time into comparable cells with printed percentages and retains the same shell, legend language and action placement.

The calendar title, branch selector and month value establish context. Most white area belongs to scanning. The action sits in a 56 px ink circle above a floating white navigation pill. The task-specific filters and record edits open in sheets.

## Typography

Plus Jakarta Sans is the loaded face across the corpus. Use `ui-sans-serif, system-ui` as fallbacks. The source loads weights 400, 500, 600, 700 and 800. Set text by role and use a tight title line box with room for diacritics and descenders. In accessible builds, check the actual font in every required script and at enlarged text settings.

- **Display.** Desktop identity is 46/46 at 800 with −1.61 px tracking. Mobile identity is 32/32 with −1.12 px. Confirmation is 30/31.5 with −1.05 px. The calendar title is 24/24 with −0.72 px. Long strings should wrap cleanly while staying visually compact.
- **Section.** Booking stage headings are 24/32 desktop and 21/31.5 mobile at 700, with −0.025 em tracking. Typical module names are 15–18 px at 600–700. The 20 px filter and create headings use 800 with −0.5 px tracking.
- **Body and rows.** Hero copy uses 15/24.375 desktop and 13.5/21.9375 mobile at 400. Booking row names are 15/22.5 desktop and 14/21 mobile at 600. Mobile support copy often uses 11/16.5 or 12/16. Confirmation service names use 13.5/20.25 at 600.
- **Labels.** Metadata uses size, role color and weight together. Ordinary metadata stays in sentence case. Short field labels such as DATE and TIME use 10–11 px, 600–700, uppercase and about 0.05 em tracking. Keep them beside the value they explain.
- **Numbers.** Date, time, capacity, durations and prices get separate weights and, in many repeated time or price roles, tabular digits. A recap total is 34/34 desktop, 32/32 confirmation and 20/25 in the dock. Values align at the row edge whenever users compare them.
- **Dense operational type.** Event time is 10/11.5 at 700, name is 11.5/13.8 at 600, and service is 10/12 at 400. These are cell-specific values. Keep times and names readable with room for a detail surface and a text-size control if the schedule is this dense.

Type sizes here use font size/line height in CSS pixels. [Design tokens](DESIGN_TOKENS.json)

## Color and surface behavior

The shared base is **canvas `#F1EEF6`**, **white `#FFFFFF`** and **ink `#151515`**. The cool canvas is desaturated enough to sit behind white. Ink stays neutral so its meaning survives any category.

- **Lilac `#E8DCF8` / `#A46CE6`** is used for catalog groupings, reminders and booked calendar cells. Deeper lilac reappears as item rails and duration fills.
- **Peach `#FBE2CA` / `#EE9757`** warms transactional context and some social proof. It also identifies medium utilization and the live time marker in B1. Full-strength orange carries a warning or time accent in small doses.
- **Sky `#CDEFF6` / `#3FBAD6`** makes availability and time information easy to recognize and marks in-progress calendar cells. Choose an appropriate deep fill against a pale track.
- **Lime `#DFF3C6` / `#79B443`** anchors specialist and preparation cards and denotes positive, available or low-load states in B1. Use its deep partner on rings, status glyphs and small outlines.
- **Variation follows jobs.** Petal mobile explicitly switches the bundle and list fill by active service category. Its review moves from lilac on desktop to peach on mobile. In B1, status colors can be configured. Keep the deeper accent coupled to the local fill and label when switching palettes.

White organizes the main record, controls and the calendar grid. Pastel usually stays flat and spans the related group. Exact flat pixels from the full-page captures put pure ink at roughly 2.8–4.4% of area. The four light pastel fills total about 25–33% in the Petal captures and about 13% in B1. These are descriptive lower bounds for theme use. Shadows, antialiasing, images and mixed colors account for much of the remaining area.

Foregrounds use ink alpha, typically 0.45–0.7 in metadata and supporting copy. A number of source labels use alpha levels that are too faint for production. On a new interface use 0.65–0.7 over these lights for meaningful small type, or verify an equivalent contrast for the actual pair. Give disabled options an explicit state where users need to understand why they are unavailable. Reserve the faintest text or marks for supplementary cues.

## Spacing and shape

The cadence comes from a roughly 4 px utility lattice with intermediate choices. Design in group-sized steps. Use 2–4 px between a label and its value, 6–12 px for compact row and control relationships, 12–20 px for component interiors, 16–24 px between modules, and 24–28 px between task stages. Desktop hero copy uses 36 px and mobile art uses 8 px around the image field. These narrow and wide spaces are intentional because the groups operate at different scales.

- A main hero or ticket is 30–32 px radius. A regular filled module is 24–28 px. An inset is often 16–22 px. The photo, option control, select state and compact chip use full curves.
- Booking rows use 18 px mobile or 20 px desktop corners. Dense calendar cards use 12 px. Week cells and blocked bands use 10 px. Keep a readable run of flat edge along a uniform lane.
- Two-tone relief usually comes from adjacent fill. Separators use 1 px ink at about 0.06–0.1 alpha. The ticket perforation has 2 px dashes at 0.1 alpha and circles cut visually into its edges using canvas color.
- Round controls are often 36–44 px across. Dominant commit bars reach 56–60 px with a contrasting 44 px icon well. A visual disc can live inside a larger row target.
- Measurement roles justify compact marks. A service rail is 4 × 40 px, an event rail 3 px wide, a duration track 10–12 px tall, and the week header track 6 px tall. Keep their thickness independent of the card radius.

## Layers, imagery and effects

Use the two observed elevation treatments by role. The low shadow combines a 1 px contact layer and a broad lavender falloff. It appears on ordinary white surfaces, including the main card, nav rail and secondary controls. The floating shadow is darker and concentrated by negative spread. It appears under the rating seal, next-slot overlay, mobile dock, calendar navigation, floating action and success disc.

Most pastel surfaces are quiet, unshadowed slabs. The booking art field is a bounded exception, using a diagonal lilac → `#EFE4F8` → peach gradient. The fine lavender SVG curves read as atmosphere across open canvas. Keep them behind readable controls. B1 shows why this matters when a line crosses a branch pill.

Use one hero image with a clear subject, in a palette that already belongs to the surrounding surface. P1/P2 use the same 4:3 source image in a bottom-aligned `contain` box. It reads as a flat cutout with dark contour, rounded human shapes and a few muted colors. Working portraits are circles with cropped photographic faces. Add a white keyline or spacing inside a metric ring so fill and photo are visually independent.

Iconography is predominantly Font Awesome 6, with a mixture of deliberate solid and light-looking regular forms at about 10–18 px in most controls. Put utility marks inside quiet light discs, give an ink action a white endpoint, and let tiny indicators sit inline with text. The illustrated background, brand mark and metric rings are custom SVG or image treatments. A single uniform icon stroke would erase that variation.

Confirmation motion is localized. The source has 600 ms pop and rise entrances and a 24 s orbit for the petals. Meaning is already present in the static check, heading and ticket. On future screens, keep the outcome recognizable in a reduced-motion state.

## Micro-level craftsmanship

- Align the strong part of a pair. Price follows a common trailing edge even when its unit or length changes. A long row title yields width before the price or selection control loses its position.
- Use two adjacent indicators for a meaningful state. A selected item has both a lifted white-tinted row and an ink check. A completed record can pair a lime field with a check. Current time has a line, anchor and label.
- Give portable formats literal logic. The ticket perforation separates accounting from the appointment facts. The duration segments map to actual item lengths and match the accents beside those line items.
- Keep optical space inside a ring, cap a fill at its endpoints, and leave a tiny gap between segments. The seals and avatar badge can cross a boundary by a few pixels because their placement is deliberate.
- Use local asymmetry inside a larger grid. The tilted seal and offset availability sticker leave the subject recognizable. The long specialist card anchors its picker at the bottom edge and leaves room around the introduction.
- Use a small typographic shift before adding another UI element. A date eyebrow, a lighter count inside a filter, a 2 px text gap or a small status dot can define a group within the existing surface.
- Put faint surface accents where the reading path can move around them. Crop background arcs and shapes at the intended surface edge. Label data marks exactly where they are read.

## Guardrails and corrective actions

- Equal-size cards with equal shadows flatten focus. Merge related controls into one surface and let task importance set area and alignment.
- Saturated backgrounds, gradient actions and multicolored button sets weaken the shared ink state. Restore the pale pairings and give each active group one decisive state.
- Filling every row with an opaque tile turns a list into a stack of cards. Use a common tinted bed, quiet unselected rows and a discrete selected treatment.
- Using the same large rounding on a time grid obscures the cell edges. Reduce the radius, maintain the timeline and rely on small rails, labels and patterns for differentiation.
- A number in a large card by itself is weak when it explains a choice elsewhere. Embed the comparison in the strip, ring, bar or receipt row that it informs.
- Copying tickets, emoji, orbiting petals and slogans into routine views makes the family feel theatrical. Use a ticket for a record with a clear recap boundary. Give a landmark flourish a real job.
- Low-contrast text, ambiguous chart positions, tiny actions and clipped labels can be present in an appealing prototype. Resolve them through contrast, spacing or a detail path while keeping the same visual roles.

Continue with the [component patterns](COMPONENT_PATTERNS.md), the [layout playbook](LAYOUT_PLAYBOOK.md) and the [decision framework](DESIGN_DECISION_FRAMEWORK.md).
