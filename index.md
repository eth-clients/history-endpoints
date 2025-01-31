---
layout: default
---

This page contains a **community-maintained list of Ethereum historical data endpoints**, including **Era1, Era, E2ss files, and torrents**.

> ⚠️ This list should not be treated as a single source of truth for these endpoints, or the data they provide. It is a **community-maintained list**, and as such, some endpoints listed here may not be up to date, or may not provide the data they claim to be providing.

Historical data providers offer **three primary storage formats**:
- **Era1** [Spec](https://github.com/ethereum/go-ethereum/pull/26621#issue-1573139029) - Execution layer historical block data **before The Merge**.
- **Era** [Spec](https://github.com/status-im/nimbus-eth2/blob/613f4a9a50c9c4bd8568844eaffb3ac15d067e56/docs/e2store.md#era-files) - Consensys layer historical block data **from The Merge onward**.
- **E2ss** [Spec](https://github.com/ethereum/trin/blob/62dd518a88eda8496f89db9f9c149231a2c326dc/e2store/src/era2.rs#L24-L37) - **State snapshots** for execution clients.
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
