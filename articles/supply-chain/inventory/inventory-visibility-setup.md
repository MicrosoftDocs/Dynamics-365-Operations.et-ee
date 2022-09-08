---
title: Varude nähtavuse lisandmooduli installimine
description: See artikkel kirjeldab, kuidas installida Microsofti varude nähtavuse lisandmoodul Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: eb17f24b90933dac0f875bb0ef2d5039a240b197
ms.sourcegitcommit: 1ca4ad100f868d518f3634dca445c9878962108e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2022
ms.locfileid: "9388536"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility installimine ja häälestamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas installida Microsofti varude nähtavuse lisandmoodul Dynamics 365 Supply Chain Management.

Varude nähtavuse lisandmooduli installimiseks peate kasutama teenust Microsoft Dynamics Lifecycle Services (LCS). LCS on koostööportaal, mis pakub keskkonda ja regulaarselt värskendatud teenuseid, mis aitavad hallata finants- ja tegevusrakenduste elutsüklit. Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Soovitame teil liituda varude nähtavuse lisandmooduli kasutajagrupiga, kus saate otsida kasulikke juhendeid, saada meie uusimaid uuendusi ja sisestada mis tahes küsimused, mis võivad olla seotud varude nähtavuse kasutamisega. Liitumiseks saatke laos varude nähtavuse tootemeeskonnale e-kiri [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) lisage oma tarneahela halduse keskkonna ID.

## <a name="inventory-visibility-prerequisites"></a>Varude nähtavuse eeltingimused

Enne Varude nähtavuse installimist peate tegema järgmist.

- Hankige LCS-i juurutamise projekt, millel on vähemalt üks juurutatud keskkond.
- Kontrollige, et lisandmoodulite seadistamise eeltingimused on täidetud. Eeltingimuste kohta lisateabe saamiseks vaadake teema [Lisandmoodulite ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Varude nähtavus ei nõua topeltkirjutuse linkimist.

> [!NOTE]
> Praegu toetatavad riigid ja regioonid hõlmavad Kanadat (CCA, ECA), USA-d (WUS, EUS), Euroopa Liitu (NEU, WEU), Suurbritanniat (SUK, WUK), Austraaliat (EAU, SEAU), Jaapanit (EJP, WJP), ja Brasiiliat (SBR, SCUS).

Kui teil on küsimusi nende eeltingimuste kohta, võtke ühendust varude nähtavuse tootemeeskonnaga siin [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Varude nähtavuse lisandmooduli installimine

Enne lisandmooduli installimist registreerige rakendus ja lisage kliendi saladus kataloogi Azure Active Directory (Azure AD) oma Azure tellimuse alla. Juhised leiate jaotistest [Rakenduse registreerimine](/azure/active-directory/develop/quickstart-register-app) ja [Kliendi saladuse lisamine](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Tehke kindlasti märge rakenduse **(kliendi) ID**, **·** **kliendi saladuse ja rentnike ID** väärtuste kohta, sest vajate neid hiljem.

> [!IMPORTANT]
> Kui teil on rohkem kui üks LCS keskkond, looge igaühel Azure AD neist erinev rakendus. Kui kasutate sama rakenduse ID-d ja rentniku ID-d varude nähtavuse lisandmooduli installimiseks erinevates keskkondades, ilmneb loa probleem vanemates keskkondades. Seetõttu kehtib ainult viimane install.

Pärast rakenduse registreerimist ja Azure AD kliendi saladuse lisamist, järgige neid samme varude nähtavuse lisandmooduli installimiseks.

1. Logige teenusesse [LCS](https://lcs.dynamics.com/Logon/Index) sisse.
1. Avalehel valige projekt, kus teie keskkond juurutati.
1. Projekti lehel valige keskkond, kuhu soovite lisandmooduli installida.
1. Kerige keskkonna lehel alla, kuni leiate jaotise **Keskkonna lisandmoodulid**, mis asub jaotises **Power Platformi integratsioon**. Siit leiate Dataverse'i keskkonna nime. Veenduge, et Dataverse keskkonna nimi oleks see, mida soovite varude nähtavuse jaoks kasutada.

    > [!NOTE]
    > Praegu toetatakse ainult LCS abil loodud Dataverse'i keskkondi. Kui teie Dataverse keskkond loodi mõnel muul viisil (PowerApps nt halduskeskuse abil) ja kui see on seotud teie tarneahela halduskeskkonnaga, peate vastendamise probleemi enne varude nähtavuse lisandmooduli installimist lahendama.
    >
    > Võimalik, et teie topeltkirjutuskeskkond on ühendatud eksemplariga Dataverse, kui LCS ei ole häälestatud integreerimiseks Power Platform. Selline seostatav lahknevus võib põhjustada ootamatut käitumist. Soovitame LCS-i keskkonna üksikasjad ühtima sellega, millega olete topeltkirjutuses ühendatud, et sama ühendust saaks kasutada ärisündmustes, virtuaaltabelites ja lisandmoodulites. Vt [vastendamise probleemi lahendamise](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) kohta lisateavet seostamise lahknevuse kohta. Kui vastendamisprobleem on lahendatud, saate jätkata varude nähtavuse installimist.

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

> [!NOTE]
> Kui LCS-lehelt installimiseks kulub rohkem kui tund, puudub teie kasutajakontol tõenäoliselt õigus keskkonnas lahendusi installida Dataverse. Probleemi lahendamiseks järgige neid samme:
>
> 1. Tühistage varude nähtavuse lisandmooduli installiprotsess LCS-i lehelt.
> 1. Logige halduskeskusesse [Microsoft 365 sisse](https://admin.microsoft.com)Dynamics 365 Unified Operations ja veenduge, et kasutajakontol, mida soovite kasutada lisandmooduli installimiseks, oleks määratud "Plaan" litsents. Vajadusel määrake litsents.
> 1. Logige vastava kasutajakonto [Power Platform abil halduskeskusesse](https://admin.powerplatform.microsoft.com) sisse. Seejärel installige lao nähtavuse lisandmoodul järgmiste sammude abil:
>     1. Valige keskkond, kuhu soovite lisandmooduli installida.
>     1. Valige **Dynamics 365 rakendused**.
>     1. Valige **installirakendus**.
>     1. Varude **nähtavuse valimine**
>
> 1. Pärast installi lõpule viimist minge tagasi LCS-lehele ja proovige varude **nähtavuse** lisandmoodul uuesti installida.

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

Kui olete lisandmooduli installinud, valmistage tarneahela haldussüsteem ette järgmiste sammude abil tööks.

1. Rakenduses Supply Chain Management avage **[funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruum ja lülitage sisse järgmised funktsioonid:
    - *Inventory Visibility integratsioon* - Nõutud.
    - *Inventory Visibility integreerimine reserveerimise vastaskontoga* – soovitatav, kuid valikuline. Nõuab versiooni 10.0.22 või uuemat. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md).

1. Avage **Varude haldus \> Seadistus \> Inventory Visibility integratsiooni parameetrid**.
1. Avage vahekaart **Üldine** ja tehke järgmised sätted:
    - **Inventory Visibility lõpp-punkt** – sisestage keskkonna URL, kus käitatakse varude nähtavust. Lisateavet vt jaotisest [Teenuse lõpp-punkti leidmine](inventory-visibility-configuration.md#get-service-endpoint).
    - **Kirjete maksimaalne arv ühes taotluses** - määrake kirjete maksimaalne arv, mida ühte taotlusse kaasata. Sisestage positiivne täisarv, mis on väiksem kui 1000 või sellega võrdne. Vaikeväärtus on 512. Soovitame säilitada vaikeväärtuse, kui te pole Microsoft`i toelt soovitust saanud või olete muidu kindel, et peate seda muutma.

1. Kui valitav varude nähtavuse *integratsioon reserveerimise vastasfunktsiooniga* lubatud, avage vahekaart **Reserveerimise vastaskonto** ja tehke järgmised sätted:
    - **Luba reserveerimise vastaskonto** – selle funktsiooni lubamiseks määrake väärtuseks *Jah*.
    - **Reserveerimise vastaskonto** - Valige laokande olek, mis tasakaalustab varude nähtavuse tehtud reserveerimised. See säte määrab tellimuse töötlemise etapi, mis käivitab vastaskontod. Etappi jälgitakse tellimuse laokande oleku alusel. Valige üks järgmistest valikutest:
        - *Tellimusel* – oleku *Kandel* korral saadab tellimus loomisel vastaskonto taotluse. Vastaskogus on loodud tellimuse kogus.
        - *Reserv* – Oleku *Reservi tellimise kanne* korral saadab tellimus vastaskonto taotluse, kui see on reserveeritud, komplekteeritud, saatelehtedega sisestatud või arveldatud. Taotlus käivitatakse ainult üks kord esimese sammu korral, kui nimetatud protsess aset leiab. Vastaskogus on kogus, mille puhul laokande olek on vastaval tellimusereal muudetud olekuks *Tellitud* või *Tellimusel reserveeritud* (või hilisem olek).

1. Minge **Varude halduse \> Perioodiline \> Varude nähtavuse integratsioon** ja lubage töö. Kõik varude muutmise sündmused teenusest Supply Chain Management sisestatakse nüüd Varude nähtavusse.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Varude nähtavuse lisandmooduli desinstallimine

Varude nähtavuse lisandmooduli desinstallimiseks järgige neid samme.

1. Logige sisse rakendusse Supply Chain Management.
1. Minge varude **halduse perioodilise \> varude nähtavuse \> integratsiooni ja** keelake töö.
1. Minge LCS-i ja avage leht keskkonnas, kus soovite lisandmooduli desinstallida (vt ka [varude nähtavuse lisandmooduli installimine](#install-add-in)).
1. Valige **desinstallimine**.
1. Desinstallimisprotsess lõpetab nüüd varude nähtavuse lisandmooduli, tühistab lisandmooduli registreerimise LCS-ist ja kustutab kõik ajutised andmed, mis on talletatud varude nähtavuse lisandmooduli andmevahemällu. Kuid esmased varude andmed, mis sünkrooniti teie kordustellimusega Dataverse, on endiselt seal. Andmete kustutamiseks viige ülejäänud protseduur lõpule.
1. Avage [Power Apps](https://make.powerapps.com).
1. Valige **navigeerimisribal** keskkond.
1. Valige keskkond Dataverse, mis on seotud teie LCS-keskkonnaga.
1. Minge lahendustesse **ja** kustutage järgmised lahendused järgmises järjekorras:
    1. Dynamics 365 varude nähtavus – ankur
    1. Dynamics 365 varude nähtavus – rakendus
    1. Dynamics 365 varude nähtavus – juhtelemendid
    1. Dynamics 365 varude nähtavus – Outlooki
    1. Dynamics 365 varude nähtavus – alus

    Pärast nende lahenduste kustutamist kustutatakse ka tabelites talletatud andmed.

> [!NOTE]
> Kui taastate tarneahela halduse andmebaasi pärast varude nähtavuse lisandmooduli desinstallimist ja soovite lisandmooduli uuesti installida, siis veenduge, et kustutate enne lisandmooduli uuesti installimist vana varude nähtavuse andmed, Dataverse mis on talletatud teie kordustellimuses (nagu kirjeldatud eelmises protseduuris). See takistab andmete vastuolud, mis võivad ilmneda.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a> Puhas varude nähtavuse andmed Dataverse enne hankeahela halduse andmebaasi taastamist

Kui olete kasutanud varude nähtavust ja seejärel taastanud tarneahela halduse andmebaasi, võib teie taastatud andmebaas sisaldada andmeid, mis ei ole enam kooskõlas eelnevalt varude nähtavuse kaudu eelnevalt sünkroonitud andmetega Dataverse. Nende andmete vastuolud võivad põhjustada süsteemitõrkeid ja muid probleeme. Seetõttu on oluline enne tarneahela Dataverse halduse andmebaasi taastamist alati puhastada kõik varude nähtavuse andmed.

Kui teil on vaja taastada tarneahela halduse andmebaas, kasutage järgmist protseduuri:

1. Desinstallige varude nähtavuse lisandmoodul ja eemaldage kõik seotud andmed Dataverse, nagu on kirjeldatud [jaotises Varude nähtavuse lisandmooduli desinstallimine.](#uninstall-add-in)
1. Taastage tarneahela halduse andmebaas, [nt nagu on kirjeldatud andmebaasi ajapunkti taastamises (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md)[või tootmisandmebaasi ajapunkti taastamises sisendkausta keskkonda](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Kui soovite seda siiski kasutada, [...](#install-add-in)[installige see uuesti ja seadistage varude nähtavuse lisandmoodul, nagu on kirjeldatud jaotises Lao nähtavuse lisandmooduli installimine ja lao nähtavuse integreerimise installimine.](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
