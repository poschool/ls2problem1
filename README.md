Buffer Overflow Visualization

An interactive, educational web-based tool that teaches buffer overflow vulnerabilities through hands-on visualization. Watch in real-time how input data can overflow a buffer and corrupt adjacent memory on the stack.

License
🚀 Quick Start

Simply open index.html in your web browser. No installation, no dependencies, no server required.
bash

git clone https://github.com/yourusername/buffer-overflow-viz.git
cd buffer-overflow-viz
open index.html

Or use GitHub Pages:

https://yourusername.github.io/buffer-overflow-viz/

🎯 Features

    Interactive Buffer Manipulation — Adjust buffer size and test different inputs in real-time
    Live Memory Visualization — Watch overflow corrupt local variables, frame pointers, and return addresses
    Multiple Display Formats — View data as characters, hexadecimal, or ASCII codes
    Stack Frame Diagram — See exactly what memory gets overwritten and why it matters
    Educational Explanations — Understand the progression from safe → warning → critical
    Code Examples — Learn vulnerable vs. safe patterns side-by-side

📚 How It Works
The Vulnerability

When a program copies user input to a fixed-size buffer without checking length, overflow occurs. Extra data overwrites adjacent memory on the stack.
What Gets Corrupted

    Local Variables — Flags, checksums, validation data
    Saved Frame Pointer (RBP) — Causes crashes on function return
    Return Address — CRITICAL: Attacker can redirect execution to arbitrary code

Try It

    Keep buffer at 8 bytes and type "hello" → ✅ Safe
    Type "helloworld" (10 chars) → ⚠️ Corrupts local variables
    Type 24+ characters → ✗ Overwrites return address (exploit!

💡 Key Takeaways

    Buffers are fixed-size — They can only hold specific amounts of data
    Overflow corrupts nearby memory — Excess data doesn't disappear; it overwrites adjacent values
    Return addresses are targets — Code execution exploits work by overwriting where execution jumps next
    Input validation is essential — Always check length before copying user input
    Modern defenses help — Stack canaries, ASLR, DEP make exploits harder (but not impossible)

🛠️ Technology

    Pure HTML5 + Vanilla JavaScript — No frameworks, no dependencies
    Client-side only — Works offline, runs everywhere
    Responsive design — Works on desktop and mobile

Browser Support

Chrome, Firefox, Safari, Edge ✅
IE11 ⚠️
📖 For Educators

Perfect for teaching:

    Memory layout and the stack
    Why input validation matters
    How classic exploits work
    Security principles in systems programming

📄 License

MIT License — See LICENSE file for details
🤝 Contributing

Issues and pull requests welcome! This is an educational tool—contributions that improve clarity and interactivity are encouraged.
