# PromptGuard Blocklist

A curated list of known malicious Chrome extension IDs used by [PromptGuard](https://github.com/obadiaha/promptguard) to protect users from dangerous browser extensions.

## How It Works

PromptGuard automatically fetches this blocklist weekly to identify known malicious extensions installed in your browser. Extensions on this list are immediately flagged as high-risk.

## Blocklist Format

The `blocklist.json` file contains:

```json
{
  "version": "1.0.0",
  "last_updated": "2026-01-12",
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

## Intelligence Sources

Our blocklist is compiled from multiple reputable sources:

### Primary Sources
- **Google Chrome Web Store Removals** - Extensions removed by Google for policy violations
- **CRXcavator** - Extension security analysis database
- **ExtensionTotal** - Malware detection for browser extensions

### Security Research
- **Avast Threat Labs** - Malicious extension campaigns
- **McAfee Labs** - Browser threat research
- **Kaspersky Research** - Extension-based malware analysis
- **Guardio Labs** - Browser security research

### Community & Academic
- **Security researcher disclosures** - Published CVEs and blog posts
- **r/chrome community reports** - User-reported suspicious extensions
- **Academic papers** - Browser extension security research

## Current Categories

| Category | Count | Description |
|----------|-------|-------------|
| Data Harvesters | 5 | Extensions stealing browsing data |
| Fake Ad Blockers | 2 | Impersonating legitimate ad blockers |
| Cryptominers | 3 | Background cryptocurrency mining |
| Credential Stealers | 4 | Stealing passwords and login sessions |
| Session Replay | 2 | Recording all user input |
| Malicious VPNs | 2 | Routing traffic through attacker servers |
| Click Fraud | 2 | Ad injection and click fraud |
| Dormant Colors | 10 | Large-scale affiliate fraud campaign |

## Contributing

Found a malicious extension? Please open an issue or PR with:
1. Extension ID (32-character string)
2. Extension name
3. Evidence of malicious behavior
4. Source/reference

## Update Frequency

This blocklist is updated:
- **Immediately** when new threats are discovered
- **Weekly** review of new Google removals
- **Monthly** comprehensive audit

## License

MIT License - Feel free to use this blocklist in your own security tools.

## Related Projects

- [PromptGuard](https://github.com/obadiaha/promptguard) - Chrome extension security scanner
- [CRXcavator](https://crxcavator.io/) - Extension analysis tool
- [Extension Monitor](https://extensionmonitor.com/) - Track extension changes
