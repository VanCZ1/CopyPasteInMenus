# Copy Paste In menus

Adds copy-paste functionality to text boxes in menus

* [SSE/AE](https://www.nexusmods.com/skyrimspecialedition/mods/79975)
* [VR](https://www.nexusmods.com/skyrimspecialedition/mods/68032)

## Requirements
* [CMake](https://cmake.org/)
	* Add this to your `PATH`
* [PowerShell](https://github.com/PowerShell/PowerShell/releases/latest)
* [Vcpkg](https://github.com/microsoft/vcpkg)
	* Add the environment variable `VCPKG_ROOT` with the value as the path to the folder containing vcpkg
* [Visual Studio Community 2022](https://visualstudio.microsoft.com/)
	* Desktop development with C++
* [CommonLibSSE](https://github.com/powerof3/CommonLibSSE/tree/dev)
	* You need to build from the powerof3/dev branch
	* Add this as as an environment variable `CommonLibSSEPath`
* [CommonLibVR](https://github.com/alandtse/CommonLibVR/tree/vr)
	* Add this as as an environment variable `CommonLibVRPath` instead of /extern

## User Requirements
* [Address Library for SKSE](https://www.nexusmods.com/skyrimspecialedition/mods/32444)
	* Needed for SSE/AE
* [VR Address Library for SKSEVR](https://www.nexusmods.com/skyrimspecialedition/mods/58101)
	* Needed for VR

## Register Visual Studio as a Generator
* Open `x64 Native Tools Command Prompt`
* Run `cmake`
* Close the cmd window

## Building
```
git clone https://github.com/powerof3/CopyPasteInMenus.git
cd CopyPasteInMenus
git submodule update --init --recursive
```

### SSE (1.5.97)
```
cmake --preset vs2022-se
cmake --build --preset vs2022-se
```
### AE (1.6.1170+)
```
cmake --preset vs2022-ae
cmake --build --preset vs2022-ae
```
### VR
```
cmake --preset vs2022-vr
cmake --build --preset vs2022-vr
```

Replace `vs2022` with `vs2026` to build with Visual Studio 2026.

## License
[GPL-3.0](LICENSE)
