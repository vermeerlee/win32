---
title: MOUNTMGR\_TARGET\_NAME structure
description: The MOUNTMGR\_TARGET\_NAME structure contains the nonpersistent target device name for a device and is used by mount manager clients with the IOCTL\_MOUNTMGR\_KEEP\_LINKS\_WHEN\_OFFLINE request to tell the mount manager to keep the symbolic link for a device active even after the device has gone offline.
ms.assetid: 7a9cdc0d-0275-4ef9-a570-8788f77099af
keywords:
- MOUNTMGR_TARGET_NAME structure Storage Devices
- PMOUNTMGR_TARGET_NAME structure pointer Storage Devices
topic_type:
- apiref
api_name:
- MOUNTMGR_TARGET_NAME
api_location:
- mountmgr.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: structure
ms.date: 05/31/2018
---

# MOUNTMGR\_TARGET\_NAME structure

The MOUNTMGR\_TARGET\_NAME structure contains the nonpersistent target device name for a device and is used by mount manager clients with the [**IOCTL\_MOUNTMGR\_KEEP\_LINKS\_WHEN\_OFFLINE**](ioctl-mountmgr-keep-links-when-offline.md) request to tell the mount manager to keep the symbolic link for a device active even after the device has gone offline.

## Syntax


```C++
typedef struct _MOUNTMGR_TARGET_NAME {
  USHORT DeviceNameLength;
  WCHAR  DeviceName[1];
} MOUNTMGR_TARGET_NAME, *PMOUNTMGR_TARGET_NAME;
```



## Members

<dl> <dt>

**DeviceNameLength**
</dt> <dd>

Contains the length, in bytes, of the device name stored in **DeviceName**.

</dd> <dt>

**DeviceName**
</dt> <dd>

Contains the nonpersistent target device name.

</dd> </dl>

## Remarks

Nonpersistent target names must contain the full path of a target object name in the system object tree. For example: "\\Device\\HarddiskVolume1". For a discussion of the different between symbolic links, unique IDs, and nonpersistent device names, see [Supporting Mount Manager Requests in a Storage Class Driver](https://msdn.microsoft.com/library/windows/hardware/ff567603).

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mountmgr.h (include Mountmgr.h)</dt> </dl> |



## See also

<dl> <dt>

[**IOCTL\_MOUNTMGR\_KEEP\_LINKS\_WHEN\_OFFLINE**](ioctl-mountmgr-keep-links-when-offline.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20MOUNTMGR_TARGET_NAME%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





