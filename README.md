--[[[PT] PeopleTracker — quick help
----------------------------------------------------------------
What it does
  Scans WHO output (including multi-page via MORE) and places small
  name labels onto the Mudlet map at the rooms the people are in.
  Output includes clickable (GOTO) links that path you there.
  ------------------------------------------------------------------------------------
  NOTE: if you have other qwho aliases and triggers, you might wanna deactivate those.
  ------------------------------------------------------------------------------------

Basics
  Start scan         qwho           — full list
  Groups only        qwhog          — only rooms with ≥2 people
  Watchfor only      qwhow          — only people on your watch list
  Filter by area     qwho <AreaSubstr>  e.g. qwho tundra

  List in area       ppin <AreaSubstr>  e.g. ppin ashaxei
  Group w/ someone   ppwith <Name>      e.g. ppwith Ashden
  Watch list         wf [Name|show|clear]     toggle or show or clear table
  Goto last loc      gotop [Name]       empty = uses your global target
  Help print         pthelp                    prints a help text

GOTO links
  Wherever you see (GOTO) at the end of a line, click it to path to
  that room. If multiple matching rooms exist, PT places lettered labels per Z-level.

Auto-cleanup & labels
  Map labels auto-clear after 120s. Change via PT.conf.autoclear_after_secs.
  Labels appear as a single line per room; when there are duplicate rooms, PT
  places letter-only markers and one full list on the right-most room per Z.

Watch list (wf)
  wf Person  toggles person on/off.
  wf show     shows everyone in the list.
  Combine with qwhow to print only watched names.

Gotchas / notes
  • Run qwho before using ppin, ppwith, or gotop — they use the last scan.
  • PT auto-MOREs up to 20 pages per scan.
  • If pathing fails, ensure your mapper has a current room and a valid path.

Current config (read-only)
  Output window      main
  Label color        white
  Label font         10
  Auto-clear         120s
  MORE limit         20

Aliases you have right now
  qwho / qwhog / qwhow / ppin / ppwith / wf / gotop / pthelp

Examples
  qwho                — list everyone and place labels
  qwhog               — show only rooms with groups
  qwhow               — show only people on your watch list
  qwho tundra         — WHO then print only areas matching 'tundra'
  ppin targossas      — recap who is in any area matching 'targossas'
  ppwith Ashden       — who is with Ashden and where
  wf Ashden           — toggle Ashden on your watch list
  wf show             — print watch list
  wf clear            — clear watch list
  gotop               — goto your target's last known room
  gotop Mizik         — goto Mizik's last known room

----------------------------------------------------------------
Tip: You can theme PT output by changing PT.out to your mini-console,
and edit PT.conf.labelcolor or PT.conf.labelsfont for map label style.]]
