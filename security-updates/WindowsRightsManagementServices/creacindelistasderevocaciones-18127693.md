---
TOCTitle: Creación de listas de revocaciones
Title: Creación de listas de revocaciones
ms:assetid: '1ef75199-3344-4225-84de-a863a777696a'
ms:contentKeyID: 18127693
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720208(v=WS.10)'
---

Creación de listas de revocaciones
==================================

Para implementar la revocación, es preciso que implemente una lista de revocaciones, que es un documento XML que utiliza el lenguaje de marcado de permisos extensible (XrML) y enumera las entidades que ya no deben tener acceso al contenido protegido por derechos. Debe crear listas de revocaciones que indiquen la fecha y la hora y dispongan de las firmas adecuadas con la herramienta de firma de lista de revocaciones (RLsigner.exe) que se proporciona con RMS.

> [!IMPORTANT]
> Para firmar la lista de revocaciones con RLsigner.exe, debe guardar el archivo de lista de revocaciones como archivo Unicode. 

Ejemplo de lista de revocaciones
--------------------------------

Este tema presenta un ejemplo de lista de revocaciones completo que muestra todos los mecanismos de revocación posibles. Puede utilizar este ejemplo como modelo para crear sus propias listas de revocaciones.

Una lista de revocaciones es un archivo XML que usa el lenguaje XrML.

El elemento BODY contiene cuatro elementos secundarios:

-   **ISSUEDTIME**. Contiene la fecha y la hora de emisión de la lista de revocaciones. RLsigner.exe inserta este elemento en el archivo; el elemento se proporciona en el ejemplo únicamente para demostrar la estructura global del archivo de lista de revocaciones.
-   **DESCRIPTOR**. Contiene datos que identifican el archivo como lista de revocaciones.
-   **ISSUER**. Contiene datos que identifican a la entidad que emite la lista de revocaciones.
-   **REVOCATIONLIST**. Contiene elementos secundarios REVOKE que especifican las entidades que se revocan en esta lista.

A continuación se muestra un ejemplo del archivo de lista de revocaciones.

| ![](images/Cc720208.note(WS.10).gif)Nota                                               |
|---------------------------------------------------------------------------------------------------------------------|
        ```
> [!CAUTION]
> Al especificar la dirección URL en la lista de revocaciones, ya no se admite una ruta UNC en RMS con SP1 o RMS con SP2. Debe usar una dirección URL. 

Una vez definidos los elementos REVOKE, la lista de revocaciones está lista para firmarse.

Con el elemento REVOKE
----------------------

En la lista de revocaciones de ejemplo de la sección Ejemplo de lista de revocaciones, cada elemento REVOKE especifica una entidad de seguridad que se va a revocar. La etiqueta inicial tiene atributos category y type que definen lo que se revoca y según qué criterio de identificación. Los diversos elementos REVOKE pueden tener diferentes elementos secundarios, dependiendo de la acción especificada en los atributos category y type.

Para obtener más información acerca de la especificación de elementos REVOKE, consulte los siguientes ejemplos:

-   [Revocación de entidades principales basándose en una clave pública](#bkmk_1)
-   [Revocación de certificados y licencias basándose en el GUID](#bkmk_2)
-   [Revocación de certificados y licencias basándose en el valor de un algoritmo hash](#bkmk_3)
-   [Revocación de certificados y licencias basándose en la clave pública del emisor](#bkmk_4)
-   [Revocación de certificados y licencias basándose en el Id. del emisor](#bkmk_5)
-   [Revocación de contenido basándose en el Id. del contenido](#bkmk_6)
-   [Revocación de certificados según el identificador de la entidad de seguridad](#bkmk_10)
-   [Revocación de entidades de seguridad según Windows Live ID](#bkmk_7)

#### Revocación de entidades principales basándose en una clave pública

        ```

#### Revocación de certificados y licencias basándose en el GUID

        ```
#### Revocación mediante un manifiesto de la aplicación

Para revocar mediante un manifiesto de la aplicación, debe extraer el Id., la clave pública o el algoritmo hash del emisor del manifiesto de la aplicación. Sin embargo, los manifiestos de aplicaciones están cifrados en base 64, para que la información no esté disponible como texto sin formato. Con el kit de desarrollo de software (SDK) de Servicios de Rights Management, puede desarrollarse un programa utilizando los métodos DRMConstructCertificateChain, DRMDeconstructCertificateChain y DRMDecode para descodificar el manifiesto de la aplicación y obtener la información necesaria.

Si desea impedir que una aplicación use contenido protegido por derechos, considere el uso de la exclusión de aplicaciones para prohibir que el clúster de RMS les otorgue licencias de uso a estas aplicaciones. La limitación de exclusión implica que no puede evitar que alguien con una licencia de uso válida descifre contenido protegido por derechos. Para obtener más información sobre la exclusión de aplicaciones, vea [Exclusión de aplicaciones](https://technet.microsoft.com/b68ae4b2-b9ba-44ae-90cb-c88df600ec86), anteriormente en este tema.

#### Revocación de certificados y licencias basándose en el valor de un algoritmo hash

        ```
#### Revocación mediante un manifiesto de la aplicación

Para revocar mediante un manifiesto de la aplicación, debe extraer el Id., la clave pública o el algoritmo hash del emisor del manifiesto de la aplicación. Sin embargo, los manifiestos de aplicación están cifrados en base 64, para que la información no esté disponible como texto sin formato. Con el kit de desarrollo de software (SDK) de los Servicios de Rights Management, puede desarrollarse un programa utilizando los métodos DRMConstructCertificateChain, DRMDeconstructCertificateChain y DRMDecode para descodificar el manifiesto de la aplicación y obtener la información necesaria.

Si desea impedir que una aplicación use contenido protegido por derechos, considere el uso de la exclusión de aplicaciones para prohibir que el clúster de RMS les otorgue licencias de uso a estas aplicaciones. La limitación de exclusión implica que no puede evitar que alguien con una licencia de uso válida descifre contenido protegido por RMS. Para obtener más información sobre la exclusión de aplicaciones, vea [Exclusión de aplicaciones](https://technet.microsoft.com/b68ae4b2-b9ba-44ae-90cb-c88df600ec86), anteriormente en este tema.

#### Revocación de certificados y licencias basándose en la clave pública del emisor

        ```

#### Revocación de certificados y licencias basándose en el Id. del emisor

        ```
> [!NOTE]
> Al especificar el tipo de id., asegúrese de que no haya un retorno de carro entre el identificador único global (GUID) y la etiqueta de cierre. Si se agrega accidentalmente un retorno de carro, el cliente de RMS no podrá analizar la lista de revocaciones. 

#### Revocación de contenido basándose en el Id. del contenido

        ```
> [!NOTE]
> Al especificar el tipo de id., asegúrese de que no haya un retorno de carro entre el identificador único global (GUID) y la etiqueta de cierre. Si se agrega accidentalmente un retorno de carro, el cliente de RMS no podrá analizar la lista de revocaciones. 

#### Revocación de entidades de seguridad según la cuenta de Windows

        ```
> [!NOTE]
> Al especificar el tipo de identificador, asegúrese de que no haya un retorno de carro entre el SID de cuenta de Windows y la etiqueta de cierre. Si se agrega accidentalmente un retorno de carro, el cliente de RMS no podrá analizar la lista de revocaciones. 

#### Revocación de entidades de seguridad según Windows Live ID

        ```
> [!NOTE]
> Al especificar el tipo de id., asegúrese de que no haya un retorno de carro entre el identificador único principal (PUID) y la etiqueta de cierre. Si se agrega accidentalmente un retorno de carro, el cliente de RMS no podrá analizar la lista de revocaciones. 

Inserción de una firma en una lista de revocaciones
---------------------------------------------------

Cuando termine de crear una lista de revocaciones, debe insertar una firma en ella como se explica en este tema. Después, puede poner a disposición de los usuarios la lista de revocaciones desde la dirección URL que especifique en la plantilla de directiva de permisos asociada.

El primer paso para insertar una firma es generar un par de claves y un archivo de clave para la lista de revocaciones, con la herramienta de nombre seguro (Sn.exe). La herramienta Sn.exe se incluye en el SDK 1.1 de Microsoft .NET Framework, que está disponible en el sitio web de Microsoft [http://go.microsoft.com/fwlink/?LinkId=104796](http://go.microsoft.com/fwlink/?linkid=104796).

El archivo de lista de revocaciones se debe haber guardado como archivo Unicode para firmarlo con RLsigner.exe.

**Para utilizar Sn.exe tanto para generar un nuevo par de claves como para escribirlo en un archivo, siga estos pasos:**
1.  Cree la clave privada. En el símbolo del sistema, escriba el siguiente comando y presione ENTRAR:

    **sn -k** *archivo\_de\_clave\_privada***.snk**

    donde *archivo\_de\_clave\_privada* es el nombre del archivo de clave.

2.  Use Sn.exe para extraer la clave pública del archivo de par de claves creado en el paso 1 y exportarlo a un archivo independiente. Escriba el siguiente comando y presione ENTRAR:

    **sn -p** *archivo\_de\_clave\_privada archivo\_de\_clave\_pública*

    donde *archivo\_de\_clave\_privada* es el nombre del archivo de clave privada creado en el paso 1 y *archivo\_de\_clave\_pública* es el nombre del archivo donde se almacenará la clave pública exportada.

3.  Cambie la extensión del archivo de clave privada (creado en el paso 1) de .snk a .dat para usarlo con RLsigner.exe.

4.  Use RLsigner.exe para insertar una firma en un archivo de lista de revocaciones. Esta herramienta se incluye con RMS. De forma predeterminada, se encuentra en el directorio %systemdrive%:\\Archivos de programa\\Servicios de Windows Rights Management\\Tools.

> [!NOTE]
> RLsigner.exe no admite nombres de archivo con espacios.               

Uso de RLsigner.exe
-------------------

Cuando se ejecuta RLsigner.exe, crea primero una firma con la clave privada que se proporciona en el archivo de clave. Después, crea un archivo de salida que se basa en el archivo de lista de revocaciones proporcionado.

> [!IMPORTANT]
> El archivo de lista de revocaciones se debe haber guardado en un archivo Unicode para usar RLsigner.exe. 

Para usar RLsigner.exe con el fin de firmar la lista de revocaciones, escriba el siguiente comando en el símbolo del sistema:

**rlsigner.exe** *input\_file* **{-f** *key\_file* **| -h** *container\_name* **CSP}** *output\_file*

Utilice la siguiente información para completar los parámetros de entrada del comando:

###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><em>input_file</em></td>
<td style="border:1px solid black;">Nombre del archivo de lista de revocaciones compatible con XrML que ha preparado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>key_file</em></td>
<td style="border:1px solid black;">Nombre del archivo que contiene las claves privada y pública que ha generado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><em>container_name</em></td>
<td style="border:1px solid black;">Nombre del contenedor de la clave</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>output_file</em></td>
<td style="border:1px solid black;">Nombre del archivo de lista de revocaciones firmado que la herramienta creará.</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc720208.note(WS.10).gif)Nota |  
|-----------------------------------------------------------------------|  
| RLsigner.exe no admite nombres de archivo con espacios.               |
  
Los siguientes ejemplos describen cómo puede usar RLsigner.exe en el símbolo del sistema con diferentes proveedores de servicios de cifrado:
  
-   Ejemplo de sintaxis de línea de comandos que utiliza un archivo de clave:  
    **rlsigner.exe rl.xml -f key.dat output.xml**  
-   Ejemplo de sintaxis de línea de comandos que utiliza un módulo de seguridad de hardware:  
    **rlsigner.exe rl.xml -h Container CSP output.xml**
  
RLsigner.exe proporciona información básica de error y éxito en el código de retorno. En la siguiente tabla, se describen los posibles códigos de retorno.
  
###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Código de retorno</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">0</td>
<td style="border:1px solid black;">Éxito</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">-1</td>
<td style="border:1px solid black;">No se puede leer el archivo de origen.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">-2</td>
<td style="border:1px solid black;">No se puede leer el archivo de clave.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">-3</td>
<td style="border:1px solid black;">El archivo de clave no es válido.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">-4</td>
<td style="border:1px solid black;">El archivo de origen no es válido.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">-5</td>
<td style="border:1px solid black;">No se puede escribir el archivo de salida.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">-6</td>
<td style="border:1px solid black;">Error desconocido</td>
</tr>
</tbody>
</table>
  
Es posible que desee programar la firma de las listas de revocaciones basándose en el intervalo de actualización que especificó en el servidor.
  
Puede automatizar el proceso de firma de listas de revocaciones utilizando una secuencia de comandos. La siguiente secuencia de ejemplo de VBScript llama a RLsigner.exe y escribe los resultados en el registro de sucesos del sistema.
  
<codesnippet asp="http://msdn2.microsoft.com/asp" language displaylanguage="Visual Basic">const EVT\_SUCCESS = 0 const EVT\_ERROR = 1 const EVT\_WARNING = 2 const EVT\_INFORMATION = 4 const EVT\_AUDIT\_SUCCESS = 8 const EVT\_AUDIT\_FAILURE = 16 Dim WshShell, oExec Set WshShell = CreateObject( "WScript.Shell" ) Set oExec = WshShell.Exec("rlsigner.exe input\_file key\_file output\_file") Do While oExec.Status = 0 WScript.Sleep 100 Loop if WshShell.ExitCode &lt;&gt; 0 Then WshShell.LogEvent EVT\_ERROR, "RLsigner failed with error """ + WshShell.ExitCode + """" else WshShell.LogEvent EVT\_SUCCESS, "RLsigner completed successfully" end if  
```
