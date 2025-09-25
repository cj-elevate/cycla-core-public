# Security Policy - Cycla Core Repository

## 🔐 Security Posture

This repository follows strict security practices to ensure no sensitive data is committed to version control.

### Key Vault + DPAPI Architecture

**Primary**: Azure Key Vault or equivalent for production secrets
**Fallback**: Windows DPAPI for local development encryption
**Repository**: Contains NO secrets, tokens, or sensitive configuration

### What's Excluded from Git

- **Environment files**: `*.env`, `.env*`
- **Database files**: `*.db`, `*.sqlite*`
- **Runtime artifacts**: `logs/`, `tmp/`, `queue/`, `receipts/`
- **Secrets directories**: `secrets/`, `keys/`, `tokens/`
- **Volatile paths**: `staging/`, `quarantine/`

### Security Verification

This repository is automatically scanned for:
- Accidentally committed secrets
- API keys and tokens
- Database contents
- Private configuration files

### Reporting Security Issues

If you discover a security vulnerability:

1. **DO NOT** create a public GitHub issue
2. Contact: [CONTACT_EMAIL_PLACEHOLDER]
3. Include: Description, steps to reproduce, potential impact
4. We will respond within 24 hours

### Security Compliance

- All secrets managed through Azure Key Vault
- Local development uses DPAPI encryption
- Pre-commit hooks prevent accidental secret commits
- Regular security scans and audits performed

---

**Last Updated**: 2025-09-25
**Security Review**: Pending
**Compliance**: Enterprise-grade secret management