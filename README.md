# GuardianRoute – Smart Emergency Pathfinding Tool

**GuardianRoute** is a smart emergency pathfinding system built with Java, leveraging the **A\*** algorithm and **Region Adjacency Graphs (RAG)** for real-time safe route detection on floor plans. Designed to help during emergencies (fire, gas leaks, building collapses), it intelligently classifies zones and calculates optimal escape paths.

---

## Problem & Solution

### The Problem
- 80% of evacuation delays are due to poor route choices (NFPA data).
- Static maps don’t account for dynamic hazards (fire, gas leaks, blocked paths).

### ✅ Our Solution
- **GuardianRoute** classifies zones on a floor plan as: Walkable, Danger, Wall, and Exit.
- Uses the **A\*** algorithm to calculate the **safest route** in real-time, avoiding danger zones.

---

## 🛠️ Features

- ✅ **Smart Image Zone Detection** using color proximity.
- 🧠 **A\*** Pathfinding with real-time cost-based decisions.
- 🖼️ **Graph Construction** from images using RAG to reduce computation.
- ⚡ Processes 1000×1000 px images in under 2 seconds.
- 🎯 Animated route traversal with smooth visual indicators.
- 🖱️ Interactive GUI for selecting start and end points.

---

## 📷 Zone Classification

| Zone Type  | RGB Value        | Cost | Description                   |
|------------|------------------|------|-------------------------------|
| **Exit**   | (14, 111, 34)    | 0    | Goal destination              |
| **Walkable**| Custom (non-danger/wall) | 1 | Standard movement             |
| **Danger** | (243, 25, 41)    | 100  | Avoid unless trapped          |
| **Wall**   | Any other/obstacle color | ∞ | Impassable                    |

> Color proximity detection is used to classify each zone based on RGB distance.

---

## 🖥️ GUI Features

- 📌 Start & End pins with labels
- 🎞️ Path animation (Pink dot follows computed path)
- 🟢 Zone highlighting (Green for exits, Pink for dangers)
- 🚨 Real-time warning system

---

## 📂 How It Works

1. Upload a floor plan image (JPEG, PNG, or blueprint)
2. Select a start and end location
3. GuardianRoute detects zones automatically
4. The A\* algorithm finds the safest route
5. The path is animated in the GUI

---

## 🚀 Getting Started

### ✅ Requirements

- **Java 21+**
- **JavaFX 21 SDK**

---

### 🧰 Step-by-Step Installation

#### 1. **Install Java 21+**

Download and install JDK 21 from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html) or [Adoptium](https://adoptium.net/en-GB/temurin/releases/?version=21).

#### 2. **Install JavaFX 21**

Download JavaFX SDK 21 from the official [Gluon website](https://gluonhq.com/products/javafx/).

Extract it to a known location on your system (e.g., `C:\javafx-sdk-21`).

#### 3. **Clone the Repository**

```bash
git clone https://github.com/yourusername/GuardianRoute.git
cd GuardianRoute
