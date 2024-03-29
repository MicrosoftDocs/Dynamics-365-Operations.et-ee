---
title: ER-konfiguratsioonide jagamine RCS-is / globaalses hoidlas väliste organisatsioonidega
description: See artikkel selgitab, kuidas jagada elektroonilise aruandluse (ER) konfiguratsioone Microsoft Regulatory Configuration Services (RCS) / globaalset hoidlat otse välisorganisatsioonidega.
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284811"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Elektroonilise aruandluse (ER) konfiguratsioonide ühiskasutusse andmine Regulatory Configuration Servicesi (RCS) globaalses hoidlas väliste organisatsioonidega

[!include [banner](../includes/banner.md)]

Saate kasutada Microsoft Regulatory Configuration Servicesi (RCS) elektroonilise aruandluse (ER) konfiguratsioonide ühiskasutusse andmiseks ja välistesse organisatsioonidesse avaldamiseks.

Järgmistes protseduurides selgitatakse, kuidas RCS-i kasutaja saab anda ühiskasutusse ER-konfiguratsiooni versiooni, mis on konfigureeritud RCS-i eksemplaris välise organisatsiooniga. Enne nende protseduuride lõpule viimist peate esmalt viima lõpule järgmised eeltingimused.

- RCS-i eksemplarile juurde pääsemine.
- Looge aktiivne konfiguratsioonipakkuja. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Looge ja laadige üles ER-konfiguratsiooni uus versioon. Lisateabe saamiseks vaadake teemat [Elektroonilise aruandluse (ER) konfiguratsiooni uue versiooni loomine ja üleslaadimine](rcs-global-repo-upload.md).

Samuti peate veenduma, et teie ettevõttele valmistatakse ette RCS-i keskkond.

1. Minge finantside ja toimingute rakendusesse Organisatsiooni halduse **tööruumide** \> **elektrooniline** \> **aruandlus**.
2. Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – välise konfigureerimine** ja seejärel järgige juhiseid selle ettevalmistamiseks.

Kui teie ettevõtte jaoks juba RCS-i keskkond ette valmistatud, kasutage sellele juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Kinnitage konfiguratsioon, mida soovite ühiskasutusse anda

Järgige neid etappe, et kinnitada, kas konfiguratsioon, mida soovite ühiskasutusse anda, on juba üles laaditud globaalsesse hoidlasse.

1. Valige tööruumis **Elektrooniline aruandlus** suvand **Hoidlad** oma konfiguratsioonipakkuja jaoks.

    ![Konfiguratsiooni pakkujad.](media/1_RCS_Repo_for_config_provider.JPG)

2. Valige **Globaalne hoidla** \> **Ava**.
3. Otsige konfiguratsiooni, mida soovite ühiskasutusse anda. Otsingu kitsendamiseks saate kasutada filtri välja. Kui konfiguratsiooni ei kuvata globaalses hoidlas, järgige juhiseid teemas [Elektroonilise aruandluse (ER) konfiguratsiooni uue versiooni loomine ja üleslaadimine](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>ER-konfiguratsioonide ühiskasutusse andmine väliste organisatsioonidega

Pärast konfiguratsiooni loomist teie konfiguratsioonipakkujas, saate anda seda otse väliste organisatsioonidega ühiskasutusse lehe **Globaalne konfiguratsiooni hoidla** kiirkaardi **Ühiskasutuses kasutajaga** abil.

1. Valige tööruumis **Elektrooniline aruandlus** suvand **Hoidlad** oma konfiguratsioonipakkuja jaoks.
2. Valige **Globaalne hoidla** \> **Ava**. 
3. Valige konfiguratsioon, mida soovite ühiskasutusse anda.
4. Valige kiirkaardil **Ühiskasutuses kasutajaga** suvand **Organisatsioon**.

    ![Kiirkaart Ühiskasutuses kasutajaga.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Sisestage dialoogiboksis välise organisatsiooni domeeninimi ja seejärel valige **OK**.

    ![Konfiguratsiooni versiooni ühiskasutusse andmine välise organisatsiooni dialoogiboksiga.](media/1_RCS_Repo_for_Share_with_form.JPG)

Konfiguratsioon on antud ühiskasutusse välise organisatsiooniga ja saadaval globaalses hoidlas selle organisatsiooni jaoks. Sealt saab seda importida organisatsiooni RCS-i eksemplari või selle finantside ja toimingute rakenduste eksemplari.

6. Välise organisatsiooniga varasemalt ühiskasutusse antud konfiguratsiooni ühiskasutusest eemaldamiseks, valige see konfiguratsioon ja klõpsake suvandit **Eemalda ühiskasutusest** ning seejärel valige **OK**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
