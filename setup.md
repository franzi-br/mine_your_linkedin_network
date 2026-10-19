# Setup: export, questions, run

Four steps: download your archive, answer eight questions, fill in [the prompt](../prompt/prompt.md), and run it in Claude. The quality of the output depends almost entirely on step 2, so spend your time there.

## Step 1: Download your LinkedIn archive

Request the full archive, not just Connections. The extra files (saved jobs, company follows, recommendations, endorsements) are what turn a flat contact list into warm, targeted leads.

1. On LinkedIn, open Settings & Privacy, then Data privacy, then Get a copy of your data. Menu names change, so search the settings for "copy of your data" if you can't find it.
2. Choose the larger data archive with all files. LinkedIn emails you when it's ready. This can take up to a day, while Connections alone arrives faster.
3. Download the zip file and keep it as is. Claude can read the zip directly.

What the archive does not contain: anyone's About section, posts, your mutual connections, or (depending on what you select) your messages. Claude can only work with what is in the file.

## Step 2: Answer eight questions

Write your answers down before you touch the prompt. Vague answers produce a vague list; specific answers produce a list you can act on the same day.

| # | Question | Why it matters | Example answer |
| --- | --- | --- | --- |
| 1 | What outcome do you want, by when, and how many? | Turns "find a job" into something Claude can rank against | 10 to 15 advice conversations within 6 weeks |
| 2 | What role are you targeting? Name one or two tracks with title, level and company type. | Different tracks need different contacts | Track A: Head of Engineering at a scale up. Track B: Senior Engineering Manager at a large tech company |
| 3 | What company size defines each track? | Lets Claude separate a founder at 30 people from one at 500 | Track A: 250 to 700 people. Track B: 750+ |
| 4 | Where can you work, and what is non negotiable? | Filters out contacts at companies you would never join | Berlin or remote Europe; no relocation |
| 5 | Who hires for your role, who can refer you, and who sits in between? | The heart of the prompt; see the note below | CTO and VP Engineering; former colleagues; tech focused search firms and VC talent partners |
| 6 | Which former employers should count as warm? | Shared history is the strongest signal the file can show | Company A, Company B, Company C |
| 7 | What one or two proof points should messages use? | Gives every opening line something concrete | Led an org redesign for 200 engineers; cut time to hire by 40% |
| 8 | How do you want the output? | Saves a reformatting round | Google Sheet, all 5s, strongest 40 of the 4s, opening lines in English and German |

For question 5, think in three groups. Decision makers are the people your future manager would be: for a first senior hire at a scale up that is usually the CEO, COO or a founder, not HR. Referral sources are peers and former colleagues who can vouch for you. Intermediaries are recruiters who specialise in your function, VC talent partners, and in house talent leads at your target companies. Most people forget the intermediaries, and they are often the ones who hear about roles first. Investors and board members are a fourth group worth its own tab: they rarely hire you, but they hear about senior searches across a whole portfolio.

## Before you send the first message

Have these ready, because the best conversations end with "send me your CV" or "register in our portal":

1. Your CV as a PDF, in the version that matches each track.
2. Your availability: are you open now, and if not, roughly when.
3. Your notice period and the salary floor you would accept. Search firm portals ask for both, and some intermediaries will only act once they know your timing.
4. Your LinkedIn job seeker preferences (target titles, company size, location) updated so the inbound side matches the roles you're chasing.

## Step 3: Fill in the prompt

Open [prompt/prompt.md](../prompt/prompt.md), copy the block, and replace every [bracket]. Delete any line that doesn't apply.

## Step 4: Run it and work the list

The first run gives you a draft list. The real value comes from the second pass, where you add what only you know.

1. Set up Claude. A Claude Project works best: upload your CV so messages can draw on real proof points. If you want a Google Sheet, connect Google Drive and Google Sheets first, and check that the connected account is your own, because the sheet is created there.
2. Paste your filled prompt, attach the LinkedIn zip, and send.
3. Check the header step. Claude should first confirm which files and signals it found. Correct anything that looks off before it scores.
4. Add what only you know. Once the list is back, go through the 5s and the strongest 4s and give Claude one line on your real history with each person you know ("worked together at X", "she recruited me into my current job", "I owe him an apology for a cancelled call"). Use the second pass prompt in [prompt/prompt.md](../prompt/prompt.md#second-pass-what-only-you-know). You only do this for the shortlist, never for your whole network, and warm context beats any title based line.
5. Check each profile before sending. Look for a recent post, a shared group or a mutual connection to sharpen the opening.
6. Send in batches of 5 to 10 and log every send in the Outreach tracker on the day you send it, not only the replies. Without the sends you can't tell what is working.
7. Ask for niche segments separately once the main list exists. A follow up like "check whether I have contacts at fast scaling AI companies and add them to a new tab" works well.

Then follow the cadence in the [outreach playbook](outreach_playbook.md).

## Limits and tips

Treat the list as a strong first draft, not a verdict. These are the things that most often need a human check.

1. Company size, stage, location and office policy come from Claude's general knowledge, which can be outdated. Check them before relying on a track tag.
2. Endorsements and recommendations match by name, so common names can link to the wrong person.
3. Saved jobs may include roles from other searches, or from other people using the account. The prompt only counts saved jobs in your function, but scan the signals column anyway.
4. Some connections arrive in the export with no name or title (hidden profiles). They can't be scored.
5. Titles are whatever people last set on their profile and can be years old.
6. The list misses people. Some of the most useful conversations can come from contacts who never make the scored lists. Keep a running list of "people I just thought of" and log them in the tracker too.
7. Your export contains other people's names and some email addresses. Keep it private, never commit it to a repository, and delete the zip when you're done.
