# Layout playbook

Start with the user's immediate job and the information they must keep in view. Pick the arrangement that links them with the fewest separate regions. The same color and state grammar works in each arrangement.

## Lay out the screen in five passes

1. **Name the outcome.** Write the one action or answer the screen exists for. Identify the state the user needs to recognize upon arrival. For a chooser it is the current selection, for an outcome it is the resolved record, and for operations it is the scope and exception data.
2. **Draw the common edges.** Start with 16 px mobile gutters or a centered desktop wrapper. Add the header/utility edge, primary content edge and trailing value edge. Make the grid's labels share its grid coordinates.
3. **Choose the largest surface.** Allocate the most continuous area to the main identity, ticket or operational board. Leave enough space in surrounding canvas to show the hierarchy. Group decisions that require comparison and separate jobs that can be read independently.
4. **Place the next action and its supporting context.** While choosing, keep enough current state visible to make the action predictable. When a record is complete, put the action immediately after the facts that let users trust it.
5. **Tune rhythm and overlays.** Use tight spacing within label/value pairs and larger gaps between jobs. Recheck scroll endings, clipping, long labels, overlap and the visibility of the reveal. Use a sparse curve or art accent only when an open region can carry it.

## Pattern A · Select and commit

**Use for** configuring a selection whose rules, cost or output changes along the way.

**Wide layout.** Set a 1360 px maximum wrapper with 24 px inner gutters as a reference. Pair a flexible 67–72% chooser lane with a narrower 320–380 px live recap and about 24 px between them when there is room. The source works at 908 / 380 px. Align their tops so the first choice and anticipated result are visible together. The recap can stick if its height and bottom constraints permit. A review, help snippet or consequence note can appear directly beneath it when the task calls for one.

Place a split introduction above the chooser. Give copy slightly more width and the artwork or contextual graphic a bounded inset. Put fast facts on one line. Keep the next stage visibly distinct with about 24 px of air. Within the stage, try an asymmetric ancillary module beside a larger list or an unequal pair of complementary controls. Keep the stages aligned to the same outer edge.

**Narrow layout.** Recompose the introduction with the image above the identity if that order gives useful context. Use short labels and lightweight, horizontally browsable categories. Change a perpendicular side module into a horizontal row where the list expects the bulk of the width. Move row details beneath the name before narrowing the action. Stack broad selectors. Use a fixed compact recap only if decisions occur down a long page and their consequences are easy to summarize. Expand to a sheet for editable detail.

**Attention path.** Context → stage title and active group → selected items → related choice of time or options → decisive button. A live recap should repeat the exact selected state and keep the amount or consequence stable in location. Allow group selection, one item selection and one commit action to use dark at the same time when each occupies its own visual group. [Desktop booking](references/petal-booking-desktop-full.png) · [Mobile booking and dock](references/petal-booking-mobile-viewport.png)

## Pattern B · Resolve and orient

**Use for** a confirmation, resolved task, order completion, or record handoff.

Center the outcome only for the opening beat. Open with a recognizable symbol and a short heading. Follow it with one line that answers where confirmation lives or what happened. A white record surface below returns to the left edge and supplies facts in the same reading order the user would recount them. Put time or another high-salience context in a light inset. Keep totals or status value separate through weight, spacing and optional perforation.

Then put one wide next action below the record. Place lower-priority paired actions in a balanced row when practical. Give utilities their own light panels if they answer separate questions. A helpful sequence is record → next action → time or location → preparation or preferences → policy → exit. Keep the critical result understandable at the top even if the deeper record extends well below the fold.

Use celebratory motion for a meaningful transition. A static icon and title carry the same meaning, and the outcome remains brief enough to leave the record preview visible. A ticket works for a handoff with real line items, a traceable reference or a record boundary. A plain structured surface works when a receipt metaphor has no role. [Confirmation](references/petal-confirmation-original-full.png)

## Pattern C · Monitor and act

**Use for** a calendar, queue, matrix, inventory, roster, moderation list or other high-cadence operational screen.

At mobile width, put the screen title and immediate scope in a compact header. Put broad filters first and more granular state chips closer to the work. Cluster the date, count or range controls into one white control surface, with a little more space around it than within it. Give the board slightly more width where a useful axis would otherwise compress. Keep column labels aligned throughout scroll or paging. Use a sticky header only if it preserves important context while leaving a useful portion of the board visible.

Start with a white working plane. Put color inside the item, under a status mark or on a coded meter. Give each repeated unit a clear leading identifier and a shared axis for comparison. Short or crowded units can show a concise identifier and an affordance to disclose the rest. A weak label should never be the sole path to a required detail.

Open filters and record changes in a reusable white sheet when task context matters outside the overlay. Keep the underlying board recognizable through a modest scrim. For time-bound data, keep the ordering or timeline in place between day and week modes. Show the actual measures and their scope. The high-load ink in a heatmap has an accompanying bound, percentage and legend. This lets users distinguish it from a selected control. [Full day board](references/br10-calendar-full.png) · [Week board](references/br10-calendar-week.png) · [Detail sheet](references/br10-calendar-detail-sheet.png)

## Pattern D · Browse a list or compare a collection

This extension is inferred from the service list and the operational matrix. Give each repeated group one shared base. Put a work's title or category on the leading edge, alignment-critical values on the trailing edge, and a single narrow rail or small chip where it encodes a meaningful distinction. Use a secondary inset or a focused color change on selection. If the groups are genuinely comparable, keep their structure repeated. If one object is featured, give it either more area or a stronger contrast edge and let neighboring objects remain stable. Use small right-aligned charts only when comparing across rows benefits from them.

## Responsive decisions

- At 375 px, preserve the 16 px page and 12 px dock or board gutters where the content fits. For very narrow widths or larger type, preserve the hierarchy through wrapping, fewer simultaneous data columns, or a larger detail state.
- At the measured 1024, 1120 and 1279 px widths, the source desktop page retains a split hero while the ticket returns to flow. Treat the 1280 px rail threshold as measured for this prototype. Choose the threshold for a new screen from its longest credible row label, the width of the comparison units and the visible height of its recap.
- The dedicated mobile booking has a separate structure. Use the same roles at smaller widths and move context to where it can be read with the action. Keep the keyboard and mobile safe areas in mind for fixed layers.
- Where content scrolls sideways, show a complete first choice and an intentional glimpse of another. Keep the scrolling affordance in its own lane. If the last content is near a fixed layer, include enough real scroll padding to bring it above that layer.

## Transfer exercise for seed inventory

This is a conceptual mobile screen for a community greenhouse. A volunteer opens a drawer, sees which seed packets still need a physical count, and records one count at a time. The layout uses compact operations, a numeric progress track and a dock for the active stock count.

- **Header and scope.** On a 375 px canvas, place the header at x = 16 with a small ink identity tile and “Seed inventory” at 24/24, weight 800. Use the greenhouse name as the supporting line. Add a trailing white filter circle. Under it, place a 343 px-wide drawer selector with “Drawer C” selected in ink. Only show actual drawer options.
- **Audit progress.** Open a 28 px radius white card with 16 px padding. Read “4 packets left” at about 28 px, then show “14 of 18 counted” with a 10 px track filled to 77.8% in deep sky. Put the count beside its track. Keep restock alerts close to the relevant inventory rows.
- **Work list.** Let the tall white board align to the 12 px edge. Stack inventory rows with name, last recorded count and target on common edges. A small peach tag can flag low stock and lime can mark a verified count when the user chooses to view completed entries. Show “To count” as the active filter so color and selection have separate jobs. If a volunteer selects a packet, use a white-tinted row and an ink disc with a check inside its group.
- **Action.** A dark 64 px dock names the chosen packet and holds a white 48 px “Record count” action. Its popover or sheet repeats the packet and drawer, groups last count and shelf target in a peach inset, and ends with one ink “Save count” button. Use a comfortably sized numeric input with a visible label and enough room for entry errors.
- **Finish the task.** When the active filter reaches zero results, show a small lime/check mark, “All packets counted” and “Show all” inside the board. The current drawer, audit total and path to the full inventory remain visible. The dock is relevant only while there is a selected item and action to take.

The layout preserves the cool shell, an ink selection/commit grammar, contextual pastels, numeric weights and a task-linked meter. It pairs the compact color treatment of the calendar with a persistent action only where the new workflow earns one. Its hierarchy can be checked from the named roles. Rendering would be needed to validate final text fit, tap targets, contrast, fold and optical spacing. [Validation evidence](ANALYSIS_EVIDENCE.md#transfer-exercise)
