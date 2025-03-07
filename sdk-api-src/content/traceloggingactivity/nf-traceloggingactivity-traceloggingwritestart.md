---
UID: NF:traceloggingactivity.TraceLoggingWriteStart
title: TraceLoggingWriteStart macro (traceloggingactivity.h)
description: Starts an activity and logs the start event.
helpviewer_keywords: ["TraceLoggingWriteStart","TraceLoggingWriteStart macro","tracelogging.traceloggingwritestart","traceloggingactivity/TraceLoggingWriteStart"]
old-location: tracelogging\traceloggingwritestart.htm
tech.root: tracelogging
ms.assetid: E5B9347E-50A7-49BE-BDD5-DCED39371234
ms.date: 12/05/2018
ms.keywords: TraceLoggingWriteStart, TraceLoggingWriteStart macro, tracelogging.traceloggingwritestart, traceloggingactivity/TraceLoggingWriteStart
f1_keywords:
- traceloggingactivity/TraceLoggingWriteStart
dev_langs:
- c++
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
- traceloggingactivity.h
api_name:
- TraceLoggingWriteStart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingWriteStart macro


## -description


Starts an activity and logs the start event.

The activity must not have already been started.


## -parameters




### -param activity [in]

The activity to start.


### -param name [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters.


#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://docs.microsoft.com/windows/desktop/tracelogging/tracelogging-wrapper-macros">TraceLogging Wrapper Macros</a>.

The args should not include <b>TraceLoggingLevel</b>, <b>TraceLoggingKeyword</b>, or <b>TraceLoggingOpcode</b>. The level and keyword are set on the activity itself, and the opcode for a start event is always “Start”.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>
 

 

