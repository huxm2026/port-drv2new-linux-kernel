commit 6af2f16ed70d928bc363774d461f74c9af54ba40 (HEAD -> master)
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Wed Sep 2 16:19:08 2026 +0800

    Clean up redundant debug information in *.ko modules and DEBUG settings in .config
    

commit 7c59ee9b9f87d2e928ea961d5216e3fd4fd89270
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Tue Sep 1 17:15:18 2026 +0800

    1. Fix eth0 NIC driver, KASAN use-after-free or slab-out-of-bounds errors
    2. Fix DMA-API: cacheline tracking EEXIST, overlapping mappings aren't supported error
    

commit 225e5e25b355c99dde32545504064bee0708ef59
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Sat Aug 29 23:23:30 2026 +0800

    Review the troubleshooting process for the hung issue after 'Starting kernel ... Uncompressing Linux... done, booting the kernel.' and remove debug information used during debugging.
    

commit 698e1ed92444b3f128410e04d33ba426c1bf9eab
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Wed Aug 26 13:36:42 2026 +0800

    clocksource and clockevent rewrite, improved using Linux-5.15 kernel's built-in driver arm,sp804 which lacks high-resolution timer
    1. The functions setup_irq, remove_irq, register_cpu_notifier may have been removed or no longer exported as symbols in Linux-5.15 kernel; rewritten and tested using request_irq(), free_irq(), and cpuhp_setup_state_nocalls.
    2. Replaced clocksource_register_hz with clocksource_mmio_init for more efficient and reasonable code.
    

commit 09483347039e197e7d9e660c42e12e6fe769ae5d
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Mon Aug 24 15:13:34 2026 +0800

    Clean up debug messages in clock controller (clk.c, clk-hi3798mv100.c) and fix a bug in EMMC host driver (himciv200.c); also remove stale Kconfig/Makefile fragments
    

commit 227f7fa9280e6498fec8e9bef12097fb7f6d5edc
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Mon Aug 10 15:18:59 2026 +0800

    fix: resolve driver bugs in sample/higo/sample_dec and improve clock controller
    
    Fix the driver issues found during testing of sample/higo/sample_dec, which also triggered a rework of the previous fix for loading hi_*.ko modules. Additionally, refine the incomplete parts of the clock controller implementation.
    

commit 1fbf49cc86201b583e18dc8fbf1a6bc5ad4a85c5
Author: Linux Kernel Upgrade <Upgrade@email.system>
Date:   Wed Jul 22 14:24:58 2026 +0800

    Fix drivers for insmod of hi_*.ko modules
    

......省略，只展示最近的部分。
