# Eclipse Kernel — Rosemary (Linux 4.19)

Custom Linux 4.19 kernel for **Xiaomi Redmi Note 10S / POCO M5s** (`rosemary` / `maltose` / `secret`), tuned for sustained gaming performance, responsive scheduling, and daily efficiency.

---

## 📱 Supported Devices
* **Xiaomi Redmi Note 10S** (`rosemary`)
* **POCO M5s** (`rosemary_p`)
* **SoC:** MediaTek Helio G95 (MT6785) — Mali-G76 MC4

---

## ✨ Key Features & Optimizations

* **GPU Overclock (Real PLL):** Mali-G76 MC4 unlocked up to **950 MHz** via `mt6785` GPUFREQ OPP table (`MFGPLL`).
* **Clang Full LTO (`CONFIG_LTO_CLANG`):** Compiled with Clang/LLVM + LLD with global Link-Time Optimization enabled for tighter instruction caching and lower syscall overhead.
* **Tuned PELT (16ms):** Scheduler Per-Entity Load Tracking half-life reduced from `32ms` to `16ms` for faster CPU frequency ramp-up under sudden gaming loads.
* **Root Support (Available Variants):**
  * **KSUN (`ksun`):** KernelSU Next + 950 MHz GPU OC.
* **Upto 27W Fast Charging Preserved:** Full `bq2597x` charge pump & `mtk_charger` support intact.

---

## 🛠️ Build Environment & Toolchain

* **Linux Version:** `4.19.x`
* **Compiler:** Clang / LLVM + `ld.lld` (`LLVM=1 LLVM_IAS=1`)
* **Defconfig:** `rosemary_defconfig`

## 📦 Installation (AnyKernel3)

### Prerequisites
* Unlocked bootloader on your **Redmi Note 10S / POCO M5s** (`rosemary`).
* Custom recovery installed (**TWRP** or **OrangeFox**).
* Download the appropriate `Eclipse-4.19-rosemary-*.zip` release matching your setup:
  * **`ksun` :** For **KernelSU Next** users (do not combine with Magisk).

### Flashing Steps
1. **Download** the kernel ZIP file (`Eclipse-4.19-rosemary-*.zip`) to your device's internal storage or microSD.
2. **Reboot to Custom Recovery** (power off, then hold `Volume Up + Power`, or run `adb reboot recovery`).
3. **Back up** your current `Boot` partitions *(highly recommended so you can restore easily if needed)*.
4. Go to **Install**, select `Eclipse-4.19-rosemary-*.zip`, and **swipe to flash**.
5. *(Optional)* Tap **Wipe Dalvik / Cache** — **do not** wipe `Data` or `System`.
6. **Reboot System** and enjoy.

## ⚠️ Disclaimer

* **Use at your own risk.** Nobody is forcing you to flash or use this kernel.
* **You are solely responsible** for any damage that may occur to your device — including bricked devices, bootloops, hardware degradation, overheating/thermal throttling from GPU overclocking, or data loss.
* Always back up your stock `boot.img` before flashing, and make sure you know how to restore them via recovery or `fastboot`.
