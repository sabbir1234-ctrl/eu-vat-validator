# EU VAT Validator — VIES Compliance Tool

A single-page web tool that validates EU VAT numbers against the European Commission's official **VIES** service and explains the design of a compliant validation service.

![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) ![VIES](https://img.shields.io/badge/API-EU%20VIES%20SOAP-003399)

## Features

- Validate a VAT number with a live SOAP request to the VIES `checkVatService` (`ec.europa.eu`)
- Lookup flow explained: cache check → VIES live query → audit entry
- Design notes on **rate limiting**, a **30-day result cache**, **audit retention**, and **retry with exponential backoff** (up to 3 attempts)

## Run

Everything is in one `index.html` file. Open it in a browser.

> Browsers may block calls to the VIES endpoint because of CORS. For real use, put the request behind a small backend proxy.
