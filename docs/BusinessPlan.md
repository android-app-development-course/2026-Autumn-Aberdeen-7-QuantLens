# QuantLens App Business Plan

**Hong Kong Company Events. Original Sources. Your Own Research Notes.**

Mobile Smart Application Development  
Team 7 | English edition: 20 October 2026

**Team Leader:** 段博铧  
**Team Members:** 段博铧, 胡与同, 张胡文康, 陈钰龙

## 1. App Overview

QuantLens is a planned Android app for students and finance learners researching Hong Kong company events. It brings an event, its original source and a personal research note into one short workflow. The first release will be a free, connected pilot for invited users. Company information will arrive over the network; watchlists, notes and essential reading caches will stay on the device.

### A task worth getting right

A student reads a company's annual results between classes. Profit has risen, but is the change coming from its main business or a one-off item? The student opens the announcement, records the relevant passage and writes a question. A week later, new information appears. The student wants to find the earlier interpretation and add an observation without reconstructing the research from several apps.

This is the task QuantLens will support: find an event, check the evidence, save an interpretation and return to it later. It will support learning and personal research, without promising investment returns.

### Unique Selling Proposition

Our proposition is a small, dependable event-research workspace on a phone. Its value must be demonstrated through three connected design choices:

| Design choice | What a user should notice | How we will check it |
| --- | --- | --- |
| An event keeps its context | The source, publication time and linked note are available together. | Ask a participant to locate and explain the source of a recorded claim. |
| Original thinking remains visible | The first interpretation stays alongside dated follow-up observations. | Ask the participant to distinguish the original view from a later update. |
| A record survives the session | Saving, returning and reopening show the same content. | Reopen the note after leaving the screen and restarting the app. |

Existing products already provide notes and event information. We are proposing a particular workflow for learners, not claiming to have invented those features. Whether this arrangement is useful enough to justify another app is our main research question.

### Status and first-release boundary

The scope covers invited-user login, stock search, watchlists, event reading, linked notes, review and local export. Development will use Android Studio, Kotlin and Jetpack Compose. Cloud synchronization, push notifications, automated summaries and payments are later options.

No Android project, installable build or user-test results exist yet. Screens and technical diagrams in the first-phase report will be identified as prototypes and implementation plans.

## 2. Users and Market

### The initial audience

We will recruit adults who use Android, have an interest in company events and are willing to discuss a recent research task. Investment experience alone does not establish a need for this app. We need people who actually check sources, keep interpretations or want to revisit earlier notes.

| Segment | Relevant behaviour | Initial decision |
| --- | --- | --- |
| University students and finance learners | Read company events in short sessions; use several places for sources and notes. | Primary interview and prototype audience. The behaviour is a hypothesis to check. |
| Other learners and early-career users | Research outside a formal course and may have similar note-review needs. | Consider after the campus pilot shows repeat use. |
| Professional or frequent traders | Require extensive coverage, sophisticated tools or real-time execution. | Outside the first-release service scope. |

Our illustrative persona is an adult Android-using student following a few Hong Kong companies. They read annual results before a class discussion and want to recall why they questioned a figure. This is a design scenario, not a completed interview finding.

### Market context, with a clear limit

The IFEC Retail Investor Study 2025 reports that 88% of surveyed stock investors used social media for stock-investment information. The stock-investor base was 913; fieldwork ran from 2 to 26 July 2025, and the report was published in February 2026 [10]. This supports examining information-checking habits. It does not establish demand among students or willingness to install QuantLens.

### A reachable first market

Our immediate opportunity is a small campus research group that the team can recruit and support directly. The 10-20-person pilot is a capacity choice, not an estimate of market size or a sales forecast. We will report actual eligible invitations and participation before estimating a wider reachable audience. A large investor population would not, by itself, make a student research app viable.

<!-- pagebreak -->

### Alternatives users can already choose

The comparison below uses official product descriptions. It separates existing capabilities from the workflow we still need to test.

| Alternative | Verified relevant capability | Question for our user research |
| --- | --- | --- |
| TradingView | Charting and analysis tools, plus text notes that can be associated with symbols [1, 11]. | Would an event-linked source and a dated follow-up record improve this particular learning task? |
| Tiger Trade | Investment tools and topic subscriptions that bring together news around major events [2]. | Would participants choose a separate, smaller research workspace alongside their existing tools? |
| HKEXnews plus a separate notes app | Access to issuer announcements, combined with the user's chosen note-taking workflow [3]. | Does reducing source-to-note switching help enough to justify installation and setup? |

TradingView's notes and Tiger Trade's event-related features mean that “notes” and “event tracking” are insufficient claims of originality. Our comparison will concern a specific task: tracing a claim to a source, keeping the original interpretation and finding it again. We have not established that competitors cannot support that task.

### What could prevent adoption?

Users may prefer familiar, free tools. Installing an APK and signing in add effort. Android-only access excludes other devices, and the initial lack of cloud synchronization makes local export important. Limited event coverage could also make the app irrelevant to a participant's interests. Interviews and the pilot must test these objections directly.

### Research questions and evidence

Five planned interviews will ask participants to describe their most recent company-research task: what triggered it, which sources they checked, where they wrote their view, whether they later found it again and what would justify changing tools. We will ask for concrete examples rather than general enthusiasm for an app idea.

We will keep three kinds of evidence separate: published facts with a source and date; planning assumptions such as recruitment capacity; and user hypotheses awaiting observation. Findings will retain anonymous participant identifiers and the question or task that produced them. A small convenience sample will guide this pilot; it will not represent all students or Hong Kong investors.

## 3. Product Plan

The main path is Watchlist to Stock to Event to Note. Users can also open an event from Events or an existing record from Notes. Saving must return to the screen that opened the editor, with the updated content available there.

| Module | First-release scope | Acceptance focus |
| --- | --- | --- |
| Invited-user login | Team-issued accounts, loading and failure feedback, expiry and logout. | A valid server session permits access; invalid or expired credentials do not. |
| Watchlist and stock details | Search by name or code, follow companies and read a simple dated price trend. | Search, follow and reopen the same company without losing list context. |
| Event reading | Company-linked category, summary, publication time and original-source link. | Open a usable source and locate the relevant information. |
| Research notes | Interpretation, evidence reference, questions and follow-up points, linked to the event. | Save successfully and reopen the same record after restart. |
| Review and export | Preserve the original note, append dated observations and export locally. | Distinguish the earlier view from later observations and open the export. |

### Reading and writing on a phone

Four main destinations will organize the app: Watchlist, Events, Notes and Settings. Source and publication details will sit near the event content. A note entry point will remain easy to find. Charts will be simple enough to leave room for reading and writing.

Price changes will use signs or text as well as colour. Screens will accommodate system font scaling. Loading, an empty result, an unavailable cache and a failed request will have distinct messages. Lists should retain their position when users return. The note editor will explain a failed save and keep the input available.

### Intelligence where it helps

The first release will associate events with followed stocks and categories such as results, dividends and share repurchases. This is structured information organization. We will not present it as a trained prediction model or an implemented AI system.

Summaries must retain a traceable source for material facts. Automatic summarization will only be considered after factual checks are defined and tested. A later price movement will be an observation; it will not, on its own, establish that an event caused the movement.

## 4. Development and Operation

### Client and service responsibilities

The planned client uses Kotlin, Jetpack Compose, ViewModel and Room in a single MainActivity. Navigation Compose is the proposed navigation approach; it will be confirmed before application coding. Dependency versions will be checked together when the project is created.

Compose will display content and collect actions. ViewModel will manage screen state. Repository will expose a common interface to network and local data, and Room will hold durable personal records and essential caches. This follows the separation described in Android's offline-first guidance [4]. The client and service will agree on account ownership, stockId, eventId, noteId and time fields before modules are integrated.

The service will authenticate trial accounts and expose consistent stock and event endpoints over HTTPS. Service credentials will remain on the server. Server-side access checks are required even when the client hides a protected screen.

### Source quality and operating limits

HKEXnews provides an entry point for checking issuer announcements [3]. Data coverage, update frequency, display rights and costs must be verified with the selected suppliers. A public webpage is not evidence of unrestricted redistribution permission. The first dataset will be limited to a permitted selection that can still support the pilot task.

Publication time, market-data date and last successful refresh will be shown separately where relevant. A failed refresh will leave a clearly dated cache available. Original documents must open in a working browser or PDF reader; an untested link icon is not sufficient evidence of source access.

### Accounts, records and distribution

Personal records will be read according to account ownership. Logout and switching accounts will clear session-related screen state so previous-account records do not appear. Local records may remain on the device for their owner; no cloud backup is promised. Users will receive clear guidance on export, uninstalling and changing devices.

A signed APK will be distributed to invited participants only after readiness checks [5]. These cover external service access, real authentication, account isolation, save-and-reopen after restart, offline behaviour, original documents, export, installation and upgrades. Each issue will have an owner and a reproducible description. New invitations will pause for any observed record-loss or account-isolation failure.

## 5. Login, Navigation and Saving Notes

### Login and session states

Team-issued accounts will be verified by the server over HTTPS. Signed-out, validating, rejected and expired-session states require distinct feedback. First authentication requires connectivity; an expired session requires reauthentication. Self-service registration, password recovery and payments are outside the first release.

| Trigger | Destination or return behaviour | What the team must verify |
| --- | --- | --- |
| Login succeeds | Open Watchlist and remove the login flow. | Back does not reopen Login. |
| Open a stock, event or note | Pass the relevant minimal identifier, then load details [6]. | The destination displays the requested record, including after recreation. |
| Save a note | Persist first, then return to the actual caller. | Opening from Event returns to that Event; opening from Notes returns to Notes. |
| Back with unsaved edits | Offer save and return, discard, or continue editing. | Toolbar Back and system Back follow the same rule. |
| Logout | Open Login and clear business-screen history. | Back cannot reveal an authenticated screen or previous-account state. |

### Explain the stack, not just the arrow

The proposed design uses navigate to enter a destination, popBackStack to return and popUpTo to remove unwanted history [7]. Internal screens share one Activity; startActivity is not the internal navigation mechanism. Bottom-navigation behaviour will be checked separately so tab changes do not create repeated copies of the same screen.

Saving must finish successfully in Room before a return action. If it fails, the editor stays open and retains the input. Event details and Notes will observe the same stored records, so they can display the new content after returning.

ViewModel manages UI state; it does not replace durable storage. Temporary input and list position may use rememberSaveable or SavedStateHandle as appropriate [8]. Passwords will not enter restored UI state. A one-time noteId result may notify the caller and must be cleared after consumption [9]; the database remains the content source. Kotlin's return only exits a function and does not navigate between screens.

## 6. Marketing and Validation

### One invitation, one understandable task

We will introduce the pilot through a concrete request: “Try checking one company event, save your interpretation, and tell us where the process breaks down.” The first release will be free. Invitations will explain the account arrangement, local records and export, observation period and voluntary participation. They will not promise financial returns.

The outreach scenario below allows up to 30 unique invitations. These are work allocations, not expected conversion rates or confirmed access to organizations. Contacts will be deduplicated and assigned to their first recruitment channel.

| Channel and owner | Planned action and capacity | Constraint and fallback |
| --- | --- | --- |
| Classmates - 胡与同 | Up to 12 individual invitations using the shared task description. | Confirm Android eligibility and interest; record refusals without pressure. |
| Study groups or societies - 张胡文康 | Up to 12 invitations through an organizer-approved message and short demonstration. | No partnership is assumed. Without permission, use individual contacts instead. |
| Voluntary referrals - 陈钰龙 | Up to 6 invitations referred by willing participants. | Referrals may not occur. Expand direct outreach only after reviewing capacity. |

段博铧 will coordinate accounts, onboarding and the shared issue queue. All four members will support recruitment and review effort weekly, so channel ownership does not assign all outreach work to one person. There is no paid advertising in this pilot.

### Order of work and capacity

Research days 1-3 will cover five interviews; days 4-7 will cover five prototype sessions and revisions. These are relative work windows to arrange with participants. The first-phase report on 21 October presents the plan; it is not an app-release commitment.

Pilot day P0 starts only after the build, source permissions and readiness checks are complete. P1-3 will onboard an initial ten users. P4-7 will review task failures and support effort. Expansion up to twenty concurrent invited accounts will occur in P8-14 only if no unresolved critical record or account issue remains and the team can provide support. Each enrolled participant needs a full seven-day follow-up window, even if this extends beyond P14.

If outreach produces fewer than ten eligible consenting users in seven days, we will review the message and channel, then agree a further seven-day window or report the smaller cohort. We will not replace missing participation with assumed results. Interviews, prototype sessions and the pilot may include the same people; their counts must not be added as unique users.

<!-- pagebreak -->

### Task and measurement definitions

The task is to log in, find a specified company event, verify its source, save a linked note, return and reopen it. Verification means identifying the issuer, publication date and location of a relevant fact in the original document. Opening a link alone does not count. In the live build, reopening after app restart checks persistence.

Login time will be recorded separately. For the remaining workflow, the clock starts at the assigned starting screen and ends when the reopened note is visible. All task starters stay in the denominator, including failures and withdrawals during the task. Moderator assistance will be recorded and will exclude a run from independent completion.

| Measure | Provisional decision rule | Interpretation |
| --- | --- | --- |
| Prototype task completion | At least 4 of 5 participants complete the designed flow without help. | A usability check; it cannot prove database persistence. |
| Live task completion | At least 8 of the initial 10 starters verify the source and save, return and reopen after restart without help. | If unmet, fix the failed steps before expanding invitations. |
| Record and account integrity | No observed record-loss or wrong-account disclosure in the tested cases. | Any such failure pauses invitations until a fix is retested. This is not a claim of zero future risk. |
| Voluntary seven-day return | Aim for at least 3 of 10 fully observed users to return voluntarily. | A planning threshold, not an industry benchmark or proof of demand. |

A voluntary return is a later session more than 24 and no more than 168 hours after onboarding, without a reminder or support request. Initial sessions, prompted follow-ups and research-support sessions do not count. Only participants with the full observation window enter that denominator. We will report n/N; if the cohort differs from ten, the provisional target is at least 30%, rounded up to a whole participant.

### Compare the task fairly

Five exploratory prototype participants will try comparable source-checking and note-taking tasks using QuantLens and an existing workflow. We will alternate task order and use events of similar difficulty. We will report completed-task median time alongside failures, help and source-verification quality. We will make no speed claim before data exist, and this small exercise cannot establish population-wide superiority.

### Records and decisions

The research log will contain an anonymous participant ID, eligibility, first-touch channel, invitation and consent status, onboarding time, task outcomes, help, failure reason, duration and follow-up-session type. Contact details will stay outside the public repository. Notes from interviews will distinguish a direct observation from the team's interpretation.

Low task completion will lead to workflow repairs. Successful tasks without voluntary return will lead to interviews about value, coverage and installation effort. Only repeat use with dependable records and manageable costs will justify a broader trial. Negative findings may narrow or change the product; they will not be presented as a successful launch.

## 7. Business Model and Costs

### A free pilot before pricing

The invited pilot will be free, with no payments or advertising. We will first test whether users return and whether the service can be supported. Future paid options might include synchronization or advanced note organization, but no price, conversion rate or revenue forecast has been validated.

For planning, we propose an operating ceiling of CNY 300 per 30-day pilot period. This is a suggested limit, not an approved spend or a supplier quotation. It excludes unpaid student work, which will be recorded separately. No purchase is required to submit the first-phase documents.

| Cost area | Information needed before commitment | Owner |
| --- | --- | --- |
| Server and domain | A quote, access limits, renewal terms and external-connectivity checks. | 段博铧 |
| Market and event data | Permitted content, coverage, usage limits, attribution and a written price or free-tier entitlement. | 张胡文康 |
| Build, export and maintenance tools | Confirm available tools and any necessary incremental charges. | 胡与同 with 陈钰龙 |
| Advertising | No allocation in the initial pilot. | Team review |

We have not divided the ceiling into invented supplier prices. Any uncommitted amount remains a reserve. If legitimate data and service quotations exceed the ceiling, we will reduce permitted coverage or refresh frequency while retaining the core task, or postpone the connected pilot. We will not assume a suitable data licence is free.

### Financial Key Metrics

We will record actual operating expenditure by category and month, separately from maintenance hours. An active trial user is someone who views at least one event or saves at least one note in that period. Operating expenditure divided by active trial users gives a service-cost measure; a zero-user period has no per-user result.

For illustration only, spending the full CNY 300 with 10 active users would mean CNY 30 per active user for that period; with 20, it would mean CNY 15. These calculations are not acquisition costs, supplier estimates or revenue predictions. Recruitment effort and any later acquisition expense must be tracked separately.

Continued investment requires evidence of repeat use, dependable service and costs within an agreed limit. Later pricing research will ask what users would pay for a specific improvement and compare that response with actual delivery costs. Expressions of interest will not be recorded as paying customers.

## 8. Team and Implementation Plan

Each member owns a main module and shares research, testing and documentation. Planned effort is approximately one quarter per person, including coordination in the leader's allocation. Work will be rebalanced against actual difficulty; server work will be estimated explicitly rather than silently added to one member's tasks.

| Member | Main responsibilities |
| --- | --- |
| 段博铧 - Team Leader | Navigation, sessions and integration; scope, account onboarding, issue coordination and submission consolidation. |
| 胡与同 | Login UI, search, watchlists and stock details; competitor checks, prototypes, classmate recruitment and module tests. |
| 张胡文康 | Event lists and details, source readers and network states; API and permission checks, interviews and group outreach. |
| 陈钰龙 | Note editor, Room, review and export; save-return behaviour, pilot measures, cost records and voluntary referrals. |

Cross-review pairs are 段博铧 with 胡与同, and 张胡文康 with 陈钰龙. All members will use the same research task and contribute to integration reviews. Presentation time is not a measure of development contribution.

### Delivery gates

| Gate | Required output before moving on |
| --- | --- |
| First-phase report | Business plan, README, course repository and clearly labelled presentation materials for 21 October, 18:30, Laboratory 110. Repository submission follows the course's earlier deadline. |
| Core workflow | A Compose project with login states, destinations, source access and durable notes; actual source locations and reproducible acceptance records. |
| Connected pilot readiness | Selected services and permissions, signed APK, real authentication, account isolation, restart, offline, export, installation and upgrade checks. |
| Expansion review | Task and follow-up results with denominators, unresolved issues, support effort and actual operating costs. |

Later dates depend on the course schedule and progress. Every task will specify the screen or API, logic, owner and acceptance check. Evidence will include actual deliverables, commits, cross-reviews and test records. Commit or line counts alone will not represent workload.

Code explanations will connect the visible action to authentication state, back-stack changes or a database write and its feedback. Prototypes and planned logic cannot stand in for running evidence. Complete source and its submission format will be checked against the course requirements when available.

## 9. Current Issues, Solutions and Future Development

These are present delivery gaps, not reproduced defects in an existing Android build.

| Current issue | Planned response | Evidence needed |
| --- | --- | --- |
| No Android project or device results | Implement one complete research workflow before expanding features. | Installable build, actual source and reproducible login, navigation and persistence records. |
| Services, rights and costs unresolved | Check authentication, source access, licences and quotations against a small pilot scope. | Working external APIs, permitted content and a cost decision. |
| User value remains untested | Conduct the planned interviews, prototype tasks and invited pilot. | Original anonymous records, task outcomes and fully observed follow-up counts. |

### Future development

First, make login, source checking and save-return-reopen dependable. Then use pilot evidence to improve coverage, search, export and accessibility. Synchronization and reminders require an account, privacy and cost review. Automatic summaries require source traceability and factual checks before release.

Expansion is conditional. Strong task completion without repeat use calls for a product-value review. Record or account failures call for repairs. Repeat use, reliable operation and affordable delivery together would support the next trial.

<!-- pagebreak -->

### References

- [1] [TradingView: Official Feature Overview](https://www.tradingview.com/features/)
- [2] [Tiger Trade: Official App Updates](https://www.itigerup.com/en/about/app/update)
- [3] [HKEXnews: Hong Kong Exchanges and Clearing](https://www.hkexnews.hk/index.htm)
- [4] [Android Developers: Build an Offline-First App](https://developer.android.com/topic/architecture/data-layer/offline-first)
- [5] [Android Developers: Sign Your App](https://developer.android.com/studio/publish/app-signing)
- [6] [Android Developers: Navigation](https://developer.android.com/guide/navigation)
- [7] [Android Developers: The Navigation Back Stack](https://developer.android.com/guide/navigation/backstack)
- [8] [Android Developers: Save UI State in Compose](https://developer.android.com/develop/ui/compose/state-saving)
- [9] [Android Developers: Interact Programmatically with the Navigation Component](https://developer.android.com/guide/navigation/use-graph/programmatic)
- [10] [IFEC: Retail Investor Study 2025, published February 2026](https://www.ifec.org.hk/web/common/pdf/about-ifec/retail-investor-study-2025.pdf)
- [11] [TradingView: How to Check All Text Notes](https://www.tradingview.com/support/solutions/43000667897-how-to-check-all-text-notes/)

Market and competitor sources checked on 20 October 2026. Android design references accessed on 19 October 2026; dependencies and implementation will be checked when coding begins.
