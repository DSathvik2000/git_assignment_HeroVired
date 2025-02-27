# 🚀 DevOps Important Scripts

🛠️ **This repository contains scripts and workflows for managing Git branches, implementing new features, handling bug fixes, and using Git LFS efficiently.**

---

## 📌 Table of Contents
- [📂 CalculatorPlus - Arithmetic Operations](#calculatorplus-arithmetic-operations)
- [🔢 Geometry Calculator](#geometry-calculator)
- [💾 Git LFS for Large Files](#git-lfs-for-large-files)
- [🔧 Setup and Requirements](#setup-and-requirements)
- [💻 Usage Instructions](#usage-instructions)
- [🤝 Contributing](#contributing)
- [📜 License](#license)

---

## 🔧 Setup and Requirements

### 1️⃣ Install Python 3

If Python is not installed, install it using:
```sh
sudo apt update && sudo apt install python3 -y   # For Linux
brew install python3                             # For macOS
winget install Python.Python.3                   # For Windows
```

### 2️⃣ Clone the Repository
Run the below command to clone the repository:
```sh
git clone https://github.com/yourusername/git_assignment_HeroVired.git
cd git_assignment_HeroVired
```

---

## 📂 CalculatorPlus - Arithmetic Operations

### 🔹 Steps to Implement Square Root Feature:
1. **Create a repository**: `git_assignment_HeroVired`
2. **Create a development branch**: `dev`
   ```sh
   git branch dev    # to create a branch
   ```
3. **Checkout to the development branch**: `dev`
   ```sh
   git checkout dev    # to checkout to dev branch
   ```
4. **Create a file named Calculator.py and add simple calculator code in it 
5. **Check the status of the branch whether the modified changes are being tracked by git, if not make them `tracked`:
   ```sh
   git status   # to check the files are being trakced by git before pusing
   git add .    # command to make git tracks the changes for the file
   ```
6. **Now `commit` the changes and push the changes:
   ```sh
   git commit -m "Commit message"   # command to commit the changes
   git push origin dev  # to push changes to dev branch
   ```
7. ** Merge the changes to `main` branch and make a release version out of it 
   ```sh
   git checkout main  
   git merge dev     
   git tag v1.0
   git push origin main --tags
   ```
4. **Create a new feature branch for square root (`feature/sqrt`) and checkout to the branch**:
   ```sh
   git branch feature/sqrt
   git checkout feature/sqrt
   ```
6. Add the `sqrt` code in the calculator.py file.
5. **Bug Fix (Divide Function)**: Ensure `divide` handles division by zero.
6. **Merge `feature/sqrt` into `dev`, test, then merge to `main` and release `v2.0`**.

---

## 🔢 Geometry Calculator

### 🔹 Steps to Implement Circle & Rectangle Area Calculation:
1. **Create a new branch** `geometry-calculator`
2. **Stash unfinished work using `git stash`** while switching branches
3. **Create separate feature branches** for circle (`feature/circle-area`) and rectangle (`feature/rectangle-area`)
4. **Retrieve stashed changes, complete, and commit each feature**
5. **Merge both features into `dev`, test, and merge to `main`**


---

## 💾 Git LFS for Large Files

### 🔹 Steps to Implement Git LFS:
1. **Install Git LFS**:
   ```sh
   git lfs install
   ```
2. **Track large files (e.g., files over 200MB)**:
   ```sh
   git lfs track "*.bin"
   ```
3. **Create an `lfs` branch**:
   ```sh
   git checkout -b lfs
   ```
4. **Add and commit large files**:
   ```sh
   git add largefile.bin
   git commit -m "Added large binary file with Git LFS"
   git push origin lfs
   ```
5. **Clone and verify on another machine**:
   ```sh
   git clone https://github.com/yourusername/git_assignment_HeroVired.git
   ```

---

## 💻 Usage Instructions

- Open a terminal or command prompt.
- Navigate to the repository directory:
  ```sh
  cd /path/to/repo-directory
  ```
- Run the desired Python script.

---

## 🤝 Contributing
🙌 Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```sh
   git branch new-branch
   ```
3. Commit your changes:
   ```sh
   git commit -m "Commit Message"
   ```
4. Push the code:
   ```sh
   git push origin new-branch
   ```
5. Submit a pull request.

---

## 📜 License
📄 This repository is licensed under the MIT License. See the LICENSE file for details.

