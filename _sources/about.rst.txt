About OSVVM
###########

Open Source VHDL Verification Methodology (OSVVM) provides
utility and verification component libraries that simplify
your FPGA and ASIC verification tasks.
Using these libraries you can create a simple, readable, and
powerful testbench that is suitable for the entire verification
process from simple RTL blocks, to Cores, and to an entire Chip.


Getting Started With OSVVM
==========================

To understand the basics of using OSVVM for verification, see:

*  `Creating Better Self-Checking FPGA Verification Tests with Open Source VHDL Verification Methodology (OSVVM) (webinar) <https://www.aldec.com/en/support/resources/multimedia/webinars/2094>`_
*  `OSVVM Test Writers User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/OSVVM_test_writers_user_guide.pdf>`_

To understand how to use OSVVM Verification Components, see:

*  `Axi4 Verification Components User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/Axi4_VC_user_guide.pdf>`_
*  `AxiStream Verification Components User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/AxiStream_user_guide.pdf>`_
*  Based on an older revision:  `Creating an AXI4 Lite, Transaction Based VHDL Testbench with OSVVM (webinar) <https://www.aldec.com/en/support/resources/multimedia/webinars/2083>`_


OSVVM Script Environment
========================

The OSVVM Script Library creates a scripting
environment that is independent of the simulator
that is running.
Hence, one script can run the simulation on any simulator.
Currently the scripting environment is TCL based.
It uses procedures to do common simulation tasks.
While any tcl can be used within OSVVM scripts,
it would be best to try to limit this as our long
term plan is to also create a bash version of the
script environment.
If you need to use TCL commands, please let us know
what so we can plan how to adapt for the bash version.

* `OSVVM Script library (repository) <https://github.com/OSVVM/OSVVM-Scripts>`_
* `Script User Guide (at bottom of page) <https://github.com/OSVVM/OSVVM-Scripts>`_
* `Script User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/Script_user_guide.pdf>`_


AXI4, AXI4Lite, AxiStream Library
=================================

* `OSVVM AXI4 Lite, Full, and Stream Verification Components (repository) <https://github.com/OSVVM/AXI4>`_
*  `Axi4 Verification Components User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/Axi4_VC_user_guide.pdf>`_
*  `AxiStream Verification Components User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/AxiStream_user_guide.pdf>`_
*  Based on an older revision:  `Creating an AXI4 Lite, Transaction Based VHDL Testbench with OSVVM (webinar) <https://www.aldec.com/en/support/resources/multimedia/webinars/2083>`_


UART Library
============

Currently the best way to learn about the UART Transmitter and
Receiver verification components is to run the testbenches.
For directions on how to do this see the OSVVM Script Environment
documentation.

* `OSVVM UART Verification Components (repository) <https://github.com/OSVVM/UART>`_
* `Script User Guide (at bottom of page) <https://github.com/OSVVM/OSVVM-Scripts>`_


OSVVM Utility Library
=====================

* `OSVVM Utility library (repository) <https://github.com/OSVVM/OSVVM>`_
   * AlertLogPkg
      * `AlertLogPkg User Guide  (pdf) <https://github.com/OSVVM/Documentation/blob/master/AlertLogPkg_user_guide.pdf>`_
      * `AlertLogPkg Quick Reference  (pdf) <https://github.com/OSVVM/Documentation/blob/master/AlertLogPkg_quickref.pdf>`_
   * CoveragePkg
      * `CoveragePkg User Guide  (pdf) <https://github.com/OSVVM/Documentation/blob/master/CoveragePkg_user_guide.pdf>`_
      * `CoveragePkg Quick Reference (pdf) <https://github.com/OSVVM/Documentation/blob/master/CoveragePkg_quickref.pdf>`_
   * RandomPkg
      * `RandomPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/RandomPkg_user_guide.pdf>`_
      * `RandomPkg Quick Reference (pdf) <https://github.com/OSVVM/Documentation/blob/master/RandomPkg_quickref.pdf>`_
   * ScoreboardPkg
      * `ScoreboardPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/ScoreboardPkg_user_guide.pdf>`_
      * `ScoreboardPkg Quick Reference (pdf) <https://github.com/OSVVM/Documentation/blob/master/ScoreboardPkg_quickref.pdf>`_
   * MemoryPkg
      * `MemoryPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/MemoryPkg_user_guide.pdf>`_
   * TbUtilPkg
      * `TbUtilPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_user_guide.pdf>`_
      * `TbUtilPkg Quick Reference (pdf) <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_quickref.pdf>`_
   * TbUtilPkg
      * `TbUtilPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_user_guide.pdf>`_
      * `TbUtilPkg Quick Reference (pdf) <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_quickref.pdf>`_
   * TranscriptPkg
      * `TranscriptPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/TranscriptPkg_user_guide.pdf>`_
      * `TranscriptPkg Quick Reference (pdf) <https://github.com/OSVVM/Documentation/blob/master/TranscriptPkg_quickref.pdf>`_
   * TextUtilPkg
      * `TextUtilPkg User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/TextUtilPkg_user_guide.pdf>`_


Model Independent Transactions
==============================

All OSVVM Streaming and Address Bus Interfaces use the
Model Independent Transaction packages from this repository.
These packages establish the pattern for transactions that
each verification component should consider supporting.
Not all verification components will support all
transactions - however, they should list which ones
they do support in their user guide.

* `OSVVM Verification Component Common library (repository) <https://github.com/OSVVM/OSVVM-Common>`_
*  `Address Bus Model Independent Transactions User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/Address_Bus_Model_Independent_Transactions_user_guide.pdf>`_
*  `Stream Model Independent Transactions User Guide (pdf) <Stream_Model_Independent_Transactions_user_guide.pdf>`_


Training:  The Quick Path to Learning OSVVM
===========================================
The fastest way to get started with OSVVM is
`SynthWorks' Advanced VHDL Testbenches and Verification <https://synthworks.com/vhdl_testbench_verification.htm>`_
which is available world wide either on-line or on-site (once we can travel again).

`Here is our current class schedule. <https://synthworks.com/public_vhdl_courses.htm#VHDL_Test_Bench_Training>`_


A Quick Note About Copyrights
=============================

The documentation is copyrighted for reference type usage in any setting.
Feel free to print and distribute (email) these materials.
However, derivatives of this material are forbidden without written permission.
A derivative would be translating the documentation to slides, other documents, or webpages.

Why? - SynthWorks, the primary developer of OSVVM and OSVVM documentation, provides training.
We cannot allow other training providers to use our documentation to write their training materials, websites, or
documents - this is commercial usage and is not in any way fair use.

This only means that if you want to write a class on OSVVM, you must develop your own examples.
Alternately you could talk to SynthWorks about licensing their materials.
