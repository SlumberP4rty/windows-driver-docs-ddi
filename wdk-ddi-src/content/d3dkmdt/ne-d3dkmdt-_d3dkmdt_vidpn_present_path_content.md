---
UID: NE:d3dkmdt._D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
title: _D3DKMDT_VIDPN_PRESENT_PATH_CONTENT (d3dkmdt.h)
description: The D3DKMDT_VIDPN_PRESENT_PATH_CONTENT enumeration is used to indicate the type of content that is displayed on a VidPN present path.
old-location: display\d3dkmdt_vidpn_present_path_content.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["D3DKMDT_VIDPN_PRESENT_PATH_CONTENT enumeration"]
ms.keywords: D3DKMDT_VIDPN_PRESENT_PATH_CONTENT, D3DKMDT_VIDPN_PRESENT_PATH_CONTENT enumeration [Display Devices], D3DKMDT_VPPC_GRAPHICS, D3DKMDT_VPPC_NOTSPECIFIED, D3DKMDT_VPPC_UNINITIALIZED, D3DKMDT_VPPC_VIDEO, DmEnums_000ba351-38c5-4ab5-981c-15e4f44b3765.xml, _D3DKMDT_VIDPN_PRESENT_PATH_CONTENT, d3dkmdt/D3DKMDT_VIDPN_PRESENT_PATH_CONTENT, d3dkmdt/D3DKMDT_VPPC_GRAPHICS, d3dkmdt/D3DKMDT_VPPC_NOTSPECIFIED, d3dkmdt/D3DKMDT_VPPC_UNINITIALIZED, d3dkmdt/D3DKMDT_VPPC_VIDEO, display.d3dkmdt_vidpn_present_path_content
req.header: d3dkmdt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
targetos: Windows
req.typenames: D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
f1_keywords:
 - _D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
 - d3dkmdt/_D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
 - D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
 - d3dkmdt/D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmdt.h
api_name:
 - _D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
 - D3DKMDT_VIDPN_PRESENT_PATH_CONTENT
---

# _D3DKMDT_VIDPN_PRESENT_PATH_CONTENT enumeration


## -description

The D3DKMDT_VIDPN_PRESENT_PATH_CONTENT enumeration is used to indicate the type of content that is displayed on a VidPN present path.

## -enum-fields

### -field D3DKMDT_VPPC_UNINITIALIZED

Indicates that a variable of type D3DKMDT_VIDPN_PRESENT_PATH_CONTENT has not yet been assigned a meaningful value.

### -field D3DKMDT_VPPC_GRAPHICS

Indicates that the path displays graphics content.

### -field D3DKMDT_VPPC_VIDEO

Indicates that the path displays video content.

### -field D3DKMDT_VPPC_NOTSPECIFIED

Indicates that no content type has been specified.

## -remarks

The <b>Content</b> member of a <a href="/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_d3dkmdt_vidpn_present_path">D3DKMDT_VIDPN_PRESENT_PATH</a> structure is a value from the D3DKMDT_VIDPN_PRESENT_PATH_CONTENT enumeration.

