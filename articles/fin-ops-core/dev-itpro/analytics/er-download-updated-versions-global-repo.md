---
title: ER-konfiguratsioonide värskendatud versioonide importimine
description: Selles teemas selgitatakse, kuidas importida konfiguratsiooniteenuse globaalsest hoidlast elektroonilise aruandluse (ER) konfiguratsioonide värskendatud versioone.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679506"
---
# <a name="import-updated-versions-of-er-configurations"></a>ER-konfiguratsioonide värskendatud versioonide importimine

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) [hoidlaid](general-electronic-reporting.md#Repository) kasutatakse [ER-konfiguratsioonide](general-electronic-reporting.md#Configuration) ühiskasutusse andmiseks. Saate [importda](download-electronic-reporting-configuration-lcs.md) ER-konfiguratsioone erinevatest hoidlatest oma Microsoft Dynamics 365 Finance'i eksemplari. ER-konfiguratsioonide importimisel saavad [konfiguratsioonipakkujad](general-electronic-reporting.md#Provider) avaldada hoidlate uusi [versioone](general-electronic-reporting.md#component-versioning), et neid saaks ühiskasutusse anda.

Selles teemas selgitatakse, kuidas importida konfiguratsiooniteenuse globaalsest hoidlast ER-konfiguratsioonide värskendatud versioone. Lisateavet vt teemast [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfiguratsiooniteenus](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Saadaolevate värskendatud versioonide ülevaatamine

1. Logige Finance'i sisse, kasutades üht järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonide versioonide värskenduste importimine**.

    ![Lokalisatsiooni konfiguratsioonide leht](./media/er-download-updated-versions-global-repo1.png)

4. Valige dialoogiboksi **Elektroonilise aruandluse konfiguratsioonide versioonide värksenduste importimine** väljal **Käitusrežiim** suvand **Kuva ainult saadaolevad värskendused**. Seejärel valige **OK**. 

    ![Käitusrežiimi välja väärtuseks on seatud Kuva ainult saadaolevad värskendused](./media/er-download-updated-versions-global-repo2.png)

5. Vaadake üle vastuvõetud teated. Need teated annavad järgmist teavet praeguse Finance'i eksemplari ER-konfiguratsioonide kohta võrreldes globaalse hoidla sisuga.

    - ER-konfiguratsioonide koguarv
    - ER-konfiguratsioonid, mida pole globaalses hoidlas
    - ER-konfiguratsioonid, mille uusim versioon on praeguses Finance'i eksemplaris juba saadaval (nende ER-konfiguratsioonide täieliku loendi kuvamiseks valige link **Teate üksikasjad**.)

        ![Teade „Järgmiste konfiguratsioonide uusimad versioonid on juba imporditud” ja teate üksikasjad](./media/er-download-updated-versions-global-repo3.png)

    - ER-konfiguratsioonid, mille uusim versioon on saadaval globaalses hoidlas ja saab importida praegusesse Finance'i eksemplari (nende ER-konfiguratsioonide täieliku loendi kuvamiseks valige link **Teate üksikasjad**.)

        ![Teade „Saadaolevad värskendused” ja teate üksikasjad](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Saadaolevate värskendatud versioonide importimine

1. Logige Finance'i sisse, kasutades üht järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonide versioonide värskenduste importimine**.
4. Valige dialoogiboksi **Elektroonilise aruandluse konfiguratsioonide versioonide värskenduste importimine** väljal **Käitusrežiim** suvand **Impordi uusimad värskendused**, et importida ER-konfiguratsioonide uusimad versioonid globaalsest hoidlast praegusesse Finance'i eksemplari.
5. Importimise jaoks pakett-töö plaanimiseks määrake kiirkaardi **Käivita taustal** suvandi **Pakktöötlus** väärtuseks **Jah**. Kui soovite korrata importimist regulaarselt, konfigureerige nõutav kordumine.

    ![Käitusrežiimi välja väärtuseks on seatud Impordi uusimad värskendused](./media/er-download-updated-versions-global-repo5.png)

6. Valige nupp **OK**.
7. Et teada saada, millised konfiguratsiooni versioonid on imporditud, järgige ühte järgmistest etappidest.

    - Kui käivitate importimise pakett-töö kasutamise asemel interaktiivselt, vaadake üle vastuvõetud teated.

        ![Interaktiivse importimise käitamise ajal vastuvõetud teated](./media/er-download-updated-versions-global-repo6.png)

    - Kui käivitate importimise partiirežiimis, toimige järgmiselt.

        1. Avage jaotis **Üldine** \> **Päringud** \> **Pakett-tööd** \> **Minu pakett-tööd**.
        2. Otsige üles ja valige töö **Elektroonilise aruandluse konfiguratsiooni versioonide värskenduste importimine** ja seejärel valige toimingupaani vahekaardil **Pakett-töö** töö ajaloo kuvamiseks suvand **Pakett-töö ajalugu**.
        3. Valige lehel **Pakett-töö ajalugu** suvand **Logi**. Seejärel valige töölogi kuvamiseks vastuvõetud teatest link **Teade üksikasjad**.

        ![Töölogi](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Me ei soovita korduva pakett-töö plaanimist, et importida ER-konfiguratsioonide värskendatud versioone globaalsest hoidlast otse töökeskkonda, kuna imporditud versioonid on kasutamiseks kohe saadaval. Selle asemel kasutage seda lähenemist ER-konfiguratsioonide versioonide juurutamiseks liivakastikeskkonda. Seejärel saab neid kõigepealt liivakastikeskkonnas hinnata enne töökeskkonda juurutamist.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](er-download-configurations-global-repo.md)
