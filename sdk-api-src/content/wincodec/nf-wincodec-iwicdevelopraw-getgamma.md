---
UID: NF:wincodec.IWICDevelopRaw.GetGamma
title: IWICDevelopRaw::GetGamma (wincodec.h)
description: Gets the current gamma setting of the raw image.
helpviewer_keywords: ["GetGamma","GetGamma method [Windows Imaging Component]","GetGamma method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetGamma method","IWICDevelopRaw.GetGamma","IWICDevelopRaw::GetGamma","_wic_codec_iwicdevelopraw_getgamma","wic._wic_codec_iwicdevelopraw_getgamma","wincodec/IWICDevelopRaw::GetGamma"]
old-location: wic\_wic_codec_iwicdevelopraw_getgamma.htm
tech.root: wic
ms.assetid: d76fc2dc-9bcc-4d7b-93fd-82a9647e7b6f
ms.date: 12/05/2018
ms.keywords: GetGamma, GetGamma method [Windows Imaging Component], GetGamma method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetGamma method, IWICDevelopRaw.GetGamma, IWICDevelopRaw::GetGamma, _wic_codec_iwicdevelopraw_getgamma, wic._wic_codec_iwicdevelopraw_getgamma, wincodec/IWICDevelopRaw::GetGamma
f1_keywords:
- wincodec/IWICDevelopRaw.GetGamma
dev_langs:
- c++
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.dll
api_name:
- IWICDevelopRaw.GetGamma
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDevelopRaw::GetGamma


## -description


Gets the current gamma setting of the raw image.


## -parameters




### -param pGamma [out]

Type: <b>double*</b>

A pointer that receives the current gamma setting.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



