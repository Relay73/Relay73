# Relay73

Relay73 is a modular, open-development amateur radio project for digital messaging, data transfer, and station connectivity. The goal is to make different radio modems easier to use from one application ecosystem without tying every component to one modem or operating system.

**This repository is the parent project hub.** Application code, gateways, modem adapters, station discovery, and RF testing live in their own repositories so they can be developed, tested, and released independently.

> **Status:** Organization and repository setup. Existing prototypes are being organized for future migration; a published release is not available from this repository yet.

## Components

| Repository | Responsibility |
| --- | --- |
| [Relay73-ios](https://github.com/Relay73/Relay73-ios) | iPhone app, messages, radio controls, and hardware integration |
| [relay73-gateway](https://github.com/Relay73/relay73-gateway) | RMS gateway integration, modem control, and service orchestration |
| [relay73-directory](https://github.com/Relay73/relay73-directory) | Station discovery and published modem capabilities |
| [relay73-modem-adapters](https://github.com/Relay73/relay73-modem-adapters) | Integration interfaces for supported modem implementations |
| [relay73-rf-lab](https://github.com/Relay73/relay73-rf-lab) | Simulated RF links, interoperability tests, and performance benchmarks |

## Design principles

- **Modular:** Each component has a clear responsibility and independent development lifecycle.
- **Upstream-friendly:** Integrate upstream modem projects through adapters rather than maintaining unnecessary forks.
- **Interoperable:** Keep messaging and gateway functions independent of any one RF transport.
- **Practical:** Support real radio hardware, unreliable links, and attended field testing.
- **Discoverable:** Help operators find stations with compatible modem capabilities.

## System overview

```text
                   Relay73 apps
                        |
                 Transport adapters
                        |
           Radio / audio / PTT hardware
                        |
                Radio RF connection
                        |
                 Relay73 gateway ---- RMS / Winlink services
                        |
              Station capability directory
```

This is a conceptual overview, not a finalized protocol specification. Central discovery is intended to supplement station operation, not become a mandatory dependency for every connection.

## Development and collaboration

- Track component-specific defects and features in the appropriate repository.
- Use this parent repository for cross-component design and project-wide coordination.
- Keep modem implementations and their licenses independent from Relay73 adapter code.
- Preserve existing build and RF-test workflows while moving code into separate repositories.
- Document compatibility claims with actual tests, not builds alone.

## Getting started

Choose the relevant component in the table above. Each repository contains a summary of its intended scope and initial development priorities.

## Licensing and radio operation

License terms and contribution guidelines will be added before publishing source releases. Upstream dependencies retain their own licenses. Operate only under applicable amateur-radio rules and station-control requirements.

Relay73 is an independent project, not an official Winlink or modem-vendor product.
