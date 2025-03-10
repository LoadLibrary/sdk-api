---
UID: NF:vdshwprv.IVdsSubSystem2.GetDrive2
title: IVdsSubSystem2::GetDrive2 (vdshwprv.h)
description: Returns the specified drive. This method is identical to the IVdsSubSystem::GetDrive method, except that it includes the enclosure number as a parameter.
helpviewer_keywords: ["GetDrive2","GetDrive2 method","GetDrive2 method","IVdsSubSystem2 interface","IVdsSubSystem2 interface","GetDrive2 method","IVdsSubSystem2.GetDrive2","IVdsSubSystem2::GetDrive2","base.ivdssubsystem2_getdrive2","vds/IVdsSubSystem2::GetDrive2","vdshwprv/IVdsSubSystem2::GetDrive2"]
old-location: base\ivdssubsystem2_getdrive2.htm
tech.root: VDS
ms.assetid: 5646da50-5ebd-44d8-b2e1-b3e96b9a6d3c
ms.date: 12/05/2018
ms.keywords: GetDrive2, GetDrive2 method, GetDrive2 method,IVdsSubSystem2 interface, IVdsSubSystem2 interface,GetDrive2 method, IVdsSubSystem2.GetDrive2, IVdsSubSystem2::GetDrive2, base.ivdssubsystem2_getdrive2, vds/IVdsSubSystem2::GetDrive2, vdshwprv/IVdsSubSystem2::GetDrive2
f1_keywords:
- vdshwprv/IVdsSubSystem2.GetDrive2
dev_langs:
- c++
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsSubSystem2.GetDrive2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsSubSystem2::GetDrive2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the specified drive. This method is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getdrive">IVdsSubSystem::GetDrive</a> method, except that it includes the enclosure number as a parameter.


## -parameters




### -param sBusNumber [in]

The number of the bus to which the drive is connected.


### -param sSlotNumber [in]

The number of the slot the drive occupies.


### -param ulEnclosureNumber [in]

The number of the enclosure that contains the drive. This parameter corresponds to the <b>ulEnclosureNumber</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop2">VDS_DRIVE_PROP2</a> structure.


### -param ppDrive [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsdrive">IVdsDrive</a> interface pointer. Callers 
      must release the interface.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
There is a software or communication problem inside a provider that caches information about 
        the array. Use the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> 
        method followed by the  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The subsystem object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The subsystem is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsdrive2">IVdsDrive2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem2">IVdsSubSystem2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getdrive">IVdsSubSystem::GetDrive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querydrives">IVdsSubSystem::QueryDrives</a>
 

 

