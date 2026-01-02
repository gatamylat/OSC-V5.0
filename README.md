# OSC — Operator Session Console

**Version 5.0**

A terminal-style PWA for tracking work sessions, tasks, decisions, and cognitive load. Built with an "operator's journal" philosophy: append-only facts, deterministic tracking, no AI advice.

## What's New in v5.0

### UX Improvements
- **Smart Autoscroll**: Only scrolls when you're near the bottom. Read history without being yanked down.
- **Mobile Autocomplete**: Tap the `>` prompt to toggle autocomplete on mobile (Tab still works on desktop).
- **Quick History Access**: `history` shows numbered list, `history 2` opens that session's report.
- **Smart Report Defaults**: `report` shows last session, `report active` shows current session.
- **Load Warning Cooldown**: Warnings appear max once per 10 minutes per level, only on increases.

## Commands

### Session
```
enter <intent>        Start session with intent
exit [outcome]        End session (completed/aborted/timeout)
status                Current session status
```

### Tasks
```
task <description>    Start new task (becomes focus)
done [id]             Complete task (focus if no id)
fail [id] [reason]    Fail task
drop [id]             Abandon task
focus [id]            Set/show focus task
tasks                 List all tasks (> marks focus)
```

### Decisions
```
decide <X> :: <Y>     Log decision with reason
decisions             List all decisions
```

### Monitoring
```
load                  Cognitive load details
history               Sessions list with # indexes
history <#>           Open report for session #
report                Last completed session
report active         Current active session  
report <id>           Session by ID
```

### Other
```
export json|csv       Export data
config                View/set configuration
scanlines on|off      Toggle CRT effect
tutorial              Interactive guide
help                  Command reference
clear                 Clear console
reset confirm         Delete all data
```

## Tips

| Input | Action |
|-------|--------|
| Tab | Toggle autocomplete (desktop) |
| Tap `>` | Toggle autocomplete (mobile) |
| ↑/↓ | Command history |
| history 1 | View most recent session |
| report | Quick view last session |

## Installation

### GitHub Pages
1. Fork/clone this repository
2. Settings → Pages → Source: main branch
3. Access at `https://your-username.github.io/osc/`

### iPhone
Safari → Share → "Add to Home Screen"

## Files
```
osc/
├── index.html      # Main application
├── manifest.json   # PWA manifest
├── sw.js           # Service Worker
├── icons/          # App icons
└── README.md
```

## Changelog

### v5.0
- Smart autoscroll (only when near bottom)
- Mobile autocomplete via prompt tap
- History with numbered indexes
- `history <#>` to open report directly
- `report` without args shows last session
- `report active` shows current session
- Load warning cooldown (10 min)

### v4.9
- Focus task concept
- `focus` command
- `scanlines on|off` command
- CSV export with proper escaping
- Single source of truth for version

---

**Philosophy**: Facts, not advice. Track what happened, make your own decisions.

**License**: MIT
