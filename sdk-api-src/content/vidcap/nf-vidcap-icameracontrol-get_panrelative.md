---
UID: NF:vidcap.ICameraControl.get_PanRelative
title: ICameraControl::get_PanRelative (vidcap.h)
description: The get_PanRelative method returns the camera's relative pan. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_PanRelative method","ICameraControl.get_PanRelative","ICameraControl::get_PanRelative","ICameraControlget_PanRelative","dshow.icameracontrol_get_panrelative","get_PanRelative","get_PanRelative method [DirectShow]","get_PanRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_PanRelative"]
old-location: dshow\icameracontrol_get_panrelative.htm
tech.root: DirectShow
ms.assetid: a7237e0a-82b3-4e2a-a6c7-97fbb03b5917
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanRelative method, ICameraControl.get_PanRelative, ICameraControl::get_PanRelative, ICameraControlget_PanRelative, dshow.icameracontrol_get_panrelative, get_PanRelative, get_PanRelative method [DirectShow], get_PanRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanRelative
f1_keywords:
- vidcap/ICameraControl.get_PanRelative
dev_langs:
- c++
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- ICameraControl.get_PanRelative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_PanRelative


## -description


The <code>get_PanRelative</code> method returns the camera's relative pan. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pValue [out]

Receives the relative pan. The size of the value represents the desired pan speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_panrelative">ICameraControl::getRange_PanRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stopped.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Panning to the right.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Panning to the left.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

