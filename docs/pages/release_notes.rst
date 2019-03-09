Release Notes
=============

1.1.0
-----

* Implement #28: Add support to generate build tasks using the VSCode built-in command ``Tasks: Configure Task``.
* Fix #18: Save all files before build. (this is actually fixed because we are now using tasks)
* Add settings to test a generic launch script to start debugging.
* Implement #10: Create a launch task to start debugging using the Segger J-Link debugger using.
  settings configurations parameters.
* Fix #44: Perform a recursive search to find eww files in the workspace root folder.

1.0.0
-----

* Add __root to default defines
* Add keywords so the extension is easier to find in the marketplace
* Add listeners to the define settings so the cpptools config file is generated when changed
* Fix issue when cpptools config file is empty or invalid: plugin would not load
* Add some more settings for default c and c++ standard configuration
* Correct relative include paths in cpptools config file
* Add ``=`` sign to default defines in settings
* Add a problem matcher
* Redisgned the extension
* Instead of completely command drive, status bar items are added to configure most things
* Automatically monitor the selected ewp file and auto generate the config file
* Only generate one config file ``IAR`` in the ``c_cpp_properties.json`` file. Changing between projects/configurations will
  automatically trigger an update of the ``IAR`` config section in the json file.
* Move all settings from iar-vsc.json to the configuration file of vscode. This way configurations are reusable.
* Make extension platform aware so you can choose from all compilers from the selected workbench.
* Add new setting to define your own ``defines`` through the IAR settings. This way it is possible to define the intrinsics
  of your compiler so you do not have to wait for extension updates.
* Add command to open IAR workbench. For now only the workbench opens without a workspace. See Issue #24 @ GitHub.
* Extension is now loaded when the workspace contains ``.ewp`` files.
* Added basic unit- and integrationtests.
* Probably a lot more...

0.0.3
-----

* Fixes #1: Extension did not detect end of build command
* Fixes #3: Renamed iar-vsc.js to iar-vsc.json

0.0.2
-----

Add system include paths

0.0.1
-----

Initial release of iar-vsc
