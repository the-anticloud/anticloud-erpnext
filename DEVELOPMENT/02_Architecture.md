# Technical Architecture — ERPNEXT

**Upstream:** [https://github.com/frappe/erpnext](https://github.com/frappe/erpnext)
**License:** GPL3 / MIT modules
**Category:** SUPERMARKETS
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Full ERP with retail/POS module

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B demand forecasting running fully offline on-premises
2. Barcode/QR scanning via local CV model — no cloud vision API
3. AES-256 POS transaction encryption with AIOSS audit trail
4. Single-binary POS executable with embedded SQLite inventory
5. Offline-first sync: works during internet outage, reconciles on reconnect
6. Zero-cloud pricing engine: replaces SaaS pricing APIs with local rules
7. Receipt generation from local template engine, no third-party service
8. GPU/CPU equalizer: inference scales from CPU-only to GPU automatically

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_erpnext.spec` or `go build -o erpnext`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |