# README.md

## HB142 Verification Bridge
**High-Integrity Age Verification for the State of Louisiana**

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Framework](https://img.shields.io/badge/Framework-Laravel_11.x-red)](https://laravel.com)
[![Database](https://img.shields.io/badge/Database-MariaDB_10.11+-green)](https://mariadb.org)

---

## ⚖️ Legal Context
This repository provides a standardized technical implementation for **Louisiana House Bill 142 (HB142)**. It is designed to meet "commercially reasonable" standards for verifying the age of individuals attempting to access restricted digital content within the jurisdiction of Louisiana.

## 🛠 Features
*   **Privacy-First Architecture:** Implements a "Zero-PII" retention policy. Once verification is hashed, raw identity data is purged from the execution layer.
*   **LA Wallet Integration:** Service providers pre-configured for the Louisiana OMV digitized ID API.
*   **Instance-Aware Execution:** Built-in logic gates for **Instance Beta** (Isolated Testing) and **Instance Alpha** (Authoritative Live Layer).
*   **Integrity Hashing:** Every verification event generates a unique `integrity_hash` (compatible with the 43565742305011987LA signature format) to prevent database tampering.

## 🚀 Quick Start

### 1. Requirements
*   PHP 8.2+
*   MariaDB 10.11+
*   Composer

### 2. Installation
```bash
composer require alotttajaffray-global/hb142
php artisan migrate
```

### 3. Configuration
Add your state-issued API credentials to your `.env` file:
```env
LA_WALLET_API_KEY=your_key_here
LA_WALLET_ENVIRONMENT=sandbox # Use 'production' for Instance Alpha
AGE_GATE_RETENTION_DAYS=0 # Default to 0 for maximum privacy compliance
```

## 🏗 Schema Design
The framework utilizes a hardened `user_age_verifications` table in MariaDB, ensuring that only the *status* of the user is stored, never the *document* itself. This aligns with the **Grandma Code** principles of honor and privacy.

## 📜 License
Distributed under the **Apache License 2.0**. See `LICENSE` for more information.

---
**Maintained by:** JaffNet Industrial Ecosystem | St. Tammany Parish, LA
