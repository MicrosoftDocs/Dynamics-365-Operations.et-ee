---
title: Koolituskursuste seadistamine
description: Inimressursside administraatorid ja haldurid saavad kasutada kursuste funktsioone töötajatele pakutavate koolituste kohta teabe haldamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 253f0d07679b6327a0ed1e3cc20ede66249750b8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418220"
---
# <a name="set-up-training-courses"></a>Koolituskursuste seadistamine

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
- Osalejate registreerimine
- Registreerimise lõpptähtaja määramine
- Osalejate vähima ja suurima arvu määratlemine
- Kursuse asukoha ja klassiruumi määramine
- Kursusel osalejatele hotellide soovitamine
- Kursuse kirjelduse loomine töötaja iseteeninduses reklaamimiseks.

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
Kursusel osalejad on töötajad, kes koolituskursusel või sündmusel osalevad. Saate registreerida osalejaid ainult avatud kursustele. Minimaalne ja maksimaalne kursusele registreeritav osalejate arv määratakse kiirkaardil **Üldine** lehel **Kursused**.

<a name="workflow"></a>Töövoog
--------

Töötajad, kes registreeruvad kursusele lehe **Töötaja iseteenindus** kaudu, saavad lasta oma registreerumisel läbida kinnitamise töövoo. Te võite määrata töövookursusele lehe **Kursused** kiirkaardil **Üldine**.







[!INCLUDE[footer-include](../includes/footer-banner.md)]