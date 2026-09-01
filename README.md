# FDA DSCSA & EU FMD Drug Serialization API (21 USC 360eee) — Rust Client

[![Crates.io](https://img.shields.io/crates/v/pharma-dscsa-client.svg)](https://crates.io/crates/pharma-dscsa-client)
[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/57865358-8bafe64c-1441-4fe3-ba7a-2d60bdeb7dc5)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![RapidAPI Listing](https://img.shields.io/badge/RapidAPI-Dedicated%20Listing-blueviolet)](https://rapidapi.com/noor-mkdad-apis-noor-mkdad-apis-default/api/us-fda-dscsa-eu-fmd-prescription-drug-serialization)

Official high-speed Rust client for **FDA DSCSA & EU FMD Drug Serialization API (21 USC 360eee)**.

> Instant <5ms US FDA DSCSA 4-element & EU FMD 2011/62/EU 2D DataMatrix barcode parser, Modulo-10 check digit validator, NDC-to-GTIN converter, and GS1 VRS engine on Cloudflare Workers edge.

> 🔑 **Get your Dedicated API Key:** [Subscribe to FDA DSCSA & EU FMD Drug Serialization API (21 USC 360eee) on RapidAPI](https://rapidapi.com/noor-mkdad-apis-noor-mkdad-apis-default/api/us-fda-dscsa-eu-fmd-prescription-drug-serialization)

---

## 🚀 Installation

```bash
cargo add pharma-dscsa-client
```

---

## ⚡ Quickstart

```rust
use pharma_dscsa_client::{PharmaDscsaClient, RapidApiConfig};
use serde_json::json;

fn main() -> Result<(), Box<dyn std::error::Error>> {
    let client = PharmaDscsaClient::new(Some(RapidApiConfig {
        api_key: "YOUR_RAPIDAPI_KEY".to_string(), // Get key from https://rapidapi.com/noor-mkdad-apis-noor-mkdad-apis-default/api/us-fda-dscsa-eu-fmd-prescription-drug-serialization
        ..Default::default()
    }));

    let result = client.validate(&json!({
        // Enter validation payload
    }))?;

    println!("Result: {:?}", result);
    Ok(())
}
```

---

## 🔗 Links
- 📖 [RapidAPI Documentation & Key](https://rapidapi.com/noor-mkdad-apis-noor-mkdad-apis-default/api/us-fda-dscsa-eu-fmd-prescription-drug-serialization)

## 📄 License
MIT © Noor Mkdad
