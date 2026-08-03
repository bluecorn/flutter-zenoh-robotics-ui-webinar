# Building a UI for Robotics Using Flutter and Zenoh

Slides for the **EF IoT Webinar** — June 17, 2026 — by **Hugo Alberto Garcia, Bluecorn**.

📄 **[flutter-zenoh-robotics-ui.pdf](flutter-zenoh-robotics-ui.pdf)** — the compiled deck.

## What it's about

Zenoh lets an app interact with a robot — through ROS — as a **peer**, eliminating the
broker/gateway and the client/server tier every other approach forces between the app and the
robot. The server keeps its place (cloud data-mining, management, aggregation) — it just isn't
the *only* door; a UI on the same fabric has real merits. Demonstrated on a real PincherX-100
arm over Zenoh; the same pattern extends to IoT and embedded.

## The code

The talk is backed by three open-source repositories:

| Repo | What it is |
|------|------------|
| [zenoh_dart](https://github.com/bluecorn/zenoh_dart) | [`package:zenoh_dart`](https://pub.dev/packages/zenoh_dart) — the pure-Dart Zenoh binding (over `dart:ffi`, wrapping `zenoh-c`) |
| [flutter_zenoh_gateway](https://github.com/bluecorn/flutter_zenoh_gateway) | App 1 — the gateway-path operator app (the live demo) |
| [flutter_zenoh_direct](https://github.com/bluecorn/flutter_zenoh_direct) | App 2 — the gateway-less direct spike ("We Went Further") |

## Building the slides

The deck is **XeLaTeX** + a small Beamer theme (`theme/`) using a Material-3 palette,
Roboto, and IBM Plex Mono.

**Prerequisites**

- A TeX distribution with XeLaTeX and `latexmk` (e.g. TeX Live)
- Fonts installed system-wide: **Roboto** and **IBM Plex Mono**

**Compile**

```bash
latexmk -xelatex flutter-zenoh-robotics-ui.tex
```

## License

[Apache-2.0](LICENSE) — consistent with the code repositories above.
