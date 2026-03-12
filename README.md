# Quizzenberg 🧠🎯

**Quizzenberg** is an engaging biochemistry quiz game built with Python. Test your knowledge with 5 randomly selected multiple-choice questions, earn points, receive instant feedback with sound effects, and get a personalized **Certificate of Excellence** emailed directly to you!

## ✨ Features

- **Interactive GUI** - Clean Tkinter interface with biochemistry-themed questions
- **Random Question Selection** - 5 unique questions from a bank of 10
- **Sound Effects** - Win/lose/good music feedback (pygame)
- **Score-based Feedback** - Three tiers: Excellent (20+), Good (10-19), Needs Work (<10)
- **Certificate Generation** - OpenCV overlays name/score on template
- **Automated Email** - Win32COM sends certificate via Outlook
- **Visual Results** - Score-based images and messages

## 📋 Topics Covered

- Carbohydrates (furanose rings)
- Vitamin deficiencies
- Protein structure/denaturation
- Elements & biochemistry
- Insulin composition

## 📦 Prerequisites

- **Windows OS** (Outlook + hardcoded paths)
- Python 3.7+
- Required libraries:
```bash
pip install opencv-python pygame pywin32
```
Assets Required (place in project root):
Images: QUIZ(2).png, Start.png, great.png, ok.png, bad.png, Certificate of Excellence.png
Sounds: winner.mp3, good.mp3, lost.mp3, correct(1).wav

🚀 Quick Start
1. Clone the repository
```bash
git clone https://github.com/yourusername/quizzenberg.git
cd quizzenberg
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Add required assets (images/sounds/certificate template)
4. Run the game
```bash
python quizzenberg.py
```
5. Play, score, and receive your certificate!


🎮 How to Play
1. Click "Start" on welcome screen
2. Answer 5 multiple-choice questions (radio button selection is FINAL)
3. View your score with feedback image/sound
4. Enter name & email to receive certificate
5. Certificate auto-generates and emails via Outlook

Scoring: 5 points per correct answer (Max: 25 points)

📁 Project Structure
```bash
quizzenberg/
├── quizzenberg.py          # Main game file
├── Generated certificates/ # Auto-generated certificates
├── Images/                 # UI assets (great.png, ok.png, etc.)
├── Sounds/                 # Audio feedback files
└── Certificate of Excellence.png  # Certificate template
```

⚠️ Current Limitations
1. Windows-only (Outlook + hardcoded paths: C:\Users\prano\...)
2. Hardcoded file paths need updating for other systems
3. No input validation for name/email
4. Requires all assets locally
5. Rules say "10 questions" but game uses 5


🔧 Path Configuration
Update these lines for your system:
```python
# Line ~60 - Certificate save path
cv2.imwrite(f'C:\\YOUR\\PATH\\Generated certificates\\{name}.png', template)

# Line ~68 - Email attachment path  
image_path = f"C:\\YOUR\\PATH\\Generated certificates\\{name}.png"
```

📧 Certificate Flow
```text
1. User submits name/email
2. OpenCV overlays text on template
3. Saves personalized PNG
4. Creates Outlook draft with attachment
5. Auto-sends certificate
```

🤝 Contributing
1. Fork the repository
2. Create your feature branch (```git checkout -b feature/AmazingFeature```)
3. Commit changes (```git commit -m 'Add some AmazingFeature'```)
4. Push to branch (```git push origin feature/AmazingFeature```)
5. Open Pull Request


Future improvements welcome:
1. Cross-platform support
2. Configurable paths
3. Input validation
4. More question banks
5. Web deployment


📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙌 Acknowledgments
1. Built for educational fun!
2. Uses OpenCV, Pygame, Tkinter, Win32COM
3. Certificate template design credit: Original project assets

⭐ Star this repository if you found it useful!
