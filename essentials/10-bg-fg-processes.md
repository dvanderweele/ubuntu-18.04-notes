# Backgrounding & Foregrounding Processes
# Essentials

If you are viewing HTOP and want to return 
to your shell, while letting HTOP run in the 
background:
```bash
CTRL+Z
```
A command to view your current background jobs:
```bash
jobs 
```
If you only have one background job, how do you 
bring it back to the foreground:
```bash
fg
```
How do you use fg to bring back a specific background
job, say job #2:
```bash
fg 2
```
A command to launch htop straight to the background:
```bash
htop &
```
