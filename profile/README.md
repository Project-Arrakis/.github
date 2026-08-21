<div align="center">

<!--
Optional branded banner.

Recommended path:
.github/profile/assets/project-arrakis-banner.png

Uncomment when ready:

<img src="./assets/project-arrakis-banner.png" alt="Project Arrakis" width="100%" />
-->

# 🏜️ Project Arrakis

### Dune: Awakening Self-Hosting Engineering & Community Operations

**Platform · Operations · Observability · Automation · Security · Quality · Community**

*Infrastructure for those who choose to operate Arrakis themselves.*

<br>

![Dune Awakening](https://img.shields.io/badge/Dune%3A%20Awakening-Self--Hosting-C97A40?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-Platform-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Infrastructure-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Prometheus](https://img.shields.io/badge/Prometheus-Observability-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-Operations-F46800?style=for-the-badge&logo=grafana&logoColor=white)

![Security](https://img.shields.io/badge/Security-DevSecOps-2E8B57?style=flat-square)
![SRE](https://img.shields.io/badge/SRE-Reliability-5C6BC0?style=flat-square)
![Quality](https://img.shields.io/badge/Quality-SDET-8E44AD?style=flat-square)
![Automation](https://img.shields.io/badge/Automation-GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Community](https://img.shields.io/badge/Community-Dune%20Awakening-555555?style=flat-square)

</div>

---

## 🏜️ What is Project Arrakis?

**Project Arrakis** is an open-source engineering and community ecosystem focused on making self-hosted **Dune: Awakening** environments easier to deploy, operate, observe, secure, automate, test, maintain, and enjoy.

The project extends beyond simply starting a game server.

Project Arrakis applies platform engineering, Site Reliability Engineering, security engineering, quality engineering, observability, automation, and operational governance practices to the complete lifecycle of a self-hosted Dune: Awakening environment.

Alongside the technical platform, Project Arrakis supports organized in-game activities designed to help players progress, build, gather resources, and participate in coordinated PvE and Deep Desert operations.

Our goal is to support both sides of operating Arrakis:

- **The infrastructure behind the server**
- **The community playing on it**

> **Deploy reliably. Observe everything. Automate carefully. Explore Arrakis together.**

---

# 🧭 Project Ecosystem

Project Arrakis is composed of complementary projects covering the full lifecycle of a self-hosted Dune: Awakening environment — from deployment and operations to observability, automation, extensibility, and infrastructure engineering.

```text
                              🏜️ PROJECT ARRAKIS
                                       │
          ┌────────────────────────────┼────────────────────────────┐
          │                            │                            │
          ▼                            ▼                            ▼
   🐳 DUNE: AWAKENING          📊 OPS OBSERVABILITY        🛡️ SENTINEL
        DOCKER                         │                            │
          │                     Prometheus / Grafana         Discord Integration
   Core Platform                Health / Readiness           Upstream Monitoring
   Server Runtime               SOC / NOC Visibility         CI Validation
   Administration               Operational Telemetry        Release Monitoring
          │                            │                     Operational Automation
          │                            │                            │
          └────────────────────────────┼────────────────────────────┘
                                       │
                         ┌─────────────┴─────────────┐
                         │                           │
                         ▼                           ▼
               📦 DOCKER ADDONS             🗺️ DEPLOYMENT
                         │                     ENGINEERING
                  Extension Model                    │
                  Addon Governance             Architecture
                  Compatibility                Infrastructure
                  Supply Chain                 Networking
                  Lifecycle                    Scaling
                                               Hardening
## 🐳 Dune: Awakening Docker

> **Core self-hosting platform and containerized server infrastructure.**

The foundation of the Project Arrakis ecosystem, providing the services and operational capabilities required to deploy and manage self-hosted Dune: Awakening environments.

**Focus:**
`Docker` · `Linux` · `Server Management` · `Networking` · `Automation`

### Core capabilities

* Containerized Dune: Awakening services
* Guided deployment
* Browser-based administration
* Service lifecycle management
* Server configuration
* Health visibility
* Readiness validation
* Backup and recovery
* Update workflows
* Player operations
* Map and instance management
* Database tooling
* Operational automation
* Scaling capabilities

➡️ **Repository:** [dune-awakening-selfhost-docker](https://github.com/yacketrj/dune-awakening-selfhost-docker)

---

## 📊 Dune: Awakening Docker Ops Observability

> **Operational visibility for Arrakis.**

Provides operational telemetry, Prometheus integration, Grafana visualization, SOC/NOC visibility, health and readiness models, resource monitoring, and reliability-focused observability.

**Focus:**
`Prometheus` · `Grafana` · `SRE` · `NOC` · `SOC` · `Telemetry`

### Operational visibility

* Service health
* Service readiness
* Runtime activity
* Resource utilization
* Environment status
* Prometheus metrics
* Grafana dashboards
* Operational telemetry
* NOC-oriented visibility
* SOC-oriented visibility
* Failure detection
* Operational diagnostics
* Capacity awareness
* Historical trend analysis

➡️ **Repository:** [dune-ops-observability-addon](https://github.com/yacketrj/dune-ops-observability-addon)

---

## 📦 Dune: Awakening Docker Addons

> **A governed extension ecosystem for the core platform.**

Provides a structured framework for discovering, validating, distributing, and managing community extensions while maintaining compatibility, lifecycle governance, and supply-chain awareness.

**Focus:**
`Extensions` · `Governance` · `Compatibility` · `Supply Chain` · `Community`

### Addon lifecycle

* Active
* Deprecated
* Unsupported
* Removed
* Blocked

### Governance goals

* Explicit addon manifests
* Defined permissions
* Versioned dependencies
* Compatibility validation
* Maintainer ownership
* Release artifacts
* Installation guidance
* Removal procedures
* Lifecycle status
* Supply-chain awareness

➡️ **Repository:** [dune-docker-addons](https://github.com/yacketrj/dune-docker-addons)

---

## 🛡️ Dune: Awakening Docker — Sentinel

> **Automation and operational intelligence for the Project Arrakis ecosystem.**

Sentinel provides Discord integration, operational notifications, upstream monitoring, CI validation, release tracking, service monitoring, synchronization safeguards, and supporting operational automation.

**Focus:**
`Discord` · `Automation` · `Monitoring` · `CI/CD` · `SRE` · `Operations`

### Sentinel capabilities

* Discord integration
* Server status visibility
* Health and readiness reporting
* Scheduled status posts
* Operational notifications
* Service monitoring
* Upstream release monitoring
* Pull-request tracking
* CI validation
* Release tracking
* Compatibility monitoring
* Failed-service detection
* Synchronization safeguards
* Operator notifications
* Controlled administrative workflows
* Permission-aware commands
* Operational auditability

---

## 🗺️ Deployment Engineering

> **Reference architectures for operating Arrakis reliably.**

Covers deployment architecture, infrastructure automation, capacity planning, network design, virtualization, host validation, scaling, security hardening, and production-readiness guidance.

**Focus:**
`Proxmox` · `Linux` · `Networking` · `Infrastructure` · `Scaling` · `Security`

### Deployment engineering topics

* Dedicated server deployment
* Virtual machine architecture
* Proxmox deployment
* CPU and memory planning
* NUMA awareness
* Storage architecture
* Network segmentation
* Firewall design
* Secure remote administration
* External service exposure
* Scaling strategies
* Failure domains
* Backup architecture
* Recovery planning
* Production hardening
* Host telemetry
* Capacity planning
* Infrastructure validation

---

# 🎮 In-Game Dune: Awakening Services

Project Arrakis also supports organized in-game services for players and communities operating within **Dune: Awakening**.

These services are intentionally separate from the software and infrastructure projects above.

The engineering ecosystem keeps Arrakis running.

The in-game services help the community thrive on it.

```text
                           🏜️ PROJECT ARRAKIS
                                    │
              ┌─────────────────────┴─────────────────────┐
              │                                           │
              ▼                                           ▼
       ⚙️ ENGINEERING                               🎮 IN-GAME SERVICES
              │                                           │
      ┌───────┼────────┐                    ┌─────────────┼─────────────┐
      │       │        │                    │             │             │
      ▼       ▼        ▼                    ▼             ▼             ▼
   Docker   Observ.  Sentinel             Base         Resource      Overmap
      │       │        │               Construction     Farming      Dungeons
      │       │        │                                                │
      └───────┼────────┘                                                ▼
              │                                              Deep Desert
              ▼                                           Testing Stations
       Deployment / Addons
```

---

## 🏗️ Base Construction

> **Construction support for functional, scalable, and organized player bases.**

Assistance with planning, gathering, and constructing Dune: Awakening bases for individual players, guilds, and communities.

### Services may include

* Base construction assistance
* Base expansion
* Resource planning
* Production-area organization
* Storage layouts
* Fabrication areas
* Refinery layouts
* Water infrastructure
* Power infrastructure
* Vehicle support areas
* Guild facilities
* Community facilities
* Functional redesigns
* Logistics-oriented layouts

**Focus:**
`Construction` · `Planning` · `Logistics` · `Infrastructure`

---

## ⛏️ Resource Farming

> **Organized gathering and logistics for the resources that keep Arrakis running.**

Coordinated farming operations for common, advanced, and high-demand materials used in construction, crafting, vehicle production, equipment progression, and community projects.

### Activities may include

* Ore and mineral gathering
* Salvage operations
* Plant and material collection
* Water acquisition
* Spice-related resource operations
* Crafting-material acquisition
* Bulk farming
* Community stockpile operations
* Construction-resource gathering
* Equipment-resource gathering
* Vehicle-resource gathering
* Logistics and transport support

**Focus:**
`Farming` · `Logistics` · `Materials` · `Community Support`

---

## 🧭 Overmap Dungeon Runs

> **Coordinated expedition support for Overmap content.**

Organized groups for completing Overmap dungeons and other expedition-oriented activities requiring coordinated travel, combat, exploration, objective completion, and extraction.

### Activities may include

* Group formation
* Expedition planning
* Combat support
* Objective completion
* Dungeon clearing
* Loot recovery
* Resource recovery
* Navigation
* Transport logistics
* Repeat farming runs
* Progression support
* New-player participation

**Focus:**
`PvE` · `Expeditions` · `Group Content` · `Progression`

---

## 🏜️ Deep Desert Testing Station Runs

> **Organized operations into Deep Desert Imperial Testing Stations.**

Coordinated Deep Desert expeditions focused on locating, clearing, looting, and extracting from Testing Stations while managing the environmental, navigation, combat, and logistical risks of the Deep Desert.

### Operations may include

* Deep Desert deployment
* Testing Station identification
* Route planning
* Group coordination
* PvE combat
* PvP-aware operations where applicable
* Station clearing
* Objective completion
* Loot recovery
* Resource extraction
* Vehicle support
* Transport coordination
* Extraction planning
* Safe-return operations

**Focus:**
`Deep Desert` · `Testing Stations` · `PvE` · `PvP Awareness` · `Expeditions` · `Loot`

---

# ⚙️ The Arrakis Stack

| Layer                       | Technology / Capability                                            |
| --------------------------- | ------------------------------------------------------------------ |
| 🏜️ **Game Infrastructure** | Dune: Awakening self-hosted services                               |
| 🐳 **Runtime**              | Docker, Docker Compose, Linux                                      |
| 🎛️ **Administration**      | Web administration, service controls, lifecycle management         |
| 🤖 **Automation**           | Sentinel, Discord, GitHub Actions, operational workflows           |
| 📊 **Metrics**              | Prometheus                                                         |
| 📈 **Visualization**        | Grafana                                                            |
| 🔔 **Operations**           | Monitoring, health, readiness, alerting, release tracking          |
| 🌐 **Networking**           | Segmentation, service exposure, firewalling, remote administration |
| 🛡️ **Security**            | Least privilege, trust boundaries, SAST, secret scanning           |
| 🔐 **DevSecOps**            | CI/CD controls, dependency review, secure delivery gates           |
| 🧪 **Quality**              | Regression, integration, compatibility and failure-path testing    |
| 📦 **Extensions**           | Governed addon ecosystem                                           |
| 🗄️ **Data**                | PostgreSQL, backup and recovery tooling                            |
| 🖥️ **Infrastructure**      | Bare metal, virtualization, Proxmox, Linux                         |
| 📚 **Governance**           | Release evidence, lifecycle controls, change management            |
| 🎮 **Community Operations** | Construction, farming, expeditions, coordinated gameplay           |

---

# 📊 Operations & Observability

Running a server is not the same as operating a service reliably.

Project Arrakis treats observability as a core platform requirement.

```text
Application / Game Services
           │
           ▼
    Health & Readiness
           │
           ▼
      Metrics Layer
           │
        Prometheus
           │
           ▼
        Grafana
           │
    ┌──────┴──────┐
    │             │
    ▼             ▼
   NOC           SOC
    │             │
    └──────┬──────┘
           │
           ▼
   Operator Awareness
```

Our observability work is intended to support:

### 🟢 Availability

* Service availability
* Process state
* Container state
* Endpoint health
* Dependency health

### 🚦 Readiness

* Application readiness
* Database availability
* Supporting-service readiness
* Dependency validation
* Startup completion

### 📈 Performance

* CPU utilization
* Memory utilization
* Disk utilization
* Network activity
* Database performance
* Service response characteristics

### 🎮 Game Operations

Where technically available and safe to expose:

* Environment activity
* Instance state
* Player-related operational signals
* Server population
* Game-service behavior
* World-service readiness

### 🛡️ Security Operations

* Authentication failures
* Permission violations
* Service anomalies
* Security-control failures
* Unexpected exposure
* Configuration drift

---

# 🛡️ Security & DevSecOps

Project Arrakis treats security as an engineering constraint rather than a final deployment step.

Our security model emphasizes:

* **Least privilege**
* **Explicit trust boundaries**
* **Secure defaults**
* **Minimal exposed attack surface**
* **Controlled administrative interfaces**
* **Secret protection**
* **Dependency awareness**
* **Supply-chain controls**
* **Auditable change**
* **Safe failure behavior**

Security controls may include:

```text
Source
  │
  ├── Secret Scanning
  ├── Static Analysis
  ├── Dependency Review
  ├── Filesystem Scanning
  │
  ▼
Build
  │
  ├── CI Validation
  ├── Artifact Validation
  ├── Security Gates
  │
  ▼
Release
  │
  ├── Controlled Publishing
  ├── Release Evidence
  ├── Version Tracking
  │
  ▼
Deployment
  │
  ├── Least Privilege
  ├── Network Controls
  ├── Runtime Validation
  │
  ▼
Operations
```

---

# 🧪 Quality Engineering

Project Arrakis applies SDET and production-quality engineering practices to infrastructure and operations.

Testing should prove more than:

> **"It worked once."**

We focus on:

* Unit testing
* Integration testing
* Regression testing
* Smoke testing
* Upgrade validation
* Installation validation
* Compatibility testing
* Failure-path testing
* Rollback testing
* Recovery testing
* Configuration validation
* CI enforcement

Special attention is given to failures capable of causing:

* Data loss
* Configuration loss
* Service outages
* Destructive synchronization
* Broken upgrades
* Operator lockout
* Unexpected privilege escalation
* Silent monitoring failures

---

# 🧭 The Arrakis Engineering Doctrine

### 🛡️ Secure by Default

Security controls should not depend entirely on operator memory or perfect configuration.

### 🔐 Least Privilege

Users, services, addons, bots, integrations, and automation should receive only the permissions required to perform their function.

### 📊 Observable Systems

If a system cannot report its own operational state, it becomes unnecessarily difficult to operate reliably.

### 🧪 Test Failure, Not Only Success

Successful workflows are only one part of system behavior. Failure paths deserve explicit validation.

### 🔁 Reproducible Operations

Deployment, validation, upgrade, recovery, and rollback should be repeatable and documented.

### 🚦 Safe Automation

Automation should eliminate repetitive work without bypassing safeguards around destructive operations.

### 📚 Documentation is Part of the Product

Implementation, architecture, operational procedures, release state, and documentation should remain aligned.

### 🔄 Design for Recovery

Failures will occur. Recovery should be considered during architecture and implementation rather than after an incident.

### 👁️ Make State Visible

Operators should be able to distinguish:

```text
RUNNING ≠ HEALTHY ≠ READY ≠ FUNCTIONAL
```

A running process does not necessarily mean a working service.

---

# 🚦 Project Lifecycle

Project Arrakis projects may use the following lifecycle indicators:

| Status              | Meaning                                               |
| ------------------- | ----------------------------------------------------- |
| 🟢 **Active**       | Actively developed and supported                      |
| 🟡 **Development**  | Under active development; interfaces may change       |
| 🔵 **Experimental** | Research or proof-of-concept work                     |
| 🟠 **Maintenance**  | Stable with limited active feature development        |
| ⚪ **Planned**       | Accepted direction but implementation has not started |
| 🔴 **Deprecated**   | Scheduled for retirement or replacement               |
| ⚫ **Archived**      | No longer actively maintained                         |

---

# 🔄 Development Philosophy

Project Arrakis favors incremental, reviewable engineering changes over uncontrolled feature expansion.

A typical change should progress through:

```text
        Requirement
             │
             ▼
        Architecture
             │
             ▼
      Threat / Risk Review
             │
             ▼
       Implementation
             │
             ▼
          Testing
             │
             ▼
       CI Validation
             │
             ▼
     Security Validation
             │
             ▼
       Documentation
             │
             ▼
          Release
             │
             ▼
       Observation
             │
             ▼
         Feedback
```

Where appropriate, changes should include:

* Defined requirements
* Acceptance criteria
* Architecture implications
* Security implications
* Tests
* Documentation
* Rollback considerations
* Operational evidence

---

# 🌐 Infrastructure Philosophy

Project Arrakis does not assume every operator has the same environment.

The ecosystem is intended to support deployment patterns ranging from:

```text
Single Host
    │
    ▼
Docker Environment
```

through:

```text
Dedicated Server
      │
      ▼
Hypervisor / Proxmox
      │
      ├── Management VM
      ├── Game Services
      ├── Monitoring
      └── Supporting Infrastructure
```

and toward more advanced environments involving:

```text
Multiple Hosts
     │
     ├── Segmented Networks
     ├── Centralized Monitoring
     ├── External Access Controls
     ├── Backup Infrastructure
     └── Operational Automation
```

Reference architectures should prioritize:

* Reliability
* Maintainability
* Security
* Recoverability
* Clear failure domains
* Reasonable operational complexity

---

# 📦 Addon Philosophy

Extensions should expand the platform without turning the core environment into an uncontrolled dependency graph.

Project Arrakis therefore favors:

* Explicit addon manifests
* Versioned dependencies
* Defined permissions
* Lifecycle status
* Review expectations
* Release artifacts
* Compatibility validation
* Clear ownership
* Removal procedures

An addon should be able to answer:

```text
What does it do?
What does it access?
What permissions does it require?
What version does it support?
Who maintains it?
How is it installed?
How is it removed?
What happens if it fails?
```

---

# 🤝 Contributing

Contributions, testing, documentation improvements, bug reports, security findings, architectural discussion, operational feedback, and community participation are welcome.

For project-specific engineering work, use the **Issues** or **Discussions** area of the appropriate repository.

When opening an issue, useful information may include:

* Project version
* Deployment environment
* Operating system
* Docker version
* Relevant configuration
* Expected behavior
* Actual behavior
* Logs
* Reproduction steps
* Recent changes

Please remove passwords, API keys, tokens, personally identifiable information, and other secrets before publishing logs or configuration.

---

# 🐛 Bug Reports

A useful bug report should make the failure reproducible.

Where possible, include:

```text
Environment:
Version:
Installation method:
Configuration:
Expected result:
Actual result:
Steps to reproduce:
Relevant logs:
Recent changes:
```

Screenshots and diagnostic output may also be useful when they do not expose sensitive information.

---

# 💡 Feature Requests

Feature proposals are most useful when they describe the operational problem rather than only the desired implementation.

Consider including:

* What problem are you trying to solve?
* Who experiences the problem?
* How is it handled today?
* What limitations exist?
* What would success look like?
* Does the change introduce new permissions?
* Does it affect compatibility?
* Does it introduce operational risk?

---

# 🔐 Security

Please avoid publishing exploitable security vulnerabilities in public issue threads before maintainers have an opportunity to review them.

Security-related changes should consider:

* Authentication
* Authorization
* Secrets
* Network exposure
* Privilege boundaries
* Input validation
* Data integrity
* Supply-chain dependencies
* Logging
* Failure behavior

Where supported by the relevant repository, use its documented private vulnerability-reporting mechanism.

---

# 🗺️ Current Engineering Focus

Current areas of interest across the Project Arrakis ecosystem include:

* 🐳 Dune: Awakening containerized infrastructure
* 🎛️ Server administration and lifecycle management
* 📊 Prometheus metrics
* 📈 Grafana dashboards
* 🚦 Health and readiness modeling
* 🔔 Operational alerting
* 🖥️ Host and VM telemetry
* 🌐 Network architecture
* 🛡️ Security hardening
* 🔐 Least-privilege integrations
* 🤖 Sentinel automation
* 💬 Discord operations
* ⚙️ CI/CD automation
* 🧪 Regression and compatibility testing
* 📦 Addon governance
* 🔄 Upstream release monitoring
* 💾 Backup and recovery
* 📚 Technical and operator documentation
* 🏗️ Reference deployment architectures
* 📋 Auditable release and security evidence

---

# 🎮 Current Community Focus

Project Arrakis community operations currently focus on:

* 🏗️ Base construction and expansion
* ⛏️ Resource farming
* 📦 Community material stockpiles
* 🧭 Overmap dungeon runs
* 🏜️ Deep Desert expeditions
* 🏭 Imperial Testing Station runs
* 🚙 Transport and logistics
* 🤝 Player progression support
* 🎯 Coordinated PvE activities
* ⚔️ PvP-aware Deep Desert operations

---

# 🏜️ Why Project Arrakis?

Self-hosted game infrastructure often begins with a simple objective:

> **Get the server running.**

Production engineering asks a much larger set of questions:

```text
How do we know it is healthy?

How do we know it is ready?

What happens when something fails?

How do we detect degradation?

How do we update safely?

How do we recover?

How do we observe the environment?

How do we prevent destructive automation?

How do we manage extensions?

How do we know a security control still works?

How do we prove a release was actually validated?
```

A community adds another set:

```text
How do we help new players progress?

How do we organize large projects?

How do we coordinate resource gathering?

How do we prepare for difficult expeditions?

How do we help players experience end-game content?

How do we turn a server into a community?
```

**Project Arrakis exists to work on both.**

---

<div align="center">

# 🏜️ Project Arrakis

### Build · Operate · Observe · Secure · Test · Explore

**Dune: Awakening Self-Hosting Engineering & Community Operations**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-Project%20Arrakis-181717?style=for-the-badge&logo=github)](https://github.com/Project-Arrakis)
[![Discussions](https://img.shields.io/badge/Community-Discussions-6E5494?style=for-the-badge&logo=github)](https://github.com/Project-Arrakis)

</div>

---

## ⚠️ Disclaimer

Project Arrakis is an independent, community-developed open-source engineering and gaming project.

It is **not affiliated with, endorsed by, sponsored by, or associated with Funcom, Legendary Entertainment, the Herbert Estate, or the owners of the Dune intellectual property**.

**Dune**, **Dune: Awakening**, and related names, trademarks, characters, imagery, and intellectual property belong to their respective owners.

Project Arrakis provides community-developed infrastructure, tooling, automation, observability, operational resources, and community gameplay services intended for use with legally obtained software and supported self-hosting functionality.
