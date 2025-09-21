# Secret Audit — motionmavericks/AutoGPT — 20250921

- generated: 2025-09-21T15:51:19+10:00
- gitleaks: 8.18.4
- trufflehog: not_run
- deep_scan: true

## Findings (redacted)

- Detector: generic-api-key
  - Location: docs/content/AutoGPT/setup/index.md:89
  - Commit: 
  - Excerpt: API_KEY=REDACTED
- Detector: generic-api-key
  - Location: docs/overrides/main.html:49
  - Commit: 
  - Excerpt: key: 'REDACTED'
- Detector: gcp-api-key
  - Location: frontend/android/app/google-services.json:23
  - Commit: 
  - Excerpt: REDACTED"
- Detector: gcp-api-key
  - Location: frontend/build/web/index.html:53
  - Commit: 
  - Excerpt: REDACTED"
- Detector: gcp-api-key
  - Location: frontend/lib/main.dart:27
  - Commit: 
  - Excerpt: REDACTED'
- Detector: discord-client-secret
  - Location: frontend/build/web/flutter_service_worker.js:28
  - Commit: 
  - Excerpt: discord_logo.png": "REDACTED"
- Detector: gcp-api-key
  - Location: frontend/web/index.html:53
  - Commit: 
  - Excerpt: REDACTED"
- Detector: gcp-api-key
  - Location: frontend/build/web/main.dart.js:100880
  - Commit: 
  - Excerpt: REDACTED"

- Detector: github-pat
  - Location: arena/gaby_agent.json:2
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: REDACTED
- Detector: gcp-api-key
  - Location: frontend/build/web/main.dart.js:100880
  - Commit: 4fe62b8063217d7edc7c18a8a7d59bb5a37fea04
  - Excerpt: REDACTED"
- Detector: generic-api-key
  - Location: docs/content/AutoGPT/setup/index.md:89
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: API_KEY=REDACTED
- Detector: generic-api-key
  - Location: docs/overrides/main.html:49
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: key: 'REDACTED'
- Detector: gcp-api-key
  - Location: frontend/android/app/google-services.json:23
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: REDACTED"
- Detector: discord-client-secret
  - Location: frontend/build/web/flutter_service_worker.js:28
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: discord_logo.png": "REDACTED"
- Detector: gcp-api-key
  - Location: frontend/build/web/index.html:53
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: REDACTED"
- Detector: gcp-api-key
  - Location: frontend/lib/main.dart:27
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: REDACTED'
- Detector: gcp-api-key
  - Location: frontend/web/index.html:53
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: REDACTED"
- Detector: gcp-api-key
  - Location: frontend/build/web/main.dart.js:101330
  - Commit: 7082e63b115d72440ee2dfe3f545fa3dcba490d5
  - Excerpt: REDACTED"

## Remediation plan
- Replace hard-coded secrets with env vars or secret manager references.
- Add .gitignore for .env*, credentials, and build artifacts.
- Add pre-commit hook to run `gitleaks protect`.
- Rotate any exposed keys at the provider.

## History rewrite (optional)
- Only performed if CONFIRM_HISTORY_REWRITE=true.
- Force-push required. May break forks and SHAs.
