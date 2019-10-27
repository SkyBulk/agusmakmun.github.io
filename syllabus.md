---
layout: page
title: Syllabus
permalink: /syllabus/
---
Course Description
==================

This course is about memory corruptions attacks manually and automatically. Students will study differents applications and how they operate; learn, study, and exploit cutting edge application vulnerabilities; understand automated vulnerability analysis tools; learn the state-of-the-art in memory corruptions automated vulnerability analysis tools; and develop a novel automated vulnerability analysis tool. We will also cover how to use these techniques legally and ethically.

The first half of the course will focus on understanding low level applications and how to exploit applications, and these topics will be reinforced with practical, hands-on. The second half of the course will focus on the state-of-the-art in automated vulnerability analysis of applications via reading and presenting research papers.


Prerequisites
=============

This course will be insane, and students are expected to learn the necessary technologies. Students will expected to already understand networking and the TCP/IP stack. Students with strong skills in C/C++, x86 assembly and at least one scripting language (Python, Ruby, Javascript, etc.) 


`To benefit from this course you need to know and be comfortable with x86 assembly. This is not negotiable!`
`Hint: I did this syllabus using windows 7 x86 enterprise , and Windows 10 Home Single Language 64-bit`

Course Topic

1. [Basic Reverse engineering](https://www.youtube.com/watch?v=cATBah30jk0&t=2569s) 
2. Software Vulnerability Review
	* [Buffer OverFlow](https://www.coengoedegebure.com/buffer-overflow-attacks-explained/)
	* [Format String Bug](https://www.geeksforgeeks.org/format-string-vulnerability-and-prevention-with-example/)
	* [Integer OverFlow](https://www.exploit-db.com/docs/english/28477-linux-integer-overflow-and-underflow.pdf)
3. Classic Technique Review
	* Writing RET Based Buffer OverFlow Exploits
		* [Buffer OverFlow](https://www.corelan.be/index.php/2009/07/19/exploit-writing-tutorial-part-1-stack-based-overflows/)
		* [more ways to place shellcode](https://www.corelan.be/index.php/2009/07/23/writing-buffer-overflow-exploits-a-quick-and-basic-tutorial-part-2/)
		* [Bad chars](https://bulbsecurity.com/finding-bad-characters-with-immunity-debugger-and-mona-py/)
		* Real Application Attack
			* [Seattle Lab Mail (SLmail) 5.5](https://www.exploit-db.com/apps/12f1ab027e5374587e7e998c00682c5d-SLMail55_4433.exe)
			*  [R 3.4.4 - Buffer Overflow](https://www.exploit-db.com/apps/a642a3de7b5c2602180e73f4c04b4fbd-R-3.4.4-win.exe)
4. Win32 ShellCode
  * [Making Win32 ShellCode](https://www.corelan.be/index.php/2010/02/25/exploit-writing-tutorial-part-9-introduction-to-win32-shellcoding/)
  * [msfvenom](https://netsec.ws/?p=331)

5. About Defence Technique
  * [GS(Stack Guard / Stack Cookie)](https://docs.microsoft.com/en-us/cpp/build/reference/gs-buffer-security-check?view=vs-2019)
  * [SafeSEH(SEH Handler Validation Check)](https://docs.microsoft.com/en-us/cpp/assembler/masm/dot-safeseh?view=vs-2019)
  * [DEP(Data Execution Prevension)](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10.md#data-execution-prevention)
  * [ASLR(Address Space Layout Randomization)](https://en.wikipedia.org/wiki/Address_space_layout_randomization)
  * [SEHOP(Structured Error Handling Overwrite Protection)](https://msrc-blog.microsoft.com/2009/02/02/preventing-the-exploitation-of-structured-exception-handler-seh-overwrites-with-sehop/)

6. SEH(Structured Error Handling)
	* [SEH(Structured Error Handling)?](https://docs.microsoft.com/en-us/windows/win32/debug/structured-exception-handling)
	* [Immunity Debugger](https://www.youtube.com/watch?v=6JBRXqT3USI)
	* [Wingdb](https://www.youtube.com/watch?v=8zBpqc3HkSE&list=PLhx7-txsG6t6n_E2LgDGqgvJtCHPL7UFu)
	* [Debugging Stack View On The SEH Chain](https://resources.infosecinstitute.com/in-depth-seh-exploit-writing-tutorial-using-ollydbg/#sehchain)
	* [The need for a POP POP RET instruction sequence](https://dkalemis.wordpress.com/2010/10/27/the-need-for-a-pop-pop-ret-instruction-sequence/)
7. Writing SEH Based Buffer OverFlow Exploits
	* [SEH Handler OverWrite](https://www.corelan.be/index.php/2009/07/25/writing-buffer-overflow-exploits-a-quick-and-basic-tutorial-part-3-seh/)
	* [Debugging GS Option Enable](https://preshing.com/20110807/the-cost-of-buffer-security-checks-in-visual-c/)
	* [Check SafeSEH](https://blog.netspi.com/verifying-aslr-dep-and-safeseh-with-powershell/)
	* Real Application Attack
		* [DVD X Player 5.5 Pro](https://www.exploit-db.com/apps/cdfda7217304f4deb7d2e8feb5696394-DVDXPlayerSetup.exe)
		* [R 3.4.4 - Buffer Overflow (SEH)](https://www.exploit-db.com/apps/a642a3de7b5c2602180e73f4c04b4fbd-R-3.4.4-win.exe)
8. Egghunting
	*  [Egghunting?](https://www.corelan.be/index.php/2010/01/09/exploit-writing-tutorial-part-8-win32-egg-hunting/)
	* Real Application Attack
		* [Easy File Sharing Web Server 7.2](https://www.exploit-db.com/apps/60f3ff1f3cd34dec80fba130ea481f31-efssetup.exe)
		* [Eureka Email Client 2.2q](https://www.exploit-db.com/apps/2b0e55c58e1355c4bd0143d06ce3d239-EurekaEmailSetup.exe)

8. ASLR(Address space layout randomization)
	* Real Application Attack
		* [ANI vulnerability](https://www.sans.org/reading-room/whitepapers/threats/ani-vulnerability-history-repeats-1926)
		*  Real Application Attack
			* [Abusing non-ASLR enabled libraries](https://www.exploit-db.com/apps/e9d68d1ad9873339d6ef0fd5a2e1f0bd-CoolPlayerPlusPortable_2.19.6.paf.exe)
			* [Partial EIP overwrite](https://www.sans.org/reading-room/whitepapers/threats/ani-vulnerability-history-repeats-1926)
9. SAFESEH
	* Real Application Attack
		* [FormatFactory 3.0.1](https://www.exploit-db.com/apps/396f6c052434dc8a386b8345be002bbc-FFSetup3.0.1.zip)

10. ROP(Return Oriented Programming)
	* [ROP(Return Oriented Programming)?](https://en.wikipedia.org/wiki/Return-oriented_programming)
	* [Practical Return Oriented Programming](https://trailofbits.files.wordpress.com/2010/04/practical-rop.pdf)
    * Flowing Going To ROP
    	* [RET Based](https://www.corelan.be/index.php/2010/06/16/exploit-writing-tutorial-part-10-chaining-dep-with-rop-the-rubikstm-cube/#directret)
    	* [SEH Based](https://www.corelan.be/index.php/2010/06/16/exploit-writing-tutorial-part-10-chaining-dep-with-rop-the-rubikstm-cube/#sehbased)
    * Real Application Attack
    	* RET Based ROP 
    		*  [VUPlayer 2.49](https://www.exploit-db.com/apps/39adeb7fa4711cd1cac8702fb163ded5-vuplayersetup.exe)
    		*  [vulnserver](https://github.com/stephenbradshaw/vulnserver)
    		*  [R 3.4.4](https://www.exploit-db.com/apps/a642a3de7b5c2602180e73f4c04b4fbd-R-3.4.4-win.exe)
    	* SEH Based ROP
    		*  [R 3.4.4](https://www.exploit-db.com/apps/a642a3de7b5c2602180e73f4c04b4fbd-R-3.4.4-win.exe)
    		*  [Quickzip 5.1.8.1](https://www.exploit-db.com/apps/1ef1b09b1167f6d5b18a9f2bbd540f28-quickzip_5.1.8.1.msi)
11. [Defeat Exploit Mitigations](https://exploit.courses/files/bfh2017/day5/0x52_DefeatExploitMitigations.pdf)
12. Heap Exploitation
	* [Heap Overflow](https://blog.rapid7.com/2019/06/12/heap-overflow-exploitation-on-windows-10-explained/)
13. EMET(Enhanced Mitigation Experience Toolkit) 5.2 / WDEG(Windows Defender Exploit Guard)
	* [EMET 5.2?](https://es.wikipedia.org/wiki/EMET)
	* [bypassing EMET](https://conference.hitb.org/hitbsecconf2017ams/materials/D1T4%20-%20Niels%20Warnars%20-%20Disarming%20EMET.pdf)
	* WDEG
		* [WDEG?](https://msrc-blog.microsoft.com/2017/08/09/moving-beyond-emet-ii-windows-defender-exploit-guard/)
		* [Mitigations for the Masses: From EMET to Windows Defender Exploit Guard](https://www.youtube.com/watch?v=Ays8GShgTQY)
