# Roadmap

This document outlines the security and development roadmap for this template repository.

## Current Status

### Completed Security Measures

- [x] **SHA-pinned GitHub Actions** - All workflow actions use commit SHA instead of version tags
- [x] **CodeQL Analysis** - Automated static analysis for JavaScript/TypeScript (expandable to other languages)
- [x] **Dependabot Configuration** - Automated dependency updates for multiple ecosystems
- [x] **Security Policy** - Comprehensive SECURITY.md with vulnerability reporting guidelines
- [x] **CODEOWNERS** - Mandatory code review requirements for security-critical files
- [x] **Issue Templates** - Structured issue reporting with security advisory links
- [x] **Secret Detection** - Gitleaks integration for preventing credential leaks
- [x] **Dependency Review** - Automated review of dependency changes in PRs
- [x] **RSR-compliant .gitignore** - Prevents accidental secret commits
- [x] **Security Validation Workflow** - Automated checks for security file integrity

---

## Roadmap

### Phase 1: Foundation Security (Current)

Focus: Establish baseline security controls for the template repository.

#### Completed
- [x] SHA-pin all GitHub Actions to specific commits
- [x] Configure Dependabot for all relevant package ecosystems
- [x] Create comprehensive security policy (SECURITY.md)
- [x] Set up CODEOWNERS for mandatory reviews
- [x] Add secret scanning with Gitleaks
- [x] Add dependency review for PRs
- [x] Configure issue templates with security links
- [x] Disable blank issues to enforce structured reporting

#### In Progress
- [ ] Enable GitHub branch protection rules (requires manual setup)
- [ ] Configure required status checks for main branch

#### Recommended Manual Steps
These require repository admin access:
1. **Enable branch protection** on `main`:
   - Require pull request reviews (1+ approvals)
   - Require status checks to pass
   - Require branches to be up to date
   - Include administrators
   - Restrict force pushes

2. **Enable security features** in repository settings:
   - Enable Dependabot alerts
   - Enable Dependabot security updates
   - Enable secret scanning
   - Enable push protection for secrets

---

### Phase 2: Enhanced Security

Focus: Add advanced security tooling and compliance checks.

#### Planned
- [ ] Add SBOM (Software Bill of Materials) generation
- [ ] Integrate container scanning (if using containers)
- [ ] Add license compliance checking
- [ ] Implement signed commits requirement workflow
- [ ] Add SLSA provenance generation for releases
- [ ] Create security scorecard workflow (OpenSSF Scorecard)

#### Future Considerations
- [ ] SARIF upload integration for security findings
- [ ] Custom CodeQL queries for project-specific vulnerabilities
- [ ] Integration with private vulnerability reporting

---

### Phase 3: Operational Security

Focus: Runtime and operational security measures.

#### Planned
- [ ] Add release signing workflow
- [ ] Create security-focused release checklist
- [ ] Implement audit logging for sensitive operations
- [ ] Add security metrics dashboard

---

## Language-Specific Security

When adapting this template, enable relevant security tools:

### Rust
```yaml
# In codeql.yml, uncomment:
- language: rust
  build-mode: manual
```
- Enable `cargo audit` in CI
- Add `cargo deny` for license/vulnerability checks

### JavaScript/TypeScript
- Already enabled in CodeQL
- Consider adding `npm audit` to CI
- Add ESLint security rules

### Python
```yaml
# In codeql.yml, uncomment:
- language: python
  build-mode: none
```
- Add `bandit` for Python security linting
- Add `safety` for dependency vulnerability scanning

### Go
```yaml
# In codeql.yml, uncomment:
- language: go
  build-mode: autobuild
```
- Add `govulncheck` for vulnerability scanning
- Add `gosec` for security linting

### Elixir
- Add `sobelow` for security analysis
- Add `mix audit` for dependency vulnerabilities

---

## Security Contacts

- **Report vulnerabilities**: [Security Advisories](https://github.com/hyperpolymath/template-repo/security/advisories/new)
- **Security policy**: [SECURITY.md](SECURITY.md)
- **Questions**: [GitHub Discussions](https://github.com/hyperpolymath/template-repo/discussions)

---

## Version History

| Date | Version | Changes |
|------|---------|---------|
| 2025-12-17 | 1.0.0 | Initial security roadmap |

---

*This roadmap is subject to change based on security landscape evolution and project needs.*
