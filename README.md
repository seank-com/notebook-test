# notebook-test
A test project for exploring Jupyter Notebooks in VS Code

This repository demonstrates how to set up and use Jupyter Notebooks in Visual Studio Code with Python. It includes examples and setup instructions for both new users and those cloning this repository.

## Quick Start (For Repository Cloners)

If you've cloned this repository and want to get started quickly:

### Prerequisites
- Python 3.7+ installed on your system [download here](https://www.python.org/downloads/)

### Setup Steps
1. **Clone and navigate to the repository:**
   ```cmd
   git clone https://github.com/seank-com/notebook-test.git
   cd notebook-test
   ```

2. **Create and activate a virtual environment:**
   ```cmd
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. **Install required packages:**
   ```cmd
   pip install -r requirements.txt
   ```

4. **Install VS Code Jupyter extension:**
   - Open VS Code in this folder
   - Press `Ctrl+Shift+X` to open Extensions
   - Search for "Jupyter" by Microsoft and install it
   - The following extensions should be installed automatically:
     - Jupyter Notebook Renderers
     - Jupyter Slide Show  
     - Jupyter Keymap
   - Optionally install "Jupyter PowerToys" for enhanced debugging features

5. **Open and run the example notebook:**
   - Open `hello-world.ipynb`
   - Select your virtual environment Python interpreter as the kernel
   - Run the cells to verify everything works

## Complete Setup From Scratch

For those setting up a Jupyter notebook environment from the beginning:

### 1. Install Python

1. Download Python from [python.org](https://www.python.org/downloads/)
2. **Recommended installation options:**
   - ✅ Install Python for all users
   - ✅ Create shortcuts for installed applications  
   - ✅ Add Python to environment variables
   - ✅ Precompile standard library
   - ✅ **Disable path length limit** (helps avoid Windows path issues)
   - ❌ Skip: Tcl/Tk and IDLE (not needed for VS Code)
   - ❌ Skip: Test suite (for Python core development only)
   - ❌ Skip: Documentation (web docs are more current)
   - ❌ Skip: Debugging symbols (for Python interpreter debugging only)
   - 🔄 Optional: py launcher (helpful for managing multiple Python versions)

### 2. Create Your Project

1. **Create project directory:**
   ```cmd
   mkdir my-notebook-project
   cd my-notebook-project
   ```

2. **Initialize Git (optional but recommended):**
   ```cmd
   git init
   ```

3. **Create virtual environment:**
   ```cmd
   python -m venv .venv
   ```

4. **Activate virtual environment:**
   ```cmd
   .venv\Scripts\activate
   ```

### 3. Install Jupyter and Dependencies

```cmd
pip install jupyter
pip install numpy pandas matplotlib seaborn
```

### 4. Setup VS Code

1. **Install VS Code Extensions:**
   - Open VS Code in your project folder
   - Install "Jupyter" extension by Microsoft
   - Consider installing "Jupyter PowerToys" for enhanced features

2. **Create your first notebook:**
   - Create a new file with `.ipynb` extension
   - VS Code will prompt you to select a kernel - choose your virtual environment's Python interpreter

### 5. Test Your Setup

Create a test cell with this code:
```python
# Test cell - basic Python
print("Hello from Jupyter!")
import sys
print(f"Python version: {sys.version}")
print(f"Jupyter is working! 🎉")

# Test common packages
import json
import datetime
print(f"Current time: {datetime.datetime.now()}")
```

## Project Structure

```
notebook-test/
├── .venv/                 # Virtual environment (not tracked in git)
├── .git/                  # Git repository files
├── .gitignore            # Git ignore rules
├── LICENSE               # MIT License
├── requirements.txt      # Python dependencies
├── hello-world.ipynb      # Example notebook
└── README.md             # This file
```

## Tips and Best Practices

### Virtual Environments
- Always use virtual environments for Python projects to avoid dependency conflicts
- Activate your virtual environment before working: `.venv\Scripts\activate`
- Your prompt should show `(.venv)` when the environment is active

### VS Code Jupyter Features
- **Cell execution**: `Shift+Enter` to run current cell and move to next
- **Kernel selection**: Click the kernel name in the top-right to change Python interpreters  
- **Variable explorer**: Available with Jupyter PowerToys extension
- **Rich output**: Plots, tables, and widgets render inline
- **Git integration**: Notebooks work with version control (though outputs can create large diffs)

### Troubleshooting

**Kernel not found:**
- Ensure your virtual environment is activated
- Refresh the kernel list in VS Code
- Restart VS Code if needed

**Import errors:**
- Verify you're in the correct virtual environment
- Install missing packages with `pip install package-name`

**Path length issues on Windows:**
- Enable "Disable path length limit" during Python installation
- Or run: `git config --system core.longpaths true`

## Next Steps

Now that you have Jupyter notebooks working:
- Explore data science libraries like pandas, numpy, matplotlib
- Try creating visualizations and data analysis notebooks
- Consider setting up Node.js notebooks with IJavascript kernel for JavaScript exploration
- Experiment with notebook extensions and widgets

## Contributing

Feel free to add example notebooks, improve setup instructions, or share tips and tricks!
