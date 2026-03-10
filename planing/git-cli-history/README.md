# ️ Git CLI History — PSE Group 02
<details>
<summary><strong>Initial Setup</strong></summary>
```powershell
git config --global credential.helper manager
git config --global user.name "stegdream"
git config --global user.email "stegdream@users.noreply.github.com"
git clone https://github.com/stegodream/PSE-GROUP-2.git
```
</details>

<details>
<summary><strong>First Commit — Folder Structure</strong></summary>
```powershell
git add .
git commit -m "Add initial project folder structure"
git push
```
</details>

<details>
<summary><strongREADME Updates</strong></summary>
```powershell
git add README.md
git commit -m "updated README.md"
git push
```
</details>

<details>
<summary><strong>Planning Files</strong></summary>
```powershell
git add FORMS-QUESTIONS.txt
git commit -m "Renamed 'FORMS QUESTIONS.txt' to 'FORMS-QUESTIONS.txt' for better CLI usage"

git rm "FORMS QUESTIONS.txt"
git commit -m "rm old filename 'FORMS QUESTIONS.txt'"

git push
```
</details>

<details>
<summary><strong>Media & Screenshots</strong></summary>
```powershell
git add github-screenshot-23-02-2026-FEB.jpg
git commit -m "added repo screenshot (23-FEB-2026)"

git add video-interview.mp4
git commit -m "Added interview (video-interview.mp4)"

git add video-interview-thumbnail.png
git commit -m "Added thumbnail for interview (video-interview-thumbnail.png)"

git add README.md
git commit -m "Added clickable link & thumbnail for media"
git push
```
</details>

<details>
<summary><strong>Design Files</strong></summary>
```powershell
git add ../design/figma-app-overview-v1.jpeg
git commit -m "Added Figma design image (figma-app-overview)"

git add README.md
git commit -m "Added clickable link & thumbnail for (figma-app-overview-v1)"
git push
```
</details>

<details>
<summary><strong>Git LFS Setup & Fix - video-interview.MOV (628MB)</strong></summary>
> **Problem:** Commit before 'git lfs' configurations.
> GitHub rejects files over 100mb.
> **Fixes:** (Soft-reset) & Re-commit after 'git lfs' configurations.
**Failed attempts — 'git lfs' not set up yet:**
```powershell
git lfs install
git lfs track "*.MOV"
git add .gitattributes
git add video-interview.MOV
git commit -m "Added fully edited interview - (video-interview.MOV)"
git push
# ERROR: File planing/video-interview.MOV is 628.53 MB — rejected
```
**Fixes — soft-reset & re-commit:**
```powershell
# undo unpushed commits, keep all files intact
git reset --soft origin/main

# re-add with lfs properly configured
git add planing/.gitattributes
git add planing/video-interview.MOV
git add planing/README.md
git add README.md
git commit -m "Add video interview via (git lfs)"
git push
# SUCCESS: Uploading LFS objects 100% — Writing objects: 951 bytes
```
</details>

<details>
<summary><strong>Sprint Notes Directory</strong></summary>
```powershell
git add ./planing/sprint-notes
git commit -m "Added (sprint-notes) Directory"

git add planing/sprint-notes/README.md
git commit -m "Edited sprint-notes README.md"
git push
```
</details>

<details>
<summary><strong>Badges & Quick Navigation</strong></summary>
```powershell
git add README.md
git commit -m "Added Badges"

git add README.md
git commit -m "Added Quick Navigation"
git push
```
</details>

<details>
<summary><strong>UML Diagrams</strong></summary>
```powershell
git add diagrams/
git commit -m "Added /diagrams & UMLs"

git add README.md
git commit -m "Updated README for UML diagrams"

git add usecase-diagram-drawio-importable.xml
git commit -m "Added importable drawio (usecase-diagram)"

git add usecase-diagram-drawio.jpeg
git commit -m "Added drawio image (usecase-diagram)"
git push
```
</details>

<details>
<summary><strong>Screenshots Cleanup & Reorganisation</strong></summary>
```powershell
git add github-screenshots/
git rm github-screenshot-23-02-2026-FEB.jpg

git add github-screenshot-09-03-2026-MAR.jpg
git commit -m "Moved screenshots to /github-screenshots — Added 09-March screenshot"

git add README.md
git commit -m "Added Links to /github-screenshots"
git push
```
</details>