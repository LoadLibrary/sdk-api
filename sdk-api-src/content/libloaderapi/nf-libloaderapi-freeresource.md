---
UID: NF:libloaderapi.FreeResource
title: FreeResource function (libloaderapi.h)
description: Decrements (decreases by one) the reference count of a loaded resource. When the reference count reaches zero, the memory occupied by the resource is freed.
helpviewer_keywords: ["FreeResource","FreeResource function [Menus and Other Resources]","_win32_FreeResource","_win32_freeresource_cpp","libloaderapi/FreeResource","menurc.freeresource","winui._win32_freeresource"]
old-location: menurc\freeresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\freeresource.htm
ms.date: 12/05/2018
ms.keywords: FreeResource, FreeResource function [Menus and Other Resources], _win32_FreeResource, _win32_freeresource_cpp, libloaderapi/FreeResource, menurc.freeresource, winui._win32_freeresource
f1_keywords:
- libloaderapi/FreeResource
dev_langs:
- c++
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
- API-MS-Win-Core-LibraryLoader-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-LibraryLoader-l1-1-1.dll
- API-MS-Win-Core-LibraryLoader-l1-2-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-Libraryloader-l1-2-1.dll
- API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
- FreeResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FreeResource function


## -description


<p class="CCE_Message">[This  function is obsolete and is only supported for backward compatibility with 16-bit Windows. For 32-bit Windows applications, it is not necessary to free the resources loaded using <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>. If used on 32 or 64-bit Windows systems, this function will return <b>FALSE</b>.]

Decrements (decreases by one) the reference count of a loaded resource. When the reference count reaches zero, the memory occupied by the resource is freed.


## -parameters




### -param hResData

TBD




#### - hglbResource [in]

Type: <b>HGLOBAL</b>

A handle of the resource. It is assumed that <i>hglbResource</i> was created by <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is zero.

If the function fails, the return value is nonzero, which indicates that the resource has not been freed.




## -remarks



For resources loaded with other functions, <b>FreeResource</b> has been replaced by the following functions:

<table class="clsStd">
<tr>
<th>Resource type</th>
<th>FreeResource replacement</th>
</tr>
<tr>
<td>Accelerator</td>
<td>
<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>
</td>
</tr>
<tr>
<td>Bitmap</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>
</td>
</tr>
<tr>
<td>Cursor</td>
<td>
<a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a>
</td>
</tr>
<tr>
<td>Icon</td>
<td>
<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>
</td>
</tr>
<tr>
<td>Menu</td>
<td>
<a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a>
</td>
</tr>
</table>
 

The reference count for a resource is incremented (increased by one) each time an application calls the <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> function for the resource.

The system automatically deletes these resources when the process that created them terminates. However, calling the appropriate function saves memory.  For more information, see <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a>



<a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>



<b>Other Resources</b>



<b>Reference</b>
 

 

