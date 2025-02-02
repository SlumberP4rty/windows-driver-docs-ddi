---
UID: NF:fcb.RxFinalizeNetRoot
title: RxFinalizeNetRoot function (fcb.h)
description: RxFinalizeNetRoot finalizes the given NET_ROOT structure. The caller must have an exclusive lock on the netname table associated with the device object.
old-location: ifsk\rxfinalizenetroot.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["RxFinalizeNetRoot function"]
ms.keywords: RxFinalizeNetRoot, RxFinalizeNetRoot function [Installable File System Drivers], fcb/RxFinalizeNetRoot, ifsk.rxfinalizenetroot, rxref_66fb454b-96a0-401b-b184-0c24510bfaf6.xml
req.header: fcb.h
req.include-header: Fcb.h, Mrxfcb.h
req.target-type: Desktop
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
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - RxFinalizeNetRoot
 - fcb/RxFinalizeNetRoot
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fcb.h
api_name:
 - RxFinalizeNetRoot
---

# RxFinalizeNetRoot function


## -description

<b>RxFinalizeNetRoot</b> finalizes the given NET_ROOT structure. The caller must have an exclusive lock on the netname table associated with the device object.

## -parameters

### -param ThisNetRoot [out]


A pointer to the NET_ROOT structure to finalize.

### -param RecursiveFinalize [in]


The value indicating whether the finalization should be done recursively.

### -param ForceFinalize [in]


The value indicating whether the finalization should be forced, regardless of the reference count. 

If <i>ForceFinalize</i> is <b>FALSE</b>, then the <b>NodeReferenceCount</b> member of the NET_ROOT structure pointed to by <i>ThisNetRoot </i>must be 1 for the NET_ROOT to be finalized.

## -returns

<b>RxFinalizeNetRoot</b> returns <b>TRUE</b> on success or <b>FALSE</b> if the finalization did not occur: If a finalization of the NET_ROOT is already in process, <b>RxFinalizeNetRoot</b> will return <b>FALSE</b>.

## -remarks

The <b>RxFinalizeNetRoot</b> routine is not normally called by network mini-redirector drivers directly. RDBSS calls this routine internally when the reference count on the NET_ROOT is decremented to 1.

Before calling <b>RxFinalizeNetRoot</b>, a lock on the netname table associated with the device object must be acquired in exclusive mode. 

If the <i>RecursiveFinalize</i> parameter is <b>TRUE</b>, then <b>RxFinalizeNetRoot</b> will purge any orphaned FCB structures associated with this NET_ROOT. These orphaned FCBs are structures where the <b>FcbState</b> member has the FCB_STATE_ORPHANED flag set on.

## -see-also

<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxcreatenetfcb">RxCreateNetFcb</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxcreatenetfobx">RxCreateNetFobx</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxcreatenetroot">RxCreateNetRoot</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxcreatesrvcall">RxCreateSrvCall</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxcreatesrvopen">RxCreateSrvOpen</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxcreatevnetroot">RxCreateVNetRoot</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxdereference">RxDereference</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxfinalizeconnection">RxFinalizeConnection</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxfinalizenetfcb">RxFinalizeNetFcb</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxfinalizenetfobx">RxFinalizeNetFobx</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxfinalizesrvcall">RxFinalizeSrvCall</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxfinalizesrvopen">RxFinalizeSrvOpen</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxfinalizevnetroot">RxFinalizeVNetRoot</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxfinishfcbinitialization">RxFinishFcbInitialization</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxforcefinalizeallvnetroots">RxForceFinalizeAllVNetRoots</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxreference">RxReference</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxsetsrvcalldomainname">RxSetSrvCallDomainName</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxpdereferencenetfcb">RxpDereferenceNetFcb</a>



<a href="/windows-hardware/drivers/ddi/fcb/nf-fcb-rxpreferencenetfcb">RxpReferenceNetFcb</a>



<a href="/windows-hardware/drivers/ifs/the-net-root-structure">The NET_ROOT Structure</a>
