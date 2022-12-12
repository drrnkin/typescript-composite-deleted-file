## Example of not detecting a deleted file in a child project in composite mode.

### Steps to reproduce:
* In both the main and child folders, run "yarn" to install each.
* In the main folder, run "yarn build" to build both projects in composite mode.
* In the child folder, delete all "child2" files.
* In the main folder, run "yarn build" again and note that it doesn't detect the missing file "child2".

Note that "yarn tsc" in the child package will detect the missing file, but it is not detected
when built with composite mode.