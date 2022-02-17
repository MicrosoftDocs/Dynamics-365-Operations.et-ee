---
title: Rakendus Human Resources Teamsis
description: Selles teemas tutvustatakse Microsoft Teamsi rakendust Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ffd6967431227b578e227ee570dbe06c356fb8d6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067047"
---
# <a name="human-resources-app-in-teams"></a>Rakendus Human Resources Teamsis


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsofti Dynamics 365 Human Resources rakendus taotleb Microsoft Teams kiiresti vaba aega ja vaatab oma saldovälise teabe kuvamist rakenduses Microsoft Teams. Teabe taotlemiseks saavad töövõtjad suhelda robotiga. Vahekaart **Vaba aeg** annab üksikasjalikumat teavet. Lisaks saavad nad saata inimestele teavet eelseisva eemaloleku kohta töörühmades ja vestlustes väljaspool rakendust Human Resources.

![Human Resources Teams`i puhkuste rakenduse robot.](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams`i puhkuse rakenduse vaba aja vahekaart.](./media/hr-teams-leave-app-timeoff-tab.png)

![Rakenduse Human Resources puhkusetaotluse kaart.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installimine ja häälestus

Rakenduse Dynamics 365 Human Resources leiate Teamsi poest. Lisateabe saamiseks Teamsi rakenduse installimise kohta, vaadake teemat [Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md).

Lisateabe saamiseks rakenduse lubade haldamise kohta Teamsis, vaadake teemat [Rakenduse lubade poliitikate haldamine Microsoft Teamsis](/MicrosoftTeams/teams-app-permission-policies).

Kui soovite, et kasutajad saaksid rakenduses vaadata puhkuste ja puudumise kalendrit, peate sätte **Puhkuste ja puudumiste kalender Teamsis** funktsioonihalduse kaudu lubama. Lisateavet funktsioonide lubamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

## <a name="update-app"></a>Rakenduse värskendamine
>[!NOTE]
> Alates 20. detsembrist 2021 lõpetatakse Microsofti rentnikus majutatud human resources app bot teenused. Installimiseks saadaval olevat ajakohast laiendust (versioon 1.1.5) ei mõjuta. Peamine mõju on aegunud laiendusele (versioon 1.1.4). Selle versiooni vestlusrobot lakkab töötamast. Vahekaart **Time-off** töötab mõlemas laienduses edasi.

Versiooni 1.1.4 puhul lõpetab vestlusrobot igale sõnumile vastamise. Näiteks sisselogimine **,** **saldode** kuvamine ja **aja mahamineku** kuvamine. Rakendus tuleb käsitsi värskendada uusimale versioonile. Lisateavet vt teemast [Update apps in Microsoft Teams](/MicrosoftTeams/apps-update-experience).

Versioonile 1.1.5 värskendamiseks tehke järgmist.
1. Microsoft Teams Avage rakenduses **Rakendused**.
2. **Leidke rakendus Human Resources**.
3. Valige **Täienda.**

Rakenduse Human Resources versiooni saate kontrollida, minnes vahekaardile **About** või minnes jaotisse **Isiklik**. 

![Vahekaart Inimressursid **About** .](./media/HR-teams-about.png)

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
| tr-TR | türgi (Türgi) |
| zh-CN | Hiina (lihtsustatud) |

## <a name="notes"></a>Märkmed

Järgmised tööüksused on kavas välja anda tulevastes väljalasetes:

| Tööüksus | Olek |
| --- | --- |
| Tulevaks kuupäevaks vaba aja taotlemisel on vale saldo. | Prognoosimine pole veel saadaval. Kuvatakse praeguse kuupäeva saldo. |
| Taotlust **Läbivaatamisel** ei saa tühistada. | See funktsioon ei ole praegu toetatud ja lisatakse tulevasse väljalaskesse. |
| Saldo teavet arvutatakse alates tänasest. | Süsteem ei kuva praegu saldosid tekkeperioodi seisuga, isegi kui see on konfigureeritud **lehel Lahkumise ja puudumise parameetrid**. |

## <a name="troubleshooting"></a>Tõrkeotsing

Kui kasutajal on probleeme Human Resources Teamsi rakendusse sisselogimisega või selle kasutamisega, proovige neid tõrkeotsingujuhiseid järgida. Kui teil on pärast tõrkeotsingut endiselt probleeme, siis võtke ühendust tugiteenusega. Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Veenduge, et Teamsi inimressursside rakendus oleks ajakohane
Kui rakendusega Teams Human Resources tekib probleeme, peate kinnitama, et kasutate uusimat versiooni. Minimaalne toetatud versioon on 1.1.5. Teamsi rakenduse värskendamise juhised leiate [teemast Teamsi dokumentatsioon](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ma ei saa Teamsis rakendusse Human Resources sisse logida

Kui kasutaja võtab teiega ühendust, kuna ta ei saa rakendusse sisse logida, veenduge, et tal oleks rakenduses Human Resources seotud töötajakirje.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Tõrge puhkusetaotluste kinnitamise korral Teamsis rakenduses Human Resources

Kui kasutajal ilmneb Teamsi rakenduses puhkusetaotluste kinnitamise katse ajal tõrge, proovige järgmisi tõrkeotsingujuhiseid.

1. Veenduge, et tema Teamsi konto oleks sama, mida ta kasutab rakendusele Human Resources juurdepääsemiseks.

2. Kontrollige, et ta oleks taotluse puhul sobiv kinnitaja, kontrollides puhkuse kinnitamise töövoo sätteid. Lisateavet puhkusetaotluse töövoogude kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Jäta kinnitajad ilma Teamsi vestluseteadete saamisest, mille eesmärgiks on puhkusetaotluste kinnitamine

1. Veenduge, et teatised on keskkonna ja kasutaja jaoks lubatud. Lisateabe saamiseks vaadake jaotist [Luba rakenduse Human Resources teavitused Teamsis](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ja [Teamsi teavituste sisse- või väljalülitamine individuaalsete kasutajate puhul](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Veenduge, et kasutajad on vahekaardile **Vestlus** sisse logitud samade mandaatidega, mida nad puhkuse taotluste kinnitamiseks kasutavad. Kasutage sõnumeid "väljalogimine" ja seejärel "sisselogimine" õigete mandaatidega sisse logimiseks.

3. Kui probleem püsib, kontrollige pakett-töö Ärisündmuste **süsteemi** süsteemiadministraatorina olekut. Kui see on **ootamise** **või** täitmise etapis, kontrollige mõne minuti pärast uuesti. Kui olek ei muutu, logige sisse tugipilet, et meie meeskond saaks probleemi lahendada.

## <a name="privacy-notice"></a>Privaatsusavaldus

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Dynamics 365 Human Resources Kui bot on rakenduses Microsoft Teams, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/kavatsust. Kasutaja sisend, näiteks "Otsingukonto Contoso", suunatakse ühte Microsofti kognitiivsesse teenusesse, mida nimetatakse keele mõistmise intelligentseks teenuseks (LUIS). Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/). Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso). Seejärel edastatakse see teave MicrosoftiAzure boti [raamistikku](https://azure.microsoft.com/services/bot-service/), mis suhtleb kasutajapäringu andmetega Dynamics 365 Human Resources ja toob soovitud teabe.

Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus. Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase. Kuigi LUIS-teenusel on juurdepääs ainult kasutaja päringutele ja see ei ole mõeldud ühendamiseks kasutaja andmete või kontoga, võib boti Dynamics 365 Human Resources kasutaja Dynamics 365 Human Resources vabatahtlikult sisestada päringu, mis sisaldab kliendiandmeid, isikuandmeid või muid andmeid, ning selline päringu sisu võidakse saata LUIS-teenusele ja Azure boti raamistikku. 

Kasutaja päringute ja sõnumite sisu säilitatakse LUIS-süsteemis maksimaalselt 30 päeva, krüpteeritakse puhkeasendis ja seda ei kasutata koolituseks ega teenuse täiustamiseks. Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid ja Azure Cosmos DB

Rakenduse Dynamics 365 Human Resources kasutamisel Microsoft Teams võivad teatud kliendiandmed liikuda väljapoole geograafilist piirkonda, kus teie rentniku personaliteenus on juurutatud.

Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövooülesande üksikasjad Microsoft Azure sündmuse ruudustikku ja Microsoft Teams. Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams. Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Vt ka 

[Microsoft Teamsi allalaadimine ja installimine](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams spikrikeskus](https://support.office.com/teams)</br>
[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
