# Ethereum Historical Data Endpoints

This page contains a **community-maintained list of Ethereum historical data endpoints**.

> ⚠️ This list should not be treated as a single source of truth for these endpoints, or the data they provide. It is a **community-maintained list**, and as such, some endpoints listed here may not be up to date, or may not provide the data they claim to be providing.

Historical data providers offer **three archive formats**:
- [**Ere**(Execution History)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/ere.md) - Stores **execution layer history** over the full range of the chain, from genesis across The Merge and onwards. Supersedes Era1 and is the format to use for new execution layer archives.
- [**Era1**(Pre-Merge Execution History)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era1.md) - Archive nodes providing **execution layer history** before The Merge (ETH1).
- [**Era**(Beacon Chain History)](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era.md) - Stores data from the genesis of the Beacon Chain onwards. Until the Gloas fork it also carries the execution blocks as payloads, which Execution layer clients can use for history **from The Merge until Gloas**.

This registry is designed to **reduce reliance on centralized providers** by creating a **publicly accessible, decentralized list of historical data sources**. It aligns with **EIP-4444** to ensure that Ethereum clients can obtain block history **beyond what the Ethereum p2p sync provides**.
Additionally, some providers may distribute historical data through **torrents**, offering alternative sync options.

<p align="center" style="display: inline-block">
  <a target=”_blank” href="https://eth-clients.github.io/history-endpoints">View the list here </a>
</p>

-----

# Contributing

If you'd like to add your endpoint to the list please read the [documentation](./CONTRIBUTING.md).

## Credits

This repository is based on the template from [eth-clients/checkpoint-sync-endpoints](https://github.com/eth-clients/checkpoint-sync-endpoints), adapted to list **Ethereum execution layer historical data providers** instead of Beacon Chain checkpoint sync sources.

Thanks to the broader **Ethereum community** for supporting decentralized historical data distribution.
