OSVVM Documentation
######################

OSVVM is an advanced verification methodology that
defines a VHDL verification framework, verification utility library, 
verification component library, and a scripting flow
that simplifies your FPGA or ASIC verification project 
from start to finish.
Using these libraries you can create a simple, readable, and 
powerful testbench that is suitable for either a simple FPGA block
or a complex ASIC.

OSVVM is developed by the same VHDL experts who
have helped develop VHDL standards.
We have used our expert VHDL skills to create
advanced verification capabilities that:

* Are simple to use and work like built-in language features.
* Maximize reuse and reduce project schedule.
* Facilitate readabilty and reviewability by the whole team including software and system engineers.
* Facilitate debug with HTML based test suite and test case reporting.
* Provide continuous integration (CI/CD) support with JUnit XML test suite reporting.
* Provide buzz word features including Constrained Random, Functional Coverage, Scoreboards, FIFOs, Memory Models, error logging and reporting, and message filtering.
* Rival the verification capabilities of SystemVerilog + UVM.


Run The Demos
=====================================

A great way to get oriented with OSVVM is to run the demos.
For directions on running the demos, see `OSVVM Scripts <https://github.com/osvvm/OSVVM-Scripts#readme>`_.

OSVVM Framework
=====================================
Some methodologies (or frameworks) are so complex that you need a script to create initial starting point for writing verification components, test cases, and/or the test harness. SystemVerilog + UVM is certainly like this. There are even several organizations that propose that you use their “Lite” or “Easy” approach.

OSVVM is simple enough to use on small blocks and powerful enough to use on large, complex chips or systems. This allows us to use the same style of framework for RTL, Core, and Chip level verification - which in turn facilitates re-use of verification components and test cases. OSVVM has added the abstractions needed to make our verification component based approach as easy as the “Lite” approach of other methodologies.

SynthWorks has been using this framework for 25+ years in our training classes and consulting work. During that time, we have innovated new capabilities and evolved our existing ones to increase re-use and reduce effort spent.

When we examine OSVVM’s framework in detail, we see that it has many similar elements to SystemVerilog + UVM. However, one thing not present is OO language constructs. Instead OSVVM uses ordinary VHDL constructs, such as structural and behavioral code. This makes it readily accessible to both verfication and RTL engineers.

Complete documentation on OSVVM's Framework is here

.. list-table:: 
    :widths: 40 10  
    :header-rows: 1
    
    * - Document Name
      - Link
    * - OSVVM Overview (HTML)
      - `osvvm.github.io <https://osvvm.github.io>`_
    * - OSVVM Overview (PDF)
      - `OSVVM_Overiew.pdf <https://github.com/OSVVM/Documentation/blob/main/OSVVM_Overiew.pdf>`_
    * - OSVVM's Structured Testbench Framework
      - `OSVVM_structured_testbench_framework.pdf <https://github.com/OSVVM/Documentation/blob/main/OSVVM_structured_testbench_framework.pdf>`_
    * - OSVVM's Verification Component Developer's Guide
      - `OSVVM_verification_component_developers_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/OSVVM_verification_component_developers_guide.pdf>`_
    * - OSVVM's Test Writers User Guide
      - `OSVVM_test_writers_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/OSVVM_test_writers_user_guide.pdf>`_
    * - OSVVM's Address Bus Model Independent Transactions Users Guide
      - `Address_Bus_Model_Independent_Transactions_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Address_Bus_Model_Independent_Transactions_user_guide.pdf>`_
    * - OSVVM's Stream Model Independent Transactions Users Guide
      - `Stream_Model_Independent_Transactions_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Stream_Model_Independent_Transactions_user_guide.pdf>`_


OSVVM Script Environment
=====================================
The goal of OSVVM's scripting is to have 
"One Script to Run them All" - where all is any simulator.

Current supported simulators are

* GHDL (Free Open Source simulator),
* Aldec's Active-HDL and Riviera-PRO, 
* Siemen's ModelSim and QuestaSim, 
* Synopsys' VCS, and
* Cadence's Xcelium.

OSVVM scripts are a TCL based API layer that provides a 
tool independent means to simulate (and perhaps in the 
future synthesize) your design. 
The API uses TCL procedures to create the abstraction 
layers – which is why they have the extension .pro. 

The scripts are executable TCL, so the full power of TCL 
can be used when needed (such as is in osvvm.pro).

Going Further
----------------------------------------------------

.. list-table:: 
    :widths: 40 10  

    * - Document Name
      - Link
    * - Script User Guide (pdf)
      - `Script_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Script_user_guide.pdf>`_
    * - Script User Guide (HTML)  
      - `README.rst <https://github.com/OSVVM/OSVVM-Scripts#readme>`_
    * - Script Repository  
      - `Repository <https://github.com/OSVVM/OSVVM-Scripts>`_


AXI4, AXI4Lite, AxiStream Library
=====================================

* `OSVVM AXI4 Lite, Full, and Stream Verification Components (repository) <https://github.com/OSVVM/AXI4>`_
*  `Axi4 Verification Components User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/Axi4_VC_user_guide.pdf>`_
*  `AxiStream Verification Components User Guide (pdf) <https://github.com/OSVVM/Documentation/blob/master/AxiStream_user_guide.pdf>`_
*  Based on an older revision:  `Creating an AXI4 Lite, Transaction Based VHDL Testbench with OSVVM (webinar) <https://www.aldec.com/en/support/resources/multimedia/webinars/2083>`_


UART Library
=====================================

Currently the best way to learn about the UART Transmitter and
Receiver verification components is to run the testbenches.
For directions on how to do this see the OSVVM Script Environment
documentation.

* `OSVVM UART Verification Components (repository) <https://github.com/OSVVM/UART>`_
* `Script User Guide (at bottom of page) <https://github.com/OSVVM/OSVVM-Scripts>`_


OSVVM Verification Utility Library
=====================================

The :gh:`OSVVM Utility Library <osvvm>` implements the advanced verification
capabilities found in other verification languages (such as 
SystemVerilog and UVM) as packages.  The list below lists
out many of the OSVVM features and the package in which they are 
implemented.

* Constrained Random test generation (RandomPkg)
* Functional Coverage with hooks for UCIS coverage database integration (CoveragePkg)
* Intelligent Coverage Random test generation  (CoveragePkg)
* Utilities for testbench process synchronization generation (TbUtilPkg)
* Utilities for clock and reset generation (TbUtilPkg)
* Transcript files (TranscriptPkg)
* Error logging and reporting - Alerts and Affirmations (AlertLogPkg)
* Message filtering - Logs (AlertLogPkg)
* Scoreboards and FIFOs (data structures for verification) (ScoreboardGenericPkg)
* HTML and JUnit XML test reporting (ReportPkg, AlertLogPkg, CoveragePkg, ScoreboardGenericPkg)
* Memory models (MemoryPkg)
* Transaction-Level Modeling Support (TbUtilPkg, ResolutionPkg)

Through the years, the packages have been updated many times.
Now, all of the packages that create data structures
(AlertLogPkg, CoveragePkg, ScoreboardGenericPkg, and MemoryPkg) 
use singleton data structures.
Usage of singletons simplifies API to an ordinary 
call interface - ie: no more shared variables and 
protected types.


Going Further
----------------------------------------------------
Read the following documents for more information on
OSVVM's VHDL Utility Library.

.. list-table:: 
    :widths: 20 30 30  
    :header-rows: 1
    
    * - Document
      - User Guide
      - Quick Reference      
    * - AlertLogPkg
      - `AlertLogPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/AlertLogPkg_user_guide.pdf>`_
      - `AlertLogPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/AlertLogPkg_quickref.pdf>`_
    * - CoveragePkg
      - `CoveragePkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/CoveragePkg_user_guide.pdf>`_
      - `CoveragePkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/CoveragePkg_quickref.pdf>`_
    * - RandomPkg
      - `RandomPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/RandomPkg_user_guide.pdf>`_
      - `RandomPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/RandomPkg_quickref.pdf>`_
    * - ScoreboardPkg
      - `ScoreboardPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/ScoreboardPkg_user_guide.pdf>`_
      - `ScoreboardPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/ScoreboardPkg_quickref.pdf>`_
    * - MemoryPkg
      - `MemoryPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/MemoryPkg_user_guide.pdf>`_
      - None
    * - TbUtilPkg
      - `TbUtilPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_user_guide.pdf>`_
      - `TbUtilPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_quickref.pdf>`_
    * - TbUtilPkg
      - `TbUtilPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_user_guide.pdf>`_
      - `TbUtilPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/TbUtilPkg_quickref.pdf>`_
    * - TranscriptPkg
      - `TranscriptPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/TranscriptPkg_user_guide.pdf>`_
      - `TranscriptPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/master/TranscriptPkg_quickref.pdf>`_
    * - TextUtilPkg
      - `TextUtilPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/master/TextUtilPkg_user_guide.pdf>`_
      - None
      


Model Independent Transactions
=====================================

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
==============================================
The fastest way to get started with OSVVM is 
`SynthWorks' Advanced VHDL Testbenches and Verification <https://synthworks.com/vhdl_testbench_verification.htm>`_
which is available world wide either on-line or on-site (once we can travel again).  
   
`Here is our current class schedule. <https://synthworks.com/public_vhdl_courses.htm#VHDL_Test_Bench_Training>`_


A Quick Note About Copyrights
=====================================

The documentation is copyrighted for reference 
type usage in any setting.  
Feel free to print and distribute (email) these materials.
However, derivatives of this material are 
forbidden without written permission.  
A derivative would be translating the 
documentation to slides, other documents, or webpages.  

Why? - SynthWorks, the primary developer of OSVVM
and OSVVM documentation, provides training.
We cannot allow other training providers to use 
our documentation to write their training materials,
websites, or documents - this is commercial usage
and is not in any way fair use.  

This only means that if you want to write a 
class on OSVVM, you must develop your own examples. 
Alternately you could talk to SynthWorks about 
licensing their materials.   


