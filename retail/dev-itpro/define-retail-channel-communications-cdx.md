---
title: "Jaemüügikanali side määratlemine (Commerce Data Exchange)"
description: "Selles artiklis antakse ülevaade rakendusest Commerce Data Exchange ja selle komponentidest. Selgitatakse rolli, mida iga komponent mängib Microsoft Dynamics 365 for Retail ja jaemüügikanalite vahelises andmete ülekandmises."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Jaemüügikanali side määratlemine (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade rakendusest Commerce Data Exchange ja selle komponentidest. Selgitatakse rolli, mida iga komponent mängib Microsoft Dynamics 365 for Retail ja jaemüügikanalite vahelises andmete ülekandmises.

<a name="overview"></a>Ülevaade
--------

Commerce Data Exchange on süsteem, mis edastab andmeid Microsoft Dynamics 365 for Retaili ja jaemüügikanalite (nt võrgupoed või traditsioonilised kauplused) vahel. Jaemüügikanali andmeid säilitav andmebaas on Microsoft Dynamics 365 for Retaili andmebaasist eraldi. Kanali andmebaasis on ainult jaemüügikannete jaoks vajalikud andmed. Koondandmed konfigureeritakse Microsoft Dynamics 365 for Retailis ja jaotatakse kanalitesse. Kandeandmete luuakse kassasüsteemis või võrgupoes ja laaditakse seejärel Microsoft Dynamics 365 for Retaili üles. Andmejaotus on asünkroonne. Teisisõnu: andmete kogumise ja pakkimise protsess allika juures toimub sihtkohas andmete vastuvõtmise ja rakendamise protsessist eraldi. Mõne stsenaariumi (nt hinna ja varude otsingu) puhul tuleb andmed tuua reaalajas. Nende stsenaariumide toetamiseks sisaldab Commerce Data Exchange ka teenust, mis võimaldab Microsoft Dynamics 365 for Retaili ja kanali vahelist reaalajas suhtlust. 

[![värskendatud-jaemüügidiagramm](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Teenus Async
Microsoft SQL Serveri muudatuste jälgimist Microsoft Dynamics 365 for Retaili andmebaasis kasutatakse kanalitele saadetavate andmete muudatuste määratlemiseks. Jaotusgraafiku alusel pakib Microsoft Dynamics 365 for Retail andmed ja salvestab need tsentraalsesse salve (Azure’i bloobimällu). Eraldi pakktöötlusprotsess kasutab Commerce Data Exchange: Async Clienti teeki selle andmepaketi lisamiseks kanali andmebaasi. 

[![Teenus Async](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Kaupluse andmeedastaja

Andmeedastaja tööd on mehhanism andmete jaotamiseks asukohtade vahel. Tööd koosnevad alamtöödest, mis määravad jaotatavaid andmeid sisaldavad tabelid ja tabeliväljad. Microsoft Dynamics 365 for Retail sisaldab eelmääratletud andmeedastaja töid ja alamtöid, mis vastavad enamiku organisatsioonide andmeedastuse nõuetele. Luuakse järgmist tüüpi eelmääratletud tööd.

-   **Allalaadimistööd** – allalaadimistööd laadivad muutunud andmeid Microsoft Dynamics 365 for Retailist kanali andmebaasidesse. Kirjete muudatusi jälgitakse SQL Serveri muudatuste jälgimise abil.
-   **Üleslaadimistööd (P-tööd)** – üleslaadimistööd toovad müügikanded kanalist Microsoft Dynamics 365 for Retaili andmebaasi. P-tööd laadivad andmeid üles järk-järgult. Kui P-töö käib, otsib Async Clienti teek andmeedastusloendurist kirjeid, mis on asukohast juba vastu võetud. Kirje laaditakse üles ainult juhul, kui selle andmeedastusloendur on suurem kui suurima leitud väärtus. P-tööd ei uuenda varem üles laaditud andmeid.

Jaotusgraafikut kasutatakse andmeedastuse käitamiseks, kas käsitsi või Microsoft Dynamics 365 for Retailis pakett-töö plaanimisel. Jaotusgraafik võib sisaldada vähemalt ühte kanali andmegruppi ja vähemalt ühte andmeedastaja tööd.

## <a name="realtime-service"></a>Teenus Real-time Service
Teenus Commerce Data Exchange: Real-time Service on integreeritud teenus, mis pakub reaalajas sünkroonitud sidet Microsoft Dynamics 365 for Retaili ja jaemüügikanalite vahel. Real-time Service lubab eraldi kassaarvutitel ja e-poodidel tuua konkreetseid andmeid Microsoft Dynamics 365 for Retailist reaalajas. Kuigi enamikku põhitoimingutest saab teha kohalikus kanali andmebaasis, nõuavad järgmised stsenaariumid otsest juurdepääsu Microsoft Dynamics 365 for Retaili salvestatud andmetele.

-   Kinkekaartide väljastamine ja lunastamine.
-   Püsikliendi punktide lunastamine.
-   Kreeditarvete väljastamine ja lunastamine.
-   Kliendikirjete loomine ja uuendamine.
-   Müügitellimuste koostamine, uuendamine ja lõpetamine.
-   Varude vastuvõtmine ostu- või üleviimistellimuse suhtes.
-   Inventuuride läbiviimine.
-   Müügitehingute toomine kaupluste lõikes ja tagastuskannete tegemine.

[![Teenus Real-time Service](./media/rts.png)](./media/rts.png) 

Luuakse eelmääratletud Real-time Service’i profiil.




