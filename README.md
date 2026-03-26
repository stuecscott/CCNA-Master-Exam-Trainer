# CCNA-Master-Exam-Trainer
The CCNA exam is 120 questions. I built 288 questions - 2.4× the exam size - so you never see the same question twice before exam day.

# 🎓 CCNA Master Exam Trainer

An AI-powered, browser-based CCNA exam preparation tool with **288 hand-crafted questions** across all 8 critical exam topic areas. No installation, no server, no account, just open the HTML file and start studying.

> Built to complement the [CCNA Subnet Reference Tool](../ccna-subnet-tool) — use both together for complete CCNA preparation.

---

## 📸 Overview

This trainer goes beyond simple flashcards. Every question includes:

- **Detailed feedback on correct answers** — explains *why* it's right with key concepts highlighted
- **Detailed feedback on wrong answers** — explains *why* your choice was wrong AND why the correct answer is right
- **Hints** available in Study Mode before you answer
- **AI-generated bonus questions** powered by Claude (Anthropic API) for unlimited fresh practice
- **Built-in Subnet Calculator** for instant reference during subnetting questions
- **Score tracking** across your session with a running percentage

---

## 🚀 Getting Started

### Option 1 — Open directly in your browser (recommended)
```bash
git clone https://github.com/YOUR-USERNAME/ccna-master-trainer.git
cd ccna-master-trainer
open ccna_exam_trainer.html        # macOS
# or double-click the file in File Explorer (Windows/Linux)
```

### Option 2 — GitHub Pages (host it online)
1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your trainer is live at `https://YOUR-USERNAME.github.io/ccna-master-trainer/`

### Option 3 — Use in Claude
You can load this tool directly in a Claude conversation by uploading the HTML file and asking Claude to run it, or ask Claude to pull it from your GitHub Pages URL.

---

## 📚 Question Bank — 288 Questions

Questions are distributed across all 8 CCNA exam topic areas with a mix of Easy, Medium, and Hard difficulty levels:

| # | Topic | Questions | Difficulty Mix |
|---|-------|-----------|----------------|
| 1 | OSI Model Layer Identification | 35 | Easy/Medium/Hard |
| 2 | Subnetting & VLSM Calculations | 38 | Medium/Hard (calculation-heavy) |
| 3 | Routing Protocol Config & Troubleshooting | 45 | Medium/Hard |
| 4 | VLAN Configuration & Trunking | 37 | Easy/Medium/Hard |
| 5 | Access Control Lists (ACLs) | 31 | Medium/Hard |
| 6 | Spanning Tree Protocol (STP) | 31 | Medium/Hard |
| 7 | IPv6 Addressing & Configuration | 33 | Easy/Medium/Hard |
| 8 | Network Device Management & Security | 38 | Medium/Hard |
| | **Total** | **288** | |

### Question Types Included
- **Multiple Choice** — standard 4-option format matching the real CCNA exam
- **Scenario-Based** — show command output interpretation, topology analysis
- **Calculation** — subnetting math, path cost, EUI-64 derivation
- **Configuration** — identify correct IOS command syntax

---

## 🛠 Features

### Study Mode
- Hints available before answering
- Full explanation displayed after every answer (correct or wrong)
- Best for learning and understanding concepts

### Exam Mode
- No hints
- Harder question weighting
- Simulates real exam pressure
- Score shown in header throughout

### Topic Filtering
Practice all 8 topics in mixed rotation, or focus on one area at a time using the sidebar. The topic selector is always visible, so you can switch mid-session.

### Built-in Subnet Calculator
The same calculator from the [CCNA Subnet Reference Tool](../ccna-subnet-tool) is embedded directly. During a subnetting question, click "Subnet Calc" to instantly compute:
- Subnet Mask
- Block Size
- Network ID
- First & Last Host
- Broadcast Address
- Usable Hosts

### AI-Generated Bonus Questions (Claude API)
Every question screen includes a "Generate AI Question" button. Claude generates a brand-new, exam-quality question on the current topic — with full feedback — giving you an effectively unlimited question pool beyond the built-in 288.

> **Note:** The AI question generator requires an active internet connection. It uses the Anthropic Claude API, which is called directly from the browser. No API key setup needed when using claude.ai.

### Progress Tracking
- Live score header: Correct / Wrong / Total / Percentage
- Color-coded: green when passing (≥70%), red when below passing
- Session results screen at the end with grade and study recommendations

---

## 🎯 How to Use It Effectively

### For Daily Study Sessions
1. Pick one topic from the sidebar
2. Use **Study Mode** — read every explanation carefully, even when you get it right
3. Focus on understanding *why*, not just memorizing answers
4. Use the subnet calculator freely — it reinforces the math

### For Exam Simulation
1. Select **All Topics** from the sidebar
2. Switch to **Exam Mode**
3. Work through 60–120 questions without hints
4. Review your score and identify weak topics
5. Return to Study Mode for those specific topics

### For Subnetting Practice
1. Select **Topic 2: Subnetting & VLSM**
2. Keep the Subnet Calculator open
3. Try to calculate mentally first, then verify
4. Repeat until you can do /24, /25, /26, /27, /28, /29, /30 instantly

---

## 📐 CCNA Subnetting Quick Reference

```
Block sizes:  128   64   32   16    8    4    2    1
Subnet mask:  128  192  224  240  248  252  254  255

Octet 1:  /1   /2   /3   /4   /5   /6   /7   /8
Octet 2:  /9  /10  /11  /12  /13  /14  /15  /16
Octet 3: /17  /18  /19  /20  /21  /22  /23  /24
Octet 4: /25  /26  /27  /28  /29  /30   x    x

Usable hosts per subnet:
/30 = 2    /29 = 6    /28 = 14   /27 = 30
/26 = 62   /25 = 126  /24 = 254  /23 = 510  /22 = 1022
```

**Magic Number Method:** 256 − subnet mask octet = block size
Network ID = round IP down to the nearest multiple of block size
Broadcast = Network ID + Block Size − 1

---

## 📁 Repository Structure

```
ccna-master-trainer/
│
├── ccna_exam_trainer.html    # Complete application — single self-contained file
└── README.md                 # This file
```

The entire application — 288 questions, all CSS, all JavaScript, the subnet calculator, and the AI integration — is contained in a single HTML file. No dependencies, no build process, no npm install.

---

## 🔗 Related Tools

| Tool | Description |
|------|-------------|
| [CCNA Subnet Reference Tool](../ccna-subnet-tool) | Interactive subnet calculator + VLAN planner based on the classroom cheat sheet |
| Cisco Packet Tracer | Free network simulator from Cisco (recommended for hands-on lab practice) |
| GNS3 / EVE-NG | Advanced network simulators for complex topology practice |

---

## 🤝 Contributing

Pull requests welcome! Ideas for contributions:

- [ ] Additional questions for any topic (follow existing format in the JS question bank)
- [ ] Binary breakdown view for subnetting questions
- [ ] Timed exam mode with countdown
- [ ] Performance history across sessions (localStorage)
- [ ] Export wrong answers to a review list
- [ ] IPv6 subnetting calculator
- [ ] Drag-and-drop OSI layer matching questions
- [ ] Cisco IOS command flashcard mode

### Adding Questions
Questions follow this format in the `QUESTION_BANK` array:
```JavaScript
{
  topic: 0,           // 0-7 matching the 8 topic areas
  diff: 'medium',     // 'easy' | 'medium' | 'hard'
  type: 'Multiple Choice',  // or 'Scenario' | 'Calculation'
  q: 'Question text here',
  opts: ['Option A', 'Option B', 'Option C', 'Option D'],
  ans: 0,             // index of correct answer (0-3)
  hint: 'A hint without giving away the answer',
  correct_fb: 'Explanation of why the correct answer is right. Use <strong> for key terms.',
  wrong_fb: 'Explanation of why wrong, and why correct is right. Use <strong> for key terms.'
}
```

---

## 📄 License

MIT License — free to use, modify, and share. Attribution appreciated.

---

## 🙏 Acknowledgments

- Question content aligned with Cisco CCNA (200-301) exam objectives
- Study strategies based on *Master Your Exam: 8 CCNA Exam Question Types for 2025*
- AI question generation powered by [Anthropic Claude](https://www.anthropic.com)
- Built as a companion to hands-on lab practice in Cisco Packet Tracer

---

*No install. No login. No ads. Just open the file and study.*
