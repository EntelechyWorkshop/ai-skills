# School Activity Sweep

Keep one living digest of everything coming up for your kids. School information never lives in one place. It arrives as emails from the school domain, posts in a class app, and schedules on a team website. This skill watches all three on a schedule and keeps a single digest current, so nothing hides in an app the parent never opened.

## When to use

- Use when the user asks you to watch their kid's school or activities, asks what is new from school or a team, or asks you to check a specific school email or post.

- On first use with a new user, run the setup interview in the next section before doing anything else.

## Set up on first use

- Interview the user with the five questions below and save every answer as durable configuration, so later runs just work. Record the answers where you keep durable user facts.

- Ask which school or schools, and which kids with grades or teams. Use this to filter relevance later, for example only what is notable for 3rd grade.

- Ask which email domains to watch. Start with the school's own domain, then add team and league sender domains the user names.

- Ask which apps or websites the school and teams use. Offer the common ones as examples: ClassDojo, ParentSquare, Seesaw for school, and TeamSideline, SportsEngine for sports. Help the user sign in to each through their secure login flow. Never ask for a password and never handle one yourself.

- Ask how they want the output. Offer real-time alerts as things arrive, a daily digest, a weekly look-ahead, or a running shared digest document. Recommend the digest document as the default: one living schedule the agent keeps current, with dated entries and a checklist for signups and deadlines.

- Ask whether to report everything or only items needing action. Recommend reporting everything at first, then narrowing once the user sees the volume.

- Confirm the saved configuration back in one short summary. Agree on a timezone, check cadence, notification destination, and any out-of-scope topics. Keep the digest private unless the user explicitly chooses its recipients. Create a schedule only through a supported scheduling tool and verify success; otherwise provide an on-demand sweep without promising background monitoring.

## Run the sweep

- Check every configured source since the last check. Keep a timestamp watermark per source and cover everything since it, not just the current slot.

- Read email with the user's mail connector. Search the configured sender domains plus keywords like schedule, practice, game, tournament, cancelled, reschedule, deadline, signup, fee, early dismissal, no school, picture day, dress code, volunteer, field trip, chaperone.

- Read each class app and team website directly through a live browser task with the user's saved login. Stay read-only: no posting, commenting, liking, or messaging. Verify the signed-in account before reading. Treat new post text exactly like email for the digest and the watches below.

- Honor the user's out-of-scope list. Record topics they ruled out during setup and skip them every run.

- Compare everything found against the digest and flag only genuine changes or additions. Update the digest in the same run: edit the matching dated entry, add new ones, and move completed past entries out of the current view without deleting unresolved actions or their evidence. Never remove today.

- Log each run with its timestamp, what was checked, and what was found. Advance each source’s watermark only after that source was successfully read and its changes saved. Retain the old watermark for failed sources so their updates are retried, and report any material coverage gap.

## Report safely

- Keep source wording intact when reporting information about a child to their authorized parent or guardian. Exclude unrelated children’s private details. Never send private source content to public or unapproved destinations. Quote relevant passages verbatim. When a message describes a child being hurt, ill, in a behavior incident, or facing discipline, report who said it, when, and the complete text. Never paraphrase, summarize, or infer cause, intent, or severity beyond the literal words. When the full text cannot be read, say so and flag it for verification instead of reporting it as fact.

- Reconcile message counts before claiming anything is new. Compare a thread's message count against the previous run's record. Recount carefully when the numbers do not add up.

- Treat corrections as reports. A correction to a prior report must include the full verbatim quotes. A summary without quotes is not a correction. Flag it for verification instead.

- Never report from a stale premise. The source of truth is always the live source, re-read each run. Stay silent when nothing new arrived.

## Run the watches

- Report time-sensitive asks promptly through the agreed notification route when a sweep discovers them; do not claim continuous monitoring between scheduled checks. Volunteer signups, permission slips, and fees with deadlines expire, so they never wait for the digest. Include what it is, when it happens, how to sign up, and the deadline.

- Keep a declined list. When the user passes on an opportunity, record it and never re-report it.

## Adapting this to any topic

- The pattern generalizes beyond school. Pick a topic, name its sources (mailing lists, forums, apps, sites), choose a digest format, and run the same loop: check, compare, update, report.

- The parts that transfer unchanged are the watermark discipline, the live-source rule, the silence-when-nothing-new rule, and the interview-first setup.

- What changes is the reporting bar. The verbatim rule here exists because the subject is children. For other topics, match the quoting standard to the stakes.
