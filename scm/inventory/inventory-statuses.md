---
title: Varude olekud
description: "Selles artiklis kirjeldatakse, kuidas kasutada varude olekuid varudel kategoriseerimiseks ja jälgimiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 1fcdf262ee1e7e1fbbdd0a5fed46fb1867f8d8fd
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-statuses"></a>Varude olekud

Selles artiklis kirjeldatakse, kuidas kasutada varude olekuid varudel kategoriseerimiseks ja jälgimiseks.

Saate varude kategoriseerimiseks kasutada varude olekuid. Seejärel saate algatada sobivad toimingud, näiteks varude täiendamise või paigutamistöö. 

Siin on mõned näited viisidest, kuidas saate varude olekuid kasutada.

-   Looge varude olekud vaba kaubavaru, sissetulevate kannete ja väljaminevate kannete jaoks.
-   Määrake lao kannete puhul varude vaikeolek.
-   Muutke kaubavarude olekut enne saabumist, saabumise ajal või siis, kui kaubad varude liikumise ajal kõrvale pannakse.
-   Kasutage varude olekuid tagastatavate kaupade hindamiseks ja kaupade katvuse plaanimiseks koondplaneerimisel.

Varude olek on üks laoala dimensioonigrupi dimensioonidest. Varude olekuid võib kategoriseerida saadaolevaks või kättesaamatuks ja saate kasutada parameetrit **Varude blokeerimine** kättesaamatu varude olekuga kaupade blokeerimiseks. Blokeeritud olekuga kaupasid loetakse füüsiliseks varuks ja neid ei saa kasutada tootmistellimuses, müügitellimuses, üleviimistellimuses või väljaminevas kandes. 

Saadaoleva ja kättesaamatu varude olekuga laokaupa saab kasutada sissetulevaks tööks. Näiteks loote saadaoleva oleku nimega **Valmis**, kättesaamatu oleku nimega **Kahjustatud** ja blokeeritud oleku nimega **Blokeeritud**. Kui loote ostutellimuse vastuvõetud või tagastatud kaupade puhul, kui mõni kaup on kahjustatud või katki, saate muuta nende kaupade varude olekuks ostutellimuse real **Kahjustatud **. Pärast nende kaupade vastuvõtmist seatakse olekuks automaatselt **Blokeeritud**. Kahjustatud kaupade skannimisel mobiilse seadme abil saab Microsoft Dynamics 365 for Operations kasutada asukohakorraldusi ja töömalle teabe kuvamiseks sobiva asukoha või asukohavahemiku kohta, kuhu saate need kaubad kõrvale panna. Tagastatud kaupade puhul luuakse väljamineku tüüp **Reserveerimine** lehel **Varude kanded**. 

Väljamineva töö jaoks kasutage saadaoleva varude olekuga kaupu. Kui teil on kaupu olekuga **Katki** ja nendele kaupadele tehakse koondplaneerimine, loetakse need kaubad puuduvateks ja varusid täiendatakse automaatselt. 

Pärast varude olekute seadistamist saate määrata saidile, kaubale ja laole varude vaikeoleku. Saate määrata vaikeoleku ka müügi-, üleviimis- ja ostutellimustele. Müügitellimuste ja väljamineva üleviimistellimuse vaikeoleku puhul ei saa suvand **Varude blokeerimine** olla seatud valikule **Jah**. Varude olekut, mis on päritud saidi, lao, kauba, ostutellimuse, üleviimistellimuse või müügitellimuse vaikesätetest, saab muuta mobiilse seadmega või ostutellimuse, müügitellimuse või üleviimistellimuse real. 

Saadaolevate varude olekuga kaupade katvuse plaanimiseks valige laoala dimensiooni puhul suvand **Laovarude plaanimine dimensiooni järgi** lehel **Laoala dimensioonigrupid**. Viisardi **Kauba laovarud **avamisel kuvatakse saadaoleva olekuga kaubad lehel **Olek**. Nende kaupade katvuse sätete loomiseks valige varude oleku ID saadaolevate varude olekute jaoks. Katvuse sätete põhjal saate arvutada kaubavajadused ning ennustada saadaolevate kaupade pakkumist ja nõudlust koondplaanimise käigus. Kauba katvuse seadistust ei saa luua blokeeritud varude olekuga. Kauba katvuse parameetrite loomiseks või muutmiseks võite ka kasutada lehte **Kauba laovarud**.


