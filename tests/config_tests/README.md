### Use test configuration
Copy files from ../../_mock_salt_pkg_windows/* to the github/salt repo

### Edit a `*.test` file
- Contains the msi-properties, of which master and minion_id simulate user input via the GUI
- May contain the `dormant` keyword, which means the configuration remains (dormant) after uninstall
- Without the `dormant` keyword, no configuaration must exist after uninstall

### Optionally edit a `*.minion_id` file
- Contains prior configuration by conf/minion_id file
- Omit this file if there is no prior conf/minion_id configuration  

### Optionally edit a `*.input` file
- Contains prior configuration by conf/minion file
- Omit this file if there is no  prior conf/minion configuration  

### Edit a `*.expected` file
- Contains the expected configuration (after install). Any difference will result in failure.
- If the test fails, the resulting configuration will be stored as *.output  

### Run `test.cmd`
- Will generate and run *-install.bat and  *-uninstall.bat files for each *.test file
