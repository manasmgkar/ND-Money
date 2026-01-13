# ND-Money
A android App that helps Dyslexic/Dyscalculic users in handling change and eases counting difficulties.

# 💸 ND Money (Neurodivergent Money)

**A visual, AI-powered financial assistant designed specifically for users with dyscalculia and neurodivergence.**

ND Money bridges the gap between physical cash and mental math. By combining Google's Gemini API for complex reasoning with on-device computer vision, the app provides a stress-free environment for handling bills, checking change, and deciding how to pay—all without requiring the user to do mental arithmetic.

---

## 🧠 Product Design & Accessibility Philosophy

The core design philosophy behind ND Money is **"Cognitive Offloading."** For users with dyscalculia, processing abstract numerical symbols ($15.75) and performing mental subtraction creates high cognitive load and anxiety.

We designed every interaction to shift that load from the user's brain to the interface:

### 1. Visual Over Abstract
*   **The Problem:** Abstract numbers are difficult to visualize and manipulate for dyscalculic users.
*   **The Solution:** We effectively removed the need to type numbers. The app features a **"Visual Money Picker"**. Instead of typing "20", the user taps an image of a 20-dollar bill. Results are shown not just as a number, but as a breakdown of physical notes and coins to give back or receive.

### 2. Linear, Step-by-Step Flows
*   **The Problem:** Multi-step arithmetic (Bill - Paid = Change) requires holding working memory, which is often a struggle.
*   **The Solution:** The app breaks complex transactions into isolated, linear steps (Step 1: Scan Bill -> Step 2: Scan Cash). The interface never asks the user to do two things at once.

### 3. Multi-Sensory Feedback
*   **The Problem:** Relying solely on visual confirmation can lead to errors if numbers are misread.
*   **The Solution:**
    *   **Text-to-Speech (TTS):** Every action and result is read aloud automatically using natural language processing.
    *   **Haptic & Visual Cues:** We use distinct color coding (Teal for "Give", Red for "Stop/Return", Green for "Keep") and clear iconography (Checkmarks vs. X's) to convey meaning without reading.

### 4. Dyslexia-Friendly UI
*   **Typography:** The app integrates the **OpenDyslexic** font family to improve readability.
*   **Contrast:** High-contrast modes and large touch targets reduce motor strain and visual noise.

---

## ✨ Key Features

### 📸 1. Verify Bill & Change (Full Auto)
The complete loop. The user takes a photo of the bill, a photo of the cash they handed over, and a photo of the change they received. The AI calculates the math and verifies if the change is correct using computer vision.

### 🧮 2. Check My Change
A hybrid flow where the user inputs what they paid (using voice or visual buttons) and scans the change received. The app visually highlights if money is missing or if too much was given back.

### 🤝 3. Payment Assistant (Reasoning Engine)
A user scans the contents of their wallet. The AI analyzes the available denominations and suggests the **optimal combination** of notes to pay a specific bill, prioritizing exact change to reduce social anxiety at the register.

### 🏪 4. Merchant Mode (Give Change)
Designed for neurodivergent employees. It calculates the change due and displays a **visual map** of exactly which notes and coins to pick from the register to hand to the customer.

### 🗣️ Voice-First Input
Integrated speech-to-text allows users to simply say "Twenty-five dollars" rather than struggling with a number pad.

### 📡 Hybrid AI Engine
*   **Online:** Uses **Google Gemini 1.5 Flash** for high-level reasoning, complex scene analysis, and payment advice.
*   **Offline:** Uses on-device **TensorFlow Lite** models for detecting and counting currency when internet connectivity is poor.

---

## 🛠️ Tech Stack

*   **Frontend:** React, TypeScript, Vite
*   **Styling:** Tailwind CSS
*   **Cloud AI:** Google Gemini API (`@google/genai`)
*   **On-Device AI:** Custom Trained Small Classifiers that run on TensorFlow Lite / MediaPipe (`@mediapipe/tasks-vision`)
*   **Deployment:** Capacitor (Android/iOS wrapper), PWA

---

## 🤖 Special Mention: Offline Detection

A special acknowledgement to **Microsoft's `bank_note_net` repository**. 

We utilized their research on currency detection to inform our offline capabilities. Specifically, we fused concepts from their **encoder-decoder model architecture** to train our own lightweight, mobile-optimized models. This allows ND Money to perform accurate bounding-box detection and denomination classification directly on the device, ensuring accessibility even in low-connectivity environments.

---

## 🚀 Coming to the Google PLay store for Android Phones Soon


## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
