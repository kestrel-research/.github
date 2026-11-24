Kestrel Research

Open-source Python libraries for drone autonomy, from the Raspberry Pi up to research.

Kestrel Research is an independent, community-driven open-source project. We build simple, well-tested Python tools for people who build and program drones: hobbyists, students, educators and researchers.

Like the kestrel, a bird known for hovering steadily in place, our aim is control that is precise, stable and easy to rely on.

🎉 flypi v0.1.0 is out! Our first library is now on PyPI: pip install flypi. Read the release notes →

🛩️ Projects
Project	What it is	Status
flypi	Core library for Raspberry Pi and companion-computer builders. A modern, high-level Python API for flying ArduPilot drones over MAVLink: connect, arm, take off, land and read live telemetry. pymavlink is its only dependency, and every command is confirmed.	✅ v0.1.0 released (alpha)
Research library (name coming soon)	Simulation environments, reinforcement learning tools, geospatial navigation and vision modules for drone research and education. Built on top of flypi.	🧪 Planned
🚀 Getting started
bash
pip install flypi
python
import flypi

with flypi.connect("udp:127.0.0.1:14550") as drone:
    drone.wait_ready()
    drone.arm()
    drone.takeoff(5)   # metres above home
    drone.land()

Python 3.10+ on Raspberry Pi OS, Linux, macOS or Windows. ArduPilot Copter is the main target, and PX4 support is experimental. Try it in ArduPilot SITL before you fly real hardware. See the flypi README for connection setups and the full API.

Coming next in flypi: guided waypoints (goto), velocity control, missions, parameter read/write, and camera helpers for the Pi.

🎯 What we care about
Simple first. Fly a drone in a few lines of Python, then go deeper when you need to.
Sim before sky. Every example runs in software-in-the-loop (SITL) simulation before it touches real hardware.
Light on the Pi. The core library keeps its dependencies small so it installs cleanly on Raspberry Pi boards.
Research that flies. Ideas built in the research library deploy to real drones through the same flypi API.
Open by default. Everything is released under the Apache-2.0 licence.
🤝 Contributing

Contributions are welcome: code, examples, docs, bug reports and build guides for your own Pi drones. Tried flypi v0.1.0? Open an issue to tell us what worked, what broke and what you need next.

⚠️ Safety

Drones can cause serious injury and damage. Always test in simulation first, fly in a safe and legal area, follow your local aviation regulations, and keep a manual override ready.

<sub>Kestrel Research · Open-source drone autonomy · Apache-2.0</sub>
