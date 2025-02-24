# Cheat Sheet
This is my personal cheat sheet, a curated collection of useful commands I've gathered over the years while working in data science and software engineering.
## BASH
|**Action**|**Command**|
|-|-|
|**Make folder**|`mkdir <name>`|
|**Rename folder**|`mv <old> <new>`|
|**Remove file**|`rm <file>`|
|**Remove non-empty folder**|`rm -r <folder>`|
|**Colored shell .bashrc**|`PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u\[\033[01;31m\]@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '`|
|**Display processes**|`top`|
|**Display processes detailed**|`htop`|
|**Kill process**|`kill <pid>`|
|**Make script executable**|`chmod +x <script.sh>`|
|**Transfer file**|`scp <from/path/file.txt> <to/server:/full/path/>`|
|**Transfer folder**|`scp -r <from/server:/full/path/folder> <to/path/folder>`|
---
## CONDA
|**Action**|**Command**|
|-|-|
|**Create env**|`conda create -n <name> -f <filename.yml>`|
|**List all env**|`conda env list`|
|**Activate env**|`conda activate <name>`|
|**Deactivate env**|`conda deactivate`|
|**Update conda**|`conda update -n base conda`|
|**Update packages**|`conda update --all`|
|**Delete env**|`conda env remove -n <name>`|
|**Export env**|`conda env export > <filename.yml>`|
---
## GIT
|**Action**|**Command**|
|-|-|
|**Clone**|`git clone <url>`|
|**Add file**|`git add <file>`|
|**Add everything**|`git add -A`|
|**Commit**|`git commit -m 'first commit'`|
|**Add a hub**|`git remote add <remote-name> git@github.com:flavioschenker/project.git`|
|**Push**|`git push`|
|**Push to hub**|`git push -u <remote-name> <branch-name>`|
|**Create branch**|`git branch <branch-name>`|
|**Switch branch**|`git checkout <branch-name>`|
|**New repository**|`git init`|
|**New at location**|`git init <directory>`|
|**Set username**|`git config --global user.name 'My Name'`|
|**Set email**|`git config --global user.email 'My E-Mail'`|
---
## NEW
|**Action**|**Command**|
|-|-|
|**Update wget**|`sudo apt update`|
|**Install git**|`sudo apt install git-all`|
|**Generate ssh-key**|`ssh-keygen -t ed25519`|
|**Read out key**|`cat ~/.ssh/id_rsa.pub`|
|**Insert keys to hubs**|GitLab, GitHub|
|**Create repo folder**|`mkdir repos`|
|**Clone git repos**|`git clone <link SSH>`|
|**Install conda**|`wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`|
|**Update conda**|`conda update -n base conda`|
|**Personalize bashrc**|`code .bashrc`|
---
## SLURM
|**Action**|**Command**|
|-|-|
|**Set environment variable**|`export SLURM_CONF=/path/to/file.conf`|
|**Interactive shell**|`srun --mem=64G --cpus-per-task=1 --gres=gpu:a100:1 --exclude=gpu[05-07,09] --pty bash -i`|
|**Train alias**|`alias strain='sbatch /path/to/slurm/script.sh'`|
|**Set PYTHONPATH in script**|`export PYTHONPATH=/path/to/repository/project:$PYTHONPATH`|
|**Set PATH in script**|`export PATH=/path/to/repository/project:$PATH`|