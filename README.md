# **Step-by-Step Guide to Setting Up a Virtual Environment for Jupyter Lab**

#### **1. Create a Virtual Environment**
Run the following command in your project directory to create a virtual environment named `venv`:
```powershell
python -m venv venv
```

#### **2. Allow Script Execution (For PowerShell Users)**
Since Windows may block script execution, temporarily allow it for the current session:
```powershell
Set-ExecutionPolicy Unrestricted -Scope Process
```

#### **3. Activate the Virtual Environment**
Activate The Enviroment :
  ```powershell
  .\venv\Scripts\Activate
  ```


#### **4. Verify `pip` Installation**
Check if `pip` is installed and working:
```powershell
pip --version
```

#### **5. Upgrade `pip` (Recommended)**
Ensure you have the latest version of `pip`:
```powershell
python -m pip install --upgrade pip
```

#### **6. Install JupyterLab**
Inside the activated virtual environment, install JupyterLab:
```powershell
pip install jupyterlab
```

#### **7. Launch JupyterLab**
Start JupyterLab:
```powershell
jupyter lab
```

#### **8. Using the Virtual Environment in VS Code**
- Open VS Code and install the **Python extension** (if not already installed).
- Select your virtual environment as the interpreter (`venv`).
- Run Jupyter notebooks within VS Code.

#### **9. Installing Additional Modules**
Whenever you need a new package, install it inside the virtual environment:
```powershell
pip install module_name
```