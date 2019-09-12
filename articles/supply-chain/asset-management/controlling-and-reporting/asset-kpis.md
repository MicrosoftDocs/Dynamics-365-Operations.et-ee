---
title: Vara KPI-d
description: Selles teemas tutvustatakse vara KPI-sid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4fc32d337be1f71932555fcb062a8d05c9ca9bda
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918414"
---
# <a name="asset-kpis"></a>Vara KPI-d

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varahalduses saate arvutada mitmesuguseid juhtimismõõdikuid (KPI-sid) varade ja vara tüüpide kohta. KPI-sid saate kasutada selleks, et saada ülevaade varade jõudlusest, mis on seotud näiteks tööaja, seisakuaja, parandamisaja ja keskmise rikkevahelise ajaga (MTBF).

1. Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Vara KPI-d**.

2. Dialoogiboksis **Arvuta vara KPI-d** valige **Ajaskaala**, mida soovite arvutamisel kasutada ja periood väljadel **Kuupäevast** ja **Kuupäevani**. 

3. Kiirkaardil **Kaasatavad kirjed** saate vajaduse korral valida konkreetsed varad ja vara tüübid, mida soovite arvutusse kaasata.

4. Arvutuse alustamiseks klõpsake **OK**.

5. Vahekaardil **Ülevaade** kuvatakse ruudustikvaates arvutuse tulemused. Iga vara kuvatakse eraldi real.

6. Kiirkaardil **Valitud rea KPI-d** näete arvutusi valitud vara kohta vahekaardil **Ülevaade**. KPI-de väärtused on kategoriseeritud järgmiste omaduste alusel: **Aeg**, **Kättesaadavus**, **Töökäsud**, **Hooldus**, **Vead**, **Hoolduskatkestus** ja **Kulu**.

Allolevast tabelist leiate lehel **Vara KPI-d** olevate väljade kirjelduse.

| Väli                   | Kirjeldus                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vara                   | Vara-ID.                                                                                                                                                                                                                                                                                             |
| Koondaeg              | Arvutuses kasutatavas kalendris sätestatud koondaeg. Kui vara on seotud ressursiga, kasutatakse seotud ressursi kalendrit. Kui vara ei ole ressursiga seotud, kasutatakse kalendrit, mis on valitud väljal **Standardne kalender** suvandis **Varahalduse parameetrid**. |
| Tööaeg                  | Koondaeg miinus seisakuaeg.                                                                                                                                                                                                                                                                            |
| Seisakuaeg                | Hoolduskatkestuse registreeringud, mis on varale valitud perioodi jooksul tehtud.                                                                                                                                                                                                                              |
| Parandamisaeg             | Töötundide koguarv, mis on kulutatud paranduse töökäskudele.                                                                                                                                                                                                                                            |
| Kättesaadavuse %          | Tööaeg jagatuna koondajaga ja korrutatud 100-ga.                                                                                                                                                                                                                                                   |
| Vigade arv        | Valitud perioodil vara vea sümptomitele registreeritud vea põhjuste arv.                                                                                                                                                                                                             |
| MTBF                    | Keskmine rikkevaheline aeg, mis on koondaeg jagatud valitud perioodil vara vea sümptomitele registreeritud vea põhjuste arvuga. Kui vigade arv on null, määratakse MTBF-i väärtuseks koondaeg.                                                                                                                   |
| Nurjumismäär               | 1 jagatud MTBF-iga.                                                                                                                                                                                                                                                                                    |
| MRT                     | Keskmine parandamisaeg, mis on parandamisaeg jagatud valitud perioodil varale registreeritud vigade arvuga. Kui vigade arv on null, määratakse MRT väärtuseks parandamisaeg.                                                                                                                           |
| Seisakute arv         | Varale loodud hoolduskatkestuse registreeringute arv.                                                                                                                                                                                                                                     |
| MTBS                    | Keskmine seisakutevaheline aeg, mis on koondaeg jagatud hoolduskatkestuste registreeringute arvuga. Kui hoolduskatkestuse registreeringute arv on valitud perioodil null, määratakse MTBS väärtuseks koondaeg.                                                                                      |
| Ennetav kulu         | Valitud perioodil varale sisestatud kulud, mis on seotud kulu tüübiga "Ennetav". Kulu tüübid määratakse töökäsu tüüpidele.                                                                                                                                                                       |
| Parandav kulu         | Valitud perioodil varale sisestatud kulud, mis on seotud kulu tüübiga "Parandav". Kulu tüübid määratakse töökäsu tüüpidele.                                                                                                                                                                       |
| Asendusväärtus       | Varale asendusväärtusena määratud väärtus.                                                                                                                                                                                                                                                  |
| Vara tüüp             | Varale valitud vara tüübi ID.                                                                                                                                                                                                                                             |
| Tootja           | Varale valitud tootja ID.                                                                                                                                                                                                                                                 |
| Mudel                   | Varale valitud tootja mudeli ID.                                                                                                                                                                                                                                           |
| Kuupäevast               | KPI arvutuse alguskuupäev. Kui vara loodi pärast arvutuse jaoks valitud alguskuupäeva, näidatakse sellel väljal vara alguskuupäeva.                                                                                                                                  |
| Kuupäevani                 | KPI arvutuse lõppkuupäev. Kui vara registreeriti passiivsena enne arvutuse jaoks valitud lõppkuupäeva, näidatakse sellel väljal kuupäeva, millal vara ei olnud enam aktiivne.                                                                                               |
| Ajaskaala              | KPI-de arvutuse jooksul valite ajaskaala, mida kasutatakse: tunnid, päevad või nädalad.                                                                                                                                                                                                            |
| Kättesaadavus            | Tööaeg jagatud koondajaga.                                                                                                                                                                                                                                                                         |
| Töökäsud             | KPI arvutusse kaasatud töökäskude koguarv.                                                                                                                                                                                                                                          |
| Töökäsu aeg         | Töötundide koguarv, mis on kulutatud töökäskudele.                                                                                                                                                                                                                                               |
| Esmased töökäsud     | KPI arvutusse kaasatud esmaste töökäskude arv.                                                                                                                                                                                                                                        |
| Teisesed töökäsud   | KPI arvutusse kaasatud teiseste töökäskude arv.                                                                                                                                                                                                                                      |
| Hoolduse töökäsud | KPI arvutusse kaasatud hoolduse töökäskude arv. Hoolduse töökäsk on töökäsk, millel pole seotud vea põhjuseid.                                                                                                                                                             |
| Hooldusaeg        | Kogu töötundide arv, mis on kulutatud hoolduse töökäskudele.                                                                                                                                                                                                                                       |
| Paranduse töökäsud      | KPI arvutusse kaasatud paranduse töökäskude arv. Paranduse töökäsk on töökäsk, millel on seotud vea põhjus.                                                                                                                                                                        |
| Usaldusväärsuse %           | Arvutus mis põhineb vara vea registreeringute oodataval eksponentsiaalsel arengul, mis tähendab, et aja jooksul muutub vara kulumise tõttu vähem töökindlaks. Selle KPI arvutus põhineb MTBF-il ja koondajal.                                                            |
| MTPS                    | Keskmine tootmisseisakute aeg, mis on hoolduskatkestuse aeg jagatud hoolduskatkestuste registreeringute arvuga. Kui hoolduskatkestuse registreeringute arv on valitud perioodil null, määratakse MTPS väärtuseks null.                                                                               |
| Kogukulu              | Valitud perioodil varale sisestatud kogukulud.                                                                                                                                                                                                                                              |
| Investeerimiskulu         | Valitud perioodil varale sisestatud kulud, mis on seotud kulu tüübiga "Investeerimine". Kulu tüübid määratakse töökäsu tüüpidele.                                                                                                                                                                       |

Allolev joonisel on näha kuvatõmmis nelja vara KPI-de arvutusest.

![Joonis 1](media/11-controlling-and-reporting.png)

- Saate mitmikvaliku abil valida mitu vara suvandis **Kõik varad** ja klõpsates nupule **Vara KPI-d** vahekaardil **Üldine**. Seejärel klõpsake **OK** dialoogiboksis **Arvuta vara KPI-d**, et arvutada valitud varade KPI-d.  
- KPI arvutuse tulemuste hulgas võib sisalduda või mitte sisalduda [hoolduskatkestuste registreeringud](../work-orders/maintenance-downtime.md), sõltuvalt hoolduskatkestuse põhjuse koodide seadistusest ja kasutusest. 

