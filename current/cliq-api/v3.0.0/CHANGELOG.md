# Changelog

All notable changes to the **CliQ Payment API** are documented in this file.  
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)  
and adheres to [Semantic Versioning](https://semver.org/).

---

## [3.0.0] - 2025-11-11

### Added
- **Standardized endpoint structure** under `/api/ExternalAPI/V3/...` for all operations:
  - OTP  
  - In-App  
  - QR  
  - Inquiry  
  - Reversal  
- **Timeout Policy** introduced:
  - CLIQ Message Timeout: 10 seconds  
  - Processing Buffer: 20 seconds  
  - Total Timeout: 30 seconds  
- **QR Validation process** added with 5-minute validity window.  
- **Unique AES and HMAC encryption keys per environment** introduced for enhanced data security.  
- **Improved documentation structure** with unified data models across all endpoints.

---

### Changed
- **Authentication**
  - Still uses JWT Bearer Tokens.
  - Token validity reduced to **5 minutes** for better session security.  
- **Security**
  - Encryption labeling clarified in documentation for better key management visibility.
  - Updated encryption handling to ensure consistent labeling across environments.  
- **Endpoints**
  - All previous non-V3 endpoints deprecated and replaced with `/api/ExternalAPI/V3/...`.
  - Improved error and response standardization.

---

### Fixed
- Fixed inconsistent timeout behavior across different environments.
- Corrected missing encryption key documentation for sandbox and production.
- Aligned request/response examples to reflect new standardized models.

---

### Removed / Breaking Changes
- All non-V3 endpoint structures removed (`/api/v2/...`, `/api/...` legacy paths no longer supported).
- Old timeout configurations deprecated and replaced by the new unified policy.

---

### Security
- Enforced **AES + HMAC encryption per environment** to isolate data across production and sandbox.
- Strengthened **JWT validation rules** and reduced token lifetime.
- Introduced **clear encryption key identification** within documentation.
- Maintained compliance with **Open API security and CBJ interoperability standards**.

---

### Base URLs
| Environment | URL |
|--------------|-----|
| **Production** | `https://orangemoney.orange.jo:1594/` |
| **Sandbox** | `https://om-dev.orange.jo:1445/` |

---

### Migration Notes
- Replace any previous `/api/v2/` or `/api/...` calls with the new `/api/ExternalAPI/V3/...` path.
- Ensure clients handle JWT token renewal every 5 minutes.
- Apply the new encryption model using environment-specific AES/HMAC keys.
- Update any timeout configurations to comply with the 30-second unified policy.

---

### Summary
> **CliQ Payment API v3 (11 November 2025)** introduces complete structural and security enhancements improving reliability, interoperability, and compliance with open API standards.

---

## [2.0.0] - 2025-05-11
*(Reference version)*  
Introduced OAuth2 Bearer authentication, standardized response envelopes, and OpenAPI 3.0 schema.
