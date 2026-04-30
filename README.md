# Academic MicroGPT

A minimal, readable implementation of a GPT-like language model for educational use. This repository is designed for students to explore the inner workings of transformer-based models, including training and inference, with pure Python and no external dependencies.

---

## Repository Structure

- **microgpt.py** — The main script. Implements a simple GPT model, training loop, and inference. All logic is contained here and heavily commented for learning.
- **microgpt_walkthrough.md** — Step-by-step annotated guide to the code. Read this first!
- **assignment.html** — Assignment instructions for using MicroGPT with your own dataset.
- **input.txt** — The default dataset (one sample per line). Replace with your own text data for experiments.
- **definitions/** — Supplementary HTML explanations for key concepts:
  - `autograd_engine.html`, `backpropagation.html`, `feedforward.html`, `multihead_self_attention.html`, `adam_optimizer.html`
  - `images/` — Diagrams and visual aids (if present)

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/BPMSTC/academic-microgpt.git
   cd academic-microgpt
   ```
2. **Prepare your dataset:**
   - Place your text data in `input.txt`, one sample per line.
   - Or, let the script auto-download a default dataset (names list).
3. **Run the model:**
   ```bash
   python microgpt.py
   ```
   - Training progress and loss will be displayed.
   - After training, the script will generate new samples.

---

## Assignment

See `assignment.html` for instructions. You will:
- Choose a dataset
- Run MicroGPT
- Analyze and report on the results

---

## Learning Resources

- `microgpt_walkthrough.md` — Read this for a detailed explanation of every part of the code.
- `definitions/` — Open the HTML files for visual and conceptual explanations of neural network components.

---

## FAQ

**Q: Do I need any special libraries?**
A: No. Only Python 3.7+ is required.

**Q: Where do I put my data?**
A: In `input.txt`, one sample per line.

**Q: Where do I start?**
A: Read `microgpt_walkthrough.md` and then run `python microgpt.py`.

---

## License

This project is for educational use. Based on the work of Andrej Karpathy and the open-source community.
