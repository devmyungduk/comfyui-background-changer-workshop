# ComfyUI Background Changer Workshop

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Vue.js](https://img.shields.io/badge/vue.js-3.0+-green.svg)
![ComfyUI](https://img.shields.io/badge/ComfyUI-API-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

> **Complete workshop series for building a production-ready AI background changer app: from Python automation to web deployment.**

---

## 🎯 What You'll Build

An AI-powered background changer web application where users can:

```
1. Upload Photo
2. Remove Background (AI)
3. Enter Prompt ("sunset beach")
4. Generate New Background (AI)
5. Composite & Download Final Image
```

**Target Platform:**
- 🌐 Responsive Web App (Desktop + Mobile)
- ☁️ Works Locally or on Cloud GPU (RunPod)

---

## 🚀 Workshop Series Overview

### 📚 Learning Path (5 Steps)

```
Step 1: Text-to-Image Basics      [Fundamentals]
    ↓
Step 2: Background Removal         [Practical Application]  
    ↓
Step 3: Background Generation      [Advanced Workflow]
    ↓
Step 4: Web Frontend               [Full-Stack App]
    ↓
Step 5: Local & Cloud Setup        [Deployment Options]
```

---

## 🎓 Prerequisites

### No Experience Necessary

**Anyone can complete this workshop.**  
Everything is taught from scratch, step by step.

**You only need:**
- A computer (Windows or Mac)
- Interest in AI image processing | building web applications
- Willingness to learn 🚀

**No coding experience?** Perfect! This is a great way to start.  
**Some experience?** Great! You'll move faster.

---

### What We'll Help You Install

Free software with installation guides:
- **Python** (programming language)
- **ComfyUI** (AI image generation tool)
- **Git** (version control)
- **Node.js** (for Step 4 web development)

Cloud option:
- **RunPod** (pay-as-you-go for GPU access)

---

### Computer Requirements

**Choose your setup:**

#### Option A: Use Your Computer
- **Minimum:** 8GB RAM, NVIDIA GPU with 6GB VRAM
- **Recommended:** 16GB RAM, 8GB+ VRAM
- Best for: Learning locally, full control

#### Option B: Use Cloud GPU (Step 5)
- **Any laptop works** - even low-end!
- Use RunPod cloud service (pay as you go)
- Best for: No GPU, faster processing, big models

**No GPU at all?** Start with Option B!

---

### What You'll Learn

By the end of this workshop, you will know how to:

✅ Use AI models through APIs  
✅ Automate image processing with Python  
✅ Build a responsive web application  
✅ Deploy to cloud GPU (optional)  

**You'll have:** A real project for your portfolio!

---

## 📖 Detailed Roadmap

### ✅ [Step 1: Text-to-Image Basics](./01-basics-text-to-image/)
**Status:** Complete  
**Goal:** Learn ComfyUI API fundamentals

**What You'll Learn:**
- API communication basics (HTTP + WebSocket)
- Workflow manipulation with Python
- Automated image generation from text
- Progress tracking and result handling

**Output:** Working Python script that generates images from text prompts

**Time:** 1-2 hours

---

### ✅ [Step 2: Background Removal](./02-background-removal/)
**Status:** Complete  
**Goal:** Automate background removal with RMBG

**What You'll Learn:**
- Image-based workflows (vs text-based)
- File upload to ComfyUI server
- RMBG model for professional background removal
- Transparent PNG output handling

**Output:** Python script that removes backgrounds from any image

**Time:** 1-2 hours

---

### 🚧 [Step 3: Background Generation & Composition](./03-background-generation/)
**Status:** Coming Soon  
**Goal:** Generate and composite new backgrounds

**What You'll Learn:**
- Inpainting techniques for background generation
- Prompt-driven background creation
- Image composition and blending
- Complete background replacement pipeline

**Pipeline:**
```python
# 1. Generate background
python generate_background.py removed_bg.png --prompt "sunset beach"

# 2. Composite images
python composite.py foreground.png background.png --output final.png
```

**Output:** Complete background changer in Python

**Time:** 2-3 hours

---

### 🚧 [Step 4: Web Frontend with Vue.js](./04-web-frontend/)
**Status:** Planned  
**Goal:** Build responsive web interface (Desktop + Mobile)

**Technology Stack:**
- **Frontend:** Vue.js 3 + Vite ⭐ (Recommended)
- **Styling:** TailwindCSS (Responsive Design)
- **API:** WebSocket API ⭐ (Official & Stable)
- **HTTP Client:** Axios

**Why Vue.js?**
- ✅ Easiest to learn
- ✅ Great documentation
- ✅ Strong ecosystem
- ✅ Perfect for ComfyUI integration
- ✅ Responsive design out of the box

**Why No Native Mobile App?**
- ✅ Vue.js + TailwindCSS = Fully responsive
- ✅ Works perfectly on mobile browsers
- ✅ Can be PWA (Progressive Web App)
- ✅ No need for separate native app development

**Why WebSocket API?**
- ✅ Official ComfyUI support
- ✅ Real-time progress tracking built-in
- ✅ Most stable and tested
- ✅ Large community support
- ✅ No custom node needed

**UI Components:**
```
ImageUploader → BackgroundRemover → PromptInput → 
BackgroundGenerator → ResultPreview → DownloadButton
```

**Features:**
- Drag & drop image upload
- Real-time progress bars
- Before/after comparison
- Instant download
- **Fully responsive** (Desktop, Tablet, Mobile)

**Output:** Full-featured responsive web application

**Time:** 4-6 hours

---

### 🚧 [Step 5: Local & Cloud Setup](./05-local-cloud-setup/)
**Status:** Planned  
**Goal:** Run your app locally or on high-performance cloud GPU

#### Part A: Local Setup (For Everyone)

**What You'll Learn:**
- Installing ComfyUI on your local machine
- Setting up Python environment
- Downloading essential models
- Running the complete workflow locally

**Requirements:**
- GPU: 6GB+ VRAM (GTX 1060 or better)
- RAM: 8GB minimum (16GB recommended)
- Storage: 20GB for models

**Output:** Working local installation

**Time:** 1-2 hours

---

#### Part B: RunPod Cloud Setup (Optional - For High Performance)

**What You'll Learn:**
- RunPod account setup and GPU selection
- Using ComfyUI Template (with Manager pre-installed)
- **Volume Network** for persistent data storage
- JupyterLab essential commands
- Downloading models from HuggingFace
- Log monitoring and troubleshooting
- Cost optimization strategies

**Why RunPod?**
- ✅ Affordable high-end GPUs (A100, H100, RTX 4090)
- ✅ Pay-per-use pricing (as low as $0.39/hour)
- ✅ Pre-configured ComfyUI Template
- ✅ ComfyUI Manager already installed
- ✅ JupyterLab for easy management
- ✅ Perfect for large models (Flux, SDXL, Qwen)

**Volume Network Explained:**
- Your data persists even after pod termination
- No need to re-download models
- Pay only for storage when pod is off
- Huge cost savings!

**JupyterLab Commands Coverage:**
```bash
# Model downloads from HuggingFace
wget https://huggingface.co/...

# Check logs
tail -f /workspace/ComfyUI/comfyui.log

# Start ComfyUI
cd /workspace/ComfyUI && python main.py

# Monitor GPU usage
nvidia-smi

# And much more...
```

**Output:** Cloud-based GPU infrastructure ready to use

**Time:** 2-3 hours

---

## 🚀 Getting Started

### Quick Start (Steps 1-2)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/comfyui-background-changer-workshop
   cd comfyui-background-changer-workshop
   ```

2. **Start with Step 1:**
   ```bash
   cd 01-basics-text-to-image
   # Follow the README.md
   ```

3. **Progress to Step 2:**
   ```bash
   cd ../02-background-removal
   # Follow the README.md
   ```

### Learning Path Recommendations

**For Beginners:**
```
Week 1: Step 1 (Basics)
Week 2: Step 2 (Background Removal)
Week 3: Step 3 (Generation & Composition)
Week 4: Step 4 (Web Frontend)
```

**For Intermediate Developers:**
```
Day 1-2: Steps 1-2
Day 3-5: Steps 3-4
Week 2: Step 5 (Setup options)
```

**For Advanced Developers:**
```
Day 1: Review Steps 1-2, implement Step 3
Day 2-3: Complete Step 4 (Frontend)
Day 4-5: Explore both local and cloud setups
```

---

## 📁 Repository Structure

```
comfyui-background-changer-workshop/
│
├── README.md                          # This file
├── .gitignore
├── LICENSE
│
├── assets/                            # Images, diagrams
│   ├── roadmap-diagram.png
│   └── ui-mockup-web.png
│
├── docs/                              # Documentation
│   ├── FAQ.md
│   ├── TROUBLESHOOTING.md
│   └── PREREQUISITES.md
│
├── 01-basics-text-to-image/          # Step 1 ✅
│   ├── README.md
│   ├── examples/
│   └── src/
│
├── 02-background-removal/             # Step 2 ✅
│   ├── README.md
│   ├── examples/
│   └── src/
│
├── 03-background-generation/          # Step 3 🚧
│   ├── README.md
│   ├── examples/
│   └── src/
│
├── 04-web-frontend/                   # Step 4 🚧
│   ├── README.md
│   └── src/ (Vue.js project)
│
└── 05-local-cloud-setup/              # Step 5 🚧
    ├── README.md
    ├── local-setup/
    │   ├── windows-guide.md
    │   └── macos-guide.md
    └── runpod-setup/
        ├── account-setup.md
        ├── comfyui-template.md
        ├── jupyter-commands.md
        ├── model-downloads.md
        ├── volume-network.md
        └── cost-optimization.md
```

---

## 🛠️ Technology Stack

### Backend
- **Language:** Python 3.8+
- **Automation:** Custom scripts
- **Image Processing:** PIL, OpenCV
- **AI Models:** ComfyUI (RMBG, Stable Diffusion, Flux, etc.)

### Frontend (Step 4)
- **Framework:** Vue.js 3 + Vite ⭐
- **Styling:** TailwindCSS (Responsive)
- **HTTP:** Axios
- **WebSocket:** Native WebSocket API
- **State:** Pinia (Vue store)

### Infrastructure (Step 5)
- **Local:** ComfyUI on personal machine
- **Cloud:** RunPod (Optional)
- **Storage:** Volume Network (persistent)
- **Environment:** JupyterLab

---

## 🎯 Key Features

### Current (Steps 1-2)
- ✅ Text-to-image generation automation
- ✅ Background removal automation
- ✅ Python scripts with CLI
- ✅ Progress tracking
- ✅ Error handling

### Planned (Steps 3-5)
- 🚧 Background generation with prompts
- 🚧 Image composition
- 🚧 Responsive web UI with real-time preview
- 🚧 Desktop & mobile support (same app)
- 🚧 Local or cloud deployment options
- 🚧 Volume Network for persistent storage
- 🚧 JupyterLab command reference

### Advanced (Future)
- 🔮 Batch processing
- 🔮 Multiple AI models (Flux, SDXL, Qwen)
- 🔮 Advanced compositing options
- 🔮 User authentication
- 🔮 Image history

---

## 📊 Comparison with Other Tutorials

| Feature | This Workshop | Typical Tutorials |
|---------|--------------|-------------------|
| **Scope** | Complete app | Single feature |
| **Responsive** | ✅ Desktop + Mobile | ❌ Desktop only |
| **Deployment** | Local + Cloud | Local only |
| **AI Models** | Multiple (RMBG, SD, Flux) | One model |
| **Real Project** | ✅ Yes | ❌ No |
| **Cloud Option** | ✅ RunPod guide | ❌ Missing |
| **Frontend** | ✅ Modern (Vue.js) | ❌ Basic HTML |
| **Cost Flexible** | ✅ Local or cloud | ❌ One option |

---

## 🤝 Contributing

### Areas Needing Help
- 📝 Documentation improvements
- 🐛 Bug fixes
- ✨ New features
- 🎨 UI/UX enhancements
- 🌍 Translations
- 📊 Performance optimizations

---

## 📞 Support & Community

### Getting Help
- 📖 Read the docs in each step's README
- 🔍 Check [FAQ](./docs/FAQ.md)
- 🐛 [Open an issue](https://github.com/YOUR-USERNAME/comfyui-background-changer-workshop/issues)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Third-Party Licenses
- ComfyUI: GPL-3.0
- [ComfyUI-RMBG](https://github.com/1038lab/ComfyUI-RMBG): Check repository license
- Other models: Check individual licenses

---

## 🙏 Acknowledgments

- **ComfyUI** team for the amazing tool
- **[ComfyUI-RMBG](https://github.com/1038lab/ComfyUI-RMBG)** for background removal
- **Stability AI** for Stable Diffusion
- **Black Forest Labs** for Flux
- **RunPod** for GPU infrastructure
- All contributors and community members

---

## 📈 Roadmap

### Phase 1: Foundation ✅
- [x] Step 1: Text-to-Image
- [x] Step 2: Background Removal

### Phase 2: Advanced Features 🚧
- [ ] Step 3: Background Generation
- [ ] Step 4: Web Frontend (Responsive)

### Phase 3: Deployment 📅
- [ ] Step 5: Local Setup Guide
- [ ] Step 5: RunPod Cloud Guide
- [ ] Volume Network documentation
- [ ] JupyterLab command reference

### Phase 4: Optimization 🔮
- [ ] Performance improvements
- [ ] Multiple model support
- [ ] Advanced features
- [ ] Community contributions

---

## ⚡ Quick Links

### Essential
- [Step 1: Get Started →](./01-basics-text-to-image/)
- [FAQ](./docs/FAQ.md)
- [Troubleshooting](./docs/TROUBLESHOOTING.md)

### External Resources
- [ComfyUI Official](https://github.com/comfyanonymous/ComfyUI)
- [ComfyUI-RMBG](https://github.com/1038lab/ComfyUI-RMBG)
- [RunPod Platform](https://runpod.io)
- [Vue.js Documentation](https://vuejs.org)

---

<div align="center">

## 🚀 Ready to Start?

**No experience necessary. Start from zero. Anyone can learn.**

**[Begin with Step 1: Text-to-Image Basics →](./01-basics-text-to-image/)**

---

Made with ❤️ for the AI and ComfyUI community

**Star ⭐ this repo if you find it helpful!**

</div>
