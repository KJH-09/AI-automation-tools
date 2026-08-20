<div align="center">
  <h1>HOA(KJH) AI Automation Toolkit</h1>
  <p><strong>Developed by HOA(KJH)</strong></p>
  <p><em>An autonomous 24/7 AI coding assistant powered by Antigravity CLI (agy)</em></p>
  </div>

## 📥 Installation

**For Compiled/Release Version:**

1. **Download:** (https://github.com/KJH-09/AI-automation-tools)
2. **Extract:** Extract the downloaded file into your desired local directory for development.
3. **Initialize:** Double-click the `Start.exe` file inside the extracted project root folder to proceed with the initial environment setup.
4. **Run AI Loop:** Once the initialization is complete, double-click `Loop Start.exe` to launch the 24/7 AI automation program.

---

## ⚠️ Important Notes for .exe Version (Troubleshooting)

- **Antivirus False Positives:** Because these `.exe` files are newly compiled custom programs that run automated commands, Windows Defender or other antivirus software may falsely flag them as malware and prevent them from running. If the files are deleted or blocked, please add the installation folder to your antivirus **Exclusion List**.
- **Execution Policy:** Ensure that your Windows environment allows running local scripts (PowerShell Execution Policy), though the `.exe` attempts to bypass this automatically.
- **Do NOT run as Administrator** unless specifically required by your project, to avoid permission conflicts with your Antigravity CLI environment.

---

## 👨‍💻 Author & Credits

- **Developed by:** KJH (HOA)
- **GitHub:** [https://github.com/KJH-09](https://github.com/KJH-09)
- **License:** Proprietary License Applied (End User License Agreement). For details, please refer to the `LICENSE` file in the project root.

## 📖 Overview
This toolkit provides a universal automation environment utilizing the **Antigravity CLI (agy)**. It empowers the AI to automatically design, code, and develop all types of software (Web, App, Python, System Scripts, etc.) 24/7, based solely on your instructions.

Say goodbye to the repetitive manual tasks of writing lengthy prompts and setting up directory structures for every new project. By running a simple initialization script and answering a few natural questions, this toolkit instantly configures an environment where the AI can autonomously plan and commence development.

## ✨ Key Features

- **ynamic Initialization**  
  Simply input the type of program you wish to build. The AI analyzes your intent and dynamically generates follow-up questions to draft an initial project specification automatically.
- **Natural Language Support & Detection**  
  Whether you request setup in English, Korean ("한국어로 해줘"), or Japanese, the AI accurately grasps your linguistic preference. All structural documents and continuous loop outputs will be generated in your preferred language.
- **Markdown-Based State Management**  
  Unlike rigid databases, this system uses natural LLM-friendly Markdown (`TODO.md`, `FEEDBACK.md`, `SPEC.md`). This guarantees perfect context retention across sessions, ensuring the AI never loses track of its progress.
- **Infinite Daemon Loop**  
  The core `run_ai.ps1` script acts as an infinite daemon. Once a task unit is complete, the AI updates its status documents and immediately proceeds to the next task—requiring zero manual intervention.

## ⚙️ Requirements

- **OS:** Windows (PowerShell Environment)
- **AI CLI:** The Antigravity CLI (`agy`) must be installed and explicitly registered in your system's Environment Variables (`PATH`).

## 🚀 How to Use

### 1. Initialize the Environment
Copy the toolkit files into an empty directory where you want to develop your project. Double-click the initialization program and answer the AI-generated prompts:
```powershell
.\Start.exe
```
*(This sets up your directories, Git repo, and initial Markdown planning files.)*

### 2. Start the AI Daemon Loop
Deploy the AI worker by running the loop program. It will enter an infinite cycle of reading instructions, writing code, and updating its status:
```powershell
.\Loop Start.exe
```

### 3. Provide Feedback on the Fly
Need to pivot the direction or give specific commands? You don't need to stop the loop! Simply write your instructions directly into `plan/FEEDBACK.md`. The AI prioritizes this file at the start of its next iteration.

### 4. Graceful Shutdown
**Do not forcefully terminate the terminal!** To safely stop the AI after its current task finishes, create an empty file named `STOP_AI` (no extension) inside the `sys` directory.

## 📁 File Structure

```text
📂 project-root
 ├── 📂 plan/
 │    ├── SPEC.md       # Project architecture and specification
 │    ├── TODO.md       # Task backlog and progress tracking
 │    └── FEEDBACK.md   # User feedback and priority instructions
 ├── 📂 src/            # Primary source code directory
 ├── 📂 tools/          # Utilities and auxiliary scripts
 ├── 📂 sys/            # System internals (run_ai.ps1, STOP_AI trigger)
 └── 📂 .git/           # Automatically initialized Git repository
```


---
<div align="center">
  <small>&copy; 2026 HOA (KJH). All rights reserved.</small>
</div>