---
title: "Koosluse lõpetatuks kinnitamine"
description: "See artikkel käsitleb koosluste lõpetatuks märkimist."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 318c88f88277a8300b1fcda5056a9a92c9a81eae
ms.lasthandoff: 03/31/2017


---

# <a name="report-boms-as-finished"></a>Koosluse lõpetatuks kinnitamine

[!include[banner](../includes/banner.md)]


See artikkel käsitleb koosluste lõpetatuks märkimist.

Lehti **Kinnita lõpetamine** ja **Max lõpetatuna kinnitatud** kasutatakse materjalikoosluste lõpetatuna kinnitamiseks. Põhimõtteliselt on koosluse lõpetamise kinnitamise protsess sama, mis tootmistellimuse lõpetamise kinnitamise protsess. Seda protsessi saab kasutada näiteks lihtsates komplekteerimisprotsessides, kus keerukamaid tootmistellimuste võimalusi pole vaja. Lehel **Kinnita lõpetamine** saate kinnitada partiina mitme koosluse lõpetamise. Lehel **Max lõpetatuna kinnitatud** saate kinnitada korraga ainult ühe koosluse lõpetamise. Leht **Kinnita lõpetamine** on saadaval jaotise Laohaldus menüüelemendis ja mõlemad lehed on saadaval menüüelementidena lehel **Väljastatud tooted**.

## <a name="report-as-finished-page"></a>Leht Kinnita lõpetamine
Kui avate väljastatud toote juures lehe **Kinnita lõpetamine**, soovitab leht, et kinnitaksite standardvaru vaikekoguse lõpetamise. Vaikimisi kuvatakse aktiivne koosluse versioon, kuid saate koosluse versiooni muuta, kui on muid kinnitatud versioone. Sellel lehel saate ka kustutada kirjeid ja luua uusi kirjeid toodetele, mille lõpetamine on vaja kinnitada. Päringu kasutamiseks toodete valimisel klõpsake menüüelementi **Vali**. Saate valitud toodete lõpetamise käsitsi kinnitada, klõpsates **OK**. Teine võimalus on seadistada pakktöötluse protsess. Kui lõpetamise kinnitamise protsess on kinnitatud, genereerib süsteem koosluse töölehe, kus töödeldakse varudesse sisestamist. See tööleht koosneb ühest valmis toote reaüksusest ja reaüksusest iga koosluse rea kohta. Saate juhtida, kas tööleht sisestatakse automaatselt või jäetakse täiendavaks kohandamiseks lahti.

## <a name="max-report-as-finished-page"></a>Maks. leht Kinnita lõpetamine
Lehel **Max lõpetatuna kinnitatud** tähistab iga koosluse rida toote tükkide arvu, mille lõpetamist saab kinnitada. See arvutus põhineb iga materjalirea füüsilisel vabal kaubavarul. Järgmises näites tarbib üks ühik kaupa numbriga FG kaks ühikut toormaterjali RM10 ja ühe ühiku toormaterjali RM20. Kuna laos on ainult 10 ühikut RM10, on maksimaalne FG kogus, mille saab lõpetatuks kinnitada, viis ühikut. Väärtus kuvatakse väljal **Max lõpetatuna kinnitatud**.

| Tase | Kaubakood | Kogus | Laoseis | Maks. Teata lõpetamisest |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | –2       | 10      | 5                       |
| 1     | RM20        | –1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Mitme tasemega kooslused
Kui kooslusel on mitu taset, saate juhtida materjalide arvestamise viisi kõigil tasemetel, kasutades välja **Koosnevus**. See väli on saadaval nii lehel **Kinnita lõpetamine** kui ka lehel **Max lõpetatuna kinnitatud**. Valikud on järgmised:

-   **Mitte kunagi** – aluseks olevaid kooslusi ei jaotata, kui materjali on puudu.
-   **Alati** – kõik aluseks olevad kooslused jaotatakse täielikult. Seetõttu ei kasutata pooleliolevate komponentkaupade puhul ühtegi vaba kaubavaru.
-   **Puudujääk** – aluseks olevad kooslused jaotatakse ainult juhul, kui kogu soovitud materjali kogust pole saadaval.

### <a name="example"></a>Näide

Selles näites on lõpetatuks märkimiseks valmis kolm valmis tooteühikut (kaubakoodiga FG). Kooslus on kahetasemeline, nagu siin näidatud.

| Tase | Kaubakood | Koosluse rea kogus | Laoseis |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | KOMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Järgmistes tabelites on näidatud, kuidas väli **Koosnevus** mõjutab koosluse töölehe ridade genereerimise viisi. **Koosnevus: mitte kunagi**

| Tase | Kaubakood | Kogus |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | KOMP        | –3       |

Nagu eelmine tabel näitas, käsitletakse töölehel mahaarvatuna ainult kaubakoodi KOMP. Kaubakood RM, mis on koodi KOMP osa, ei jaotata töölehe reale ja kahte laos olevat koodi KOMP ühikut ei arvestata. **Koosnevus: alati**

| Tase | Kaubakood | Kogus |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | –3       |

Sellisel juhul jagatakse kaubakood KOMP toormaterjaliks kaubakoodiga RM. Kahte laos olevat kaubakoodi KOMP ühikut ei arvestata tarbitava RM-i koguses. **Koosnevus: puudujääk**

| Tase | Kaubakood | Kogus |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | KOMP        | –2       |
| 1     | RM          | –1       |

Sellisel juhul arvestatakse kaubakoodi KOMP kahte laoühikut. Kuid kuna kaubakoodi FG on vaja kolm ühikut, on vaja ka ühte ühikut kaubakoodiga RM, et teha veel üks ühik kaupa KOMP.




