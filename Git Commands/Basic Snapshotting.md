## Git Commands

### Basic Snapshotting
<br>

```bash
git add [file]
```
- Add a file to thr staging area.
<br>

```bash
git add .
```
- Add all new and changed files to the staging area.
<br>

```bash
git commit -m "Commit message"
```
- Commit changes to the repository with a message.
<br>

```bash
git status
```
- Show the status of changes as untracked, modified, or staged.
<br>

```bash
git diff
```
- Show differences between working directory and index.
<br>

```bash
git diff --staged
```
- Show differences between the index and the last commit.
<br>

```bash
git reset [file]
```
- Unstage a file while retaining chages in working directory.
<br>

```bash
git reset --hard
```
- Reset the working directory to the last commit.
<br>
