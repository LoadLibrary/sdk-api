---
UID: NF:oleauto.VarR8FromR4
title: VarR8FromR4 function (oleauto.h)
description: Converts a float value to a double value.
helpviewer_keywords: ["VarR8FromR4","VarR8FromR4 function [Automation]","_oa96_VarR8FromR4","automat.varr8fromr4","oleauto/VarR8FromR4"]
old-location: automat\varr8fromr4.htm
tech.root: automat
ms.assetid: 207d9d78-0db1-48b7-a686-7bacbd805af6
ms.date: 12/05/2018
ms.keywords: VarR8FromR4, VarR8FromR4 function [Automation], _oa96_VarR8FromR4, automat.varr8fromr4, oleauto/VarR8FromR4
f1_keywords:
- oleauto/VarR8FromR4
dev_langs:
- c++
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- VarR8FromR4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarR8FromR4 function


## -description


Converts a float value to a double value.


## -parameters




### -param fltIn [in]

The value to convert.


### -param pdblOut [out]

The resulting value.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data pointed to by the output parameter does not fit in the destination type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 



