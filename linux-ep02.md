# Linux Terminal Series - Episode 2: Essential File Handling & Monitoring

Welcome to **Episode 2** of the *Linux Terminal Series*!

In this video, you'll learn 6 essential Linux commands for creating, editing, viewing, and monitoring files like a pro. Whether you are managing servers, working in DevOps, or starting out with Linux, mastering file handling in the command line is a critical skill.

## 📌 Commands Covered

| Command | Description | Example Usage | Key Shortcuts / Flags |
| :--- | :--- | :--- | :--- |
| `touch` | **Create File** – Create a new empty file instantly. | `touch notes.txt` | — |
| `nano` | **Text Editor** – Open a simple, user-friendly CLI text editor. | `nano notes.txt` | `Ctrl+O` (Save)<br>`Ctrl+X` (Exit) |
| `cat` | **Concatenate & Print** – Display short file contents directly in the terminal. | `cat notes.txt` | — |
| `less` | **Paginated Viewer** – Interactively view large files page-by-page. | `less server.log` | `/` (Search)<br>`q` (Quit) |
| `head` | **View Beginning** – View the first few lines of a file. | `head -n 5 server.log` | `-n [number]` (Line count) |
| `tail` | **View End & Stream** – View the last lines or stream live log updates in real-time. | `tail -f server.log` | `-f` (Follow/Live stream)<br>`Ctrl+C` (Stop) |

## 🚀 Practical Use Cases

* **DevOps & SysAdmin:** Use `tail -f` to monitor application or server logs live during troubleshooting.
* **Quick Configuration:** Use `nano` or `touch` to set up environment variables or configuration files on remote servers.
* **Log Inspection:** Use `less` and `head` to quickly inspect log outputs without crashing terminal buffers.

## 📚 Series Navigation

* **Episode 1:** File Navigation Basics (`pwd`, `ls`, `cd`, `mkdir`, `clear`)
* **Episode 2:** File Handling & Monitoring *(Current)*
* **Episode 3:** File Permissions & Ownership (`chmod` & `chown`) – *Coming Soon!*

---
*Feel free to star ⭐ this repository if you found it helpful!*