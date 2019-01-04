# Scanner
Scanner library for roblox

# namespace Scanner
- Process
- AOB
- Memory
- Console
- ReturnCheck

# Scanner::Process

DWORD GetPID(char* processName)

void Kill(const char *filename)

Usage:

- Scanner::Process::GetPID("RobloxPlayerBeta.exe") // Will return PID of process

- Scanner::Process::Kill("RobloxPlayerBeta.exe") // Kill proccess by filename

# Scanner::AOB

bool Check(const BYTE* pd, const BYTE* aob, const char* mask)

DWORD FindPattern(const char* aob, const char* mask)

Usage:

- Scanner::AOB::FindPattern("\xCC\xCC\xCC\xCC", "xxxx") // Return address from AOB

# Scanner::Memory

bool Compare(const char* pData, const char* bMask, const char* szMask)

DWORD Scan(const char* vftable)

Usage:

- Scanner::Memory::Scan((char*)&ScriptContextVFTable)

# Scanner::Console

void CreateConsole(const char *Name)

void CloseConsole()

Usage:
- Scanner::Console::CreateConsole("Title Name") // Create console with title

- Scanner::Console::CloseConsole() // Close current console

# Scanner::ReturnCheck

DWORD RemoveProtection(DWORD Address)

Usage:

- Scanner:ReturnCheck::RemoveProtection(ScanAddress(0x775444)) // Remove retcheck on address, and return DWORD
