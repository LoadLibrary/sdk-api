---
UID: NF:mfidl.MFCreateMediaTypeFromProperties
title: MFCreateMediaTypeFromProperties function (mfidl.h)
description: Create an IMFMediaType from properties.
helpviewer_keywords: ["MFCreateMediaTypeFromProperties","MFCreateMediaTypeFromProperties function [Media Foundation]","mf.mfcreatemediatypefromproperties","mfidl/MFCreateMediaTypeFromProperties"]
old-location: mf\mfcreatemediatypefromproperties.htm
tech.root: medfound
ms.assetid: F34F5C7F-880B-40A8-85EF-537CD36759CB
ms.date: 12/05/2018
ms.keywords: MFCreateMediaTypeFromProperties, MFCreateMediaTypeFromProperties function [Media Foundation], mf.mfcreatemediatypefromproperties, mfidl/MFCreateMediaTypeFromProperties
f1_keywords:
- mfidl/MFCreateMediaTypeFromProperties
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFCreateMediaTypeFromProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateMediaTypeFromProperties function


## -description


Create an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> from properties.


## -parameters




### -param punkStream [in]

A pointer to properties.


### -param ppMediaType [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

