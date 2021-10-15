---
title: Varude nähtavuse lisandmooduli installimine
description: See teema kirjeldab varude nähtavuse lisandmooduli installimist rakenduse Microsoft Dynamics 365 Supply Chain Management jaoks.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d6f58eab38d1aee97a5d39704255bf06a168b36c
ms.sourcegitcommit: 79d19924ed736c9210fa9ae4e0d4c41c53c27eb5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2021
ms.locfileid: "7581861"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility installimine ja seadistamine

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

See teema kirjeldab varude nähtavuse lisandmooduli installimist rakenduse Microsoft Dynamics 365 Supply Chain Management jaoks.

Varude nähtavuse lisandmooduli installimiseks peate kasutama teenust Microsoft Dynamics Lifecycle Services (LCS). LCS on koostööportaal, mis pakub keskkonda ja regulaarselt värskendatud teenuseid, mis aitavad hallata finants- ja tegevusrakenduste elutsüklit.

Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Varude nähtavuse eeltingimused

Enne Varude nähtavuse installimist peate tegema järgmist.

- Hankige LCS-i juurutamise projekt, millel on vähemalt üks juurutatud keskkond.
- Kontrollige, et lisandmoodulite seadistamise eeltingimused on täidetud. Eeltingimuste kohta lisateabe saamiseks vaadake teema [Lisandmoodulite ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Varude nähtavus ei nõua topeltkirjutuse linkimist.

> [!NOTE]
> Praegu toetatavad riigid ja regioonid hõlmavad Kanadat (CCA, ECA), USA-d (WUS, EUS), Euroopa Liitu (NEU, WEU), Suurbritanniat (SUK, WUK), Austraaliat (EAU, SEAU), Jaapanit (EJP, WJP), ja Brasiiliat (SBR, SCUS).

Kui teil on küsimusi nende eeltingimuste kohta, võtke ühendust varude nähtavuse tootemeeskonnaga siin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Varude nähtavuse lisandmooduli installimine

Enne lisandmooduli installimist registreerige rakendus ja lisage kliendi saladus kataloogi Azure Active Directory (Azure AD) oma Azure tellimuse alla. Juhised leiate jaotistest [Rakenduse registreerimine](/azure/active-directory/develop/quickstart-register-app) ja [Kliendi saladuse lisamine](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Märkige väärtused **Rakenduse (kliendi) ID**, **Kliendi saladus** ja **Rentniku ID** üles, sest neid läheb hiljem vaja.

Pärast rakenduse registreerimist ja Azure AD kliendi saladuse lisamist, järgige neid samme varude nähtavuse lisandmooduli installimiseks.

1. Logige teenusesse [LCS](https://lcs.dynamics.com/Logon/Index) sisse.
1. Avalehel valige projekt, kus teie keskkond juurutati.
1. Projekti lehel valige keskkond, kuhu soovite lisandmooduli installida.
1. Kerige keskkonna lehel alla, kuni leiate jaotise **Keskkonna lisandmoodulid**, mis asub jaotises **Power Platformi integratsioon**. Siit leiate Dataverse'i keskkonna nime. Veenduge, et Dataverse keskkonna nimi oleks see, mida soovite varude nähtavuse jaoks kasutada.

    > [!NOTE]
    > Praegu toetatakse ainult LCS abil loodud Dataverse'i keskkondi. Kui teie Dataverse'i keskkond loodi mõnel muul viisil (näiteks Power Apps halduskeskuse abil) ja kui see on seotud teie rakenduse Supply Chain Management keskkonnaga, peate esmalt vastendamise probleemi lahendamiseks kontakteeruma varude nähtavuse tootemeeskonnaga siin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Seejärel saate Varude nähtavuse installida.

1. Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.

    ![LCS-i keskkonna leht](media/inventory-visibility-environment.png "LCS-i keskkonna leht")

1. Valige link **Installi uus lisandmoodul**. Ilmub saadaolevate lisandmoodulite loend.
1. Valige loendist **Varude nähtavus**.
1. Määrake oma keskkonnale järgmised väljad.

    - **AAD rakenduse (kliendi) ID** – sisestage varem loodud ja üles märgitud Azure AD rakenduse ID.
    - **AAD rentniku ID** – sisestage varem üles märgitud rentniku ID.

    ![Lisandmooduli lehe seadistamine](media/inventory-visibility-setup.png "Lisandmooduli lehe seadistamine")

1. Nõustuge tingimustega, valides märkeruudu **Tingimused**.
1. Valige **Installi**. Lisandmooduli olek kuvatakse kui **Installimine**. Kui installimine on lõpule viidud, värskendage lehte. Uueks olekuks peaks muutuma **Installitud**.
1. Valige Dataverse vasakpoolsel navigeerimisel jaotis **Rakendused** ja veenduge, et **Varude nähtavus** Power Apps on edukalt installitud. Kui jaotist **Rakendused** pole olemas, võtke ühendust varude nähtavuse tootetiimiga siin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!IMPORTANT]
> Kui teil on rohkem kui üks LCS keskkond, looge igale Azure AD keskkonnale erinev rakendus. Kui kasutate sama rakenduse ID-d ja rentniku ID-d varude nähtavuse lisandmooduli installimiseks erinevates keskkondades, ilmneb loa probleem vanemates keskkondades. Kehtib ainult viimane installitud versioon.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Varude nähtavuse lisandmooduli desinstallimine

Varude nähtavuse lisandmooduli eemaldamiseks valige LCS-i lehel **Desinstalli**. Desinstallimisprotsess eemaldab varude nähtavuse lisandmooduli, tühistab lisandmooduli registreeringu LCS-t ja kustutab kõik ajutised andmed, mis on salvestatud Varude nähtavuse lisandmooduli andmete vahemällu. Siiski ei kustutata esmaseid varude andmeid, mis on salvestatud teie Dataverse'i tellimusse.

Dataverse'i tellimusse salvestatud varude andmete desinstallimiseks avage [Power Apps](https://make.powerapps.com), valige navigeerimisribal **Keskkond** ja valige see Dataverse'i keskkond, mis on seotud teie LCS-i keskkonnaga. Seejärel avage **Lahendused** ja kustutage järgmised viis lahendust selles järjekorras:

1. Varude nähtavuse rakenduse ankurlahendus Dynamics 365 lahendustes
1. Dynamics 365 FNO SCM-i Varude nähtavuse rakenduste lahendus
1. Laoteenuse konfiguratsioon
1. Eraldiseisev Varude nähtavus
1. Dynamics 365 FNO SCM-i Varude nähtavuse põhilahendus

Pärast nende lahenduste kustutamist kustutatakse ka tabelites talletatud andmed.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Saate häälestada Inventory Visibility rakenduses Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Juuruta varude nähtavuse integreerimispakett

Kui käitate teenuse Supply Chain Management versiooni 10.0.17 või varasemat, võtke ühendust varude nähtavuse tugimeeskonnaga [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) paketifaili saamiseks. Seejärel juurutage pakett LCS-i.

> [!NOTE]
> Kui juurutamisel ilmneb versiooni lahknevuse tõrge, peate käsitsi importima X++ projekti oma arenduskeskkonda. Seejärel looge juurutatav pakett oma arenduskeskkonnas ja juurutage see oma tootmiskeskkonnas.
>
> Kood sisaldub teenuse Supply Chain Management versioonis 10.0.18. Kui käitate seda või hilisemat versiooni, pole juurutamine vajalik.

Veenduge, et järgmised funktsioonid on sisse lülitatud teenuse Supply Chain Management keskkonnas. (Vaikimisi on need sisse lülitatud.)

| Funktsiooni kirjeldus | Koodi versioon | Ümberlülituse klass |
|---|---|---|
| Varude dimensioonide kasutamise lubamine või keelamine InventSum tabelis      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Varude dimensioonide kasutamise lubamine või keelamine InventSumDelta tabelis | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Inventory Visibility integratsiooni seadistamine

Kui olete lisandmooduli installinud, valmistage Supply Chain Management süsteem ette järgmiste sammude abil tööks.

1. Rakenduses Supply Chain Management avage **[funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruum ja lülitage sisse järgmised funktsioonid:
    - *Inventory Visibility integratsioon* - Nõutud.
    - *Inventory Visibility integreerimine reserveerimise vastaskontoga* – soovitatav, kuid valikuline. Nõuab versiooni 10.0.22 või uuemat. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md).

1. Avage **Varude haldus \> Seadistus \> Inventory Visibility integratsiooni parameetrid**.
1. Avage vahekaart **Üldine** ja tehke järgmised sätted:
    - **Inventory Visibility lõpp-punkt** – sisestage keskkonna URL, kus käitatakse varude nähtavust. Lisateavet vt jaotisest [Teenuse lõpp-punkti leidmine](inventory-visibility-configuration.md#get-service-endpoint).
    - **Kirjete maksimaalne arv ühes taotluses** - määrake kirjete maksimaalne arv, mida ühte taotlusse kaasata. Sisestage positiivne täisarv, mis on väiksem kui 1000 või sellega võrdne. Vaikeväärtus on 512. Soovitame säilitada vaikeväärtuse, kui te pole Microsoft`i toelt soovitust saanud või olete muidu kindel, et peate seda muutma.

1. Kui valitav varude nähtavuse *integratsioon reserveerimise vastasfunktsiooniga* lubatud, avage vahekaart **Reserveerimise vastaskonto** ja tehke järgmised sätted:
    - **Luba reserveerimise vastaskonto** – selle funktsiooni lubamiseks määrake väärtuseks *Jah*.
    - **Reserveerimise vastaskonto** - Valige laokande olek, mis tasakaalustab varude nähtavuse tehtud reserveerimised. See säte määrab tellimuse töötlemise etapi, mis käivitab vastaskontod. Etappi jälgitakse tellimuse laokande oleku alusel. Valige üks järgmistest:
        - *Tellimusel* – oleku *Kandel* korral saadab tellimus loomisel vastaskonto taotluse. Vastaskogus on loodud tellimuse kogus.
        - *Reserv* – Oleku *Reservi tellimise kanne* korral saadab tellimus vastaskonto taotluse, kui see on reserveeritud, komplekteeritud, saatelehtedega sisestatud või arveldatud. Taotlus käivitatakse ainult üks kord esimese sammu korral, kui nimetatud protsess aset leiab. Vastaskogus on kogus, mille puhul laokande olek on vastaval tellimusereal muudetud olekuks *Tellitud* või *Tellimusel reserveeritud* (või hilisem olek).

1. Minge **Varude halduse \> Perioodiline \> Varude nähtavuse integratsioon** ja lubage töö. Kõik varude muutmise sündmused teenusest Supply Chain Management sisestatakse nüüd Varude nähtavusse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
