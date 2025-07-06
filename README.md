# aprsc-9m2pju-git

Unofficial Arch Linux AUR package for the latest development version of [aprsc](https://github.com/hessu/aprsc), a high-performance APRS-IS core server daemon.

Maintained by [9M2PJU](https://github.com/9M2PJU) for experimentation, custom setups, and Arch Linux compatibility.

---

## 📦 What is `aprsc`?

[`aprsc`](https://github.com/hessu/aprsc) is a fast, lightweight, multithreaded APRS-IS server daemon written in C. It acts as the backbone server software for the global [APRS-IS](https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System) network, relaying packets between users, IGates, and repeaters.

Key features:

- Fully multithreaded design
- Supports thousands of simultaneous connections
- Implements APRS-IS filtering
- Includes a web status interface
- Supports SSL/TLS and SCTP

---

## ⚙️ About This AUR Package

This package builds the latest **git version** of `aprsc` with upstream sources from:

📎 https://github.com/hessu/aprsc

It installs `aprsc` into `/opt/aprsc`, includes a systemd service, and prepares directories for logs and configuration.

---

## 🛠️ Installation

Using an [AUR helper](https://wiki.archlinux.org/title/AUR_helpers) like `yay`:

```bash
yay -S aprsc-9m2pju-git
```

Or manually:

```bash
git clone https://aur.archlinux.org/aprsc-9m2pju-git.git
cd aprsc-9m2pju-git
makepkg -si
```

---

## 📂 Files Installed

- `/opt/aprsc/` – aprsc binary, config, logs, web files
- `/usr/lib/systemd/system/aprsc.service` – systemd service file
- `/usr/lib/sysusers.d/aprsc.conf` – creates `aprsc` system user
- `/usr/lib/tmpfiles.d/aprsc.conf` – handles `/opt/aprsc/logs` and data dir

---

## 🧪 Run the Server

After installation, start the server:

```bash
sudo systemctl enable --now aprsc.service
```

Logs can be found in `/opt/aprsc/logs/`.

Default config: `/opt/aprsc/etc/aprsc.conf`

---

## 🧾 Notes

- APRS-IS login requires a valid callsign and passcode.
- Configuration must be customized before public operation.
- This version follows the latest upstream `main` branch.

---

## 🙏 Special Thanks

Big thanks to:

- **[Heikki Hannikainen (hessu)](https://github.com/hessu)** – original author and maintainer of [aprsc](https://github.com/hessu/aprsc)
- **Arch Linux AUR community** – for making it easy to package and distribute software on Arch-based systems

---

## 📫 Maintainer

- Callsign: **9M2PJU**
- GitHub: [@9M2PJU](https://github.com/9M2PJU)
- Email: [9m2pju@hamradio.my](mailto:9m2pju@hamradio.my)

---

## 📜 License

This package and upstream `aprsc` are licensed under the [GPLv2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html).

---

## 🔗 Links

- [Upstream GitHub (hessu/aprsc)](https://github.com/hessu/aprsc)
- [APRS-IS Wiki](https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System)
- [AUR Package](https://aur.archlinux.org/packages/aprsc-9m2pju-git)
