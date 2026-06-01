# flirt-pallet-labels

Static 4×6 pallet-label generator for Flirt Drinks Inc.

Pure client-side page (jsPDF). It reads the shipment data from URL query params
and renders one 4×6" label per pallet, ready to download as a PDF and print.

**No secrets live here.** The page holds only rendering logic + the Flirt logo.
All order data (PO, customer, address, pallet count, ship date) is passed per
click via the URL by the Airtable "Generate Pallet Labels" button — nothing is
stored in this repo.

## Usage

```
https://alexy-flirt.github.io/flirt-pallet-labels/?po=PO123&customer=Acme&addr=123%20Main%20St&pallets=6&ship=2026-06-05
```

Params: `po`, `customer`, `addr` (use `%0A` for line breaks), `pallets` (int), `ship`.
