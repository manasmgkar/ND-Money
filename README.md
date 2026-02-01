# 💸 ND Money (Neurodivergent Money)

**A visual, AI-powered financial assistant designed specifically for Neurodivergent visual thinkers and users with dyscalculia.**

ND Money bridges the gap between physical cash and mental math. By combining Google's Gemini API for complex reasoning with on-device computer vision, the app provides a stress-free environment for handling bills, checking change, and deciding how to pay—all without requiring the user to process abstract numbers.
---

## The reddit post that inspired this app

<img width="1347" height="678" alt="dycalculia reddit" src="https://github.com/user-attachments/assets/53969861-c32b-471c-bc0b-9c737010e6f2" />


## 🧠 Design Philosophy: The Visual Thinking Advantage

Traditional finance apps are built on **abstract symbols** (numbers). For neurodivergent minds—particularly those with dyslexia or dyscalculia—processing symbols and numbers can be mentally exhausting.

Change and physical monetry transactions and change calculation can be difficult. 

However, many dyslexic individuals are **highly proficient visual thinkers**. Their memory and processing is anchored in imagery, color, and pattern recognition rather than rote arithmetic. ND Money was designed to leverage these strengths.

### 1. Visual Anchors Over Digits
*   **The Insight:** A lot of currencies have the same basic color for every denomination,Japanese yen being one example. A user might struggle to distinguish "1000" from "10000" at a glance, but they instantly recognize visual landmarks. 
*   **The Solution:** We display currency as **high-fidelity images**, not just numbers.
    *   *Example:* Instead of forcing a user to read "¥10,000", the app shows the cropped photo of the note featuring **The Tokyo station**. The user recognizes the "Tokyo Station," not the zero count. **or Lincoln on the 5$ note.**
    *   *Implementation:* The app includes a dedicated asset library for notes and coins (USD, JPY, EUR, etc.) to trigger this visual memory match.
 
<p align="center">
  <img src="https://github.com/user-attachments/assets/6b87731a-2d07-4993-927f-f581d1cb1a76" width="22%" alt="Home Screen">
  <img src="https://github.com/user-attachments/assets/59cab3df-470b-4583-8a3e-650f9d02cd6e" width="22%" alt="Visual Scanner">
  <img src="https://github.com/user-attachments/assets/58244224-b11a-44db-912f-f61ba01fd49b" width="22%" alt="Payment Advice">
  
</p>



### 2. Color Association & Recognition
*   **The Insight:** Dyslexic users often rely on color coding to categorize information quickly without reading.For currencies that have unique colors for each denomination we have a differetn visual solution. 
*   **The Solution:**
    *   **Currency Tinting:** The UI mimics the real-world color palette of the currency to reduce cognitive load. Example : The Indian 100 rupee note is purple, INR 20 Note is Green. The 100 GBP note has a Different Color than the 20 GBP note.
    *   **Action Coding:** We utilize distinct semantic colors for instructions:
        *   <span style="color:#059669">**Green (Keep)**</span>: Money you hold.
        *   <span style="color:#dc2626">**Red (Return)**</span>: Excess change to give back.
        *   <span style="color:#0d9488">**Teal (Total)**</span>: The calculated sum.
          
<p align="center">
     <img src="https://github.com/user-attachments/assets/28bd81d2-9ed8-482f-ae5b-931d9c14d7f6" width="22%" alt="Visual Result">
     <img src="https://github.com/user-attachments/assets/0ace5c1b-5330-4e3c-8dad-5695e1aa9aed" width="22%" alt="Payment Advice">
     <img src="https://github.com/user-attachments/assets/1791a711-af97-4071-8ed4-1c2b44c3c9e2" width="22%" alt="Correct Change">
</p>

### 3. Cognitive Offloading via Linear Flows
*   **The Problem:** Working memory is often a bottleneck. Holding a number in your head while counting change leads to anxiety.
*   **The Solution:** The app breaks complex transactions into isolated, linear steps (Step 1: Scan Bill -> Step 2: Scan Cash). The interface acts as an external working memory, ensuring the user never has to "hold" a number in their head.

<h3>📱 Step-by-Step Flow</h3>

<p>
  <img
    src="https://github.com/user-attachments/assets/ab509322-dd81-4d95-80b5-030c319c940f"
    width="220"
    alt="Step 1"
  />
  <img
    src="https://github.com/user-attachments/assets/4431815f-db98-4b83-8045-1fd7a949c67e"
    width="220"
    alt="Step 2"
  />
  <img
    src="https://github.com/user-attachments/assets/7fd1efb9-49d9-4caa-a32e-aff71566c64c"
    width="220"
    alt="Step 3"
  />
  <img
    src="https://github.com/user-attachments/assets/ac9c2e6c-ad7b-4bed-959b-d44fe992ac6e"
    width="220"
    alt="Step 4"
  />
</p>


---

## ✨ Key Features

### 📸 1. Verify Bill & Change (Full Auto)
The complete loop. The user takes a photo of the bill, a photo of the cash they handed over, and a photo of the change they received. The AI calculates the math and verifies if the change is correct using computer vision to count the coins and notes.

Watch a short walkthrough of **ND-Money’s bill verification and change detection flow**, demonstrating how the system helps users quickly verify currency and handle change with confidence.

👉 **[Watch the demo on YouTube](https://www.youtube.com/watch?v=_2EsGE4REKc)**

[![ND-Money Verify Bill & Change Demo](https://img.youtube.com/vi/_2EsGE4REKc/maxresdefault.jpg)](https://www.youtube.com/watch?v=_2EsGE4REKc)



### 🧮 2. Check My Change (Visual Picker)
A hybrid flow where the user inputs what they paid using **Visual Money Cards** (tapping an image of a $20 bill rather than typing "20") and scans the change received. The app visually highlights exactly which notes are missing or extra.

Watch a short walkthrough of the **Check my change flow**, showing how transactions move through the system and how the primary user interactions work end-to-end.

👉 **[Watch the demo on YouTube](https://www.youtube.com/watch?v=i3c02MN0B4k)**

[![ND-Money Core Money Flow Demo](https://img.youtube.com/vi/i3c02MN0B4k/maxresdefault.jpg)](https://www.youtube.com/watch?v=i3c02MN0B4k)



### 🤝 3. Payment Assistant
A user scans the contents of their wallet. The AI analyzes the available denominations and suggests the **optimal combination** of notes to pay a specific bill, prioritizing exact change to reduce social anxiety at the register.

👉 **[Watch the Pay Helper demo on YouTube](https://www.youtube.com/watch?v=_2EsGE4REKc)**

[![ND-Money Pay Helper Demo](https://img.youtube.com/vi/_2EsGE4REKc/maxresdefault.jpg)](https://www.youtube.com/watch?v=_2EsGE4REKc)


### 🏪 4. Merchant Mode (Give Change)
Designed for neurodivergent employees. It calculates the change due and displays a **visual map** of exactly which notes and coins to pick from the register to hand to the customer.

Watch a quick demo of **ND-Money’s Merchant Mode**, designed for ND folks working the cash register and point-of-sale workflows.

👉 **[Watch the demo on YouTube](https://www.youtube.com/watch?v=IGCEPZj7300)**

[![ND-Money POS Demo](https://img.youtube.com/vi/IGCEPZj7300/maxresdefault.jpg)](https://www.youtube.com/watch?v=IGCEPZj7300)


### 🗣️ Voice-First Input
Integrated speech-to-text allows users to simply say "Twenty-five dollars" rather than struggling with a number pad.

### 📡 Hybrid AI Engine
*   **Online:** Uses **Google Gemini 3.0 Flash** for high-level reasoning, complex scene analysis, and payment advice.
*   **Offline:** Uses on-device  **custom trained small classifiers** that run on **TensorFlow Lite** models for detecting and counting currency when internet connectivity is poor.

## 🧠 Client-Side Composite AI Pipeline (WASM)

The app runs a **fully client-side Composite AI Pipeline** using **WebAssembly (WASM)** via `@mediapipe/tasks-vision`.
The problem is intentionally split into two stages:

* **Localization** → *Where is the object?*
* **Classification** → *What is the object?*

This separation improves accuracy, performance, and resilience in real-world conditions.

## 🧩 Pipeline Architecture

### **Stage 1: Localization — Global Object Detection**

**Engine:** MediaPipe Object Detector (`efficientdet_lite0`)
**Role:** Acts as a lightweight *Region Proposal Network* (RPN), drawing bounding boxes around potential objects in the frame.

**Why `efficientdet_lite0`?**

* Quantized **INT8** model
* Optimized for mobile CPUs / GPUs
* Consistently achieves **<100ms inference**, even on older Android devices

#### 🔁 Fallback Mechanism — *Smart Crops*

Object detectors can fail with:

* Fanned currency notes
* Extreme angles
* Partial occlusions

**Algorithm**

* If detection fails (or as a supplement), the frame is sliced into **6 overlapping Smart Crops**:

  * 4 quadrants
  * Center crop
  * Full frame

**Benefit**
Even if the detector misses the object, **relevant visual data is still passed to the classifier**, dramatically improving recall.

### **Stage 2.0: Classification - Online Mode**

#### 🏗️ AI Architecture Decision: Why Gemini 3 Flash?

For this specific use case, I selected **Gemini 3 Flash Preview** over older models (Gemini 1.5 Pro/Flash). Here is the technical justification:

### 1. The "Checkout Latency" Constraint

*   **The Problem:** Users with dyscalculia experience acute anxiety at the checkout line. Every second of delay increases social pressure. A 3-4 second latency (common with Gemini 1.5 Pro) feels like an eternity when a line is forming behind you.
*   **The Solution:** Gemini 3 Flash offers significantly lower **Time-To-First-Token (TTFT)**. By setting the `thinkingBudget` to 0, we leverage the model's raw speed to return structured JSON in sub-seconds, creating a "real-time" feeling that is critical for accessibility tools.

### 2. Spatial Grounding (Bounding Boxes)
*   **The Problem:** Older LLMs often "hallucinate" coordinates. They might correctly identify a $10 bill but draw the bounding box in the wrong location.
*   **The Solution:** Gemini 3 has vastly improved **spatial reasoning capabilities**. It can accurately return `[ymin, xmin, ymax, xmax]` coordinates for multiple overlapping objects (fanned cash). This accuracy is non-negotiable for our AR overlay feature—if the "Red X" appears on the wrong note, the user might give away the wrong money.

### 3. Combinatorial Reasoning (The "Knapsack Problem")
*   **The Problem:** The "Payment Assistant" feature (suggesting which notes to use to pay a $17.50 bill) is a variation of the Knapsack optimization problem. Smaller/older models often default to "give the largest note," which isn't helpful.
*   **The Solution:** Gemini 3 demonstrates stronger logic coherence. It can follow complex heuristics (e.g., "Prioritize exact change," "Get rid of heavy coins first") without needing a massive context window or chain-of-thought prompting.

### 4. Strict Schema Adherence
*   **The Problem:** The app relies entirely on a strict JSON schema to render the UI. Conversational models often add "Here is the analysis..." filler text, breaking the JSON parser.
*   **The Solution:** Gemini 3 Flash follows `responseSchema` constraints more rigidly than previous generations, reducing client-side parsing errors to near zero.

---

### **Stage 2.1: Offline Classification(if gemini api is unavailable/offline mode) — Custom Encoder–Decoder**

**Engine:** MediaPipe Image Classifier using custom `.tflite` models
**Architecture:** Encoder–Decoder inspired by Microsoft’s `bank_note_net`

* **Encoder:** Extracts high-level features
  *(textures, holographic strips, typography, security patterns)*
* **Decoder:** Maps features to a probability distribution
  *(e.g. `USD_20`, `USD_50`, `INR_100`, `Background`)*

#### 🌍 Dynamic Model Loading

To minimize memory usage:

* The app **does not load a global classifier**
* Uses **Geolocation** to lazy-load only the relevant model

  * `classifier_INR.tflite`
  * `classifier_USD.tflite`
  * etc.

**Quantization**

* Models are **Float16 / INT8**
* ~**2MB per currency**
* Optimized for low RAM usage inside a mobile WebView



## 🎯 Accuracy & Logic — *The Heuristic Layer*

Raw AI output is noisy. A dedicated post-processing layer improves reliability and removes false positives.


### **1. Bounding Box Logic (NMS Variant)**

* **IoU (Intersection over Union)**
  Measures overlap between detector boxes and Smart Crops

* **Containment Ratio**

  * If a low-confidence box is **>40% contained** inside a higher-confidence box of the same class → discard it

* **Center Distance Clustering**

  * Boxes predicting the same value with centers within **20% of the image diagonal** are merged


### **2. Weighted Confidence Scoring**

Not all predictions are treated equally:

| Source          | Multiplier |
| --------------- | ---------- |
| Object Detector | **1.2×**   |
| Smart Crop      | **0.9×**   |

**Detector Bonus:**  Boxes found by the Object Detector get a 1.2x score multiplier (because the AI "saw" an object).

**Blind Crop Penalty:** "Smart Crops" get a 0.9x score penalty (because they are blind guesses).


**Result**
* This biases the system towards actual objects while keeping the Smart Crops as a safety net for difficult angles.
* Biases decisions toward *true object detections*
* Keeps Smart Crops as a safety net for difficult angles



### **3. Ghost Killing (Currency-Specific Heuristics)**

**Problem**
Visually similar currencies can produce weak, overlapping signals
*(e.g., INR 20 vs INR 50)*

**Solution**

* Currency-aware suppression rules
* Example:

  * If a **weak ₹200** signal appears inside a **strong ₹50** detection
    → suppress the ₹200 as a texture misread

This dramatically reduces false positives in real-world lighting.



## 📲 UI Integration — Coordinate Mapping

* **Normalization:**
  TF Lite returns bounding boxes in normalized coordinates *(0.0 → 1.0)*

* **Canvas Projection:**
  Coordinates are mapped to viewport dimensions to render **AR overlays** (green/red badges)

* **Performance:**
  The full pipeline
  *(Capture → Detect → Crop → Classify → Filter → Render)*
  runs inside a `requestAnimationFrame` loop, ensuring:

  * Zero React UI blocking
  * Smooth real-time video feed



## 🚀 Why This Approach?

* **🔐 Privacy(offline mode)**
  All inference runs on-device — no images leave the phone in Offline Mode

* **⚡ Low Latency**
  No HTTP calls. End-to-end inference in milliseconds enables a real-time AR experience

* **🛡️ Resilience**
  The **Detector + Smart Crop hybrid** reliably handles fanned notes and odd angles — a known failure mode of standard object detectors


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

This project utilizes custom-trained TensorFlow Lite classifier models for offline on-device currency detection(still in beta mode). I would like to give a special mention to [Microsoft's Bank note note](https://github.com/microsoft/banknote-net) .

I adapted concepts from their research, specifically fusing their **encoder-decoder model architecture**, to create the lightweight mobile classifier's that run using tensorflow-lite/lightrt on any edge device out there. Their work on robust currency embeddings was instrumental in enabling this apps offline functionality.

---

## 🚀 Coming to the Google PLay store for Android Phones Soon

Internal Test Link --> https://play.google.com/apps/internaltest/4701315411457144348

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.


