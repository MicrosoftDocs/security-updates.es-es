---
TOCTitle: Instalación de símbolo del sistema del servidor RMS
Title: Instalación de símbolo del sistema del servidor RMS
ms:assetid: 'b55b1e2a-dd14-4168-a37f-9cdedbec660b'
ms:contentKeyID: 18127937
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747733(v=WS.10)'
---

Instalación de símbolo del sistema del servidor RMS
===================================================

Puede instalar RMS con Service Pack 2 (SP2) desde el símbolo del sistema, lo que permite automatizar la instalación. La automatización de la instalación se puede realizar de dos formas: realizando una instalación desatendida con el cliente EXE descargado o usando los archivos MSI extraídos del EXE descargado para instalar el cliente de RMS. Para instalar con el archivo EXE descargado, use la siguiente sintaxis:

**WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe -override 1 /I MsDrmClient.msi REBOOT=ReallySuppress /q -override 2 /I RmClientBackCompat.msi REBOOT=ReallySuppress /q**

Para instalar con los archivos de Windows® Installer (.msi), primero debe extraer los archivos msi de RMS con el archivo ejecutable de SP2. El siguiente comando puede ejecutarse desde un símbolo del sistema para extraer los archivos msdrmclient.msi y RmClientBackCompat.msi:

**WindowsRightsManagementServiceSP2-KB917275-Server-ENU.exe /X:C:\\***Install\_Location*

Una vez extraídos los archivos .msi, puede usar el siguiente comando para instalar RMS:

**msiexec.exe /I MSDrmClient.msi /qn ALLUSERS=2 /m MSIDHOG /lei logfile.log DISPLYPAGE="NO" TARGETDIR=c:\\***Install\_Location*

**msiexec.exe /I RMClientBackCompat.msi /qn ALLUSERS=2 /m MSIDHOG /lei logfile.log DISPLYPAGE="NO" TARGETDIR=c:\\***Install\_Location*

En la siguiente tabla se describe la sintaxis de cada comando.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>/I MSDrmClient.msi</strong> o <strong>/I RMClientBackCompat.msi</strong></td>
<td style="border:1px solid black;">Requerido. Especifica el producto que se instalará.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>/qn</strong></td>
<td style="border:1px solid black;">Opcional. Especifica una instalación silenciosa, sin intervención del usuario.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>/lei</strong> <em>logfile.log</em></td>
<td style="border:1px solid black;">Opcional. Especifica el archivo en el que se registrarán los mensajes de estado y de error.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>DISPLAYPAGE=”NO”</strong></td>
<td style="border:1px solid black;">Opcional. Especifica que la página <strong>Administración global</strong> no se mostrará después de la instalación.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>TARGETDIR=c:\</strong><em>Install_Location</em></td>
<td style="border:1px solid black;">Opcional. Especifica el directorio en el que se debe instalar RMS con Service Pack 2. Si no especifica una ubicación, se utiliza la ubicación de instalación predeterminada.</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc747733.note(WS.10).gif)Nota                                                                                                                                                                                   |  
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Independientemente del método de instalación que decida implementar, asegúrese de que los dos archivos .msi se instalan correctamente. Si se produce un error que impide la instalación de MSDrmClient.msi, no podrá instalarse RMClientBackCompat.msi. |
