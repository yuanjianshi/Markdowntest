## Description


This project includes a set of sample PowerShell scripts that utilize the Redfish API to manage Lenovo ThinkSystem servers using the Redfish API.

For more information on the Redfish API, visit http://redfish.dmtf.org/

## Requirements

* PowerShell 5.0 or above need to be installed. If you need update, please install Windows Management Framework accordingly. 

## Installing

* To install/update PowerShell:

Windows PowerShell comes installed by default starting with Windows 7. Windows 8 and Windows Server 2012 Installed PowerShell 3.0 by default.

Please use the following table to locate the installer for the version of PowerShell if you need update to follow the requirements.
.

| Windows                            | PS 3.0    | PS 4.0    | PS 5.0  | PS 5.1    |
| ---------------------------------- | --------- | --------- | ------- | --------- |
| Windows 10/Windows Server 2016     | -         | -         | -       | installed |
| Windows 8.1/Windows Server 2012 R2 | -         | installed | WMF 5.0 | WMF 5.1   |
| Windows 8/Windows Server 2012      | installed | WMF 4.0   | WMF 5.0 | WMF 5.1   |

Please download and install Windows Management Framework on Microsoft website according to your OS:

    https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6

## Usage

A set of PowerShell examples is provided under the examples directory of this project. 

For help message, please use:

```
Import-Module .\example_module_name.psm1
Get-help example_module_name
```

### Using the PowerShell examples to get and set values


Simply run the PowerShell script to print out the values from the HTTP GET request.

This example prints the current system power state (such as On or Off)

```
Import-Module ./ lenovo_get_power_state.psm1
lenovo_get_power_state.psm1
```

This example prints the system current power state, passes one of the values (ForceOff) to force the server to shutdown ,and then print reset types that are supported by this server if exception occurred.

```
Import-Module ./ lenovo_set_power_state.psm1
lenovo_set_power_state –reset_type ForceOff
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

* 08/16/2018 : Initial version

## Copyright and License

Copyright 2018 Lenovo Corporation

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
