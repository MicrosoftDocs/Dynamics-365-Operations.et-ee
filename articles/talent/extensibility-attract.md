---
title: Rakenduse Attract laiendatavus
description: "See teema kirjeldab, kuidas Microsofti Power Platformiga on võimalik laiendada Microsoft Dynamics 365 for Talent - Attract rakendust."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Rakenduse Attract laiendatavus

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent on ehitatud lahenduse Common Data Service (CDS) for Apps platvormile ning seda on võimalik mitmel viisil laiendada, kasutades Microsofti Power Platformi ja lahenduse Common Data Service for Apps võimalusi. Seega saate süsteemi konfigureerida ja isikupärastada, kasutades Microsoft PowerAppsi ja Microsoft Flow'd. Microsoft Power BI-ga saate ka inimeste kohta täiendavat analüütikat koguda. Lisaks muudavad uued kohandatud tegevused nagu PowerAppsi ja veebisisu (iFrame'i) tegevused värbamisprotsessi kohandatavamaks kui kunagi varem. Nende tegevuste abil saate kohandada värbamisprotsessi vastavalt oma ettevõtte vajadustele ja protsessidele ning veenduda, et nii värbamismeeskond kui ka kandidaadid saavad sujuva, kohandatud kogemuse osaliseks.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Kasutage Microsofti Power platformi ära. 

Kuna kõik rakenduse Attract andmed asvuad lahenduses Common Data Service for Apps, saate oma ainulaadsete ärivajaduste Attracti kaasamiseks kasutada Microsofti Power platformi tööriistu.

### <a name="powerapps"></a>PowerApps

PowerAppsi abil saate hõlpsasti luua rakendusi, mis loovad ühenduse teie Attract andmetega ja kasutavad loogika lisamiseks Microsoft Exceli avaldisi. PowerAppsiga loodud rakendused töötavad nii veebis kui ka Apple iOS-is ja Google Android seadmetel.

Näiteks saate ülikoolide karjäärimessid värbajate jaoks lihtsamaks muuta, luues kergema rakenduse, mis võimaldab värbajatel CV-sid skannida ja rakenduses Attract kandidaate ametipositsioonidele esitada. Teise võimalusena võite luua rakenduse, mis aitab rahuldada teie ettevõtte vastavause vajadusi. Lisateavet PowerAppsi ja selle abil rakenduste loomise kohta vt [Andmete integreerimine lahendusse Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Saate kasutada Microsoft Flowd automaatsete töövoogude loomiseks, mis töötavad rakenduse Attract andmetel. Saate hõlpsalt luua ühenduse sadade populaarsete rakenduste ja teenustega, ilma et peaksite koodi kirjutama. Luues teenuses Common Data Service for Apps vooge, mis suhtlevad rakendustega Attract Job, Candidate ja Application, saate automatiseerida mitmesuguseid toiminguid. Näiteks kui kandidaat võtab pakkumise vastu, võib saata teatise värbamismeeskonnale, või võib uudisest teavitada ka Twitteris. Voogude kohta lisateabe saamiseks vt [Microsoft Flow dokumentatsiooni](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI võimaldab teil koostada ja vaadata kohandatud aruandeid ja arumatuurlaudu, mis annavad teile sügavama ülevaate teie rakenduse Attract andmetest. Lisateavet Power BI ja interaktiivsete aruannete ning armatuurlaudade loomise kohta vt [Power BI dokumentatsioonist](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Kohandatud tegevused 

Saate lisada kohandatud tegevusi (nt PowerApps ja veebisisu (iFrame'i) tegevusi) tööprotsessi malli tasemel või uue töö loomisel. Need tegevused võimaldavad teil kohandada värbamisprotsessi ja tuua organisatsiooni ainulaadse äriloogika rakendusse Attract.

#### <a name="powerapps-activity"></a>PowerAppsi tegevus 

PowerApps tegevus võimaldab töö või tööportsessi malli loojal PowerAppsi rakenduse värbamisvoogu kaasata. Pärast rakenduse loomist ja avaldamist saate selle rakenduse ID sisestada tegevuse konfiguratsioonidesse. PowerApps rakendust kasutades saate lugeda ja kirjutada andmeid teenusesse Common Data Service for Apps. Saate rakenduse isegi vooga siduda. Näiteks on teil rakendus, mida värbajad kasutavad telefoniintervjuude ajal vormi täitmiseks. Sellisel juhul saate linkida rakenduse vooga, mis hindab, kas kandidaadiga saab kandideerimisprotsessis edasi liikuda. Sellist tüüpi tegevusi näevad vaid värbamismeeskonna liikmed. Lisateabe saamiseks PowerAppsi tegevuste konfigureerimise kohta vt [Tegevused rakenduses Attract](./activities-attract.md).

> [!NOTE]
> Tegevus PowerApps on saadaval ainult tervikliku värbamise lisandmooduli korral.

#### <a name="web-content-iframe-activity"></a>Veebisisu (iFrame'i) tegevus

Veebisisu (IFRAME'i) tegevus võimaldab teil kaasatada kohandatud veebilahenduse, mille olete loonud värbamisprotsessis või kandidaadi portaalis. Saate lugeda ja kirjutada andmeid vahetult teenusest Common Data Service for Apps. Lisaks saate kohandada lahenduse nii, et see käivitab voogusid või kasutab ära Microsoft Azure'i funktsioone. Lisateabe saamiseks veebisisu tegevuste konfigureerimise kohta vt [Tegevused rakenduses Attract](./activities-attract.md).

> [!NOTE]
> Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral.

