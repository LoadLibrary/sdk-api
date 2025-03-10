---
UID: NF:vds.IVdsSubSystem.CreateLun
title: IVdsSubSystem::CreateLun (vds.h)
description: Creates a logical unit number (LUN).
helpviewer_keywords: ["CreateLun","CreateLun method [VDS]","CreateLun method [VDS]","IVdsSubSystem interface","IVdsSubSystem interface [VDS]","CreateLun method","IVdsSubSystem.CreateLun","IVdsSubSystem::CreateLun","base.ivdssubsystem_createlun","vds/IVdsSubSystem::CreateLun","vdshwprv/IVdsSubSystem::CreateLun"]
old-location: base\ivdssubsystem_createlun.htm
tech.root: VDS
ms.assetid: e8097364-1f23-4cda-8f12-a750bbb4eb4c
ms.date: 12/05/2018
ms.keywords: CreateLun, CreateLun method [VDS], CreateLun method [VDS],IVdsSubSystem interface, IVdsSubSystem interface [VDS],CreateLun method, IVdsSubSystem.CreateLun, IVdsSubSystem::CreateLun, base.ivdssubsystem_createlun, vds/IVdsSubSystem::CreateLun, vdshwprv/IVdsSubSystem::CreateLun
f1_keywords:
- vds/IVdsSubSystem.CreateLun
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
- IVdsSubSystem.CreateLun
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsSubSystem::CreateLun


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

The <b>CreateLun</b> method creates a logical unit number (LUN).


## -parameters




### -param type [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value that specifies the LUN type. The new 
      LUN can be an automagic type or a specific RAID type, but not both. If the caller specifies an automagic type, one or more automagic hints should be specified in the <i>pHints</i> parameter. 

The interface pointer for the new 
      <a href="https://docs.microsoft.com/windows/desktop/VDS/lun-object">LUN object</a> can be retrieved by calling the 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method on the interface pointer returned in the 
      <i>ppAsync</i> parameter. The 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure returned by <b>Wait</b>  contains the 
      LUN object interface pointer in the <b>cl.pLunUnk</b> member.


### -param ullSizeInBytes [in]

The size, in bytes, of the new LUN. The provider can round the size up or down to meet alignment 
      requirements or other restrictions. (In most cases, the provider rounds up, ensuring that, with rare 
      exceptions, the LUN is at least as large as requested.) 
      

After the LUN is created, the caller can determine the actual size of the LUN by calling the 
       <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method.


### -param pDriveIdArray [in]

A pointer to an array that contains a <a href="https://docs.microsoft.com/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> for each of the drives to be used to create the LUN. By specifying a non-<b>NULL</b> value for this parameter, the caller is requesting that the provider use all of the drives, in the order provided, using all of the extents on one drive before moving on to the 
      next, and stopping when the LUN has reached the requested size. 
      

Alternatively, the caller can direct the provider to select the drives automatically by passing 
       <b>NULL</b> in this parameter and 0 in <i>lNumberOfDrives</i>. (Pass 
       <b>NULL</b> if and only if <i>lNumberOfDrives</i> is 0.)

If the <i>type</i> parameter specifies an automagic type, this parameter should be <b>NULL</b>.


### -param lNumberOfDrives [in]

The number of drives specified in <i>pDriveIdArray</i>. If the caller passes 0, the 
      provider selects the drives.
      

If the <i>type</i> parameter specifies an automagic type, this parameter should be 0.

After the LUN is created, the caller can determine which drives are in use by calling the 
       <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a> method.


### -param pwszUnmaskingList [in]

A list specifying the computers to be granted access the LUN. The list is a 
      semicolon-delimited, <b>NULL</b>-terminated, human-readable string. 

If the value is "*", all computers that have an HBA port attached to the storage subsystem are to be granted access to the LUN. If the value is "", no computers are to be granted access to the LUN.
      <div class="alert"><b>Note</b>  In practice, if the value is "*", most hardware providers only grant the ports and initiators on the local computer access to the LUN.</div>
<div> </div>


If "*" or "" is specified, no other value can be specified.

For Fibre Channel networks and serial attached SCSI (SAS) networks, each entry is a 64-bit World-Wide Name (WWN) of each port to which the LUN is unmasked, 
       formatted as a hexadecimal string (16 characters long), most significant byte first. For 
       example, a WWN address of 01:23:45:67:89:AB:CD:EF is represented as "0123456789ABCDEF". For more information, see the T10 specifications for <a href="https://t10.org/drafts.htm#FibreChannel">Fibre Channel</a> and <a href="https://t10.org/drafts.htm#SCSI3_SAS">SAS</a>.

For iSCSI networks, each entry is an iSCSI qualified name (IQN) of each initiator to which the LUN is unmasked. A LUN unmasked 
       to a particular initiator is considered to be associated with that initiator.

<div class="alert"><b>Note</b>  The unmasking list can contain the same WWN or IQN more than once. The caller is not expected to remove 
       duplicates from the list or to validate the format of the WWN or IQN.</div>
<div> </div>
After the LUN is created, the caller can determine the actual unmasking list by calling the 
       <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method.


### -param pHints [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure that specifies the hints to be used in creating the LUN. The provider is not required to apply the hints to the LUN. The hints specified in the VDS_HINTS structure are only a request to the provider.

After the LUN is created, the caller can determine the hints that the provider applied by calling either the 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a> method or 
      the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryhints">IVdsLunPlex::QueryHints</a> method.

If the <i>type</i> parameter specifies a non-automagic type, this parameter should be <b>NULL</b>.


### -param ppAsync [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, 
      which VDS initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or 
      query the status of the operation.

If <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> is called on the returned interface pointer and a success HRESULT value is returned, 
      the interfaces returned in the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> 
      structure must be released by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.


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
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method
        followed by the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This 
        return value indicates that the identifier does not refer to an existing object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_ENOUGH_SPACE</b></dt>
<dt>0x8004240FL</dt>
</dl>
</td>
<td width="60%">
There is not enough usable space for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_ENOUGH_DRIVE</b></dt>
<dt>0x80042410L</dt>
</dl>
</td>
<td width="60%">
Too few free drives are present in the subsystem to complete this operation.

</td>
</tr>
</table>
 




## -remarks



By choosing appropriate values for the <i>type</i> and <i>pHints</i> parameters, the caller can specify the attributes of the LUN wholly, partially, or minimally. The provider can 
    automatically include unspecified attributes, based on the automagic hints specified in the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure that the <i>pHints</i> parameter points to.

If the VDS provider supports only simple target configurations, the subsystem should automatically associate the newly created LUN object with an iSCSI target object. See the <b>VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG</b> value of the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

The list of WWNs and IQNs in the <i>pwszUnmaskingList</i> parameter may contain duplicate names. It is the provider's responsibility to validate all names in the list and remove duplicates if necessary.

The hardware provider is responsible for removing the LUN's partition information so that the LUN can be reused. If the LUN is an MBR disk, this is accomplished by writing zeros to the first and last 1 MB of the disk. For a GPT disk, zeros must be written to the first and last 16 KB of the disk.

There is a subtle difference between the <b>E_INVALIDARG</b> and 
    <b>VDS_E_NOT_SUPPORTED</b> return values. Providers are not expected to implement every feature that the VDS 
    API can present to a client. For example, the 
    <b>CreateLun</b> method exposes the ability to 
    create many different types of LUNs (for example, simple, mirror, striped, and parity). However, providers are not required to support all 
    types of LUNs. If the caller specifies a value for the <i>type</i> parameter that is not a valid <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value, the provider should return <b>E_INVALIDARG</b>. If the caller specifies a valid <i>type</i> value that the provider does not support, the provider should return VDS_E_NOT_SUPPORTED.

<b>Notes to implementers:  </b>The provider must return an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer in the <i>ppAsync</i> parameter, even if the call to this method does not initiate an asynchronous operation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryhints">IVdsLunPlex::QueryHints</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-queryluns">IVdsSubSystem::QueryLuns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>
 

 

