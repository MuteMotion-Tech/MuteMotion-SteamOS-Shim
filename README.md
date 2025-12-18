# MuteMotion-SteamOS-Shim

Official integration layer and validation prototype for the **MuteMotion Project**. This module serves as the primary technical deliverable for academic auditing and performance verification on the Valve Steam Deck environment.

## System Overview
The Shim operates as a platform-specific "Body," responsible for hardware-level communication and real-time visual injection. It bridges high-frequency sensor data with the external **MuteMotion Core Engine**.

### Technical Implementation
* **Hardware Interface:** Low-level sensor acquisition via `libinput` and `evdev`.
* **Graphics Pipeline:** Low-latency overlay rendering targeting the `Gamescope` micro-compositor via `Vulkan`.
* **Service Architecture:** Persistent background execution managed via `systemd` user services.
* **Data Persistence:** Relational configuration management using `SQLite` in WAL mode for concurrent access.

## Academic Validation
This specific repository and its associated documentation were developed as a technical proof-of-concept for the **Universidade Lusófona**.

* **Lead Implementation:** Adriano N. (a22307762@alunos.ulht.pt)
* **Institutional Supervision:** Prof. José Braga de Vasconcelos

## Architectural Constraints
To fulfill portability requirements (NFR-6.4), the system utilizes a strictly decoupled architecture. The implementation provided in this repository handles only the platform-specific integration.

* **Shim Implementation:** Open-source module for system integration and validation.
* **Core Logic:** External dependency providing proprietary inertial transformation algorithms.

## Licensing
* **SteamOS Shim:** Released under the MIT License for community and academic audit.
* **MuteMotion Core Engine:** Proprietary technology and **Prior Art** research. All algorithmic rights are reserved by [MuteMotion Tech](https://mutemotion-tech.n0t.space/).

## Contact
For technical inquiries regarding the integration layer or licensing of the underlying research initiative:

* **Technical / Licensing (Astro):** astro@n0t.space
* **General / Partnerships:** adriano@n0t.space

---
© 2024-2025 MuteMotion Tech. All rights reserved.
