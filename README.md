## WebPlayground Pro

A simplified yet powerful browser-based IDE built with vanilla JavaScript. This project is designed to demonstrate core web development fundamentals including DOM manipulation, cross-window communication, and the Blob API.

## 🚀 Key Features

- Real-time Editor: Multi-tabbed interface for HTML, CSS, and JavaScript.

- Sandboxed Preview: Uses an <iframe> to isolated code execution for security and stability.

- Virtual Terminal: Captures console.log and console.warn outputs using a custom postMessage bridge.

- Resizable Workspace: Interactive draggable divider to customize the layout ratio.

- Project Export: Instantly download your project as a standalone .html file.

- Clean UI: Professional dark-themed interface built without external CSS frameworks.

## 🛠️ Technical Implementation

1. The Terminal Bridge

To communicate between the preview window and the main UI, I implemented a messaging system:

- Injection: A script is injected into the preview that overrides the global console object.

- PostMessage: Logs are stringified and sent to the parent window.

- Receiver: The main window listens for these events and renders them in the custom console UI.

2. Live Execution

Instead of simple source updates, the app uses document.write() logic. This ensures that the iframe's global state (variables, listeners) is completely cleared and re-initialized every time the "Run" button is clicked.

3. Layout Management

The resizable sidebar is built using absolute mouse coordinate tracking. By calculating the ratio of the mouse position to the window width, the app dynamically updates Flexbox basis values for a smooth user experience.

## 📦 Getting Started

1. Local Setup

Since the project is built as a portable tool, you only need the single index.html file to run it.

2. Download the index.html file.

Open the file in any modern web browser (Chrome, Firefox, or Edge recommended).

3. Start coding!

## ⌨️ Usage

- Switching Tabs: Click on HTML, CSS, or JS tabs to toggle the active editor.

- Running Code: If "Auto-Run" is enabled in preferences, your code updates 1 second after you stop typing. Otherwise, click the RUN CODE button in the header.

- Viewing Logs: Click the TERMINAL button in the preview bar to see JavaScript execution outputs.

## 📄 License

This project is open-source and free to use for personal or educational purposes.

## 📬 Contact

- 🔗 GitHub: [@PriyanshuGupta1404](https://github.com/priyanshugupta1404)
- 🧑‍💻 LinkedIn: [@PriyanshuGupta1404](https://linkedin.com/in/priyanshugupta0551)
- 📩 Email: priyanshugupta1404@gmail.com
