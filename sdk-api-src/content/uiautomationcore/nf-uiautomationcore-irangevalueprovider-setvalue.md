---
UID: NF:uiautomationcore.IRangeValueProvider.SetValue
title: IRangeValueProvider::SetValue (uiautomationcore.h)
description: Sets the value of the control.
helpviewer_keywords: ["IRangeValueProvider interface [Windows Accessibility]","SetValue method","IRangeValueProvider.SetValue","IRangeValueProvider::SetValue","SetValue","SetValue method [Windows Accessibility]","SetValue method [Windows Accessibility]","IRangeValueProvider interface","uiauto.uiauto_IRangeValueProvider_SetValue","uiauto_IRangeValueProvider_SetValue","uiautomationcore/IRangeValueProvider::SetValue","winauto.uiauto_IRangeValueProvider_SetValue"]
old-location: winauto\uiauto_IRangeValueProvider_SetValue.htm
tech.root: WinAuto
ms.assetid: 3ce214a0-e7ff-440a-a308-fea5608e13f0
ms.date: 12/05/2018
ms.keywords: IRangeValueProvider interface [Windows Accessibility],SetValue method, IRangeValueProvider.SetValue, IRangeValueProvider::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],IRangeValueProvider interface, uiauto.uiauto_IRangeValueProvider_SetValue, uiauto_IRangeValueProvider_SetValue, uiautomationcore/IRangeValueProvider::SetValue, winauto.uiauto_IRangeValueProvider_SetValue
f1_keywords:
- uiautomationcore/IRangeValueProvider.SetValue
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uiautomationcore.dll
api_name:
- IRangeValueProvider.SetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRangeValueProvider::SetValue


## -description


Sets the value of the control.


## -parameters




### -param val [in]

Type: <b>double</b>

The value to set.



## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The actual value set depends on the control implementation. The control may round the requested value up or down.
		




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irangevalueprovider">IRangeValueProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

