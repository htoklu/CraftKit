# CraftKit

&gt; AI-powered vehicle inspection in a single portable EXE. No setup, no cloud, no dependencies.

CraftKit is a standalone desktop application that automates vehicle check-in and check-out for rental companies, parking facilities, and fleet operators. It runs entirely offline from one executable — no server installation, no database configuration, no internet required.

## What It Does

- **License Plate Recognition** — Captures and reads plates from camera or image files using OCR with confidence scoring.
- **AI Damage Detection** — Identifies scratches, dents, cracks, and broken lights on vehicle photos using computer vision.
- **Before / After Comparison** — Compares check-in and check-out images side-by-side, flags new damage, and assigns severity scores.
- **Auto-Generated Reports** — Exports timestamped PDF inspection reports with annotated photos for insurance and customer records.

## Under the Hood

- **Regex Engine** — Custom pattern matching for plate format validation, report ID parsing, and structured data extraction across different regions.
- **Color Space Converters** — Dynamic RGB ↔ HSV ↔ LAB transformations for accurate damage detection under varying lighting conditions (daylight, garage, night flash).
- **Base64 Pipeline** — Embedded image encoding for zero-dependency report generation; photos are processed, annotated, and embedded directly into portable PDFs without external asset folders.
- **Single-Binary Architecture** — The entire stack (YOLO inference, OCR engine, PDF renderer, SQLite database) is compiled into one self-contained EXE using PyInstaller. No Python runtime, no DLL hell.

## How It Works

1. **Launch** — Double-click `CraftKit.exe`. It creates a local workspace automatically.
2. **Inspect** — Snap or upload photos. AI processes them instantly on your machine.
3. **Compare** — Select before/after pairs. Damage is highlighted and scored locally.
4. **Export** — Generate a signed PDF report with embedded base64 images and regex-structured metadata.

## System Requirements

- Windows 10/11 (64-bit)
- 4 GB RAM
- Webcam or smartphone for photo capture

No installation. No accounts. No cloud.

---

**Download the latest release → Run CraftKit.exe → Start inspecting.**

https://github.com/htoklu/CraftKit/releases/tag/v1.0
