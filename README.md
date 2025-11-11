# 🧮 Binary Arithmetic Visualizer  
### _An Interactive Web Simulator for Booth’s, Restoring, and Non-Restoring Division Algorithms_

![GitHub repo size](https://img.shields.io/github/repo-size/yourusername/binary-arithmetic-visualizer?color=38bdf8)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML](https://img.shields.io/badge/tech-HTML-orange)
![CSS](https://img.shields.io/badge/tech-CSS-blue)
![JavaScript](https://img.shields.io/badge/tech-JavaScript-yellow)

---

## 🧭 Project Overview
The **Binary Arithmetic Visualizer** is a web-based educational simulator that demonstrates three major signed binary arithmetic algorithms used in digital electronics:

- **Booth’s Multiplication Algorithm**
- **Restoring Division Algorithm**
- **Non-Restoring Division Algorithm**

It provides a **step-by-step visualization** of arithmetic operations like add, subtract, and shift, allowing users to observe register contents (`AC`, `Q`, `Q-1`, `M`) at every iteration.  
Designed to help students understand the **hardware logic** behind multiplication and division.

---

## 🚀 Live Demo
👉 [**View the Project**](https://yourusername.github.io/binary-arithmetic-visualizer/)  
_(Replace with your hosted GitHub Pages or Netlify link)_

---

## ⚙️ Features

✅ Step-by-step binary register visualization  
✅ "Start", "Next Step", "Auto-Run", and "Reset" controls  
✅ Real-time explanations for every operation  
✅ Color-coded highlights — 🟩 Add, 🟥 Subtract, 🟨 Shift  
✅ Collapsible **Theory Section** for each algorithm  
✅ Modern gradient dark UI with glowing transitions  
✅ Sticky navigation bar for seamless switching  
✅ 100% offline functionality — pure HTML, CSS, JS  

---

## 🧠 Algorithms Implemented

### 🔹 Booth’s Multiplication Algorithm
Performs signed binary multiplication efficiently using bit-pair recoding.  

**Logic Table:**
| Q₀Q₋₁ | Operation |
|--------|------------|
| 01 | AC = AC + M |
| 10 | AC = AC - M |
| 00 / 11 | No Operation |
| — | Arithmetic Right Shift |

**Result:**  
Final product = `(AC + Q)`

---

### 🔹 Restoring Division Algorithm
Performs binary division by restoring the partial remainder when subtraction leads to a negative accumulator.

**Steps:**
1. Shift left `(AC, Q)`  
2. Subtract divisor `M` from `AC`  
3. If `AC < 0` → Restore AC, set Q₀ = 0  
4. Else keep result, set Q₀ = 1  
5. Repeat for n bits  

**Result:**  
Quotient → Q  
Remainder → AC

---

### 🔹 Non-Restoring Division Algorithm
Eliminates the restoration step, improving speed and efficiency.

**Steps:**
1. Shift left `(AC, Q)`  
2. If `AC ≥ 0` → `AC = AC - M`  
   Else → `AC = AC + M`  
3. If `AC ≥ 0` → `Q₀ = 1`  
   Else → `Q₀ = 0`  
4. Repeat for all bits  
5. If `AC < 0` → Final correction: `AC = AC + M`

---

## 🖥️ Project Structure

binary-arithmetic-visualizer/
│
├── index.html # Home page
├── booth.html # Booth’s Algorithm page
├── restoring.html # Restoring Division page
├── nonrestoring.html # Non-Restoring Division page
│
├── css/
│ └── style.css # Common UI styling
│
└── js/ # (Optional) External JS logic files


---

## 🧩 User Interface
### Key Components
- **Dark gradient UI** with glowing blue accents  
- **Register display** for AC, Q, M, and Q-1  
- **Explanation box** with operation details  
- **Auto-run** simulation for visualization  
- **Navbar** for quick algorithm switching  

### Example Pages
| Page | Description |
|------|--------------|
| Booth’s | Step-by-step signed multiplication |
| Restoring | Binary division with restoration |
| Non-Restoring | Optimized binary division |

---

## 🧮 Sample Output

**Input:**  
`M = -3`, `Q = 5`

**Output (Booth’s Algorithm):**
Final Product = -15
Binary Product = 11110001


**Input:**  
`Dividend = 13`, `Divisor = 3`

**Output (Non-Restoring Algorithm):**
Quotient = 4
Remainder = 1


---

## 💡 Educational Value

This simulator helps students:
- Visualize internal register transitions in binary arithmetic  
- Bridge theory and hardware-level implementation  
- Understand signed arithmetic, shifting, and two’s complement operations  
- Build conceptual clarity in **Computer Organization** and **Digital System Design**

---

## 🧰 Tech Stack

| Layer | Technology |
|--------|-------------|
| Frontend | HTML5 |
| Styling | CSS3 (Flexbox, Gradients, Glow Effects) |
| Logic | JavaScript (ES6) |
| Hosting | GitHub Pages / Netlify |
| IDE | VS Code |

---

## 🧾 How to Run Locally

```bash
# Clone the repository
git clone https://github.com/yourusername/binary-arithmetic-visualizer.git

# Move into project folder
cd binary-arithmetic-visualizer

# Open in browser
start index.html
```
✅ No dependencies, no installations required. Just open in any modern browser.

📈 Future Improvements

Add support for custom bit-widths (8-bit, 16-bit, 32-bit)

Integrate more algorithms (Array Multiplier, Newton-Raphson)

Export simulation steps as .pdf or .txt report

Add timing diagrams and performance comparisons

Include sound or animation cues for each operation

🧠 Acknowledgements

NIT Goa – Department of Electronics and Communication Engineering

Faculty of Digital System Design Laboratory

Open-source community for UI design inspiration

🧑‍💻 Developer

Your Name
B.Tech, Electronics and Communication Engineering
National Institute of Technology Goa

📧 Email: [your.email@example.com
]
🌐 GitHub: github.com/yourusername

🔗 LinkedIn: linkedin.com/in/yourprofile

🪪 License

Distributed under the MIT License.
See LICENSE for more information.

⭐ If you found this project helpful, please consider giving it a star on GitHub!