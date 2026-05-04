# ClearWave Approvals State

Public repository hosting the approval-state JSON file the dashboard writes to and the Mac cron reads from.

Architecture:
- Dashboard buttons → GitHub Contents API → commit to `state.json`
- Mac cron → `raw.githubusercontent.com/zangzabam/clearwave-approvals-state/main/state.json` → updates local approval JSON

The state file is auto-rotated daily; only the latest day's file matters.
