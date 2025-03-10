---
UID: NN:d2d1_1.ID2D1DrawingStateBlock1
title: ID2D1DrawingStateBlock1 (d2d1_1.h)
description: Implementation of a drawing state block that adds the functionality of primitive blend in addition to already existing antialias mode, transform, tags and text rendering mode.
helpviewer_keywords: ["ID2D1DrawingStateBlock1","ID2D1DrawingStateBlock1 interface [Direct2D]","ID2D1DrawingStateBlock1 interface [Direct2D]","described","d2d1_1/ID2D1DrawingStateBlock1","direct2d.id2d1drawingstateblock1"]
old-location: direct2d\id2d1drawingstateblock1.htm
tech.root: Direct2D
ms.assetid: F3A364F6-2C30-4DDE-A5C7-7B58758F111F
ms.date: 12/05/2018
ms.keywords: ID2D1DrawingStateBlock1, ID2D1DrawingStateBlock1 interface [Direct2D], ID2D1DrawingStateBlock1 interface [Direct2D],described, d2d1_1/ID2D1DrawingStateBlock1, direct2d.id2d1drawingstateblock1
f1_keywords:
- d2d1_1/ID2D1DrawingStateBlock1
dev_langs:
- c++
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1DrawingStateBlock1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DrawingStateBlock1 interface


## -description


Implementation of a drawing state block that adds the functionality of primitive blend in addition to already existing antialias mode, transform, tags and text rendering mode.<div class="alert"><b>Note</b>  You can get an <b>ID2D1DrawingStateBlock1</b> using the  <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-createdrawingstateblock(constd2d1_drawing_state_description1__id2d1drawingstateblock1)">ID2D1Factory::CreateDrawingStateBlock</a> method or you can use the QueryInterface method on an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a> object.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DrawingStateBlock1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>. <b>ID2D1DrawingStateBlock1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DrawingStateBlock1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1drawingstateblock1-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the antialiasing mode, transform, tags, primitive blend, and unit mode portion of the drawing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1drawingstateblock1-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_drawing_state_description1">D2D1_DRAWING_STATE_DESCRIPTION1</a> associated with this drawing state block.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1drawingstateblock1-getdescription">ID2D1DrawingStateBlock1::GetDescription1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1drawingstateblock1-setdescription">ID2D1DrawingStateBlock1::SetDescription1</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1factory-createdrawingstateblock">ID2D1Factory::CreateDrawingStateBlock</a>
 

 

