# Calendar, existing queues and resumable state

Read this before proposing slots or resuming a campaign. The ledger is private operational state, not a public artifact or proof that the platform accepted a post.

## Dates and cadence

- Use a named IANA timezone and the user's client-local date/time. Convert “today”, “tomorrow” and “after tomorrow” once, save the resolved dates and show them in the handoff. Re-check the current time before submission so a long run cannot schedule in the past. Compute offsets per target date; daylight-saving changes can alter the UTC offset.
- The preferred recipe is one project per day **per selected destination**, Meta about 20:00 and LinkedIn about 10:30. These are workflow preferences, not claimed optimal engagement times. Both Meta destinations may share a day; both LinkedIn destinations may share a day. Platform families may start on different days because their existing queues differ.
- Read current queue entries across the relevant local days, not just the desired minute. Preserve an unrelated existing post when the user's cadence is one per day. Use the next free day when permitted by the request; explain material shifts. An exact fixed date/window takes precedence over a default and must not be silently moved beyond its boundary.
- Verify the platform/display timezone and convert when it differs from the user's timezone. State both where needed. Read the final calendar and AM/PM fields back before submitting. Current platform scheduling windows and validation messages take precedence over an old example.

## Reconciliation and idempotence

For every project × destination, inspect the live queue. Identify by actual account, repo URL or characteristic text/keyword, intended image and date/time, with native post URL/ID when available. Keywords may be absent from a queue excerpt; open the post rather than treating that as missing.

- Already scheduled and correct: record it; do not create another.
- Existing post for the same project but another channel: add only the missing destination. A combined Meta post must not recreate a Facebook entry merely to add Instagram.
- Existing post with wrong copy/time: preserve it unless the task authorizes correcting it; prepare the concrete correction and resolve material uncertainty.
- Previous save timed out: mark submitted/unconfirmed and inspect the queue before any retry. If it exists, reconcile it. If the full relevant queue confirms it is absent, retry the intended action once using the current UI state.
- An expired slot or occupied day: choose the next appropriate permitted day; never post immediately just because a schedule value vanished.

Record each transition after it happens: planned → draft → submitted/unconfirmed → scheduled_verified. Use published_verified only for a live published post actually inspected. Store platform references, saved local timestamps/offsets and verification evidence, plus rule states. Do not overwrite a verified item with a new unverified assumption. A finite item list determines when the campaign is complete; “always do this” supplies future defaults, not new posts without a request.

## Synthetic walkthroughs

These examples are invented; they are not the creator's actual schedule.

- Two repos, four destinations. A LinkedIn profile already has a different post on the requested first day. Preserve it. If the window is flexible, start the LinkedIn pair the next free day while the Meta pair may start on the requested day; verify all 8 destination entries separately.
- Facebook has Repo A scheduled, Instagram is missing. Schedule Instagram only. Reopen the shared Meta keyword rule and enable/verify the Instagram channel without disabling Messenger. The existing Facebook post and rule are retained.
- The Schedule action times out. A queue entry with the right repo, image and time exists. Mark that entry verified instead of clicking Schedule again.
- The native rule looks enabled, but no authorized real comment was sent. Report “saved rule enabled and verified”; do not claim actual message receipt was tested.
