---
UID: NS:vdshwprv._VDS_CONTROLLER_NOTIFICATION
title: VDS_CONTROLLER_NOTIFICATION (vdshwprv.h)
description: Defines the details of controller events.
helpviewer_keywords: ["VDS_CONTROLLER_NOTIFICATION","VDS_CONTROLLER_NOTIFICATION structure [VDS]","VDS_NF_CONTROLLER_ARRIVE","VDS_NF_CONTROLLER_DEPART","VDS_NF_CONTROLLER_MODIFY","VDS_NF_CONTROLLER_REMOVED","base.vds_controller_notification","vds/_VDS_CONTROLLER_NOTIFICATION","vdshwprv/_VDS_CONTROLLER_NOTIFICATION"]
old-location: base\vds_controller_notification.htm
tech.root: VDS
ms.assetid: de2aa5d8-b9b0-4e3d-9846-e886ac1d4241
ms.date: 12/05/2018
ms.keywords: VDS_CONTROLLER_NOTIFICATION, VDS_CONTROLLER_NOTIFICATION structure [VDS], VDS_NF_CONTROLLER_ARRIVE, VDS_NF_CONTROLLER_DEPART, VDS_NF_CONTROLLER_MODIFY, VDS_NF_CONTROLLER_REMOVED, base.vds_controller_notification, vds/_VDS_CONTROLLER_NOTIFICATION, vdshwprv/_VDS_CONTROLLER_NOTIFICATION
f1_keywords:
- vdshwprv/VDS_CONTROLLER_NOTIFICATION
dev_langs:
- c++
req.header: vdshwprv.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- VDS_CONTROLLER_NOTIFICATION
targetos: Windows
req.typenames: VDS_CONTROLLER_NOTIFICATION
req.redist: 
ms.custom: 19H1
---

# VDS_CONTROLLER_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of controller events.


## -struct-fields




### -field ulEvent

Determines the controller event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_CONTROLLER_ARRIVE"></a><a id="vds_nf_controller_arrive"></a><dl>
<dt><b>VDS_NF_CONTROLLER_ARRIVE</b></dt>
<dt>103</dt>
</dl>
</td>
<td width="60%">
A controller is reported as physically present on the subsystem. The <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a> value associated with this notification should be any value except <b>VDS_CS_REMOVED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_CONTROLLER_DEPART"></a><a id="vds_nf_controller_depart"></a><dl>
<dt><b>VDS_NF_CONTROLLER_DEPART</b></dt>
<dt>104</dt>
</dl>
</td>
<td width="60%">
A controller was physically removed from the subsystem.  The <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a> value should be <b>VDS_CS_UNKNOWN</b> or <b>VDS_CS_REMOVED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_CONTROLLER_MODIFY"></a><a id="vds_nf_controller_modify"></a><dl>
<dt><b>VDS_NF_CONTROLLER_MODIFY</b></dt>
<dt>350</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_controller_prop">VDS_CONTROLLER_PROP</a> structure changed.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_CONTROLLER_REMOVED"></a><a id="vds_nf_controller_removed"></a><dl>
<dt><b>VDS_NF_CONTROLLER_REMOVED</b></dt>
<dt>351</dt>
</dl>
</td>
<td width="60%">
A controller is physically present but not available for use. The <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a> value should be <b>VDS_CS_FAILED</b> (removed from use because of failure), <b>VDS_CS_ONLINE</b>  (not failed, but not in use either), <b>VDS_CS_NOT_READY</b>,  or <b>VDS_CS_UNKNOWN</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

</td>
</tr>
</table>
 


### -field controllerId

The GUID of the controller that triggered the event.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this structure as a member.

An application can receive controller events by implementing the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface pointer as an argument to the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method.

To get the controller object, use the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getproperties">IVdsController::GetProperties</a> method to get the controller properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
 

 

