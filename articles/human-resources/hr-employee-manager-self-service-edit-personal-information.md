---
title: Isiklike andmete muutmine
description: Selles artiklis kirjeldatakse, kuidas redigeerida isikuandmeid töövõtja ja ülemuse iseteeninduses.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7e78873d0995334ac80ac22e8058b7fe0bc31ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686118"
---
# <a name="edit-personal-information"></a>Isiklike andmete muutmine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate Dynamics 365 Human Resources`i isikuandmeid redigeerida jaotises **Töövõtja iseteeninduse** tööruum.

Redigeeritavate isikuandmete hulka kuulub järgnev.

- Aadressid
- Kontakti üksikasjad
- Isiklikud kontaktid
- ID-numbrid
- Makseviis
- Human Resourcesis kasutatav pilt

>[!NOTE]
>On võimalik, et te ei saa redigeerida teatud tüüpi isiklikke andmeid, nt ärikontakti üksikasju. Lisateavet vt teemast [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md).

**Globaalses aadressiraamatu parameetrid** lehel seatud parameetrid määratlevad rollid, kes näevad teie isikuandmeid.

1. Human Resourcesis valige **Töövõtja iseteenindus**.

2. Valige **Redigeeri isikuandmeid**.

3. Aadressi muutmiseks valige vahekaart **Aadressid**. Teie tehtud muudatused kuvatakse personalijuhi teavitamiseks tööruumis **Personalihaldus**.

    - Uue aadressi lisamiseks valige **Lisa**.
    - Olemasoleva aadressi redigeerimiseks valige aadress ja seejärel valige **Redigeeri**.
    - Kaardi vaatamiseks valige **Kaart**.
    - Kontakti lisamiseks või eemaldamiseks valige **Rohkem suvandeid** ja seejärel valige **Täpsem**. Jaotises **Kontaktteave** valige **Lisa** või **Eemalda** ja redigeerige välju vastavalt vajadusele.
    - Ajavööndi ja asukoha määramiseks valige **Rohkem suvandeid** ja seejärel valige **Täpsem**. Jaotises **Üldine** redigeerige välju vastavalt vajadusele.

4. Oma kontaktandmete muutmiseks valige vahekaart **Kontaktandmed**. Saate anda erinevat kontaktteavet, sh telefoni, meili ja sotsiaalmeedia linke. Saate määrata kontaktteabe esmaseks, kuid esmaseks saab määrata igast tüübist ainult ühe.

    - Uue kontaktteabe lisamiseks valige **Lisa**. Redigeerige välju vastavalt vajadusele.
    - Olemasoleva kontaktteabe redigeerimiseks valige üksus ja seejärel valige **Redigeeri**. Redigeerige välju vastavalt vajadusele.
    - Kontaktteabe privaatsena määramiseks valige see üksus, valige **Täpsem** ja seadke nupp **Privaatne** väärtusele **Jah**. Valige nupp **OK**.
      >[!NOTE]
      >Nupp **Täpsem** pole saadaval, kui teie administraator on lubanud teie keskkonnas funktsiooni **(Eelversioon) Piirake töötajatel aadressi- ja kontaktteabe lisamist või redigeerimist kindlal otstarbel**. Lisateavet vt teemast [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md).
  
5. Isiklike kontaktide muutmiseks valige vahekaart **Isiklikud kontaktid**. Saate määrata lähedasi isikuid, kasusaajaid ja sõltuvaid. Kontaktiks võib olla isik või organisatsioon. Funktsioon **Soodustuste haldus** kasutab isiklikke kontaktandmeid. Lisateavet leiate teemast [Isiklike kontaktide sobivuse suvandite konfigureerimine](hr-benefits-setup-contact-eligibility-options.md).

6. ID-numbrite (nt isikukood) muutmiseks valige vahekaart **ID-numbrid**. Muudatused võivad läbida kinnitamise protsessi, kui teie organisatsioonis on seadistatud kinnitamise töövoog.

    - ID-numbri lisamiseks valige **Uus**. Täitke väljad vastavalt vajadusele ja valige **Salvesta**.
    - Numbri redigeerimiseks valige **Redigeeri**. Redigeerige väljad vastavalt vajadusele ja valige **Salvesta**.

7. Makseviiside muutmiseks, mille järgi teile makstakse, valige vahekaart **Minu makseteave** . See vahekaart on saadaval ainult siis, kui makseviisid on inimressursside **parameetrite lehel** lubatud. Personalijuht saab lubada suvandid **Pangaveksel**, **Sularaha**, **Tšekk**, **Elektroonilise makse** või **Muu**. Personalijuht saab keelata ka elektroonilise makse kinnitamise (kasutatakse USA palga puhul) ning pangakonto ja marsruudi valiku numbri kinnitamise.

8. Human Resourcesis kuvatava profiilipildi muutmiseks valige vahekaart **Pilt**. Olenevalt teie organisatsiooni sätetest võivad pildid läbida kinnitamise protsessi.

    - Pildi üleslaadimiseks valige **Laadi üles uus pilt**.
    - Pildi eemaldamiseks valige pilt ja seejärel valige **Eemalda**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
