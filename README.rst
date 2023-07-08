OSVVM Documentation
######################

OSVVM is an advanced verification methodology that 
defines a VHDL verification framework, verification utility library, 
verification component library, scripting API, and co-simulation capability 
that simplifies your FPGA or ASIC verification project from start to finish. 
Using these libraries you can create a simple, readable, 
and powerful testbench that will boost productivity for either 
low level block tests (unit tests) or complex FPGA and ASIC tests.

OSVVM is developed by the same VHDL experts who
have helped develop VHDL standards.
We have used our expert VHDL skills to create
advanced verification capabilities that:  

- A structured transaction-based framework using verification components that is suitable for all verification tasks - from Unit/RTL to full chip/system level testing.
- Test cases and verification components that can be written any VHDL Engineer.
- Test cases that are readable and reviewable by the whole team including software and system engineers.   
- Unmatched reuse through the entire verification process.    
- Unmatched test reporting with HTML based test suite reports, test case reports, and logs that facilitate debug and test artifact collection.   
- Support for continuous integration (CI/CD) with JUnit XML test suite reporting.  
- Powerful and concise verification capabilities including Constrained Random, Functional Coverage, Scoreboards, FIFOs, Memory Models, error logging and reporting, and message filtering that are simple to use and work like built-in language features.
- A common scripting API to run all simulators - including GHDL, NVC, Aldec Riviera-PRO and ActiveHDL, Siemens Questa and ModelSim, Synopsys VCS, and Cadence Xcelium.  
- A Co-simulation capability that supports running software (C++) in a hardware simulation environment.
- A Model Independent Transaction (MIT) library that defines a transaction API (procedures such as read, write, send, get, …)  and transaction interface (a record) that simplifies writing verification components and test cases.
- A rival to the verification capabilities of SystemVerilog + UVM.  


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

Documents related to OSVVM Framework
----------------------------------------------------

.. list-table:: 
    :widths: 40 10  
    :header-rows: 1
    
    * - Document Name
      - Link
    * - OSVVM Overview (HTML)
      - `osvvm.github.io <https://osvvm.github.io>`_
    * - OSVVM Overview (PDF)
      - `OSVVM_Overview.pdf <https://github.com/OSVVM/Documentation/blob/main/OSVVM_Overview.pdf>`_
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

.. list-table:: 
    :widths: 30 20  
    :header-rows: 1
    
    * - Publications and Webinars
      - Event
    * - `OSVVM Leading Edge Verification for the VHDL Community <https://www.aldec.com/en/support/resources/multimedia/webinars/2186>`_
      - Part 1 of Better FPGA Verification with VHDL, With Aldec May 2022 
    * - `Faster than Lite Verification Component Development with OSVVM <https://www.aldec.com/en/support/resources/multimedia/webinars/2187>`_
      - Part 2 of Better FPGA Verification with VHDL, With Aldec June 2022 
    * - `OSVVM's Test Reports and Simulator Independent Scripting <https://www.aldec.com/en/support/resources/multimedia/webinars/2188>`_
      - Part 3 of Better FPGA Verification with VHDL, With Aldec June 2022 
    * - `Advances in OSVVM's Verification Data Structures <https://www.aldec.com/en/support/resources/multimedia/webinars/2190>`_
      - Part 4 of Better FPGA Verification with VHDL, With Aldec June 2022 
    * - `OSVVM: Leading Edge Verification for the VHDL Community <https://www.youtube.com/watch?v=KVmGDy_PHNI>`_
      - DVClub Europe April 2022 


OSVVM Script Environment
=====================================
The goal of OSVVM's scripting is to have 
"One Script to Run them All" - where all is any simulator.

Current supported simulators are

* NVC (Free Open Source simulator),
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

Documents related to OSVVM Scripting
----------------------------------------------------

.. list-table:: 
    :widths: 40 10  

    * - Document Name
      - Link
    * - Script User Guide (pdf)
      - `Script_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Script_user_guide.pdf>`_
    * - Script User Guide (HTML)  
      - `README.rst <https://github.com/OSVVM/OSVVM-Scripts#readme>`_
    * - OSVVM Scripts Repository  
      - `Repository <https://github.com/OSVVM/OSVVM-Scripts>`_



OSVVM Verification Utility Library
=====================================

The `OSVVM Utility Library <https://github.com/osvvm/osvvm>`_ implements the advanced verification
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


Documents related to OSVVM Verification Utility Library
-----------------------------------------------------------------

.. list-table:: 
    :widths: 20 30 30  
    :header-rows: 1
    
    * - Document
      - User Guide
      - Quick Reference      
    * - AlertLogPkg
      - `AlertLogPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/AlertLogPkg_user_guide.pdf>`_
      - `AlertLogPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/main/AlertLogPkg_quickref.pdf>`_
    * - CoveragePkg
      - `CoveragePkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/CoveragePkg_user_guide.pdf>`_
      - `CoveragePkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/main/CoveragePkg_quickref.pdf>`_
    * - RandomPkg
      - `RandomPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/RandomPkg_user_guide.pdf>`_
      - `RandomPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/main/RandomPkg_quickref.pdf>`_
    * - ScoreboardGenericPkg
      - `ScoreboardPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/ScoreboardPkg_user_guide.pdf>`_
      - `ScoreboardPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/main/ScoreboardPkg_quickref.pdf>`_
    * - MemoryPkg
      - `MemoryPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/MemoryPkg_user_guide.pdf>`_
      - None
    * - TbUtilPkg
      - `TbUtilPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/TbUtilPkg_user_guide.pdf>`_
      - `TbUtilPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/main/TbUtilPkg_quickref.pdf>`_
    * - TranscriptPkg
      - `TranscriptPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/TranscriptPkg_user_guide.pdf>`_
      - `TranscriptPkg_quickref.pdf <https://github.com/OSVVM/Documentation/blob/main/TranscriptPkg_quickref.pdf>`_
    * - ResolutionPkg
      - `ResolutionPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/ResolutionPkg_user_guide.pdf>`_
      - None
    * - TextUtilPkg
      - `TextUtilPkg_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/TextUtilPkg_user_guide.pdf>`_
      - None

.. list-table:: 
    :widths: 30 20  
    :header-rows: 1
    
    * - Publications and Webinars
      - Event
    * - `OSVVM Leading Edge Verification for the VHDL Community <https://www.aldec.com/en/support/resources/multimedia/webinars/2186>`_
      - Part 1 of Better FPGA Verification with VHDL, With Aldec May 2022 
    * - `Faster than Lite Verification Component Development with OSVVM <https://www.aldec.com/en/support/resources/multimedia/webinars/2187>`_
      - Part 2 of Better FPGA Verification with VHDL, With Aldec June 2022 
    * - `OSVVM's Test Reports and Simulator Independent Scripting <https://www.aldec.com/en/support/resources/multimedia/webinars/2188>`_
      - Part 3 of Better FPGA Verification with VHDL, With Aldec June 2022 
    * - `Advances in OSVVM's Verification Data Structures <https://www.aldec.com/en/support/resources/multimedia/webinars/2190>`_
      - Part 4 of Better FPGA Verification with VHDL, With Aldec June 2022 
    * - `OSVVM: Leading Edge Verification for the VHDL Community <https://www.youtube.com/watch?v=KVmGDy_PHNI>`_
      - DVClub Europe April 2022 

Model Independent Transactions
=====================================
All OSVVM verification components use the OSVVM 
Model Independent Transaction for Streaming and Address Bus Interfaces.
These packages are our internal standard for the 
transaction interface and transaction API. 
Not all verification components will support all 
transactions - however, they should list which ones
they do support in their user guide.

Documents related to OSVVM Model Independent Transactions
-----------------------------------------------------------------------

.. list-table:: 
    :widths: 30 30  
    :header-rows: 1
    
    * - Document Name
      - Link
    * - Address Bus Model Independent Transactions User Guide
      - `Address_Bus_Model_Independent_Transactions_user_guide.pdf  <https://github.com/OSVVM/Documentation/blob/main/Address_Bus_Model_Independent_Transactions_user_guide.pdf>`_
    * - Stream Model Independent Transactions User Guide 
      - `Stream_Model_Independent_Transactions_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Stream_Model_Independent_Transactions_user_guide.pdf>`_
    * - OSVVM Verification Component Common library (repository) 
      - `OSVVM Common <https://github.com/OSVVM/OSVVM-Common>`_


OSVVM Verification Component Library
===========================================
OSVVM's growing verification component library 
is tabulated below.  

.. list-table:: 
    :widths: 40 10 10
    :header-rows: 1
    
    * - Verification Component(s)
      - User Guide
      - Repository
    * - Axi4 Full (Manager, Memory, and Subordinate) VCs
      - `Axi4_VC_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Axi4_VC_user_guide.pdf>`_
      - `AXI4  <https://github.com/OSVVM/AXI4>`_
    * - Axi4 Lite (Manager, Memory, and Subordinate) VCs
      - `Axi4_VC_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/Axi4_VC_user_guide.pdf>`_
      - `AXI4  <https://github.com/OSVVM/AXI4>`_
    * - AxiStream Transmitter and Receiver VCs
      - `AxiStream_user_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/AxiStream_user_guide.pdf>`_
      - `AXI4  <https://github.com/OSVVM/AXI4>`_
    * - UART Transmitter and Receiver VCs
      - None
      - `UART  <https://github.com/OSVVM/UART>`_
    * - DpRam behavioral model and DpRam controller
      - `OSVVM_verification_component_developers_guide.pdf <https://github.com/OSVVM/Documentation/blob/main/OSVVM_verification_component_developers_guide.pdf>`_
      - `DpRam  <https://github.com/OSVVM/DpRam>`_

Note all of the OSVVM verification components use the model independent 
transaction interfaces which are defined in `OSVVM Common <https://github.com/OSVVM/OSVVM-Common>`_. 
It is required to be in the directory `OsvvmLibraries/Common`.


Co-simulation
=====================================
OSVVM co-simulation supports running software (C++) in a hardware simulation environment.  
This includes either writing tests cases in C++ or running C++ models such as instruction set simulators.

Documents related to Co-simulation
-----------------------------------------------------------------------

.. list-table:: 
    :widths: 30 30  
    :header-rows: 1
    
    * - Document Name
      - Link
    * - OSVVM's Co-simulation Framework
      - `OSVVM_cosimulation_framework.pdf  <https://github.com/OSVVM/Documentation/blob/main/OSVVM_cosimulation_framework.pdf>`_



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


