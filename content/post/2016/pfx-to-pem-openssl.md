+++
date = "2016-11-18T20:46:39-08:00"
title = "Convert PFX to PEM"
description = "Convert a PFX (PKCS12) Certificate to the PEM format"
tags = [
    'x509',
    'openssl'
]

+++

Windows uses the PFX file format for certificates, and UNIX uses the PEM 
format.  If you have to use both platforms you frequently have to convert 
between the two worlds.  PEM is a good _base_ format choice.  Store in 
PEM, and then convert to PFX as necessary.

```bat
openssl pkcs12 -in cert.pfx -out cert.pem -nodes
```

> The **-nodes** does not encrypt the private key.
