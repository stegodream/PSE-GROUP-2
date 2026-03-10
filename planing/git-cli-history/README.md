# Git Command History — PSE Group 02
> Reconstructed from PowerShell history.

## Initial Setup
```powershell
git config --global credential.helper manager
git config --global user.name "stegdream"
git config --global user.email "stegdream@users.noreply.github.com"
git clone https://github.com/stegodream/PSE-GROUP-2.git
```

## First Commit - Folder Structure
```powershell
git add .
git commit -m "Add initial project folder structure"
git push
```

## README Updates
```powershell
git add README.md
git commit -m "updated README.md"
git push
```

## Planning Files
```powershell
git add FORMS-QUESTIONS.txt
git commit -m "Renamed 'FORMS QUESTIONS.txt' to 'FORMS-QUESTIONS.txt' for better CLI usage"

git rm "FORMS QUESTIONS.txt"
git commit -m "rm old filename 'FORMS QUESTIONS.txt'"

git push
```

## Media & Screenshots
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

## Design Files
```powershell
git add ../design/figma-app-overview-v1.jpeg
git commit -m "Added Figma design image (figma-app-overview)"

git add README.md
git commit -m "Added clickable link & thumbnail for (figma-app-overview-v1)"
git push
```

## Git LFS Setup & Fix — video-interview.MOV (628MB)
> Problem: Committed file before LFS configured.
> GitHub rejects files over 100mb
> Fixed: (soft reset & recommit) after LFS configured.
```powershell
# initial failed attempts (lfs not set up yet)
git lfs install
git lfs track "*.MOV"
git add .gitattributes
git add video-interview.MOV
git commit -m "Added fully edited interview - (video-interview.MOV)"
git push
# ERROR: File planing/video-interview.MOV is 628.53 MB — rejected
```
```powershell
# fix — undo unpushed commits, keep files
git reset --soft origin/main

# re-add with lfs properly configured
git add planing/.gitattributes
git add planing/video-interview.MOV
git add planing/README.md
git add README.md
git commit -m "Add video interview via (git lfs)"
git push
# SUCCESS: Uploading LFS objects 100% 
```

## Sprint Notes Directory
```powershell
git add ./planing/sprint-notes
git commit -m "Added (sprint-notes) Directory"

git add planing/sprint-notes/README.md
git commit -m "Edited sprint-notes README.md"
git push
```

## Badges & Quick Navigation
```powershell
git add README.md
git commit -m "Added Badges"

git add README.md
git commit -m "Added Quick Navigation"
git push
```

## UML Diagrams
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

## Screenshots Cleanup/Organize
```powershell
git add github-screenshots/
git rm github-screenshot-23-02-2026-FEB.jpg

git add github-screenshot-09-03-2026-MAR.jpg
git commit -m "Moved screenshots to /github-screenshots — Added 09-March screenshot"

git add README.md
git commit -m "Added Links to /github-screenshots"
git push
```