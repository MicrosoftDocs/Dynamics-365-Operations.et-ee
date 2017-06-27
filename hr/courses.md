---
title: Koolituskursuste seadistamine
description: "Inimressursside administraatorid ja haldurid saavad kasutada kursuste funktsioone töötajatele pakutavate koolituste kohta teabe haldamiseks."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 095f41c35641834a1ed8ac2527c7014826921376
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-training-courses"></a>Koolituskursuste seadistamine

[!include[banner](includes/banner.md)]


Inimressursside administraatorid ja haldurid saavad kasutada kursuste funktsioone töötajatele pakutavate koolituste kohta teabe haldamiseks.

 <a name="set-up-prerequisites"></a> Seadistuse eeltingimused
---------------------

Järgmine teave on vajalik ja tuleb seadistada enne kursuste loomist.
-   **Kursuste tüübid**

Järgmine teave on valikuline teave, mille saate kursustele määrata. Kui teate, et kavatsete seda teavet kursuste kohta sisestada, tuleb see seadistada enne kursuse kirjete loomist.
-   **Klassiruumide grupid**
-   **Kursuste grupid**
-   **Kursuste toimumiskohad**
-   **Klassiruumid**
-   **Juhendajad**

## <a name="course-types"></a>Kursuste tüübid
Saate kursusi nende struktuuri või sisu alusel tüüpide järgi kategooriatesse paigutada. Saate luua kursuste tüüpe lehel **Kursuste tüübid**. Kursuse kirje loomisel tuleb valida kursuse tüüp.

## <a name="course-setup-type"></a>Kursuse seadistuse tüüp
Järgmises tabelis on antud kolm kursuste seadistuse tüüpi. Seadistuse tüübid määravad kursuse struktuuri.

<table>
<thead>
<tr class="header">
<th>Seadistuse tüüp</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standardne</strong></td>
<td>Valige see tüüp ilma päevakavata kursuste puhul. See on uue kursuse loomisel seadistuse vaiketüüp.</td>
</tr>
<tr class="even">
<td><strong>Päevakord</strong></td>
<td>Valige see tüüp mitme päeva jooksul toimuva kursuse iga päeva üksikasjade plaanimiseks.</td>
</tr>
<tr class="odd">
<td><strong>Päevakord + seanss</strong></td>
<td>Valige see tüüp keerukamate kursuste puhul. Näiteks saate jaotada kursuse päevakava teedeks ja sessioonideks.
<ul>
<li><strong>Tee</strong> – teed on kursuse konkreetsed teemavaldkonnad.</li>
<li><strong>Sessioonid</strong> – sessioonid jagavad teid ja aitavad tuvastada tee konkreetseid protsesse või võtteid.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kursuse ülesanded
Iga kursuse puhul saate täita järgmisi ülesandeid.
-   Osalejate registreerimine
-   Registreerimise lõpptähtaja määramine
-   Osalejate vähima ja suurima arvu määratlemine
-   Kursuse asukoha ja klassiruumi määramine
-   Kursusel osalejatele hotellide soovitamine
-   Kursuse kirjelduse loomine töötaja iseteeninduses reklaamimiseks.

  >**Märkus.** Kursuse saate kustutada ainult siis, kui keegi pole sellele registreerunud. 
    
## <a name="course-statuses"></a>Kursuse olekud
Järgmises tabelis on antud võimalikud kursuse olekud ja toimingud, mida saate teha, kui kursus on teatud olekuga.

<table>
<thead>
<tr class="header">
<th>Olek</th>
<th>Tegevused</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Loodud</strong></td>
<td><ul>
<li>Kursuseteabe sisestamine ja redigeerimine.</li>
<li>Kursusele oleku <strong>Avatud</strong> määramine, et töötajad saaksid end kursusele registreerida.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ava</strong></td>
<td><ul>
<li>Kursusele osalejate registreerimine.</li>
<li>Kursuselt osalejate eemaldamine.</li>
<li>Kursusel osalejate kinnitamine.</li>
<li>Kursuse olekuks saab määrata<strong> Suletud</strong> või <strong>Tühistatud</strong>.</li>
<li>Nende osalejate jaoks, kelle olek on <strong>Kinnitatud</strong>, saab kavandada küsimustikke.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Suletud</strong></td>
<td>Saate kursuse uuesti avada.</td>
</tr>
<tr class="even">
<td><strong>Tühistatud</strong></td>
<td>Saate kursuse uuesti avada.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kursusel osalejad
Kursusel osalejad on töötajad, kandidaadid või kontaktisikud, kes koolituskursusel või sündmusel osalevad. Saate registreerida osalejaid ainult avatud kursustele. Minimaalne ja maksimaalne kursusele registreeritav osalejate arv määratakse kiirkaardil **Üldine** lehel **Kursused**.

<a name="workflow"></a>Töövoog
--------

Töötajad, kes registreeruvad kursusele lehe **Töötaja iseteenindus** kaudu, saavad lasta oma registreerumisel läbida kinnitamise töövoo.  Töövoo saab kursusele määrata lehe **Kursused** kiirkaardil **Üldine**.






