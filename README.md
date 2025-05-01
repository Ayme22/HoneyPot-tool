# HoneyPot-tool : used for demonstrating purposes
# Deceptive RDP Honeypot
This project simulates a realistic Windows Remote Desktop (RDP) environment to lure and monitor unauthorized access. It features a fake corporate desktop environment with interactive components designed to deceive and gather intelligence on intruders.

## **📦 Features**
- Fake Desktop GUI: Simulated Windows-like interface with folder structure and clickable fake files.

- Login Page: Internal browser simulates a login screen using credentials from admin_creds.txt.

- Employee Dashboard: Displays fake employee records (names, emails, addresses, etc.).

- Fake Terminal: Responds with scripted outputs for common commands (whoami, ipconfig, etc.).

- Fake Email Client: Simulated inbox with predefined email content.

- Decoy Chat Window: Displays fabricated messages from "coworkers".

- Task Manager Simulation: Fake process/activity view for added realism.

- File Browser: Clickable fake files open simulated content in new windows.

- Auto-Updating Internal Dashboard: Random graphs and fake system alerts.

- Thread-Safe Logging: All activities are logged safely to avoid conflicts.
Log Location: All logs are stored in ~/Documents/Fake_Corp/.

## **📂 Directory Structure**
project/
├── honeypot.py                # Main Python script
├── admin_creds.txt            # Fake login credentials
├── resources/                 # Optional icons, images, or fonts
├── README.md                  # This file
└── Documents/
    └── Fake_Corp/             # All log files and screenshots go here
    
## **🛠️ Requirements**
Python 3.7+
Tkinter (comes with standard Python on most systems)
Pillow (pip install pillow)

## **▶️Running the Honeypot**
Run Manually
python honeypot.py
Run on Startup (Windows)
### To deploy as a persistent service that runs at login:

Convert to executable (optional): Use pyinstaller to bundle the script:

pip install pyinstaller
pyinstaller --noconsole --onefile honeypot.py
Add to Startup folder:

Press Win + R, type shell:startup, and press Enter.

Place a shortcut to honeypot.exe in this folder.

Run as a Windows Service (Advanced)
Install NSSM (Non-Sucking Service Manager).

Open Command Prompt as Administrator and install the honeypot as a service:

cmd
nssm install RDPHoneypot
In the NSSM GUI:

Path: Full path to Python executable or bundled .exe

Arguments: Full path to honeypot.py (if using Python script)

Startup directory: Project folder

Click Install service, then start it via:
cmd
nssm start RDPHoneypot

###**🧠Purpose**
This tool is designed for cybersecurity research, deception-based defense, and controlled environment testing. It must not be used in production networks or against real users.

###**⚠️Disclaimer**
This software is provided for educational and ethical security research purposes only. Misuse of this tool may violate laws or terms of service. The author is not responsible for any consequences arising from unauthorized or unethical use.
