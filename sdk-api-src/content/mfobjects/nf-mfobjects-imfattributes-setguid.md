---
UID: NF:mfobjects.IMFAttributes.SetGUID
title: IMFAttributes::SetGUID (mfobjects.h)
description: Associates a GUID value with a key.
helpviewer_keywords: ["IMFAttributes interface [Media Foundation]","SetGUID method","IMFAttributes.SetGUID","IMFAttributes::SetGUID","SetGUID","SetGUID method [Media Foundation]","SetGUID method [Media Foundation]","IMFAttributes interface","d73b53f5-4a8f-4903-986d-fbf4277a2d45","mf.imfattributes_setguid","mfobjects/IMFAttributes::SetGUID"]
old-location: mf\imfattributes_setguid.htm
tech.root: medfound
ms.assetid: d73b53f5-4a8f-4903-986d-fbf4277a2d45
ms.date: 12/05/2018
ms.keywords: IMFAttributes interface [Media Foundation],SetGUID method, IMFAttributes.SetGUID, IMFAttributes::SetGUID, SetGUID, SetGUID method [Media Foundation], SetGUID method [Media Foundation],IMFAttributes interface, d73b53f5-4a8f-4903-986d-fbf4277a2d45, mf.imfattributes_setguid, mfobjects/IMFAttributes::SetGUID
f1_keywords:
- mfobjects/IMFAttributes.SetGUID
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFAttributes.SetGUID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAttributes::SetGUID


## -description



Associates a GUID value with a key.




## -parameters




### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.


### -param guidValue [in]

New value for this key.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



To retrieve the GUID value, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid">IMFAttributes::GetGUID</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
 

 

