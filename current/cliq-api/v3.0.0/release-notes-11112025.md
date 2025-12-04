
# CliQ Payment API – Release Notes (Version 3 | 11 November 2025)

## General Updates
- All endpoints standardized under `/api/ExternalAPI/V3/...` for OTP, In-App, QR, Inquiry, and Reversal operations.
- Improved documentation structure with unified data models for requests and responses.

---

## Authentication
- Still uses **JWT Bearer Tokens**.
- **Token validity:** 5 minutes.

---

## Base URLs
- **Production:** `https://orangemoney.orange.jo:1594/`
- **Sandbox:** `https://om-dev.orange.jo:1445/`

---

## Functional Enhancements

### Timeout Policy
- **CLIQ Message Timeout:** 10 seconds  
- **Processing Buffer:** 20 seconds  
- **Total:** 30 seconds (failure beyond this).
- **QR Validation:** 5 Minutes

---

## Encryption & Security
- Unique AES and HMAC keys per environment.
- Clear encryption labeling in documentation.

---


## Summary of Changes

| Area | Type | Description |
|------|------|-------------|
| **Authentication** | Updated | JWT validity set to 5 minutes. |
| **Timeout Policy** | New | 10s + 20s total limit. |
| **QR Validation** | New | QR Validation |
| **Security** | Updated | AES/HMAC per environment. |
| **Endpoints** | Updated | All non-V3 endpoints replaced. |

---

## Summary
> **CliQ Payment API V3 (11 November 2025)** introduces complete structural and security enhancements improving reliability, interoperability, and compliance with open API standards.
