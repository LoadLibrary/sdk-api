---
UID: NF:vds.IVdsLunPlex.QueryExtents
title: IVdsLunPlex::QueryExtents (vds.h)
description: Returns an array of the drive extents that contribute to the plex.
helpviewer_keywords: ["IVdsLunPlex interface [VDS]","QueryExtents method","IVdsLunPlex.QueryExtents","IVdsLunPlex::QueryExtents","QueryExtents","QueryExtents method [VDS]","QueryExtents method [VDS]","IVdsLunPlex interface","base.ivdslunplex_queryextents","vds/IVdsLunPlex::QueryExtents","vdshwprv/IVdsLunPlex::QueryExtents"]
old-location: base\ivdslunplex_queryextents.htm
tech.root: VDS
ms.assetid: e9ed5bdd-c696-47cc-84c8-266b230f7970
ms.date: 12/05/2018
ms.keywords: IVdsLunPlex interface [VDS],QueryExtents method, IVdsLunPlex.QueryExtents, IVdsLunPlex::QueryExtents, QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS],IVdsLunPlex interface, base.ivdslunplex_queryextents, vds/IVdsLunPlex::QueryExtents, vdshwprv/IVdsLunPlex::QueryExtents
f1_keywords:
- vds/IVdsLunPlex.QueryExtents
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IVdsLunPlex.QueryExtents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLunPlex::QueryExtents


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an array of the drive extents that contribute to the plex.


## -parameters




### -param ppExtentArray [out]

A pointer to the array of pointers to drive extents passed in by the caller. These are the extents that contribute to the plex. See the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_extent">VDS_DRIVE_EXTENT</a> structure. Callers must free this array by using the 
      <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


### -param plNumberOfExtents [out]

A pointer to the number of drive extents returned in <i>ppExtentArray</i>.


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
This return value signals a software or communication problem inside a provider that caches information about the array. Use the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method followed by the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore the cache.

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
  
The LUN plex is no longer present.

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
The LUN plex is in a failed state, and is unable to perform the requested operation.

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
Another operation is in progress; this operation cannot proceed until the previous operation or operations are complete.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-queryextents">IVdsDrive::QueryExtents</a> method to get the extents on a given drive.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-queryextents">IVdsDrive::QueryExtents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunplex">IVdsLunPlex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_extent">VDS_DRIVE_EXTENT</a>
 

 

