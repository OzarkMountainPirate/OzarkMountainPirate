## Carl Alcott

Systems & Network Administrator · Infrastructure & Security Engineer

Building and operating infrastructure since 2005, across managed services,
K-12, and higher education.

Windows Server and Active Directory, Microsoft 365 and Exchange, VMware and
Hyper-V, multi-vendor switching and firewalls, campus networks, and security
operations — alongside the Linux, detection, and automation work below.

**[resume.alcott.dev](https://resume.alcott.dev)** · Lake of the Ozarks, Missouri

---

### Currently running

A three-host Linux environment used to build and validate infrastructure and
security tooling:

- **Detection** — Suricata IDS feeding Elasticsearch and Kibana through
  syslog-ng and Logstash, with GeoIP enrichment
- **Prevention** — CrowdSec across the fleet, with a bouncer at each host's
  reverse proxy
- **Edge** — Traefik behind Cloudflare Tunnel; no inbound ports on any host
- **Storage** — ZFS snapshots, raw-encrypted replication on site, encrypted
  offsite backup
- **Platform** — Docker with a socket proxy in front of the API and
  file-based secrets

### Repositories

| | |
|---|---|
| **[suricata-elk](https://github.com/OzarkMountainPirate/suricata-elk)** | pfSense and Suricata EVE logs into a self-hosted ELK stack over TCP, with GeoIP enrichment and a scoped, non-superuser ingest path. |
| **[ark-fleet](https://github.com/OzarkMountainPirate/ark-fleet)** | Infrastructure as code from bare metal up — PXE unattended install, Ansible configuration management, lint CI on every push. |
| **[utilities](https://github.com/OzarkMountainPirate/utilities)** | Linux administration tooling, including a 3-2-1 ZFS backup stack built on Sanoid, Syncoid and Restic. |
| **[sslh-vpn-edge](https://github.com/OzarkMountainPirate/sslh-vpn-edge)** | A web server and an OpenVPN endpoint sharing one IP and one TCP port, documented down to how conformance-based detection classifies the result. |
| **[resume-site](https://github.com/OzarkMountainPirate/resume-site)** | The site above. Built by CI and deployed over an access-controlled tunnel to a host with no inbound ports — source and pipeline both public. |

Each repository documents a working deployment rather than a tutorial, and
every one of them is GPL-3.0 or MIT.
