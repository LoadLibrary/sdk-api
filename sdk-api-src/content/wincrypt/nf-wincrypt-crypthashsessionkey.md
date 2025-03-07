---
UID: NF:wincrypt.CryptHashSessionKey
title: CryptHashSessionKey function (wincrypt.h)
description: Computes the cryptographic hash of a session key object.
helpviewer_keywords: ["CRYPT_LITTLE_ENDIAN","CryptHashSessionKey","CryptHashSessionKey function [Security]","_crypto2_crypthashsessionkey","security.crypthashsessionkey","wincrypt/CryptHashSessionKey"]
old-location: security\crypthashsessionkey.htm
tech.root: SecCrypto
ms.assetid: 75781993-7faf-4149-80cc-ae50dbd4de2a
ms.date: 12/05/2018
ms.keywords: CRYPT_LITTLE_ENDIAN, CryptHashSessionKey, CryptHashSessionKey function [Security], _crypto2_crypthashsessionkey, security.crypthashsessionkey, wincrypt/CryptHashSessionKey
f1_keywords:
- wincrypt/CryptHashSessionKey
dev_langs:
- c++
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-Security-cryptoapi-l1-1-0.dll
- cryptsp.dll
api_name:
- CryptHashSessionKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptHashSessionKey function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptHashSessionKey</b> function computes the cryptographic <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash</a> of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">session key</a> object. This function can be called multiple times with the same hash handle to compute the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash</a> of multiple keys. Calls to <b>CryptHashSessionKey</b> can be interspersed with calls to 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>.

Before calling this function, 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a> must be called to create the handle of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash object</a>.


## -parameters




### -param hHash [in]

A handle to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash object</a>.


### -param hKey [in]

A handle to the key object to be hashed.


### -param dwFlags [in]

The following flag value is defined. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LITTLE_ENDIAN"></a><a id="crypt_little_endian"></a><dl>
<dt><b>CRYPT_LITTLE_ENDIAN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
When this flag is set, the bytes of the key are hashed in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">little-endian</a> form. Note that by default (when <i>dwFlags</i> is zero), the bytes of the key are hashed in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/b-gly">big-endian</a> form.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP you are using. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hHash</i> handle specifies an algorithm that this CSP does not support.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is nonzero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_HASH</b></dt>
</dl>
</td>
<td width="60%">
The hash object specified by the <i>hHash</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_HASH_STATE</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to add data to a hash object that is already marked "finished."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEY</b></dt>
</dl>
</td>
<td width="60%">
A keyed hash algorithm is being used, but the session key is no longer valid. This error is generated if the session key is destroyed before the hashing operation is complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the hash object was created cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The function failed in some unexpected way.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Hash and Digital Signature Functions</a>
 

 

