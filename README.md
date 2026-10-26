<div align="center">

<img src="snap/gui/drawdb.png" alt="drawDB logo" width="128" />

# drawDB

**Design database diagrams in your browser.**

[![drawdb](https://snapcraft.io/drawdb/badge.svg)](https://snapcraft.io/drawdb)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [drawDB](https://github.com/drawdb-io/drawdb), a database diagram editor and SQL generator.

</div>

---

## Getting Started

<a href="https://snapcraft.io/drawdb"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install drawdb
```

Open [http://127.0.0.1:3000/editor](http://127.0.0.1:3000/editor). The service starts automatically.

Diagrams are saved in your browser. Use the same address, port and browser profile to find them again, and export diagrams for backups. Snap snapshots do not include browser data.

## Configure

| Setting | Accepted values | Default |
| --- | --- | --- |
| `address` | `host:port` or `[IPv6]:port`; port `1024`–`65535` | `127.0.0.1:3000` |

```bash
sudo snap get drawdb
sudo snap set drawdb address=0.0.0.0:3000
```

Changes restart the running service. `sudo snap unset drawdb address` restores the default. Use an HTTPS reverse proxy for internet access.

## Limitations

- Sharing, remote version history and in-app bug reports need the optional upstream backend, which is not included.
- Some editor assets, including the SQL editor, load from the internet.

## Build

```bash
git clone https://github.com/sidalit/drawdb-snap.git
cd drawdb-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/drawdb-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/drawdb-io/drawdb/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/drawdb-snap/blob/main/LICENSE).
