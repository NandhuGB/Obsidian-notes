To list running processes and kill processes on Fedora, you can use a combination of commands and tools like `ps`, `top`, `htop`, and `kill`. Here's a guide on how to do this:

### 1. **Using `ps` to List Processes**

The `ps` command is a simple way to list processes on your system. It shows information about the running processes such as the process ID (PID), user, and command.

- **Basic usage:**
  ```bash
  ps aux
  ```

  - `a`: Shows processes from all users.
  - `u`: Shows user information.
  - `x`: Includes processes not associated with a terminal (daemon processes).

This command will output a list of running processes with columns like:
- **USER**: The user who started the process.
- **PID**: The process ID.
- **%CPU**: CPU usage.
- **%MEM**: Memory usage.
- **COMMAND**: The command that started the process.

### 2. **Using `top` to List and Monitor Processes**

`top` is an interactive command to display real-time system activity.

- To start `top`, simply type:
  ```bash
  top
  ```

This will display a dynamic list of running processes sorted by CPU usage by default. You can press:
- **`k`**: To kill a process. After pressing `k`, enter the **PID** of the process you want to kill and then press **Enter**.
- **`q`**: To quit `top`.

### 3. **Using `htop` for a More User-Friendly Interface**

`htop` is similar to `top` but provides a more visual and interactive interface. You can scroll through the list of processes, sort them, and easily kill processes.

- Install `htop` on Fedora:
  ```bash
  sudo dnf install htop
  ```

- To start `htop`, simply type:
  ```bash
  htop
  ```

In `htop`:
- **Use arrow keys** to scroll through the process list.
- **F9** to kill a process. Select the process you want to kill, then press `F9`, and choose the signal (usually **SIGKILL** or **9**).

### 4. **Killing a Process with `kill`**

To kill a process, you need its **PID**. You can get the PID from the output of `ps`, `top`, or `htop`. Once you have the PID, use the `kill` command to terminate it.

- **Basic kill command:**
  ```bash
  kill <PID>
  ```

- **Forcefully kill a process:**
  If the process does not respond to a regular kill, use the **`-9`** option (SIGKILL) to forcefully terminate it:
  ```bash
  kill -9 <PID>
  ```

### 5. **Killing All Processes by Name**

To kill all processes with a specific name, use `pkill`.

- Example to kill all instances of `firefox`:
  ```bash
  pkill firefox
  ```

Or, to kill by PID using `killall`:
```bash
sudo killall <process_name>
```

### Summary of Commands

- **List processes:** `ps aux` or use `top`/`htop` for a dynamic display.
- **Kill a process:** `kill <PID>` or use `htop`/`top` interactive kill options.
- **Forcefully kill a process:** `kill -9 <PID>`.
- **Kill processes by name:** `pkill <name>`.

This should give you the tools needed to manage running processes and kill unwanted ones in Fedora!