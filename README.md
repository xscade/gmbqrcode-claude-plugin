# GMBQrcode for Claude

Manage your Google Business Profile from Claude. The plugin connects Claude Code to your
[GMBQrcode](https://gmbqrcode.com) account and adds four skills:

| Skill | What it does |
|---|---|
| `review-replies` | Drafts replies to new Google reviews in your brand tone and publishes the ones you approve. |
| `weekly-gbp-report` | Reports views, searches, calls, website clicks and direction requests, compared with the previous period. |
| `plan-gbp-posts` | Plans and drafts a month of posts, and schedules them when you ask. |
| `local-rank-check` | Runs a local ranking grid for a keyword and explains where you are strong and weak. |

## Install

```bash
claude plugin marketplace add xscade/gmbqrcode-claude-plugin
claude plugin install gmbqrcode@gmbqrcode
```

Then run `/mcp` in Claude Code, pick `gmbqrcode`, and choose Authenticate. Sign in to
GMBQrcode, pick the business to share and an access level:

- **Read only**: reviews, performance, posts and ranking reports.
- **Read + drafts**: also create and edit post drafts. Drafts never reach Google.
- **Full access**: also publish posts and review replies to Google and start ranking analyses.

You need a GMBQrcode account with your Google Business Profile connected.

## Manage access

Every connection appears under **Settings → AI Agents** in the GMBQrcode dashboard, where you
can revoke it at any time. Revoking stops Claude's access immediately.

## Use with claude.ai

Add `https://mcp.gmbqrcode.com/mcp` as a custom connector in claude.ai under
Settings → Connectors. The same sign-in screen appears.

## Privacy and support

- Privacy policy: https://gmbqrcode.com/legal/privacy
- Issues and questions: https://github.com/xscade/gmbqrcode-claude-plugin/issues
