---
TOCTitle: 'MS09-MAR'
Title: Resumen del boletín de seguridad de Microsoft de marzo 2009
ms:assetid: 'ms09-mar'
ms:contentKeyID: 61225403
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-mar(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de marzo 2009
===========================================================

Publicado: martes, 10 de marzo de 2009 | Actualizado: miércoles, 11 de marzo de 2009

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para marzo de 2009.

Con la publicación de los boletines de marzo de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 5 de marzo de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 11 de marzo de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de marzo](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032395124). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones de descarga y software afectado**.

 
<p> </p>
<table style="border:1px solid black;">
<thead>
<tr class="header">
<th style="border:1px solid black;" >Identificador del boletín</th>
<th style="border:1px solid black;" >Título de boletín y resumen ejecutivo</th>
<th style="border:1px solid black;" >Clasificación máxima de gravedad y consecuencias de la vulnerabilidad</th>
<th style="border:1px solid black;" >Requisito de reinicio</th>
<th style="border:1px solid black;" >Software afectado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-006">MS09-006</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el kernel de Windows podrían permitir la ejecución remota de código (958690)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades en el kernel de Windows de las que se ha informado de forma privada. La vulnerabilidad más grave podría permitir la ejecución remota de código si un usuario visualiza un archivo de imagen EMF o WMF especialmente diseñado de un sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-007">MS09-007</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en SChannel podría permitir la suplantación de identidad (960225)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en el paquete de seguridad de canal seguro (SChannel) en Windows de la que se ha informado de forma privada. La vulnerabilidad podría permitir la suplantación de identidad si un atacante obtiene acceso al certificado que usa el usuario final para la autenticación. Los clientes sólo están afectados cuando el atacante ha obtenido el componente de clave pública del certificado usado para la autenticación por otros medios.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Suplantación</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-008">MS09-008</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el servidor DNS y WINS podrían permitir la suplantación de identidad (962238)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades en el servidor DNS de Windows y en el servidor WINS de Windows de las que se ha informado de forma privada. Estas vulnerabilidades podrían permitir que un atacante remoto redireccionara el tráfico de red destinado a sistemas en Internet a los sistemas propios del atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Suplantación</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título del boletín                                                                                | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                                                                                                                              |  
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-006](http://technet.microsoft.com/security/bulletin/ms09-006) | Vulnerabilidades en el kernel de Windows podrían permitir la ejecución remota de código (958690)  | [CVE-2009-0081](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0081) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | La denegación de servicio es más probable que una ejecución de código confiable y funcional                                                                                                              |  
| [MS09-006](http://technet.microsoft.com/security/bulletin/ms09-006) | Vulnerabilidades en el kernel de Windows podrían permitir la ejecución remota de código (958690)  | [CVE-2009-0082](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0082) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | La denegación de servicio es más probable que una ejecución de código confiable y funcional                                                                                                              |  
| [MS09-006](http://technet.microsoft.com/security/bulletin/ms09-006) | Vulnerabilidades en el kernel de Windows podrían permitir la ejecución remota de código (958690)  | [CVE-2009-0083](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0083) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | La amenaza local sólo existe para la denegación de servicio o divulgación de información, que son más probables que una ejecución de código confiable y funcional                                        |  
| [MS09-007](http://technet.microsoft.com/security/bulletin/ms09-007) | Una vulnerabilidad en SChannel podría permitir la suplantación de identidad (960225)              | [CVE-2009-0085](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0085) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Los requisitos para las posibilidades de aprovechar la vulnerabilidad son elevados y el número de escenarios de cliente importantes es bajo                                                              |  
| [MS09-008](http://technet.microsoft.com/security/bulletin/ms09-008) | Vulnerabilidades en el servidor DNS y WINS podrían permitir la suplantación de identidad (962238) | [CVE-2009-0093](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0093) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es probable la prueba de concepto de suplantación de identidad pero el código funcional que aproveche la vulnerabilidad y que dé como resultado la ejecución de código malintencionado es muy improbable |  
| [MS09-008](http://technet.microsoft.com/security/bulletin/ms09-008) | Vulnerabilidades en el servidor DNS y WINS podrían permitir la suplantación de identidad (962238) | [CVE-2009-0094](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0094) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es probable la prueba de concepto de suplantación de identidad pero el código funcional que aproveche la vulnerabilidad y que dé como resultado la ejecución de código malintencionado es muy improbable |  
| [MS09-008](http://technet.microsoft.com/security/bulletin/ms09-008) | Vulnerabilidades en el servidor DNS y WINS podrían permitir la suplantación de identidad (962238) | [CVE-2009-0233](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0233) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es probable la prueba de concepto de suplantación de identidad pero el código funcional que aproveche la vulnerabilidad y que dé como resultado la ejecución de código malintencionado es muy improbable |  
| [MS09-008](http://technet.microsoft.com/security/bulletin/ms09-008) | Vulnerabilidades en el servidor DNS y WINS podrían permitir la suplantación de identidad (962238) | [CVE-2009-0234](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0234) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es probable la prueba de concepto de suplantación de identidad pero el código funcional que aproveche la vulnerabilidad y que dé como resultado la ejecución de código malintencionado es muy improbable |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-006**](http://technet.microsoft.com/security/bulletin/ms09-006)
</td>
<td style="border:1px solid black;">
[**MS09-007**](http://technet.microsoft.com/security/bulletin/ms09-007)
</td>
<td style="border:1px solid black;">
[**MS09-008**](http://technet.microsoft.com/security/bulletin/ms09-008)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=98bb7d40-89a0-470a-8eb7-06f15072a635)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=bf7065bc-c183-4a78-8d46-72fe7385c07c)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servidor DNS en Microsoft Windows 2000 Server Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=110354f7-5ece-4c4d-b563-3adba6ac0116)  
(961063)  
(Importante)  
[Servidor WINS en Microsoft Windows 2000 Server Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=4319abb3-1ea2-466a-a815-c0b3b86b4462)  
(961064)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-006**](http://technet.microsoft.com/security/bulletin/ms09-006)
</td>
<td style="border:1px solid black;">
[**MS09-007**](http://technet.microsoft.com/security/bulletin/ms09-007)
</td>
<td style="border:1px solid black;">
[**MS09-008**](http://technet.microsoft.com/security/bulletin/ms09-008)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e09641ba-6cbe-4095-82b5-703d3a7dc33b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=942d87f6-3cb1-4d36-a70a-70d9c34488f3)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d0d704c6-48c2-4907-b6c3-2455d7cf21c8)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6d02306e-9e2e-4ae8-bd21-8a2c1a229472)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-006**](http://technet.microsoft.com/security/bulletin/ms09-006)
</td>
<td style="border:1px solid black;">
[**MS09-007**](http://technet.microsoft.com/security/bulletin/ms09-007)
</td>
<td style="border:1px solid black;">
[**MS09-008**](http://technet.microsoft.com/security/bulletin/ms09-008)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f5cfb8da-e7cc-4183-8631-507c2a406500)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0b3f6fdd-276e-4267-99d8-8f00d91ad6a2)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servidor DNS en Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6cc42c9e-c34e-4577-8b23-9e07e2369878)  
(961063)  
(Importante)  
[Servidor WINS en Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=049e5db5-7315-4188-99fd-4a54833e6bf2)  
(961064)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ecf75c70-8489-41ad-9759-3a07e13957be)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ce98ff55-f565-469d-bbd2-32b681faf908)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servidor DNS en Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1f81fd2-0099-4450-8543-0459561d22d0)  
(961063)  
(Importante)  
[Servidor WINS en Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4a393c63-eff5-4c8c-9c3f-33ce45c32428)  
(961064)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=04be3d7e-7dda-4dca-887a-e7a8156ede1c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=5ca3c72c-cadb-4b0a-b3a3-fb81d0bfd7b3)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servidor DNS en Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=d3ed7d9a-d652-4bd0-aecc-5a415bec6c59)  
(961063)  
(Importante)  
[Servidor WINS en Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=37e3a75e-0a5d-4df0-881f-cdb87efa4dcf)  
(961064)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-006**](http://technet.microsoft.com/security/bulletin/ms09-006)
</td>
<td style="border:1px solid black;">
[**MS09-007**](http://technet.microsoft.com/security/bulletin/ms09-007)
</td>
<td style="border:1px solid black;">
[**MS09-008**](http://technet.microsoft.com/security/bulletin/ms09-008)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista y Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=4b1aaaba-f355-4265-83c0-50b901856ced)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=21086a04-402a-4940-8358-7fa63508102b)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0fcac480-d6db-4a94-8c7d-b7319282cf56)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c75a2ea9-b42f-457b-be09-5c8fa0339388)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-006**](http://technet.microsoft.com/security/bulletin/ms09-006)
</td>
<td style="border:1px solid black;">
[**MS09-007**](http://technet.microsoft.com/security/bulletin/ms09-007)
</td>
<td style="border:1px solid black;">
[**MS09-008**](http://technet.microsoft.com/security/bulletin/ms09-008)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=38851df2-4fb5-4d28-9d15-181c260cf8cf)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=47b361ce-624b-466c-b5c5-8703f6532615)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Servidor DNS en Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=92e89882-d656-4b61-a05c-3afb44895f08)\*  
(961063)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ec15acc4-3e0f-4414-9383-61c122ff1382)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=5c81ac45-60e6-4121-ab6b-d3b3179aacc4)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Servidor DNS en Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=be068d06-5939-4ad8-8191-e85931ed610f)\*  
(961063)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=eead6f93-10fd-4492-8137-481d9876a5fe)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=bf8f5a86-1757-4f9b-b632-d4aa7005a9f8)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Notas para Windows Server 2008**

**\*Instalación principal de servidor de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como “MS07-036”), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/smserver/default.mspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/bb466214.aspx).

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://www.microsoft.com/spain/technet/seguridad/areas/actualiza/default.mspx) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Helmut Buhler (<http://home.arcor.de/clipboarder/>), por informar de un problema descrito en MS09-006
-   Thomas Garnier, de [SkyRecon](http://www.skyrecon.com/), por informar de un problema descrito en MS09-006
-   [Secretaria da Fazenda do Estado do Rio Grande do Sul](http://www.sefaz.rs.gov.br/), por informar de un problema descrito en MS09-007
-   [Cia de Processamento de Dados do Estado do Rio Grande do Sul](http://www.procergs.rs.gov.br/), por informar de un problema descrito en MS09-007
-   Kevin Day, por colaborar con nosotros en dos problemas descritos en MS09-008
-   Dave Dagon, de [Georgia Tech Information Security Center](http://www.gtisc.gatech.edu/), por colaborar con nosotros en dos problemas descritos en MS09-008

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (10 de marzo de 2009): Publicación del resumen del boletín.
-   V1.1 (11 de marzo de 2009): Se ha actualizado la información del descubridor de MS09-008.

*Built at 2014-04-18T01:50:00Z-07:00*
