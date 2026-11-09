Apex Retail Broken Size Analysis
Login: admin / admin123 (change the password on the Users page after the first login)

FIRST TIME ON A COMPUTER
 1. Install Python 3.10+ (tick "Add python.exe to PATH"), then run Install_Requirements.bat once.
 2. Put app.py and Create_Shortcut.bat in the SAME folder and run Create_Shortcut.bat once -> "Apex Retail Broken Size Analysis" shortcut (Desktop + Start menu) + auto-start. (Only app.py is required; the other files are optional.)
 3. Use the shortcut. It starts the app by itself and opens it in its own window (Edge or Chrome required).

If the window says "refused to connect" / the app does not open:
 - The app (server) was not running. Create_Shortcut.bat now also makes it start automatically with Windows, so http://127.0.0.1:5000 keeps working.
 - http://127.0.0.1:5000 works ONLY on the computer that runs the app. Other computers must use the network link shown on the Install page (same Wi-Fi/LAN; allow Python in the Windows Firewall prompt the first time).
 - The app (server) was not running. Use the shortcut made by Create_Shortcut.bat (not an old one), or double-click Run_App.vbs.
 - Still failing? Double-click Run_App_debug.bat: the error message is shown in a console. Also check data\app.log.
 - Most common cause: Python/Flask missing -> run Install_Requirements.bat.

Other files
 Run_App.vbs          start without a console window (Add_to_Startup.bat = start with Windows)
 Run_App_debug.bat    start with a console window (shows errors)
 To stop: "Exit App" in the sidebar.
 Online / network     : HOST=0.0.0.0 PORT=5000 PUBLIC_URL=https://your-domain ADMIN_PASSWORD=<password> python app.py
 Install link + QR    : <app-link>/install  (other computers: the Windows Setup there makes a shortcut to the link; the app/server must be running)
 Windows exe          : build_windows.bat (no console window)
Data folder: .\data (exe: %APPDATA%\ApexRetailBrokenSizeAnalysis)
