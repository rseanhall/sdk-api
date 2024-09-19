---
UID: NF:dxcore_interface.IDXCoreAdapterFactory1.CreateAdapterListByWorkload(DXCoreWorkload,DXCoreRuntimeFilterFlags,DXCoreHardwareTypeFilterFlags,T)
title: IDXCoreAdapterFactory1::CreateAdapterListByWorkload
description: Generates a list of adapter objects representing the current adapter state of the system, and meeting the workload and hardware type criteria specified.
tech.root: dxcore
ms.date: 09/18/2024
ms.localizationpriority: low
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: method
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - COM
api_location:
 - dxcore.dll
api_name:
 - IDXCoreAdapterFactory1::CreateAdapterListByWorkload
f1_keywords:
 - IDXCoreAdapterFactory1::CreateAdapterListByWorkload
 - dxcore_interface/IDXCoreAdapterFactory1::CreateAdapterListByWorkload
dev_langs:
 - c++
helpviewer_keywords:
 - CreateAdapterListByWorkload
---

## -description

Generates a list of adapter objects representing the current adapter state of the system, and meeting the workload and hardware type criteria specified. For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters). With **CreateAdapterListByWorkload**, DXCore supports neural processing units (NPUs), which process machine-learning (ML) workloads, and media accelerators, for video encode/decode/processing workloads.

You can retrieve MCDM NPUs and media accelerators by calling [CreateAdapterList](./nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md), but the default sorting for that method is based on runtime capabilities and device performance. **CreateAdapterListByWorkload** allows DXCore to provide an adapter list sorted by what works best for a given workload, based on operating system (OS) policy, that you can easily narrow down by the type of hardware and level of Direct 3D runtime support. The default sorting in **CreateAdapterListByWorkload** can be thought of as the opposite of **CreateAdapterList**, where more specialized hardware is prioritized in the ordering that may be less generally capable than a full GPU.

## -parameters

### -param workload

TBD

### -param runtimeFilter

TBD

### -param hardwareTypeFilter

### -param ppvAdapterList [out]

Type: **void\*\***

The address of a pointer to an interface meeting the workload and hardware type criteria specified. Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|A value was provided outside of the range of the *workload*, *runtimeFilter*, or *hardwareTypeFilter* parameters.|
|E_POINTER|`nullptr` was provided for *ppvAdapterList*.|

## -remarks

## -see-also

[IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory), [DXCore reference](/windows/win32/dxcore/dxcore-reference), [DXCore adapter attribute GUIDs](/windows/win32/dxcore/dxcore-adapter-attribute-guids), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
