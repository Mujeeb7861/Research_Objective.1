🧠 HTS Rule-Based Ransomware Detection
This repository contains a rule-based approach to detect ransomware attacks in the Honeypot-based Threat Simulation (HTS) environment. The project leverages observable indicators such as file extension changes, entropy, and content similarity to detect early signs of ransomware activity before files are fully encrypted.

📁 Repository Structure
bash
Copy
Edit
├── Code_objective_1.ipynb   # Main Jupyter notebook containing the detection algorithm
├── README.md                # Project documentation
🧪 Objective
Develop a lightweight and interpretable rule-based ransomware detection system using heuristics such as:

File extension renaming patterns

Shannon entropy analysis

SDHash content similarity

File size and structure anomaly

⚙️ Key Features
Early-stage ransomware detection (pre-encryption)

No ML model required – fast, explainable, and interpretable

Suitable for integration in real-time monitoring or forensic analysis

📊 Indicators Used
Indicator	Description
File extension change	Unusual extensions like .locked, .enc
Entropy	High entropy indicating encryption
SDHash Similarity	Low similarity suggests content alteration
File Size Anomaly	Sudden reduction or inflation in file size

🧰 Dependencies
Python 3.7+

Jupyter Notebook

pandas, numpy, hashlib

sdhash (CLI-based, optional)

To install Python dependencies:

bash
Copy
Edit
pip install -r requirements.txt
▶️ Getting Started
Clone the repo:

bash
Copy
Edit
git clone https://github.com/yourusername/hts-ransomware-detector.git
cd hts-ransomware-detector
Launch the notebook:

bash
Copy
Edit
jupyter notebook Code_objective_1.ipynb
Run the cells to simulate detection on a sample dataset.

🧪 Example Output
Files flagged: ["resume.docx.locked", "photo.jpg.enc"]

Detection reason: High entropy + altered extension + low SDHash similarity

📌 Limitations
Heuristic rules may miss novel obfuscation techniques

Requires tuning for specific environments or ransomware families
