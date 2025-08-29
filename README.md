Active Breaks
A free, open source application designed to help office workers reduce shoulder and neck pain through regular break exercises.
About the Project
Active Breaks was developed by a physiotherapist who constantly sees patients with work-related pain from computer use. The application displays fullscreen exercise videos and ensures users complete the entire exercise sequence before returning to work.
Features
	•	Fullscreen kiosk mode - prevents users from skipping their break
	•	Code protection - only the correct unlock code can end a break session
	•	macOS integration - hides dock and menu bar during use
	•	Configurable settings - duration, number of videos, break timing
	•	Multi-monitor support - displays on all connected screens
	•	System tray integration - runs discreetly in the background
Installation
Requirements
	•	macOS 10.14+
	•	Python 3.8+
	•	PySide6
Installation Steps
	1	Clone repository: git clone https://github.com/[your-username]/active-breaks.git
	2	cd active-breaks
	3	
	4	Create virtual environment: python3 -m venv .venv
	5	source .venv/bin/activate
	6	
	7	Install dependencies: pip install -r requirements.txt
	8	
	9	Run the application: python main.py
	10	
Usage
	1	Start the app - an icon will appear in the system tray
	2	Right-click the icon to open the menu
	3	Select "Show break now" to test the functionality
	4	Set unlock code via "Settings" to prevent skipping breaks
Keyboard Shortcuts
	•	⌘ + ⌥ + L - Opens unlock dialog during break
Configuration
Settings are automatically saved in ~/.active_breaks_cache/settings.json. You can modify:
	•	Break duration (10-3600 seconds)
	•	Videos per break (1-10)
	•	Post-break time (0-600 seconds)
	•	Unlock code (empty = user can choose any code)
	•	Audio (start with/without sound)
Development
Contributions Welcome!
This project needs help with:
	•	macOS kiosk mode improvements
	•	UI/UX enhancements
	•	Video management system
	•	Automatic break scheduling
	•	Testing on different macOS versions
Development Setup
# Clone and setup as described above
cd active-breaks
source .venv/bin/activate

# Install development dependencies
pip install -r requirements-dev.txt

# Run tests
python -m pytest tests/
Current Known Issues
See Issues for a complete list. Help is especially wanted for:
	•	Unlock button responsiveness - button doesn't always respond to clicks
	•	Kiosk mode escapes - users can still exit via various shortcuts
	•	Video loading indicators - no feedback during video loading
Architecture
active-breaks/
├── main.py                 # Main application and system tray
├── settings.py            # Configuration management
├── fullscreen_break.py    # Fullscreen break window
├── video_player.py        # Video playback and controls
└── utils/
    ├── kiosk.py          # macOS kiosk mode manager
    └── logger.py         # Logging system
Roadmap
Phase 1 - Stability
	•	[ ] Fix unlock button responsiveness
	•	[ ] Improved macOS kiosk mode
	•	[ ] Robust error handling and logging
	•	[ ] Standalone app bundle (.dmg installer)
Phase 2 - Features
	•	[ ] Automatic break scheduling
	•	[ ] Multiple exercise categories
	•	[ ] User-defined videos
	•	[ ] Statistics and progress tracking
Phase 3 - Expansion
	•	[ ] Windows/Linux support
	•	[ ] Web-based admin panel
	•	[ ] Calendar system integration
	•	[ ] Enterprise deployment tools
License
This project is licensed under the MIT License - see the LICENSE file for details.
Support
	•	Issues: GitHub Issues
	•	Email: aftermath6082@gmail.com
	•	Discussions: GitHub Discussions
Acknowledgments
	•	Developed by a physiotherapist for the benefit of all office workers
	•	Inspired by the need for better workplace ergonomics and fewer work-related injuries
	•	Thanks to all contributors and testers

Important: This is not a replacement for professional physiotherapy treatment. Consult a healthcare professional if you have persistent pain.
