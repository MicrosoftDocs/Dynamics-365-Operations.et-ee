---
title: ER-konfiguratsioonide loomine RCS-is ja üleslaadimine globaalsesse hoidlasse
description: See artikkel selgitab, kuidas luua elektroonilise aruandluse (ER) konfiguratsiooni Microsoft Regulatory Configuration Servicesis (RCS) ja laadida see üles globaalsesse hoidlasse.
author: JaneA07
ms.date: 01/11/2021
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
ms.openlocfilehash: f73f7189ad82d85169a4e0df573dd26dab8bb009
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070596"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-konfiguratsioonide loomine Regulatory Configuration Servicesis RCS ja üleslaadimine globaalsesse hoidlasse

[!include [banner](../includes/banner.md)]

Saate kasutada Microsoft Regulatory Configuration Servicesi (RCS) elektroonilise aruandluse (ER) konfiguratsioonide loomiseks ja avaldamiseks, et neid saaks kasutada teie organisatsioonis.

Järgmistes protseduurides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolliga kasutaja saab luua RCS-i eksemplaris loodud ER-konfiguratsiooni tuletatud versiooni ja seejärel laadida tuletatud konfiguratsioon üles globaalsesse hoidlasse. 

Enne nende protseduuride lõpule viimist peate esmalt viima lõpule järgmised eeltingimused.

- Omage juurdepääsu teie organisatsiooni RCS-keskkonnale.
- Looge aktiivne konfiguratsioonipakkuja ja tehke see aktiivseks. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Peate veenduma, et RCS-keskkond on teie organisatsiooni jaoks ette ettevalmistamine. Kui teie organisatsiooni jaoks pole RCS-i eksemplari ette vaadatud, saate seda teha järgmiste sammude abil:

1. Minge finantside ja toimingute rakendusesse Organisatsiooni halduse **tööruumide** \> **elektrooniline** \> **aruandlus**.
2. Väljadel **Seotud lingid / Välised lingid** valige **Regulatiivsed teenused –** Konfiguratsioon ja järgige seejärel juhiseid, et **eraldisesse** registreeruda.

Kui RCS-keskkond on juba teie organisatsiooni jaoks ette ettevalmistamine, kasutage sellele juurdepääsuks lehe URL-i **ja valige sisselogimissuvand**.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Konfiguratsiooni tuletatud versiooni loomine RCS-is

> [!NOTE]
> Kui see on esimene kord, mil olete kasutanud RCS-i, ei ole teil võimalik tuletada ühtegi konfiguratsiooni. Peate importima konfiguratsiooni globaalsest hoidlast. Lisateavet leiate teemast [ER konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Logige sisse** RCS-i ja valige elektroonilise **aruandluse** tööruum.
2. Kontrollige, kas teie organisatsioonil on aktiivne konfiguratsioonipakkuja, mis on seadistatud aktiivseks (vt eeltingimusi). 
3. Valige **Aruandluse konfiguratsioonid**.
4. Valige konfiguratsioon, millest soovite tuletada uut versiooni. Otsingu kitsendamiseks saate kasutada puu kohal olevat filtri välja.
5. Valige **Konfiguratsiooni loomine** \> **Tuleta nimest**.
6. Sisestage nimi ja kirjeldus ning seejärel valige käsk **Loo konfiguratsioon**, et luua uus tuletatud versioon olekuga Mustand.
7. Valige vastloodud konfiguratsioon ja tehke vajadusel konfiguratsioonivormingus lisamuudatusi. 
8. Kui muudatused on tehtud, peate **selle** **avaldamiseks** hoidlas häälestama konfiguratsiooni oleku Muuda olekuks Lõpetatud. Valige nupp **OK**.

![Uus konfiguratsiooni versioon RCS-is.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kui konfiguratsiooni olekut muudetakse, võidakse kuvada ühendatud rakendustega seotud kinnitamise tõrketeade. Kinnitamise väljalülitamiseks valige Toimingupaani vahekaardil **Konfiguratsioonid** suvand **Kasutaja parameetrid** ja seadke seejärel suvandi **Konfiguratsiooni oleku muutmise ja lahendamise vahele jätmine** väärtuseks **Jah** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Konfiguratsiooni üleslaadimine globaalsesse hoidlasse

Uue või tuletatud konfiguratsiooni jagamiseks oma organisatsiooniga saate selle globaalsesse hoidlasse üles laadida järgmiste sammude abil:

1. Valige konfiguratsiooni lõpule viidud versioon ja seejärel valige **Hoidlasse üleslaadimine**.
2. Valige suvand **Globaalne (Microsoft)** ja seejärel valige **Laadi üles**.

    ![Hoidlasse üleslaadimise suvandid.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Valige kinnituse teateaknast **Jah**. 
4. Värskendage versiooni kirjeldust vastavalt vajadusele ja seejärel valige **OK**. Soovi korral saate versiooni üles laadida kas ühendatud rakendusse või GIT-hoidlasse.  

Konfiguratsiooni olek värskendatakse olekusse Ühiskasutuses **ja** konfiguratsioon laaditakse üles globaalsesse hoidlasse. Samuti luuakse teie üleslaaditud konfiguratsiooni mustandversioon ja seda saab kasutada siis, kui on vaja teha edaspidisi muudatusi.

Kui konfiguratsioon on globaalsesse hoidlasse üles laaditud, saate sellega töötada järgmistel viisidel:

- Importige see oma Dynamics 365 eksemplari. Lisateabe saamiseks vt teemat [(ER) konfiguratsioonide importimine RCS-ist](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Kolmanda osapoolega või välise organisatsiooniga ühiskasutusse andmiseks vt teemat [RCS-i ühiskasutatava elektroonilise aruandluse (ER) konfiguratsioonid väliste organisatsioonidega](rcs-global-repo-share-configuration.md)

    ![Tuletatud Intrastati Contoso konfiguratsiooni versioon globaalses hoidlas.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Konfiguratsiooni kustutamine globaalsest hoidlast
Organisatsiooni loodud konfiguratsiooni kustutamiseks tehke järgmist.

1. Veenduge tööruumis **Elektrooniline aruandlus**, et teie konfiguratsioonipakkuja oleks **Aktiivne**. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Valige oma aktiivse konfiguratsioonipakkuja juures **hoidla**.
3. Valige hoidla tüüp **Globaalne** ja valige **Ava**.
4. Leidke kiirkaardil **Filter** konfiguratsioon, mida soovite kustutada funktsiooni **Filter** abil.
5. Valige kiirkaardil **Versioon** konfiguratsiooni versioon, mida soovite kustutada, ja seejärel valige **Kustuta**.

    ![Konfiguratsiooni kustutamine globaalsest hoidlast.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Valige kinnituse teateaknast **Jah**.

    ![Konfiguratsiooni versiooni kinnitusteate kustutamine.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfiguratsiooni versioon kustutatakse ja kuvatakse kinnitusteade. 

> [!NOTE]
> Konfiguratsiooni saab kustutada ainult konfiguratsiooni loonud konfiguratsioonipakkuja. Kui konfiguratsiooni on jagatud mõne muu organisatsiooniga, tuleb jagamine enne konfiguratsiooni kustutamist tühistada.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

