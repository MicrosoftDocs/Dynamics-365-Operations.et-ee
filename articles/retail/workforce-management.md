---
title: "Tööjõu halduse ülevaade"
description: "Selles teemas kirjeldatakse, kuidas tööjõu halduse (WFM) teenust saab kasutada tuttava kassa (POS) klientide, Modern POS-i ja pilvekassa kasutamiseks nii, et kaupluse juhid saaksid hõlpsasti oma töötajaid hallata."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Tööjõu halduse ülevaade

[!include[banner](includes/banner.md)]
    
Tööjõu halduse (WFM) teenus kasutab tuttavaid kassa (POS) kliente, Modern POS-i ja pilvekassat, et kaupluse juhid saaksid hõlpsasti oma töötajaid hallata. WFM-i teenus kasutab laiendusraamistikku vastavate pakettide allalaadimiseks kassas. Need paketid laaditakse alla kassa sulgemisel ja uuesti avamisel. Seega kui Microsoft annab välja uusi WFM-i funktsioone, tuleb kassarakendus sulgeda ja uuesti avada.

Selle teenuse abil saavad kaupluste juhid oma kauplustele hõlpsasti iganädalasi töögraafikuid luua ja avaldada. Siis saavad kaupluse töötajad kiiresti enda ja kolleegide graafikuid vaadata. Nii saavad nad teada, kes määratud vahetuste ajal koos nendega töötab. Kaupluse töötajad saavad luua ka taotlusi puudumiseks, vahetuse vahetamiseks ja vahetuse pakkumiseks. Kõik need taotlused käivitavad kindlaksmääratud töövoo.

Vahetuse ajal saavad kaupluse töötajad kasutada kassaklientidesse integreeritud sisse ja välja registreerimise funktsiooni. Siis saadetakse andmed peakontorisse palga töötlemiseks. Sisse ja välja registreerimise funktsioon on kassas juba olemas. Lisateavet seadistuse ja toetatud stsenaariumide kohta leiate jaotisest [Sisse- ja väljaregistreerimine](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Toetatud stsenaariumid
Selles jaotises on lisateave toetatud stsenaariumide kohta.

- **Graafikute koostamine ja avaldamine** – WFM-i teenus kasutab peakontoris konfigureeritud kassa lubasid määramiseks, kas töötajal on kaupluse juhataja privileegid. Ainult kaupluse juhatajad võivad graafiku haldamise toimingu abil graafikuid koostada ja avaldada. Nad saavad kiiresti graafiku koostada, kopeerides ja kleepides olemasoleva töövahetuse ühelt töötajalt teisele töötajale. Samuti saavad nad koostada graafiku, importides mõne eelmise nädala graafiku jooksvasse nädalasse.

    Kui graafikut pole avaldatud, on see mustandi olekus ja näeb avaldatud graafikust erinev välja. Kaupluste juhatajad saavad avaldada graafiku, klõpsates mis tahes nädalal nuppu **Avalda**. Kui nädalagraafik on avaldatud, avaldatakse automaatselt mis tahes muudatused. Muudatused on näiteks töövahetuste või puudumiste lisamine või kustutamine või töövahetuste või puudumiste redigeerimine. Kaupluse töötajad saavad vaadata ainult mitmesuguste nädalate kohta avaldatud graafikuid.
    
- **Taotluste koostamine ja kinnitamine** – kaupluse töötajad saavad luua kolme tüüpi taotlusi.

    - Puudumistaotlus
    - Vahetuse vahetamise taotlus
    - Vahetuse pakkumise taotlus

    Neid taotlusi saab koostada toiminguga Vahetuse taotlused. Iga taotlus järgib kindlaksmääratud töövoogu ja töötajad näevad hõlpsasti oma taotluste olekut.
    
    Puudumistaotlused saadetakse automaatselt kaupluse juhatajale kinnitamiseks. Kui kaupluse juhatajaid on mitu, saavad kõik juhatajad antud taotlust vaadata, kuid seda saab kinnitada või tagasi lükata ainult üks juhataja. Puudumise tüübid konfigureeritakse jaemüügi peakontoris lehe **Puhkuste ja puudumiste tüübid** moodulis **Jaemüük**. Kui kaupluse juhataja on taotluse kinnitanud või tagasi lükanud, viiakse see toimingu Graafiku taotlused vahekaardile **Ajalugu**.
    
    Vahetuse vahetamise või vahetuse pakkumise taotlus läheb kõigepealt töötajale, kellele taotlus saadeti. Kaupluse juhataja saab vaadata taotlust alles siis, kui see töötaja on selle kinnitanud. Seetõttu, kui töötaja vahetuse vahetamise või pakkumise taotluse tagasi lükkab, ei saa juhataja seda vaadata. Taotluse koostanud töötaja saab selle ka tühistada, enne kui juhataja selle kinnitab või tagasi lükkab.

- **Aktiivsete kaupluse töötajate kuvamine graafikuvaates** – kui töötaja kauplusse lisatakse, seostades ta näiteks kaupluse töötaja aadressiraamatuga, muutub töötaja WFM-i teenuses plaanimiseks kättesaadavaks. Peakontoris käitatakse korduv pakett-töö nimega **Töötaja andmete töötlemine tööjõu halduse jaoks**. See töö valmistab ette kaupluse töötaja seosed, mis saadetakse teenusesse Common Data Service (CDS).

    Sama protsessi kasutatakse töötaja eemaldamisel kauplusest. Kuid eemaldatud töötaja kuvatakse siiski varasemate, praeguse ja tulevaste nädalate puhul, kui sellele töötajale on määratud aktiivne töövahetus või puudumine. Seega, kui neid töövahetusi ja puudumisi ei kustutata, näidatakse eemaldatud töötajat nende nädalate puhul edasi.

