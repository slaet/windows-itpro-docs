---
title: DeveloperSetup DDF file
description: This topic shows the OMA DM device description framework (DDF) for the DeveloperSetup configuration service provider. This CSP was added in Windows 10, version 1703.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 
ms.author: windows-hardware-design-content
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# DeveloperSetup DDF file

This topic shows the OMA DM device description framework (DDF) for the DeveloperSetup configuration service provider. This CSP was added in Windows 10, version 1703.

You can download the DDF files from the links below:

- [Download all the DDF files for Windows 10, version 1703](http://download.microsoft.com/download/C/7/C/C7C94663-44CF-4221-ABCA-BC895F42B6C2/Windows10_1703_DDF_download.zip)
- [Download all the DDF files for Windows 10, version 1607](http://download.microsoft.com/download/2/3/E/23E27D6B-6E23-4833-B143-915EDA3BDD44/Windows10_1607_DDF.zip)

The XML below is the current version for this CSP.

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC " -//OMA//DTD-DM-DDF 1.2//EN"
  "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
  [<?oma-dm-ddf-ver supported-versions="1.2"?>]>
<MgmtTree xmlns:MSFT="http://schemas.microsoft.com/MobileDevice/DM">
  <VerDTD>1.2</VerDTD>
      <Node>
        <NodeName>DeveloperSetup</NodeName>
        <Path>./Device/Vendor/MSFT</Path>
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
            <DDFName>com.microsoft/1.0/MDM/DeveloperSetup</DDFName>
          </DFType>
        </DFProperties>
        <Node>
          <NodeName>EnableDeveloperMode</NodeName>
          <DFProperties>
            <AccessType>
              <Replace />
            </AccessType>
            <DefaultValue>False</DefaultValue>
            <Description>Enables developer mode on the device</Description>
            <DFFormat>
              <bool />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <CaseSense>
              <CIS />
            </CaseSense>
            <DFTitle>EnableDeveloperMode</DFTitle>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>DevicePortal</NodeName>
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
          </DFProperties>
          <Node>
            <NodeName>Authentication</NodeName>
            <DFProperties>
              <AccessType>
                <Get />
              </AccessType>
              <Description>Specifies characteristics of the authentication mechanism used for the Windows Device Portal.</Description>
              <DFFormat>
                <node />
              </DFFormat>
              <Occurrence>
                <One />
              </Occurrence>
              <Scope>
                <Permanent />
              </Scope>
              <CaseSense>
                <CIS />
              </CaseSense>
              <DFTitle>Authentication</DFTitle>
              <DFType>
                <DDFName></DDFName>
              </DFType>
            </DFProperties>
            <Node>
              <NodeName>Mode</NodeName>
              <DFProperties>
                <AccessType>
                  <Replace />
                </AccessType>
                <Description>Describes the mode of authentication used when making requests to the Device Portal.</Description>
                <DFFormat>
                  <int />
                </DFFormat>
                <Occurrence>
                  <One />
                </Occurrence>
                <Scope>
                  <Permanent />
                </Scope>
                <CaseSense>
                  <CIS />
                </CaseSense>
                <DFTitle>Mode</DFTitle>
                <DFType>
                  <MIME>text/plain</MIME>
                </DFType>
              </DFProperties>
            </Node>
            <Node>
              <NodeName>BasicAuth</NodeName>
              <DFProperties>
                <AccessType>
                  <Get />
                </AccessType>
                <Description>Describes credentials used for basic authentication</Description>
                <DFFormat>
                  <node />
                </DFFormat>
                <Occurrence>
                  <One />
                </Occurrence>
                <Scope>
                  <Permanent />
                </Scope>
                <CaseSense>
                  <CIS />
                </CaseSense>
                <DFTitle>BasicAuth</DFTitle>
                <DFType>
                  <DDFName></DDFName>
                </DFType>
              </DFProperties>
              <Node>
                <NodeName>Username</NodeName>
                <DFProperties>
                  <AccessType>
                    <Replace />
                  </AccessType>
                  <Description>Describes the username to use when performing basic authentication with the Windows Device Portal</Description>
                  <DFFormat>
                    <chr />
                  </DFFormat>
                  <Occurrence>
                    <One />
                  </Occurrence>
                  <Scope>
                    <Dynamic />
                  </Scope>
                  <CaseSense>
                    <CIS />
                  </CaseSense>
                  <DFTitle>Username</DFTitle>
                  <DFType>
                    <MIME>text/plain</MIME>
                  </DFType>
                </DFProperties>
              </Node>
              <Node>
                <NodeName>Password</NodeName>
                <DFProperties>
                  <AccessType>
                    <Replace />
                  </AccessType>
                  <Description>Describes the password to use when authenticating requests against the Windows Device Portal</Description>
                  <DFFormat>
                    <chr />
                  </DFFormat>
                  <Occurrence>
                    <One />
                  </Occurrence>
                  <Scope>
                    <Dynamic />
                  </Scope>
                  <CaseSense>
                    <CIS />
                  </CaseSense>
                  <DFTitle>Password</DFTitle>
                  <DFType>
                    <MIME>text/plain</MIME>
                  </DFType>
                </DFProperties>
              </Node>
            </Node>
          </Node>
          <Node>
            <NodeName>Connection</NodeName>
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
              <DFTitle>Connection</DFTitle>
              <DFType>
                <DDFName></DDFName>
              </DFType>
            </DFProperties>
            <Node>
              <NodeName>HttpPort</NodeName>
              <DFProperties>
                <AccessType>
                  <Replace />
                </AccessType>
                <Description>Configures the HTTP port for incoming connections to the Device Portal Service.</Description>
                <DFFormat>
                  <int />
                </DFFormat>
                <Occurrence>
                  <One />
                </Occurrence>
                <Scope>
                  <Permanent />
                </Scope>
                <DFTitle>HttpPort</DFTitle>
                <DFType>
                  <MIME>text/plain</MIME>
                </DFType>
              </DFProperties>
            </Node>
            <Node>
              <NodeName>HttpsPort</NodeName>
              <DFProperties>
                <AccessType>
                  <Replace />
                </AccessType>
                <Description>Configures the HTTPS port for incoming connections to the Device Portal Service.</Description>
                <DFFormat>
                  <int />
                </DFFormat>
                <Occurrence>
                  <One />
                </Occurrence>
                <Scope>
                  <Permanent />
                </Scope>
                <DFTitle>HttpsPort</DFTitle>
                <DFType>
                  <MIME>text/plain</MIME>
                </DFType>
              </DFProperties>
            </Node>
          </Node>
        </Node>
      </Node>
</MgmtTree>
```

 

 






