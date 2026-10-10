# Assignment 01: Git, Gitea, GitHub, Git LFS, and GitHub Pages

**Student Name:**Maryum Nasim  
**Registration No:** FA24B1-SE-082  
**Course:** Cloud Computing / Software Engineering  
**Submission Repository:** CC  
**Path:** `Assignments/Assignment01/Assignment01.md`

---

## 1. Objectives
- Install, configure, and run a local Gitea instance using Docker Compose on Ubuntu Server.
- Manage Git repositories with dual remotes (`gitea` and `github`).
- Configure Git LFS to track and push large binary files (>100 MiB).
- Build and publish a personal portfolio website using GitHub Pages.

---

## 2. Summary of Tasks & Commands Executed

### Task 1: Gitea Setup & First Push
- **Environment:** Ubuntu Server (`fatimajaleel@ubuntu`)
- **Key Commands:**
  ```bash
  sudo apt update && sudo apt install -y docker.io curl
  docker compose up -d
  curl -sS -o /dev/null -w "Gitea HTTP status: %{http_code}\n" [http://127.0.0.1:3000/](http://127.0.0.1:3000/)
  git remote add gitea [http://fatimajaleel@127.0.0.1:3000/fatimajaleel/Assignment01.git](http://fatimajaleel@127.0.0.1:3000/fatimajaleel/Assignment01.git)
  git push -u gitea main
  Task 2: GitHub Dual Remote Configuration
Key Commands:

Task 2: GitHub Dual Remote Configuration
git remote add github [https://github.com/fatimajaleel/Assignment01.git](https://github.com/fatimajaleel/Assignment01.git)
git remote -v
git push -u github main
Task 3: Git LFS File Tracking
Key Commands:

Task 3: Git LFS File Tracking
git lfs install
git lfs track "*.bin"
git lfs ls-files --size
git push github main
Task 4: GitHub Pages Portfolio
Repository: fatimajaleel.github.io

Live Site URL: https://fatimajaleel.github.io/

3. Evidence Screenshots Index
task1_gitea_running.png - Docker compose ps status and HTTP 200 verification for Gitea.

task1_gitea_push.png - Terminal log of initial commit pushed to Gitea remote.

task1_gitea_repository.png - Browser view of public Gitea repository with rendered README.md.

task2_remotes.png - Terminal output of git remote -v confirming both gitea and github remotes.

task2_github_push.png - Terminal log of successful push to GitHub main branch.

task2_github_repository.png - Browser view of public GitHub repository.

task3_lfs_setup.png - Terminal output showing git lfs install and .gitattributes rule creation.

task3_lfs_files.png - Output of git lfs ls-files --size showing three 100+ MiB .bin files tracked.

task3_lfs_push.png - Terminal output confirming 100% (3/3) LFS object upload to GitHub.

task4_pages_repository.png - Browser view of fatimajaleel.github.io with index.html and styles.css.

task4_pages_deployment.png - GitHub Pages settings page showing live deployment banner.

task4_portfolio_live.png - Rendered portfolio page at https://fatimajaleel.github.io/.

4. Final Submission Checklist
[x] Completed assignment individually.

[x] Assignment01.md created inside CC/Assignments/Assignment01/.

[x] Assignment01_Solution.docx and .pdf saved in CC/Assignments/Assignment01/.

[x] All 12 .png screenshots present in CC/Assignments/Assignment01/screenshots/.

[x] Repositories (CC, Assignment01, fatimajaleel.github.io) set to Public on GitHub.


3. **Paste into GitHub and save:**
   * Click inside the empty text box on GitHub and press **Ctrl + V** to paste everything.
   * Click the green **Commit changes...** button at the top right.
   * Click **Commit changes** again in the popup to complete saving.
