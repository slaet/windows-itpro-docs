---
title: RemoteWipe DDF file
description: RemoteWipe DDF file
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 10ec4fb7-f911-4d0c-9a8f-e96bf5faea0c
ms.author: windows-hardware-design-content
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# RemoteWipe DDF file


This topic shows the OMA DM device description framework (DDF) for the **RemoteWipe** configuration service provider. DDF files are used only with OMA DM provisioning XML.

You can download the Windows 10 version 1607 DDF files from [here](http://download.microsoft.com/download/2/3/E/23E27D6B-6E23-4833-B143-915EDA3BDD44/Windows10_1607_DDF.zip).

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC " -//OMA//DTD-DM-DDF 1.2//EN"
    "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
    [<?oma-dm-ddf-ver supported-versions="1.2"?>]>
<MgmtTree xmlns:MSFT="http://schemas.microsoft.com/MobileDevice/DM">
    <VerDTD>1.2</VerDTD>
    <Node>
        <NodeName>RemoteWipe</NodeName>
        <Path>./Vendor/MSFT</Path>
        <DFProperties>
            <AccessType>
                <Get />
            </AccessType>
            <DFFormat>
                <node />
            </DFFormat>
            <Occurrence>
                <One />
            </Occurrence>
            <Scope>
                <Permanent />
            </Scope>
            <DFType>
                <DDFName></DDFName>
            </DFType>
            <Description>The root node for remote wipe function.</Description>
        </DFProperties>
        <Node>
            <NodeName>doWipe</NodeName>
            <DFProperties>
                <AccessType>
                    <Exec />
                </AccessType>
                <DFFormat>
                    <chr />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
                <Description>Exec on this node will perform a remote wipe on the device. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>doWipePersistProvisionedData</NodeName>
            <DFProperties>
                <AccessType>
                    <Exec />
                </AccessType>
                <DFFormat>
                    <chr />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
                <Description>Exec on this node will back up provisioning data to a persistent location and perform a remote wipe on the device. The information that was backed up will be restored and applied to the device when it resumes. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>doWipeProtected</NodeName>
            <DFProperties>
                <AccessType>
                    <Exec />
                </AccessType>
                <DFFormat>
                    <chr />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
                <Description>Exec on this node will perform a remote wipe on the device and fully clean the internal drive. In some device configurations, this command may leave the device unable to boot. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
    </Node>
</MgmtTree>
```

## Related topics


[RemoteWipe configuration service provider](remotewipe-csp.md)

 

 






