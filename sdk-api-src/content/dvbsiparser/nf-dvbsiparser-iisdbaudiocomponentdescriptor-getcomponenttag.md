---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetComponentTag
title: IIsdbAudioComponentDescriptor::GetComponentTag (dvbsiparser.h)
description: Gets the value of the component_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
helpviewer_keywords: ["GetComponentTag","GetComponentTag method [Microsoft TV Technologies]","GetComponentTag method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetComponentTag method","IIsdbAudioComponentDescriptor.GetComponentTag","IIsdbAudioComponentDescriptor::GetComponentTag","dvbsiparser/IIsdbAudioComponentDescriptor::GetComponentTag","mstv.iisdbaudiocomponentdescriptor_getcomponenttag"]
old-location: mstv\iisdbaudiocomponentdescriptor_getcomponenttag.htm
tech.root: mstv
ms.assetid: 4b06f566-b5e0-43c8-8694-24d913bbf971
ms.date: 12/05/2018
ms.keywords: GetComponentTag, GetComponentTag method [Microsoft TV Technologies], GetComponentTag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetComponentTag method, IIsdbAudioComponentDescriptor.GetComponentTag, IIsdbAudioComponentDescriptor::GetComponentTag, dvbsiparser/IIsdbAudioComponentDescriptor::GetComponentTag, mstv.iisdbaudiocomponentdescriptor_getcomponenttag
f1_keywords:
- dvbsiparser/IIsdbAudioComponentDescriptor.GetComponentTag
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
- dvbsiparser.h
api_name:
- IIsdbAudioComponentDescriptor.GetComponentTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetComponentTag


## -description


 Gets the value of the component_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field identifies the component stream and has the same value
as the component_tag field in the stream identifier descriptor in
the Program Specific Information (PSI) program map section for the component stream.


## -parameters




### -param pbVal [out]

Receives the component tag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 

