# postmarketOS for Samsung Galaxy A21s

Experimental TWRP recovery ZIP build for Samsung Galaxy A21s (`SM-A217F`).

The current device tree is intended for the 3 GB RAM variant. Do not flash the
result on another model or RAM variant without adapting and testing its device
tree.

The repository contains a previously compiled Linux 7.2 kernel package. The
workflow repackages it with the current CI signing key instead of compiling the
kernel again.

## Build recovery ZIP

1. Open the repository's **Actions** tab.
2. Select **Build postmarketOS recovery ZIP for Galaxy A21s**.
3. Click **Run workflow**.
4. Use the `console` interface for the first test.
5. Download `postmarketOS-galaxy-a21s-recovery-*` from the **Artifacts**
   section after the job finishes.

Optionally create an Actions secret named `PMOS_PASSWORD`. If it is not set,
the image uses `147147` as the password for the `pmos` user.

The generated recovery ZIP targets the `USERDATA` partition. Flashing it from
TWRP erases Android user data. Unlocking a Samsung bootloader also erases user
data and trips Knox. Keep the exact stock firmware and a backup before flashing
this experimental image.
