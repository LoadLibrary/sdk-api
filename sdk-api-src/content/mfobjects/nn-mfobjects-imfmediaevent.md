---
UID: NN:mfobjects.IMFMediaEvent
title: IMFMediaEvent (mfobjects.h)
description: Represents an event generated by a Media Foundation object. Use this interface to get information about the event.
helpviewer_keywords: ["IMFMediaEvent","IMFMediaEvent interface [Media Foundation]","IMFMediaEvent interface [Media Foundation]","described","b4f686be-9472-433c-b983-6c48dfd3ac76","mf.imfmediaevent","mfobjects/IMFMediaEvent"]
old-location: mf\imfmediaevent.htm
tech.root: medfound
ms.assetid: b4f686be-9472-433c-b983-6c48dfd3ac76
ms.date: 12/05/2018
ms.keywords: IMFMediaEvent, IMFMediaEvent interface [Media Foundation], IMFMediaEvent interface [Media Foundation],described, b4f686be-9472-433c-b983-6c48dfd3ac76, mf.imfmediaevent, mfobjects/IMFMediaEvent
f1_keywords:
- mfobjects/IMFMediaEvent
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
- IMFMediaEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEvent interface


## -description


Represents an event generated by a Media Foundation object. Use this interface to get information about the event.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">IMFMediaEventGenerator::BeginGetEvent</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">IMFMediaEventGenerator::GetEvent</a> on the event generator.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEvent</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFMediaEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype">GetExtendedType</a>
</td>
<td align="left" width="63%">
Retrieves the extended type of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves an <b>HRESULT</b> that specifies the event status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the event type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with the event.

</td>
</tr>
</table> 


## -remarks



If you are implementing an object that generates events, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediaevent">MFCreateMediaEvent</a> function to create a new event object.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/event-attributes">Event Attributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-event-generators">Media Event Generators</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

