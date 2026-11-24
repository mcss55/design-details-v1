# BR10 Business mobile UI/UX handoff

Act as the UI/UX designer for BR10 Business, a Flutter app for owners, managers, reception staff and employees operating a multi-branch business. Create original phone and tablet designs for the inventory below. Use the implementation plan for capability, data and workflow, then use the researched design DNA to set the visual hierarchy and interaction patterns. [Mobile implementation plan](MOBILE_DETAILS_PLAN.md) · [Master design prompt](MASTER_DESIGN_PROMPT.md)

## Screen count and design scope

The plan contains **77 unique `…Screen` identifiers**. The handoff specifies **82 screen-level design frames**. It adds the explicitly listed More tab, a proposed Profile and Account frame for the navigation destination, and one frame for each of the three booking wizard steps. Two named document viewers share a viewing pattern. Count the five tab roots once each. Use component variants for tabs inside a record, repeatable forms, sheets, banners, native handoffs, and changes in device, theme, state or language. [Navigation map and phase definitions](MOBILE_DETAILS_PLAN.md)

- **Phase 1 · 13 frames** covering 11 named screens, More and Profile and Account.
- **Phase 2 · 6 frames** covering Home and Catalog.
- **Phase 3 · 7 frames** covering Schedules and Calendar.
- **Phase 4 · 6 frames** covering 3 named screens and 3 booking stages.
- **Phase 5 · 10 frames** covering CRM and private documents.
- **Phase 6 · 16 frames** covering Finance.
- **Phase 7 · 6 frames** covering Packages and Dental.
- **Phase 8 · 11 frames** covering Inventory and POS.
- **Phase 9 · 7 frames** covering Booking Link, WhatsApp, Notifications, Subscription and AI.

Phases 1–6 are scoped for live BR10 workflows by the plan. Phases 7–9 use feature flags and sandbox data in design prototypes. Show the applicable availability state at the entry point and carry it through the flow. Treat Home Stories as an extension feature and keep the native WhatsApp message action on Appointment Detail distinct from branch-linked WhatsApp Cloud sessions. [Backend scope](MOBILE_DETAILS_PLAN.md#user-review-required)

## Visual and interaction rules

- **Surface and state.** Use lavender `#F1EEF6` as the default light canvas, white `#FFFFFF` for the main working surface and ink `#151515` for selection, decisive action and the strongest text. Use a visible check, label, shape or pattern with each semantic color. Apply lilac `#E8DCF8` with `#A46CE6`, peach `#FBE2CA` with `#EE9757`, sky `#CDEFF6` with `#3FBAD6`, and lime `#DFF3C6` with `#79B443` as pale fields with small, deeper marks. Keep one dominant object and one leading action per action zone. [Design DNA](DESIGN_DNA.md#color-and-surface-behavior) · [Design tokens](DESIGN_TOKENS.json)
- **Type and geometry.** Start with Plus Jakarta Sans, weights 400–800, and a verified system fallback for Russian and any missing glyphs. Use a tight 800-weight title near 24sp for operations or 30–32sp for a short welcome or outcome. Use 14–16sp readable row and form text, compact supporting labels, and aligned tabular figures for time, money, percentages and counts. Start with 16dp page gutters, 12dp at dense boards or docks, 28–32dp outer rounds, 16–22dp insets and 10–12dp dense cells. Use full pills and circles, hairlines within continuous surfaces and distinct floating elevation for nav, FABs and sheets. Treat reference CSS measurements as starting points for Flutter dp and sp. [Type and spacing](DESIGN_DNA.md#typography) · [Component patterns](COMPONENT_PATTERNS.md)
- **Scope and layout.** Keep active branch, date and filters close to the working plane. The phone shell has Home, Calendar, Appointments, Customers and More in a floating white capsule with an ink selection. At 600dp and above, move destinations to a rail. Use a second pane for a selected record, contextual sheet or live recap when the available width fits it. For example, keep the Calendar grid continuous beside Appointment Detail and keep payment totals visible beside denomination inputs. On phone, keep a dock only when it carries live context or commitment. Let sheets and keyboards leave the final field and action reachable within safe areas. [Navigation architecture](MOBILE_DETAILS_PLAN.md#navigation-architecture-mapped-to-analysismd--br10-api) · [Layout playbook](LAYOUT_PLAYBOOK.md)
- **Choose the composition from the job.** Use the BR10 Calendar's white working plane for boards, queues and lists. Use grouped selection, a close recap and a clear commit action for editors and booking. Use a brief result and a left-aligned white record for outcomes. Use a peach context inset, line-item rails and a perforation when a receipt or booking record benefits from that boundary. Draw quantities from the same data as their labels, tracks and segments. [Calendar reference](references/br10-calendar-viewport.png) · [Booking and dock reference](references/petal-booking-mobile-viewport.png) · [Record detail reference](references/br10-calendar-detail-sheet.png) · [Confirmation reference](references/petal-confirmation-rebrand-full.png)
- **Production states.** Design loading, empty, retryable failure, disabled with a reason, validation, submitting and success where the task warrants them. Keep recoveries in the working surface and carry branch, date or record context across any retry. For a version conflict, preserve the attempted change where useful, show the changed fields and offer a reload or explicit comparison. Gate financial values, mutations and private data on server capabilities and record state. Avoid embedding restricted content in previews, skeletons or prior-screen snapshots. [Protocol and permissions](MOBILE_DETAILS_PLAN.md#user-review-required) · [Verification](MOBILE_DETAILS_PLAN.md#manual-verification)
- **Accessibility and localization.** Make Azerbaijani (`az`) the primary design copy and verify `en`, `ru` and `tr`. Include diacritics, long names, Cyrillic and the manat symbol `₼`. Present times in the branch time zone and amounts in AZN with the correct sign and exact payable value. Use meaningful names for icon actions, focus indication, a 48dp target for primary touch controls, and readable contrast on actual surfaces. Aim for at least 4.5:1 for normal text. Check reduced motion and all three font settings. Give color-coded, draggable and visually dense controls a labeled non-gesture path. [Design quality checklist](DESIGN_QUALITY_CHECKLIST.md) · [Reference limitations](ANALYSIS_EVIDENCE.md#differences-and-source-flaws)
- **Artwork and theme.** Give optional imagery a purpose on Welcome or in a business-type choice, using original BR10 assets or licensed placeholders. Use small icons, rails and proportions around operational data. For dark and alternate presets, keep canvas, elevated surface, text, selected control and semantic accent roles distinct. Use strong foreground contrast and persistent selection cues. The evidence demonstrates the light palette. Develop and check dark and alternate preset treatments as design extensions. [Design evidence](ANALYSIS_EVIDENCE.md#scope-and-remaining-uncertainty)

## Phase 1 · Access, workspace and preferences

The plan specifies email and password access, four-step workspace setup, capability-based administration and device-local appearance. The navigation map supplies More and Profile and Account. [Plan lines 83–103 and 267–271](MOBILE_DETAILS_PLAN.md)

### 01. Welcome · `WelcomeScreen`

Use a short BR10 identity moment on the lavender field, with a bounded original visual if it explains the product. Place the current slogan in tight 800-weight type, with a stable ink **Sign in** action and white **Create account** action. Keep a complete single message in reduced motion. Give session restoration a quiet progress treatment while the app resolves the next destination.

### 02. Sign in · `LoginScreen`

Place labeled email and password fields in one white panel under a compact title. Make password visibility a named utility and anchor **Sign in** to the form. Show field validation, malformed or rejected credentials, network retry and in-progress submission without clearing the email. Use email as the account identifier.

### 03. Register · `RegisterScreen`

Use the same auth panel with name, email and password in reading order. Validate 2–255 characters for the name and at least 12 characters with a maximum of 72 UTF-8 bytes for the password. The live identity service validates characters and bytes separately. Group feedback under the affected fields, with **Create account** as the ink action. Carry successful registration directly into the workspace guard and onboarding when needed.

### 04. Business type · `BusinessTypeScreen`

Start the four-step setup with roomy white choice rows or wrapped tiles for Barber, Beauty Salon, Dental, Spa and Other. Use quiet lilac or sky icon insets. Use an ink check and an explicit selected state. Give **Continue** a stable position with visible progress through the wizard, and preserve the choice when navigating back.

### 05. Team size · `TeamSizeScreen`

Use one white choice surface with Solo, Small, Growing and Large. Keep descriptions concise and expose the choice by label and check. Align the step indicator and **Continue** with Business Type. Preserve the selection when moving between steps.

### 06. Business details · `BusinessDetailScreen`

Make the white form the focus. Group name and slug with a restrained link preview or availability hint linked to the slug field. Present AZN as the specified currency. Keep **Continue** near the consequence and show invalid or unavailable slug inline while retaining edits.

### 07. First branch · `FirstBranchScreen`

Group branch name, city and address, then contact phone and time zone. Use a small peach context inset for the time zone when it clarifies the branch schedule. Validate E.164 phone and require an explicit IANA time-zone choice. **Create business** commits the wizard. Show pending, field failures and a successful path into Home with the new branch active.

### 08. Branches · `BranchesScreen`

Use a white directory with branch name and location on aligned rows. Keep active and archived status visible as text with small muted chips. Give **Add branch** the main action and open create or edit in a form surface that retains branch context. Treat archive and restore as labeled, permission-aware actions with version conflict recovery.

### 09. Team members · `TeamMembersScreen`

Use one roster with name, membership and role aligned on repeatable edges. Put role and capability changes in a white disclosure or detail pane that identifies the member and scope. Feature the applicable invite or edit action by capability. Show read-only and empty roster states, and keep role labels distinct from effective permissions.

### 10. Invitations · `InvitationsScreen`

Use a segmented selection for sent business invitations and invitations addressed to the signed-in user. Show organization, role and pending state in quiet rows. Emphasize **Invite** in the sent view and **Accept** on an actionable inbound invitation. Support cancel, decline and expired or already-resolved states with the relevant context intact.

### 11. Appearance · `ThemeScreen`

Keep a live preview of a selected pill, white or elevated surface, status chip and sample text above the settings. Group all 18 presets by the plan's appearance model, with names, visible selection and Small, Medium and Large text examples. Apply changes locally and preview light and dark contrast. Confirm the complete preset roster and mapping against `theme_presets.dart` when available. The plan states 18 and leaves some entries unnamed.

### 12. More · Navigation tab

Use a compact workspace header and a grouped white list for Finance, Catalog, Schedules, Team and Preferences, with eligible extension destinations nearby. Lead each row with a useful icon, short title and disclosure affordance. Keep More selected in the shell. Use capability-aware entries and an understandable availability state for sandbox features.

### 13. Profile and account · Navigation destination

Use a white identity area with name and email, then a short settings list for account information, appearance, language and sign-out where appropriate. Keep device-local settings visually grouped. Use a dedicated confirmation for sign-out and avoid emphasizing it as the first action on the page. Account fields and edit actions follow the available identity contract.

Supporting frames include the business and branch switcher, Language picker (`az`, `en`, `ru`, `tr`), invitation and role editor, branch editor, archive and restore confirmations and sign-out dialog. Use a checked white chooser for short selections and a keyboard-safe form for longer edits. The switcher shows both the business and the resulting active branch.

## Phase 2 · Home and catalog

Use the branch header and operational working plane from BR10 Calendar. Reserve larger pastel groupings for a catalog choice or meaningful dashboard summary. [Plan lines 275–286](MOBILE_DETAILS_PLAN.md) · [List composition](LAYOUT_PLAYBOOK.md#pattern-d--browse-a-list-or-compare-a-collection)

### 14. Home · `MainScreen`

Lead with business and active branch, then a white working surface for today's upcoming appointments. Use quiet groups for Overview, Finance and service shortcuts, and show Stories with the applicable extension flag. Put one quick booking FAB above the bottom nav and keep adjacent actions secondary. Support refresh, a quiet day, device-local section visibility and gated Finance without leaving a hole in the layout.

### 15. Categories · `CategoriesScreen`

Show one white ordered list with aligned names and handles. Use a pale lilac category accent where it distinguishes the grouping. Lead with **Add category** in browse mode and **Save order** when reordering. Provide accessible move-up and move-down controls, save and retry states, and a white create or edit sheet.

### 16. Employees · `EmployeesScreen`

Show an employee roster with avatar or initials, name, branch and active status. Keep branch assignments and state readable without dominating the row. Use **Add employee** for permitted users and route each row to Employee Detail. At tablet width keep the roster visible beside the selected employee where space permits.

### 17. Employee detail · `EmployeeDetailScreen`

Anchor the page with a compact identity and active status. Group General, Branches, Commission, Working Hours link and Online into the same detail anatomy. Make assigned branches and commission percentages easy to scan. Use **Save** in edit mode, label unavailable online controls by availability, and link Working Hours to the existing schedule screen.

### 18. Services · `ServicesScreen`

Place search and active or archived selection above a shared category-grouped list. Put service name and duration on consistent edges, with a right-aligned price or meaningful price-type label. Use pale group accents and keep the primary **Add service** action reachable. Differentiate empty catalog from filtered no results and preserve scroll when returning from an editor.

### 19. Service editor · `ServiceEditorScreen`

Give core details, pricing and duration, online availability, translations and employee overrides distinct sections inside a white form. Expose Fixed, Range, From, Free and No price as meaningful selector states and show only their relevant amount fields. Validate 5–1440 minutes, price range and the online requirement for at least one employee. Show `az`, `en`, `ru`, `tr` translation tabs and clearly marked inherited or overridden employee price, duration and commission. Keep **Save service** and the exact resulting price in view on supported layouts.

Supporting frames include Home section visibility, category create and edit, employee create and edit states, and Single, Multi and Batch commission rule preview and apply. Put scope, proposed differences and affected count in the preview. Make Apply enabled once the changes are ready and keep the result tied to the same scope.

## Phase 3 · Schedules and calendar

Use the BR10 operational reference as the closest visual evidence. Preserve the plan's load bands of green below 40%, orange from 40% to below 75%, and red at 75% or above. Use contrast-tested marks, percentages, labels and a separate selection outline. The reference establishes the matrix and its selection cues. The plan governs the red high-load band. [Plan lines 290–305](MOBILE_DETAILS_PLAN.md) · [Week reference](references/br10-calendar-week.png)

### 20. Branch working hours · `WorkingHoursScreen`

Show the selected branch and a seven-day white schedule editor. Give hours, nested breaks and online windows legible aligned times. Use a small sky accent for online settings and group date-specific overrides separately. Make **Save hours** reachable after a long week. Show closed days, maximum four non-overlapping windows per day, breaks contained within their windows and the shared bounds for lead minutes and overrides where configured.

### 21. Employee schedule · `EmployeeScheduleScreen`

Use the branch-hours layout with employee identity in the scope header. Give **Inherit branch hours** a clear switch and render inherited values in a distinct readable state. Surface editable personal windows, breaks, online disablement, lead minutes of 0–240 and up to 366 date overrides where applicable. Identify overridden days and keep **Save schedule** beside the effective scope.

### 22. Blocked time · `BlockedTimeScreen`

Make branch, employee, local date, start and end the focal group in a peach time inset. Place reason and **Block time** below. Show unavailable or ambiguous local times with clear daylight-saving resolution choices. Carry the same patterned block and reason label back to the calendar and preserve inputs on a conflict.

### 23. Blocked time series · `BlockedTimeSeriesScreen`

Use a compact weekday selector, time controls and a start and end range supporting 1–91 days. Make the resulting active range legible before **Save series**. For an existing rule, display occurrences and exceptions in a dated list. Give move, restore, reattach and cancel distinct scopes and quote the selected occurrence or series in the confirmation.

### 24. Calendar · `CalendarScreen`

Place branch, compact white date controls, day or seven-day selection and status chips above the widest white board. Align the roster and time grid, starting from a 38dp time gutter and 72dp per hour as reference geometry. Page staff in 3–4 columns on phones where labels fit, use capacity-driven paging on tablets and avoid an orphan single column. Use lilac for booked, sky for started, lime for completed, and a labeled muted dashed state for cancelled. Distinguish off-hours, breaks, blocked and free areas by pattern. Show a labeled peach now rule, load rings and a legible weekly percentage matrix. Open clustered events in a detail picker and offer a labeled Reschedule action alongside dragging. Design move confirmation, no-op, failure, empty staff, busy overlap and narrow-grid variants. [Day grid](references/br10-calendar-full.png) · [Empty board](references/br10-calendar-empty.png)

### 25. Calendar settings · `CalendarSettingsScreen`

Use a white settings surface with ink selection for 15, 30 and 60 minute slot granularity and small, medium and large calendar type. Pair status swatches with names and a small sample event. Give **Only working employees** a labeled switch and show an accurate preview or effective value. Check every custom accent against the actual event background. [Display sheet](references/br10-calendar-display-sheet.png)

### 26. Calendar resources · `CalendarResourcesScreen`

Use a shared staff list with avatar or initials, name, visible state and an aligned reorder affordance. Keep visibility and order as independent controls. Identify the arrangement as personal to this device. Provide accessible move actions and a **Restore defaults** path, including recovery when all employees are hidden. [Staff filter reference](references/br10-calendar-filters-sheet.png)

Supporting frames include month selection, staff and status filters, overlap selection, availability for one service or a cart, date overrides, and drag confirmation. Use aligned dates and explicit time windows. Keep drag and button-driven rescheduling behavior equivalent. [Month sheet](references/br10-calendar-month-sheet.png)

## Phase 4 · Appointments and booking

Use one record language from Calendar to appointment history, booking and checkout. The booking review sits with the third stage in this brief. The slot stage uses availability and preview feedback before review. [Plan lines 309–325](MOBILE_DETAILS_PLAN.md) · [Create reference](references/br10-calendar-create-sheet.png) · [Detail reference](references/br10-calendar-detail-sheet.png)

### 27. Appointments · `AppointmentsScreen`

Use search, date and staff filters above one white date-grouped queue. Offer Active, Booked, Started, Completed and Cancelled as localized filter labels. The live scheduling contract maps Started and Cancelled to `START` and `CANCEL`. Align appointment time, customer, service, employee and textual status so a busy list can be scanned. Keep **New appointment** near the queue and expose loading more, filter reset and no results.

### 28. Appointment detail · `AppointmentScreen`

Use a white record with status and booking ID, customer, a peach date and staff inset, then ordered service lines with rails and tabular amounts. Where duration is useful, size segments from the real lines. Let the current status and capability determine whether **Start**, **Checkout** or **View receipt** leads. Checkout also requires the scheduled start time to have arrived. Keep move, line edit, reassignment, cancellation, history and native WhatsApp in contextual secondary actions. Show booked-only line editing, changed snapshots after reassignment, checkout quote regeneration and version conflicts. Reuse the same hierarchy for Calendar sheet and tablet side pane entry.

### 29. Appointment history · `AppointmentHistoryScreen`

Use one white timeline with time, actor or permitted role, change label and before and after values on clear axes. Expand a long revision on demand. Design a full manager view and a restricted reception or employee projection with protected data absent from the layout. Keep empty history tied to the appointment reference.

### 30. Booking · Service cart

Begin with branch and dated context if launched from Calendar. Put categorized service choices and selected quantities in a single well-organized white area with lilac group cues and ink checks. Keep the cart and total duration or estimated amount in a short recap. **Choose time** advances when the cart is valid. Explain unavailable items in place and preserve the cart if the user backs out of the next step.

### 31. Booking · Employee and time

Keep the cart recap visible near a staff chooser and bounded slot picker. A sky availability panel can show a common-baseline measure when there is real capacity data. Use ink selection for staff and slot, identify branch time zone, and keep selected duration visible. Show no slots, a slot taken after preview, and changes to time or price. Offer a date or employee change that preserves the cart.

### 32. Booking · Customer and review

Use a focused customer search and selection with a linked create-customer entry when allowed. Confirm the branch, employee, local date and time, customer, ordered services, duration and amount in a compact white recap with peach timing context. **Create appointment** submits once, with a visible pending state and a clear path to the saved record. Preserve entered choices on a retryable failure and return the user to the affected field when availability changes.

Supporting frames include appointment filters, move or reschedule, booked service-line edit, employee reassignment with before and after snapshot, localized cancellation reason, confirmation, and native WhatsApp selection or unavailable fallback. Use a close button and restored focus for each overlay.

## Phase 5 · Customers, private files and CSV jobs

Keep customer identity and active scope stable across the CRM tabs. Treat the financial and private file views as capability-scoped work surfaces. [Plan lines 329–344](MOBILE_DETAILS_PLAN.md)

### 33. Customers · `CustomersScreen`

Give search, branch, tag and lifecycle filters a compact header and put paged results in one white directory. Align name, useful contact metadata and tag or state cues. **Add customer** leads in browse mode. Multi-select replaces it with a contextual bulk action bar showing selection count and allowed tag, branch, archive or restore actions.

### 34. Customer detail · `CustomerDetailScreen`

Use a compact name and permitted contact summary above tabs for Details, Appointments, Finance Timeline or Statement, Files and Settings. In each tab, let its one main object fill a shared white area. Keep the customer, branch and relevant record state visible during navigation and adapt long tab names with a scrollable tab row or suitable alternate picker. Apply file and finance access to both content and deep links.

### 35. Add or edit customer · `AddEditCustomerScreen`

Use a white form with identity and contact groups. Place device Contacts import next to contact fields and support permission denial, unavailable contacts and manual entry. Use **Save customer** as the clear commitment. Indicate validation near the relevant field and give a possible duplicate a route to review while preserving form values.

### 36. Customer tags · `CustomerTagsScreen`

Use a tag list with a light swatch, legible name and available edit action. Use the documented palette for color choices and a check and named label for the active swatch. Put **Add tag** above the list or in the action zone. Preview the label on its actual fill, and expose affected customers or selection count in batch assignment.

### 37. Merge customers · `CustomerMergeScreen`

Make source and destination records unmistakable. On phone stack aligned field comparisons. On tablet allow a side-by-side preview when values stay readable. Use an ink choice, a labeled consequence and a white preview with the resulting customer record. Make the final **Merge customers** action explicit and show stale duplicate, conflict and completed states.

### 38. Customer settings · `CustomerSettingsScreen`

Group communication preferences as labeled switch rows. Give the booking ban its own consequence, reason input and visible on/off state. Gate editing with `customers:write` and keep shown settings readable in view mode. Use **Save settings** for changes, including validation and recovery when a reason is needed.

### 39. Customer documents · `CustomerDocumentsScreen`

Lead with the customer's file list and a labeled quota bar for used, reserved and available bytes. Show upload progress and resumption, then pending, waiting, scanning, failed scan, clean or rejected states with text and icon. Keep private previews and opening behind scan state and permissions. Surface manager-only retry and clean-file download where available, with expired-ticket recovery. Include a removal reason and an accessible file audit timeline.

### 40. Image viewer · `ImageViewScreen`

Use a calm viewing plane, visible close or back, file name and zoom or pan support. Make a labeled zoom and reset path available alongside gestures. Preserve privacy and keep actions scoped to a valid download or allowed native share. Show image loading, an expired ticket or an unreadable image, with return to the same file row.

### 41. File viewer · `FilesViewerScreen`

Share a viewing shell with the image viewer and give PDFs or supported documents title, visible page position, readable zoom and available native open controls. Show progress for retrieval and plain text for ticket expiry, unsupported file or viewer failure. Maintain access state when returning from the OS viewer.

### 42. Customer CSV jobs · `CustomerCsvJobsScreen`

Use a white job list and a clear import or bulk update action. Show upload and staging, preview counts, conflict review, apply, results and history in a consistent job-detail sequence. Label accepted, rejected and unresolved rows and keep affected counts visible before **Apply**. Expose cancel where allowed and retain the job when showing partial completion or a retryable issue.

Supporting frames include customer filters and bulk actions, tag edit, contact permission or native picker, file pick and upload progress, rescan and removal, audit history, CSV row conflicts and final apply review. Keep customer and branch scope visible across every step.

## Phase 6 · Finance and checkout

Give finance the same operational shell and a strong, right-aligned numeric axis. Keep AZN amounts, branch, date range and document state explicit. Place effects on payable totals and balances next to the relevant choice. [Plan lines 348–371](MOBILE_DETAILS_PLAN.md) · [Outcome layout](LAYOUT_PLAYBOOK.md#pattern-b--resolve-and-orient)

### 43. Finance · `FinanceScreen`

Use a compact branch header and one grouped white menu for Overview, Registers and Entries, Categories and Totals, Receivables, Commissions and Customer Finance. Make the overview entry easy to find and keep adjacent entries quiet. Show permitted destinations with accessible names and reflect actual capabilities when the branch or workspace changes.

### 44. Finance overview · `FinanceDashboardScreen`

Lead with a branch and date filter, then one principal summary and its supporting chart or measures. Use tabular signed amounts, an explicit time scale, labeled comparison groups and accessible numeric chart details. Reserve pastel for meaningful series. Show loading and a real zero-activity view with the selected range intact, and distinguish missing data from a measured zero.

### 45. Quote · `QuoteScreen`

Use a white itemized record with appointment identity, service quantities and exact total due. Make agreed line totals editable for Range, From and No price services within the supported bounds. Show Fixed and Free totals as resolved values. Place transaction context in a pale peach inset. The plan calls for discounts and the current quote input has no generic discount field. Confirm a supported source before exposing that control. Show the 15-minute quote expiry and a refresh path. **Continue to checkout** leads when the quote is current.

### 46. Checkout · `CheckoutScreen`

Use the quote's anatomy to review customer, branch, service lines and due amount before choosing how to record payment. Make payment or balance information visible in the main white surface and advance to the single or split payment editor with the selected quote. Show stale quote recovery, a pending result and the transition to Receipt when the command resolves.

### 47. Payment · `PaymentScreen`

Keep amount due and the allocated or remaining amount visible above the inputs. Use an ink single or split selection, explicit Cash or Card labels and eligible active same-branch registers. Default to full payment and require an exact allocation. Expose deliberate partial payment with the resulting receivable and reject overpayment. **Record payment** submits once. If transport times out, show a checking state until command status confirms the result or permits recovery. Treat Card as a register payment method recorded by staff.

### 48. Receipt · `ReceiptScreen`

Start with a brief labeled outcome and give the white internal receipt most of the space. Show the traceable document ID, service lines, amount paid, register breakdown and remaining balance when applicable. Keep original checkout and current settlement or later activity in distinct groups with a visible snapshot time. Use a perforation where it separates the accounting section. Give authorized internal **Share** or **Export** priority and keep Print accessible. Provide `az` and `en` document choices and a recoverable rendering or export error.

### 49. Receivables · `ReceivablesScreen`

Use a white debt queue with customer or appointment, branch context, due and open amounts on common axes. Show a distinct settled state and make **Record collection** the selected record's main action. The collection form repeats the current open amount, register and proposed remaining balance before confirmation. Refresh the exact balance after success or conflict.

### 50. Cash registers · `CashRegistersScreen`

Group register rows by branch scope with names, Cash or Card and active or archived state. Use **Add register** and a focused create or edit form. Open the statement from its row. Make changes to archived registers explicit and keep archived registers out of eligible payment selection.

### 51. Register statement · `RegisterStatementScreen`

Anchor the white ledger with register, branch, time range and category filter. Use fixed trailing columns or a stacked signed value on narrow screens. Show dated entries and available balances with a stable sign convention. Tuck details and authorized reversal behind the entry. Preserve the filter when returning from an entry and distinguish empty activity from a failed load.

### 52. Finance categories · `FinanceCategoriesScreen`

Use a shared list with category name and its financial classification or state in compact metadata. Use **Add category** and a white create or edit form with a clearly visible type. Keep category selection, duplicate validation and the allowed actions consistent with Ledger Entry and Category Totals.

### 53. Category totals · `CategoryTotalsScreen`

Use filters close to one white comparison surface. Align category, signed total and any relevant grouping labels. Add a small baselined measure only if it supports comparison with the same numeric data. Keep the range visible in the export preview and expose **Export** with pending, empty result and recovery states.

### 54. Ledger entry · `LedgerEntryScreen`

Use an ink selector for Income, Expense and Transfer. Group amount, register, category and applicable metadata in one white form. In Transfer, label source and destination, and put their relationship beside the amount. **Post entry** commits the scoped form. For an existing entry, show the original record and effect in a labeled **Reverse entry** confirmation where permitted.

### 55. Commission directory · `CommissionDirectoryScreen`

Use an employee list with OPEN, SETTLED and ALL filters above it. Give due, paid or settled amounts a stable trailing edge and use a small labeled state mark. Open the selected employee's details from the row. Keep the scope and filter readable when the queue is empty.

### 56. Employee commissions · `EmployeeCommissionsScreen`

Anchor the page with employee and current commission balance. Follow with appointment-linked accrual, payout and return rows showing the permitted amount, status and branch context. Use **Record payout** as the strongest eligible action and return at the applicable payout. Keep statement access visible and explain an ineligible action beside the amount or record.

### 57. Commission statement · `CommissionStatementScreen`

Show employee and a date range capped at 31 days, followed by a white reconciliation block. Align opening, accrued, credited, paid, returned and closing amounts and make closing visually strongest. Preserve the arithmetic of opening plus accrued minus credited minus paid plus returned. Place matching ledger detail beneath and provide a recovery for invalid ranges or failed loads.

### 58. Customer finance · `CustomerFinanceScreen`

Use a directory or linked customer selection, then a shared customer-finance surface for current debt, timeline with running balance and statement. Show signed entries and totals on the same axis and enforce the 31-day statement range. Provide a preview and eligible actions for the JSON, HTML and CSV document variants. Keep customer, date range and document format visible through share or export failure.

**Finance sheets.** Refund shows the selected source and preview before commit. Bill Credit shows the proposed balance and the paid-commission floor where it constrains the amount. Commission Payout shows the eligible appointment, amount and resulting balance. Commission Return names the original payout and returnable amount. Give each sheet a labeled consequence, exact amounts, confirm, submitting and retry states. Use the same form anatomy for register and category editing and subsequent collections. [Plan lines 358–370](MOBILE_DETAILS_PLAN.md)

## Phase 7 · Packages and dental

Apply the same design language to feature-flagged sandbox data. Keep precise package calculations and tooth identifiers visible in the UI. [Plan lines 375–385](MOBILE_DETAILS_PLAN.md)

### 59. Packages · `PackagesScreen`

Use a white catalog with package name, applicable branch, price, expiry and textual status. Quiet lilac rails can group package types. Show status priority in the order Expired, Deactivated, Draft and Active. Emphasize **New package** for the authorized task and make the entry into package detail or sale clear.

### 60. New package · `NewPackageScreen`

Group identity, expiry or no expiry, service items and pricing on a white form. Align quantities and label the unit on each service line as sessions or minutes. Show the calculated total and a manual override with its current validity. When changed items invalidate the prior override, update the displayed total and communicate the change. Keep **Save package** with the recap.

### 61. Sell package · `SellPackageScreen`

Make the selected package and customer the anchor, with branch, expiry, price, amount paid or due, and the included items in a live recap. Use peach for transaction context and right-align money. Keep selection, validation and the final **Sell package** action visible. Use a brief outcome and a link to the durable package record after the sandbox sale.

### 62. Select package · `SelectPackageScreen`

Use one white chooser showing package name, status, valid dates and remaining quantity by service and unit. Use precise text to explain expired, unavailable or depleted choices. Use an ink check for the active eligible record and carry the selection and usage details to the originating booking.

### 63. Package detail · `PackageDetailScreen`

Keep owner, package and state stable above Info, Usage and Payments. Use a compact white record for expiry and price, labeled service-usage meters for sessions or minutes, and signed payment rows. Show total, used and remaining values explicitly. Derive the package usage limit from the minimum across items and flag over-limit values in text if present.

### 64. Dental plan · `DentalPlanScreen`

Let a white FDI chart lead. Provide an explicit permanent 32 or primary 20 selector, stable quadrant order, visible tooth numbers and ink outlines or checks for selected teeth. Preserve correct anatomical IDs in the accessible list and display chart orientation. Pair the chart with a treatment row editor for chosen teeth, a service and notes. **Add treatment** validates tooth and service selection. Keep edit and delete scope explicit and show a list path when chart cells cannot meet touch or text-size needs.

Supporting presentations include service and package selectors, sale confirmation, and the customer's Dental tab. Let the tab summarize treatments and open the existing chart screen. Reuse accurate tooth IDs and time or usage units throughout.

## Phase 8 · Inventory and point of sale

Use an operational plane and aligned quantity or monetary lanes. Keep whole packs and measures explicit in every preview, especially for technical cards and product usage. [Plan lines 389–395](MOBILE_DETAILS_PLAN.md) · [Inventory layout example](LAYOUT_PLAYBOOK.md#transfer-exercise-for-seed-inventory)

### 65. Inventory · `InventoryScreen`

Use the branch scope and a white hub for Products, Stock, Suppliers, Supplies, Technical Cards and Sales. Put the most relevant inventory condition or destination first and use a short label and disclosure on each row. Keep sandbox availability visible to users who reach an extension entry.

### 66. Products · `ProductsScreen`

Use search and barcode lookup above a grouped white catalog. Put product or SKU in the leading lane and sale price, availability and unit on stable edges. Keep **Add product** and the scanner action distinct. Design camera permission, recognized product, no match and manual lookup so a scan has a complete path back to the list or current task.

### 67. Stock · `StockScreen`

Show branch-scoped on-hand stock in a white comparison list with clear sign and unit. Pair low or out-of-stock labels with small state markers. Expose received, sold, used and returned counts within row detail when available. Keep boxes and fractional measures readable together, and use any threshold bar with its defined baseline and label.

### 68. Suppliers · `SuppliersScreen`

Use a white supplier directory with name, permitted contact details and clear row disclosure. Keep supplier identity and branch context during add or edit and when linking into supplies. Use a quiet empty state offering the relevant create action. Apply consistent labels to tax ID and contact details in the supplier record.

### 69. Supplies · `SuppliesScreen`

Use a scope and status filter above rows showing supplier, invoice reference, process date, quantity or amount and labeled status. Emphasize **New supply**. For an existing supply, expose eligible draft, approve and return actions in its context, with clear progress and recorded outcomes.

### 70. New supply · `NewSupplyScreen`

Use a white form for supplier, branch, invoice and date, then a product line editor. Align pack quantities, measurement units and costs, and keep the whole-box supplier summary traceable to the inputs. Separate **Save draft** and **Approve** by consequence and show a transaction review before approval or return.

### 71. Technical cards · `TechnicalCardsScreen`

Show service-linked material plans in a white list, with linked service and concise product or measure summary. Use a light lilac marker for grouping and aligned labels for consumption quantities. Put **New technical card** near the list and preserve the scope when returning from an edit.

### 72. New technical card · `NewTechnicalCardScreen`

Give linked services and consumable lines their own groups. Show product, measure used, available unit and derived cost or reconciliation where applicable. Explain missing measures or invalid quantities at the line. Keep the total and **Save card** near the result, with the relationships intact when editing template or service choices.

### 73. Sales and usage · `SalesScreen`

Put Sale and Product usage in a labeled selection group. Align dated transaction, branch, associated person and amount or quantity in a white list. Label the mode on rows that share a combined view. Set **New sale** or **Record usage** to match the active task and keep search, status and empty states in that context.

### 74. New sale or usage · `NewSalesScreen`

Use one form structure with visibly distinct Sale and Product usage modes. For sales, show product quantities, payment summary and any applicable adjustments. For material use, show measure and unit, applicable employee or appointment, price basis and the derived split where available. Show available measure and validity per line. A usage line held as a fractional measure stays a measure in the recap, even when its whole-box count is zero. Keep a single mode-specific commit with the exact total or quantity.

### 75. Sale or usage detail · `SalesDetailsScreen`

Use a white record with reference, date, mode, branch, status, item rows and right-aligned totals. Use a receipt boundary for a completed sale and an accounting breakdown that keeps quantities and cost allocation explicit for product usage. Make the next permitted action obvious for each status and keep any reversal or return tied to its original line and record.

Supporting presentations include the barcode camera and manual fallback, product and supplier editors, stock item detail, approval and return review, and product or material pickers. Use repeatable input and record layouts for each.

## Phase 9 · Booking link, messaging, subscription and AI

Use capability- and feature-aware entry points. Preserve the difference between a sandbox result, a staged action and durable confirmation. [Plan lines 399–408](MOBILE_DETAILS_PLAN.md)

### 76. Online booking link · `OnlineBookingLinkScreen`

Anchor the screen with the branch and the shareable `link.<domain>/<slug>` URL, with named copy and share actions. Group interval, automatic availability, pending-time inclusion, customer note, uploads and builder steps into white form sections. Show the pending-time dependency by the disabled control and explain its prerequisite. Preview step order and effective settings before **Save settings**. Treat the customer-facing booking site as a linked destination.

### 77. WhatsApp sessions · `WhatsAppScreen`

Give each branch-linked session a readable name, branch association and label for Connected, Scan QR code, Starting, Failed, Stopped or Not found. A selected session opens a white connection surface with QR or code, instructions and the applicable next step. Distinguish restart, logout and remove by their consequences. Design unavailable, reconnecting and failed states and recovery by session.

### 78. Notifications · `NotificationsScreen`

Use one white chronological feed with type, concise subject, time and clearly readable unread state. Keep the related record path subject to capability and feature visibility. Lead a selected notification to the relevant existing surface. Show an empty inbox, load failure and unavailable linked record with a way back to the feed.

### 79. Notification settings · `NotificationsSettingsScreen`

Use grouped white switch lists with short channel and event descriptions. Keep preferences scoped to the correct recipient, role or branch. Where platform permission is required, make its state legible and show the available settings action. Preserve each toggle on a failed save or indicate exactly which one is still pending.

### 80. Subscription expired · `SubscriptionExpiredScreen`

Use a restrained outcome treatment, one clear expired status and a white panel identifying the affected business and plan state. Offer the available plan or account action and a stable permitted exit or workspace switch. Account for the navigation guard so that permitted account or plan actions stay reachable without cycling back. Use SubscriptionBanner for contextual warnings in the shared shell.

### 81. AI catalog assistant · `AiScreen`

Use a readable conversation plane with a keyboard-safe composer. Put a quiet progress label beside streaming text or activity and show Stop, Retry and completion distinctly. Explain the 12 MiB file and 20 MiB image limits at upload validation. Present staged service drafts and consequential tools in white cards with a batch count, changed fields and editable previews. Confirm and Cancel stay explicit and update to an actual sandbox outcome. Give stream errors, interrupted replies and expired confirmations stable recovery states.

### 82. AI history · `AiHistoryScreen`

Use a white history list with conversation title, timestamp and status where useful. Give **New conversation** a clear position and keep resume and any supported rename accessible from the selected row. Preserve the correct workspace during navigation and handle empty history, a removed thread and a retryable load failure.

Supporting presentations include the link builder preview, QR or code instructions, subscription banner, Home Stories and optional viewer when enabled, notification permission, and AI attachments, staged edits and tool confirmation. Give each supporting presentation the identity and context of the record it affects.

## First connected flow from the UI/UX designer

Use one synthetic booking at the Nərimanov branch in `Asia/Baku` on 24 November 2026, from 15:00 to 16:15. Aysel Rzayeva serves Günay Məmmədova. **Saç kəsimi** is 45 minutes at 45,00 ₼ and **Saç düzümü** is 30 minutes at 30,00 ₼. Carry 75 minutes and 75,00 ₼ across the experience. Record a complete split of 25,00 ₼ cash and 50,00 ₼ card.

1. **24 Calendar** shows the Nərimanov branch, date and filters above the board. A 75-minute event occupies 90dp at the 72dp per hour reference scale. Start booking at the eligible slot or with the FAB. Keep the chosen employee and time as context.
2. **30 Service cart** uses a white categorized list with lilac rails and ink checks. The recap shows two services, 75 minutes and the estimated 75,00 ₼.
3. **31 Employee and time** places staff above a sky availability panel. The selected slot reads 15:00–16:15. If the slot becomes unavailable, keep both services and return to eligible alternatives.
4. **32 Customer and review** places search above the recap. Show the branch, Aysel and time in a peach inset, confirm Günay, and commit once before opening the saved appointment.
5. **28 Appointment detail** shows the ID and status, appointment facts in peach and a duration strip segmented 60% and 40% to match the service lines. Make start and eligible checkout distinct next actions as the record moves through its lifecycle.
6. **45 Quote** renders the exact line amounts, 75,00 ₼ total and expiry from the server quote. Refreshing an expired quote preserves scope and makes changed totals visible.
7. **46 Checkout** reviews the customer, branch, current quote and amount due. The primary action opens the payment editor with that context intact.
8. **47 Payment** shows two active same-branch registers, 25,00 ₼ Cash, 50,00 ₼ Card and 0,00 ₼ remaining. Show overpayment or split mismatch beside the amounts and a checking state for an uncertain submission.
9. **48 Receipt** opens with a short confirmation, then shows the internal receipt, checkout reference, original split and separately labeled current settlement with snapshot time.

Use the tablet rail from 600dp. Add Calendar detail, booking recap or payment recap beside the main surface when each pane can hold its required content. Use scrollable detail and a safe-area recap dock on phones. [Calendar detail reference](references/br10-calendar-detail-sheet.png) · [Booking recap reference](references/petal-booking-mobile-summary-sheet.png) · [Confirmation record reference](references/petal-confirmation-rebrand-full.png)

## Design delivery and review

1. Produce one editable default phone frame per numbered entry, using realistic Azerbaijani content and consistent synthetic records across linked flows. Use stable frame names such as `24 Calendar` and label supporting states under their parent. Keep the two document viewers in a shared component family.
2. Start with the shell, Calendar day and week, booking, Appointment Detail, payment and receipt. Reuse those components across the remaining scope. Show a representative 375dp phone layout, a narrow or large-type state where needed and tablet layouts starting at 600dp. Show expanded Calendar, customer detail, checkout and inventory comparison where they benefit from the extra space.
3. Link the primary journeys. Cover register through branch creation, calendar booking through split payment and receipt, customer file upload through scan and view, and the extended flows behind their availability states. Include review, blocked states, failure and recovery for irreversible or high-consequence actions.
4. Annotate component and token roles, capability gates, branch and time context, input errors and what each quantity or state means. Include the keyboard, sheet close and focus behavior where it affects the design. Keep rendered localized strings and action names legible under long copy and large type.
5. Run the existing checklist on the rendered frames and interactive prototype. Check contrast and touch targets against the actual surfaces, scrolling through the final row, chart scale integrity, permissions, alternate themes and device sizes. Record any open assumptions and the frames they affect. [Design quality checklist](DESIGN_QUALITY_CHECKLIST.md)
