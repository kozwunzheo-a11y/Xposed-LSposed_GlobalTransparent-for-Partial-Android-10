Android 10 Global Transparency LSPosed Module (Redmi 9A Specialized Edition)

This is a lightweight global transparency background LSPosed module specifically developed for Android 10 (deeply optimized and tuned based on Redmi 9A / MIUI 12).
By directly hooking the system's low-level window attributes (Theme / Style), this module achieves a seamless transparent look without running persistent background services. It features zero idle RAM consumption and places no rendering burden on low-end processors.
CRITICAL WARNING: This project is strictly designed for Android 10 environments. DO NOT activate this module on Android 11 or higher (such as Xiaomi HyperOS, OneUI, or any newer systems). Doing so will 100% result in a bootloop (stuck on boot logo/soft-brick)!

App Compatibility and Support

• Most Applications: Perfectly supported. The framework injection works flawlessly for the majority of standard apps, providing a fully transparent background with smooth scrolling performance.
• Incompatible Exceptions: A small number of specific applications may not render transparency or could experience force-closes (crashes). This is due to app-level code obfuscation, system-level anti-screenshot/anti-overlay protections (such as FLAG_SECURE), or complex hardware-accelerated direct rendering.
• Recommendation: If you encounter any application that crashes or fails to display correctly, please make sure to uncheck or blacklist it in your LSPosed scope or module settings to maintain system stability.

Repository Structure

• /release : Contains the pre-compiled, ready-to-install .apk installer file.
• MainHook.java : The core hook logic source code, demonstrating how to intercept and override window background attributes at the Android 10 framework level.

Core Technical Advantages for Low-End Devices

1. No GPU Layer Blending Overhead: Unlike traditional transparency overlay apps that force-draw a real-time semi-transparent floating window layer, this module modifies the window properties directly. It requires zero extra blending calculations from the MediaTek Helio G25's GPU, preventing overheating and frame drops.
2. Zero RAM Footprint: Operating purely as an Xposed/LSPosed module, it injects code directly into the target processes. There are no background persistent daemons, preserving the extremely limited RAM on entry-level legacy devices.

Contributions and Disclaimer

Contributions, bug fixes, or adaptations for other legacy Android 10 devices via Pull Requests are highly welcome. This module is provided as-is for technical exchange and legacy device customization. The author holds no responsibility for any bootloops or device bricks caused by users ignoring the system version warnings.
