---
title: Projektimeeskonna koostamine
description: See teema sisaldab teavet projektimeeskondade loomise ja haldamise kohta.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760524"
---
# <a name="create-a-project-team"></a>Projektimeeskonna koostamine

[!include [banner](../includes/banner.md)]

Projektis eelnevalt seadistatud rollide kasutamiseks peab projektijuht need rollid projektiga seostama. Projektile saab määrata mitu rolli. Segaduse vältimiseks märgistatakse need rollid reserveerimise käigus automaatselt. Näiteks kui projektijuht vajab kolme tarkvarainseneri, luuakse automaatselt kolm tarkvarainseneri rolli, mille sildid on **tarkvarainsener 1**, **tarkvarainsener 2** ja **tarkvarainsener 3**. Kui rollile olid eelnevalt määratud rolli omadused, rakendatakse need ressursi otsingute käigus filtrina. Otsingu täiendavaks täpsustamiseks saab omadusi lisada.

Kuvasätteid saab samuti kohandada, et anda parem vaade ressursi saadavuse kohta. On olemas valikud saadavuse kuvamiseks tunnis, päevas, nädalas, kuus, kvartalis ja aastas. On olemas ka valik näidata ressursside olemasolevat ja järelejäänud mahtu. Sellest valikust on kasu aja juhtimisel, kui hindate tegevuste jaoks saadaolevat aega või ressursi kättesaadavust.

Projektijuht võib valida lehelt rolli ja siis, kui on olemas vajadusele vastav kättesaadav ressurss, valida ressursi reserveerimise rolli täitmiseks. Pange tähele, et ressursse pole plaanimise etapi selles osas vaja reserveerida. WBS-i loomisel saate asendada rollid projekti komplekteeritud ressurssidega. Kui rollid asendatakse WBS-is komplekteeritud ressurssidega, värskendab ressursi seadistus automaatselt projektimeeskonna loendit ja plaanimist.

[![Projekti töörühma loend, mis sisaldab nii rolle kui ka tegelikke ressursse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektijuhil on mitmesuguseid võimalusi projektile ressursi reserveerimiseks, nt **Järelejäänud võimsus**, **Täisvõimsus**, **Võimsuse protsent** ja **Tundide määramine**. Neid reserveerimisvalikuid saab ressursi määrangute muutumisel igal ajal tühistada. Toetatakse kahte reserveerimise tüüpi:

- **Fikseeritud reserveerimine** – ressursi reserveerimine kinnitati töötamiseks tegevusega määratud perioodil.
- **Esialgne reserveerimine** – ressurss reserveeriti esialgselt töötamiseks tegevusega määratud perioodil.

Järgmine protseduur selgitab, kuidas projektimeeskonda koostada.

## <a name="create-a-project-team"></a>Projektimeeskonna koostamine

1. Valige loendilehelt **Kõik projektid** projekt ja valige siis **Redigeeri**.
2. Sisestage vahekaardile **Projektimeeskond ja plaanimine** väljal **Graafiku lõppkuupäev** graafiku alguskuupäev pluss üks kuu. Näiteks kui graafiku alguskuupäev on 24. juuni 2017 (24/06/2017), sisestage **24/07/2017**.
3. Valige **Lisa**.
4. Valige paanilt **Projektile rollide lisamine** väljal **Roll** väärtus **Vanem-projektijuht**.
5. Valige **Nõutud pädevused**.
6. Lehel **Omaduste valimine** on vaikimisi valitud omadused, mille eelnevalt vanem-projektijuhi rollile määrasite. Valige **OK**.
7. Sisestage lehe **Rollide lisamine projektidele** väljale **Ressursside arv** väärtus **1**.
8. Väljal **Ressurss** näitab otsing kõiki ressursse, millel on vajalikud kompetentsid. Valige **Daniel Goldschmidt** ja seejärel **Loo**.
9. Tehke lehel **Projekt** valik **Lisa**.
10. Valige paanilt **Projektile rollide lisamine** väljal **Roll** väärtus **Meeskonnaliige**. Sisestage väljale **Ressursside arv** väärtus **5**.
11. Valige **Loo**.
12. Tehke lehel **Projektid** valik **Täida ressurss**.

## <a name="monitor-project-teams"></a>Jälgida projektimeeskondi
1. Valige lehelt **Kõik projektid** projekti **XYZ täiendusfaas 2** link **Projekti ID**.
2. Veenduge, et kiirkaardil **Projektimeeskond ja plaanimine** loetletud projektiressursid on õiged.
