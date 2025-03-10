---
UID: NF:psapi.GetProcessMemoryInfo
title: GetProcessMemoryInfo function (psapi.h)
description: Retrieves information about the memory usage of the specified process.
helpviewer_keywords: ["GetProcessMemoryInfo","GetProcessMemoryInfo function [PSAPI]","K32GetProcessMemoryInfo","_win32_getprocessmemoryinfo","base.getprocessmemoryinfo","psapi.getprocessmemoryinfo","psapi/GetProcessMemoryInfo","psapi/K32GetProcessMemoryInfo"]
old-location: psapi\getprocessmemoryinfo.htm
tech.root: psapi
ms.assetid: 12990e8d-6097-4502-824e-db6c3f76c715
ms.date: 12/05/2018
ms.keywords: GetProcessMemoryInfo, GetProcessMemoryInfo function [PSAPI], K32GetProcessMemoryInfo, _win32_getprocessmemoryinfo, base.getprocessmemoryinfo, psapi.getprocessmemoryinfo, psapi/GetProcessMemoryInfo, psapi/K32GetProcessMemoryInfo
f1_keywords:
- psapi/GetProcessMemoryInfo
dev_langs:
- c++
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- Psapi.dll
- Psapi.dll
- API-MS-Win-Core-PsAPI-L1-1-0.dll
- KernelBase.dll
api_name:
- GetProcessMemoryInfo
- K32GetProcessMemoryInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetProcessMemoryInfo function


## -description


Retrieves information about the memory usage of the specified process.


## -parameters




### -param Process [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right and the <b>PROCESS_VM_READ</b> access right. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights.


### -param ppsmemCounters [out]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/psapi/ns-psapi-process_memory_counters">PROCESS_MEMORY_COUNTERS</a> or <a href="https://docs.microsoft.com/windows/desktop/api/psapi/ns-psapi-process_memory_counters_ex">PROCESS_MEMORY_COUNTERS_EX</a> structure that receives information about the memory usage of the process.


### -param cb [in]

The size of the 
<i>ppsmemCounters</i> structure, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetProcessMemoryInfo</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetProcessMemoryInfo</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetProcessMemoryInfo</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetProcessMemoryInfo</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/psapi/collecting-memory-usage-information-for-a-process">Collecting Memory Usage Information for a Process</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>



<a href="https://docs.microsoft.com/windows/desktop/api/psapi/ns-psapi-process_memory_counters">PROCESS_MEMORY_COUNTERS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/psapi/ns-psapi-process_memory_counters_ex">PROCESS_MEMORY_COUNTERS_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/psapi/process-memory-usage-information">Process Memory Usage Information</a>
 

 

