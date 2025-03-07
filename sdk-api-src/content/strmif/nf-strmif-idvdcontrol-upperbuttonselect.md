---
UID: NF:strmif.IDvdControl.UpperButtonSelect
title: IDvdControl::UpperButtonSelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects the upper directional button from the displayed menu.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","UpperButtonSelect method","IDvdControl.UpperButtonSelect","IDvdControl::UpperButtonSelect","IDvdControlUpperButtonSelect","UpperButtonSelect","UpperButtonSelect method [DirectShow]","UpperButtonSelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_upperbuttonselect","strmif/IDvdControl::UpperButtonSelect"]
old-location: dshow\idvdcontrol_upperbuttonselect.htm
tech.root: DirectShow
ms.assetid: bd0e4086-087b-460f-a6af-fa073644f1bb
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],UpperButtonSelect method, IDvdControl.UpperButtonSelect, IDvdControl::UpperButtonSelect, IDvdControlUpperButtonSelect, UpperButtonSelect, UpperButtonSelect method [DirectShow], UpperButtonSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_upperbuttonselect, strmif/IDvdControl::UpperButtonSelect
f1_keywords:
- strmif/IDvdControl.UpperButtonSelect
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IDvdControl.UpperButtonSelect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::UpperButtonSelect


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Selects the upper directional button from the displayed menu.




## -parameters






## -returns



Returns an <b>HRESULT</b> value .




## -remarks



On physical or electronic remote control devices, there is often a group of four directional buttons used for certain types of operations (such as menu navigation). This method tells DirectShow that something (the user, probably) triggered the upper directional button.

Selecting a DVD button simply highlights the button but does not activate the button. Selecting is the Windows equivalent of tabbing to a button but not pressing the SPACEBAR or ENTER key. Activating is the Windows equivalent of pressing the SPACEBAR or ENTER key after tabbing to a button.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

