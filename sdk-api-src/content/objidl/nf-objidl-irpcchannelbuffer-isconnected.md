---
UID: NF:objidl.IRpcChannelBuffer.IsConnected
title: IRpcChannelBuffer::IsConnected (objidl.h)
description: Determines whether the RPC channel is connected.
helpviewer_keywords: ["IRpcChannelBuffer interface [COM]","IsConnected method","IRpcChannelBuffer.IsConnected","IRpcChannelBuffer::IsConnected","IsConnected","IsConnected method [COM]","IsConnected method [COM]","IRpcChannelBuffer interface","_com_irpcchannelbuffer_isconnected","com.irpcchannelbuffer_isconnected","objidlbase/IRpcChannelBuffer::IsConnected"]
old-location: com\irpcchannelbuffer_isconnected.htm
tech.root: com
ms.assetid: 4068f0bb-35fb-452b-8ab1-1a38b1a0c2fa
ms.date: 12/05/2018
ms.keywords: IRpcChannelBuffer interface [COM],IsConnected method, IRpcChannelBuffer.IsConnected, IRpcChannelBuffer::IsConnected, IsConnected, IsConnected method [COM], IsConnected method [COM],IRpcChannelBuffer interface, _com_irpcchannelbuffer_isconnected, com.irpcchannelbuffer_isconnected, objidlbase/IRpcChannelBuffer::IsConnected
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRpcChannelBuffer::IsConnected
 - objidl/IRpcChannelBuffer::IsConnected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcChannelBuffer.IsConnected
---

# IRpcChannelBuffer::IsConnected


## -description

Determines whether the RPC channel is connected.



## -returns

If the RPC channel knows that the server object has been disconnected,
the return value is <b>S_FALSE</b>. Otherwise, it is <b>S_OK</b>.

## -remarks

Channel implementations typically report server connectedness based on their
local state and are not expected to test transport-level connections or make
any calls to the server to prove connectedness.
It is possible for this method to return <b>S_OK</b>
even when the server object has been disconnected.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>
