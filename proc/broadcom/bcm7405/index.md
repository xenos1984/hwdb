# BCM7405

## Features

* Advanced multi-format decoder supporting the following:
     * HD/SD H.264/AVC Main and High Profile to Level 4.1 (HD), Level 3.1 (SD)
     * VC-1 Advanced Profile @ Level 3, Simple and Main Profile
     * HD/SD MPEG-2 Main Profile at Main and High levels
     * MPEG still image decode
     * SD MPEG-4 P2 SP/ASP, DivX 3.11/4.11/5.x
* Advanced audio processor supporting the following:
     * AAC LC, AAC LC+SBR Level 2, AAC+ Level 2, AAC-HE
     * Dolby® Digital, Dolby Digital Plus
     * MPEG I layers 1, 2, and 3 (MP3)
     * Windows Media®and Windows Media Pro audio
     * One pair of on-chip stereo high-fidelity audio DACs
     * 3D SRS audio support
     * One I2S input port and one I2S output port, plus S/PDIF output
* High-performance 2D-effects graphic engine
     * Studio-quality text and graphics at HD resolution
     * Supports multiple layers and windows
* Digital noise and contour reduction (DNR/DCR)
     * Reduces artifacts such as block/mosquito noise
* Picture-in-picture
     * Supports simultaneous HD+SD display
* Mosaic Mode
     * Supports up to 16 video decode/display for video-rich navigation
* Motion-adaptive deinterlacer with reverse 3:2/2:2 pulldown
* OpenCable™ ready with on-chip MPOD support
* 400-MHz Dual-Core CMT MIPS32®/16e class processor
* 64-bit DDR2 DRAM controller
* Dual SATA-2 interfaces for DVR and DVD applications
* HD analog video encoder with simultaneous SD outputs
     * NTSC-M/J, PAL-BDGHIN/M/Nc, SECAM analog outputs
     * 480i/480p/576i/576p/720p/1080i output formats
     * Component RGB/YPrPb HD/HD-DVO outputs
     * Macrovision® 7.1/NICAM support
     * SCART 1 and 2
     * Component, S-Video, and composite via six on-chip V-DACs
     * VBI encoders for CC/TTX with NABTS/CGMSA/WSS/Gemstar®, AMOL I/II standards and dedicated TTX sideband
     * RF modulator with BTSC encoder
     * ITU-R-656 input and output ports
* HDMI 1.3/DVI 1.0 Mac and PHY with HDCP 1.1
* Broadcom security processor
* AES/1DES/3DES/CSS/CPRM/DTCP copy protection
* MPEG-2/DIRECTV/DVB/ARIB data transport demux with 1DES/3DES/DVB/Multi2/AES descramblers
* V.92-capable soft modem with integrated SiLab Si305x system side device
* Dual USB 2.0 host controller with host transceiver
     * Additional client USB 2.0 host controller/transceiver
* Dual Ethernet MACs with integrated single PHY and MII
* UHF remote control receiver
* Dual Smartcard support

## Memory map

This section contains a list of known MMIO addresses for the BCM7405. All addresses are physical. They can be accessed in kernel mode through the &quot;kseg1&quot; window for uncached access at virtual adress = physical address + 0xa0000000.

### External Bus Interface (EBI)

    0x10000800 : CS Base 0
    0x10000804 : CS Config 0
    0x10000808 : CS Base 1
    0x1000080c : CS Config 1
    0x10000810 : CS Base 2
    0x10000814 : CS Config 2
    0x10000818 : CS Base 3
    0x1000081c : CS Config 3
    0x10000820 : CS Base 4
    0x10000824 : CS Config 4
    0x10000828 : CS Base 5
    0x1000082c : CS Config 5
    0x10000900 : Configuration
    0x10000914 : Synchronous Intel StrataFlash Burst Configure
    0x10000918 : CS Tristate Configuration
    0x1000091c : TA Configuration
    0x100009f0 : Data Array Address

### NAND flash control

    0x10002800 : Revision
    0x10002804 : Command Start
    0x10002808 : Command Extended Address
    0x1000280c : Command Address
    0x10002810 : Command End Addres
    0x10002814 : EBI CS Select
    0x10002818 : EBI CS Address XOR with 1FC0 Control
    0x10002820 : Spare Area Read Bytes 0-3
    0x10002824 : Spare Area Read Bytes 4-7
    0x10002828 : Spare Area Read Bytes 8-11
    0x1000282c : Spare Area Read Bytes 12-15
    0x10002830 : Spare Area Write Bytes 0-3
    0x10002834 : Spare Area Write Bytes 4-7
    0x10002838 : Spare Area Write Bytes 8-11
    0x1000283c : Spare Area Write Bytes 12-15
    0x10002840 : Access Control
    0x10002844 : Config
    0x10002848 : Timing Parameters 1
    0x1000284c : Timing Parameters 2
    0x10002850 : Semaphore
    0x10002854 : Device ID
    0x10002858 : Block Lock Status
    0x1000285c : Interface Status
    0x10002860 : ECC Correctable Error Extended Address
    0x10002864 : ECC Correctable Error Address
    0x10002868 : ECC Uncorrectable Error Extended Address
    0x1000286c : ECC Uncorrectable Error Address
    0x10002870 : Flash Read Data Extended Address
    0x10002874 : Flash Read Data Address
    0x10002878 : Page Program Extended Address
    0x1000287c : Page Program Address
    0x10002880 : Copy Back Extended Address
    0x10002884 : Copy Back Address
    0x10002888 : Block Erase Extended Address
    0x1000288c : Block Erase Address
    0x10002890 : Flash Invalid Data Extended Address
    0x10002894 : Flash Invalid Data Address
    0x10002898 : Block Write Protect Enable and Size for EBI_CS0b

### Clock control

    0x10040000 : Clock generator revision
    0x10040004 : Software power management control to turn off 108 MHz clocks
    0x10040008 : Software power management control to turn off 200, 81, 54, 32.4, 27, 25, 20.25 and 40.5 MHz clocks
    0x1004000c : Software power management control to turn off audio DSP, MIPS, SATA_PCI clocks
    0x10040010 : Clock generator block output clock selection
    0x10040014 : Low 3rd Overtone Oscillator Control
    0x10040024 : Current lock status of main PLL
    0x10040030 : SYS 1 PLL control bus lower word
    0x10040034 : SYS 1 PLL control bus lower word
    0x10040070 : Clock generator scratch

### Ethernet

    0x10080000 : eth0
    0x10090000 : eth1

### Timers and watchdog

    0x104007c0 : Timer Interrupt Status
    0x104007c4 : Timer IRQ Enable
    0x104007c8 : Timer 0 Control
    0x104007cc : Timer 1 Control
    0x104007d0 : Timer 2 Control
    0x104007d4 : Timer 3 Control
    0x104007d8 : Timer 0 Status
    0x104007dc : Timer 1 Status
    0x104007e0 : Timer 2 Status
    0x104007e4 : Timer 3 Status
    0x104007e8 : Watchdog Timeout
    0x104007ec : Watchdog Command
    0x104007f0 : Watchdog Chip Reset Count
    0x104007f4 : Watchdog Chip Reset Status
    0x104007f8 : Timer PCI Interrupt Enable
    0x104007fc : Watchdog Control

### Serial UARTs

The BCM7405 contains three 16550A UARTs at the following addresses:

    0x10400b00 - 0x10400b3f : UART 1
    0x10400b40 - 0x10400b7f : UART 2
    0x10400b80 - 0x10400bbf : UART 3

Since the MIPS architecture allows direct memory access to 32 bit aligned memory addresses only, the 16550 registers can be found at the following addresses (shown only for UART 1):

    0x10400b00 : Receiver Buffer (read), Transmitter Holding Register (write)
    0x10400b04 : Interrupt Enable
    0x10400b08 : Interrupt Identification (read) / FIFO control (write)
    0x10400b0c : Line Control
    0x10400b10 : Modem Control
    0x10400b14 : Line Status
    0x10400b18 : Modem Status
    0x10400b1c : Scratch
    0x10400b00 : Divisor Latch (LSB)
    0x10400b04 : Divisor Latch (MSB)

### Chip identification and configuration

    0x10404000 : Product Revision ID
    0x10404004 : Sundry Revision ID
    0x10404008 : Reset control
    0x10404014 : Software reset
    0x10404018 : Reset history
    0x1040401c : Strapping values 1
    0x10404020 : Strapping values 2
    0x10404024 : Bond option value
    0x10404028 : OTP option test
    0x1040402c : OTP option status
    0x10404030 : Semaphore channel 0
    0x10404034 : Semaphore channel 1
    0x10404038 : Semaphore channel 2
    0x1040403c : Semaphore channel 3
    0x10404040 : Semaphore channel 4
    0x10404044 : Semaphore channel 5
    0x10404048 : Semaphore channel 6
    0x1040404c : Semaphore channel 7
    0x10404050 : Semaphore channel 8
    0x10404054 : Semaphore channel 9
    0x10404058 : Semaphore channel 10
    0x1040405c : Semaphore channel 11
    0x10404060 : Semaphore channel 12
    0x10404064 : Semaphore channel 13
    0x10404068 : Semaphore channel 14
    0x1040406c : Semaphore channel 15
    0x10404070 : General watchdog timer 0
    0x10404074 : General watchdog timer 1
    0x10404078 : General control 0
    0x1040407c : General control 1
    0x10404080 : General control 2
    0x10404084 : General status 0
    0x10404088 : General status 1
    0x1040408c : General status 2
    0x10404090 : Scratch
    0x10404100 : Pin mux control 0
    0x10404104 : Pin mux control 1
    0x10404108 : Pin mux control 2
    0x1040410c : Pin mux control 3
    0x10404110 : Pin mux control 4
    0x10404114 : Pin mux control 5
    0x10404118 : Pin mux control 6
    0x1040411c : Pin mux control 7
    0x10404120 : Pin mux control 8
    0x10404124 : Pin mux control 9
    0x10404128 : Pin mux control 10
    0x1040412c : Pin mux control 11
    0x10404130 : Pin mux control 12
    0x10404134 : Pin mux control 13
    0x10404200 : Test port control
    0x10404208 : EJTAG input bus enables
    0x1040420c : EJTAG output select
    0x10404210 : UART Router select
    0x1040421c : Serial Slave Port configuration
    0x10404220 : SERS Revision
    0x10404224 : SERS Configuration
    0x10404280 : Testport out peek
    0x10404284 : Testport out poke
    0x10404288 : Testport in peek
    0x1040428c : Testport in poke
    0x10404300 : Spare control bits reserved for future use
    0x10404400 : Block select for RO testmode
    0x10404404 : Simultaneous switching testmode control
    0x10404408 : Testmode

0x10404000 contains a CPU model ID and a revision ID:
{{Register32
|width=320px
|offset0=0
|name0=Revision ID
|offset1=16
|name1=BCD coded CPU model
}}
The upper 16 bits contain 0x7405 for the BCM7405 and 0x7413 for the BCM7413.

### USB

    0x10480300 - 0x104803a8 : EHCI 0
    0x10480400 - 0x1048046f : OHCI 0
    0x10480500 - 0x104805a8 : EHCI 1
    0x10480600 - 0x1048066f : OHCI 1

### SATA

    0x10510000 : ata1
    	0x10510000 : Command
    	0x10510020 : Control
    	0x10510030 : DMA

    0x10510100 : ata2
    	0x10510100 : Command
    	0x10510120 : Control
    	0x10510130 : DMA

### DDR Memory Controller

The BCM7405 has two separate memory bank controllers:

    0x10c08000 - 0x10c082d7, 0x10c09000 - 0x10c0923f, 0x10c0a000 - 0x10c0a027 : Bank 0
    0x10c02000 - 0x10c022d7, 0x10c03000 - 0x10c0323f, 0x10c04000 - 0x10c04027 : Bank 1

In the following, only the registers for bank 0 will be shown.

    0x10c0a000 Mode-Configuration
    0x10c0a004 DDR Mode
    0x10c0a008 DDR-SDRAM Timing 0
    0x10c0a00c DDR-SDRAM Timing 1
    0x10c0a010 Read to Write &amp; Write to Read Timing
    0x10c0a014 Auto-Refresh Power Down Control
    0x10c0a018 Sequencer Enable
    0x10c0a01c State Machine Timeout
    0x10c0a020 Status
    0x10c0a024 Bank Status

## Pinout

The BCM7405 is packaged as a 976 pin, 1 mm, 34 * 34 ball grid array (BGA). See [BCM7405/Pinout] for a complete pinout.

## Devices containing BCM7405 microprocessors

* [[ET9000]] DVB-S receiver
* Dreambox [[DM 500 HD]]
* Dreambox [[DM 800 HD SE]]
* Dreambox [[DM 7020 HD]]

## Links

* http://www.broadcom.com/products/IPTV/IPTV-Solutions/BCM7405
* http://www.broadcom.com/products/Cable/Cable-Set-Top-Box-Solutions/BCM7405
* [Product brief](http://www.datasheets.org.uk/indexdl/Datasheet-025/DSA00437494.pdf)
* **bcm97405mbv00\_p10.pdf** / **bcm97405mbv00\_p10.rar** Circuit diagram / pinout

[BCM7405/Pinout]: pinout.html
