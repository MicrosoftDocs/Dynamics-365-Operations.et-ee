---
title: "Jaemüügikanali side määratlemine (Commerce Data Exchange)"
description: "Selles artiklis antakse ülevaade rakendusest Commerce Data Exchange ja selle komponentidest. Ta selgitab osa, mis iga komponendi mängib andmete ülekannet Microsoft Dynamics 365 operatsioonide ja jaemüügikanalid."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Jaemüügikanali side määratlemine (Commerce Data Exchange)

Selles artiklis antakse ülevaade rakendusest Commerce Data Exchange ja selle komponentidest. Ta selgitab osa, mis iga komponendi mängib andmete ülekannet Microsoft Dynamics 365 operatsioonide ja jaemüügikanalid.

<a name="overview"></a>Ülevaade
--------

Commerce andmevahetus on süsteem, mis edastab andmeid Dynamics 365 operatsioonide ja jaemüügikanalid, nagu Telliskivi-ja mördi kauplustes või online kauplustes. Jaemüügi kanali andmed andmebaas on eraldunud Dynamics 365 operatsioonide andmebaasi. Kanali andmebaasis on ainult jaemüügikannete jaoks vajalikud andmed. Kapten andmete konfigureeritud Dynamics 365 toiminguteks ning levitamise kanaleid. Kandeandmete luuakse Müügikoht (POS) süsteemi punktis või online, ja seejärel laadida Dynamics 365 toiminguteks. Andmejaotus on asünkroonne. Teisisõnu: andmete kogumise ja pakkimise protsess allika juures toimub sihtkohas andmete vastuvõtmise ja rakendamise protsessist eraldi. Mõne stsenaariumi (nt hinna ja varude otsingu) puhul tuleb andmed tuua reaalajas. Neil juhtudel toetada kaubanduse andmevahetus ka teenus, mis võimaldab reaalajas suhtlemist Dynamics 365 operatsioonide ja kanal. 

[![Uuendatud jaemüük pilt](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Teenus Async
Andmete muutmine, mis saadetakse kanalite määramiseks kasutatakse Microsoft SQL serveri muutuste jälitamise Dynamics 365 operatsioonide andmebaasi. Jaotus graafiku alusel, Dynamics 365 toimingute andmed paketid ja salvestab selle tsentraalselt (Azure bloobimälu). Eraldi pakktöötlusprotsess kasutab Commerce Data Exchange: Async Clienti teeki selle andmepaketi lisamiseks kanali andmebaasi. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Kaupluse andmeedastaja

Andmeedastaja tööd on mehhanism andmete jaotamiseks asukohtade vahel. Tööd koosnevad alamtöödest, mis määravad jaotatavaid andmeid sisaldavad tabelid ja tabeliväljad. Dynamics 365 operatsioonide sisaldab eelmääratletud Toiminguajasti töökohti ja subjobs, enamik organisatsioonide replikatsiooni nõuetele vastavad. Luuakse järgmist tüüpi eelmääratletud tööd.

-   **Lae töökohti** – lae töökohti saada andmed muutunud Dynamics 365 tegevuste kanali andmebaasidele. Kirjete muudatusi jälgitakse SQL Serveri muudatuste jälgimise abil.
-   **Upload tööde (P töökohti)** – Upload tööde pull müügi tehingud alates kanali Dynamics 365 operatsioonide andmebaasi. P-tööd laadivad andmeid üles järk-järgult. Kui P-töö käib, otsib Async Clienti teek andmeedastusloendurist kirjeid, mis on asukohast juba vastu võetud. Kirje laaditakse üles ainult juhul, kui selle andmeedastusloendur on suurem kui suurima leitud väärtus. P-tööd ei uuenda varem üles laaditud andmeid.

Jaotus ajakava saab käivitada andmete edastamise, kas käsitsi või pakett-töö Dynamics 365 operatsioonide planeerimine. Jaotusgraafik võib sisaldada vähemalt ühte kanali andmegruppi ja vähemalt ühte andmeedastaja tööd.

## <a name="realtime-service"></a>Reaalajas teenus
Commerce andmevahetus: Reaalajas teenus on integreeritud teenus, mis annab reaalajas suhtlemine Dynamics 365 operatsioonide ja jaemüügikanalid. Reaalajas teenus võimaldab POS arvutite ja konkreetsete andmete allalaadimiseks Dynamics 365 operatsioonide reaalajas online kauplustes. Kuigi enamik peamisi toiminguid teha kohalike kanalite andmebaasi, järgmistel juhtudel nõuda otsest juurdepääsu Dynamics 365 operatsioonide salvestatud andmete:

-   Kinkekaartide väljastamine ja lunastamine.
-   Püsikliendi punktide lunastamine.
-   Kreeditarvete väljastamine ja lunastamine.
-   Kliendikirjete loomine ja uuendamine.
-   Müügitellimuste koostamine, uuendamine ja lõpetamine.
-   Varude vastuvõtmine ostu- või üleviimistellimuse suhtes.
-   Inventuuride läbiviimine.
-   Müügitehingute toomine kaupluste lõikes ja tagastuskannete tegemine.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Eelnevalt määratletud reaalajalise teenus profiil on loodud.


