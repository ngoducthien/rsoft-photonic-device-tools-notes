# rsoft-photonic-device-tools-notes
A collection of notes, tips, tricks, and guides on running and troubleshooting the RSoft Photonic Device Tools.


## MPI (parallel engine) is not running on your computer.

**Error Message**

```
RSoft MOST Error:
Couldn't connect to simulation server:
We are using MPICH_MPD but the mpd daemon does not seem to be running.
```

Quick Fix (Most Common Solution):

**Step 1 - Open Command Prompt as Administrator**

- Press **Windows key**
- Type `cmd`
- Right-click → **Run as administrator**

**Step 2 - Install and Start MPI Service**

Type:

```
smpd -install
```

Press Enter.

Then type:

```
smpd -start
```

**Step 3 - Test MPI**

Type:

```
mpiexec -n 2 hostname
```

If your computer name appears twice -> MPI is working.

Now reopen RSoft and run again.
