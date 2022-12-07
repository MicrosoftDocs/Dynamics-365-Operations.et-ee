---
title: Rakendus Human Resources Teamsis
description: See artikkel tutvustab Microsoft Dynamics 365 Human Resources rakendust Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d29802bdf3411c93f20d710e1f26e541e5022d57
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812182"
---
# <a name="human-resources-app-in-teams"></a>Rakendus Human Resources Teamsis


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsofti rakendus Dynamics 365 Human Resources lubab Microsoft Teams töötajatel kiiresti taotleda aega ja vaadata oma mittesaldoteavet Microsoft Teams. Teabe taotlemiseks saavad töövõtjad suhelda robotiga. Vahekaart **Vaba aeg** annab üksikasjalikumat teavet. Lisaks saavad nad saata inimestele teavet eelseisva eemaloleku kohta töörühmades ja vestlustes väljaspool rakendust Human Resources.

![Human Resources Teams`i puhkuste rakenduse robot.](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams`i puhkuse rakenduse vaba aja vahekaart.](./media/hr-teams-leave-app-timeoff-tab.png)

![Rakenduse Human Resources puhkusetaotluse kaart.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installimine ja häälestus

Rakenduse Dynamics 365 Human Resources leiate Teamsi poest. Lisateabe saamiseks Teamsi rakenduse installimise kohta, vaadake teemat [Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md).

Lisateabe saamiseks rakenduse lubade haldamise kohta Teamsis, vaadake teemat [Rakenduse lubade poliitikate haldamine Microsoft Teamsis](/MicrosoftTeams/teams-app-permission-policies).

Kui soovite, et kasutajad saaksid rakenduses vaadata puhkuste ja puudumise kalendrit, peate sätte **Puhkuste ja puudumiste kalender Teamsis** funktsioonihalduse kaudu lubama. Lisateavet funktsioonide lubamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

## <a name="update-app"></a>Uuenda rakendust
>[!NOTE]
> Alates 20. detsembrist 2021, on Microsofti rentnikus majutatud Inimressursside rakenduse ressursiteenused kasutuselt kõrvaldatud. Installiks saadaolevale ajapikendusle (versiooniversioonile 1.1.5) mõju ei ole. Põhimõju on aegunud laiendile (versiooni 1.1.4). Selle versiooni vestlus lõpetab töötamise. Vahekaart **Aja väljalülitamine** jätkab tööd mõlemas laiendis.

Versiooni 1.1.4 puhul lõpetab vestlus sõnumi vastamise. Näiteks sisse logimine, saldode **vaade** ja **aja lõppaeg**. **·** Rakendus tuleb käsitsi värskendada uusimale versioonile. Lisateavet vt jaotisest Rakenduste [värskendamine. Microsoft Teams](/MicrosoftTeams/apps-update-experience)

Versioonile 1.1.5 uuendamiseks läbige järgmised sammud:
1. Sisse Microsoft Teams, minge **rakendustesse**.
2. Saate otsida **inimressursside rakenduse** .
3. Valige **täiendus**.

Inimressursside rakenduse versiooni saate kontrollida, kas minna vahekaardile **Teave**  **või minna jaotisse Isiklik** rakendus. 

![Vahekaart Inimressursid **Teave**](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Teatiste lubamine rakenduse Human Resources jaoks Teamsis

Kui soovite, et kasutajad saaksid puhkusetaotluse teatisi Teamsis vastu võtta, peate lubama teatised rakenduses Dynamics 365 Human Resources.

>[!NOTE]
>Teatisi saavad ainult need kasutajad, kes on Teamsis sisse logitud ja kasutavad Teamsis rakendust Dynamics 365 Human Resources.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige **Lingid**.

3. Tehke jaotises **Seadistamine** valik **Süsteemi parameetrid**.

4. Seadke vahekaardil **Üldine** seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**.

   ![Teamsi rakenduse teatiste lubamine süsteemi parameetrites.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Kõigi kasutajate jaoks Teamsi teatiste sisselülitamiseks valige **Jah**.

   ![Teams`i teatiste lubamine kõigi kasutajate jaoks.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine

Kui olete lubanud Teamsis rakenduse Dynamics 365 Human Resources teatised, saate teatised üksikute kasutajate jaoks sisse või välja lülitada.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige **Lingid**.

3. Tehke jaotises **Kasutajad** valik **Kasutaja valikud**.

4. Valige vahekaart **Töövoog**.

5. Määrake seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**, et lubada kasutajate jaoks teatiste kuvamine, või **Ei**, et keelata kasutajale teatiste kuvamine.

   ![Teams`i rakenduse teatiste lubamine kasutaja suvandite vahekaardil Töövoog.](./media/hr-admin-teams-leave-app-notifications.png)

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
| tr-TR | Türgi (Jadžik) |
| zh-CN | Hiina (lihtsustatud) |

## <a name="notes"></a>Märkmed

Järgmised tööüksused on kavas välja anda tulevastes väljalasetes:

| Tööüksus | Olek |
| --- | --- |
| Tulevaks kuupäevaks vaba aja taotlemisel on vale saldo. | Prognoosimine pole veel saadaval. Kuvatakse praeguse kuupäeva saldo. |
| Taotlust **Läbivaatamisel** ei saa tühistada. | See funktsioon ei ole praegu toetatud ja lisatakse tulevasse väljalaskesse. |
| Saldo teavet arvutatakse alates tänasest. | Süsteem ei näita praegu viitvõlaperioodi seisuga saldosid, isegi kui see on **konfigureeritud puhkuse ja puudumise parameetrite** lehel. |

## <a name="troubleshooting"></a>Tõrkeotsing

Kui kasutajal on probleeme Human Resources Teamsi rakendusse sisselogimisega või selle kasutamisega, proovige neid tõrkeotsingujuhiseid järgida. Kui teil on pärast tõrkeotsingut endiselt probleeme, siis võtke ühendust tugiteenusega. Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Veenduge, et töörühmade inimressursside rakendus on ajasõbralik.
Kui teil tekib probleeme Teamsi inimressursside rakendusega, peate kinnitama, et kasutate uusimat versiooni. Minimaalne toetatud versioon on 1.1.5. Juhendite saamiseks teamsi rakenduse uuendamise kohta vt töörühmade [dokumentatsiooni](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ma ei saa Teamsis rakendusse Human Resources sisse logida

Kui kasutaja võtab teiega ühendust, kuna ta ei saa rakendusse sisse logida, veenduge, et tal oleks rakenduses Human Resources seotud töötajakirje.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Tõrge puhkusetaotluste kinnitamise korral Teamsis rakenduses Human Resources

Kui kasutaja saab vea, kui ta proovib kinnitada puhkuse taotlusi Teamsi rakenduses, proovige järgmisi tõrkeotsingu samme:

1. Veenduge, et tema Teamsi konto oleks sama, mida ta kasutab rakendusele Human Resources juurdepääsemiseks.

2. Kontrollige, et ta oleks taotluse puhul sobiv kinnitaja, kontrollides puhkuse kinnitamise töövoo sätteid. Lisateavet puhkusetaotluse töövoogude kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Jäta kinnitajad ilma Teamsi vestluseteadete saamisest, mille eesmärgiks on puhkusetaotluste kinnitamine

1. Veenduge, et teatised on keskkonna ja kasutaja jaoks lubatud. Lisateabe saamiseks vaadake jaotist [Luba rakenduse Human Resources teavitused Teamsis](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ja [Teamsi teavituste sisse- või väljalülitamine individuaalsete kasutajate puhul](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Veenduge, et kasutajad on vahekaardile **Vestlus** sisse logitud samade mandaatidega, mida nad puhkuse taotluste kinnitamiseks kasutavad. Kasutage sõnumeid "väljalogimine" ja seejärel "sisselogimine" õigete mandaatidega sisse logimiseks.

3. Kui probleem ei lahene, kontrollige ärisündmuste **süsteemi** pakett-töö olekut süsteemiadministraatorina. Kui see on etapis Ootamine **või** **Teostamine**, kontrollige mõne minuti pärast uuesti. Kui olek jääb muutmata, logige tugipilet, et meie meeskond saaks probleemi lahendada.

## <a name="privacy-notice"></a>Privaatsusavaldus

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Kasutaja tekstisisestuse Dynamics 365 Human Resources  Microsoft Teams abil analüüsitakse aluseks olevat päringut/eesmärki mõista. Kasutajasisend, nt Otsingukonto Contoso, suunatakse ühte Microsofti kokuptiivne teenusest Language Understanding Nutikas Teenus (SOFT). Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/). Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso). See teave edastatakse siis [Microsoft'sAzure'i](https://azure.microsoft.com/services/bot-service/) raamistikule, Dynamics 365 Human Resources mis suhtleb andmetega ja toob kasutajapäringu jaoks soovitud teabe.

Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus. Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase. Kui AJATEENUSEl Dynamics 365 Human Resources on juurdepääs ainult kasutajapäringutele ja see ei ole loodud ühenduseks kasutaja andmete või kontoga, Dynamics 365 Human Resources võib osa kasutaja ise sisestada kliendiandmeid, isikuandmeid või muid andmeid ja sellist päringu sisu sisaldava päringu, mille saab saataKOOSTE teenusesse ja Azure azure’i raamistikusse. 

Kasutaja päringute ja teadete sisu säilitatakse KRÜPTO süsteemi maksimaalselt 30 päevaks, krüptitakse ülejäänud ajal ja seda ei kasutata koolitusel või teenuse täiustamisel. Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid ja Azure Cosmos DB

Rakenduse kasutamisel võivad Dynamics 365 Human Resources teatud kliendiandmed Microsoft Teams voogu väljapoole geograafilises piirkonnas, kus teie rentniku Inimressursid teenus juurutatakse.

Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad sündmuste tabelisse Microsoft Azure ja Microsoft Teams. Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams. Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Vt ka 

[Microsoft Teamsi allalaadimine ja installimine](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams spikrikeskus](https://support.office.com/teams)</br>
[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
