---
UID: NF:dbghelp.SymSetHomeDirectory
title: SymSetHomeDirectory function (dbghelp.h)
description: Sets the home directory used by Dbghelp.
helpviewer_keywords: ["SymSetHomeDirectory","SymSetHomeDirectory function","SymSetHomeDirectoryW","base.symsethomedirectory","dbghelp/SymSetHomeDirectory","dbghelp/SymSetHomeDirectoryW"]
old-location: base\symsethomedirectory.htm
tech.root: Debug
ms.assetid: 12e65054-c4d5-44b9-8597-b841cac012f5
ms.date: 12/05/2018
ms.keywords: SymSetHomeDirectory, SymSetHomeDirectory function, SymSetHomeDirectoryW, base.symsethomedirectory, dbghelp/SymSetHomeDirectory, dbghelp/SymSetHomeDirectoryW
f1_keywords:
- dbghelp/SymSetHomeDirectory
dev_langs:
- c++
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSetHomeDirectoryW (Unicode) and SymSetHomeDirectory (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dbghelp.dll
api_name:
- SymSetHomeDirectory
- SymSetHomeDirectory
- SymSetHomeDirectoryW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.1 or later
ms.custom: 19H1
---

# SymSetHomeDirectory function


## -description


Sets the home directory used by Dbghelp.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param dir [in, optional]

The home directory. This directory must be writable, otherwise the home directory is the common application directory specified with [CSIDL_COMMON_APPDATA](/windows/win32/shell/csidl). If this parameter is <b>NULL</b>, the function uses the default directory.


## -returns



If the function succeeds, the return value is a pointer to the <i>dir</i> parameter.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The default home directory is the directory in which Dbghelp.dll resides. Dbghelp uses this directory as a basis for other directories, such as the default downstream store directory (the sym subdirectory of the home directory).

The home directory used for the default symbol store and the source server cache location is stored in the DBGHELP_HOMEDIR environment variable.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symgethomedirectory">SymGetHomeDirectory</a>
 

 

