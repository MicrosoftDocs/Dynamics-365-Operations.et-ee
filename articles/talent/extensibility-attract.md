---
title: Rakenduse Attract laiendatavus
description: Selles teemas kirjeldatakse, kuidas saate laiendada rakendust Microsoft Dynamics 365 for Talent - Attract Microsofti Power Platformiga.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichsew
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 52790fbe500d9f55bc9cc86fba5d54f30b11e559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505860"
---
# <a name="extensibility-in-attract"></a>Rakenduse Attract laiendatavus

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent on rajatud lahenduse Common Data Service platvormile ning seda on võimalik mitmel viisil laiendada, kasutades Microsoft Power Platformi ja lahenduse Common Data Service võimalusi. Seega saate süsteemi konfigureerida ja isikupärastada, kasutades Microsoft PowerAppsi ja Microsoft Flow’d. Microsoft Power BI-ga saate ka inimeste kohta täiendavaid analüüsiandmeid koguda. Lisaks muudavad uued kohandatud tegevused nagu PowerAppsi ja veebisisu (iFrame'i) tegevused värbamisprotsessi kohandatavamaks kui kunagi varem. Nende tegevuste abil saate kohandada värbamisprotsessi vastavalt oma ettevõtte vajadustele ja protsessidele ning veenduda, et nii värbamismeeskond kui ka kandidaadid saavad sujuva, kohandatud kogemuse osaliseks.

## <a name="extending-option-sets-in-attract"></a>Suvandikomplektide laiendamine Attractis

**Suvandikomplekt** (märkeloend) on välja tüüp, mille saab üksusesse kaasata. See määratleb suvandite komplekti. Kui suvandikomplekt kuvatakse vormil, kasutab see ripploendi juhtelementi.  Attractis on mitu välja, mis on suvandikomplektid.  Hakkame tutvustama võimalust suvandikomplektide laiendamiseks, alustades väljadega Tagasilükkamise põhjus, Töösuhte tüüp ja Staaži tüüp.   Samuti saate lisatavatele suvanditele lisada lokaliseeritud kuvasilte. Lisateavet vt jaotisest [Suvandikomplekti siltide kohandamine](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Funktsioon Töö sisestamine LinkedIni nõuab lehel **Töö üksikasjad** väljade **Töösuhte tüüp** ja **Staaži tüüp** kasutamist. LinkedIn toetab nende väljade vaikeväärtuseid ja need kuvatakse pärast töö sisestamist. Seetõttu, kui sisestate töid LinkedIni ja muudate nende väljade olemasolevaid suvandikomplekti väärtusi, töö siiski sisestatakse, kuid LinkedIn ei kuva väljade **Töösuhte tüüp** ja **Staaži tüüp** kohandatud väärtusi.  

Allpool on toodud etapid, kuidas värskendada välja **Tagasilükkamise põhjus** väärtustega, mis on omased teie ettevõttele.  

1. Suvandikomplekti **Tagasilükkamise põhjus** laiendamiseks liikuge [PowerAppsi halduse veebisaidile](https://admin.powerapps.com).
2. Teil võidakse paluda oma kontole sisse logida. Esitage oma kasutajatunnus ja parool, mida kasutate teenusesse Dynamics365 ja/või Office365 sisselogimiseks, ning seejärel klõpsake nuppu **Edasi**.
3. Valige vahekaardil **Keskkonnad** keskkond, mida soovite hallata ja topeltklõpsake, et liikuda vahekaardile **Üksikasjad**.
4. Vahekaardil **Üksikasjad** tehke valik **Dynamics 365 halduskeskus**.
5. Valige eksemplar, mida soovite muuta ja tehke valik **Ava**.
6. Liikuge jaotisesse **Sätted**, **Kohandused** ja valige **Süsteemi kohandamine**.
7. Üksuse, mille jaoks soovite suvandikomplekti laiendada leiate, kui teete valiku **Üksused** ja laiendate gruppi. Selles näites on selleks **Tööavalduse üksus**.
8. Väljale, mille jaoks soovite suvandikomplekti laiendada, saate liikuda, kui valite suvandi **Väljad**. Selles näites on selleks **msdyn_rejectionreason**. Topeltklõpsake välja.
9. Tehke väljal **Suvandikomplekt** valik **Redigeeri**.
10. Valige ikoon **+**.
11. Sisestage **Silt**.  (See peab olema kordumatu väärtus – duplikaadid pole lubatud).
12. Valige käsk **Salvesta**.
13. Tehke lehe ülaosas valik **Avalda**.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Kasutage Microsofti Power platformi ära. 

Kuna kõik Attracti andmed asuvad lahenduses Common Data Service, saate oma ainulaadsete ärivajaduste Attracti kaasamiseks kasutada Microsofti Power Platformi tööriistu.

### <a name="powerapps"></a>PowerApps

PowerAppsi abil saate hõlpsasti luua rakendusi, mis loovad ühenduse teie Attracti andmetega ja kasutavad loogika lisamiseks Microsoft Exceli avaldisi. PowerAppsiga loodud rakendused töötavad nii veebis kui ka Apple iOS-i ja Google Androidi seadmetes.

Näiteks saate ülikoolide karjäärimessid värbajate jaoks lihtsamaks muuta, luues kergema rakenduse, mis võimaldab värbajatel CV-sid skannida ja rakenduses Attract kandidaate ametipositsioonidele esitada. Teise võimalusena võite luua rakenduse, mis aitab rahuldada teie ettevõtte vastavause vajadusi. Lisateavet PowerAppsi ja selle abil rakenduste loomise kohta vt teemast [Andmete integreerimine lahendusse Common Data Service](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Saate kasutada Microsoft Flow’d automaatsete töövoogude loomiseks, mis töötavad Attracti andmetel. Saate hõlpsalt luua ühenduse sadade populaarsete rakenduste ja teenustega, ilma et peaksite koodi kirjutama. Luues lahenduses Common Data Service vooge, mis suhtlevad rakendustega Attract Job, Candidate ja Application, saate automatiseerida mitmesuguseid toiminguid. Näiteks kui kandidaat võtab pakkumise vastu, võib saata teatise värbamismeeskonnale, või võib uudisest teavitada ka Twitteris. Lisateavet voogude kohta vt [Microsoft Flow arendaja dokumentatsioonist](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI võimaldab teil koostada ja vaadata kohandatud aruandeid ning armatuurlaudu, mis annavad teile sügavama ülevaate teie Attracti andmetest. Lisateavet Power BI ja interaktiivsete aruannete ning armatuurlaudade loomise kohta vt [Power BI dokumentatsioonist](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Kohandatud tegevused 

Saate lisada kohandatud tegevusi (nt PowerApps ja veebisisu (iFrame'i) tegevusi) tööprotsessi malli tasemel või uue töö loomisel. Need tegevused võimaldavad teil kohandada värbamisprotsessi ja tuua organisatsiooni ainulaadse äriloogika rakendusse Attract.

#### <a name="powerapps-activity"></a>PowerAppsi tegevus 

PowerApps tegevus võimaldab töö või tööportsessi malli loojal PowerAppsi rakenduse värbamisvoogu kaasata. Pärast rakenduse loomist ja avaldamist saate selle rakenduse ID sisestada tegevuse konfiguratsioonidesse. PowerAppsi rakendust kasutades saate lugeda ja kirjutada andmeid lahendusse Common Data Service. Saate rakenduse isegi vooga siduda. Näiteks on teil rakendus, mida värbajad kasutavad telefoniintervjuude ajal vormi täitmiseks. Sellisel juhul saate linkida rakenduse vooga, mis hindab, kas kandidaadiga saab kandideerimisprotsessis edasi liikuda. Sellist tüüpi tegevusi näevad vaid värbamismeeskonna liikmed. Lisateabe saamiseks PowerAppsi tegevuste konfigureerimise kohta vt [Tegevused rakenduses Attract](./activities-attract.md).

> [!NOTE]
> Tegevus PowerApps on saadaval ainult tervikliku värbamise lisandmooduli korral.

#### <a name="web-content-iframe-activity"></a>Veebisisu (iFrame'i) tegevus

Veebisisu (IFRAME'i) tegevus võimaldab teil kaasatada kohandatud veebilahenduse, mille olete loonud värbamisprotsessis või kandidaadi portaalis. Saate lugeda ja kirjutada andmeid vahetult lahendusest Common Data Service. Peale selle saate kohandada lahendust nii, et see käivitab voogusid või kasutab ära Microsoft Azure’i funktsioone. Lisateabe saamiseks veebisisu tegevuste konfigureerimise kohta vt [Tegevused rakenduses Attract](./activities-attract.md).

> [!NOTE]
> Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral.
