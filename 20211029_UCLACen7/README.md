The TMB firmware is compiled from TMB_FW_2021_V0
https://github.com/tahuang1991/tmb_fw_code/tree/TMB_FW_2021_v0

the new features added to this TMB firmware on top of Run2 legacy version:
  - Run3 trigger data format
  - Run3 DAQ data format 
  - New registers and controls for above changes 

The new TMB firmware is still running the Run2 legacy pattern finder but converting the bending and strip position into the CCLUT convention: 4bits for bending value, 10bits for strip position, Run3 pattern id range from 0-4.  The bending value and Run3 pattern id is converted from Run2 pattern id.  The 1/4 strip bit is always 1 and 1/8 strip bit is always 0.  The Run3 trigger data format and Run3 DAQ data format for this new TMB firmware are the same for OTMB version with CSC only case.   

Revision code for new TMB firmware uses the Run3 convention for Run3 mode: 
  - format_version = 4'h5
  - major_version = 4'h0 if run3_daq_dataformat_enable=1, otherwise 4'h1 
  - minor_version = 4'h0


If run3_daq_dataformat_enable=0 and run2_revcode_enable=1, then revision code rolls back to Run2 legacy convention with firmware date 2016-04-14, namely 0xF08E
 
