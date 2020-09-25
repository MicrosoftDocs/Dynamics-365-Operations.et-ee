---
title: Rollide seadistamine tööjaotuse struktuuri mallides
description: Selles teemas antakse teavet rolliteabe seadistamise kohta tööjaotuse struktuuri mallides.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760526"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Rollide seadistamine tööjaotuse struktuuri mallides

[!include [banner](../includes/banner.md)]

Projektijuhid saavad seadistada tööjaotuse struktuuri (WBS) malle, mida saab rakendada uutele projektidele WBS-i loomisel. Projektijuhid saavad malli loomisel rolle lisada. Kasutage järgmist protseduuri rolli määramiseks WBS-i mallile. 

1. Valige **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektid** > **Tööjaotuse struktuuri mallid**.
2. Tehke valitud WBS-i mallil valik **Üksikasjad**.
3. Valige loendist toiming ja seejärel valige väljalt **Roll** ülesandele määramiseks roll.

## <a name="work-with-a-wbs"></a>WBS-iga töötamine

Saate luua uue WBS-i või kopeerida WBS-i olemasolevalt WBS-i mallilt. Projektijuht saab hõlpsasti ressursse hallata, määrates WBS-is uutele toimingutele rollid. Rollid saab asendada pärast ressursi hankimist või pärast seda, kui on tuvastatud kinnitatud ressurss, kes toiminguga tööle hakkab. See paindlikkus laseb projektijuhtidel järgmisi toiminguid teha.

- Tuvastada WBS-i tööpakettide jaoks vajalike ressursside arvu.
- Prognoosida projekti kulusid.
- Määratleda esialgset eelarvet.
- Prognoosida tegevuse kestust, tuginedes rollidele ja ressurssidele.
- Töötada välja projektijuhtimise plaane, tuginedes olemasolevale projektiteabele.

WBS-i on lisatud valikuid, et ressursieralduse funktsiooni paremini kasutada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressursi määramised</td>
<td>Saate vaadata WBS-i toimingutele määratud ressursse, kuupäevi, tundide arvu ja reserveerimise tüüpi.</td>
</tr>
<tr class="even">
<td>Meeskonna automaatne loomine</td>
<td>Saate lisada automaatselt plaanitud ressursse, kasutades toiminguga seostatud rolle. Finance soovitab automaatselt plaanitud ressursse, kasutades mitmel kriteeriumil põhinevat otsustamise analüüsi, mis põhineb rollidel. Pärast toimingutele WBS-is rollide ja panuse (tunnid) määramist ja struktuuri vabastamist valige <strong>Meeskonna automaatne loomine</strong>. Vajalik arv plaanitud ressursse lisatakse WBS-i ja vahekaardile <strong>Projekti ja meeskonna plaanimine</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurss (ripploend)</td>
<td>Lehel <strong>Ressursi määramise käivitamine </strong>saate valida ressursid fikseeritult või esialgselt reserveerimiseks, tuginedes määratud kestusele. Saate reguleerida kuvasätteid ressursi tegevuste vaatamiseks ja nende kestuse määramiseks. Saate valida ja määrata ressursse tööpaketi tasemel, kasutades järgmisi valikuid.
<ul>
<li><strong>Kinnita</strong> – ülesandele määratud ressursi muudatuste kinnitamine.</li>
<li><strong>Tühista</strong> – ülesandele määratud ressursi muudatuste tühistamine.</li>
<li><strong>Määra automaatselt</strong> – vastava rolliga olemasolev komplekteeritud ressurss valitakse automaatselt ja määratakse valitud toimingule.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Valige lehelt **Kõik projektid** projekt **XYZ täiendusfaas 2**.
2. Valige **Plaanimine** > **Tegevused** > **Tööjaotuse struktuur**.
3. Valige **Uus** järgmiste esimese taseme tegevuste lisamiseks WBS-i.

    - Algatamine
    - Planeerimine
    - Teostamine
    - Seire ja juhtimine
    - Sule

4. Määrake kuupäevad ja panus (tunnid) nii, nagu järgmisel illustratsioonil näidatud.

    [![Kuupäevade ja panuse seadistamine](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valige ülesande rida **Algatamine** ja seejärel tehke väljal **Roll** valik **Vanem-projektijuht**.
6. Valige **Avalda**.
7. Tehke sama rea väljal **Ressurss** valik **Daniel Goldschmidt** ja seejärel **Nõustu**.
8. Valige ülesande rida **Plaanimine** ja seejärel tehke väljal **Roll** valik **Ärianalüütik**.
9. Valige **Avalda** ja seejärel **Meeskonna automaatne loomine**.
10. Valige kuvatavast teateaknast **Jah**.
11. Veenduge, et väljal **Ressurss** oleks väärtus **Ärianalüütik 1**.
12. Ressursi **Ärianalüütik 1** puhul avage otsing ja valige **Ressursi määramise käivitamine**. Siis valige ülesande jaoks töötaja.
13. Valige **Esialgne määramine** &gt; **Täisvõimsus**.

    > [!NOTE] 
    > Te ei saa hoiatust, et määratud ressurss on nüüd 2, kuna ressursside arvuks jääb 1.

14. Kinnitage lehel **Tööjaotuse struktuur** WBS-is ressursi määrang ja valige siis **Salvesta**.
