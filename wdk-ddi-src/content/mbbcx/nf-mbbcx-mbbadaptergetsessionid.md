---
UID: NF:mbbcx.MbbAdapterGetSessionId
title: MbbAdapterGetSessionId function (mbbcx.h)
description: The MbbAdapterGetSessionId method retrieves the data session ID represented by the given NETADAPTER object.
tech.root: netvista
ms.date: 06/29/2018
keywords: ["MbbAdapterGetSessionId function"]
ms.keywords: MbbAdapterGetSessionId
req.header: mbbcx.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 10, version 1809
req.target-min-winversvr: 
req.kmdf-ver: 1.27
req.umdf-ver: 
req.lib: mbbcxstub.lib
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: RS5
f1_keywords:
 - MbbAdapterGetSessionId
 - mbbcx/MbbAdapterGetSessionId
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mbbcxstub.lib
api_name:
 - MbbAdapterGetSessionId
---

# MbbAdapterGetSessionId function


## -description

The **MbbAdapterGetSessionId** method retrieves the data session ID represented by the given NETADAPTER object.

## -parameters

### -param Adapter

A handle to a NetAdapterCx NETADAPTER object previously created with a call to [**NetAdapterCreate**](../netadapter/nf-netadapter-netadaptercreate.md) and initialized with [**MbbAdapterInitialize**](nf-mbbcx-mbbadapterinitialize.md).

## -returns

Returns the data session's ID to the network interface represented by the NETADAPTER object.

## -remarks

The client driver must call [**MbbAdapterInitialize**](nf-mbbcx-mbbadapterinitialize.md) first before calling this method. 

For more information, see [Creating the NetAdapter interface for the PDP context/EPS bearer](/windows-hardware/drivers/netcx/writing-an-mbbcx-client-driver#creating-the-netadapter-interface-for-the-pdp-contexteps-bearer).

## -see-also
