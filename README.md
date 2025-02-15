## Intel xrandr Overscan Fix  

A simple script to fix HDMI overscan issues on Intel GPUs using `xrandr`.  

#### ⚠️ Important Note  
The default values (`HDMI-1` and `1920x1080`) are specific to my system.  
Before running the script, **modify them** to match your display setup.  
Using incorrect values may cause display issues.  

#### 📌 Why This Script?  
Some external monitors and TVs introduce overscan when connected via HDMI to Intel GPUs, causing parts of the screen to be cut off.  
This script adjusts the underscan settings to fix the issue.  

#### 🛠️ Usage  

##### 1️⃣ Identify Your Display Name  
Run the following command to list connected displays:  

```bash
xrandr --listmonitors
```  

Find the name of your HDMI output (e.g., `HDMI-1`, `HDMI-2`).  

##### 2️⃣ Check Available Resolutions  
Run:  

```bash
xrandr
```  

This will show supported resolutions. Choose the correct one for your display.  

##### 3️⃣ Modify the Script  
Edit the script and replace:  
- `HDMI-1` with your actual display name.  
- `1920x1080` with your desired resolution.  

##### 4️⃣ Apply the Fix  
Run the script:  

```bash
./xrandr_overscan_fix.sh
```  

#### 🛠️ Troubleshooting  
- If the display name is incorrect, `xrandr` will return an error.  
- If the resolution is unsupported, the screen may not display correctly.  
- Try different resolutions if the issue persists.
