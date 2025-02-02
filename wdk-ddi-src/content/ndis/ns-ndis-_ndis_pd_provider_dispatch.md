---
UID: NS:ndis._NDIS_PD_PROVIDER_DISPATCH
title: _NDIS_PD_PROVIDER_DISPATCH (ndis.h)
description: This structure is used as input for the OID_PD_OPEN_PROVIDER and serves as a container for all the provider's driver routines.
old-location: netvista\ndis_pd_provider_dispatch.htm
tech.root: netvista
ms.date: 05/02/2018
keywords: ["NDIS_PD_PROVIDER_DISPATCH structure"]
ms.keywords: NDIS_PD_PROVIDER_DISPATCH, NDIS_PD_PROVIDER_DISPATCH structure [Network Drivers Starting with Windows Vista], PNDIS_PD_PROVIDER_DISPATCH, PNDIS_PD_PROVIDER_DISPATCH structure pointer [Network Drivers Starting with Windows Vista], _NDIS_PD_PROVIDER_DISPATCH, ndis/NDIS_PD_PROVIDER_DISPATCH, ndis/PNDIS_PD_PROVIDER_DISPATCH, netvista.ndis_pd_provider_dispatch
req.header: ndis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.typenames: NDIS_PD_PROVIDER_DISPATCH
f1_keywords:
 - _NDIS_PD_PROVIDER_DISPATCH
 - ndis/_NDIS_PD_PROVIDER_DISPATCH
 - NDIS_PD_PROVIDER_DISPATCH
 - ndis/NDIS_PD_PROVIDER_DISPATCH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ndis.h
api_name:
 - _NDIS_PD_PROVIDER_DISPATCH
 - NDIS_PD_PROVIDER_DISPATCH
---

# _NDIS_PD_PROVIDER_DISPATCH structure


## -description

This structure is used as input for the <a href="/windows-hardware/drivers/network/oid-pd-open-provider">OID_PD_OPEN_PROVIDER</a> and serves as a container for all the provider's driver routines.

## -struct-fields

### -field Header

The <a href="/windows-hardware/drivers/ddi/objectheader/ns-objectheader-ndis_object_header">NDIS_OBJECT_HEADER</a> structure for the <b>NDIS_PD_PROVIDER_DISPATCH</b> structure. Set the members of this structure as follows:

<ul>
<li><b>Type</b> = <b>NDIS_OBJECT_TYPE_DEFAULT</b></li>
<li><b>Revision</b> = <b>NDIS_PD_PROVIDER_DISPATCH_REVISION_1</b></li>
<li><b>Size</b> = <b>NDIS_SIZEOF_PD_PROVIDER_DISPATCH_REVISION_1</b></li>
</ul>

### -field Flags

This member is reserved and must be set to 0 by the provider.

### -field NdisPDAllocateQueue

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_allocate_queue">NdisPDAllocateQueue</a>.

### -field NdisPDFreeQueue

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_free_queue">NdisPDFreeQueue</a>.

### -field NdisPDAcquireReceiveQueues

### -field NdisPDReleaseReceiveQueues

### -field NdisPDAllocateCounter

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_allocate_counter">NdisPDAllocateCounter</a>.

### -field NdisPDFreeCounter

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_free_counter">NdisPDFreeCounter</a>.

### -field NdisPDQueryCounter

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_query_counter">NdisPDQueryCounter</a>.

### -field NdisPDSetReceiveFilter

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_set_receive_filter">NdisPDSetReceiveFilter</a>.

### -field NdisPDClearReceiveFilter

See <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-ndis_pd_clear_receive_filter">NdisPDClearReceiveFilter</a>.

### -field NdisPDRequestDrainNotification

### -field NdisPDQueueControl

### -field NdisPDProviderControl


## -see-also

<a href="/windows-hardware/drivers/ddi/objectheader/ns-objectheader-ndis_object_header">NDIS_OBJECT_HEADER</a>

