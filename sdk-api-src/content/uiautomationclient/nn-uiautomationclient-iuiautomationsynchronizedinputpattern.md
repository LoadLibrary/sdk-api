---
UID: NN:uiautomationclient.IUIAutomationSynchronizedInputPattern
title: IUIAutomationSynchronizedInputPattern (uiautomationclient.h)
description: Provides access to the keyboard or mouse input of a control.
helpviewer_keywords: ["IUIAutomationSynchronizedInputPattern","IUIAutomationSynchronizedInputPattern interface [Windows Accessibility]","IUIAutomationSynchronizedInputPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationSynchronizedInputPattern","uiauto_IUIAutomationSynchronizedInputPattern","uiautomationclient/IUIAutomationSynchronizedInputPattern","winauto.uiauto_IUIAutomationSynchronizedInputPattern"]
old-location: winauto\uiauto_IUIAutomationSynchronizedInputPattern.htm
tech.root: WinAuto
ms.assetid: 8e1ad860-7288-4600-8e88-59d5b1c86694
ms.date: 12/05/2018
ms.keywords: IUIAutomationSynchronizedInputPattern, IUIAutomationSynchronizedInputPattern interface [Windows Accessibility], IUIAutomationSynchronizedInputPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationSynchronizedInputPattern, uiauto_IUIAutomationSynchronizedInputPattern, uiautomationclient/IUIAutomationSynchronizedInputPattern, winauto.uiauto_IUIAutomationSynchronizedInputPattern
f1_keywords:
- uiautomationclient/IUIAutomationSynchronizedInputPattern
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IUIAutomationSynchronizedInputPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationSynchronizedInputPattern interface


## -description


Provides access to  the keyboard or mouse input of a control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSynchronizedInputPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationSynchronizedInputPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationSynchronizedInputPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationsynchronizedinputpattern-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Causes the UI Automation provider to stop listening for mouse or keyboard input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationsynchronizedinputpattern-startlistening">StartListening</a>
</td>
<td align="left" width="63%">
Causes the UI Automation provider to start listening for mouse or keyboard input.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

