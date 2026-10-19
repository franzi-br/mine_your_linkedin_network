# The prompt

Copy everything inside the code block, replace every [bracket] with your answers from [docs/setup.md](../docs/setup.md), and delete any line that does not apply (for example Track B if you have one target role). Attach your LinkedIn zip and send.

```
GOAL
I'm a [current title] at [current company], based in [city]. [Location constraint, e.g. I will not relocate.]
I'm pursuing [one / two] career track(s):
Track A: [role, level, company type], roughly [size range] people.
Track B: [role, level, company type], roughly [size range] people.
Within [timeframe] I want [number] advice conversations with people who hire for, or can refer me into, these roles. Outreach asks for advice, not a job.

WHO I'M LOOKING FOR (tag each match with the track it serves: A, B or both)
1. Decision makers: [titles of the people who would hire me, per track].
2. Referral sources: [senior peers in my function]; former colleagues from [former employers] now in senior roles; anyone at a company in my target overlap files.
3. Intermediaries: [search firms or recruiters specialising in my function]; VC talent partners; heads of talent at target companies. Generalist recruiters score low unless their title shows a focus on my function or level.
4. Investors and board members: VC partners, angels and board members who hear about senior hires across a portfolio before roles are posted.
5. Warm network: people with a strong warmth signal (recommendations, endorsements both ways, a shared employer) at a company in my target space, in any function. Warmth alone never moves them into the main list; they get their own tab.

DATA
The uploaded file is my full LinkedIn export. Start with Connections.csv (name, URL, email, company, position, connected on). It has no industry, size, location or tenure.
Use as target overlap signals: Jobs/Saved Jobs.csv and Jobs/Job Applications.csv (strong), Company Follows.csv (weaker). Only count saved jobs that match my function.
Use as warmth signals: Recommendations_Received.csv, Recommendations_Given.csv, Endorsement_Received_Info.csv, Endorsement_Given_Info.csv (match by full name and flag uncertain matches), Invitations.csv, Member_Follows. Treat the Connected On year as a weak proxy only.
Ignore every other file in the export.
Whenever I name a person in chat, check the name against the file and flag near matches. Typed or dictated names are often slightly wrong.

METHOD
First show me the column headers and tell me which signals are actually available, before scoring anything.
Process every row. Don't sample or skip anyone. Triage with a keyword pass and tell me the keywords and how many rows the pass kept. Then manually review titles the pass could miss (Partner, Principal, Managing Director, Chief of Staff, Advisor), plus every row with a target overlap or warmth signal, regardless of title.
Score 1 to 5:
5 = decision maker or intermediary for one of my tracks at a relevant company.
4 = strong referral source or adjacent decision maker.
3 and below = not shown.
A warmth or target overlap signal can lift a score by one point. It cannot make an irrelevant title relevant.
When two or more matches work at the same company, mark the strongest "contact first" and the others "hold until the first replies".
Mark anything you infer from your own knowledge (company size, stage, location, industry, office policy) as "(inferred)". Never present it as data from the file. Treat titles as possibly outdated.

OUTPUT
[Google Sheet / tables in chat] with these tabs:
1. Matches: one row per match, columns #, Score, Category, Track, Name, Title, Company, Signals used, Why they fit (one sentence, specific to my goal), Opening line [language 1], Opening line [language 2], Profile URL, Contact order. Group into 2 to 4 categories that fit the data. Show all 5s. Cap 4s at the strongest [40] and tell me how many more exist.
2. Investors & boards: same columns.
3. Warm network: same columns, capped at [20].
4. Outreach tracker: empty, one row per message I actually send, columns Date sent, Name, Company & title, Source (list match with tab and #, existing connection not on the lists, intro from whom, inbound, direct application), Track, Status, Followed up on, Reply date, What came back, Next step, Follow up by. Status uses only: Sent, Followed up, No reply, Declined, Replied, Call booked, Talked, Lead shared, Interviewing, Closed.
5. Gaps: match counts per category and per track, naming which are thin or missing, then the companies from my saved jobs where I have zero connections.
6. Method & limits: rows processed, rows that could not be scored, triage keywords, caps, and which fields are inferred.

OPENING LINES
Ask for advice, not a job, and ask for 15 minutes. Reference a real detail from their title or company. Mention shared history only if the file shows it or I tell you. Keep each line under 60 words. No generic "I'd love to connect". Never invent facts about the person or company.
Investors and board members: no call in the first message. Ask for one tip and whether anyone in their founder network may be hiring soon.
If I tell you I owe someone an apology, open with it. If they may not remember me, say so plainly.
Use [formal / informal] address by default and switch to informal where a shared employer or what I tell you shows a first name relationship.
For every 5: remind me to check their actual profile for a recent post, shared group or mutual connection before sending.

LIMITS
State plainly that you only see this export: no About sections, posts, mutual connections or messages.

ONGOING
When I add personal context about a match, treat it as true, mark it "(your note)" in the signals column, adjust the score if it changes the picture, and rewrite that opening line.
When I report a send or a reply, update the Outreach tracker. When I ask how outreach is going, compute from the tracker: messages sent, reply rate, conversations booked or held, leads (CV passed on, intro, interview), split by source and category. Always state the sample size and say when it is too small to read much into.
```

## Second pass: what only you know

Run this once the first list is back. Go through the 5s and the strongest 4s, and add one line for each person you actually know. You only need to do this for the shortlist, not for your whole network.

```
Here is what only I know about some of the matches. Treat it as true, mark it "(your note)", adjust scores where it changes the picture, and rewrite those opening lines.
[Name: how we know each other, informal or formal address, anything to avoid.]
[Example: Jane Doe: my manager at Company A, 2019 to 2021, informal.]
[Example: John Roe: I cancelled a call with him and owe him an apology.]
[Example: Alex Kim: we met once at a conference; she may not remember me.]
```

Ten honest one liners like these improve the messages more than any prompt tuning, because the export can't tell a former manager from a stranger with the same title.

## Why it is written this way

The first prompt asks only for what is true across your whole network (goal, tracks, who hires you), and the second pass adds what only you know, about the shortlist only. It makes Claude show the column headers before scoring, so a broken or partial export is caught before an hour of work. It separates data from inference everywhere, so you never send a message built on a company size Claude guessed. And it creates the tracker in the same run, because a list nobody tracks stops being worked within a week.
