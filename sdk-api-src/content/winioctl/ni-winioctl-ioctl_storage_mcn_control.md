---
UID: NI:winioctl.IOCTL_STORAGE_MCN_CONTROL
title: IOCTL_STORAGE_MCN_CONTROL
description: Enables or disables media change notification. Disabling media change notification prevents the GUID_IO_MEDIA_ARRIVAL and GUID_IO_MEDIA_REMOVAL events.
helpviewer_keywords: ["IOCTL_STORAGE_MCN_CONTROL","IOCTL_STORAGE_MCN_CONTROL control","IOCTL_STORAGE_MCN_CONTROL control code","_win32_ioctl_storage_mcn_control","base.ioctl_storage_mcn_control","winioctl/IOCTL_STORAGE_MCN_CONTROL"]
old-location: base\ioctl_storage_mcn_control.htm
tech.root: devio
ms.assetid: 1122f27f-c1a6-49a9-b09a-5b33c451e1cc
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_MCN_CONTROL, IOCTL_STORAGE_MCN_CONTROL control, IOCTL_STORAGE_MCN_CONTROL control code, _win32_ioctl_storage_mcn_control, base.ioctl_storage_mcn_control, winioctl/IOCTL_STORAGE_MCN_CONTROL
f1_keywords:
- winioctl/IOCTL_STORAGE_MCN_CONTROL
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
- WinIoCtl.h
api_name:
- IOCTL_STORAGE_MCN_CONTROL
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_MCN_CONTROL IOCTL

## -description

Enables or disables media change notification. Disabling media change notification prevents the **GUID_IO_MEDIA_ARRIVAL** and **GUID_IO_MEDIA_REMOVAL** events.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_STORAGE_MCN_CONTROL,    // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```


## -ioctlparameters

### -input-buffer


### -input-buffer-length


### -output-buffer


### -output-buffer-length


### -in-out-buffer


### -inout-buffer-length


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).


## -see-also

* [Device Management Control Codes](https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
