# ⚡️ Supabase Region Ping

A high-performance, browser-based utility to measure network latency between your location and Supabase's global regions.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Supabase](https://img.shields.io/badge/Supabase-Database-3ecf8e?logo=supabase)](https://supabase.com)

## 🚀 Overview

When setting up a Supabase project, choosing the right region is critical for application performance. This tool pings the underlying AWS regional endpoints (where Supabase infrastructure resides) to give you an accurate estimation of the Round Trip Time (RTT).

### Key Features
* **Real-time Benchmarking:** Measures latency using the browser's `fetch` API.
* **Automatic Sorting:** Ranks regions from fastest to slowest automatically.
* **Visual Grading:** Color-coded bars (Green < 100ms, Yellow < 200ms, Red > 200ms).
* **Privacy-Centric:** No tracking, no backend, and no data collection. Everything happens in your browser.

## 🛠 Installation & Usage

### Option 1: GitHub Pages (Recommended)
1. Push this code to a GitHub repository.
2. Go to **Settings > Pages**.
3. Set the source to the `main` branch and root `/`.
4. Your tool will be live at `https://<your-username>.github.io/<repo-name>/`.

### Option 2: Local Run
1. Clone the repository.
2. Open `index.html` in any modern web browser.

## 🧪 How it Works

The tool uses a `fetch` request with the `no-cors` mode to bypass Cross-Origin Resource Sharing restrictions while still capturing the timing of the request.

1.  **Warm-up:** Performs an initial ping to establish a TCP connection.
2.  **Sampling:** Executes 3 consecutive pings per region.
3.  **Averaging:** Calculates the mean latency to provide a stable result.

## 📋 Supported Regions

All standard Supabase/AWS regions are included, such as:
* 🇺🇸 US East (N. Virginia & Ohio)
* 🇺🇸 US West (N. California & Oregon)
* 🇪🇺 EU (Ireland, London, Frankfurt, Paris, Stockholm)
* 🌏 Asia Pacific (Tokyo, Seoul, Singapore, Mumbai, Sydney)
* 🇧🇷 South America (São Paulo)
* 🇨🇦 Canada (Central)

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---
*Disclaimer: This tool is not an official Supabase product. It measures latency to the AWS regions where Supabase services are hosted.*
