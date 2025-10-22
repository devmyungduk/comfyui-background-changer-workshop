# Prerequisites Guide

Complete setup guide for ComfyUI API Workshop.

## System Requirements

### Hardware
- **GPU**: NVIDIA GPU with 6GB+ VRAM (8GB+ recommended for SDXL)
- **RAM**: 16GB+ system memory
- **Storage**: 20GB+ free space

### Software
- **Python**: 3.10+ (3.11 recommended) - *Not needed for Windows Portable*
- **Git**: For cloning repositories - *Not needed for Windows Portable*
- **Node.js**: 16+ (Required for Step 2 - Vue.js integration only)

---

## Choose Your Installation Method

### 🎯 Recommended: Windows Portable
**Best for beginners and Windows users**

✅ No Python installation needed  
✅ No command line required  
✅ Double-click to run  
✅ Everything pre-configured  

👉 **Jump to Step 3: Download ComfyUI**

### 🔧 Alternative: Git Clone
**For advanced users, macOS, or Linux**

✅ Latest updates from GitHub  
✅ Full control over dependencies  
✅ Works on all operating systems  
⚠️ Requires Python and Git knowledge  

👉 **Follow all steps 1-7**

### ☁️ Cloud Option: RunPod
**No local GPU needed**

✅ Access to powerful GPUs  
✅ Pay per hour  
✅ Pre-configured templates  

👉 **Skip to Cloud Setup section**

---

## ComfyUI Installation

> **Windows Portable users**: Jump directly to [Step 3: Download ComfyUI](#step-3-download-comfyui)  
> **Git Clone users**: Follow all steps  
> **RunPod users**: Skip to [Cloud Setup](#cloud-setup-runpod)

---

### Step 1: Install Python (Git Clone Only)

**⚠️ Skip if using Windows Portable**

#### Windows
1. Download from [python.org](https://www.python.org/downloads/)
2. Run installer
3. ✅ **IMPORTANT**: Check "Add Python to PATH"
4. Click "Install Now"

Verify installation:
```cmd
python --version
```

#### macOS
```bash
# Install Homebrew (if not installed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Python
brew install python@3.11

# Verify
python3 --version
```

---

### Step 2: Install Git (Git Clone Only)

**⚠️ Skip if using Windows Portable**

#### Windows
1. Download from [git-scm.com](https://git-scm.com/)
2. Run installer with default options

#### macOS
```bash
brew install git
```

Verify:
```bash
git --version
```

---

### Step 3: Download ComfyUI

#### Option A: Windows Portable (Recommended - Easiest)

1. **Download** the portable version:
   - 🔗 [Direct Download Link](https://github.com/comfyanonymous/ComfyUI/releases)
   - Look for "ComfyUI_windows_portable" (usually latest release)

2. **Extract** with [7-Zip](https://www.7-zip.org/)
   - Right-click → 7-Zip → Extract Here
   - If you have trouble: Right-click file → Properties → Unblock

3. **Ready to use!** You'll see:
   - `run_nvidia_gpu.bat` - For NVIDIA GPU users
   - `run_cpu.bat` - For CPU-only (slower)
   - `ComfyUI/` folder with everything pre-configured

**Skip to Step 6** (Download Models) if using portable version!

#### Option B: Git Clone (For advanced users)

```bash
# Clone the repository
git clone https://github.com/comfyanonymous/ComfyUI
cd ComfyUI
```

**Continue to Step 4** if using Git clone method.

---

### Step 4: Install PyTorch (Git Clone Only)

**⚠️ Skip Steps 4-5 if you used Windows Portable version**

**IMPORTANT**: The `requirements.txt` file already exists in the ComfyUI folder you just cloned. You will use it in the next step.

Choose the command based on your GPU:

#### Windows (NVIDIA GPU)

**For most GPUs (CUDA 11.8 - Compatible with most cards):**
```cmd
python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

**For newer GPUs (CUDA 12.1 - RTX 40 series, newer cards):**
```cmd
python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

**For latest GPUs (CUDA 12.4 - RTX 50 series and future cards):**
```cmd
python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
```

#### macOS (Apple Silicon / Intel)
```bash
python3 -m pip install torch torchvision torchaudio
```

#### Verify PyTorch Installation
```python
python
>>> import torch
>>> print(torch.cuda.is_available())  # Should return True on GPU systems
>>> print(torch.version.cuda)  # Check CUDA version
>>> exit()
```

---

### Step 5: Install ComfyUI Dependencies (Git Clone Only)

**⚠️ Skip this step if you used Windows Portable version**

**Run this command inside the ComfyUI folder:**

#### Windows
```cmd
python -m pip install -r requirements.txt
```

#### macOS
```bash
python3 -m pip install -r requirements.txt
```

**What this does**: Installs all required Python packages listed in the `requirements.txt` file that comes with ComfyUI.

---

### Step 6: Download AI Models

ComfyUI needs at least one Stable Diffusion model to work.

#### Model Storage Location
Place models in:
```
ComfyUI/models/checkpoints/
```

#### Recommended Models

1. **Stable Diffusion v1.5** (Fast, good for learning)
   - 🔗 [Download from HuggingFace](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5)
   - File: `v1-5-pruned-emaonly.safetensors` (4.27 GB)
   - Click "Files and versions" → Download the `.safetensors` file

2. **Stable Diffusion XL 1.0** (Higher quality, slower)
   - 🔗 [Download from HuggingFace](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0)
   - File: `sd_xl_base_1.0.safetensors` (6.94 GB)
   - Click "Files and versions" → Download the `.safetensors` file

#### Alternative: Civitai
Browse and download models from [Civitai](https://civitai.com/):
- Filter by "Checkpoint" type
- Choose `.safetensors` format
- Download and place in `ComfyUI/models/checkpoints/`

---

### Step 7: Run ComfyUI

#### Windows Portable Users

**Simply double-click:**
- `run_nvidia_gpu.bat` (for NVIDIA GPU)
- `run_cpu.bat` (for CPU only - slower)

**That's it!** The batch file handles everything automatically.

#### Git Clone Users

##### Windows
```cmd
python main.py
```

##### macOS
```bash
python3 main.py
```

**First launch may take 1-2 minutes** as ComfyUI initializes.

#### Expected Output
```
Total VRAM 8192 MB, total RAM 16384 MB
pytorch version: 2.x.x
...
To see the GUI go to: http://127.0.0.1:8188
```

#### Access ComfyUI
Open your browser and go to:
```
http://127.0.0.1:8188
```

---

## Verify Installation

### Test ComfyUI Workflow

1. **Open** `http://127.0.0.1:8188`
2. **Load** default workflow (should load automatically)
3. **Select** your downloaded model from the "Load Checkpoint" node
4. **Click** "Queue Prompt" (orange button on the right)
5. **Wait** for image generation (may take 10-30 seconds)
6. ✅ **Success**: Image appears in the interface

If you see a generated image, you're ready for the workshop!

---

## Troubleshooting

### Common Issues

#### "Python is not recognized"
- **Solution**: Reinstall Python with "Add to PATH" checked

#### "CUDA not available"
- **Check GPU**: `nvidia-smi` (Windows) or system info
- **Reinstall PyTorch** with correct CUDA version
- **Verify**: 
  ```python
  import torch
  print(torch.cuda.is_available())
  ```

#### "No module named 'torch'"
- **Solution**: Install PyTorch again (Step 4)

#### "Model not found"
- **Check location**: Model must be in `ComfyUI/models/checkpoints/`
- **Check format**: Use `.safetensors` or `.ckpt` files
- **Restart**: Restart ComfyUI after adding models

#### Out of Memory (VRAM)
- **Use smaller model**: Try SD 1.5 instead of SDXL
- **Lower resolution**: Reduce image size to 512x512
- **Enable optimizations**: Add `--lowvram` flag:
  ```bash
  python main.py --lowvram
  ```

#### macOS: "command not found: python"
- **Solution**: Use `python3` instead of `python`

---

## Cloud Setup (RunPod)

### What is RunPod?
RunPod is a cloud GPU rental service. Use it if you don't have a local GPU.

### Why Use RunPod for This Workshop?
- ✅ Instant access to powerful GPUs
- ✅ No local installation needed
- ✅ Pay only for what you use
- ✅ Pre-configured templates available

### Quick Start

#### 1. Create Account
1. Go to [RunPod.io](https://www.runpod.io/)
2. Sign up (free account available)
3. Add payment method (required even for free credits)

#### 2. Create a Pod

1. **Click** "Deploy" from dashboard
2. **Choose Template**:
   - **Recommended**: Search for "ComfyUI" template
   - This includes ComfyUI pre-installed with start scripts
   - Alternative: "RunPod PyTorch" template (requires manual setup)
3. **Select GPU**:
   - **Budget option**: RTX 3090 (~$0.39/hr)
   - **Balanced**: RTX 4090 (~$0.69/hr)
   - **High-end**: A100 (~$1.89/hr)
4. **Configure**:
   - Storage: 50GB minimum
   - Select closest region
5. **Deploy Pod**

#### 3. Access Your Pod

After deployment (1-2 minutes):

**Option A: Web Terminal (Easiest)**
1. Click "Connect" → "Start Web Terminal"
2. Web-based terminal opens in browser

**Option B: Jupyter Notebook**
1. Click "Connect" → "Jupyter Notebook"
2. Opens web-based Python environment
3. Click "New" → "Terminal" for command line

**Option C: SSH**
1. Click "Connect" → "SSH over exposed TCP"
2. Copy SSH command
3. Paste in your local terminal

#### 4. Start ComfyUI on RunPod

**If you used ComfyUI template:**

The template includes start scripts like `run_gpu.sh`.

```bash
# Find and run the start script
cd /workspace/ComfyUI  # or wherever ComfyUI is installed
./run_gpu.sh         # or ./comfyui_start.sh

# Alternative: Manual start
python main.py --listen 0.0.0.0
```

**Download a model (required):**
```bash
cd models/checkpoints
wget https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5/resolve/main/v1-5-pruned-emaonly.safetensors
cd ../..
```

#### 5. Access ComfyUI Web Interface

1. **Get Pod URL**: RunPod provides a public URL
2. **Port**: Add `:8188` to the URL
3. **Example**: `https://your-pod-id.runpod.net:8188`

### RunPod + Jupyter Workflow

**Will be detailed in Step 3 (Deployment):**
- Setting up persistent storage
- Creating custom templates
- Automating ComfyUI startup
- Using Jupyter for development
- Deploying as a public API

> **Note**: Full RunPod deployment guide will be in `03-Backend-Server-and-Deployment/`

---

## Next Steps

Once installation is verified:

1. ✅ ComfyUI runs and generates images
2. ✅ Python and dependencies installed
3. ✅ At least one model downloaded

**You're ready for:**
- **Step 1**: [Basic Python Script](../01-Basic-Python-Script/)
- **Step 2**: [Vue.js Frontend](../02-VueJS-Frontend-Integration/) (requires Node.js)
- **Step 3**: [Deployment](../03-Backend-Server-and-Deployment/) (includes full RunPod guide)

---

## Quick Reference

### Important Paths

**Windows Portable:**
```
ComfyUI_windows_portable/
├── run_nvidia_gpu.bat   # Double-click to start (GPU)
├── run_cpu.bat          # Double-click to start (CPU)
├── ComfyUI/
│   ├── models/
│   │   └── checkpoints/ # Place model files here
│   └── output/          # Generated images save here
└── python_embeded/      # Built-in Python
```

**Git Clone:**
```
ComfyUI/
├── main.py              # Run this to start ComfyUI
├── requirements.txt     # Dependencies (already included)
├── models/
│   └── checkpoints/     # Place model files here
└── output/              # Generated images save here
```

### Essential Commands

**Start ComfyUI (Portable):**
```
Double-click run_nvidia_gpu.bat
```

**Start ComfyUI (Git Clone):**
```bash
python main.py
```

**Start with low VRAM mode:**
```bash
python main.py --lowvram
```

**Check Python version:**
```bash
python --version
```

**Check installed packages:**
```bash
pip list
```

---

## Support Resources

- 📖 [Official ComfyUI Docs](https://github.com/comfyanonymous/ComfyUI)
- 💬 [ComfyUI Discord](https://discord.gg/comfyui)
- 🎥 [ComfyUI Tutorials](https://www.youtube.com/results?search_query=comfyui+tutorial)
- 🔧 [Troubleshooting Guide](./TROUBLESHOOTING.md)

---

**Ready to start?** → [Basic Python Script](../01-Basic-Python-Script/README.md)
