+++
description = "Create a self-signed certificate with PowerShell"
date = "2016-11-18T20:38:38-08:00"
title = "Self-Signed Certificate with PowerShell"
tags = [
    'x509',
    'powershell'
]

+++

How many ways are there to create a self-signed certificate? 

One: PowerShell

Open a PowerShell prompt as root, and execute.

```ps
$cert = New-SelfSignedCertificate -DnsName yourdomain.cloudapp.net
$pass = ConvertTo-SecureString -String "secret" -Force -AsPlainText
Export-PfxCertificate -Cert $cert -FilePath .\cert.pfx -Password $pass
```
