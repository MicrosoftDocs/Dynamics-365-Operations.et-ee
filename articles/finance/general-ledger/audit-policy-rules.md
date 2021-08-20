---
title: Auditipoliitika reeglid
description: Auditipoliitikaga saate hinnata kuluaruandeid, hankija arveid ja ostutellimusi, et kontrollida, kas need vastavad loodud poliitikareeglitele. Kõik auditi poliitikaga seotud reeglid käitatakse pakett-režiimis vastavalt teie määratud graafikule.  Iga poliitikareegel on poliitikareegli tüübi eksemplar. Iga poliitikareegli tüübi puhul saab korraga aktiivne olla vaid üks reegel.
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbf93f5b8b2f8d95102a52178b096d7e334894483c0ac0bacc62653aea845022
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744302"
---
# <a name="audit-policy-rules"></a>Auditipoliitika reeglid

[!include [banner](../includes/banner.md)]

Auditipoliitikaga saate hinnata kuluaruandeid, hankija arveid ja ostutellimusi, et kontrollida, kas need vastavad loodud poliitikareeglitele. Kõik auditi poliitikaga seotud reeglid käitatakse pakett-režiimis vastavalt teie määratud graafikule.  Iga poliitikareegel on poliitikareegli tüübi eksemplar. Iga poliitikareegli tüübi puhul saab korraga aktiivne olla vaid üks reegel. 

## <a name="queries-and-query-types"></a>Päringud ja päringu tüübid

Auditipoliitika reegli loomisel valite esmalt poliitikareegli tüübi. Poliitikareegli tüübiga määratakse rakendusobjektide puu (AOT) päring, mida kasutatakse poliitikareegli loomisel alguspunktina. Samuti määratakse poliitikareegli jaoks kasutatav päringu tüüp. Päring määrab, millist lähtedokumenti poliitikareegel hindab. See määrab ka lähtedokumendi väljad, mis näitavad dokumentide auditi jaoks valimisel kasutatavat juriidilist isikut ja kuupäeva. Päringu tüübiga määratakse päringulehe ja lehe Auditipoliitika reegel vaikeväljad. Järgmises tabelis on auditi poliitikareeglite jaoks saadaolevad päringu tüübid.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Päringu tüüp</th>
<th>Eesmärk</th>
<th>Lisateave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tinglik</td>
<td>Võrrelge lähtedokumendi atribuute määratud väärtustega.</td>
<td></td>
</tr>
<tr class="even">
<td>Koonda</td>
<td>Võrrelge mitut lähtedokumenti või lähtedokumendi rida poliitikareegliga, koondades arvväärtusi.</td>
<td></td>
</tr>
<tr class="odd">
<td>Diskreetimine</td>
<td>Valige kindla protsendimäära alusel juhuslikult lähtedokumendid, et kontrollida poliitika rikkumist.</td>
<td>Kui valite selle suvandi, kasutage auditiks juhuslikult valitavate dokumentide protsendi määramiseks lehte Auditipoliitika reegel.</td>
</tr>
<tr class="even">
<td>Duplikaat</td>
<td>Hinnake lähtedokumente kontrollimaks, kas nende määratud väljadel on topeltkirjeid.</td>
<td>Kui valite selle suvandi, määrake lehel Auditipoliitika reegel päevade arv, mis liidetakse dokumentide valimise kuupäevavahemiku algusele, kui dokumentidest otsitakse topeltkirjeid.</td>
</tr>
<tr class="odd">
<td>Loendi otsing</td>
<td>Otsige lähtedokumentidest kindlaid üksusi.</td>
<td>Päringu juurdokumendi määratleb auditeeritava dokumendi. Päring peab olema loendipäring, mis sisaldab viidet tabelile dirpartytable. Seda suvandit saab kasutada ainult järgmiste AOT päringutega.
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (kuluaruande jälgitavad töötajad)</li>
<li><span class="ui">AuditPolicyPurchList</span> (ostutellimuse jälgitavad hankijad)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (hankija arve jälgitavad hankijad)</li>
</ul>
Selle suvandi valimisel määrake jälgitavad üksused lehel Auditipoliitika reegel.</td>
</tr>
<tr class="even">
<td>Märksõna otsing</td>
<td>Kontrollige, kas lähtedokumentides on teatud sõnu.</td>
<td>Selle suvandi valimisel sisestage otsitavad sõnad lehel Auditipoliitika reegel. Lehel Auditipoliitika reegel on ka suvandid, millega saate määrata tabelid ja väljad, millest sisestatud sõnu otsida.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Üldparameetrid
Kõigil kindla auditipoliitika poliitikareeglitel on samad partiiparameetrid ja sama dokumendi valiku kuupäevavahemik. Need parameetrid on määratud poliitikas lehel Lisavalikud.



## <a name="additional-resources"></a>Lisaressursid

[Auditipoliitika rikkumised ja juhtumid](audit-policy-violations-cases.md)
[Lähtedokumentide jaoks auditipoliitikate määratlemine](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]