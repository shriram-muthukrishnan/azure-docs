---
 ms.topic: include
 author: cherylmc
 ms.service: vpn-gateway
 ms.date: 05/23/2022
 ms.author: cherylmc
---
Obtain the .cer file for the root certificate. You can use either a root certificate that was generated with an enterprise solution (recommended), or generate a self-signed certificate. After you create the root certificate, export the public certificate data (not the private key) as a Base64 encoded X.509 .cer file. You upload this file later to Azure.

* **Enterprise certificate:** If you're using an enterprise solution, you can use your existing certificate chain. Acquire the .cer file for the root certificate that you want to use.
* **Self-signed root certificate:** If you aren't using an enterprise certificate solution, create a self-signed root certificate. Otherwise, the certificates you create won't be compatible with your P2S connections and clients will receive a connection error when they try to connect. You can use Azure PowerShell, MakeCert, or OpenSSL. The steps in the following articles describe how to generate a compatible self-signed root certificate:

  * [Windows 10 or later PowerShell instructions](../articles/vpn-gateway/vpn-gateway-certificates-point-to-site.md): These instructions require Windows 10 or later and PowerShell to generate certificates. Client certificates that are generated from the root certificate can be installed on any supported P2S client.
  * [MakeCert instructions](../articles/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert.md): Use MakeCert if you don't have access to a Windows 10 or later computer to use to generate certificates. Although MakeCert is deprecated, you can still use it to generate certificates. Client certificates that you generate from the root certificate can be installed on any supported P2S client.
  * [Linux instructions](../articles/vpn-gateway/vpn-gateway-certificates-point-to-site-linux.md).