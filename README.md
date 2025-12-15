# [Client Side AI Training Light](https://github.com/europanite/client_side_ai_training_light "Client Side AI Training Light")

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![OS](https://img.shields.io/badge/OS-Linux%20%7C%20macOS%20%7C%20Windows-blue)
[![CI](https://github.com/europanite/client_side_ai_training_light/actions/workflows/ci.yml/badge.svg)](https://github.com/europanite/client_side_ai_training_light/actions/workflows/ci.yml)
[![docker](https://github.com/europanite/client_side_ai_training_light/actions/workflows/docker.yml/badge.svg)](https://github.com/europanite/client_side_ai_training_light/actions/workflows/docker.yml)
[![GitHub Pages](https://github.com/europanite/client_side_ai_training_light/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/europanite/client_side_ai_training_light/actions/workflows/deploy-pages.yml)

![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Jest](https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&logo=jest&logoColor=white)
![Expo](https://img.shields.io/badge/expo-1C1E24?style=for-the-badge&logo=expo&logoColor=#D04A37)


!["web_ui"](./assets/images/web_ui.png)

 [PlayGround](https://europanite.github.io/client_side_ai_training_light/)

A Light-Weight KNN-based AI Image Classifier Playground. 

---

##  ✨ Features

* **100% client‑side**: No server required; privacy by design.
* **Fast training**: Uses MobileNet‑V2 as a feature extractor + KNN classifier for instant incremental learning.
* **Top‑k prediction view**: Shows predicted label and per‑class confidences.

---

## 🧰 How It Works

* **Feature extractor**: [@tensorflow-models/mobilenet] provides embeddings.
* **Classifier**: [@tensorflow-models/knn-classifier] stores examples and predicts via nearest neighbors.
* **Performance**: Training scales with example count; memory is bounded by image + embedding sizes.
* **Privacy**: All computation and data stay in the tab (no network I/O of user images).

---

## Data Structure

<pre>
DATA_DIRECTORY
├── CLASS_NAME_1
│   ├── image_01.png
│   ├── image_02.png
│   ├── image_03.png
│   ├── ...
├── CLASS_NAME_2
│   ├── image_01.png
│   ├── image_02.png
│   ├── image_03.png
│   ├── ...
├── CLASS_NAME_3
│   ├── image_01.png
│   ├── image_02.png
│   ├── image_03.png
│   ├── ...
 ...
</pre>

---

## 🚀 Getting Started

### 1. Prerequisites
- [Docker Compose](https://docs.docker.com/compose/)

### 2. Build and start all services:

```bash
# set environment variables:
export REACT_NATIVE_PACKAGER_HOSTNAME=${YOUR_HOST}

# Build the image
docker compose build

# Run the container
docker compose up
```

### 3. Test:
```bash
docker compose \
-f docker-compose.test.yml up \
--build --exit-code-from \
frontend_test
```

---

# License
- Apache License 2.0