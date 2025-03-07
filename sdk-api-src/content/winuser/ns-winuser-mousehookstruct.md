---
UID: NS:winuser.tagMOUSEHOOKSTRUCT
title: MOUSEHOOKSTRUCT (winuser.h)
description: Contains information about a mouse event passed to a WH_MOUSE hook procedure, MouseProc.
helpviewer_keywords: ["*LPMOUSEHOOKSTRUCT","*PMOUSEHOOKSTRUCT","LPMOUSEHOOKSTRUCT","LPMOUSEHOOKSTRUCT structure pointer [Windows and Messages]","MOUSEHOOKSTRUCT","MOUSEHOOKSTRUCT structure [Windows and Messages]","PMOUSEHOOKSTRUCT","PMOUSEHOOKSTRUCT structure pointer [Windows and Messages]","_win32_MOUSEHOOKSTRUCT_str","_win32_mousehookstruct_str_cpp","winmsg.mousehookstruct","winui._win32_mousehookstruct_str","winuser/LPMOUSEHOOKSTRUCT","winuser/MOUSEHOOKSTRUCT","winuser/PMOUSEHOOKSTRUCT"]
old-location: winmsg\mousehookstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\mousehookstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPMOUSEHOOKSTRUCT, *PMOUSEHOOKSTRUCT, LPMOUSEHOOKSTRUCT, LPMOUSEHOOKSTRUCT structure pointer [Windows and Messages], MOUSEHOOKSTRUCT, MOUSEHOOKSTRUCT structure [Windows and Messages], PMOUSEHOOKSTRUCT, PMOUSEHOOKSTRUCT structure pointer [Windows and Messages], _win32_MOUSEHOOKSTRUCT_str, _win32_mousehookstruct_str_cpp, winmsg.mousehookstruct, winui._win32_mousehookstruct_str, winuser/LPMOUSEHOOKSTRUCT, winuser/MOUSEHOOKSTRUCT, winuser/PMOUSEHOOKSTRUCT'
f1_keywords:
- winuser/MOUSEHOOKSTRUCT
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
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
- Winuser.h
api_name:
- MOUSEHOOKSTRUCT
targetos: Windows
req.typenames: MOUSEHOOKSTRUCT, *LPMOUSEHOOKSTRUCT, *PMOUSEHOOKSTRUCT
req.redist: 
ms.custom: 19H1
---

# MOUSEHOOKSTRUCT structure


## -description


Contains information about a mouse event passed to a <b>WH_MOUSE</b> hook procedure, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)">MouseProc</a>. 


## -struct-fields




### -field pt

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>

The x- and y-coordinates of the cursor, in screen coordinates. 


### -field hwnd

Type: <b>HWND</b>

A handle to the window that will receive the mouse message corresponding to the mouse event. 


### -field wHitTestCode

Type: <b>UINT</b>

The hit-test value. For a list of hit-test values, see the description of the <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-nchittest">WM_NCHITTEST</a> message. 


### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

Additional information associated with the message. 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/hooks">Hooks</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)">MouseProc</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-nchittest">WM_NCHITTEST</a>
 

 

