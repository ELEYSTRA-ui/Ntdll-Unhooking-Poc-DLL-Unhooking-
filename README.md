# Ntdll-Unhooking-Poc-DLL-Unhooking-
A C++ Proof of Concept demonstrating classic ntdll.dll unhooking by mapping a fresh copy from disk.


# Classic Ntdll Unhooking

A simple C++ PoC demonstrating how to restore the `.text` section of `ntdll.dll` by mapping a clean copy from disk to remove user-mode hooks.

## How It Works
1. Gets handle to the loaded `ntdll.dll`.
2. Maps a fresh copy of `ntdll.dll` directly from `C:\Windows\System32\ntdll.dll`.
3. Changes `.text` section memory protection (`PAGE_EXECUTE_READWRITE`).
4. Overwrites the in-memory `.text` section with the clean copy from disk.
5. Restores original memory protections and cleans up handles.

## Build
* Requirements: Windows, Visual Studio (MSVC)
* Target Architecture: x64 recommended

## Disclaimer
This project is for educational and security research purposes only.

## License
MIT
