---
title: Isiklike andmete muutmine
description: Selles artiklis kirjeldatakse, kuidas redigeerida isikuandmeid töövõtja ja ülemuse iseteeninduses.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80b4537601491c97c24cfa1fef5088cbf1ac276df76534034117161b0fe79dc2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715891"
---
# <a name="edit-personal-information"></a>Isiklike andmete muutmine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate Dynamics 365 Human Resourcesi isikuandmeid redigeerida jaotises **Töövõtja iseteeninduse tööruum**.

Redigeeritavate isikuandmete hulka kuulub järgnev.

- Aadressid
- Kontakti üksikasjad
- Isiklikud kontaktid
- ID-numbrid
- Makseviis
- Human Resourcesis kasutatav pilt

>[!NOTE]
>On võimalik, et te ei saa redigeerida teatud tüüpi isiklikke andmeid, nt ärikontakti üksikasju. Lisateavet vt teemast [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md).

Globaalses aadressiraamatus seatud parameetrid määratlevad rollid, mis näevad teie isikuandmeid.

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

7. Selleks, et muuta meetodeid, mille alusel teile makstakse, valige vahekaart **Minu makseteave**. See vahekaart on saadaval ainult juhul, kui makseviisid on lubatud vormil **Human Resourcesi parameetrid**. Personalijuht saab lubada suvandid **Pangaveksel**, **Sularaha**, **Tšekk**, **Elektroonilise makse** või **Muu**. Personalijuht saab keelata ka elektroonilise makse kinnitamise (kasutatakse USA palga puhul) ning pangakonto ja marsruudi valiku numbri kinnitamise.

8. Human Resourcesis kuvatava profiilipildi muutmiseks valige vahekaart **Pilt**. Olenevalt teie organisatsiooni sätetest võivad pildid läbida kinnitamise protsessi.

    - Pildi üleslaadimiseks valige **Laadi üles uus pilt**.
    - Pildi eemaldamiseks valige pilt ja seejärel valige **Eemalda**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]