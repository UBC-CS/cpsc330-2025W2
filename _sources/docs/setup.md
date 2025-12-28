# Setting up your coding environment

This guide will help you get ready to run lecture notebooks and complete homework assignments on your own computer.  

You'll need three main tools:  
1. **Git:** to download and update course materials from GitHub  
2. **Python & Conda:** to run code and manage packages  
3. **JupyterLab:** or **VS Code** as your main coding environment

## Quick start (TL;DR)

If you already know what you're doing, here are the essential commands:

```bash
# Clone the repo
git clone https://github.com/UBC-CS/cpsc330-2025W1.git
cd cpsc330-2025W1

# Add conda-forge channel (Miniconda only)
conda config --add channels conda-forge

# Create environment
conda env create -f cpsc330env.yml

# (Optional) Test activating/deactivating the environment
conda activate cpsc330
conda deactivate

# Start JupyterLab from base
jupyter lab

# Or start VS Code from base
code .
```

> ⚠️ Normally, you will launch JupyterLab or VS Code from `(base)` and then select the `cpsc330` environment inside those tools. Activating it in the terminal is only needed for testing or if you want to install additional packages in the environment later on.


## Step 1: Install Git

We use Git to manage and download course material from GitHub. Follow the [Git setup instructions](https://ubc-cs.github.io/cpsc330-2025W1/docs/git_installation.html).

Once installed:

```bash
git clone https://github.com/UBC-CS/cpsc330-2025W1.git
cd cpsc330-2025W1
```

To update later:
```bash
git pull
```

> ⚠️ Tip: Don't keep personal notes inside this repository. Otherwise, `git pull` may fail due to conflicts. Keep notes in a separate folder/repo.



## Step 2: Install Python and Conda

We use Python 3.12 (Python 2 is not supported). To manage Python and packages, you'll install a Conda distribution. You have two options:

### Option A (recommended): Miniforge

- Lightweight installer that defaults to the conda-forge channel (up-to-date, consistent across platforms).
- Works smoothly on Windows, Linux, and macOS (including Apple Silicon).

[Download Miniforge here](https://conda-forge.org/download/). Choose the installer for your operating system.

### Option B: Miniconda

- The official distribution from Anaconda.
- Defaults to the defaults channel (stable, but sometimes outdated).
- Requires one extra step: adding the conda-forge channel.

[Download Miniconda here](https://www.anaconda.com/docs/getting-started/miniconda/main). Choose the installer for your operating system.



## Step 3: Verify installation

After installation:

- **macOS:** open Terminal (⌘ + Space → type “Terminal”).  
- **Windows:** open **Anaconda Prompt (miniforge3 or miniconda3)** from the Start Menu.  
- **Linux:** open your system's terminal (Ctrl+Alt+T).  

You should see `(base)` at the start of your command line prompt: 

```
(base) yourusername@computer:~$
```

Check installation:

```bash
conda --version
python --version
```

Expected:

> conda: recent version (e.g., 24.x.x)  
> python: 3.12 or greater  

If you see Python 2.7, reinstall with Python 3.12.


## Step 4: Configure conda-forge (Miniconda only)

If you installed Miniconda, add the conda-forge channel:

```bash
conda config --add channels conda-forge
```

If you installed Miniforge, you can skip this step (it’s already the default).


## Step 5: Create the course environment

A virtual environment keeps course packages isolated from other projects.

1. Navigate to the course repo if you are not already there. Make sure `cpsc330env.yml` exists in the repo you cloned:
```bash
cd cpsc330-2025W1
ls 
```

2. Create the environment.
```bash
conda env create -f cpsc330env.yml
```

3. (Optional) Test activating and deactivating the environment.
```bash
conda activate cpsc330
conda deactivate
```

Your prompt should return to `(base)` when deactivated.

> ✅ You only need to create the environment once. Normally, you will stay in `(base)` and select the `cpsc330` kernel in JupyterLab or VS Code.

4. Launch JupyterLab (from base environment):
```bash
jupyter lab
```

JupyterLab will open in your browser. At the top-right corner of your notebook, click on the kernel dropdown. Select the kernel named `Python [conda env:cpsc330]`. Now you're running the notebook inside the course environment.

---

## Step 6: Using VS Code (alternative to JupyterLab)

Some of you may prefer using [VS Code](https://code.visualstudio.com/) instead of JupyterLab. Both work fine. It's your choice.

### Install VS Code

- [Download from Visual Studio Code](https://code.visualstudio.com/).  
- Install the **Python** extension and the **Jupyter** extension (search in the Extensions Marketplace inside VS Code).  

### Open the repo in VS Code

- Open VS Code → File → Open Folder → select the cloned `cpsc330-2025W1` folder.  
- Or in the terminal navigate to `cpsc330-2025W1` and open VS Code:  
```bash
code . 
```

### Select the correct environment

1. Open the Command Palette (⇧⌘P on macOS, Ctrl+Shift+P on Windows/Linux).  
2. Type **Python: Select Interpreter**.  
3. Choose the interpreter starting with `conda env:cpsc330`.  

⚠️ If you don't see the interpreter, restart VS Code after creating the environment.

### Running notebooks

- Open any `.ipynb` file from the repo.  
- At the top right, select the `cpsc330` kernel if it isn’t already selected.  
- Run cells with **Shift+Enter**.  


## Step 7: Troubleshooting

### Errors when creating course environment 
If `conda env create -f cpsc330env.yml` fails:

- Check the error message and identify the problematic package.  
- Remove that package line from `cpsc330env.yml`.  
- Re-run the command.  
- If needed, install missing packages manually:  

```bash
conda install packagename
# or
pip install packagename
```

Still stuck? Bring your laptop to office hours or tutorials and get help.


## (Optional) Learn JupyterLab and Python

If you're new to JupyterLab and/or Python, here is a short video of an introduction to JupyterLab and Python created by one of the instructors of the course for another course that uses similar tooling.

<div class="container youtube">
<iframe src="https://player.vimeo.com/video/1006820659?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Introduction to JupyterLab and Python"></iframe>
<script src="https://player.vimeo.com/api/player.js"></script>
</div>

## Credit

These installation instructions are based on [the MDS software installation instructions](https://ubc-mds.github.io/resources_pages/installation_instructions/).
