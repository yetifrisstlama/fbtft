# FORK
Because the world clearly needs __another__ fork of `fbtft` ;)

  * tried to get the most up to date and cleanest sources by copying the files
    from the linux kernel staging tree
  * make `fb_ssd1306.c` compatible with the 128 x 32 OLED on the Zedboard
    (UG-2832HSWEG04). Tested and works well
  * Add `dts/zynq-zed.dts` as an example of how I added the OLED to the device
    tree
  * Add `fb_ssd1322.c` from Ryan Press. Compiles but not tested yet.


  FBTFT
=========

2015-01-19
The FBTFT drivers are now in the Linux kernel staging tree: https://git.kernel.org/cgit/linux/kernel/git/gregkh/staging.git/tree/drivers/staging/fbtft?h=staging-testing
Development in this github repo has ceased.


Linux Framebuffer drivers for small TFT LCD display modules.
The module 'fbtft' makes writing drivers for some of these displays very easy.

Development is done on a Raspberry Pi running the Raspbian "wheezy" distribution.

INSTALLATION
  Download kernel sources

  From Linux 3.15
    cd drivers/video/fbdev
    git clone https://github.com/notro/fbtft.git

    Add to drivers/video/fbdev/Kconfig:   source "drivers/video/fbdev/fbtft/Kconfig"
    Add to drivers/video/fbdev/Makefile:  obj-y += fbtft/

  Before Linux 3.15
    cd drivers/video
    git clone https://github.com/notro/fbtft.git

    Add to drivers/video/Kconfig:   source "drivers/video/fbtft/Kconfig"
    Add to drivers/video/Makefile:  obj-y += fbtft/

  Enable driver(s) in menuconfig and build the kernel


See wiki for more information: https://github.com/notro/fbtft/wiki


Source: https://github.com/notro/fbtft/
