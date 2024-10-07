`htop` is an interactive process viewer for Unix systems, similar to `top` but with more features and an easier-to-use interface. It provides a real-time, dynamic overview of system resource usage (CPU, memory, swap, etc.) and running processes.

Here’s a guide to using `htop` on Linux (including Fedora).

### Installation on Fedora
To install `htop`, use the following command:
```bash
sudo dnf install htop
```

### Launching `htop`
Simply type:
```bash
htop
```

### Key Features of `htop`
- **Graphical CPU and Memory Usage:** `htop` provides a visual representation of CPU, memory, and swap usage via color-coded bar graphs.
- **Process List:** Displays all running processes with additional information like process ID (PID), user, CPU/memory usage, and uptime.
- **Interactive Interface:** You can scroll vertically to view all processes and horizontally to view more detailed columns. You can also kill or renice processes directly from the interface.

### `htop` Interface Breakdown

1. **Header (Top Section):**
   - **CPU usage bars:** Each core's usage is represented in a separate bar, color-coded to indicate different types of load (user, system, IO wait, etc.).
   - **Memory usage bars:** Displays RAM usage in a color-coded bar.
   - **Swap usage:** Shows swap space usage.

2. **Main Section (Process List):**
   - Lists all running processes, updated in real-time.
   - Columns include:
     - **PID:** Process ID.
     - **User:** The owner of the process.
     - **CPU%:** Percentage of CPU used by the process.
     - **MEM%:** Percentage of memory used by the process.
     - **Command:** The command that started the process.

3. **Footer (Control Section):**
   - Provides key shortcuts to perform actions like killing or filtering processes.

### Key Shortcuts and Commands

| Key    | Functionality                      |
|--------|------------------------------------|
| `F1`   | Help menu (displays keyboard shortcuts) |
| `F2`   | Setup menu (customize columns, colors, etc.) |
| `F3`   | Search for a process by name |
| `F4`   | Filter processes (e.g., show only processes with a specific name) |
| `F5`   | Tree view (displays processes in a hierarchical tree format) |
| `F6`   | Sort by column (choose which column to sort by) |
| `F7`   | Decrease priority (renice a process) |
| `F8`   | Increase priority |
| `F9`   | Kill a process (choose signal to send) |
| `F10`  | Quit `htop` |

### Useful Features

1. **Scrolling:**
   - Scroll vertically with the arrow keys to navigate through the process list.
   - Scroll horizontally to view additional columns like uptime or swap usage.

2. **Tree View