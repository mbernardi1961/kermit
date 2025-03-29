# Setting up various versions of Kermit
I recently (February 2024) rediscoverd the [Kermit Project](https://kermitproject.org), after being a serious user in the 1980's-90's.

Initially I wanted to be able to use kermit on my recently purchased AgonLight2. The CP/M version was included with the version of CP/M made available with the AgonLight2. But it was unable to configure the serial port used.
The new ZINC (Zinc is not CP/M) wrapper <b>does</b> appear to allow this to be configured. But I haven't managed to get it working yet.

I also got my BBC Master working again (after 40 years) with the [PiTubeDirect](https://github.com/mbernardi1961/PiTubeDoc) and wanted to be able to install kermit on the various processors (so far without sucess). The following ought to be available: 
<li>BBC Kermit [1.46] MOS (Native confirmed working)
<li>MS-DOS Kermit [3.16] DR-DOSPlus
<li>Kermit 80 [4.11] Z80 CP/M
<li>C-Kermit [4C(057)] PANOS (this may be upgradeable to the current C-Kermit 10 Beta)

So I wanted to get something working and decided to test compile the new [C-Kermit 10  Beta](https://www.kermitproject.org/ck10devbuilds.html).
As Frank da Cruz says on the C-Kermit 10.0 Beta-Test Builds 2021-25 page; I provided a large percentage of the recent x86_64 Linux, BSD &amp; Solaris builds in VirtualBox and most the of the ARM builds using a Raspberry Pi 4.
C-Kermit 10 Beta 11 was released on 8 August 2024 and has bee built sucessfully for 175 systems; including various BSD, Linux, & Solaris systems. With gcc, clang and ssl.

C-Kermit is available via github.com at [ckermit](https://github.com/KermitProject/ckermit), and the customised Windows version can be found at [ckwin](https://github.com/davidrg/ckwin).

It was particularly interesting building under the BSD and Solaris flavours, as I hadn't used either of these systems before.

There are a few systems that SHOULD compile C-Kermit, but haven't been built for decades! These include the following: Coherent 4.2, BeOS 4.5 (Haiku), OpenStep 4.2 &amp; Plan9, I haven't managed to get C-Kermit on any of these working yet.

C-Kermit will compile without any aditional libraries / dependancies in a few OS instances, (ie all the requisite libraries were preinstalled). 
However for most Debian derivitives the follwing are needed:
<li>make (if not installed) or cmake
<li>gcc (if not installed)
<li>clang (as an alternatve to gcc)
<li>libc-dev or glibc-dev (if not installed)
<li>libssl-dev (to add ssl)
<li>libpam-dev (to add ssl)
<li>libz-dev (to add ssl if not installed)<br>
For non Debian distros the following library names are used<br>
<li>openssl-devel
<li>pam-devel
<li>zlib-devel
<li>libc-devel or glibc-devel

So far I've build C-Kermit on over 40 different systems running under VirtualBox and 20 systems on a Raspberry Pi 4.

The following OSes require non standard make commands to compile (once all the dependancies are installed)
<li>Minix 3.4 RC6 - make netbsd
<li>Open Mandriva - make LIBS=-lcrypt linux
<li>Gentoo Linux - make LIBS=-ltinfo linux

