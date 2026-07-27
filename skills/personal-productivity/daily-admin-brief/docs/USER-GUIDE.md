# Daily Admin Brief User Guide

Step-by-step scenarios for turning three raw dumps into one page you can run your day from.

---

## Quick Start

1. Copy your day out of the calendar, the handful of inbox items that matter, and your todo list.
2. Say **"Daily admin brief"** and paste all three, one block after another.
3. Read Top Actions, fix whatever Schedule Risk flags, copy the reply stubs into your mail client, and put Dates to Capture into your calendar.

The whole thing takes about ninety seconds. Nothing is sent, nothing is connected, nothing leaves your machine.

---

## Scenarios

### Scenario 1: The 9am triage

**Situation.** You open the laptop and there are three tabs. The calendar says the day is full, the inbox has eleven unread, and the todo list is from Thursday. You have twenty minutes before the first call and no idea which tab to start with.

**What to do.**

1. Copy the day out of the calendar — select and copy is fine, you do not need to tidy it.
2. From the inbox, copy the six or seven items that actually matter. Sender and subject are enough; a snippet of the body makes the reply stubs much better.
3. Paste the todo list as it is.
4. Trigger with "Daily admin brief" and paste all three blocks. Label them if the formats are unusual.

**Expected result.** One page. Three to five Top Actions, each showing the pasted line it came from. A Schedule Risk section naming the two meetings that collide at 10:30. Reply stubs for the mail that needs an acknowledgement rather than a decision. And Dates to Capture — the deadline someone mentioned in passing that is not in your calendar yet.

The order is deliberate: fix the schedule collision first (it costs you a meeting if you don't), then work down Top Actions.

---

### Scenario 2: Evening prep for tomorrow

**Situation.** It's 18:30 and you would rather start tomorrow knowing what it holds. You have tomorrow's calendar and today's inbox leftovers, but no todo list worth pasting.

**What to do.**

1. Copy tomorrow's calendar and the inbox items you did not get to today.
2. Trigger the skill and paste both. Say nothing about the missing todos — the brief will name the gap itself.
3. Read Schedule Risk closely. Tonight is when a collision is still cheap to fix.

**Expected result.** A brief with a header line stating that no todo list was provided and which sections are therefore incomplete. Top Actions built from the calendar and inbox only. The prep flags are the useful part here: a "final decision" meeting at 14:00 with no preparation block anywhere before it is exactly the thing that ruins a Tuesday.

---

### Scenario 3: The whole week got pasted by accident

**Situation.** You copied a week view rather than a day view, and the paste covers Monday through Friday.

**What to do.**

1. Paste it anyway.
2. Read the assumption line at the top of the brief.

**Expected result.** The brief picks the earliest day covered as the target day and says so in one line. Everything from later in the week does not clutter Top Actions — instead the deadlines land in Dates to Capture, where they belong. If Monday was not the day you meant, say "brief me on Wednesday instead" and paste again.

---

## Tips

### Tip 1: Include a line of the email body, not just the subject

The reply stubs are only as good as what they have to work with. "Ivan — Budget sign-off" produces a generic acknowledgement. "Ivan — Budget sign-off: *need it before the board pack goes out today*" produces a stub that names the actual constraint. One extra line per item pays for itself.

### Tip 2: Don't clean up the dump first

Meeting links, attendee lists, RSVP markers, unread counts — the noise gets stripped for you and never reaches the brief. Time spent tidying the paste is time the skill was going to save you anyway.

### Tip 3: Trust "duration not stated" over a confident conflict

If your calendar dump lost the end times, the brief will say `duration not stated` and mark the adjacency unverified rather than assert an overlap it cannot prove. That is deliberate: a section that flags fake conflicts is a section you stop reading. If you want firm overlap detection, paste intervals (`10:00-11:00`), not start times.

### Tip 4: Read "Needs Your Call" before Top Actions on messy days

When the inbox and the todo list describe the same commitment in two different words, the brief will not merge them silently — it asks. On days when everything feels duplicated, that section is where the actual confusion lives.

---

> Back to [README](../README.md)
