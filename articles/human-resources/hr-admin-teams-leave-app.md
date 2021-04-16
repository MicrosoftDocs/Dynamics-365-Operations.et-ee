---
title: Rakendus Human Resources Teamsis
description: Selles teemas tutvustatakse Microsoft Teamsi rakendust Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b44cee0574794ae4b3cfd1987934aa4933b46b2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803989"
---
# <a name="human-resources-app-in-teams"></a>Rakendus Human Resources Teamsis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teamsi rakendus Microsoft Dynamics 365 Human Resources võimaldab töövõtjatel kiirelt esitada vaba aja taotlust ja kuvada vaba aja saldo teavet otse Microsoft Teamsis. Teabe taotlemiseks saavad töövõtjad suhelda robotiga. Vahekaart **Vaba aeg** annab üksikasjalikumat teavet. Lisaks saavad nad saata inimestele teavet eelseisva eemaloleku kohta töörühmades ja vestlustes väljaspool rakendust Human Resources.

![Human Resources Teamsi puhkuste rakenduse robot](./media/hr-teams-leave-app-bot.png)

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)

![Rakenduse Human Resources puhkusetaotluse kaart](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installimine ja häälestus

Rakenduse Dynamics 365 Human Resources leiate Teamsi poest. Lisateabe saamiseks Teamsi rakenduse installimise kohta, vaadake teemat [Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md).

Lisateabe saamiseks rakenduse lubade haldamise kohta Teamsis, vaadake teemat [Rakenduse lubade poliitikate haldamine Microsoft Teamsis](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

Kui soovite, et kasutajad saaksid rakenduses vaadata puhkuste ja puudumise kalendrit, peate sätte **Puhkuste ja puudumiste kalender Teamsis** funktsioonihalduse kaudu lubama. Lisateavet funktsioonide lubamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Teatiste lubamine rakenduse Human Resources jaoks Teamsis

Kui soovite, et kasutajad saaksid puhkusetaotluse teatisi Teamsis vastu võtta, peate lubama teatised rakenduses Dynamics 365 Human Resources.

>[!NOTE]
>Teatisi saavad ainult need kasutajad, kes on Teamsis sisse logitud ja kasutavad Teamsis rakendust Dynamics 365 Human Resources.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige **Lingid**.

3. Tehke jaotises **Seadistamine** valik **Süsteemi parameetrid**.

4. Seadke vahekaardil **Üldine** seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**.

   ![Teamsi rakenduse teatiste lubamine süsteemi parameetrites](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Kõigi kasutajate jaoks Teamsi teatiste sisselülitamiseks valige **Jah**.

   ![Teamsi teatiste lubamine kõigi kasutajate jaoks](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine

Kui olete lubanud Teamsis rakenduse Dynamics 365 Human Resources teatised, saate teatised üksikute kasutajate jaoks sisse või välja lülitada.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige **Lingid**.

3. Tehke jaotises **Kasutajad** valik **Kasutaja valikud**.

4. Valige vahekaart **Töövoog**.

5. Määrake seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**, et lubada kasutajate jaoks teatiste kuvamine, või **Ei**, et keelata kasutajale teatiste kuvamine.

   ![Teamsi rakenduse teatiste lubamine kasutaja suvandite vahekaardil Töövoog](./media/hr-admin-teams-leave-app-notifications.png)

6. Valige käsk **Salvesta**.

## <a name="supported-languages"></a>Toetatud keeled

Teamsi rakendus Dynamics 365 Human Resources toetab järgmisi keeli:

| Lokaadi ID | Keel |
| --- | --- |
| de-DE | saksa (Saksamaa) |
| es-ES | hispaania (Hispaania) |
| es-MX | Hispaania (Mehhiko) |
| fr-CA | Prantsuse (Kanada) |
| fr-FR | prantsuse (Prantsusmaa) |
| it-IT | itaalia (Itaalia) |
| nl-NL | hollandi (Holland) |
| pt-BR | portugali (Brasiilia) |
| tr-TR | türgi (Türgi) |
| zh-CN | Hiina (lihtsustatud) |

## <a name="notes"></a>Märkmed

Järgmised tööüksused on kavas välja anda tulevastes väljalasetes:

| Tööüksus | Olek |
| --- | --- |
| Tulevaks kuupäevaks vaba aja taotlemisel on vale saldo. | Prognoosimine pole veel saadaval. Kuvatakse praeguse kuupäeva saldo. |
| Taotlust **Läbivaatamisel** ei saa tühistada. | See funktsioon ei ole praegu toetatud ja lisatakse tulevasse väljalaskesse. |
| Saldo teavet arvutatakse alates tänasest. | Süsteem ei kuva praegu puhkuseperioodi seisuga saldosid, isegi kui see on konfigureeritud puhkuste ja puudumiste parameetrites. |

## <a name="troubleshooting"></a>Tõrkeotsing

Kui kasutajal on probleeme Human Resources Teamsi rakendusse sisselogimisega või selle kasutamisega, proovige neid tõrkeotsingujuhiseid järgida. Kui teil on pärast tõrkeotsingut endiselt probleeme, siis võtke ühendust tugiteenusega. Lisateavet leiate teemast [Toe hankimine](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ma ei saa Teamsis rakendusse Human Resources sisse logida

Kui kasutaja võtab teiega ühendust, kuna ta ei saa rakendusse sisse logida, veenduge, et tal oleks rakenduses Human Resources seotud töötajakirje.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Tõrge puhkusetaotluste kinnitamise korral Teamsis rakenduses Human Resources

Kui kasutaja saab Teamsi rakenduses puhkusetaotluste kinnitamise katsel tõrke, proovige järgmisi tõrkeotsingutoiminguid.

1. Veenduge, et tema Teamsi konto oleks sama, mida ta kasutab rakendusele Human Resources juurdepääsemiseks.

2. Kontrollige, et ta oleks taotluse puhul sobiv kinnitaja, kontrollides puhkuse kinnitamise töövoo sätteid. Lisateavet puhkusetaotluse töövoogude kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).

## <a name="privacy-notice"></a>Privaatsusavaldus

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki. Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS). Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/). Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso). Seejärel edastatakse see teave Microsofti  [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/), mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe. 

Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus. Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase. Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku. 

Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks. Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid ja Azure Cosmos DB

Rakenduse Dynamics 365 Human Resources kasutamisel rakenduses Microsoft Teams võivad mõned kliendiandmed liikuda väljapoole geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud.

Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad Microsoft Azure Event Gridi ja Microsoft Teamsi. Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams. Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Vt ka 

[Microsoft Teamsi allalaadimine ja installimine](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams spikrikeskus](https://support.office.com/teams)</br>
[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]