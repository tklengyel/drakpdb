# drakpdb

## Installation

```
pip3 install -r requirements.txt
```

## Example

1. Get PDB name and GUID/Age using `vmi-win-guid`
   ```
   # vmi-win-guid name windows7-sp1
   Windows Kernel found @ 0x2610000
           Version: 64-bit Windows 7
           PE GUID: 4ce7951a5ea000
           PDB GUID: 3844dbb920174967be7aa4a2c20430fa2
           Kernel filename: ntkrnlmp.pdb
           ...
   ```

2. Download PDB and parse it to a json profile 
   ```
   python3 drakpdb.py fetch_pdb ntkrnlmp 3844dbb920174967be7aa4a2c20430fa2
   python3 drakpdb.py parse_pdb ntkrnlmp > ntkrnlmp.json
   ```
