---
UID: NF:xpsobjectmodel.IXpsOMPath.Clone
title: IXpsOMPath::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface.
helpviewer_keywords: ["Clone","Clone method [XPS Documents and Packaging]","Clone method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","Clone method","IXpsOMPath.Clone","IXpsOMPath::Clone","xps.ixpsompath_clone","xpsobjectmodel/IXpsOMPath::Clone"]
old-location: xps\ixpsompath_clone.htm
tech.root: printdocs
ms.assetid: 4602f9fe-6001-4a5a-8870-f2a6e97ccc55
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],Clone method, IXpsOMPath.Clone, IXpsOMPath::Clone, xps.ixpsompath_clone, xpsobjectmodel/IXpsOMPath::Clone
f1_keywords:
- xpsobjectmodel/IXpsOMPath.Clone
dev_langs:
- c++
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMPath.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPath::Clone


## -description


Makes a deep copy of the interface.


## -parameters




### -param path [out, retval]

A pointer to the copy of the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
Not enough memory to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>path</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

