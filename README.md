# PromptGuard Blocklist

A curated, multi-source blocklist of malicious Chrome extension IDs used by [PromptGuard](https://github.com/obadiaha/promptguard) to protect users from dangerous browser extensions.

## 📊 Current Stats

| Metric | Count |
|--------|-------|
| Total Blocked Extensions | 30 |
| AI-Targeted Threats | 3 |
| Intel Sources | 6+ |
| Last Updated | 2026-01-12 |

## 🔍 Intelligence Sources

We aggregate threat intelligence from multiple reputable sources:

### Primary Sources
| Source | Type | Coverage |
|--------|------|----------|
| **[CRXcavator](https://crxcavator.io)** | Risk Analysis API | All extensions |
| **[ExtensionTotal](https://extensiontotal.com)** | Malware Detection | On-demand scans |
| **Google Removals** | Official Takedowns | Chrome Web Store |
| **Community Reports** | User Submissions | [Report an extension](../../issues/new?template=report-malicious-extension.md) |

### Security Research
- Guardio Labs - Browser security research
- Avast Threat Labs - Malicious extension campaigns
- McAfee Labs - Extension-based malware
- Kaspersky Research - Browser threat analysis
- Independent security researchers

### AI-Focused Monitoring
We specifically track extensions targeting AI platforms:
- ChatGPT (chat.openai.com)
- Claude (claude.ai)
- Gemini (gemini.google.com)
- Copilot (copilot.microsoft.com)
- And 6+ more platforms

See [ai-threats.json](./ai-threats.json) for the dedicated AI threat feed.

## 📁 Files

| File | Description |
|------|-------------|
| `blocklist.json` | Main blocklist with all malicious extension IDs |
| `ai-threats.json` | AI platform-specific threats (prompt harvesting, etc.) |
| `CONTRIBUTING.md` | How to contribute and report extensions |

## 🚨 Threat Categories

| Category | Count | Description |
|----------|-------|-------------|
| Data Harvesters | 5 | Extensions stealing browsing data |
| Fake Ad Blockers | 2 | Impersonating legitimate ad blockers |
| Cryptominers | 3 | Background cryptocurrency mining |
| Credential Stealers | 4 | Stealing passwords and sessions |
| Session Replay | 2 | Recording all user input |
| Malicious VPNs | 2 | Routing traffic through attackers |
| Click Fraud | 2 | Ad injection and click fraud |
| Dormant Colors | 10 | Large-scale affiliate fraud campaign |

## 🤖 AI-Specific Threats

Extensions that specifically target AI chatbots to steal prompts:

| Threat Type | Risk | Description |
|-------------|------|-------------|
| Prompt Harvesting | Critical | Captures everything you type into AI |
| Response Injection | High | Modifies AI responses |
| Session Hijacking | High | Steals AI platform credentials |
| Data Exfiltration | High | Sends conversations to third parties |
| Fake AI Tools | Critical | Malicious ChatGPT/Claude clones |

## 🔄 Update Schedule

- **Real-time**: Critical threats added immediately
- **Weekly**: New Google removals and research reports
- **Monthly**: Comprehensive audit and cleanup

## 📥 Integration

### For PromptGuard Users
The blocklist is automatically fetched weekly. No action needed.

### For Developers
```bash
# Fetch the blocklist
curl https://raw.githubusercontent.com/obadiaha/promptguard-blocklist/main/blocklist.json

# Fetch AI-specific threats
curl https://raw.githubusercontent.com/obadiaha/promptguard-blocklist/main/ai-threats.json
```

### API Format
```json
{
  "malicious_ids": [
    {
      "id": "extension-id-here",
      "name": "Extension Name",
      "reason": "Why it's malicious",
      "discovered": "2024-01"
    }
  ]
}
```

## 🆘 Report an Extension

Found a malicious extension? Help us protect others:

**[→ Report Malicious Extension](../../issues/new?template=report-malicious-extension.md)**

Please include:
1. Extension ID (from `chrome://extensions`)
2. Description of malicious behavior
3. Any evidence (screenshots, logs)

## 🔗 Related Projects

- [PromptGuard](https://github.com/obadiaha/promptguard) - Chrome extension security scanner
- [CRXcavator](https://crxcavator.io) - Extension risk analysis
- [ExtensionTotal](https://extensiontotal.com) - Extension malware scanner

## 📄 License

MIT License - Use this blocklist in your own security tools.

---

**Protecting your AI conversations, one extension at a time.**
