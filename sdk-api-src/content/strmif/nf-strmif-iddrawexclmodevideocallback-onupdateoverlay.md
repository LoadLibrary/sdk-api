---
UID: NF:strmif.IDDrawExclModeVideoCallback.OnUpdateOverlay
title: IDDrawExclModeVideoCallback::OnUpdateOverlay (strmif.h)
description: The OnUpdateOverlay method informs the application when the overlay surface for the video is about to become visible, invisible, change size, or change position, so that the application can repaint its window appropriately.
helpviewer_keywords: ["IDDrawExclModeVideoCallback interface [DirectShow]","OnUpdateOverlay method","IDDrawExclModeVideoCallback.OnUpdateOverlay","IDDrawExclModeVideoCallback::OnUpdateOverlay","IDDrawExclModeVideoCallbackOnUpdateOverlay","OnUpdateOverlay","OnUpdateOverlay method [DirectShow]","OnUpdateOverlay method [DirectShow]","IDDrawExclModeVideoCallback interface","dshow.iddrawexclmodevideocallback_onupdateoverlay","strmif/IDDrawExclModeVideoCallback::OnUpdateOverlay"]
old-location: dshow\iddrawexclmodevideocallback_onupdateoverlay.htm
tech.root: DirectShow
ms.assetid: ede823ba-8340-4339-8e8a-e1d4f9ad1273
ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideoCallback interface [DirectShow],OnUpdateOverlay method, IDDrawExclModeVideoCallback.OnUpdateOverlay, IDDrawExclModeVideoCallback::OnUpdateOverlay, IDDrawExclModeVideoCallbackOnUpdateOverlay, OnUpdateOverlay, OnUpdateOverlay method [DirectShow], OnUpdateOverlay method [DirectShow],IDDrawExclModeVideoCallback interface, dshow.iddrawexclmodevideocallback_onupdateoverlay, strmif/IDDrawExclModeVideoCallback::OnUpdateOverlay
f1_keywords:
- strmif/IDDrawExclModeVideoCallback.OnUpdateOverlay
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDDrawExclModeVideoCallback.OnUpdateOverlay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDDrawExclModeVideoCallback::OnUpdateOverlay


## -description



The <code>OnUpdateOverlay</code> method informs the application when the overlay surface for the video is about to become visible, invisible, change size, or change position, so that the application can repaint its window appropriately.




## -parameters




### -param bBefore [in]

Boolean value specifying whether the call is being made before or after the overlay-related change. <b>TRUE</b> specifies before, <b>FALSE</b> specifies after.


### -param dwFlags [in]

Value from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_am_overlay_notify_flags">AM_OVERLAY_NOTIFY_FLAGS</a> enumeration that specifies what is about to change or what changed.


### -param bOldVisible [in]

Boolean value specifying whether the old window is visible. <b>TRUE</b> means the old window is visible.


### -param prcOldSrc [in]

Pointer to the rectangle representing the old source position of the DirectDraw surface.


### -param prcOldDest [in]

Pointer to the rectangle representing the old destination position of the rectangle in the overlay surface.


### -param bNewVisible [in]

Boolean specifying whether the new window is visible. <b>TRUE</b> means the new window is visible.


### -param prcNewSrc [in]

Pointer to the rectangle representing the new source position of the DirectDraw surface.


### -param prcNewDest [in]

Pointer to the rectangle representing the new destination position of the rectangle in the overlay surface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
</table>
 




## -remarks



The application should call this method once before the overlay-related change occurs and once after the changes are done. In the call before the change, the overlay change doesn't happen until the application completes executing this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback Interface</a>
 

 

