---
title: Ärivestlus Koos Dllchanneliga klienditeeninduse mooduli jaoks
description: See artikkel kirjeldab Rakenduse Commerce Vestlus koos Thechanneliga customer Service’i moodulile moodulis Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: b8eaed3eb015e96b1db6fa2297c341ea9d3ff8ad
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473805"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Ärivestlus Koos Dllchanneliga klienditeeninduse mooduli jaoks

[!include [banner](includes/banner.md)]

See artikkel kirjeldab *Rakenduse Commerce Vestlus koos Thechanneliga customer Service’i* moodulile moodulis Microsoft Dynamics 365 Commerce.

Commerce version 10.0.29 väljalaskes on Ärimoodulile Lisatud Commerce Commerce Commerce Koos Klienditeeninduse mooduliga Commerce Commerce vestlus. Ärivestluse funktsioon pakub e-commerce’i kliente Dynamics 365 klienditeeninduse vestlusvõimalustega, mis hõlmab reaalajas agendi tuge kliendipäringute lahendamiseks, klienditeeninduse loomiseks ja äriklientidele müügi hõlbustamiseks.

Ärivestluse funktsioon võimaldab jaemüüjatel need eesmärgid saavutada.

- Klientide isikupärastatud kaasamise suurendamine, et aidata kliendilojaalsuset parandada.
- Parandada klienditeenindust inimagendi ja iseteeninduse vestluste integreerimise kaudu.
- Abiagendid saavad kogemust reaalajas kliendiprofiili, tellimuse ja ostu andmete kaudu, mis juhtida töö parendust ja kaasamist.
- Parandada klientide üldist rahulolu, et aidata müügi kasvu.

Ärivestluse funktsiooni osana on saadaval järgmised võimalused:

- Ärivestlus klienditeeninduse jaoks Koos Channeliga
- Commerce Call **Centeri lisamine** rakenduse vahekaardina agendi kogemuses Dynamics 365 Thechannel for Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Klienditeeninduse hankija eeltingimused

Eeltingimuseks on ärivestluse konfigureerimine klienditeeninduse halduse elemendis Ning ärivestluse kogemuse konfigureerimiseks on vaja osa parameetreid. Juhiseid vt vestluse [kanali konfigureerimine](/dynamics365/customer-service/set-up-chat-widget).

Pärast klienditeenuse administreerimishalduse klienditeeninduse halduse vestluse konfigureerimist saate skripti, mis sarnaneb järgmise näitega.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopeerige see skript, sest teil on vaja selle väärtusi vestlusemooduli konfigureerimiseks.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Ärivestlus Koos Sisendi kanaliga klienditeeninduse kohustuslike väljade jaoks

Järgmises tabelis on näidatud klienditeeninduse halduse halduse skriptväärtused klienditeeninduse halduskeskuse jaoks, mis on vajalik klienditeeninduse mooduli jaoks ärivestluse ja klienditeeninduse kanali konfigureerimiseks.

| Elemendi atribuut | Kirjeldus |
| ------------- |--------------|
| Skripti allikas | **Src väärtus vestluse** elemendi skriptis. |
| Andmerakenduse ID | Andmerakenduse **ID väärtus vestluse** elemendi skriptis. |
| Andmeorganisatsiooni ID | **Data-org-ID väärtus** vestluse elemendi skriptis. |
| Andmeorganisatsiooni URL | Andmete org **- URL-i väärtus** vestluse elemendi skriptis. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Konfigureerige ärivestluse kogemus oma e-äri saidi jaoks.

Üks soovitatav viis oma e-äri saidi vestluskogemuse juurutamiseks on Lisada klienditeeninduse mooduli Commerce Commerce koos Klienditeeninduse mooduliga Ärivestlus ühiskasutusega päise killust, mida kasutatakse teie e-commerce’i saidi lehtedel.

Vestlusmooduli lisamiseks saidi päise killustaks Commerce’i saidi koostajas, järgige neid samme.

1. Minge saidikonstruktoris **killustajatele**.
1. Valige suvand **Uus**.
1. Tükidialoogi **valimine** valige **klienditeeninduse mooduli Commerce** Commerce Vestlus koos klienditeenindusega, sisestage killu jaoks nimi ja seejärel valige **OK**.
1. Valige liigendusvaates **Msdmeeter365 CS-i vestluseühenduse pesa**.
1. Paremal oleval **vestluse** atribuutide paanil järgige neid samme.

    1. Sisestage **skripti lähteväljale** **rc** väärtus, mille olete klienditeeninduse skripti jaoks klienditeenuse skripti kaudu kliendilt saanud.
    1. Sisestage **andmerakenduse ID** väljale andmerakenduse ID **väärtus,** mille te klienditeeninduse skripti jaoks rakenduseltChannel omandate.
    1. **Andmeorganisatsiooni ID väljal** on andmeorganisatsiooni ID **väärtus,** mille te klienditeeninduse skripti jaoks Ettevõttelt saadi.
    1. Sisestage **andmeorganisatsiooni URL-i** väljale andmeorganisatsiooni URL-i väärtus **,** mille te klienditeeninduse skripti jaoks klienditeenuse pakkujalt saate.

    ![Commerce’i vestlusmooduli killu loomine Commerce’i saidi koostajas.](media/Commerce-chat-creating-new-fragment.png)

1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. **Minge killustele** ja avage oma saidi päise killust.
1. **Valige konteineri vaikepesas** kolmikpunkt (**...**) ja seejärel valige käsk Lisa **kill.**
1. Dialoogiaknas **Vali** moodulid valige varem loodud vestluse tükk ja seejärel valige **OK**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Commerce headquartersi lisamine klienditeeninduse jaoks rakenduse vahekaardina

Võite lisada rakenduse vahelehte Commerce headquartersi jaoks klienditeeninduse klienditeeninduse äris. Live-agentid saavad siis Kasutada Dynamics 365 Commerce klienditeeninduse agendi jaoks Kliendi agendi kogemuse kasutajaliidest, et pääseda hõlpsasti juurde kliendi jaoks kontekstiteavet ja müügitellimuste teavet sisaldavale klienditeeninduse moodulile. Lisaks saavad klienditeeninduse agendid teha uusi tellimusi, käivitada tagastusi ja kontrollida tellimuse olekuteavet.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Uue rakenduse vahekaardi loomine, kus laaditakse moodulis Commerce Headquarters iFrame 

Rakenduse uue vahekaardi loomiseks, mis laadib rakendusmoodulis Commerce headquartersi iFrame, järgige neid samme.

1. Avage tegija [Power Apps portaal](https://make.powerapps.com).
1. Vasakul oleval navigeerimispaanil valige suvand **Rakendused**.
1. Valige **klienditeeninduse halduskeskus**.
1. Minge agendi **kogemusele**.
1. Vahekaardil **Avalduse mallid** valige **Haldamine**.
1. Looge kolmanda osapoole veebisaidi tüübi **jaoks uus rakenduse vahekaart**. Juhiseid vt rakenduse vahekaardi [mallide haldamine](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Sisestage **URL**-parameetri **väärtuse** väljale Parameetrid **järgmine URL**, `<YourOrganizationHeadquartersURL>``<LegalEntityname>` kus ja asendatakse need asjakohaste väärtustega. Kanali klienditeenindus loeb vestluse **{AccountNumber}** kontekstist. Seetõttu puhkus nii **{AccountNumber}**, nagu on.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. **Jätke andmeparameetri** väärtuse **väli** tühjaks.

![Dynamics 365Channel Customer Service’is rakenduse vahekaardi loomine.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Dynamics 365 klienditeeninduse kliendi agentidele uue rakenduse vahekaardi lubamine

Dynamics 365 klienditeeninduse kliendi agentidele uue rakenduse vahekaardi lubamiseks järgige neid samme.
    
1. Avage tegija [Power Apps portaal](https://make.powerapps.com).
1. Vasakul oleval navigeerimispaanil valige suvand **Rakendused**.
1. Valige **klienditeeninduse halduskeskus**.
1. Minge klienditoe **workstreami \>.**
1. Avage oma agentide jaoks loodud töövoog ja seejärel valige jaotises **Täpsemad sätted** suvand Seansi **vaikeväärtus**.
1. Valige **jaotises Rakenduse vahekaardid** **vahekaart Lisa olemasolev rakendus** ja seejärel lisage varem loodud rakenduse vahekaart. See samm tagab, et rakenduse vahekaart, mis laadib Commerce headquartersi iFrame moodulisse, ilmub, kui agent saab sissetuleva vestluskutse teie e-äri veebisaidilt.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Dynamics 365Channel’i kontekstimuutujate lisamine klienditeeninduse jaoks

Dynamics 365Keskusest klienditeeninduse jaoks kontekstimuutujate lisamiseks järgige neid samme.

1. Avage tegija [Power Apps portaal](https://make.powerapps.com).
1. Vasakul oleval navigeerimispaanil valige suvand **Rakendused**.
1. Valige **klienditeeninduse halduskeskus**.
1. Minge klienditoe **workstreami \>.**
1. Avage oma agentide jaoks loodud sissevoolu ja seejärel **minge** jaotisesse Täpsemad sätted kontekstimuutuja **jaotisse**.
1. Valige **käsk** Redigeeri ja lisage **AccountNumber** tekstitüübi **kontekstimuutujana**. See muutuja aitab Commerce Headquartersi laadida klienditeavet vastavate kontonumbritega.

> [!NOTE]
> Kui soovite e-ärikanalist lugeda sisse logitud kasutajate meiliaadressisid ja nimesid, **·** **·** **·** **saate** lisaks tekstitüübi kontekstimuutujale lisada ka e-posti ja nime tekstitüübi kontekstimuutujatena.
