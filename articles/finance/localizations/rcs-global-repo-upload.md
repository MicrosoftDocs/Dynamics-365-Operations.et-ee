---
title: ER-konfiguratsioonide loomine RCS-is ja üleslaadimine globaalsesse hoidlasse
description: Selles teemas selgitatakse, kuidas luua elektroonilise aruandluse (ER) konfiguratsiooni Microsoft Regulatory Configuration Servicesis (RCS) ja globaalsesse hoidlasse üles laadida.
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a138fd4b525077f12f6575f4b10f682728b71203
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838715"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-konfiguratsioonide loomine Regulatory Configuration Servicesis RCS ja üleslaadimine globaalsesse hoidlasse

[!include [banner](../includes/banner.md)]

Saate kasutada Microsoft Regulatory Configuration Servicesi (RCS) elektroonilise aruandluse (ER) konfiguratsioonide loomiseks ja avaldamiseks, et neid saaks kasutada teie organisatsioonis.

Järgmistes protseduurides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolliga kasutaja saab luua RCS-i eksemplaris loodud ER-konfiguratsiooni tuletatud versiooni ja seejärel laadida tuletatud konfiguratsioon üles globaalsesse hoidlasse. 

Enne nende protseduuride lõpule viimist peate esmalt viima lõpule järgmised eeltingimused.

- RCS-i eksemplarile juurde pääsemine.
- Looge aktiivne konfiguratsioonipakkuja. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Samuti peate veenduma, et teie ettevõttele valmistatakse ette RCS-i keskkond.

1. Avage rakenduse Finance and Operations jaotis **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – välise konfigureerimine** ja seejärel järgige juhiseid selle ettevalmistamiseks.

Kui teie ettevõtte jaoks juba RCS-i keskkond ette valmistatud, kasutage sellele juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Konfiguratsiooni tuletatud versiooni loomine RCS-is

1. Kinnitage tööruumis **Elektrooniline aruandlus**, et teie organisatsioonil on aktiivne konfiguratsiooni pakkuja. 
2. Valige **Aruandluse konfiguratsioonid**.
3. Valige konfiguratsioon, millest soovite tuletada uut versiooni. Otsingu kitsendamiseks saate kasutada puu kohal olevat filtri välja.
4. Valige **Konfiguratsiooni loomine** \> **Tuleta nimest**.
5. Sisestage nimi ja kirjeldus ning seejärel valige **Konfiguratsiooni loomine** uue tuletatud versiooni loomiseks.
6. Valige äsja tuletatud konfiguratsioon, lisage versiooni kirjeldus ja seejärel valige **OK**. Konfiguratsiooni olekuks muudetakse **Lõpetatud**.

![Uus konfiguratsiooni versioon RCS-is](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kui konfiguratsiooni olekut muudetakse, võidakse kuvada ühendatud rakendustega seotud kinnitamise tõrketeade. Kinnitamise väljalülitamiseks valige Toimingupaani vahekaardil **Konfiguratsioonid** suvand **Kasutaja parameetrid** ja seadke seejärel suvandi **Konfiguratsiooni oleku muutmise ja lahendamise vahele jätmine** väärtuseks **Jah** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Konfiguratsiooni üleslaadimine globaalsesse hoidlasse

Uue või tuletatud konfiguratsiooni ühiskasutusse andmiseks oma organisatsioonis, saate selle üles laadida globaalsesse hoidlasse.

1. Valige konfiguratsiooni lõpule viidud versioon ja seejärel valige **Hoidlasse üleslaadimine**.
2. Valige suvand **Globaalne (Microsoft)** ja seejärel valige **Laadi üles**.

    ![Hoidlasse üleslaadimise suvandid](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Valige kinnituse teateaknast **Jah**. 
4. Värskendage versiooni kirjeldust vastavalt vajadusele ja seejärel valige **OK**. 

Konfiguratsiooni olekuks värskendatakse **Ühiskasutus** ja konfiguratsioon laaditakse üle globaalsesse hoidlasse. Seal saate sellega töötada järgmistel viisidel.

- Importige see oma Dynamics 365 eksemplari. Lisateabe saamiseks vt teemat [(ER) konfiguratsioonide importimine RCS-ist](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Kolmanda osapoolega või välise organisatsiooniga ühiskasutusse andmiseks vt teemat [RCS-i ühiskasutatava elektroonilise aruandluse (ER) konfiguratsioonid väliste organisatsioonidega](rcs-global-repo-share-configuration.md)

    ![Tuletatud intrastati Contoso konfiguratsiooni versioon globaalses hoidlas](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Konfiguratsiooni kustutamine globaalsest hoidlast
Organisatsiooni loodud konfiguratsiooni kustutamiseks tehke järgmist.

1. Veenduge tööruumis **Elektrooniline aruandlus**, et teie konfiguratsioonipakkuja oleks **Aktiivne**. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Valige oma aktiivse konfiguratsioonipakkuja juures **hoidla**.
3. Valige hoidla tüüp **Globaalne** ja valige **Ava**.
4. Leidke kiirkaardil **Filter** konfiguratsioon, mida soovite kustutada funktsiooni **Filter** abil.
5. Valige kiirkaardil **Versioon** konfiguratsiooni versioon, mida soovite kustutada, ja seejärel valige **Kustuta**.

    ![Konfiguratsiooni kustutamine globaalsest hoidlast](media/RCS_Delete_from_GlobalRepo.JPG)

6. Valige kinnituse teateaknast **Jah**.

    ![Konfiguratsiooni versiooni kinnitusteate kustutamine](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfiguratsiooni versioon kustutatakse ja kuvatakse kinnitusteade. 

> [!NOTE]
> Konfiguratsiooni saab kustutada ainult konfiguratsiooni loonud konfiguratsioonipakkuja. Kui konfiguratsiooni on jagatud mõne muu organisatsiooniga, tuleb jagamine enne konfiguratsiooni kustutamist tühistada.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]