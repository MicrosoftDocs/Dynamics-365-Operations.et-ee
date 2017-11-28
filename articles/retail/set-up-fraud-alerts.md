---
title: Pettuseteatiste seadistamine
description: "Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Pettuseteatiste seadistamine

[!include[banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada kriteeriume ja reegleid, et panna potentsiaalselt petturlikud müügitellimused täiendavaks ülevaatamiseks ootele. Pettuste ülevaatamise funktsioon võimaldab kontrollida müügitellimuse teabe kehtivust. Kui müügitellimuse teave tundub organisatsiooni petturliku tegevuse kriteeriumite ja reeglite alusel kahtlane, võidakse tellimus ootele panna, et administraator saaks selle üle vaadata.

> [!NOTE]
> Seda funktsiooni saab kasutada ainult Retaili kõnekeskuse kanali müügitellimuse töötlemisel. 

Kui kõnekeskuse kanal on määratud, peab **Tellimuse lõpetamise lubamine** olema seatud väärtusele **Jah**. Kui tellimuse lõpetamine on lubatud, saavad kasutajad vaadata tellimuse kokkuvõtet ja klõpsata tellimuse lõpuleviimiseks käsku **Edasta**. Kasutajate jaoks on saadaval ka suvandid, mis võimaldavad panna müügitellimuse pettuse tõttu ülevaatamise ootele. Kõnekeskuse kasutaja sisestatud müügitellimusi töödeldakse edastamisprotsessi ajal pettuse kontrolli reeglite ja kriteeriumite alusel.

Süsteem järgib kaht tüüpi pettuse kriteeriume, et kontrollida, kas tellimus tuleks pettuse tõttu ülevaatamise ootele panna.

-   **Staatilised reeglid** kasutavad kindlat väärtust, nt telefoninumbrit, mis kantud musta nimekirja, või meiliaadressi, mida on teadaolevalt varem kasutatud petturlike kannete tegemiseks. Lehel **Staatilised pettuse andmed** saab lisada pettuse teabe käsitsi või andmete importimise kaudu, nii et petturlikule teabele on lisatud skoorid. Kui pettuse kontroll on sisse lülitatud, võrreldakse iga sisestatud müügitellimust staatiliste andmetega. Kui andmed sisalduvad kliendi arveldus- või tarneaadressis või müügireale märgitud tarneaadressis, liidetakse kõigi kordumatute vastete skoorid.  
-   **Dünaamilised reeglid** koosnevad muutujatest ja nende jaoks määratletud tingimustest. Dünaamiliste reeglitega saab kontrollida muid kriteeriume, mis ei ole staatilistes reeglites määratletud. Keerukamate JA-/VÕI-avaldiste abil saab võtta arvesse mitut tingimust, et tuvastada, kas reegli kriteeriumite ja edastatava müügitellimuse vahel on positiivne vaste. Näiteks kui kasutaja soovib panna pettuse ülevaatuse ootele kõikide nende klientide tellimused, kes on seotud konkreetse kliendigrupi väärtusega ja kes tellisid konkreetse toote, on kliendi ja toodete kontrollimiseks kasutatavad tingimused määratletud lehel **Reeglid** JA-tingimusega. Tellimus pannakse pettuse tõttu ootele ainult juhul, kui mõlemad tingimused vastavad tõele ja reeglile määratud skoori liitmine tõstab tellimuse pettuse skoori üle kõnekeskuse parameetrites määratletud pettuse miinimumskoori.

Kõnekeskuse kasutaja võib tellimuse ka käsitsi pettuse tõttu ootele panna. Kui tellimust sisestav kasutaja arvab, et tellimust esitav klient võib olla kahtlane, ja soovib, et keegi tellimuse enne töötlemist täpsemalt üle vaataks, võib tellimust sisestav kasutaja valida lehe **Müügitellimuse kokkuvõte** rippmenüüst **Ootel** suvandi **Pettuse tõttu käsitsi ootele viimine** (leht ilmub pärast funktsiooni **Tellimuse lõpuleviimine** käivitamist). Kasutajal palutakse sisestada selgitav märkus, miks ta peab tellimust petturlikuks, et ülevaatajal oleks rohkem konteksti.

Kõik pettuse skooride süstemaatilise arvutamise alusel või käsitsi ootele pandud tellimused kuvatakse lehel **Ootelolevad tellimused**, kus saab tellimuse üle vaadata ja seejärel tühistada või töötlemiseks vabastada.

> [!NOTE]
> Mitme reegli või liiga keerukate reeglite kasutamisel väheneb süsteemi jõudlus müügitellimuste edastamisel. Pettuseteatiste funktsioon ei ole optimeeritud käsitlema suurt hulka staatiliste pettuse andmete kirjeid ja paljusid aktiivseid reegleid. Pidage meeles, et kõnekeskuse müügitellimuse sisestamise esitamisfunktsiooni ajal analüüsitakse kõiki reegleid. Reegleid võrreldakse müügitellimuse päise ja tellimuse kõigi ridadega. Mida rohkem on reegleid ja mida keerukamad on nende avaldised, seda rohkem kulub töötlemiseks aega. Kui teie tellimuses on suur hulk rea kaupu ning palju aktiivseid reegleid ja staatilisi andmekirjeid, võib kõikide andmete ülevaatamise ja kontrollimise ning pettuse skoori arvutamise süstemaatiline protsess jõudlust märkimisväärselt mõjutada.  Seda funktsiooni kasutavad organisatsioonid peavad enne reeglimuudatuste või staatiliste pettuse kriteeriumite muudatuste tootmiskeskkonnas juurutamist alati veenduma, et tellimuste edastamisel töötlemisele kuluv aeg oleks aktsepteeritav.

