---
UID: NS:d3d11.D3D11_TEX2D_SRV
title: D3D11_TEX2D_SRV (d3d11.h)
description: Specifies the subresource from a 2D texture to use in a shader-resource view.
helpviewer_keywords: ["54ba00bb-9aec-6653-324a-0b65dc123c63","D3D11_TEX2D_SRV","D3D11_TEX2D_SRV structure [Direct3D 11]","d3d11/D3D11_TEX2D_SRV","direct3d11.d3d11_tex2d_srv"]
old-location: direct3d11\d3d11_tex2d_srv.htm
tech.root: direct3d11
ms.assetid: 2edfe9bd-6f26-4007-a2bd-0911649e7237
ms.date: 12/05/2018
ms.keywords: 54ba00bb-9aec-6653-324a-0b65dc123c63, D3D11_TEX2D_SRV, D3D11_TEX2D_SRV structure [Direct3D 11], d3d11/D3D11_TEX2D_SRV, direct3d11.d3d11_tex2d_srv
f1_keywords:
- d3d11/D3D11_TEX2D_SRV
dev_langs:
- c++
req.header: d3d11.h
req.include-header: 
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
- HeaderDef
api_location:
- D3D11.h
api_name:
- D3D11_TEX2D_SRV
targetos: Windows
req.typenames: D3D11_TEX2D_SRV
req.redist: 
ms.custom: 19H1
---

# D3D11_TEX2D_SRV structure


## -description


Specifies the subresource from a 2D texture to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture2D for which <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.


### -field MipLevels

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
 

 

