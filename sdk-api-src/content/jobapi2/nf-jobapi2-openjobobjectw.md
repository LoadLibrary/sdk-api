---
UID: NF:jobapi2.OpenJobObjectW
title: OpenJobObjectW function (jobapi2.h)
description: Opens an existing job object.
helpviewer_keywords: ["OpenJobObject","OpenJobObject function","OpenJobObjectA","OpenJobObjectW","_win32_openjobobject","base.openjobobject","winbase/OpenJobObject","winbase/OpenJobObjectA","winbase/OpenJobObjectW"]
old-location: base\openjobobject.htm
tech.root: ProcThread
ms.assetid: cb6ebc6f-5c61-408d-a781-ba029c83ddeb
ms.date: 12/05/2018
ms.keywords: OpenJobObject, OpenJobObject function, OpenJobObjectA, OpenJobObjectW, _win32_openjobobject, base.openjobobject, winbase/OpenJobObject, winbase/OpenJobObjectA, winbase/OpenJobObjectW
f1_keywords:
- jobapi2/OpenJobObject
dev_langs:
- c++
req.header: jobapi2.h
req.include-header: Windows.h, Jobapi2.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenJobObjectW (Unicode) and OpenJobObjectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-job-l2-1-0.dll
- kernel32legacy.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Job-L2-1-1.dll
api_name:
- OpenJobObject
- OpenJobObjectA
- OpenJobObjectW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenJobObjectW function


## -description


Opens an existing job object.


## -parameters




### -param dwDesiredAccess [in]

The access to the job object. This parameter can be one or more of the 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/job-object-security-and-access-rights">job object access rights</a>. This access right is checked against any security descriptor for the object.


### -param bInheritHandle [in]

If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param lpName [in]

The name of the job to be opened. Name comparisons are case sensitive.

This function can open objects in a private namespace. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the job. The handle provides the requested access to the job.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To associate a process with a job, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-assignprocesstojobobject">AssignProcessToJobObject</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-assignprocesstojobobject">AssignProcessToJobObject</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/job-objects">Job Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

