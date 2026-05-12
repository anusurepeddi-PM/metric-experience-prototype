## TAB 1: Slackbot (Jordan)

### Layout
Two-panel Slack-style layout:

Left panel (sidebar, 220px):
- Tableau app icon + name at top
- Internal tab bar below:
  [Messages] [My Metrics] [History] 
  [Skills] [Files]
- Active tab highlighted
- Default active tab: Messages

Right panel (main content area):
- Renders content based on active tab
- Messages tab → conversation view
- My Metrics tab → My Metrics list view
- Other tabs (History, Skills, Files) → 
  show a simple "Coming soon" placeholder

### Messages tab (conversation view)
[Same conversation flow as before —
Jordan asks questions, receives metric cards,
taps Follow metric]

When Jordan taps [Follow metric]:
Toast at top of right panel:
"Qualified Pipeline added to My Metrics ✓
 [View My Metrics →]"
Tapping toast switches active tab 
to My Metrics (right panel updates,
My Metrics tab highlighted in left panel).

### My Metrics tab (list view)

Header:
"My Metrics"
Subtitle: "3 metrics · Last updated today"
Top right: [Ask agent ↗]

Manage section at top:
Small text: "Tap any metric to expand · 
Remove to unfollow"

Section 1: "From your team"
Label: "From your team · Configured by Maya"
Cards:
- Qualified Pipeline (at risk, red)
- Average Deal Size (warning, amber)
Each card has [···] overflow only — 
no remove (analyst-controlled)

Section 2: "Added by you"
Label: "Added by you"
Cards:
- Win Rate by Territory (at risk, red)
  [− Remove] button visible
Empty state: "Follow metrics in Messages 
to add them here."

### Managing followed metrics

Remove flow (Section 2 cards only):
Jordan taps [− Remove] on Win Rate
Inline confirmation:
"Remove Win Rate by Territory from 
My Metrics? You'll no longer get alerts.
[Yes, remove] [Cancel]"

Tapping Yes:
- Card disappears from Section 2
- Toast: "Win Rate by Territory removed 
  from My Metrics"

Add more metrics:
[+ Discover more metrics] button at bottom
Switches active tab to Messages and 
pre-populates the input with:
"Show me more pipeline metrics I should track"