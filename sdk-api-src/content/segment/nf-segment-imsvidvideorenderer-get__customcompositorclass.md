---
UID: NF:segment.IMSVidVideoRenderer.get__CustomCompositorClass
title: IMSVidVideoRenderer::get__CustomCompositorClass (segment.h)
description: The get__CustomCompositorClass method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a GUID.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get__CustomCompositorClass method","IMSVidVideoRenderer.get__CustomCompositorClass","IMSVidVideoRenderer::get__CustomCompositorClass","IMSVidVideoRendererget__CustomCompositorClass","get__CustomCompositorClass","get__CustomCompositorClass method [Microsoft TV Technologies]","get__CustomCompositorClass method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get__customcompositorclass","segment/IMSVidVideoRenderer::get__CustomCompositorClass"]
old-location: mstv\imsvidvideorenderer_get__customcompositorclass.htm
tech.root: mstv
ms.assetid: 0ac48bbb-a0d3-4c37-9f3e-4f4cc79b550b
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__CustomCompositorClass method, IMSVidVideoRenderer.get__CustomCompositorClass, IMSVidVideoRenderer::get__CustomCompositorClass, IMSVidVideoRendererget__CustomCompositorClass, get__CustomCompositorClass, get__CustomCompositorClass method [Microsoft TV Technologies], get__CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__customcompositorclass, segment/IMSVidVideoRenderer::get__CustomCompositorClass
f1_keywords:
- segment/IMSVidVideoRenderer.get__CustomCompositorClass
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- segment.h
api_name:
- IMSVidVideoRenderer.get__CustomCompositorClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer::get__CustomCompositorClass


## -description


The <b>get__CustomCompositorClass</b> method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a <b>GUID</b>.


## -parameters




### -param CompositorCLSID [out]

Receives the CLSID.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositor">IMSVidVideoRenderer::get__CustomCompositor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositorclass">IMSVidVideoRenderer::put__CustomCompositorClass</a>
 

 

