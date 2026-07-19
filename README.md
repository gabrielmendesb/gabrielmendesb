# Gabriel Mendes Bonato

**Full-Stack Software Engineer · Industrial IoT & Energy** — Araraquara, Brazil (GMT-3)

I build software that runs solar plants. Lead engineer of **MeuWatt**, a monitoring and
remote-control platform running across a fleet of utility-scale solar plants in Brazil.

> The platform is my employer's, so the repositories are private. This page is the case
> study — happy to go deep on the architecture and the reasoning behind it.

---

## The platform, end to end

**Edge.** A containerized Python collector per plant, with a multi-vendor device layer:
register maps and drivers for inverters, protection relays, thermal relays, weather
stations, energy meters and RS-485 gateways. A fault-detection state machine follows each
inverter through its daily lifecycle, and polling is built for unreliable field networks.

**Cloud API.** Ingests telemetry from every plant and serves monitoring, generation
reports, alerting, and energy-loss attribution against a peer baseline — idempotent and
replay-safe.

**Remote operations.** An audited command rail carries operator actions to plant
equipment — configuration and power state, every mutation authenticated, two-factor
gated, and logged end to end. Collectors update themselves over the same rail.

**Frontend.** The daily working surface for plant operators: real-time monitoring,
generation and availability reporting, breakdown management, and fleet health.

**Delivery.** From commit to a running plant: automated tests, image builds, cloud
deploys, and Ansible fleet rollout, with centralized logging across all sites.

**Field tooling.** A desktop tool technicians run inside the plant network to probe and
validate any device before go-live.

---

## How I work

**End to end.** I can carry a system the whole way — architecture, data model,
implementation, rollout, and whatever it does in production afterwards. I work best with
real autonomy and a say in the decisions that matter, on a team or on my own.

**In production.** I operate what I ship. Design choices are made with operations in
mind — idempotency, replay safety, observability — because I'm the one who answers when
they're wrong.

**AI-native.** Agentic tooling (Claude Code, MCP) is my daily method. Conventions live in
context files agents load every session; tests and review hold the merge bar. The
leverage is real and the accountability stays mine. Currently building an AI analytics
layer on fleet telemetry — structuring time-series into training-ready datasets and
evaluating ML/LLM pipelines for automated operational insight.

**Stack:** Python · FastAPI · SQLAlchemy/Alembic · PostgreSQL · TimescaleDB ·
TypeScript · React · Vite · Docker · Ansible · GitHub Actions · WebSockets ·
OAuth2/JWT · TOTP 2FA · Modbus TCP

---

## Contact

[gabrielmbona.to](https://gabrielmbona.to) ·
[gabriel.mbonato@gmail.com](mailto:gabriel.mbonato@gmail.com) ·
[LinkedIn](https://www.linkedin.com/in/g-mendes-bonato/)

Fluent English · Open to remote full-time and contract work — energy, climate, and
industrial IoT.
