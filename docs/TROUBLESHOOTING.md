# Troubleshooting Guide

## Common Issues

### Python Issues

**Issue**: `python: command not found`  
**Solution**: 
- Windows: Make sure Python was added to PATH during installation
- macOS: Use `python3` instead of `python`

**Issue**: Virtual environment won't activate  
**Solution**:
- Windows: Run `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` in PowerShell
- macOS: Check file permissions with `ls -la venv/bin/activate`

### ComfyUI Issues

**Issue**: Can't connect to ComfyUI  
**Solution**:
1. Verify ComfyUI is running: Open `http://127.0.0.1:8188` in browser
2. Check firewall settings
3. Ensure no other service is using port 8188

**Issue**: Workflow file not loading  
**Solution**:
1. Re-export workflow from ComfyUI as API Format
2. Verify JSON is valid using online JSON validator
3. Check file encoding (should be UTF-8)

### Step 1: Text-to-Image

**Issue**: `ModuleNotFoundError: No module named 'requests'`  
**Solution**: Activate virtual environment and run `pip install -r requirements.txt`

**Issue**: KSampler node not found  
**Solution**: Use a workflow with KSampler node (standard text-to-image workflow)

### Step 2: Background Removal

**Issue**: `RMBG node not found in workflow!`  
**Solution**: Install ComfyUI-RMBG via ComfyUI Manager

**Issue**: Background not fully removed  
**Solution**: Adjust RMBG sensitivity in JSON file (lower value = more aggressive)

### Step 4: Web Frontend

**Issue**: `npm: command not found`  
**Solution**: Install Node.js from [nodejs.org](https://nodejs.org/)

**Issue**: Port 5173 already in use  
**Solution**: Change port in `vite.config.js` or kill the process using that port

### Step 5: RunPod

**Issue**: Can't connect to RunPod pod  
**Solution**: 
1. Check pod status (must be running)
2. Use the correct connection URL from RunPod dashboard
3. Verify SSH key is configured correctly

**Issue**: Models not loading  
**Solution**: Check Volume Network is properly mounted and models are in correct folder

---

Still having issues? [Open an issue](https://github.com/YOUR-USERNAME/comfyui-background-changer-workshop/issues)
