# Ethereum Historical Data Endpoints

This page contains a **community-maintained list of Ethereum historical data endpoints**, including **Era1, Era, E2SS, E2HS files, and torrents**.

> ⚠️ This list should not be treated as a single source of truth for these endpoints, or the data they provide. It is a **community-maintained list**, and as such, some endpoints listed here may not be up to date, or may not provide the data they claim to be providing.

Historical data providers offer **three primary storage formats**:
- [**Era1**(Pre-Merge Execution History)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era1.md) - Archive nodes providing **execution layer history** before The Merge (ETH1).
- [**Era**(Beacon Chain History)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era.md) - Stores data from the genesis of the Beacon Chain onwards. Can be used by Execution layer clients for history **from The Merge onward**, including historical block data.
- [**E2SS**(Execution State)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/e2ss.md) - **State snapshots** for execution clients.
- [**E2HS**(Execution Layer History)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/e2hs.md) - **full execution layer history** for execution clients, provides data from genesis to latest, headers are accompanied by proofs of canonicalness.
- **Erb**(Blob) - Era file equivalent for blob sidecars [ ⚠️ Under Development ].

This registry is designed to **reduce reliance on centralized providers** by creating a **publicly accessible, decentralized list of historical data sources**. It aligns with **EIP-4444** and **Portal Network** efforts to ensure that Ethereum clients can obtain block history **beyond what traditional p2p sync provides**.
Additionally, some providers may distribute historical data through **torrents**, offering alternative sync options.

**Type** indicates whether the endpoint is a **torrent** or **web** endpoint.
-----
<p align="center" style="display: inline-block"> 
  <a target=”_blank” href="https://eth-clients.github.io/history-endpoints">View the list here </a>
</p>

-----

# Contributing

If you'd like to add your endpoint to the list please read the [documentation](./CONTRIBUTING.md).

## Credits

This repository is based on the template from [eth-clients/checkpoint-sync-endpoints](https://github.com/eth-clients/checkpoint-sync-endpoints), adapted to list **Ethereum execution layer historical data providers** instead of Beacon Chain checkpoint sync sources.  

Thanks to the broader **Ethereum community** for supporting decentralized historical data distribution.

---

🚀 Let's decentralize historical data access! 🚀
