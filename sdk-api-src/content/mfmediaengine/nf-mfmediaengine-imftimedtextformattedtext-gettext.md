---
UID: NF:mfmediaengine.IMFTimedTextFormattedText.GetText
title: IMFTimedTextFormattedText::GetText (mfmediaengine.h)
description: Gets the text in the formatted timed-text object.
helpviewer_keywords: ["GetText","GetText method [Media Foundation]","GetText method [Media Foundation]","IMFTimedTextFormattedText interface","IMFTimedTextFormattedText interface [Media Foundation]","GetText method","IMFTimedTextFormattedText.GetText","IMFTimedTextFormattedText::GetText","mf.imftimedtextformattedtext_gettext","mfmediaengine/IMFTimedTextFormattedText::GetText"]
old-location: mf\imftimedtextformattedtext_gettext.htm
tech.root: medfound
ms.assetid: 0D734EF8-BE52-404D-BEEC-504ECB0F7107
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Media Foundation], GetText method [Media Foundation],IMFTimedTextFormattedText interface, IMFTimedTextFormattedText interface [Media Foundation],GetText method, IMFTimedTextFormattedText.GetText, IMFTimedTextFormattedText::GetText, mf.imftimedtextformattedtext_gettext, mfmediaengine/IMFTimedTextFormattedText::GetText
f1_keywords:
- mfmediaengine/IMFTimedTextFormattedText.GetText
dev_langs:
- c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
- mfmediaengine.h
api_name:
- IMFTimedTextFormattedText.GetText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextFormattedText::GetText


## -description


Gets the text in the formatted timed-text object.


## -parameters




### -param text [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext">IMFTimedTextFormattedText</a>
 

 

