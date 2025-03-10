---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyAdministratorName
title: IAzAuthorizationStore::AddPolicyAdministratorName (azroles.h)
description: Adds the specified account name to the list of principals that act as policy administrators.
helpviewer_keywords: ["AddPolicyAdministratorName","AddPolicyAdministratorName method [Security]","AddPolicyAdministratorName method [Security]","AzAuthorizationStore object","AddPolicyAdministratorName method [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","AddPolicyAdministratorName method","IAzAuthorizationStore interface [Security]","AddPolicyAdministratorName method","IAzAuthorizationStore.AddPolicyAdministratorName","IAzAuthorizationStore::AddPolicyAdministratorName","azroles/IAzAuthorizationStore::AddPolicyAdministratorName","security.azauthorizationstore_addpolicyadministratorname"]
old-location: security\azauthorizationstore_addpolicyadministratorname.htm
tech.root: SecAuthZ
ms.assetid: b77348c7-4389-47ba-9f4f-e5643cf992aa
ms.date: 12/05/2018
ms.keywords: AddPolicyAdministratorName, AddPolicyAdministratorName method [Security], AddPolicyAdministratorName method [Security],AzAuthorizationStore object, AddPolicyAdministratorName method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyAdministratorName method, IAzAuthorizationStore interface [Security],AddPolicyAdministratorName method, IAzAuthorizationStore.AddPolicyAdministratorName, IAzAuthorizationStore::AddPolicyAdministratorName, azroles/IAzAuthorizationStore::AddPolicyAdministratorName, security.azauthorizationstore_addpolicyadministratorname
f1_keywords:
- azroles/AzAuthorizationStore.AddPolicyAdministratorName
dev_langs:
- c++
req.header: azroles.h
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- AzAuthorizationStore.AddPolicyAdministratorName
- IAzAuthorizationStore.AddPolicyAdministratorName
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzAuthorizationStore::AddPolicyAdministratorName


## -description


The <b>AddPolicyAdministratorName</b> method adds the specified account name to the list of principals that act as policy administrators.

This method is an alternate version of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyadministrator">AddPolicyAdministrator</a> method.


## -parameters




### -param bstrAdmin [in]

Account name  to add to the list of policy administrators. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Policy administrators for an object can perform the following tasks:

<ul>
<li>Read the object</li>
<li>Write attributes to the object</li>
<li>Read attributes of child objects of the object</li>
<li>Write attributes to child objects of the object</li>
<li>Delete the object</li>
<li>Delete child objects of the object</li>
<li>Create child objects of the object</li>
</ul>
To view the list of policy administrators in account name format, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyadministratorsname">PolicyAdministratorsName</a> property.

You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method to persist any changes made by this method.



