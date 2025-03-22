# Bash Scripting Tasks Repository

Welcome to the **Bash Scripting Tasks Repository**! 🎉 This repository contains a collection of organized Bash script tasks that aim to simplify automation, solve practical challenges, and demonstrate scripting techniques.

## Repository Structure
The tasks are organized into subdirectories. Each directory contains:
- **Script File**: The actual Bash script for the task.
- **Task README**: A description of the task, usage, and expected output.

### Task Index:
- **Task 01**: [Intro to Bash Script](1/README.md)
    - **1.1**: [Find insecure files](1/1.1)
    - **1.2**: [Odd or Even? Try!](1/1.2)
    - **1.3**: [Fishy IPs, Founded!](1/1.3)

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/username/bash-scripts-repo.git
   cd bash-scripts-repo
    ```

2. Navigate to deseired task directory.
3. Run the script according to it's instructions



## Controller

```markdown
# Bash Script Controller

The `controller` is a Bash script designed to dynamically execute task files based on your input. It simplifies running specific tasks located in organized directories, making it easier to manage and reuse scripts.

---

## Features
- Dynamically locate and execute Bash script tasks based on task identifiers (e.g., `1.1`).
- Supports passing additional parameters to the target script.
- Validates input and provides clear error messages.

---

## Repository Structure
Here’s an example directory structure for the repository:
.
├── controller          # The main controller script
├── README.md           # This README file
├── 1/
│   ├── 1.sh            # Script for Task 1.1
│   ├── 2.sh            # Script for Task 1.2
├── 2/
│   ├── 3.sh            # Script for Task 2.3
```

---

## How to Use
1. **Make the script executable**:
   ```bash
   chmod +x controller
   ```

2. **Run a Task**:
   - To execute `1.1` (located in `./1/1`), run:
     ```bash
     ./controller run 1.1
     ```

   - To execute `2.3` (located in `./2/3`), run:
     ```bash
     ./controller run 2.3
     ```

3. **Pass Parameters**:
   If the task script requires parameters, pass them after the task identifier:
   ```bash
   ./controller run 1.1 --help
   ./controller run 2.3 arg1 arg2
   ```

---

## Errors and Warnings
- **Invalid Task Identifier**:
  If the task script does not exist, you’ll see an error message like:
  ```
  Error: Task script './1/1.sh' not found or not executable
  ```

- **Invalid Command**:
  If you use an unsupported command:
  ```
  Error: Unsupported command 'invalid'
  ```

- **Missing Arguments**:
  If no task identifier is provided:
  ```
  Usage: ./controller run <task> [parameters]
  ```

---

## Contribution
Feel free to contribute by improving the controller script or adding more task examples. Open a pull request or create an issue to get involved!
