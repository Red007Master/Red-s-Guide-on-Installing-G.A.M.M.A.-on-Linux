# Updating GAMMA

## 1 - Backup
  - **1.1** - Backup your saves (and other stuff that you may need).

## 2 - Folder prep 
  - **2.1** - Delete `./GAMMA` and `./Anomaly`.

## 3 - Updating `gamma-launcher`.
  - **3.1** - Enter `venv` (i.e: one you created when installing GAMMA, in step `3.2`/`3.3` of install guide).
  - **3.2** - Enter `gamma-launcher`'s folder.
  - **3.3** - Do `git pull`, you should see something like:
    ```
    remote: Enumerating objects: 34, done.
    remote: Counting objects: 100% (23/23), done.
    remote: Compressing objects: 100% (9/9), done.
    remote: Total 34 (delta 14), reused 14 (delta 14), pack-reused 11 (from 1)
    Unpacking objects: 100% (34/34), 8.83 KiB | 2.21 MiB/s, done.
    From https://github.com/Mord3rca/gamma-launcher
       1ce5ad5..dff3ef3  master      -> origin/master
     * [new branch]      fix/updates -> origin/fix/updates
    Updating 1ce5ad5..dff3ef3
    Fast-forward
     .gitignore                  |  6 +++++-
     README.md                   | 10 ++++++++++
     easy-install/Makefile       | 58 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++
     easy-install/README.md      | 32 +++++++++++++++++++++++++++++++
     easy-install/gamma-launcher | 29 +++++++++++++++++++++++++++++
     5 files changed, 134 insertions(+), 1 deletion(-)
     create mode 100644 easy-install/Makefile
     create mode 100644 easy-install/README.md
     create mode 100755 easy-install/gamma-launcher
     ```
     or 

     ```
     Already up to date.
     ```

     If you got something like:
     ```
     fatal: not a git repository (or any of the parent directories): .git
     ```
     It means that you are (likely) in the wrong folder.
  - **3.4** - Do `pip install .`:

    If you got something like `ERROR: Directory '.' is not installable. Neither 'setup.py' nor 'pyproject.toml' found.` it means that you are (likely) not in `gamma-launcher`'s folder.
    You need to be in venv as per **3.1**.
  
    If you did **3.4** right you shoud see `Successfully installed gamma-launcher-X.X`.

## 4 - "Update"(Install) GAMMA.
   - **4.1** - Follow steps from "4 - GAMMA Installation" install guide, make sure that `--cache-directory` points to actual cache folder from before (initial insall).
