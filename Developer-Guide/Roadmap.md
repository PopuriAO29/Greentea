## Roadmap and goals

The main idea of the project is to quickly and efficiently create a compatible environment for the existing software and provide the best user experience of a personal computer.

### Planned features and improvements

* CPU
 * [x] UEFI boot
 * [x] [x86-64-only mode (**dropping x86-32**)](x64.md)
 * [ ] Multi-core CPUs and scheduler
* GPU
 * [ ] [Software Vulkan](../User-Guide/Vulkan.md)
 * [ ] Hardware Vulkan
 * [ ] OpenGL
 * [ ] D3D
* Engine
 * [x] [New one in Hexa](../User-Guide/Hexa.md)
 * [x] Stable memory manager
 * [x] Initial .exe support
 * [x] GUI-capable .exe support
 * [ ] Browsers
 * [ ] Wi-Fi & Bluetooth
 * [ ] Networking protocols
 * [ ] Third-party drivers support
 * [ ] [Moving to a modern filesystem](../User-Guide/Greentea-FS.md)
 * [ ] Unix subsystem (only software)
 * [ ] Android subsystem
 * [x] LiveCD/USB
 * [ ] GUI for OS installer
 * [ ] [Easy system updates](../User-Guide/Rolling.md)
* Visuals
 * [x] New default theming and visuals
 * [ ] HiDPI
 * [ ] Theming engine
 * [ ] [New flexible theming engine and toolkit](../User-Guide/Web.md)
 * [ ] Overhaul of theming engine (GPU-accelerated, shadows, blurs, effects)
* Shell and UI
 * [x] Initial implementations of shell, tray, explorer, start button and others
 * [x] Greentea widgets and GUI elements
 * [ ] Stabilization of shell, tray, explorer, start button and others
 * [ ] [Shell overhaul to add modern features and look](../User-Guide/Control-Panel.md)
 * [ ] Customizable themes and widgets with external theme-packs
 * [ ] Stable and finished user space software

---

### Not planned features

This project started as a controversy to undefined future (and past) of existing operating systems.
Our team decided to define precise list of *the most useful* features to the wide audiences.
Some features aren't really useful in any real manner *right now*, and their priority may be lowered.

**Update from 2023:** seems like M1 CPUs finally make ARM support valuable?
**Update from 2025:** M2+ CPUs seems like nearly impossible to fully support due to hardware changes

Features, like LPT printing, has so small applicability (LPT ports in 2025+ anyone?),
so can't be considered in any manner real target for Greentea OS team and use case for our users.
Also, multiply that by a *enormous* number of bugs, hacks and workarounds, which we should fix now,
to at least make non-academic project! And then improve implementations, **the real things**.
Otherwise it is a waste of time.

---

### Feature timings

Features are highly dependent of the API version.
Also, the ecosystem defines it's own distribution rules.
For example: while it *is* possible to run Vulkan API over virtually any (even 20 years old) operating system,
no hardware or middleware (LunarG) distributors actually did it.
Some features also, like native Wi-Fi or BLE support, were non-existent on old versions.
So we need to declare timings and dependencies per feature.
