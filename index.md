---
layout: default
---

This page contains a **community-maintained list of Ethereum historical data endpoints**, including **Era1, Era, E2SS, E2HS files, and torrents**.

> ⚠️ This list should not be treated as a single source of truth for these endpoints, or the data they provide. It is a **community-maintained list**, and as such, some endpoints listed here may not be up to date, or may not provide the data they claim to be providing.

Historical data providers offer **four primary storage formats**:
- **Era1** [Spec](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era1.md) - Execution layer historical block data **before The Merge**.
- **Era** [Spec](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era.md) - Stores data from the genesis of the Beacon Chain onwards. Can be used by Execution layer clients for history **from The Merge onward**, including historical block data.
- **E2SS** [Spec](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/e2ss.md) - **State snapshots** for execution clients.
- **E2HS** [Spec](https://github.com/eth-clients/e2store-format-specs/blob/main/formats/e2hs.md) - **full execution layer history** for execution clients, provides data from genesis to latest, headers are accompanied by proofs of canonicalness.
- **Erb** [Spec](https://github.com/status-im/nimbus-eth2/pull/5882) - Era file equivalent for blob sidecars [ ⚠️ Under Development ].

This registry is designed to **reduce reliance on centralized providers** by creating a **publicly accessible, decentralized list of historical data sources**. It aligns with **EIP-4444** and **Portal Network** efforts to ensure that Ethereum clients can obtain block history **beyond what traditional p2p sync provides**.
Additionally, some providers may distribute historical data through **torrents**, offering alternative sync options.

**Type** indicates whether the endpoint is a **torrent** or **web** endpoint.

If you'd like to add your endpoint to the list, please read the [documentation]({{ site.github.repository_url }}/blob/master/CONTRIBUTING.md).


---

## Endpoints

**Networks:**
{% for network in site.data.endpoints %}
  - [{{ network[0] | capitalize }}](#{{ network[0] }})
{% endfor %}

{% for network in site.data.endpoints %}
{% assign endpoints = network[1] | sample:99999 %}
### {{ network[0] | capitalize }}

| Format  | Name      |                 Endpoint                   | Type |            Contact Details             | Notes |
|:--------|:----------|:-------------------------------------------|------|:---------------------------------------|:------|{% for endpoint in endpoints %}
| {{ endpoint.format | capitalize }} | {{ endpoint.name }} | [{{ endpoint.endpoint }}]({{ endpoint.endpoint }}) | {% if endpoint.torrent %}torrent{% else %}web{% endif %} | {% if endpoint.contacts %}{% for contact in endpoint.contacts %}{% if contact.link %}[{{ contact.name }}]({{ contact.link }}){% else %}{{ contact.name }}{% endif %} {% endfor %}{% endif %} | {% if endpoint.notes %}{% for note in endpoint.notes %}{% if note.link %}[{{ note.name }}]({{ note.link }}){% else %}{{ note.name }}{% endif %}{% endfor %}{% endif %} |{% endfor %}

{% endfor %}
