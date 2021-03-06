# XInputApplicationLauncher
Launch Programs and control the mouse using an XInput controller

#### Building:
XInputAppplicationLauncher is was developed in VS2017 using .NET 4.7. 
The [SharpDX](http://sharpdx.org/) wrapper was used to read from the XInput controller. This will be downloaded via NuGet during the build.

#### Usage:
- Guide Button: Show Application
- Menu Button: Show Menu
- D-Pad Up/Down, Left Stick: Scroll / Move Mouse (When Mouse Control is active)
- A: Select / Left Mouse Click (When Mouse Control is active)
- B: Hide Application
- X: Toggle Mouse Control
- Y: Close Highlighted Application

#### Adding Applications to Launcher:
Add programs to the launcher in ProgramList.xml, e.g:
```xml
  <Program>
    <Name>Steam</Name>
    <Path><![CDATA[C:\Program Files (x86)\Steam\Steam.exe]]></Path>
    <Argument><![CDATA[steam://open/bigpicture]]></Argument>
  </Program>
```
ProgramList.xml Schema
- Name: Name to display in launcher (required)
- Path: Path to executable (required)
- Argument: Addition arguments (not required, can be used multiple times)

The program icon will be read from the specified executable.
