# 🚀 

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
git clone https://github.com/DSathvik2000/git_assignment_HeroVired.git
cd git_assignment_HeroVired
```

---

## 📂 CalculatorPlus - Arithmetic Operations

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

5. **Check the status of the branch whether git is tracking the modified changes, if not make them `tracked`:
   ```sh
   git status   # to check the files are being tracked by git before pushing
   git add .    # command to make git track the changes for the file
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
   --![image](https://github.com/user-attachments/assets/58ea9d16-1d70-4b3d-a2ad-e68f4faef784)

8. **Create a new feature branch for square root (`feature/sqrt`) and checkout to the branch**:
   ```sh
   git branch feature/sqrt
   git checkout feature/sqrt
   ```
9. Add the `sqrt` code in the calculator.py file.

10. Bug Fix (Divide Function): A bug has been reported in `main` branch in which the application should handle `division` by zero, so checkout to `dev` branch while keeping the changes in `feature/sqrt`, to achieve this follow these steps.
   ```sh
   git stash     # to save changes temporarily and checking out to different branches
   git checkout dev     # checkout dev branch and fix the bug that causing issue     
   ```

11. After fixing the bug in `dev` branch test it throughly and if the bug is fixed, push the changes to `dev` branch 
  ```sh
    python calculator.py   # run the application and make sure the bug is fixed
    git add .
    git commit -m "Bug has been fixed"
    git push origin dev
  ```

12. Making sure the bug is fixed now, create a pull request to merge these changes into `main` branch to keep in sync with the updated code. 
 ![image](https://github.com/user-attachments/assets/aebc0c95-5a99-47fa-b6d6-4b68dda568d7)

13. Now chekout to `featur/sqrt` branch and bring back the stashed changes to achieve this follow these steps
   ```sh
    git stash list   # to see the stashed changes list
    git stash apply  # to bring back the latest/recent most stashed changes
    git stash apply stash@{stash number}  # to bring back the particular stashed change  
   ```

14. Merge these changes into `dev` branch.
![image](https://github.com/user-attachments/assets/2320b3d8-d0f2-404d-bf79-3502fb9a5bee)

15. After successful testing done in `dev` branch merge them in `main` branch and create a version of `v2.0`.
   ```sh
   git tag v2.0
   git push origin main --tags
  ```
![image](https://github.com/user-attachments/assets/00e8ab10-2f98-4b9e-a89a-594d6201b4bd)

---

## 💾 Git LFS for Large Files Storage  

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
   git clone https://github.com/DSathvik2000/git_assignment_HeroVired.git
   ```
   ![WhatsApp Image 2025-02-27 at 20 45 48_4fdfc2dc](https://github.com/user-attachments/assets/b93d6e94-b0f7-4dcf-acf2-ab6880d5f4b7)


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

