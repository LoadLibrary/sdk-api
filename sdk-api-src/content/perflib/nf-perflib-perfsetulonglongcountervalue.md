---
UID: NF:perflib.PerfSetULongLongCounterValue
title: PerfSetULongLongCounterValue function (perflib.h)
description: Updates the value of a counter whose value is an 8-byte unsigned integer. Providers use this function.
helpviewer_keywords: ["PerfSetULongLongCounterValue","PerfSetULongLongCounterValue function [Perf]","base.perfsetulonglongcountervalue","perf.perfsetulonglongcountervalue","perflib/PerfSetULongLongCounterValue"]
old-location: perf\perfsetulonglongcountervalue.htm
tech.root: perfctrs
ms.assetid: c38f9efc-7ea8-4841-9a31-a88d4f87369c
ms.date: 12/05/2018
ms.keywords: PerfSetULongLongCounterValue, PerfSetULongLongCounterValue function [Perf], base.perfsetulonglongcountervalue, perf.perfsetulonglongcountervalue, perflib/PerfSetULongLongCounterValue
f1_keywords:
- perflib/PerfSetULongLongCounterValue
dev_langs:
- c++
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-Core-perfcounters-l1-1-0.dll
- KernelBase.dll
api_name:
- PerfSetULongLongCounterValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PerfSetULongLongCounterValue function


## -description


Updates the value of a counter whose value is an 8-byte unsigned integer. Providers use this function.


## -parameters




### -param Provider [in]

The handle of the provider. Use the handle variable that the <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://docs.microsoft.com/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.


### -param Instance [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance. The <a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a> function returns this pointer.


### -param CounterId [in]

Identifier that uniquely identifies the counter to update in the instance block. The identifier is defined in the <b>id</b> attribute of the <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element">counter</a> element and must match the <b>CounterId</b> member of one of the <a href="https://docs.microsoft.com/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> structures in the instance block. Use the counter ID constant that the <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the constant, see the <b>symbol</b> attribute of the <b>counter</b> element.

<b>Windows Vista:  </b>The counter ID constant is not available.


### -param Value [in]

New 8-byte counter value.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>. 




## -remarks



This is a convenience function for setting raw counter data. To update the raw counter data yourself, use the <b>Offset</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> structure to access the raw counter data for a specific counter. The <a href="https://docs.microsoft.com/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure block contains one or more counter information structures.

You can use the <a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfincrementulonglongcountervalue">PerfIncrementULongLongCounterValue</a> and <a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfdecrementulonglongcountervalue">PerfDecrementULongLongCounterValue</a> functions to increment or decrement the counter value, respectively.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfdecrementulonglongcountervalue">PerfDecrementULongLongCounterValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfincrementulonglongcountervalue">PerfIncrementULongLongCounterValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfsetcounterrefvalue">PerfSetCounterRefValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfsetulongcountervalue">PerfSetULongCounterValue</a>
 

 

