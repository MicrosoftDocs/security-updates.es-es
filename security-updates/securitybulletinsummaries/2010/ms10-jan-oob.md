---
title: Resumen del boletín de seguridad de Microsoft de  enero 2010
TOCTitle: MS10-JAN-OOB
ms:assetid: ms10-jan-oob
ms:mtpsurl: https://msdn.microsoft.com/es-ES/library/ms10-jan-oob(v=Security.10)
ms:contentKeyID: 61225412
ms.date: 04/18/2014
mtps_version: v=Security.10
_tocRel: dn610244(v=security.10)/toc.json
ms.translationtype: HT
---

# Resumen del boletín de seguridad de Microsoft de enero 2010

Publicado: martes, 12 de enero de 2010 | Actualizado: jueves, 21 de enero de 2010

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para enero de 2010.

Con la publicación de los boletines de enero de 2010, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 20 de enero de 2010. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 13 de enero de 2010, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de enero](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032427677&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Para el boletín de seguridad fuera de ciclo agregado a la versión 2.0 de este resumen, MS10-002, Microsoft realizará un webcast para atender las preguntas de los clientes acerca del boletín el 21 de enero de 2010, a la 1:00 p.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del 21 de enero a la 1:00 p.m](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032440627&culture=en-us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

## Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones de descarga y software afectado**.

<table>
<thead>
<tr class="header">
<th>Identificador del boletín</th>
<th>Título de boletín y resumen ejecutivo</th>
<th>Clasificación máxima de gravedad y consecuencias de la vulnerabilidad</th>
<th>Requisito de reinicio</th>
<th>Software afectado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-001">MS10-001</a></td>
<td><strong>Una vulnerabilidad en el motor de fuentes OpenType incrustadas podría permitir la ejecución remota de código (972270)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario consulta contenido representado en una fuente OpenType incrustada (EOT) especialmente diseñada en las aplicaciones cliente que pueden representar fuentes EOT, como Microsoft Internet Explorer, Microsoft Office PowerPoint o Microsoft Office Word. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas, ver, cambiar o eliminar datos, o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td>Puede requerir reinicio</td>
<td>Microsoft Windows</td>
</tr>
<tr class="even">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td><strong>Actualización de seguridad acumulativa para Internet Explorer (978207)</strong><br />
<br />
Esta actualización de seguridad resuelve siete vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario de Internet Explorer visita una página web especialmente diseñada. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td>Requiere reinicio</td>
<td>Microsoft Windows</td>
</tr>
</tbody>
</table>


## Índice de explotabilidad

La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.

**¿Cómo se usa esta tabla?**

Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).

<table>
<thead>
<tr class="header">
<th>Identificador del boletín</th>
<th>Título de vulnerabilidad</th>
<th>Identificador CVE</th>
<th>Evaluación de índice de explotabilidad</th>
<th>Notas clave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-001">MS10-001</a></td>
<td>Vulnerabilidad de error de entero de las fuentes comprimidas de Microtype Express en el descompresor LZCOMP</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0018">CVE-2010-0018</a></td>
<td><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td>Esta evaluación del índice de explotabilidad se aplica a los sistemas que ejecutan Microsoft Windows 2000. Es improbable que se aproveche en los sistemas que ejecutan Windows XP y sistemas operativos posteriores.</td>
</tr>
<tr class="even">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad en el tratamiento de secuencias de comandos de filtro XSS</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-4047">CVE-2009-4047</a></td>
<td>Ninguna</td>
<td>No es posible la ejecución de código con esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de validación de direcciones URL</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0027">CVE-2010-0027</a></td>
<td><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td>(Ninguna)</td>
</tr>
<tr class="even">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de daños en la memoria sin inicializar</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0244">CVE-2010-0244</a></td>
<td><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td>(Ninguna)</td>
</tr>
<tr class="odd">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de daños en la memoria sin inicializar</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0245">CVE-2010-0245</a></td>
<td>Ninguna</td>
<td>Los clientes que aplicaron <a href="http://technet.microsoft.com/security/bulletin/ms09-072">MS09-072</a> están protegidos porque esta vulnerabilidad está bloqueada por los cambios incluidos en la actualización MS09-072.</td>
</tr>
<tr class="even">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de daños en la memoria sin inicializar</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0246">CVE-2010-0246</a></td>
<td>Ninguna</td>
<td>Los clientes que aplicaron <a href="http://technet.microsoft.com/security/bulletin/ms09-072">MS09-072</a> están protegidos porque esta vulnerabilidad está bloqueada por los cambios incluidos en la actualización MS09-072.</td>
</tr>
<tr class="odd">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de daños en la memoria sin inicializar</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0247">CVE-2010-0247</a></td>
<td><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td>(Ninguna)</td>
</tr>
<tr class="even">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de daños en la memoria sin inicializar</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0248">CVE-2010-0248</a></td>
<td><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td>(Ninguna)</td>
</tr>
<tr class="odd">
<td><a href="http://technet.microsoft.com/security/bulletin/ms10-002">MS10-002</a></td>
<td>Vulnerabilidad de daños en la memoria sin inicializar</td>
<td><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0249">CVE-2010-0249</a></td>
<td><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td><strong>Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.</strong></td>
</tr>
</tbody>
</table>


## Ubicaciones de descarga y software afectado

Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.

**¿Cómo se usan estas tablas?**

Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Componentes y sistema operativo Windows

<table xmlns="http://www.w3.org/1999/xhtml">
  <tr class="thead">
    <th></th>
    <th></th>
    <th></th>
  </tr>
                <tr><th colspan="3">Microsoft Windows 2000</th></tr>
              
                <tr><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr><td>Microsoft Windows 2000 Service Pack 4</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=47f85cbd-282e-4c92-9809-68bba49e0a12">Microsoft Windows 2000 Service Pack 4</a>
                    <br />(Crítica)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=51e99e4f-1670-4b12-a9fe-e0ccf50cdabc">Internet Explorer 5.01 Service Pack 4 cuando está instalado en Microsoft Windows 2000 Service Pack 4</a>
                    <br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=a38aa9d0-c3fe-4d41-8805-7d5370263c1b">Internet Explorer 6 Service Pack 1 cuando está instalado en Microsoft Windows 2000 Service Pack 4</a><br />(Crítica)</td></tr>
              
                <tr><th colspan="3">Windows XP</th></tr>
              
                <tr class="alternateRow"><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Baja</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>Windows XP Service Pack 2 y Windows XP Service Pack 3</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=793a6b3f-7660-40be-b7d5-7b0eec55e1cd">Windows XP Service Pack 2 y Windows XP Service Pack 3</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=207eecad-6e84-48e6-ae18-6794a3618ee0">Internet Explorer 6 para Windows XP Service Pack 2 y Windows XP Service Pack 3</a>
                    <br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=3510c7d8-7e8f-479e-b6f9-5745a845664d">Internet Explorer 7 para Windows XP Service Pack 2 y Windows XP Service Pack 3</a><br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=7c2948fb-f486-4801-bc21-bbf40d5a78c2">Internet Explorer 8 para Windows XP Service Pack 2 y Windows XP Service Pack 3</a><br />(Crítica)</td></tr>
                <tr><td>Windows XP Professional x64 Edition Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=31609ce9-656a-4f7d-a501-709a31ca34c3">Windows XP Professional x64 Edition Service Pack 2</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=eb2d8055-4d50-4f83-82b8-055c7b8f5422">Internet Explorer 6 para Windows XP Professional x64 Edition Service Pack 2</a>
                    <br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=cc5aea0b-e553-4f7f-a2cc-cba41bb87ae7">Internet Explorer 7 para Windows XP Professional x64 Edition Service Pack 2</a><br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=41b83fad-948b-4a9c-80ed-9c5a60bd35b4">Internet Explorer 8 para Windows XP Professional x64 Edition Service Pack 2</a><br />(Crítica)</td></tr>
              
                <tr><th colspan="3">Windows Server 2003</th></tr>
              
                <tr class="alternateRow"><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Baja</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>Windows Server 2003 Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=e1d6e338-dea9-458e-b35d-796e069d74d7">Windows Server 2003 Service Pack 2</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=fea91227-44ad-4549-8732-497a8ceff870">Internet Explorer 6 para Windows Server 2003 Service Pack 2</a>
                    <br />(Moderada)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=14726445-3ff4-463c-9fc1-c9b758079aca">Internet Explorer 7 para Windows Server 2003 Service Pack 2</a><br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=7d480c87-2ca9-4505-a59d-a6d73d001fa5">Internet Explorer 8 para Windows Server 2003 Service Pack 2</a><br />(Crítica)</td></tr>
                <tr><td>Windows Server 2003 x64 Edition Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=ddbcf231-9fde-4dc2-ad04-a01b69d1a980">Windows Server 2003 x64 Edition Service Pack 2</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=633e63f4-605b-43c4-8a4b-2730312a1c72">Internet Explorer 6 para Windows Server 2003 x64 Edition Service Pack 2</a>
                    <br />(Moderada)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=c8742230-16d8-4b2f-bd3e-8834c759856b">Internet Explorer 7 para Windows Server 2003 x64 Edition Service Pack 2</a><br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=3e2e740b-8417-4758-8468-15221249ec71">Internet Explorer 8 para Windows Server 2003 x64 Edition Service Pack 2</a><br />(Crítica)</td></tr>
                <tr class="alternateRow"><td>Windows Server 2003 con SP2 para sistemas con Itanium</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=c71a13cf-7e2f-4b02-8684-1a4e4b46ddda">Windows Server 2003 con SP2 para sistemas con Itanium</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=b9308d50-ca66-43ff-9dc5-d05c90baa764">Internet Explorer 6 para Windows Server 2003 con SP2 para sistemas con Itanium</a>
                    <br />(Moderada)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=5622f223-df9c-4a6a-bdf0-feebaf9920fd">Internet Explorer 7 para Windows Server 2003 con SP2 para sistemas con Itanium</a><br />(Crítica)</td></tr>
              
                <tr><th colspan="3">Windows Vista</th></tr>
              
                <tr><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Baja</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr><td>Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=6387228c-eedc-4511-b3c6-8922606f4c84">Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=92495551-dedd-43d4-bb3a-51028bc5c6d6">Internet Explorer 7 en Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2</a>
                    <br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=5e2cbd7d-f64f-49e5-a159-1965ebfe2a92">Internet Explorer 8 en Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2</a><br />(Crítica)</td></tr>
                <tr class="alternateRow"><td>Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=7b4f5089-13b1-421b-a00b-22632bba4229">Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=3cb139b3-59f4-44ef-9911-4dd4e3b83e7d">Internet Explorer 7 en Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</a>
                    <br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=b7a7e8e7-f4c5-459d-ab6c-05a192e1e3f9">Internet Explorer 8 en Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</a><br />(Crítica)</td></tr>
              
                <tr><th colspan="3">Windows Server 2008</th></tr>
              
                <tr><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Baja</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr><td>Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=e175c436-37e0-497f-8b7f-6cacaa25ad7c">Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</a>**<br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=8c4c91ec-1b2b-4176-bd77-45245b590329">Internet Explorer 7 en Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</a>**<br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=f5ce8582-af63-4870-bee3-0abeeefa1458">Internet Explorer 8 en Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</a>**<br />(Crítica)</td></tr>
                <tr class="alternateRow"><td>Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=1b10a177-fd45-406f-8edc-b8d4b84881b7">Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</a>**<br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=4f9975b8-3f91-4116-9200-ef55ece75854">Internet Explorer 7 en Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</a>**<br />(Crítica)<br /><br /><a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=be11981c-d286-4e3c-94bf-d4e67a975d5a">Internet Explorer 8 en Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</a>**<br />(Crítica)</td></tr>
                <tr><td>Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=e8bc9a24-a794-4827-a6bb-785c6b2189f4">Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=9395547f-b620-4cbd-9ff5-11b76cd73859">Internet Explorer 7 en Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</a>
                    <br />(Crítica)</td></tr>
              
                <tr><th colspan="3">Windows 7</th></tr>
              
                <tr class="alternateRow"><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Baja</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>Windows 7 para sistemas de 32 bits</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=75491ad0-40a6-4efb-9574-d82210f6d0da">Windows 7 para sistemas de 32 bits</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=278443c1-15dc-436b-893b-ffea6d29d16d">Internet Explorer 8 en Windows 7 para sistemas de 32 bits</a>
                    <br />(Crítica)</td></tr>
                <tr><td>Windows 7 para sistemas x64</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=8a53f0e9-0616-440e-90f2-a12524e1bee4">Windows 7 para sistemas x64</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=a584cd0f-2e05-4e36-8858-0ffead637162">Internet Explorer 8 en Windows 7 para sistemas x64</a>
                    <br />(Crítica)</td></tr>
              
                <tr><th colspan="3">Windows Server 2008 R2</th></tr>
              
                <tr class="alternateRow"><td>
                    <strong>Identificador del boletín</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-001">
                      <strong>MS10-001</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/ms10-002">
                      <strong>MS10-002</strong>
                    </a>
                  </td></tr>
                <tr><td>
                    <strong>Clasificación de gravedad acumulada</strong>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Baja</strong>
                    </a>
                  </td><td>
                    <a Target="" runat="server" href="http://technet.microsoft.com/security/bulletin/rating">
                      <strong>Crítica</strong>
                    </a>
                  </td></tr>
                <tr class="alternateRow"><td>Windows Server 2008 R2 para sistemas x64 </td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=308166e4-571b-4d6c-bd9f-3ed4afa4eafe">Windows Server 2008 R2 para sistemas x64</a>**<br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=d3386793-a594-4bc5-8308-28b561d43087">Internet Explorer 8 en Windows Server 2008 R2 para sistemas x64</a>**<br />(Crítica)</td></tr>
                <tr><td>Windows Server 2008 R2 para sistemas con Itanium</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=1d0da42b-9755-4fd2-afd1-0d023d187133">Windows Server 2008 R2 para sistemas con Itanium</a>
                    <br />(Baja)</td><td>
                    <a Target="" runat="server" href="http://www.microsoft.com/downloads/details.aspx?familyid=9d137bab-8312-4240-af74-c65ba652fde0">Internet Explorer 8 en Windows Server 2008 R2 para sistemas con Itanium</a>
                    <br />(Crítica)</td></tr>
              </table>


**Nota para Windows Server 2008 y Windows Server 2008 R2**

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891\(vs.85\).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631\(vs.85\).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

## Herramientas y consejos para la detección e implementación

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejará de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

  - [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
  - [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

  - En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
  - Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
  - Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

  - Tavis Ormandy, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS10-001
  - [David Lindsay "thornmaker"](http://p42.us/) y [Eduardo A. Vela Nava "sirdarckcat"](http://www.sirdarckcat.net/), por informar de un problema descrito en MS10-002
  - Lostmon Lords, por informar de un problema descrito en MS10-002
  - Brett Moore, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS10-002
  - Wushi, de [team509](http://www.team509.com/), en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS10-002
  - Sam Thomas, de eshu.co.uk, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS10-002
  - Sam Thomas, de eshu.co.uk, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS10-002
  - Haifei Li, de [FortiGuard Global Security Research Team](http://www.fortiguardcenter.com/) de Fortinet, por informar de un problema descrito en MS10-002
  - Peter Vreugdenhil, de [Verisign iDefense Labs](http://labs.idefense.com/), en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS10-002
  - Meron Sellem, de [BugSec](http://www.bugsec.com/), por informar de un problema descrito en MS10-002

Microsoft [agradece](http://go.microsoft.com/fwlink/?linkid=21127) a las siguientes empresas su colaboración y los detalles proporcionados sobre un problema descrito en MS10-002:

  - [Google Inc.](http://www.google.com/) y [MANDIANT](http://www.mandiant.com/)
  - [Adobe](http://www.adobe.com/)
  - [McAfee](http://www.mcafee.com/)

#### Soporte técnico

  - El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
  - Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
  - Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

  - V1.0 (12 de enero de 2010): Publicación del resumen del boletín.
  - V2.0 (21 de enero de 2010): Se ha agregado el boletín de seguridad de Microsoft **MS10-002, Actualización acumulativa para Internet Explorer (978207)**. También se ha agregado un vínculo de webcast de boletín para este boletín de seguridad fuera de ciclo.

*Built at 2014-04-18T01:50:00Z-07:00*

