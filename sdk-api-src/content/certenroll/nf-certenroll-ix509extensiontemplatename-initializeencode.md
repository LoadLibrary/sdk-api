---
UID: NF:certenroll.IX509ExtensionTemplateName.InitializeEncode
title: IX509ExtensionTemplateName::InitializeEncode (certenroll.h)
description: Initializes the extension from a string that contains the template name.
helpviewer_keywords: ["IX509ExtensionTemplateName interface [Security]","InitializeEncode method","IX509ExtensionTemplateName.InitializeEncode","IX509ExtensionTemplateName::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionTemplateName interface","certenroll/IX509ExtensionTemplateName::InitializeEncode","security.ix509extensiontemplatename_initializeencode_method"]
old-location: security\ix509extensiontemplatename_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: 8b72b73a-bfd5-4a56-a106-01f2fd59e922
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplateName interface [Security],InitializeEncode method, IX509ExtensionTemplateName.InitializeEncode, IX509ExtensionTemplateName::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionTemplateName interface, certenroll/IX509ExtensionTemplateName::InitializeEncode, security.ix509extensiontemplatename_initializeencode_method
f1_keywords:
- certenroll/IX509ExtensionTemplateName.InitializeEncode
dev_langs:
- c++
req.header: certenroll.h
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509ExtensionTemplateName.InitializeEncode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionTemplateName::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a string that contains the template name.  This method is web enabled.


## -parameters




### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the name.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



You must call either <b>InitializeEncode</b> or <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplatename-initializedecode">InitializeDecode</a> before you can use an  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplatename-get_templatename">TemplateName</a> property retrieves the template name (the raw extension data).</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a>
 

 

