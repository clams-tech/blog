+++
title = "Release v0.3.0"
date = 2025-01-04
+++

# Custom Imports

Clams connects to many Bitcoin and Lightning wallets automatically. If your wallet isn’t supported yet, you can manually upload your transaction data using the CSV import feature.

To ensure Clams recognizes your transactions, format your CSV file with the correct transaction types, column names, and values. This guide explains the required formats and provides examples for each type.

---

## Transaction Types

Your CSV file must include a `type` column, and each row must have a value that tells Clams how to process it. Below are the available transaction types, required/optional columns, and examples.

---

### **INVOICE**

A BOLT11 or BOLT12 Lightning invoice where funds are being received to a self-custodial Lightning wallet or node.

| **Column Name(s)**                           | **Required?** | **Value Type**           |
| -------------------------------------------- | ------------- | ------------------------ |
| `timestamp` or `date`                        | required      | Timestamp                |
| `amount_btc`, `amount_sat`, or `amount_msat` | required      | Amount BTC, SAT, or MSAT |
| `id` or `reference`                          | required      | ID                       |
| `request`                                    | optional      | Invoice Request          |
| `zap`                                        | optional      | Zap                      |

**Example CSV Snippet**:

```
type,timestamp,amount_btc,id,request,zap
INVOICE,2024-10-04T15:30:45Z,0.01234567,invoice123,lnbc1p3zjth0pp5qqqsyqcyq5rqwzqf...,true
```

---

#### **PAY**

A payment to a BOLT11 or BOLT12 Lightning invoice where funds are being sent from a Lightning wallet or node that is self-custodial.

| **Valid Column Name(s)**                     | **Required?** | **Value Type**           |
| -------------------------------------------- | ------------- | ------------------------ |
| `timestamp` or `date`                        | required      | Timestamp                |
| `amount_btc`, `amount_sat`, or `amount_msat` | required      | Amount BTC, SAT, or MSAT |
| `id` or `reference`                          | required      | ID                       |
| `request`                                    | optional      | Invoice Request          |
| `zap`                                        | optional      | Zap                      |
| `fee_btc`, `fee_sat`, or `fee_msat`          | optional      | Amount BTC, SAT, or MSAT |

**Example CSV Snippet**:

```
type,timestamp,amount_btc,id,fee_btc
PAY,2024-10-05T12:00:00Z,0.00567890,payment456,0.00004567
```

---

#### **DEPOSIT**

A deposit into a custodial wallet. This could involve depositing Bitcoin via Lightning or on-chain, or fiat into an exchange.

| **Valid Column Name(s)** | **Required?**                                                             | **Value Type**               |
| ------------------------ | ------------------------------------------------------------------------- | ---------------------------- |
| `timestamp` or `date`    | required                                                                  | Timestamp                    |
| `amount`                 | required                                                                  | Amount BTC or Fiat           |
| `id` or `reference`      | required                                                                  | ID or Lightning Payment Hash |
| `asset`                  | required                                                                  | Asset                        |
| `btc_destination`        | required if `asset` is BTC and `id` is not a valid lightning payment hash | BTC Destination              |
| `fee`                    | optional                                                                  | Amount BTC or Fiat           |

**Example CSV Snippet**:

```
type,timestamp,amount,asset,id
DEPOSIT,2024-10-06T14:25:00Z,500,USD,deposit789
```

---

#### **WITHDRAWAL**

A withdrawal from a custodial wallet. This could involve withdrawing Bitcoin via Lightning or on-chain or withdrawing fiat from an exchange.

| **Valid Column Name(s)** | **Required?**                                                             | **Value Type**               |
| ------------------------ | ------------------------------------------------------------------------- | ---------------------------- |
| `timestamp` or `date`    | required                                                                  | Timestamp                    |
| `amount`                 | required                                                                  | Amount BTC or Fiat           |
| `id` or `reference`      | required                                                                  | ID or Lightning Payment Hash |
| `asset`                  | required                                                                  | Asset                        |
| `btc_destination`        | required if `asset` is BTC and `id` is not a valid lightning payment hash | BTC Destination              |
| `fee`                    | optional                                                                  | Amount BTC or Fiat           |

**Example CSV Snippet**:

```
type,timestamp,amount,asset,id,btc_destination
WITHDRAWAL,2024-10-07T16:45:00Z,0.5,BTC,withdrawal101,bc1qxy2kgdygjrsqtzq2n0yrf2493p83kkfjhx0wlh
```

---

#### **TRADE**

A trade from one asset to another. This could involve buying or selling Bitcoin for fiat.

| **Valid Column Name(s)** | **Required?** | **Value Type**     |
| ------------------------ | ------------- | ------------------ |
| `timestamp` or `date`    | required      | Timestamp          |
| `from_amount`            | required      | Amount BTC or Fiat |
| `to_amount`              | required      | Amount BTC or Fiat |
| `fee_amount`             | optional      | Amount BTC or Fiat |
| `id` or `reference`      | required      | ID                 |
| `from_asset`             | required      | Asset              |
| `to_asset`               | required      | Asset              |
| `fee_asset`              | optional      | Asset              |
| `trade_id`               | optional      | ID                 |
| `order_id`               | optional      | ID                 |

**Example CSV Snippet**:

```
type,timestamp,from_amount,from_asset,to_amount,to_asset,fee_amount,fee_asset
TRADE,2024-10-08T18:00:00Z,0.1,BTC,3000,USD,5,USD
```

---

### Value Types

#### **Timestamp**

All timestamps need to be in UTC timezone and follow a valid RFC 3339 format, unix timestamp in seconds, or one of the custom formats below:
Examples:

- 2024-10-04T15:30:45Z
- 2024-10-04T15:30:45+00:00
- 2024-10-04T15:30:45.123Z
- 2024-10-04T15:30:45.123456Z
- 1728055845.123
- 2024-10-04T00:00:00Z
- 04/10/2024 5:07:59 AM

---

#### **ID**

A unique ID for this transaction. This can be any value as long as it is unique to the transaction and wallet. Examples:

- invoice123
- trade789

---

#### **Amount BTC**

Bitcoin denominated amount with up to 8 decimal places. Examples:

- 0.13850031
- 1.000045
- 0.00000001

---

#### **Amount SAT**

SATS denominated Bitcoin amount. Examples:

- 400
- 234

---

#### **Amount Fiat**

Fiat amount as a decimal. Examples:

- 4.32
- 9589.47

---

#### **Invoice Request**

A BOLT11 or BOLT12 Lightning invoice request. Example:

- lnbc1p3zjth0pp5qqqsyqcyq5rqwzqfqqqsyqcyq5rqwzqfqqqsyqcyq5rqwzqfqypqdpl2pkx2ctnv5sxxmmwwd5kgetjypeh2ursdae8gxqyjw5qcqpjrzjqwfn3p9278ttzzpe0e00uhyxhned3j5d9acqak5emwfpflp8zqpsp5lraer6xyeztnadn8m3rpppr5v2zx3l2r7t70rdjlxe2qup2n7tzs9qyyssqapu4gv3h9y8q2ds73xge4pxx5vet4nvavhxk4gs05vjcl2jr5jzr3zoxw4zaxz7rl6rs2lc3g2yxlqfpk8n6k5jfj9z4xr6z9l6wjlhrxqpl66lrm

---

#### **BTC Destination**

An on-chain address, BOLT11 invoice, or BOLT12 invoice. Examples:

- bc1qweq8vxpsvx3d89uvp65qgwjql68s4e43csgtvf
- lnbc1p3zjth0pp...

---

#### **Zap**

Boolean indicating if this is a NOSTR zap. Examples:

- true
- false

---

#### **Asset**

The asset being transacted. Examples:

- BTC
- USD
- EUR
- GBP
- CNY
- JPY
- CAD
- AUD
- HKD
- SGD
- SEK
- CHF
- THB
- PLN
- NOK
- MYR
- DKK
- ZAR
- NZD
- MXN
- RUB

---

### Checklist Before Uploading

- [ ] File includes a `type` column with valid transaction types.
- [ ] All required columns for each type are filled.
- [ ] Timestamps follow UTC and a supported format.
- [ ] Values are correctly formatted (e.g., BTC amounts, SATs, or fiat).

If your file meets these requirements, you’re ready to upload it to Clams.
