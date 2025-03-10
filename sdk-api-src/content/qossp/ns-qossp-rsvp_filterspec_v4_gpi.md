---
UID: NS:qossp._RSVP_FILTERSPEC_V4_GPI
title: RSVP_FILTERSPEC_V4_GPI (qossp.h)
description: The RSVP_FILTERSPEC_V4_GPI structure provides general port identifier information for a given FILTERSPEC.
helpviewer_keywords: ["*LPRSVP_FILTERSPEC_V4_GPI","*LPRSVP_FILTERSPEC_V4_GPI structure [QOS]","RSVP_FILTERSPEC_V4_GPI","RSVP_FILTERSPEC_V4_GPI structure [QOS]","qos.rsvp_filterspec_v4_gpi","qossp/*LPRSVP_FILTERSPEC_V4_GPI","qossp/RSVP_FILTERSPEC_V4_GPI"]
old-location: qos\rsvp_filterspec_v4_gpi.htm
tech.root: QOS
ms.assetid: bedb3526-700c-4c99-ba02-19389a78acf8
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_FILTERSPEC_V4_GPI, *LPRSVP_FILTERSPEC_V4_GPI structure [QOS], RSVP_FILTERSPEC_V4_GPI, RSVP_FILTERSPEC_V4_GPI structure [QOS], qos.rsvp_filterspec_v4_gpi, qossp/*LPRSVP_FILTERSPEC_V4_GPI, qossp/RSVP_FILTERSPEC_V4_GPI'
f1_keywords:
- qossp/RSVP_FILTERSPEC_V4_GPI
dev_langs:
- c++
req.header: qossp.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Qossp.h
api_name:
- RSVP_FILTERSPEC_V4_GPI
targetos: Windows
req.typenames: RSVP_FILTERSPEC_V4_GPI, *LPRSVP_FILTERSPEC_V4_GPI
req.redist: 
ms.custom: 19H1
---

# RSVP_FILTERSPEC_V4_GPI structure


## -description


The <b>RSVP_FILTERSPEC_V4_GPI</b> structure provides general port identifier information for a given FILTERSPEC.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC general port identifier applies, expressed as an <a href="https://docs.microsoft.com/windows/desktop/api/qossp/ns-qossp-in_addr_ipv4">IN_ADDR_IPV4</a> union.


### -field GeneralPortId

General Port Identifier for the FILTERSPEC.


## -remarks



When working with IPv6 addresses, use <a href="https://docs.microsoft.com/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_gpi">RSVP_FILTERSPEC_V6_GPI</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qossp/ns-qossp-in_addr_ipv4">IN_ADDR_IPV4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_gpi">RSVP_FILTERSPEC_V6_GPI</a>
 

 

