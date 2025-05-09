
# Visual Workflow Guide
1. Start Here → [Terminal 🖥️] → Install Python & Git  
2. Code Here → [VS Code 🟣] → Write & Debug  
3. Experiment → [Jupyter 📓] → Test Ideas  
4. Manage → [Conda 🐍📦] → Keep Projects Safe  
5. Power Combo → [Jupyter + VS Code 🔥] → Best of Both Worlds

# Python Development Tools – Quick Guide
| Tool               | Logo                                                                                                                                                                                                      | Purpose             | Why Use It?                         | Best For                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------|-------------------------------|
| Windows Terminal   | 🖥️                                                                                                                                                                                                         | Modern command-line | Tabs, fast, supports Python/Git     | Running scripts, Git commands |
| VS Code            | <img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Visual_Studio_Code_1.35_icon.svg" width="30">                                                                                               | Code editor         | Autocomplete, debugging, extensions | Writing & managing projects   |
| Jupyter Notebook   | <img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" width="30">                                                                                                               | Interactive coding  | Step-by-step execution, visuals     | Data science, learning        |
| Conda              | <img src="https://upload.wikimedia.org/wikipedia/commons/e/ea/Conda_logo.svg" width="30">                                                                                                                 | Environment manager | Avoid library conflicts             | Stable projects               |
| Jupyter in VS Code | <img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Visual_Studio_Code_1.35_icon.svg" width="20"> + <img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" width="20"> | Notebooks in IDE    | Debug notebooks + use Git           | Clean data science            |

# When to Use Which?
"I'm just starting" → Jupyter Notebook

"I'm building something big" → VS Code + Terminal

"I need to organize my libraries" → Conda

"I want notebooks but better" → Jupyter in VS Code

# WSL

| Concept              | What It Means                         | Why It Matters for Python               |
|----------------------|---------------------------------------|-----------------------------------------|
| Windows OS (🖥️)       | Microsoft's operating system          | Default environment for many users      |
| Unix/Linux Tools (🐧) | Powerful dev tools (e.g., bash, grep) | Python/Coding workflows rely on them    |
| WSL (🔀)              | Windows Subsystem for Linux           | Lets you run Linux tools inside Windows |

# How to start?

## How to Open Windows Terminal from PowerShell

### Quick Method:
1. Press **`Windows + X`**
2. Select **PowerShell** (or PowerShell Admin)
3. Type:
   ```powershell
   wt


# How to "highlight", "bold", "italic", "underline" in Markdown?

| Action         | How                          |
|----------------|------------------------------|
| Open .ipynb    | Click in Explorer sidebar    |
| Edit text      | Double-click a Markdown cell |
| Make bold      | `**text**`                   |
| Highlight text | `<mark>text</mark>`          |
| Save           | `Ctrl + S`                   |


# Comparing Prompt, Command, and Code:

| Term    | Purpose                               | Example (Tech)                       | Example (Real-World Analogy)    | Where Used                | Key Differences                                            |
|---------|---------------------------------------|--------------------------------------|---------------------------------|---------------------------|------------------------------------------------------------|
| Prompt  | Guides AI/human with natural language | "ChatGPT, explain DNS like I’m 5"    | Asking a teacher a question     | ChatGPT, Copilot, DALL·E  | Flexible, human-language request (no strict rules).        |
| Command | Direct action for a computer          | del file.txt (deletes a file)        | Pressing "Start" on a microwave | Cmd, Terminal, PowerShell | Rigid, immediate action (exact syntax required).           |
| Code    | Program logic for automation/apps     | for i in range(3): print(i) (Python) | Writing a recipe for a chef     | Python, JavaScript, Java  | Reusable program logic (needs interpretation/compilation). |

# File System Structure in Unix-Based Systems
Unix-based systems (Linux, macOS) organize files in a hierarchical tree structure, starting from the root directory (/). All files and subdirectories branch from this single root, unlike Windows, which uses drive letters (e.g., C:\).

![image](https://github.com/user-attachments/assets/d20dbac7-f3ef-47f8-945d-b13349170696)



## Key Features:
- Root Directory (/) – The top-level directory containing all other files and folders.

- Tree-Like Hierarchy – Subdirectories (e.g., /home, /etc) extend from the root.

- No Drive Letters – Unlike Windows, Unix systems mount all storage under /.

- Case-sensitive paths

# Navigating the File System

| Command                       | Description                               | Example      | Notes                            |
|-------------------------------|-------------------------------------------|--------------|----------------------------------|
| cd (change directory)         | Moves between directories                 | cd Documents | Moves to "Documents" directory   |
| .                             | Refers to current directory               | ./script.sh  | Runs script in current directory |
| ..                            | Refers to parent directory                | cd ..        | Moves back one level             |
| ls (list)                     | Shows files/directories in current folder | ls           | Add -l for detailed list         |
| pwd (print working directory) | Displays current directory path           | pwd          | Shows full absolute path         |

## Key Notes:

All paths are case-sensitive in Unix/Linux

```~``` refers to your home directory (e.g., cd ~)

Use tab for auto-completion of file/directory names

# Path Type
| Path Type     | Description                   | Example                | When to Use                          |
|---------------|-------------------------------|------------------------|--------------------------------------|
| Absolute Path | Starts from root (/)          | /home/user/Documents   | When you need a fixed, full location |
| Relative Path | Starts from current directory | ../Downloads or ./file | When targeting nearby files          |


## Key Differences:

Absolute: Always works from any location (begins with /)

Relative: Depends on your current directory (uses . or ..)

# Directory vs. Folder: The Same Thing, Different Terms

| System               | Term Used   | Command                  | What It Creates                      | Visual Representation |
|----------------------|-------------|--------------------------|--------------------------------------|-----------------------|
| Windows (GUI)        | "Folder"    | Right-click → New Folder | A container for files/subfolders     | 📁 New Folder          |
| Linux/WSL (Terminal) | "Directory" | mkdir new_dir            | A container for files/subdirectories | 📂 new_dir/            |

💡 Remember 💡 When you run mkdir new_folder:

- You're creating a new directory (what Windows calls a "folder")

- The command works exactly the same way whether you think of it as a "folder" or "directory"

- The system creates an empty container called "new_folder" in your current location

- GUI (File Explorer) → Calls it a "folder"

- Terminal (WSL/CMD) → Calls it a "directory"

- Functionally identical – just different naming conventions! 


```bash
$ mkdir new_folder  # Creates a directory (you'll see it as a folder in Windows Explorer)
$ ls
new_folder/  # Now exists (can put files inside)
```


# Working with Files and Directories

| Command | Action                      | Example                     | Critical Notes                         |
|---------|-----------------------------|-----------------------------|----------------------------------------|
| mkdir   | Create directory            | mkdir project               | Creates new folder                     |
| touch   | Create file                 | touch notes.txt             | Creates empty file                     |
| rm      | Delete file                 | rm notes.txt                | Permanent deletion (no undo!)          |
| rm -r   | Delete directory + contents | rm -r project               | 🔴 Dangerous! Deletes everything inside |
| rmdir   | Delete empty directory      | rmdir project               | ❌ Fails if directory contains files    |
| cp      | Copy file                   | cp notes.txt notes_copy.txt | Creates duplicate file                 |
| mv      | Move/rename file            | mv notes.txt project/       | Moves or renames in one operation      |

💡 Key Functional Notes:
1.  ```rm -r``` is the nuclear option - always double-check what you're deleting

2.  ```rmdir``` is the safer alternative for empty directories

3.  ```mv``` serves dual purpose:

   -  ```mv``` old.txt new.txt (rename)

   -  ```mv``` file.txt dir/ (move)

4. All commands operate in current directory unless specified otherwise

# Additional Useful Commands
| Command | Description                 | Example Usage                       | Notes                                                                     |
|---------|-----------------------------|-------------------------------------|---------------------------------------------------------------------------|
| history | Shows command history       | history                             | Displays numbered list of recent commands Use !123 to re-run command #123 |
| clear   | Clears terminal screen      | clear                               | Just scrolls output up (history remains accessible)                       |
| wget    | Downloads files from web    | wget http://example.com/file.txt    | Downloads "file.txt" from the web                                         |
| curl    | Advanced data transfer tool | curl -O http://example.com/file.txt | Downloads "file.txt" from the web using cURL                              |

💡|``` ↑```/```↓``` | Browse command history | Press ```↑``` to recall last command | Scroll through past commands |

| Option | Type          | Meaning                     | Example                                    | Output              |
|--------|---------------|-----------------------------|--------------------------------------------|---------------------|
| -o     | Lowercase 'o' | Save with custom filename   | curl -o myfile.txt http://example.com/data | Saves as myfile.txt |
| -O     | Uppercase 'O' | Save with original filename | curl -O http://example.com/data.txt        | Saves as data.txt   |


## Mounting

Mounting = Attaching a filesystem (USB, disk, network share) to a directory ("mount point") to access its files.

### Key Paths

```/mnt``` – Manually mounted filesystems (e.g., sudo mount /dev/sdb1 /mnt/mydrive).

## Mounting Windows Drive (C:) in Linux/WSL

In WSL, access Windows drives at:
```bash
/mnt/c/      # Windows C: drive  
/mnt/d/      # Windows D: drive, etc.
```


# **Summary of the relationship between VS Code, WSL, and Windows:**

VS Code is installed on the Windows system, not inside WSL itself. However, VS Code can connect to and work inside the WSL environment. Essentially, Windows treats WSL like a lightweight Linux virtual machine or server. Through the **Remote - WSL** extension, VS Code connects to this Linux environment, allowing you to edit and run code directly within WSL as if you were working on a remote machine.

Additionally, Windows mounts its local drives (like C:) into WSL, making Windows files accessible inside the WSL environment under the `/mnt` directory (e.g., `/mnt/c`). This setup allows smooth interaction between the Windows file system, WSL, and VS Code.

----------

### **Simplified relationship:**

-   **VS Code** runs on Windows.
    
-   **WSL** runs a Linux environment inside Windows.
    
-   **VS Code + Remote-WSL** connects to WSL, letting you work inside Linux.
    
-   **Windows drives** are mounted inside WSL under `/mnt/*`, allowing file access between the systems.


### **Simple Example**

-   You write Python code in VS Code (Windows).
    
-   When you hit "Run":
    
    -   The  **Windows UI**  shows you the output.
        
    -   The  **WSL Python extension**  runs the code in Linux (`/usr/bin/python3`).
 
  ### Command Palette in VScode: 
  
  Accessible through `Ctrl+Shift+P` (Windows/Linux), the Command Palette allows you to execute commands and access various features with ease.

  ## Extensions
  
  One of the most compelling aspects of VS Code is its extensibility. Extensions are add-ons that enhance the editor's capabilities, tailored to different programming languages, frameworks, and development workflows.

  ## Basic Editing
 the basics of code editing in VS Code:
 - Open a file by clicking File -> Open or using the keyboard shortcut Ctrl+O (Windows/Linux) or Cmd+O (Mac).
 - Save your changes with Ctrl+S (Windows/Linux) or Cmd+S (Mac). You can use essential editing commands such as cut, copy, paste, and undo with familiar shortcuts.
 - You can move any line by pressing Alt
  
# How to go to home folder in "windows terminal":

|   What you want to do  |      Command     |
|:----------------------:|:----------------:|
| Go home                | ```cd ~  ```           |
| List files/folders     |``` ls   ```            |
| Enter your repo folder |``` cd <folder-name> ```|
| Open in VSCode         | ```code .```           |


### Example:
```bash
cd ~
ls
cd Python-Programming
code .
```
##

|      You want to see...     |              Run this command             |
|:---------------------------:|:-----------------------------------------:|
| Conda environments (Python) | `conda env list`  or  `conda info --envs` |
| Files/Folders in Home       | `ls` or `ls -la`                          |



# How to find where your spesific folder for example: "Python-Programming" folder is?


`find ~ -type d -name "Python-Programming"`

This command means:

```find``` → search

```~``` → starting from your home directory

```-type d``` → look for directories (folders)

```-name "Python-Programming"``` → name matching Python-Programming

## Summary


| Action                 | Command                                     |
|------------------------|---------------------------------------------|
| Search for folder      | `find ~ -type d -name "Python-Programming"` |
| Go into folder         | `cd /path/to/Python-Programming`            |
| Open in VSCode         | `code`                                      |
| means "current folder" | `.`                                         |


# Package manager

Python package management helps you easily install, update, and manage the libraries your projects need within isolated environments.
- This is essential in Python because projects often rely on external libraries (called packages) that may have different version requirements. Without isolation, installing packages globally can cause version conflicts across projects.
- A Python environment acts as a separate workspace with its own Python interpreter and packages, keeping projects independent and conflict-free.
### The main benefits of using a package manager like Conda are:

- Dependency management: It automatically installs compatible package versions.

- Environment isolation: You can work on multiple projects without conflicts.

- Reproducibility: Others can easily reproduce your setup by recreating the same environment.

Overall, using Conda (especially through Miniconda) gives Python developers a powerful, flexible way to manage packages and create stable, shareable development environments—particularly useful in data science and scientific computing. At the core are package repositories like PyPI (Python Package Index) and Conda Forge, which are online hubs where developers share packages. To install these packages, we use package managers — the most common are pip (which installs Python packages from PyPI) and conda (which installs both Python and non-Python packages, often as ready-to-use binaries, from Conda channels).



![image](https://github.com/user-attachments/assets/a0dd8633-1454-4833-9f65-e671da8d3066)

#  Environment Creation & Basics

![image](https://github.com/user-attachments/assets/24760f49-ecee-461d-93b5-39a0bfb67c8d)


| **Command**                            | **Description**                                                          |
|----------------------------------------|--------------------------------------------------------------------------|
| `conda create --name my_env python=3.10` | Creates a new environment with a specific Python version.  
|`conda create -n my_env python`          |Creates a new environment with the latest python version. `-n` is = `--name`|
| `conda activate my_env`                 | Activates the specified Conda environment.                               |
| `conda deactivate`                       | Deactivates the current environment and returns to the base environment. |
| `conda env list or conda info --envs`    | Lists all available Conda environments.                                  |
| `conda env remove --name my_env`        | Deletes the specified environment.                                       |

## Note:

If you want to create a new environment with the **latest version of Python** and from the **conda forge** channel:
use this command: 
- `conda create -n myenv python -c conda-forge`
### Breakdown:

- `-n myenv` → names the environment myenv (you can change it).

- `python` → installs the latest Python version available in conda-forge.

- `-c conda-forge` → pulls everything from the conda-forge channel

## Activating and Deactivating Environments

![image](https://github.com/user-attachments/assets/d88d94bb-4bb2-4832-bcdc-080af91457af)


# Installing and Managing Packages
| **Command**                          | **Description**                                                                                                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `conda list`                         | Lists installed packages in the activated environment.                                                                     |
| `conda install PACKAGE_NAME`         | Installs a package (must activate environment first). Example workflow: `conda activate my_env` `conda install numpy`      |
| `conda install PACKAGE_NAME=VERSION` | Installs a specific version (e.g., numpy=1.25). Example:  `conda install numpy=1.25`                                       |
| `pip install PACKAGE_NAME`           | Installs a package using pip (use within activated Conda env). Example: `conda activate my_env` `pip install PACKAGE_NAME` |
| `conda update PACKAGE_NAME`          | Updates a specific package. Example: `conda activate my_env` `conda update numpy`                                          |
| `conda update --all`                 | Updates all packages in the activated environment. Example: `conda activate my_env` `conda update --all`                   |
| `conda remove PACKAGE_NAME`          | Uninstalls a package. Example: `conda activate my_env` `conda remove numpy`                                                |

# Environment Sharing (YAML Files)
Conda allows you to export the environment configuration to a YAML file and recreate the same environment on another system.

| **Command**                                                  | **Description**                                                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `conda activate my_env` `conda env export > environment.yml` | Saves the environment configuration to a YAML file.                                                              |
|`cat environment.yml`                                          |It shows all that is included in that file|
| `conda env create -f environment.yml`                        | Creates a new environment from a YAML file. Replace `environment.yml` with the filename of your environment file |

# Conda environments in Vscode

- To run your code on windows terminal, run the command: ` python main.py`. Change `main.py` with the address of your file. Because I was in the same directory, I just wrote the name of the file.

# Placeholder

Placeholder in Python is like a temporary spot or marker in your code where you plan to put some specific information later. It's a way to say "I'll fill in this part with actual data when I need to."

In other words, Placeholders are part of a broader concept called string formatting. They allow for dynamic string creation and manipulation.

## 
- What does a placeholder look like?
In Python, placeholders are often written with curly braces {} inside a string.

- When do we use placeholders?
We use them when we want to create a string that will have some parts filled in later with specific values.

```bash
name = "Bob"
age = 30
message = f"My name is {name} and I am {age} years old."
print(message)
```

# Objects

An object is like a container that holds data and functions related to that data. Almost everything in Python is an object.
Example:

```bash
my_car = "Toyota"  # my_car is a string object
my_numbers = [1, 2, 3]  # my_numbers is a list object
```

# Arguments
Arguments are pieces of information that you pass into a function when you call it. They're like inputs for the function to work with.
Example:
```bash
def greet(name, time_of_day):
    print(f"Good {time_of_day}, {name}!")

greet("Alice", "morning")  # Outputs: Good morning, Alice!
```
# Parameteres

- Parameters are variables listed in the definition of a function or method.

- They will receive arguments when a new object is created.

- They act as placeholders for the values that will be passed into the function when it's called.

- Parameters have a scope limited to the function they're defined in.

# Attributes

- Attributes are pieces of information attached to an object. They're like characteristics or properties of the object.

- Attributes are variables that belong to an object.

- They store data that is associated with that object.

- Attributes have a lifespan as long as the object exists and can be accessed from various methods within the class.

## Key differences between parameteres and attributes

### 1. Lifespan:

- Parameters exist only during the execution of the method.
- Attributes persist as long as the object exists.


### 2. Scope:

- Parameters are local to the method they're defined in.
- Attributes can be accessed by any method in the class (and sometimes from outside the class).


### 3. Purpose:

- Parameters are used to pass data into methods.
- Attributes are used to store data that belongs to an object.


### 4. Assignment:

- Parameters get their values when a method is called.
- Attributes are typically assigned values within methods (often in ```__init__```), but can be modified later.


### 5. Syntax:

- Parameters are listed in method definitions: ```def method(parameter1, parameter2)```:
- Attributes are usually prefixed with ```self.``` inside class methods: ```self.attribute = value```


```bash
class Car:
    def __init__(self, make, model, year):
        self.make = make    # attribute
        self.model = model  # attribute
        self.year = year    # attribute
        self.mileage = 0    # attribute (not from a parameter)
        self.running = False  # attribute (not from a parameter)

    def start_engine(self):
        self.running = True
        print(f"The {self.year} {self.make} {self.model}'s engine is now running.")

    def drive(self, distance):
        if self.running:
            self.mileage += distance
            print(f"Drove {distance} miles. Total mileage is now {self.mileage}.")
        else:
            print("You need to start the engine first!")

The ```__init__``` method:

- This is a special method in Python classes, called a constructor.
- It initializes a new object of the class.
- The ```self``` parameter refers to the instance being created.

# Creating an instance (object) of the Car class
my_car = Car("Toyota", "Corolla", 2020)

# Using the object
my_car.start_engine()
my_car.drive(50)
```

Let's break this down:

### 1. Object:

An object is an instance of a class. In this example, ```my_car``` is an object of the ```Car``` class.
Objects have their own set of attributes and can perform actions defined by their methods.


### 2. Parameters:

Parameters are variables in a method definition that act as placeholders for values passed when the method is called.
In ```__init__(self, make, model, year)```, ```make```, ```model```, and ```year``` are parameters.
In ```drive(self, distance)```, distance is a parameter.


### 3. Attributes:

Attributes are variables that belong to an object and store its state.
In this example, ```self.make```, ```self.model```, ```self.year```, ```self.mileage```, and ```self.running``` are all attributes.
Note that ```mileage``` and ```running``` are attributes that weren't created from parameters.


### 4. Instance:

An instance is a specific realization of a class. It's synonymous with "object" in this context.
```my_car``` is an instance of the ```Car``` class.


### 5. Arguments:

- Arguments are the actual values passed to a method when it's called.
- In ```Car("Toyota", "Corolla", 2020)```, "Toyota", "Corolla", and 2020 are arguments.
- In ```my_car.drive(50)```, 50 is an argument.



Now, to address your question about why we don't define all attributes as parameters:

1. Default or Calculated Values:

Some attributes might have default values or be calculated based on other attributes. For example, ```mileage``` starts at 0 for all new cars.


2. Internal State:

Attributes like ```running``` represent the internal state of the object that doesn't need to be set during initialization.


3. Flexibility:

Not all attributes need to be set when an object is created. Some might be set or changed later.


4. Simplicity:

Having too many parameters can make object creation cumbersome. It's often better to have a few essential parameters and set other attributes as needed.


5. Encapsulation:

Some attributes might be intended for internal use only, and not exposing them as parameters helps maintain encapsulation.



In our ```Car``` class, ```make```, ```model```, and year are essential for creating a car, so they're parameters. But ```mileage``` (which starts at 0) and running (which starts as False) don't need to be set during initialization, so they're not parameters.

