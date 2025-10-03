---
title: "Ethereum history providers"
---

The Ethereum blockchain consists of all block and transaction data from genesis. Clients store this data by default, but it is not needed to validate new blocks added to the chain. Because of this and because the historical chain is large, >1TB in many instances, most clients support pruning older blocks in accordance with [EIP-4444][4444]. In order to retain a high guarantee of availability, we offer the following community curated list of data providers.

Below is a list of providers offering complete historical archive of the Ethereum protocol. While many nodes store this data locally, some newer forms of nodes may choose to implement EIP-4444 and only download recent history and account state to verify blocks. These archives are made available for historical inspection, client bootstrapping, and independent verification.

For more information on the archive formats see the specifications for [`era1`][era1] and [`era`][era]. To use these endpoints and data files, consult the corresponding Ethereum client documentation.

## Proof-of-work chain

The proof-of-work chain preceeded the current proof-of-stake chain and has a
slightly different format for block data. Only Mainnet and Sepolia remain as
active networks with a PoW prefix. 

### Mainnet

Historical data starting at genesis on July 30, 2015 and ending at the merge block 15537393 on September 15, 2022 is available from the following sources.

- [Magnet link <img src="https://torrindex.net/images/icon-magnet.gif" style="vertical-align: middle; height: 1em; width: 1em; margin: 0px; display: inline;"/>][magnet]
- [Torrent file](https://ethereum-mainnet-pre-merge-era-files.fra1.cdn.digitaloceanspaces.com/EthereumMainnetPreMergeEraFiles.torrent)
- Mirrors
    - [https://data.ethpandaops.io/era1/mainnet/](https://data.ethpandaops.io/era1/mainnet/)
    - [https://mainnet.era1.nimbus.team](https://mainnet.era1.nimbus.team/)

### Sepolia

- Magnet link (TBA)
- Torrent link (TBA)
- Mirrors
    - [https://data.ethpandaops.io/era1/sepolia/](https://data.ethpandaops.io/era1/sepolia/)
    - [https://sepolia.era1.nimbus.team](https://mainnet.era1.nimbus.team/)

Each file can be verified for correctness by importing into a supporting Ethereum client. For fast verification, each `era1` source includes a list of `sha256`  hashes in `checksums.txt` that correspond with every `era1` file.

## Proof-of-stake chain

All historical beacon chain data for the corresponding networks is available from the following sources.

### Mainnet

- Mirrors
    - [https://mainnet.era.nimbus.team](https://mainnet.era.nimbus.team/)

### Sepolia

- Mirrors
    - [https://sepolia.era.nimbus.team](https://sepolia.era.nimbus.team/)

### Holesky

- Mirrors
    - [https://holesky.era.nimbus.team](https://holesky.era.nimbus.team/)

### Hoodi

- Mirrors
    - [https://hoodi.era.nimbus.team](https://hoodi.era.nimbus.team/)

Each epoch corresponds to a value in the beacon state’s `historical_roots` accumulator. This allows for quick verification and proving of specific elements.

## Joining the mirror list

If your organization is interested in hosting historical data and being listed as a mirror here, please send an email to `historydata@ethereum.org` .

[era1]: https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era1.md
[era]: https://github.com/eth-clients/e2store-format-specs/blob/main/formats/era.md
[4444]: https://eips.ethereum.org/EIPS/eip-4444
[magnet]: magnet:?xt=urn:btih:edcc7c112bae520e3226065a61817d3575904e0d&dn=EthereumMainnetPreMergeEraFiles&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fopen.tracker.cl%3A1337%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fopentracker.io%3A6969%2Fannounce&tr=https%3A%2F%2Ftracker.gbitt.info%3A443%2Fannounce&tr=http%3A%2F%2Ftracker.gbitt.info%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.0x7c0.com%3A6969%2Fannounce&tr=udp%3A%2F%2Frun.publictracker.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Fretracker01-msk-virt.corbina.net%3A80%2Fannounce&tr=udp%3A%2F%2Fretracker.lanta.me%3A2710%2Fannounce&tr=udp%3A%2F%2Fopen.u-p.pw%3A6969%2Fannounce&tr=udp%3A%2F%2Foh.fuuuuuck.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmoonburrow.club%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fepider.me%3A6969%2Fannounce&tr=udp%3A%2F%2Famigacity.xyz%3A6969%2Fannounce&tr=https%3A%2F%2Ftracker.tamersunion.org%3A443%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.theoks.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.dump.cl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.bittor.pw%3A1337%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fleet-tracker.moe%3A1337%2Fannounce&tr=https%3A%2F%2Ftracker.renfei.net%3A443%2Fannounce&tr=http%3A%2F%2Ftracker.renfei.net%3A8080%2Fannounce&tr=https%3A%2F%2Ftracker.loligirl.cn%3A443%2Fannounce&tr=http%3A%2F%2Ftracker1.bt.moack.co.kr%3A80%2Fannounce&tr=http%3A%2F%2Ftracker.ipv6tracker.org%3A80%2Fannounce&tr=http%3A%2F%2Ftr.kxmp.cf%3A80%2Fannounce&tr=udp%3A%2F%2Fwepzone.net%3A6969%2Fannounce&tr=http%3A%2F%2Fwepzone.net%3A6969%2Fannounce&tr=udp%3A%2F%2Fttk2.nbaonlineservice.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker2.dler.org%3A80%2Fannounce&tr=http%3A%2F%2Ftracker2.dler.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker1.myporn.club%3A9337%2Fannounce&tr=udp%3A%2F%2Ftracker.tryhackx.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.srv00.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qu.ax%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.qu.ax%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.jamesthebard.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.fnix.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filemail.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.edkj.club%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.edkj.club%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.dler.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.dler.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.deadorbit.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ccp.ovh%3A6969%2Fannounce&tr=udp%3A%2F%2Ftamas3.ynh.fr%3A6969%2Fannounce&tr=udp%3A%2F%2Fryjer.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fpublic.tracker.vraphim.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fpublic.publictracker.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Fp2p.publictracker.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.free-tracker.ga%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.dstud.io%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonoid.ch%3A6969%2Fannounce&tr=udp%3A%2F%2Fodd-hd.fr%3A6969%2Fannounce&tr=udp%3A%2F%2Fnew-line.net%3A6969%2Fannounce&tr=udp%3A%2F%2Fjutone.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fisk.richardsw.club%3A6969%2Fannounce&tr=udp%3A%2F%2Fipv4.rer.lol%3A2710%2Fannounce&tr=udp%3A%2F%2Fevan.im%3A6969%2Fannounce&tr=udp%3A%2F%2Fbt2.archive.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fbt1.archive.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fbt.ktrackers.com%3A6666%2Fannounce&tr=udp%3A%2F%2Fbittorrent-tracker.e-n-c-r-y-p-t.net%3A1337%2Fannounce&tr=http%3A%2F%2Fbittorrent-tracker.e-n-c-r-y-p-t.net%3A1337%2Fannounce&tr=udp%3A%2F%2F6ahddutb1ucc3cp.ru%3A6969%2Fannounce&tr=udp%3A%2F%2F1c.premierzal.ru%3A6969%2Fannounce&tr=https%3A%2F%2Ftracker.yemekyedim.com%3A443%2Fannounce&tr=https%3A%2F%2Ftracker.lilithraws.org%3A443%2Fannounce&tr=https%3A%2F%2Ftracker.cloudit.top%3A443%2Fannounce&tr=https%3A%2F%2Ftr.ready4.icu%3A443%2Fannounce&tr=http%3A%2F%2Ftracker.mywaifu.best%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.files.fm%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.bt4g.com%3A2095%2Fannounce&tr=http%3A%2F%2Ft1.aag.moe%3A17715%2Fannounce&tr=http%3A%2F%2Ft.overflow.biz%3A6969%2Fannounce&tr=udp%3A%2F%2Fu.peer-exchange.download%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.therarbg.to%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.therarbg.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ddunlimited.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.darkness.services%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrents.artixlinux.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ffh2.cmp-gaming.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fconcen.org%3A6969%2Fannounce&tr=udp%3A%2F%2Faegir.sexy%3A6969%2Fannounce&tr=https%3A%2F%2Ftrackers.run%3A443%2Fannounce&tr=https%3A%2F%2Ftracker.pmman.tech%3A443%2Fannounce&tr=https%3A%2F%2Ftracker.ipfsscan.io%3A443%2Fannounce&tr=https%3A%2F%2Ftracker.gcrenwp.top%3A443%2Fannounce&tr=http%3A%2F%2Ftracker1.itzmx.com%3A8080%2Fannounce&tr=http%3A%2F%2Fregion.nl1.privex.cc%3A6969%2Fannounce&tr=http%3A%2F%2Fch3oh.ru%3A6969%2Fannounce&tr=http%3A%2F%2Fbvarf.tracker.sh%3A2086%2Fannounce&tr=udp%3A%2F%2F93.158.213.92%3A1337%2Fannounce&tr=http%3A%2F%2F93.158.213.92%3A1337%2Fannounce&tr=udp%3A%2F%2F23.168.232.9%3A1337%2Fannounce&tr=udp%3A%2F%2F185.243.218.213%3A80%2Fannounce&tr=udp%3A%2F%2F208.83.20.20%3A6969%2Fannounce&tr=udp%3A%2F%2F45.9.60.30%3A6969%2Fannounce&tr=udp%3A%2F%2F23.153.248.83%3A6969%2Fannounce&tr=udp%3A%2F%2F15.204.56.171%3A6969%2Fannounce&tr=udp%3A%2F%2F83.102.180.21%3A80%2Fannounce&tr=udp%3A%2F%2F37.235.176.37%3A2710%2Fannounce&tr=udp%3A%2F%2F37.27.4.53%3A6969%2Fannounce&tr=udp%3A%2F%2F167.99.185.219%3A6969%2Fannounce&tr=udp%3A%2F%2F23.157.120.14%3A6969%2Fannounce&tr=udp%3A%2F%2F51.68.174.87%3A6969%2Fannounce&tr=udp%3A%2F%2F96.126.98.54%3A6969%2Fannounce&tr=udp%3A%2F%2F83.146.118.175%3A6969%2Fannounce&tr=udp%3A%2F%2F185.230.4.150%3A1337%2Fannounce&tr=http%3A%2F%2F156.234.201.18%3A80%2Fannounce&tr=http%3A%2F%2F34.94.76.146%3A80%2Fannounce&tr=http%3A%2F%2F35.227.59.57%3A80%2Fannounce&tr=udp%3A%2F%2F83.6.225.179%3A6969%2Fannounce&tr=http%3A%2F%2F83.6.225.179%3A6969%2Fannounce&tr=udp%3A%2F%2F54.39.48.3%3A6969%2Fannounce&tr=udp%3A%2F%2F125.227.79.123%3A80%2Fannounce&tr=http%3A%2F%2F125.227.79.123%3A80%2Fannounce&tr=udp%3A%2F%2F193.42.111.57%3A9337%2Fannounce&tr=udp%3A%2F%2F135.125.202.143%3A6969%2Fannounce&tr=udp%3A%2F%2F89.110.76.229%3A6969%2Fannounce&tr=udp%3A%2F%2F143.198.64.177%3A6969%2Fannounce&tr=udp%3A%2F%2F5.255.124.190%3A6969%2Fannounce&tr=udp%3A%2F%2F52.58.128.163%3A6969%2Fannounce&tr=udp%3A%2F%2F15.204.57.168%3A6969%2Fannounce&tr=http%3A%2F%2F15.204.57.168%3A6969%2Fannounce&tr=udp%3A%2F%2F211.23.142.127%3A6969%2Fannounce&tr=http%3A%2F%2F211.23.142.127%3A6969%2Fannounce&tr=udp%3A%2F%2F64.23.195.62%3A6969%2Fannounce&tr=udp%3A%2F%2F176.31.250.174%3A6969%2Fannounce&tr=udp%3A%2F%2F82.156.24.219%3A6969%2Fannounce&tr=udp%3A%2F%2F51.15.41.46%3A6969%2Fannounce&tr=udp%3A%2F%2F107.175.221.194%3A6969%2Fannounce&tr=udp%3A%2F%2F176.123.1.180%3A6969%2Fannounce&tr=udp%3A%2F%2F5.181.156.41%3A6969%2Fannounce&tr=udp%3A%2F%2F198.12.89.149%3A6969%2Fannounce&tr=udp%3A%2F%2F62.210.114.129%3A6969%2Fannounce&tr=udp%3A%2F%2F94.243.222.100%3A6969%2Fannounce&tr=udp%3A%2F%2F121.199.16.229%3A6969%2Fannounce&tr=udp%3A%2F%2F117.29.108.216%3A2710%2Fannounce&tr=udp%3A%2F%2F23.163.56.66%3A6969%2Fannounce&tr=udp%3A%2F%2F207.241.231.226%3A6969%2Fannounce&tr=udp%3A%2F%2F207.241.226.111%3A6969%2Fannounce&tr=udp%3A%2F%2F51.159.54.68%3A6666%2Fannounce&tr=udp%3A%2F%2F104.244.77.14%3A1337%2Fannounce&tr=http%3A%2F%2F104.244.77.14%3A1337%2Fannounce&tr=udp%3A%2F%2F185.189.13.108%3A6969%2Fannounce&tr=http%3A%2F%2F93.185.165.29%3A6969%2Fannounce&tr=http%3A%2F%2F95.217.167.10%3A6969%2Fannounce&tr=http%3A%2F%2F159.148.57.222%3A6969%2Fannounce&tr=http%3A%2F%2F191.23.62.7%3A6969%2Fannounce&tr=udp%3A%2F%2F130.61.158.165%3A6969%2Fannounce&tr=udp%3A%2F%2F89.213.174.212%3A6969%2Fannounce&tr=udp%3A%2F%2F116.202.49.58%3A6969%2Fannounce&tr=udp%3A%2F%2F37.59.48.81%3A6969%2Fannounce&tr=udp%3A%2F%2F51.15.26.25%3A6969%2Fannounce&tr=http%3A%2F%2F185.130.47.2%3A6969%2Fannounce&tr=http%3A%2F%2F5.182.86.242%3A6969%2Fannounce&tr=udp%3A%2F%2F186.10.181.37%3A1337%2Fannounce&tr=udp%3A%2F%2F104.244.77.87%3A6969%2Fannounce
