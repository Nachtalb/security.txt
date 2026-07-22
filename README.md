# security.txt

Machine-readable security contact information for Nachtalb services, per
[RFC 9116](https://www.rfc-editor.org/rfc/rfc9116).

## Contents

- [`.well-known/security.txt`](.well-known/security.txt) — the policy file (PGP clearsigned)
- [`.well-known/report-nachtalb.asc`](.well-known/report-nachtalb.asc) — PGP public key for `report@nachtalb.io`

## PGP key & signature

    report@nachtalb.io
    ed25519 — 526E C423 7AFB EA17 6856  4341 C119 D3B5 0A55 1412

`security.txt` is clearsigned with this key. Verify:

    curl -s https://naa.gg/.well-known/security.txt | gpg --verify

## Maintenance

`Expires` is **2027-07-22** (RFC 9116 recommends < 1 year). Before that date:
re-check the contact address + key, bump `Expires`, and **re-sign** the file
(the signature covers the body, so any edit invalidates it).
