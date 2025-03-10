---
UID: NF:dwrite_3.IDWriteFontList1.GetFontFaceReference
title: IDWriteFontList1::GetFontFaceReference (dwrite_3.h)
description: Gets a font face reference given its zero-based index.
helpviewer_keywords: ["GetFontFaceReference","GetFontFaceReference method [Direct Write]","GetFontFaceReference method [Direct Write]","IDWriteFontList1 interface","IDWriteFontList1 interface [Direct Write]","GetFontFaceReference method","IDWriteFontList1.GetFontFaceReference","IDWriteFontList1::GetFontFaceReference","directwrite.idwritefontlist1_getfontfacereference","dwrite_3/IDWriteFontList1::GetFontFaceReference"]
old-location: directwrite\idwritefontlist1_getfontfacereference.htm
tech.root: DirectWrite
ms.assetid: E8EFDD13-2B6E-4C50-9A5D-AFBB4C0AF08B
ms.date: 12/05/2018
ms.keywords: GetFontFaceReference, GetFontFaceReference method [Direct Write], GetFontFaceReference method [Direct Write],IDWriteFontList1 interface, IDWriteFontList1 interface [Direct Write],GetFontFaceReference method, IDWriteFontList1.GetFontFaceReference, IDWriteFontList1::GetFontFaceReference, directwrite.idwritefontlist1_getfontfacereference, dwrite_3/IDWriteFontList1::GetFontFaceReference
f1_keywords:
- dwrite_3/IDWriteFontList1.GetFontFaceReference
dev_langs:
- c++
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFontList1.GetFontFaceReference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontList1::GetFontFaceReference


## -description


Gets a font face reference given its zero-based index.


## -parameters




### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.


### -param fontFaceReference [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a> interface for the newly created font face reference object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1">IDWriteFontList1</a>
 

 

