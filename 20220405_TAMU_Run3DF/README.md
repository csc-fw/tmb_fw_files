# New features included:
   - Anode HMT: trigger and readout
   - New Run3 trigger data format, with Run2 pattern finder.  LCT0/1_CLCT_BEND is filled by run2 pattern id and LCT_CLCT_PAT_ID is not filled 
   - Partial Run3 DAQ data format: 
   - New firmware revision code 
      - format version[3:0]: 0x4, for TMB with Run3 data foramt + Run2 pattern finder
      - major versoin[3:0] : 0x0
      - minor version[4:0] : 0x1
      - if run3_daq_dataforamt_enable==0 and run2_revcode_enable==1, roll back to Run2 legacy revision code with firmware date 2016-04-14


## Updates compared to last version
Used register 0x1AA to control the Run3 data format:
   - run3_trigger_dataforamt_enable
   - run3_daq_dataforamt_enable
   - run3_alct_dataformat_enable
   - run2_revcode_enable

fixed the bug of missing MPC 

## Firmware date and type
The date is 2022-04-03 and it is the typeA TMB firmware
