# VisionKH 👁️

> Real-time AI object detection with Khmer language support — inspired by the Korean drama [Start-Up (스타트업)](https://en.wikipedia.org/wiki/Start-Up_(South_Korean_TV_series))

🔴 **Live Demo:** [visionkh.oudom.dev](https://visionkh.oudom.dev)

---

## Inspiration

While watching the Korean drama *Start-Up (2020)*, I was inspired by a scene where an AI app identifies objects through a camera to help visually impaired people. That moment sparked the idea for VisionKH — a real-time object detection web app that not only identifies objects but displays and speaks their names in **Khmer (ភាសាខ្មែរ)**.

---

## Features

- 📷 **Real-time object detection** — detects objects live through your camera
- 🇰🇭 **Khmer language** — displays detected object names in Khmer script
- 🔊 **Text-to-speech** — speaks the detected object name out loud
- 🎯 **Confidence score** — shows how confident the AI is for each detection
- 🖥️ **HUD UI** — sci-fi Iron Man style interface with glowing bounding boxes
- ⚡ **100% free** — runs entirely in the browser, no API key, no server, no cost

---

## Tech Stack

| Technology | Purpose |
|---|---|
| [Next.js](https://nextjs.org/) | Frontend framework |
| [TensorFlow.js](https://www.tensorflow.org/js) | Running AI model in the browser |
| [COCO-SSD](https://github.com/tensorflow/tfjs-models/tree/master/coco-ssd) | Pre-trained object detection model (80 classes) |
| [Tailwind CSS](https://tailwindcss.com/) | Styling |
| [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) | Text-to-speech |
| [Vercel](https://vercel.com/) | Deployment |

---

## Detectable Objects

VisionKH can detect **80 object classes** including:

`មនុស្ស` `កៅអី` `តុ` `ទូរស័ព្ទ` `កុំព្យូទ័រ` `រថយន្ត` `ឆ្កែ` `ឆ្មា` `ដំរី` `សៀវភៅ` and many more...

---

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Installation

```bash
# Clone the repository
git clone https://github.com/oudomm/visionkh.git

# Navigate into the project
cd visionkh

# Install dependencies
npm install

# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser and allow camera access.

### Build for Production

```bash
npm run build
npm start
```

---

## How It Works

1. **Camera** — browser accesses your device camera via `getUserMedia()`
2. **Detection** — each frame is passed to the COCO-SSD model running locally in your browser via TensorFlow.js
3. **Translation** — detected English labels are mapped to Khmer using a local translation dictionary
4. **Speech** — the Khmer label is spoken aloud using the Web Speech API
5. **Display** — glowing bounding boxes are drawn on a canvas overlay on top of the video

---

## Author

**Oudom** — [oudom.dev](https://oudom.dev)

---

## License

MIT License — feel free to use, modify and share.