---
UID: NF:fwpmu.IkeextSaDbGetSecurityInfo0
title: IkeextSaDbGetSecurityInfo0 function (fwpmu.h)
description: The IkeextSaDbGetSecurityInfo0 function retrieves a copy of the security descriptor for a security association (SA) database.
helpviewer_keywords: ["IkeextSaDbGetSecurityInfo0","IkeextSaDbGetSecurityInfo0 function [Filtering]","fwp.ikeextsadbgetsecurityinfo0","fwpmu/IkeextSaDbGetSecurityInfo0"]
old-location: fwp\ikeextsadbgetsecurityinfo0.htm
tech.root: fwp
ms.assetid: e84fef94-3e75-4812-8427-b20a023588fa
ms.date: 12/05/2018
ms.keywords: IkeextSaDbGetSecurityInfo0, IkeextSaDbGetSecurityInfo0 function [Filtering], fwp.ikeextsadbgetsecurityinfo0, fwpmu/IkeextSaDbGetSecurityInfo0
f1_keywords:
- fwpmu/IkeextSaDbGetSecurityInfo0
dev_langs:
- c++
req.header: fwpmu.h
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Fwpuclnt.dll
api_name:
- IkeextSaDbGetSecurityInfo0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IkeextSaDbGetSecurityInfo0 function


## -description


The <b>IkeextSaDbGetSecurityInfo0</b> function retrieves a copy of the security descriptor for a security association (SA) database.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine generated by a previous  call to  <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a>.


### -param securityInfo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a></b>

The type of security information to retrieve.


### -param sidOwner [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">PSID</a>*</b>

The owner security identifier (SID) in the returned security descriptor.


### -param sidGroup [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">PSID</a>*</b>

The primary group security identifier (SID) in the returned security descriptor.


### -param dacl [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">PACL</a>*</b>

The discretionary access control list (DACL) in the returned security descriptor.


### -param sacl [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">PACL</a>*</b>

The system access control list (SACL) in the returned security descriptor.


### -param securityDescriptor [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a>*</b>

The returned security descriptor.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The security descriptor was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



The returned <i>securityDescriptor</i> parameter must be freed through a call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>. The other four (optional) returned parameters must not be freed, as they point to addresses within the <i>securityDescriptor</i> parameter.

This function behaves like the standard Win32 	<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>GetSecurityInfo</b> reference topic.

<b>IkeextSaDbGetSecurityInfo0</b> is a specific implementation of IkeextSaDbGetSecurityInfo. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0">IkeextSaDbSetSecurityInfo0</a>
 

 

