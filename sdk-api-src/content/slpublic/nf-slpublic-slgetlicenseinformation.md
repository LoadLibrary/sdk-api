---
UID: NF:slpublic.SLGetLicenseInformation
title: SLGetLicenseInformation function (slpublic.h)
description: Gets the specified license information.
helpviewer_keywords: ["SLGetLicenseInformation","SLGetLicenseInformation function [Security]","SL_DATA_BINARY","SL_DATA_DWORD","SL_DATA_SZ","SL_INFO_KEY_DESCRIPTION","SL_INFO_KEY_LICENSE_TYPE","SL_INFO_KEY_VERSION","security.slgetlicenseinformation","slpublic/SLGetLicenseInformation"]
old-location: security\slgetlicenseinformation.htm
tech.root: SecSLApi
ms.assetid: d573bf38-590c-4f8e-a465-9322cbe2b7c4
ms.date: 12/05/2018
ms.keywords: SLGetLicenseInformation, SLGetLicenseInformation function [Security], SL_DATA_BINARY, SL_DATA_DWORD, SL_DATA_SZ, SL_INFO_KEY_DESCRIPTION, SL_INFO_KEY_LICENSE_TYPE, SL_INFO_KEY_VERSION, security.slgetlicenseinformation, slpublic/SLGetLicenseInformation
f1_keywords:
- slpublic/SLGetLicenseInformation
dev_langs:
- c++
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Slc.dll
api_name:
- SLGetLicenseInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SLGetLicenseInformation function


## -description


Gets the specified license information.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pSLLicenseId [in]

Type: <b>const SLID*</b>

A pointer to the license ID.


### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The name associated with the value to retrieve.. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_DESCRIPTION"></a><a id="sl_info_key_description"></a><dl>
<dt><b>SL_INFO_KEY_DESCRIPTION</b></dt>
<dt>L"Description"</dt>
</dl>
</td>
<td width="60%">
The description of the license.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_LICENSE_TYPE"></a><a id="sl_info_key_license_type"></a><dl>
<dt><b>SL_INFO_KEY_LICENSE_TYPE</b></dt>
<dt>L"LicenseType"</dt>
</dl>
</td>
<td width="60%">
The type of the license.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_VERSION"></a><a id="sl_info_key_version"></a><dl>
<dt><b>SL_INFO_KEY_VERSION</b></dt>
<dt>L"Version"</dt>
</dl>
</td>
<td width="60%">
The version of the license.

</td>
</tr>
</table>
 


### -param peDataType [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a>*</b>

A pointer to a value of the <a href="https://docs.microsoft.com/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a> enumeration that specifies the type of data in the <i>ppbValue</i> buffer. Acceptable values are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_SZ"></a><a id="sl_data_sz"></a><dl>
<dt><b>SL_DATA_SZ</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
UNICODE string

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_DWORD"></a><a id="sl_data_dword"></a><dl>
<dt><b>SL_DATA_DWORD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
DWORD

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_BINARY"></a><a id="sl_data_binary"></a><dl>
<dt><b>SL_DATA_BINARY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Binary BLOB

</td>
</tr>
</table>
 


### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.


### -param ppbValue [out]

Type: <b>PBYTE*</b>

If successful, the data is returned in the buffer allocated by SLC.     
		When finished using the memory, free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

</td>
</tr>
</table>
 



