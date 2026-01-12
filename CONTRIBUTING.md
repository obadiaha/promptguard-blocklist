# Contributing to PromptGuard Blocklist

Thank you for helping keep the browser extension ecosystem safe! This document explains how to contribute to the PromptGuard blocklist.

## Ways to Contribute

### 1. Report a Malicious Extension

If you've found a suspicious or malicious Chrome extension:

1. **Open an issue** using the "Report Malicious Extension" template
2. **Provide the extension ID** (32-character string from `chrome://extensions`)
3. **Describe the malicious behavior** you observed
4. **Include evidence** if possible (screenshots, network logs, code analysis)

### 2. Verify Reported Extensions

Help us verify community reports by:

- Testing reported extensions in a sandboxed environment
- Analyzing extension code for malicious patterns
- Cross-referencing with other security databases (CRXcavator, ExtensionTotal)
- Documenting your findings in the issue

### 3. Add Intelligence Sources

Know of a security research report or database we should integrate?

- Open an issue with the source details
- Explain what data is available and how to access it
- Suggest how it could improve our coverage

## Blocklist Entry Format

When adding entries to `blocklist.json`:

```json
{
  "id": "32-character-extension-id",
  "name": "Extension Name",
  "reason": "Brief description of malicious behavior",
  "discovered": "YYYY-MM"
}
```

## AI Threats Feed

For extensions targeting AI platforms (ChatGPT, Claude, etc.), add entries to `ai-threats.json`:

```json
{
  "id": "extension-id",
  "name": "Extension Name",
  "category": "prompt_harvesting|response_injection|session_hijacking|data_exfiltration|fake_ai_tools",
  "platforms_targeted": ["chat.openai.com", "claude.ai"],
  "behavior": "Detailed description of malicious behavior",
  "discovered": "YYYY-MM",
  "source": "Where this was reported/discovered"
}
```

## Verification Criteria

Before adding an extension to the blocklist, we verify:

1. **Extension ID is valid** (32 characters, lowercase alphanumeric)
2. **Malicious behavior is confirmed** through:
   - Code analysis
   - Network traffic analysis
   - Reproduction of malicious behavior
   - Multiple independent reports
   - Removal by Google from Chrome Web Store
3. **Entry is not a duplicate**
4. **Documentation exists** (link to report, CVE, or analysis)

## Pull Request Process

1. Fork the repository
2. Add your entry to `blocklist.json` or `ai-threats.json`
3. Update the counts in `README.md` if applicable
4. Submit a PR with:
   - Description of the malicious extension
   - Evidence or source links
   - Category of threat

## Code of Conduct

- Only report extensions with genuine security concerns
- Do not submit false reports to harm legitimate developers
- Respect the privacy of extension users affected by malware
- Follow responsible disclosure practices

## Questions?

Open an issue with the "question" label or reach out to the maintainers.
