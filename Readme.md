<div align="center">

<a href="https://github.com/Shreyashg07/GDG-PROMPT-INJECTION-CTF-LAB">

<img src="./Prompt%20Injection%20CTF%20Room%20Banner.png" alt="Prompt Injection CTF Room - GDG Symbiosis Skills and Professional University" width="100%">

</a>

<br>

# 🛡️ [Prompt Injection CTF Room](https://github.com/Shreyashg07/GDG-PROMPT-INJECTION-CTF-LAB)

### Google Developer Student Clubs — Symbiosis Skills and Professional University

**An interactive Capture The Flag laboratory for learning Prompt Injection and AI Security.**

<br>

[![🌐 Live CTF](https://img.shields.io/badge/🌐_LIVE_CTF-Play_Now-4285F4?style=for-the-badge)](https://gdg-prompt-injection-ctf-lab.onrender.com/)
[![💻 Source Code](https://img.shields.io/badge/💻_SOURCE_CODE-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/Shreyashg07/GDG-PROMPT-INJECTION-CTF-LAB)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)]

</div>

---

# 🎯 About the Lab

**Prompt Injection CTF Room** is a hands-on AI security challenge developed for **Google Developer Student Clubs at Symbiosis Skills and Professional University**.

The lab simulates an internal AI assistant that contains sensitive information and is protected by security rules.

Participants must interact with the simulated assistant, identify weaknesses in its instruction-handling logic, discover hidden information through a controlled prompt-injection challenge, and submit the final flag.

The application is intentionally designed as a **local/educational CTF environment** rather than a production AI assistant.

---

# 🧠 What You'll Learn

The challenge introduces practical concepts related to:

- Prompt Injection
- Instruction Confusion
- System Prompt Security
- AI Security Testing
- Sensitive Information Disclosure
- Social Engineering Against AI Systems
- Security Boundary Bypass
- AI Red Teaming
- CTF Methodology
- Secure AI Application Design

---

# 🚩 Challenge Objective

Your mission is to compromise the simulated **SecureCorp AI Assistant** and retrieve the hidden CTF flag.

The challenge is designed around a conversation-based attack chain.

```text
┌──────────────────────────┐
│      AI Assistant        │
│                          │
│  "How can I help you?"   │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│   Explore the Assistant  │
│                          │
│   Discover hidden clues  │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│   Identify Prompt        │
│   Injection Weakness     │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│   Trigger Verification   │
│        Workflow          │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│   Extract Encoded Data   │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      Decode → Flag       │
└──────────────────────────┘
```

---

# 🖥️ CTF Interface

The application provides two main components.

## 🤖 AI Console

The AI console allows participants to communicate with the simulated assistant.

Participants can:

- Send messages
- Observe AI responses
- Discover conversation clues
- Investigate internal information
- Explore the challenge logic

---

## 🚩 Flag Submission

After discovering the required information, participants can submit the flag through the dedicated verification panel.

The application validates the submitted flag and returns the challenge result.

---

# 🔐 How the Challenge Works

The lab uses a deliberately simplified simulated AI backend.

The Flask application:

1. Receives the participant's message.
2. Processes the input through the challenge logic.
3. Maintains a small conversation state.
4. Returns a simulated AI response.
5. Provides a controlled path toward the hidden challenge data.
6. Allows the participant to submit the final flag.

This approach makes the challenge deterministic and suitable for workshops and classroom environments.

---

# 🧩 Challenge Flow

The intended challenge progression is approximately:

### 1. Reconnaissance

Start a conversation with the assistant.

Look for:

- Unusual responses
- References to internal information
- Security-related hints
- Unexpected instructions

### 2. Follow the Clues

The assistant gradually reveals information that points toward an internal communication workflow.

### 3. Identify the Injection Opportunity

Participants need to recognize that instructions contained within apparently trusted content can influence the assistant's behavior.

### 4. Trigger the Verification Workflow

The challenge contains a simulated verification mechanism.

Participants must discover how the mechanism can be activated through conversation.

### 5. Recover the Encoded Reference

The challenge returns an encoded value as part of the simulated verification process.

### 6. Decode the Value

Decode the recovered Base64 value to obtain the challenge flag.

### 7. Submit the Flag

Enter the recovered flag into the **Submit Flag** panel.

---

# 🏗️ Architecture

```text
                     ┌───────────────────────┐
                     │       Web Browser      │
                     └───────────┬───────────┘
                                 │
                                 ▼
                     ┌───────────────────────┐
                     │     Flask Web App     │
                     └───────────┬───────────┘
                                 │
                  ┌──────────────┴──────────────┐
                  │                             │
                  ▼                             ▼
        ┌──────────────────┐          ┌──────────────────┐
        │    /chat         │          │    /submit       │
        │                  │          │                  │
        │ Challenge Logic  │          │ Flag Validation  │
        └────────┬─────────┘          └────────┬─────────┘
                 │                             │
                 ▼                             ▼
        ┌──────────────────┐          ┌──────────────────┐
        │ Simulated AI     │          │ Challenge Result │
        │ Response Engine  │          │                  │
        └──────────────────┘          └──────────────────┘
```

---

# 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Backend | Python |
| Web Framework | Flask |
| Frontend | HTML5 |
| Styling | CSS3 |
| Client Logic | JavaScript |
| Encoding | Base64 |
| Deployment | Render |

The repository is intentionally lightweight and does not require a database or external AI model for the challenge logic.

---

# 📁 Project Structure

```text
GDG-PROMPT-INJECTION-CTF-LAB/
│
├── Prompt Injection CTF Room Banner.png
├── Readme.md
├── app.py
├── index.html
├── style.css
└── requirements.txt
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/Shreyashg07/GDG-PROMPT-INJECTION-CTF-LAB.git

cd GDG-PROMPT-INJECTION-CTF-LAB
```

## 2. Create a Virtual Environment

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

### Windows

```powershell
python -m venv venv

venv\Scripts\activate
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Start the Flask Application

```bash
python app.py
```

The application will start locally.

Open:

```text
http://127.0.0.1:5000/
```

---

# 🌐 Live CTF

The hosted version of the challenge is available here:

### 🚩 [Launch Prompt Injection CTF Room](https://gdg-prompt-injection-ctf-lab.onrender.com/)

### 💻 [View Source Code](https://github.com/Shreyashg07/GDG-PROMPT-INJECTION-CTF-LAB)

---

# 🎓 GDG Workshop

This project was created as an educational security laboratory for:

**Google Developer Student Clubs  
Symbiosis Skills and Professional University**

The lab can be used during workshops to demonstrate how seemingly trusted instructions can manipulate an AI application's behavior.

---

# 🔬 Security Concepts Demonstrated

## Prompt Injection

Prompt injection occurs when attacker-controlled input influences an AI system to behave contrary to its intended instructions.

## Indirect Prompt Injection

The challenge demonstrates how information presented as trusted internal content can contain instructions that influence an AI assistant.

## Sensitive Data Exposure

The simulated assistant contains a protected challenge value that participants must discover through the intended attack chain.

## AI Red Teaming

Participants approach the assistant as an attacker and attempt to identify weaknesses in its instruction-processing behavior.

---

# 🧪 Learning Exercise

After completing the challenge, consider the following:

### Challenge Questions

1. Which input caused the assistant's behavior to change?
2. Which information source contained the malicious instruction?
3. Why did the simulated assistant trust that instruction?
4. How could a real AI application prevent this behavior?
5. What security controls should be placed around sensitive data?
6. How should applications treat instructions retrieved from external content?
7. What would happen if the application used a real LLM instead of deterministic challenge logic?

---

# 🛡️ Defensive Takeaways

Developers building AI-powered applications should consider:

- Treating external content as untrusted input
- Separating system instructions from user-controlled data
- Applying strict authorization around sensitive operations
- Avoiding direct exposure of secrets to model context
- Validating tool calls server-side
- Implementing output filtering
- Logging AI security events
- Testing applications against prompt-injection attacks
- Applying least privilege to AI agents and tools
- Never relying solely on model instructions for authorization

> **Important:** Prompt injection is an application-security problem, not simply a prompt-writing problem. Sensitive operations should be protected by deterministic application-level controls.

---

# ⚠️ Educational Use Only

This project is intentionally vulnerable and designed for controlled cybersecurity education.

Use the CTF only against the provided application or environments where you have explicit authorization.

Do **not** use prompt-injection techniques against third-party AI systems, applications, or data without permission.

---

# 👨‍💻 Author

<div align="center">

### Shreyash Ghare

Cybersecurity Researcher • Bug Hunter • VAPT • DFIR

[GitHub](https://github.com/Shreyashg07)

</div>

---

# ⭐ Support

If you found this CTF useful for learning AI security, consider giving the repository a ⭐.

<div align="center">

**Learn → Attack → Understand → Secure**

### 🛡️ Prompt Injection CTF Room

**Google Developer Student Clubs  
Symbiosis Skills and Professional University**

</div>
