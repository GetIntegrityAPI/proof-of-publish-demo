# Proof of Publish Demo

This repository demonstrates how to use `GetIntegrityAPI/proof-of-publish@v1` in a consumer GitHub repository.

## What this demo shows

- a GitHub Actions workflow calling the Proof of Publish action
- a generated `proof_id`
- a public `receipt_url`
- downloadable workflow artifacts:
  - `receipt.json`
  - `receipt.sha256`
  - `receipt.pdf`

## How it works

1. The workflow runs on push or manual dispatch.
2. The action generates a signed publish proof.
3. GitHub Actions uploads the receipt artifacts.
4. The verification URL can be opened publicly.

## Secret required

Add this repository secret before running the workflow:

- `GI_API_KEY`

## Action used

```yaml
uses: GetIntegrityAPI/proof-of-publish@v1
