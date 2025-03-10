---
UID: NF:wmp.IWMPControls3.get_currentPositionTimecode
title: IWMPControls3::get_currentPositionTimecode (wmp.h)
description: The get_currentPositionTimecode method retrieves the current position in the current media item using a time code format. This method currently supports SMPTE time code.
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","get_currentPositionTimecode method","IWMPControls3.get_currentPositionTimecode","IWMPControls3::get_currentPositionTimecode","IWMPControls3get_currentPositionTimecode","get_currentPositionTimecode","get_currentPositionTimecode method [Windows Media Player]","get_currentPositionTimecode method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_get_currentpositiontimecode","wmp/IWMPControls3::get_currentPositionTimecode"]
old-location: wmp\iwmpcontrols3_get_currentpositiontimecode.htm
tech.root: WMP
ms.assetid: dbf981d7-1787-462c-b0d2-fd705f07ee23
ms.date: 12/05/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],get_currentPositionTimecode method, IWMPControls3.get_currentPositionTimecode, IWMPControls3::get_currentPositionTimecode, IWMPControls3get_currentPositionTimecode, get_currentPositionTimecode, get_currentPositionTimecode method [Windows Media Player], get_currentPositionTimecode method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_get_currentpositiontimecode, wmp/IWMPControls3::get_currentPositionTimecode
f1_keywords:
- wmp/IWMPControls3.get_currentPositionTimecode
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPControls3.get_currentPositionTimecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPControls3::get_currentPositionTimecode


## -description



The <b>get_currentPositionTimecode</b> method retrieves the current position in the current media item using a time code format. This method currently supports SMPTE time code.




## -parameters




### -param bstrTimecode [out]

Pointer to a <b>BSTR</b> containing the time code.


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
</table>
 




## -remarks



SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback. If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a <b>BSTR</b> containing a particular time code.

SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame—the frame designated as time zero. Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.

The time code is in the format [<i>range</i>]<i>hh</i>:<i>mm</i>:<i>ss</i>.<i>ff</i> where [<i>range</i>] represents the range, <i>hh</i> represents hours, <i>mm</i> represents minutes, <i>ss</i> represents seconds, and <i>ff</i> represents frames. When specifying a value for <b>IWMPControls3::put_currentPositionTimecode</b>, you must include all eight digits, using zeros as placeholders.

[<i>range</i>] corresponds to the <b>wRange</b> member of the Windows Media Format <b>WMT_TIMECODE_EXTENSION_DATA</b> structure. For more information about time code ranges, see the Windows Media Format SDK.

Specifying and retrieving values by using <b>put_currentPositionTimecode</b> and <b>get_currentPositionTimecode</b> are supported only for files that contain SMPTE time code information.

<b>Windows Media Player 10 Mobile: </b>When retrieving or specifying an SMPTE time code through the object model, the range and frames sections of the time code format are not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentpositiontimecode">IWMPControls3::put_currentPositionTimecode</a>
 

 

