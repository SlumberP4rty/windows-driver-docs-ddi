---
UID: NF:netdevice.NetDeviceOpenConfiguration
title: NetDeviceOpenConfiguration function (netdevice.h)
description: The NetDeviceOpenConfiguration function opens a net device's configuration database.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NetDeviceOpenConfiguration function"]
ms.keywords: NetDeviceOpenConfiguration
req.header: netdevice.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.27
req.umdf-ver: 2.33 
req.lib: netadaptercxstub.lib
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
 - NetDeviceOpenConfiguration
 - netdevice/NetDeviceOpenConfiguration
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetDeviceOpenConfiguration
---

# NetDeviceOpenConfiguration function


## -description

The **NetDeviceOpenConfiguration** function opens a net device's configuration database.

## -parameters

### -param Device [_In_]

The WDFDEVICE object the client driver previously created with a call to [**WdfDeviceCreate**](../wdfdevice/nf-wdfdevice-wdfdevicecreate.md).

### -param ConfigurationAttributes [_In_opt_]

A pointer to a [**WDF_OBJECT_ATTRIBUTES**](../wdfobject/ns-wdfobject-_wdf_object_attributes.md) structure that contains driver-supplied attributes for the new configuration object. This parameter is optional and can be **WDF_NO_OBJECT_ATTRIBUTES**.

### -param Configuration [_Out_]

A pointer to the location that receives the new NETCONFIGURATION object.

## -returns

This function returns STATUS_SUCCESS if the operation succeeds. Otherwise, this function may return an appropriate NTSTATUS error code.

## -remarks

Typically, the client calls this function from its [*EVT_WDF_DRIVER_DEVICE_ADD*](../wdfdriver/nc-wdfdriver-evt_wdf_driver_device_add.md) callback function.

If the client provides a [**WDF_OBJECT_ATTRIBUTES**](../wdfobject/ns-wdfobject-_wdf_object_attributes.md), it specifies **NULL** for **ParentObject**. The device configuration object is automatically parented to the device object.

As a result, WDF automatically deletes the configuration object when the device is deleted. However, the client can manually delete a configuration object by calling [**WdfObjectDelete**](../wdfobject/nf-wdfobject-wdfobjectdelete.md), typically from its [*EVT_WDF_OBJECT_CONTEXT_CLEANUP*](../wdfobject/nc-wdfobject-evt_wdf_object_context_cleanup.md) callback function.

## -see-also

[Accessing configuration information](/windows-hardware/drivers/netcx/accessing-configuration-information)
