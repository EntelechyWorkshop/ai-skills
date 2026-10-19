# Library Holds

Check a public library catalog, place holds, and remind the user about pickups only from verified live state. This skill is written for BiblioCommons first. BiblioCommons powers the online catalogs of many large US library systems, and the worked examples here use a BiblioCommons catalog address like `https://yourlibrary.bibliocommons.com`. Other catalog systems follow the same pattern with a different click path, and the adapter section covers that.

## When to use

- Use when the user asks about a library book, asks you to hold or check out a book, or when a scheduled reminder needs to verify holds before messaging.

- On first use with a new user, run the setup interview in the next section before doing anything else.

## Set up on first use

- Ask the user three questions and save the answers for every later use. Ask which library or library system they use. Ask them to sign in to the catalog through their secure login flow. Never ask for the password and never handle it yourself. Ask which branch or location should be the default pickup point for holds. Ask whether the user wants pickup reminders and automatic re-placement of expired holds; save those choices, including reminder timing, only when authorized.

- Record the answers where you keep durable user facts so later sessions skip the interview and just work. Confirm the saved pickup branch back to the user in one line.

## Check holds on BiblioCommons

- Sign in at the catalog through a live browser task, for example `https://yourlibrary.bibliocommons.com`, using the user-completed secure login. Read the holds page read-only: which holds are ready with pickup-by dates, which are pending with queue positions, and anything overdue.

- Treat the catalog as the source of truth. Never trust a remembered or previously recorded holds state when the question is what is true now.

## Place a hold

- Search the catalog for the title and author. Confirm the edition and format before acting, and prefer the physical book when the user asked for one. Note other editions only when no physical copy exists.

- When the user asks for the hold or has authorized this standing workflow, place it at the saved pickup branch. Check for any fee or unusual condition before submitting; do not assume all libraries' holds are free. Report the exact title and author as shown, the format held, the pickup branch on the confirmation, and the queue position when the item is checked out.

## Remind safely

- Create recurring reminders only with the user’s chosen schedule and a supported scheduling tool. Confirm that scheduling succeeded; if unavailable, offer an on-demand check instead. Verify against the live catalog before every pickup reminder. Never remind from a stale premise. People pick up holds without notice, and a stale nudge erodes trust.

- Stay silent when the book is already picked up or no longer on hold. Stay silent when the live check fails after one retry later in the day. Log the verified state or the miss where you keep working notes.

## Handle expired holds

- Re-place an expired hold only when the user has authorized that behavior and no duplicate is active. A new hold may have a different queue position; it does not restore the old one. Check for fees before submitting. Confirm the new hold the same way as a fresh placement.

## Other catalog systems

- The pattern is identical on Polaris, SirsiDynix, Koha, and other catalog systems: sign in to the catalog, search, place the hold, choose the pickup location. Only the click path differs.

- Ask the user which system their library runs on and adapt the steps. Do not guess at menu names you have not seen.

- When the user does not know, check the library website. The catalog link URL usually gives it away. A URL containing `bibliocommons.com` means BiblioCommons. Otherwise ask the user and adapt from there.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If the available tools cannot reach the catalog, explain the missing access. Use a supported connector setup workflow only if the user requests it; this skill does not authorize installing new integrations.

## Websites

- The user's library catalog (for example `https://yourlibrary.bibliocommons.com`) for searching the catalog, reading holds status, and placing holds. Use the authenticated session and verify sign-in before acting. Never copy credentials into prompts or saved skill files.
