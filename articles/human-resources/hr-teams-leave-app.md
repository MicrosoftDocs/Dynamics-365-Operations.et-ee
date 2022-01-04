---
title: Puhkusetaotluste haldamine Teamsis
description: Selles teemas kirjeldatakse, kuidas esitada puhkusetaotlust Microsoft Teamsi rakenduses Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d004e33d01dbd171626d7e23f93df081bc0210a9
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924743"
---
# <a name="manage-leave-requests-in-teams"></a>Puhkusetaotluste haldamine Teamsis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teamsi rakendus Dynamics 365 Human Resources võimaldab teil kiiresti taotleda puhkepäevi ja vaadata vaba aja saldo teavet otse Microsoft Teamsis. Saate suhelda robotiga, et taotleda teavet ja algatada puhkusetaotlus. Vahekaart **Vaba aeg** annab üksikasjalikumat teavet. Lisaks saate inimestele saata teavet eelseisva eemaloleku kohta Teamsis ja vestlustes väljaspool rakendust Human Resources.

## <a name="install-the-app"></a>Rakenduse installimine

Rakenduse Dynamics 365 Human Resources leiate Teamsi poest.

1. Rakenduses Microsoft Teams navigeerige rakenduste loendisse.
 
2. Otsige üles Dynamics 365 Human Resources ja seejärel valige paan **Human Resources**.

> [!NOTE]
> 20.03.2021 algavad Microsofti rentnikus majutatud inimressursside rakenduse 1.1.4 teenused (versioon 1.1.4). Installimiseks on saadaval kõige ajani 1.1.5 (versiooni laiend). Lisateavet vt Töörühmade [puhkusetaotluste haldamine](hr-admin-teams-leave-app.md#update-app).

3. Rakenduse installimiseks valige nupp **Lisa**.

Kui rakendus ei logi teid automaatselt sisse, valige sisselogimiseks vahekaart **Sätted**.

> [!NOTE]
> Kui te ei näe sisselogimisdialoogi, uuendage brauseri sätteid hüpikakende võimaldamiseks. 

Kui teil on juurdepääs rohkem kui ühele Human Resourcesi eksemplarile, saate valida vahekaardil **Sätted** keskkonna, millega soovite ühenduse luua.

> [!NOTE]
> Rakendus toetab nüüd süsteemiadministraatori turberolli.
 
## <a name="use-the-bot"></a>Roboti kasutamine

Pärast rakenduse installimist kuvatakse tervitussõnum, mis teavitab teid tegevuste tüüpidest, mida robot saab teie eest teha.

> [!NOTE]
> Kui te esimest korda süsteemiga suhtlete, peate võibolla sisse logima. Kui te ei näe sisselogimisdialoogi, uuendage brauseri sätteid hüpikakende võimaldamiseks.

Võite paluda robotil teha järgnevat.

- Vaadake oma praegusi puhkuse saldosid. Näiteks saatke teade "Puhkuse saldode vaade."

- Puhkusetaotluse alustamine teie eest. Näiteks saatke teade, kus on kirjas "Vaba aeg" või "Ma soovin võtta puhkuse puhkuse järgmisel neljapäeval ja reedel", et olla puhkuse tüübilt puhkuse taotlemisel spetsiifilisem. 

  ![Puhkusetaotluse alustamine Teams`i vestluses.](./media/hr-teams-leave-app-initiate.png)

- Vestlusrobot sisestab puhkusetaotluse andmed teie eest. Valige **Vaba aja taotlemine** ja redigeerige taotluse üksikasju.

   Kui soovite esitada puhkusetaotlusi mitmele samale kuupäevale puhkusetüübile, valige **Tükeldatud päev** valik menüüst **Veel**. 

   Kui valite poolaasta puhkuse, kui puhkuse taotluse üksus on päevades, saate määrata, kas soovite taotleda vaba aega esimesel poolaastal või teisel poolaastal, valides suvandi **Poolaasta määratlus** **Veel** menüüst.
   
   ![Poolpäevade määratlemine.](./media/HalfDayDefinitions.png)

- Kui olete puhkusetaotluse üksikasjade redigeerimise lõpetanud, valige **Edasta**, et saata taotlus kinnitamiseks.

  ![Puhkusetaotluse edastamine.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Puhkuse haldamine Teamsis

Vahekaardil **Vaba aeg** saate kuvada järgnevat. 

- Saldo teabe iga registreeritud puhkuse tüübi kohta

- Tulevased puhkusetaotlused

- Vaba aja taotlused

- Puhkusetaotluste mustandid
 
### <a name="create-a-new-request"></a>Uue taotluse loomine

1. Valige uue puhkusetaotluse loomiseks **Uus taotlus**.

2. Sisestage päev või päevad, mida soovite vabaks võtta ja seejärel valige **Lisa**.

   ![Human Resources Teams`i puhkuse rakenduse vaba aja lisamine.](./media/TimeOffHours.png)

3. Vajadusel sisestage põhjusekood. Sisestage ka vajalikud kommentaarid ja lisage manused.

4. Valige valik **Tükeldatud päev** menüüst **Veel** kui soovite erinevatele puhkusetüüpidele esitada mitu puhkepäevakirjet samal kuupäeval.

5. Valige suvand **Poole päeva definitsioon**, et määratleda, kas soovite taotleda esimest pool vaba päeva või teist pool vaba päeva. See suvand on saadaval, kui puhkuse taotluse üksus on päevades ja taotletud summa on 0,5 päeva.

6. Kui olete lõpetanud teabe sisestamise, valige **Esita**, et esitada see kinnitamiseks. Saate sisestada ka **Salvesta mustandina**, et hiljem jätkata.

### <a name="manage-draft-requests"></a>Taotluste mustandite haldamine

1. Valige vahekaart **Mustandid**.

2. Taotluse redigeerimiseks valige pliiats või selle kustutamiseks prügikast.

3. Tehke vajalikud muudatused. Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks. Saate valida ka **Salvesta mustandina**, et hiljem jätkata.
   
### <a name="respond-to-teams-notifications"></a>Rakenduse Teams teatistele vastamine

Kui te olete või töötaja, kes olete puhkusetaotluse kinnitaja, saate te teatise Inimressursside rakenduses Teamsis. Saate valida teatise puhkuse taotluse vaatamiseks. Teatised kuvatakse ka alal **Vestlus**.

Kui olete kinnitaja, saate teatises valida **Kinnita** või **Keeldu** . Saate ka esitada valikulise teate.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Saada tulevane aja mahaminev teave kaastööjatele

Pärast rakenduse Human Resources installimist rakenduse Teamsi jaoks saate hõlpsalt saata teavet eelseisva eemaloleku kohta oma kaastöötajatele töörühmades või vestlustes.

1. Valige rakenduse Teams töörühmas või vestluses selle vestlusakna all olev nupp Human Resources.

   ![Nupp Human Resources vestlusakna all.](./media/hr-teams-leave-app-chat-button.png)

2. Valige puhkusetaotlus, mida soovite jagada. Kui soovite jagada puhkusetaotluse mustandit, valige enne **Mustandid**.

Teie puhkusetaotlus kuvatakse vestluses.

Kui jagasite taotluse mustandit, kuvatakse see mustandina.

## <a name="view-your-teams-leave-calendar"></a>Oma töörühma puhkusekalendri vaatamine

Kui olete otseste alluvatega juht, saate vaadata oma töörühma kinnitatud ja ootelolevaid vabu aegu.

1. Tehke Teamsi rakenduses Human Resources valik **Vaba aeg**.

2. Valige **Töörühma kalender**. Kalendris kuvatakse teie otsesed aruanded, mis on kinnitatud ja ootel vaba ajaga.

   > [!NOTE]
   > Kui te ei näe töörühma kalendrit, paluge administraatoril see lubada. Lisateabe saamiseks vt teemat [Installimine ja häälestus](hr-admin-teams-leave-app.md#install-and-setup).

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

## <a name="troubleshooting"></a>Tõrkeotsing

Kui teil on probleeme Teamsis rakendusse Dynamics 365 Human Resources sisselogimisega või selle kasutamisega, proovige neid tõrkeotsingujuhiseid. Kui teil on pärast tõrkeotsingut endiselt probleeme, siis võtke ühendust tugiteenusega. Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ma ei saa Teamsis rakendusse Human Resources sisse logida

Kui te ei saa rakendusse sisse logida, siis on võimalik, et konto, mida kasutate rakendusse Microsoft Teams sisse logimiseks, ei ole seotud töötajakirjega rakenduses Dynamics 365 Human Resources. Võtke ühendust oma süsteemiadministraatoriga, et teha kindlaks, et teie töötajakirje on korralikult seotud.

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>Sätetest ei Dynamics 365 Human Resources leia keskkonda

Kui te ei saa õiget Dynamics 365 keskkonda valida, ei pruugi kasutaja kirje õigesti sünkroonitud olla. Kasutajakirje uuesti loomiseks ja kasutaja sisselogimisandmetega seostamiseks pöörduge oma süsteemiadministraatori poole. Seejärel proovige mõne minuti jooksul Microsoft Teams Human Resources rakendusse sisse logida.

### <a name="translations-dont-display-correctly"></a>Tõlkeid ei kuvata õigesti

Kui tõlkeid ei kuvata ootuspäraselt, veenduge, et Teamsis valitud keel ühtiks inimressursside mooduli lehel **Kasutaja valikud** valitud keelega.

Otsige Teamsis aknas **Sätted** üles **Rakenduse keel**.

![Teams`i sätted.](./media/hr-teams-leave-app-settings.png)

Valige inimressursside moodulis **Sätted** ja seejärel **Kasutaja valikud**. Veenduge, et väljal **Keel** oleks valitud sama keel, mis Teamsi väljal **Rakenduse keel**.

![Human Resources kasutajavalikud.](./media/hr-teams-leave-app-user-options.png)

Kui tõlkeprobleemid ei lahene, andke meile teada. Teavet leiate teemast [Finance and Operationsi rakenduste või teenuse Lifecycle Services (LCS) tugi](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Tõrge puhkusetaotluste kinnitamise korral Teamsis rakenduses Human Resources

Kui saate Teamsi rakenduses puhkusetaotluste kinnitamise katsel tõrke, proovige järgmisi tõrkeotsingutoiminguid.

1. Veenduge, et konto, mida kasutate rakendusse Microsoft Teams sisse logimiseks, oleks sama, mida kasutate rakendusele Dynamics 365 Human Resources juurde pääsemiseks.

2. Kontrollige, et te oleks taotluse puhul sobiv kinnitaja, kontrollides puhkuse kinnitamise töövoo sätteid. Lisateavet puhkusetaotluse töövoogude kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Jäta kinnitajad ilma Teamsi vestluseteadete saamisest, mille eesmärgiks on puhkusetaotluste kinnitamine

1. Veenduge, et teatised on keskkonna ja kasutaja jaoks lubatud. Lisateabe saamiseks vaadake jaotist [Luba rakenduse Human Resources teavitused Teamsis](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ja [Teamsi teavituste sisse- või väljalülitamine individuaalsete kasutajate puhul](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Veenduge, et kasutajad on vahekaardile **Vestlus** sisse logitud samade mandaatidega, mida nad puhkuse taotluste kinnitamiseks kasutavad. Kasutage sõnumeid "väljalogimine" ja seejärel "sisselogimine" õigete mandaatidega sisse logimiseks.

3. Kui probleem ei lahene, kontrollige ärisündmuste süsteemi **pakett**-töö olekut süsteemiadministraatorina. Kui see on etapis **Ootamine** või **Teostamine**, kontrollige mõne minuti pärast uuesti. Kui olek jääb muutmata, logige tugipilet, et meie meeskond saaks probleemi lahendada.

## <a name="known-accessibility-issues"></a>Teadaolevad hõlbustusprobleemid

Teamsi rakendusel Human Resources on järgmised hõlbustusprobleemid, mille lahendamise nimel teeme tööd, et neid tulevastes väljaannetes poleks.

| Väljasta | Lahendus või selgitus |
| --- | --- |
| 400% suumimine töölaual peidab vaates mõned tegevusnupud. | Selle asemel soovitame kasutada luupi, kuni saame sellel tasemel suumi toetada. |
| Vahekaardil Eemaldus on vaate kaudu nuputegevus, samal ajal kui ta **loeb** päist väljaminekuruudustiku jaoks. | Ruudustikus päised ja elemendid on grupeeritud aasta alusel ning kokkupandavad. Seda esitust tõlgendatakse tegevustava kaubana, kuid mitte nii. |
| Vahekaardil **Vaba aeg** saab teha lisaks veel ühe nipsamise, kui valitakse uue taotluse **põhjuse kood**. | See nipsamine ei ava siiski ühtki peidetud juhtelementi. |
| Kui nipsate vahekaardil **Vaba aeg** avatud kalendri korral, liigutakse uue taotluse korral või taotluse redigeerimisel ülaosa asemel hoopis juhtelemendist välja. | Kui jõuate valikuni **Liigu tänase juurde**, võtke arvesse, et see on juhtelemendi lõpp ja nipske vastassuunas, et tagasi algusse saada. |
| Vahekaardil **Vestlus** viiakse fookus tagasi algusse, kui sisestate kuupäeva abistavat tööriista kaustades või klaviatuuri abil valides. | Vajutage tabeldusklahvi, kuni jõuate uuesti sisendi juurde. |

## <a name="privacy-notice"></a>Privaatsusavaldus

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Kasutaja Dynamics 365 Human Resources tekstisisestuse abil analüüsitakse aluseks olevat Microsoft Teams päringut/eesmärki mõista. Kasutajasisend, nt Otsingukonto Contoso, suunatakse ühte Microsofti kokuptiivne teenusest Language Understanding Nutikas Teenus (SOFT). Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/). Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso). See teave edastatakse siis Microsoft  [Azure boti raamistikule](https://azure.microsoft.com/services/bot-service/), mis suhtleb andmetega ja toob Dynamics 365 Human Resources kasutajapäringu jaoks soovitud teabe. 

Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus. Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase. Kui AJATEENUSEl on juurdepääs ainult kasutajapäringutele ja see ei ole loodud ühenduseks kasutaja andmete või kontoga, võib osa kasutaja ise sisestada kliendiandmeid, isikuandmeid või muid andmeid ja sellist päringu sisu sisaldava päringu, mille saab saataKOOSTE teenusesse ja Dynamics 365 Human Resources Dynamics 365 Human Resources Azure azure'i raamistikusse. 

Kasutaja päringute ja teadete sisu säilitatakse KRÜPTO süsteemi maksimaalselt 30 päevaks, krüptitakse ülejäänud ajal ja seda ei kasutata koolitusel või teenuse täiustamisel. Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid ja Azure Cosmos DB

Rakenduse kasutamisel võivad teatud kliendiandmed voogu väljapoole geograafilises piirkonnas, kus Dynamics 365 Human Resources Microsoft Teams teie rentniku Inimressursid teenus juurutatakse.

Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad sündmuste Microsoft Azure tabelisse ja . Microsoft Teams Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams. Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks. Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Vt ka

[Microsoft Teamsi allalaadimine ja installimine](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams spikrikeskus](https://support.office.com/teams)</br>
[Rakendus Human Resources Teamsis](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
