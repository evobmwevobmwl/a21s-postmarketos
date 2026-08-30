# postmarketOS for Samsung Galaxy A21s

Experimental GitHub Actions build for Samsung Galaxy A21s (`SM-A217F`).

The current device tree is intended for the 3 GB RAM variant. Do not flash the
result on another model or RAM variant without adapting and testing its device
tree.

## Build

1. Open the repository's **Actions** tab.
2. Select **Build postmarketOS for Galaxy A21s**.
3. Click **Run workflow**.
4. Use the `console` interface for the first test.
5. Download the build from the **Artifacts** section after the job finishes.

Optionally create an Actions secret named `PMOS_PASSWORD`. If it is not set,
the image uses `147147` as the password for the `pmos` user.

Unlocking a Samsung bootloader erases user data and trips Knox. Keep the exact
stock firmware for the phone before attempting to flash any experimental image.
