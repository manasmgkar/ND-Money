# 💸 ND Money (Neurodivergent Money)

**A visual, AI-powered financial assistant designed specifically for visual thinkers and users with dyscalculia.**

ND Money bridges the gap between physical cash and mental math. By combining Google's Gemini API for complex reasoning with on-device computer vision, the app provides a stress-free environment for handling bills, checking change, and deciding how to pay—all without requiring the user to process abstract numbers.
---

## The reddit post that inspired this app

<img width="1347" height="678" alt="dycalculia reddit" src="https://github.com/user-attachments/assets/53969861-c32b-471c-bc0b-9c737010e6f2" />


## 🧠 Design Philosophy: The Visual Thinking Advantage

Traditional finance apps are built on **abstract symbols** (numbers). For neurodivergent minds—particularly those with dyslexia or dyscalculia—processing symbols and numbers can be mentally exhausting.

Change and physical monetry transactions and change calculation can be difficult. 

However, many dyslexic individuals are **highly proficient visual thinkers**. Their memory and processing is anchored in imagery, color, and pattern recognition rather than rote arithmetic. ND Money was designed to leverage these strengths.

### 1. Visual Anchors Over Digits
*   **The Insight:** A user might struggle to distinguish "1000" from "10000" at a glance, but they instantly recognize visual landmarks.
*   **The Solution:** We display currency as **high-fidelity images**, not just numbers.
    *   *Example:* Instead of forcing a user to read "¥10,000", the app shows the note featuring **The Great Wave off Kanagawa**. The user recognizes the "Wave," not the zero count.
    *   *Implementation:* The app includes a dedicated asset library for notes and coins (USD, JPY, EUR, etc.) to trigger this visual memory match.
 
<p align="center">
  <img src="https://github.com/user-attachments/assets/6b87731a-2d07-4993-927f-f581d1cb1a76" width="22%" alt="Home Screen">
  <img src="https://github.com/user-attachments/assets/59cab3df-470b-4583-8a3e-650f9d02cd6e" width="22%" alt="Visual Scanner">
  <img src="https://github.com/user-attachments/assets/28bd81d2-9ed8-482f-ae5b-931d9c14d7f6" width="22%" alt="Visual Result">
  <img src="https://github.com/user-attachments/assets/58244224-b11a-44db-912f-f61ba01fd49b" width="22%" alt="Payment Advice">
  <img src="https://github.com/user-attachments/assets/0ace5c1b-5330-4e3c-8dad-5695e1aa9aed" width="22%" alt="Payment Advice"> 
</p>



### 2. Color Association & Recognition
*   **The Insight:** Dyslexic users often rely on color coding to categorize information quickly without reading.
*   **The Solution:**
    *   **Currency Tinting:** The UI mimics the real-world color palette of the currency (e.g., Beige/Green for USD, Purple/Brown for large JPY notes) to reduce cognitive load.
    *   **Action Coding:** We utilize distinct semantic colors for instructions:
        *   <span style="color:#059669">**Green (Keep)**</span>: Money you hold.
        *   <span style="color:#dc2626">**Red (Return)**</span>: Excess change to give back.
        *   <span style="color:#0d9488">**Teal (Total)**</span>: The calculated sum.

### 3. Cognitive Offloading via Linear Flows
*   **The Problem:** Working memory is often a bottleneck. Holding a number in your head while counting change leads to anxiety.
*   **The Solution:** The app breaks complex transactions into isolated, linear steps (Step 1: Scan Bill -> Step 2: Scan Cash). The interface acts as an external working memory, ensuring the user never has to "hold" a number in their head.

---

## ✨ Key Features

### 📸 1. Verify Bill & Change (Full Auto)
The complete loop. The user takes a photo of the bill, a photo of the cash they handed over, and a photo of the change they received. The AI calculates the math and verifies if the change is correct using computer vision to count the coins and notes.

### 🧮 2. Check My Change (Visual Picker)
A hybrid flow where the user inputs what they paid using **Visual Money Cards** (tapping an image of a $20 bill rather than typing "20") and scans the change received. The app visually highlights exactly which notes are missing or extra.

### 🤝 3. Payment Assistant
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
*   **On-Device AI:** TensorFlow Lite / MediaPipe (`@mediapipe/tasks-vision`)
*   **Deployment:** Capacitor (Android/iOS wrapper), PWA

---

## 🤖 Special Acknowledgements

**Offline Detection Architecture**

This project utilizes custom-trained TensorFlow Lite models for on-device currency detection. We would like to give a special mention to **Microsoft's `bank_note_net` repository**.

We adapted concepts from their research, specifically fusing their **encoder-decoder model architecture**, to create our lightweight mobile models. Their work on robust currency embeddings was instrumental in enabling our offline functionality.

---

## 🚀 Getting Started

### Prerequisites
*   Node.js (v18+)
*   A Google Gemini API Key

### Installation

1.  **Clone the repo**
    ```bash
    git clone https://github.com/yourusername/nd-money.git
    cd nd-money
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Set up Environment Variables**
    Create a `.env` file in the root:
    ```env
    VITE_API_KEY=your_gemini_api_key_here
    ```

4.  **Run Development Server**
    ```bash
    npm run dev
    ```

### Building for Mobile (Capacitor)

1.  **Build the React App**
    ```bash
    npm run build
    ```

2.  **Sync with Android/iOS**
    ```bash
    npx cap sync
    npx cap open android
    ```

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🚀 Coming to the Google PLay store for Android Phones Soon


## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
