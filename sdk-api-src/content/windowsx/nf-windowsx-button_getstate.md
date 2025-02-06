---
UID: NF:windowsx.Button_GetState
title: Button_GetState macro (windowsx.h)
description: Retrieves the state of a button or check box. You can use this macro or send the BM_GETSTATE message explicitly.
helpviewer_keywords: ["Button_GetState","Button_GetState macro [Windows Controls]","_win32_Button_GetState","_win32_Button_GetState_cpp","controls.Button_GetState","controls._win32_Button_GetState","windowsx/Button_GetState"]
old-location: controls\Button_GetState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getstate.htm
ms.date: 10/21/2024
ms.keywords: Button_GetState, Button_GetState macro [Windows Controls], _win32_Button_GetState, _win32_Button_GetState_cpp, controls.Button_GetState, controls._win32_Button_GetState, windowsx/Button_GetState
req.header: windowsx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Button_GetState
 - windowsx/Button_GetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Button_GetState
---

# Button_GetState macro

## -syntax

```cpp
LRESULT Button_GetState(
   HWND hwndCtl
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

The return value specifies the current state of the button. It is a combination of the following values:

| Return code | Description |
|---|---|
| BST_CHECKED | The button is checked. |
| BST_DROPDOWNPUSHED | Windows Vista. The button is in the drop-down state. Applies only if the button has the TBSTYLE_DROPDOWN style. |
| BST_FOCUS | The button has the keyboard focus. |
| BST_HOT | The button is hot; that is, the mouse is hovering over it. |
| BST_INDETERMINATE | The state of the button is indeterminate. Applies only if the button has the BS_3STATE or BS_AUTO3STATE style. |
| BST_PUSHED | The button is being shown in the pushed state. |
| BST_UNCHECKED | No special state. Equivalent to zero. |



## -description

Retrieves the state of a button or check box.  You can use this macro or send the <a href="/windows/desktop/Controls/bm-getstate">BM_GETSTATE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

## -see-also

<a href="/windows/desktop/api/windowsx/nf-windowsx-button_getcheck">Button_GetCheck</a>



<a href="/windows/desktop/api/windowsx/nf-windowsx-button_setstate">Button_SetState</a>



<b>Reference</b>
