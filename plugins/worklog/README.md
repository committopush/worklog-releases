# WorkLog plugin for Claude

Books your working day from [WorkLog](https://github.com/committopush/worklog-releases) — a macOS menu-bar app
that records which window you work in, privately on your Mac — into Jira/Tempo.

## Install

- **Claude (chat, Cowork):** Customize → Plugins → Add → Add marketplace → `committopush/worklog-releases`, then add **WorkLog**.
- **Claude Code:**

  ```
  /plugin install worklog --marketplace committopush/worklog-releases
  ```

## Use

Use `/timebooking` (in Cowork and Claude Code: `/worklog:timebooking`), optionally with a day such as
`yesterday`. Claude reads WorkLog's rounded day summary, proposes a timesheet as an interactive timeline and
books the approved entries through your time-tracking connector.

Requires the WorkLog app. Its MCP server runs locally (Cowork and Claude Code start it from this plugin; in
chat, install the WorkLog desktop extension). Activity data never leaves your Mac except as the aggregated
summary Claude reads when you ask it to book your time.
