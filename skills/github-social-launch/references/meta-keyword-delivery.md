# SuperMod comment and incoming-message keyword delivery

For every new repo in a campaign authorized for keyword delivery, use an already connected **SuperMod** instance for both triggers on Facebook/Messenger and Instagram. Current instructions or saved standing authorization may cover this work; repository publication or copy preparation alone does not. Native platform queues still handle post scheduling.

## Connection gate and optional availability

Find the user's existing SuperMod connection through available authorized tools, their chosen signed-in browser or private installed `references/local-profile.md`. Inspect the current instance and verify the intended linked Facebook Page/Instagram identity, connection health and required channel/trigger readiness. A saved URL, old ledger or generic connected badge alone does not prove current readiness. Use only controls/API capabilities actually exposed by that instance; do not invent endpoints or extract tokens from the browser.

SuperMod may remain private. This skill does not include it, require open-source publication, promise public access or supply a creator's instance URL. Do not fetch a private source repo, install/deploy a service, add billing or request new account permissions just to satisfy a launch.

- No configured/accessible authorized instance: record every affected cell as `skipped_not_connected` with reason **SuperMod not connected**. Continue authorized post scheduling and provide manual reply copy. Do not substitute native Meta keyword automations or another service.
- Partially connected or unhealthy channels: complete only the ready cells; mark the rest `skipped_not_connected` or `blocked_not_ready` with the observed reason. Do not claim four-cell coverage.
- Before scheduling copy/artwork with a keyword-delivery promise, check whether automation is ready or a manual reply plan is agreed. When it is skipped, use truthful manual wording or a direct-link CTA appropriate to the destination; report any material approved-copy change. Skipping automation does not cancel the authorized posts.

## Reconcile workflows and four-cell coverage

Inspect existing SuperMod workflows before creating one. Match by linked account, repo URL, keyword/aliases and trigger scope, not just the workflow name. Reuse correct workflows, reconcile missing triggers/channels and preserve unrelated workflows and settings. An uncertain save requires inspection before retrying.

| Trigger | Facebook/Messenger | Instagram | Result |
| --- | --- | --- | --- |
| Comment keyword | Verify independently | Verify independently | Private opener plus a reply under the triggering comment, with ordered follow-up steps when permitted |
| Incoming-message keyword | Verify independently | Verify independently | Welcome and repo-delivery sequence in the existing conversation |

A shared workflow may cover all four cells, but each cell needs independent saved-state verification. A comment trigger, general AI assistant, Instant reply or Away message does not prove incoming-message keyword coverage. Keep one intentional keyword-to-repo mapping and inspect exact/contains semantics and post/account scope in the current instance.

Inspect overlapping native Meta keyword rules read-only. When replacing a matching native rule, verify the saved SuperMod replacement and relevant delivery readiness first; use an authorized delivery test when available. Within authorized rule-maintenance scope, disable only the matching superseded rule before leaving duplicate responders active. If readiness or authority is unresolved, keep the new workflow paused and report the overlap. Never disable unrelated native rules, or any native rule merely because SuperMod is unavailable.

## Arabic spelling aliases

For every Arabic-keyword repo, review common spelling variants before saving either trigger. Keep the canonical phrase unchanged in artwork/captions; aliases expand accepted matching only. Do not assume normalization or a contains match makes hamza variants equivalent.

- Include plausible hamza/no-hamza forms: initial أ or إ (and آ when natural) versus ا; for example `أداة جديدة` / `اداة جديدة`. Preserve meaning and do not mechanically replace every letter.
- Review common informal spellings such as final ة/ه (`اداة جديده`) and unvocalized forms when relevant. Prefer actual misses and ordinary typing over speculative typos, broad fragments or synonyms.
- Maintain one explicit accepted-keyword list per repo, deduplicate it and check collisions with other workflows. If no natural variant applies, record that review rather than inventing one.
- Apply the same list to both trigger types on both channels. Preserve existing valid aliases, messages and links. Inspect actual SuperMod field limits; do not carry over an old native Meta keyword-count limit. Record useful uncovered aliases if a real limit prevents them.

## Reply sequence and platform limits

- Use the same short welcome, exact public repo URL and approved brand in both trigger paths. Mention an Arabic guide only if it exists. Preserve yellow hearts 💛 for this brand; the current user's explicit brand takes precedence.
- Use the instance's supported Messenger/Instagram card or button templates when suitable, with a working text/link fallback. Preview each channel's actual output; do not assume template parity.
- For a comment, use the triggering comment as the parent of the public acknowledgement; never create a separate top-level comment. Say a private message was sent only after confirmed opener acceptance. Respect the current private-reply limits and wait for recipient interaction before further messages when required. Incoming-message triggers need no public acknowledgement.
- Preserve the approved ordered message/card/setup sequence. Respect current messaging windows, duplicate-event suppression, cooldowns and stop conditions. Do not enable the general AI inbox assistant or change model/key/budget settings for a repo launch.
- Follow requirements are optional owner-selected workflow settings. Do not enable them by default. Where already authorized, verify an actual supported Instagram follow check; label Facebook self-confirmation accurately. Keep links after the gate and do not bypass it in public acknowledgements or fallback messages.

## Save, reopen and report

1. Configure/reconcile the repo workflow with both triggers, ready channels, full accepted-keyword list, scope, public child reply and approved private sequence. Save and reload the list, then reopen it.
2. Verify enabled state, intended linked identities, both triggers, all aliases, channel coverage, correct repo URL/brand, template/button payloads, ordered steps, follow setting and current window/cooldown/repeat limits. A paused draft is not active coverage.
3. Record per-cell status, provider `SuperMod`, private workflow reference, alias rationale, observed limits, native-rule overlap/migration outcome and verification time in the private ledger. Record skipped cells explicitly.
4. Report **saved configuration verified** separately from **delivery tested**. A live test comment or DM needs explicit authority; inspect logs after an authorized test and do not claim delivery from a saved setting alone. Keep raw logs, recipients and screenshots private.

LinkedIn replies remain manual unless a supported authorized mechanism is separately established. Missing SuperMod access is a reported automation skip, not permission to create another integration.
