# Analysis evidence

Investigation date **24 November 2026**. Five generated designs were visible in the signed-in UXPilot library. The library reached “No more designs to load.” One file contained all five frames. The preview grouped the two confirmation frames under one flow and displayed desktop booking, mobile booking and BR10 Calendar under single screens. All five were opened individually. The credit indicator read 0 before and after the investigation. [UXPilot generated screens](https://uxpilot.ai/a/all-designs) · [Source file](https://uxpilot.ai/a/ui-design?page=hkQa1hPIHsARNUdqrJiS) · [Reference overview](references/reference-overview.png)

## How to read the evidence

- **Measured.** CSS values, SVG attributes and element boxes came from the generated frame alone. Full-capture proportions and the revision diff came from pixel counting. Lengths are CSS px unless explicitly labeled as image pixels or SVG units.
- **Declared.** Theme configuration, authored classes, markup and the source asset loading configuration establish a value or relationship. Computed values were preferred when the two diverged after layout or transforms.
- **Observed.** A shape, ordering, role, group, artifact or behavior is visible in a screenshot or confirmed in a replay state. High confidence applies to visible pixels or direct measurements. Moderate confidence applies when deciding what a localized visual choice is doing.
- **Inferred.** A reusable principle or design decision is proposed from repeated observations. The confidence depends on whether distinct compositions demonstrate the relationship.
- **Open.** Some boundaries remain untested or require extrapolation, especially dark mode, wide operational layouts, alternate languages, accessibility behavior and the original designer's intent.

Chrome's live DevTools identified the generated `about:srcdoc` frames and read the frame declarations and static canvas copies. Live computed body styles in all five static copies give `#F1EEF6` background, `#151515` text and the Plus Jakarta Sans family. The interactive preview documents were rendered in isolated Chrome contexts at the same desktop and mobile preview widths. The local replays supplied the computed geometry and most state evidence. Source fonts and all visible image assets loaded in those replays. The live editor title bars, canvas tools, preview pager, chat sidebar and promotional UI were excluded from the design measurements.

The PNGs are 2× captures. The five full-page images cover all vertically scrolling default content. For the P2 and B1 full-page images only, fixed bars and controls were hidden at capture time so they would leave the content beneath readable. Separate viewport and scrolled captures show their rendered placement. The two confirmation PNGs capture their settled entrances and a paused orbit. Calendar and booking interactions described here were exercised on local copies with disposable state. The screenshots preserve rendered designs, including prototype artifacts where visible.

## Screen inventory and anchors

### P1 · Petal Studio Booking, desktop

- **Frame** `HWj1vC952HMVaYFstVl3`. Dedicated preview 1440 × 920 CSS px. Full page 1440 × 1468, saved at 2880 × 2936 image px. [Live preview](https://uxpilot.ai/p/hkQa1hPIHsARNUdqrJiS?wireframeId=HWj1vC952HMVaYFstVl3) · [Full capture](references/petal-booking-desktop-full.png)
- **Measured.** Header, main and footer are bounded by a 1360 px wrapper with 24 px inner padding. The `#layout` grid begins at x = 64, y = 160 and is 1312 px wide. Chooser and rail are 908 / 380 with a 24 px gap. The rail sticks 24 px from the top. At 1280 its columns measure 828 / 380. At 1279, 1120 and 1024 the rail is static and stacks in a single parent column. The paired hero remains split at these measured intermediate widths.
- **Measured.** `#hero` is 908 × 330 with a 32 px radius and 475.61 / 432.39 px inner columns. Copy is inset 36 px and the right art field has a 12 px margin. The art measures 408.39 × 306. Headline 46/46 at 800, tracking −1.61 px. Support paragraph 15/24.375 at 400, ink/60. The four metric cells share a 46 px-high row with faint vertical lines.
- **Measured.** Category nav and header nav have white beds and 6 px inner padding. A sample `#service-list` is 686 × 294 with four 666 × 68.5 px rows, 10 px list inset and 14 × 16 px row padding. The active row is white/80 with a small shadow and ink check disc. `#service-grid` is 210 / 686 with a 12 px gap. The later schedule split is 373.33 / 522.66 with a 12 px gap.
- **Measured.** The 380 px ticket has 24 px padding and a 32 px radius. The peach inset is 332 px wide, with 22 px corners and 16 px padding. The ticket's cut line is dashed ink/10 at 2 px, with 24 px round edge cutouts. The €86 total is 34/34 at 800 with tabular digits. A 60 px primary action has a 44 px contrasting inset circle.
- **Observed.** The ink title and the illustration balance each other. The rail starts at the hero baseline and ends earlier than the chooser. The profile panel has a long interval above its bottom avatar picker. The space allows the action area of the profile and time panels to align at the bottom of the row. Strong anchors recur at different scales.

### P2 · Petal Studio Booking, mobile

- **Frame** `XlBuWLaqSrHRHgMfDNQU`. Dedicated preview 375 × 840 CSS px. Full page 375 × 2030, saved at 750 × 4060 image px. [Live preview](https://uxpilot.ai/p/hkQa1hPIHsARNUdqrJiS?wireframeId=XlBuWLaqSrHRHgMfDNQU) · [Full capture](references/petal-booking-mobile-full.png) · [Viewport with dock](references/petal-booking-mobile-viewport.png)
- **Measured.** Main gutters 16 px. The 343 px hero has a 30 px radius and 8 px inset. The 327 × 210 art field comes first and has a 24 px radius. The title is 32/32 at 800, tracking −1.12 px. The hero fact strip is 303 px wide with a 16 px radius, canvas at 70% and four equal columns. Service and schedule blocks begin 28 px after the previous stage.
- **Measured.** Categories are 40 px high with 8 px gaps. The 343 px list uses 6 px padding with roughly 331 × 82 px rows, radius 18 and 12 px padding. The rails remain 4 × 40. Duration and price share a line below the supporting copy, while the icon stays trailing. The specialist portrait shrinks from 90 to 64 px. The sky time picker has a 26 px radius, 16 px padding and 22 × 90 px tracks.
- **Measured.** The handoff dock is 351 × 64 px, with 26 px rounding and 12 px outside gutters. It carries the date at 11/16.5, amount at 20/25 and Book in a white 48 px pill. The expanded 351 × 299 white summary has a 28 px radius, 16 px padding, floating shadow, 40 × 4 px handle, 10 px segmented track and 20 px edge notches. It sits 8 px above the dock. [Expanded summary](references/petal-booking-mobile-summary-sheet.png)
- **Observed.** P2 carries the desktop associations through a different layout. Art moves ahead of copy, list columns become metadata lines, the offer becomes a strip and the summary moves within thumb reach. The mobile review has a peach fill while desktop uses lilac. Switching all four categories in replay changes both the bundle and list fills together. Hair is lilac, Nails is peach, Laser is sky, Brows & Lashes is lime. Selection remains ink. [Nails category](references/petal-booking-mobile-nails.png)

### P3 · Petal Booking Confirmed, original wordmark

- **Frame** `b93lxzZ7hzUqO5yb23dz`. Dedicated preview 375 × 840 CSS px. Full page 375 × 2005, saved at 750 × 4010 image px. [Live preview](https://uxpilot.ai/p/hkQa1hPIHsARNUdqrJiS?wireframeId=b93lxzZ7hzUqO5yb23dz) · [Full capture](references/petal-confirmation-original-full.png)
- **Measured.** The centered celebration region spans about 315 px below the 60 px header. A 150 px petal region surrounds a 76 px ink disc. The H1 is 30/31.5 at 800 with −1.05 px tracking and settles into two lines at 375 px. A 343 × 610.75 white ticket follows, with 30 px corners and 20 px padding. The peach `#when-block` uses equal 129.5 px internal columns and a divider over the portrait row.
- **Measured.** The duration strip is 12 px high with a 4 px gap. Widths split 60:25, and the second uses deep lilac at 50% alpha. The two service labels are 13.5/20.25 at 600 and matched line prices use 700. Two dotted-edge cutouts and a 2 px dashed separator introduce a 32/32 total. The code panel below is 303 × 72 with a 20 px radius. The primary button is 58 px high. Equal white secondary buttons are 48 px high and 10 px apart. The countdown, preparation and reminders are 26 px-radius cards with 16 px padding.
- **Observed.** Sky → lime → lilac reprises the same quiet grouping at the end of the screen. Checklists add a round check and a strike when complete. Reminder switches recur in a different geometry while using the same ink state. The drop from celebratory display to a left-reading record is the biggest change in rhythm. The ticket's assets include an illustrative barcode with a readable adjacent code.

### P4 · Petal Booking Confirmed, br10 wordmark revision

- **Frame** `jcTbOUXEZGvO7KqSlxZM`. Same 375 × 840 CSS px preview and 750 × 4010 image px full capture as P3. [Live preview](https://uxpilot.ai/p/hkQa1hPIHsARNUdqrJiS?wireframeId=jcTbOUXEZGvO7KqSlxZM) · [Full capture](references/petal-confirmation-rebrand-full.png)
- **Measured.** With both renders settled, 2,683 pixels differed out of 3,007,500, about 0.089%. The difference rectangle was x 298–451 and y 48–103 in image pixels. This is the width adjustment and text change in the centered brand group, from “petal” to “br10.” Everything outside that rectangle matched in the captured reference state.
- **Observed.** The new wordmark works in the same shell with the same flower, illustration-free confirmation, title, ticket and lower cards. These two frames are independent saved designs and count as one composition when evaluating recurrence.

### B1 · BR10 Business Calendar

- **Frame** `a4880620-3c47-48ff-af7e-8344ec5b8624`. Dedicated preview 375 × 840 CSS px. Full page 375 × 1644, saved at 750 × 3288 image px. [Live preview](https://uxpilot.ai/p/hkQa1hPIHsARNUdqrJiS?wireframeId=a4880620-3c47-48ff-af7e-8344ec5b8624) · [Full day capture](references/br10-calendar-full.png) · [Viewport](references/br10-calendar-viewport.png) · [Scrolled board](references/br10-calendar-scrolled.png)
- **Measured.** Header title 24/24 at 800, tracking −0.72 px. Branch rail 343 × 52 with a 6 px inset and 40 px buttons. Date card 343 × 230 with 28 px radius and 16 px padding. Seven day tiles are about 42.7 × 76 with a 24 × 6 load meter. Branch, selected day, range and status can each use ink in their local group. The float nav is 351 × 60 and the 56 px FAB sits 20 px above its top.
- **Measured.** White board begins at x = 12, y = 440 and is 351 px wide. The staff bar and grid use matched 38 px left insets, 8 px trailing insets and 6 px column gaps. The three columns are each about 97.7 px. The 09:00–20:00 axis establishes 72 px/hour, measured 792 px of usable time range. Event cards use 12 px corners, a 3 px deep accent rail and contents at roughly 10–11.5 px. The 2 px peach current-time line has a white-keylined 10 px anchor.
- **Measured.** Employee rings use a 44 px box over a 30 px portrait and pale track. The source load bands are below 40% lime, 40% to below 75% peach and 75% or higher ink. Week cells are 40 px tall with 10 px rounds, tabular percentage labels, hatch for outside scope, and a white/ink double ring for applicable cells in the selected date column. The day and week reads share the same scope controls. [Week view](references/br10-calendar-week.png)
- **Observed.** Off-hours hatch, break dots, dark blocked hatch and dashed availability create different textures near pastels with dark text. The shifted spacing and smaller radius preserve the grid at a width where a booking card would consume a full column. Cancellation is gray/dashed with a strike. Staff paging, the range toggle and the status strip expose denser data through existing shapes.
- **Measured and observed.** Modal states use 32 px top corners, 20 px horizontal padding, a 40 × 4 handle, ink/30 scrim and 2 px backdrop blur. The reference CSS declares an 86vh maximum and the UXPilot viewport shim produced about 791 px of height at the 840 px replay. A large body scrolls internally. The filters include staff and display tabs. The create form uses a pale pill search, choice tiles and a footer action. The appointment detail transfers the peach time inset, rails, duration, perforation and black action from Petal's ticket. The empty staff state remains inside the white work region and offers a reset. [Staff filters](references/br10-calendar-filters-sheet.png) · [Display preferences](references/br10-calendar-display-sheet.png) · [Month picker](references/br10-calendar-month-sheet.png) · [Create form](references/br10-calendar-create-sheet.png) · [Create form lower section](references/br10-calendar-create-sheet-bottom.png) · [Detail](references/br10-calendar-detail-sheet.png) · [Empty state](references/br10-calendar-empty.png)

## Repeated relationships

**High confidence.** All five use Plus Jakarta Sans, the same ink, light canvas, four pastel/deep pairs and the same named shadow recipes. Titles are weight 800 with tight tracking and labels use a lower-weight hierarchy. At recurring decision points, selected controls read as understated dark silhouettes within white, pale or transparent surroundings. P1/P2 and B1 use matching category or status accents on a parent group, item edge or legend. P1–P4 emphasize a state with a dominant dark action or disc. [Design tokens](DESIGN_TOKENS.json)

**High confidence.** Wide, continuous white surfaces carry top-level context or detailed reading. Pastels occupy more area on the Petal consumer screens. Exact flat shares are shown in the order canvas / white / four pastel fills / ink.

- P1 measured **32.26 / 18.96 / 24.75 / 2.83%**.
- P2 measured **22.14 / 11.64 / 33.07 / 3.45%**.
- P3 measured **31.34 / 19.97 / 26.30 / 4.36%**.
- P4 measured **31.35 / 19.97 / 26.30 / 4.35%**.
- B1 measured **13.42 / 38.72 / 13.32 / 3.99%**.

These shares count exact matches in the full-page PNGs, including the canvas at the scroll tail. Alpha blends, antialiasing, gradients, artwork and textures fall outside the counts for their base colors. The split captures explain the small difference in white and ink where fixed layers were hidden. The figures support the distribution relationship and are descriptive of these captures.

**High confidence.** Data is integrated into controls and records. P1/P2 use baselined availability bars and specialist rings. P3/P4 use proportional length, a countdown track and a checklist count. B1 uses day-strip bars, roster rings, event blocks and a labeled occupancy matrix. All give the underlying measure an obvious point of contact with the task.

**Moderate confidence as a reusable design principle.** Use the nearest pastel or shape to signal a coherent cluster, and recover hierarchy by strengthening a small role before adding another surface. This reads through the choice row, ticket line and calendar event pattern. Different jobs call for different color mappings and density. The exact ornament, asset, radius or geometry should follow its role.

## Differences and source flaws

- **Contrast.** The source commonly uses ink/45 and ink/55 for small metadata. Calculated on plain white, ink/45 is roughly 2.97:1 and ink/55 is about 4.04:1. On lilac, ink/55 is about 3.74:1 and ink/65 is about 5.08:1. White lettering on the deep orange time tag is about 2.28:1. The spec uses stronger text for meaningful small labels and ink on orange where that color treatment is needed. These values are composited sRGB pairs and characterize the styles, independent of raster antialiasing.
- **Mobile overflow.** P2 deliberately scrolls its category and date strips. Its hour track row itself has visible overflow. At 375 px the final tracks extend beyond the 343 px card and are partly clipped by the viewport. Keep the intentional strip peek and bound the chart lane. Very narrow B1 overlapping blocks can truncate a person to an initial or fragment. Use a compact identifier or overlap count with a detail path.
- **Decoration layer.** A B1 background curve crosses the active branch pill. The reusable rule places contour lines behind controls and in open canvas where possible. P1/P2 show more breathing room for that effect.
- **Chart semantics.** The P3/P4 countdown keeps the “Now 12:40” label near the center while the black pill is separately positioned 52% across and overlaps the label area. The cyan fill is about 37% of the track, while the displayed time spans one third of 09:00–20:00. In the receipt the midpoint timestamp is also laid out independently of the segment break. Preserve the display pattern and derive its positions and labels from the same values.
- **Selection versus quantity.** B1 uses ink for high occupancy as well as selected controls and the primary action. Explicit percentages and the legend make high occupancy visible as a scale. The week view gives selected eligible dates an additional outline. This qualifies the initial rule about dark fill.
- **Interaction scope.** The Petal month pill shows a label and chevron. B1's month control demonstrably opens a picker sheet. The Petal prototypes include glyph-only controls and compact action areas. These render observations cover appearance and the inspected flows. Focus management, full keyboard behavior, all disabled cases, persistence and assistive technology behavior require implementation-level checks.

## Rule check across the corpus

- **P1** checks asymmetric composition, editorial scale, layered art, a white transaction surface and shared black state. Its longer profile panel shows how an intentional empty interval can align two differently structured modules.
- **P2** checks that the category palette and component roles survive a mobile reflow. Its light review color changes and the record becomes a dock disclosure, which makes component geometry and hue mapping conditional. Its hour-row overflow is a source flaw with a bounded implementation path.
- **P3** checks that the same palette and dark state can mark an outcome and its next action. It supplies the compact checklist, paired secondary buttons and dedicated record reference roles. Its countdown exposes a limit on reusing visual positioning verbatim.
- **P4** checks the scope of brand variation. The shared hierarchy, sizing and component positions survive the text swap in the top brand group.
- **B1** checks the same hierarchy at operational density. The lighter shell carries the board and the deeper palette moves to labels, edges and marks. Its high-utilization cells require the additional distinction between a quantity and a selection.

## Held-out validation

B1 was inventoried and sighted in the live browser during discovery. Detailed extraction started with P1–P4, then seven predictions were written from the Petal screens before the detailed B1 replay measurements and state captures. B1 functions as an operational holdout for testing the rules. P3 and P4 duplicate a composition. The pair tests how the same layout reads with a changed wordmark.

1. **Ink marks selection and action.** B1 supports this in branch, date, range, status, destination and create controls. The check produced one refinement. In an ordinal chart, ink can also encode the top band when its legend and selection outline clarify the role.
2. **Lavender and white carry the shell.** B1 supports the shared colors. Its exact white area is about double the desktop booking capture, with pastel moving to repeated data units and accents.
3. **Type uses the same hierarchy with a lower ceiling.** The face and weight range carry over. The 24 px operations title and compact labels add a dense role to the Petal scale.
4. **Radii follow level.** The 28 px date card and board, 32 px sheet edge, tight 10–12 px cells and full pills require the role-based scale in the spec.
5. **Metrics sit where they inform a choice.** Load tracks in date cells and rings in the roster replace the large booking availability instrument. The top-left time axis and legend show how to carry a greater quantity of data.
6. **Ornament is conditional.** The default board puts dates and staff in the space that a consumer view gives to a hero. Curves and rings still appear. The record-detail state brings back the ticket where its grouping helps.
7. **Stability and variation coexist.** Aligned case-specific columns, a persistent scope shell and different content structures for day and week validate the principle of keeping the same design grammar while changing the layout to fit the job.

The held-out view supported the major rules about palette, typography, state, data and surface geometry. The master prompt was refined to name when high occupancy can be dark, how to contain decorative lines, how the white plane expands with density, and how to keep label geometry data-driven.

## Transfer exercise

The [seed inventory audit](LAYOUT_PLAYBOOK.md#transfer-exercise-for-seed-inventory) applies the rules to a new setting with a bounded 375 px operational shell, drawer selection, a short instrument tracking 14 of 18 items, a white reading plane, status-rich rows and a dock that summarizes a selected item. Its 77.8% fill follows 14 ÷ 18. Secondary colors label stock and verification, leaving selection and commitment to ink. The core identity reads in the proposed structure through the dark decision state, proportioned progress and softly colored status.

The paper design passes the conceptual hierarchy, palette/state and task-related data checks. An actual render is needed to score optical alignments, contrast, clipping, targets and behavior. The exercise supports using the same typographic and component relationships with different data, and allowed the prompt to reduce reliance on the original booking motifs.

## Scope and remaining uncertainty

The corpus is rich in variants within one visual direction and spans only three main task families. A broad recommendation such as role-based color has stronger evidence than any fixed threshold for every layout. P1 provides the desktop evidence. Tablet, arbitrary browser widths, dark mode and fully implemented production states would require additional references or design decisions. Motion was inspected through declarations and settled frames. Alternative states such as staff filters and empty views were sampled to explain the visual grammar. The identity, hierarchy, component roles and suggested production adjustments are evidence-based design inferences.
