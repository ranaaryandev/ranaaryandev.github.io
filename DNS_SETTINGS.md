# Recommended DNS TXT Records for Email Security & Deliverability (ranaaryan.online)

To resolve domain spoofing and email deliverability warnings:

## 1. SPF (Sender Policy Framework) Record
Add a `TXT` record at the root domain (`@` or `ranaaryan.online`):
- **Type**: `TXT`
- **Name/Host**: `@`
- **Value**: `v=spf1 include:_spf.google.com ~all`
- **TTL**: `3600` (or Auto)

## 2. DMARC (Domain-based Message Authentication, Reporting, and Conformance) Record
Add a `TXT` record at `_dmarc.ranaaryan.online`:
- **Type**: `TXT`
- **Name/Host**: `_dmarc`
- **Value**: `v=DMARC1; p=none; sp=none; rua=mailto:ranaaryan.dev@gmail.com`
- **TTL**: `3600` (or Auto)
