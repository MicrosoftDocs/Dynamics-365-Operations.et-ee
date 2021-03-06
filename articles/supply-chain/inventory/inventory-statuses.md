---
title: Varude olekud
description: Selles artiklis kirjeldatakse, kuidas kasutada varude olekuid varudel kategoriseerimiseks ja jälgimiseks.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3c8b467f29037bbb869189e3607e11f40aad2c2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829856"
---
# <a name="inventory-statuses"></a>Varude olekud

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas kasutada varude olekuid varudel kategoriseerimiseks ja jälgimiseks.

## <a name="set-up-and-use-inventory-statuses"></a>Varude olekute häälestamine ja kasutamine

Saate varude kategoriseerimiseks kasutada varude olekuid. Seejärel saate algatada sobivad toimingud, näiteks varude täiendamise või paigutamistöö.

Siin on mõned näited viisidest, kuidas saate varude olekuid kasutada.

- Looge varude olekud vaba kaubavaru, sissetulevate kannete ja väljaminevate kannete jaoks.
- Määrake lao kannete puhul varude vaikeolek.
- Muutke kaubavarude olekut enne saabumist, saabumise ajal või siis, kui kaubad varude liikumise ajal kõrvale pannakse.
- Kasutage varude olekuid tagastatavate kaupade hindamiseks ja kaupade katvuse plaanimiseks koondplaneerimisel.

Varude olek on üks laoala dimensioonigrupi dimensioonidest. Varude olekuid võib kategoriseerida saadaolevaks või kättesaamatuks ja saate kasutada parameetrit **Varude blokeerimine** kättesaamatu varude olekuga kaupade blokeerimiseks. Blokeeritud olekuga kaupasid loetakse füüsiliseks varuks ja neid ei saa kasutada tootmistellimuses, müügitellimuses, üleviimistellimuses või väljaminevas kandes.

Saadaoleva ja kättesaamatu varude olekuga laokaupa saab kasutada sissetulevaks tööks. Näiteks loote saadaoleva oleku nimega *Valmis*, kättesaamatu oleku nimega *Kahjustatud* ja blokeeritud oleku nimega *Blokeeritud*. Kui loote ostutellimuse vastuvõetud või tagastatud kaupade puhul, kui mõni kaup on kahjustatud või katki, saate muuta nende kaupade varude olekuks ostutellimuse real *Kahjustatud*. Pärast nende kaupade vastuvõtmist seatakse olekuks automaatselt *Blokeeritud*. Mobiilse seadme abil kahjustatud kaupade skannimisel saab Supply Chain Management kasutada asukohakorraldusi ja töömalle teabe kuvamiseks sobiva asukoha või erinevate asukohtade kohta, kuhu saate need kaubad kõrvale panna. Tagastatud kaupade puhul luuakse väljamineku tüüp *Reserveerimine* lehel **Varude kanded**.

Saate määrata, millised varude olekud on blokeerivad olekud, kasutades lehe **Varude olekud** märkeruute **Varude blokeerimine**. Varude olekuid ei saa kasutada blokeerivate olekutena müügitellimuste, üleviimistellimuste ega projekti integreerimise puhul.

Väljamineva töö puhul saate kasutada erinevaid blokeerimata varude olekuid, et kontrollida, milliseid varusid reserveerida. Kui teil on kaupu olekuga *Blokeeriv* ja nendele kaupadele tehakse koondplaneerimine, loetakse need kaubad puuduvateks ja varusid täiendatakse automaatselt. Lisaks ei saa väljamineva tööga seotud kvaliteettellimuste puhul **varude olekut** kvaliteettellimuse kinnitamise osana uuendada.

> [!NOTE]
> Varude olekut ei saa muuta kohtades, kus on olemas avatud töö. Näiteks kui tegite ostu kauba saamiseks, kuid ei teinud "pane ära" sammu, oleks vastuvõtva asukoha jaoks olemas avatud töö ja kui prooviksite selles asukohas varude olekut muuta, kuvatakse tõrge. Seotud töö lõpuleviimine või tühistamine võimaldaks teil olekut muuta.
>
> Tavaliselt muudavad avatud laotööga seotud vaba kaubavaru olekut ainult töötajad, kes kasutavad laohalduse mobiilirakendust Warehouse Management (nt teisaldamisprotsessi käigus).

Pärast varude olekute seadistamist saate määrata saidile, kaubale ja laole varude vaikeoleku. Saate määrata vaikeoleku ka müügi-, üleviimis- ja ostutellimustele. Müügitellimuste ja väljamineva üleviimistellimuse vaikeoleku puhul ei saa suvand **Varude blokeerimine** olla seatud valikule *Jah*. Varude olekut, mis on päritud saidi, lao, kauba, ostutellimuse, üleviimistellimuse või müügitellimuse vaikesätetest, saab muuta mobiilse seadmega või ostutellimuse, müügitellimuse või üleviimistellimuse real.

Saadaolevate varude olekuga kaupade katvuse plaanimiseks valige laoala dimensiooni puhul suvand **Laovarude plaanimine dimensiooni järgi** lehel **Laoala dimensioonigrupid**. Viisardi **Kauba laovarud** avamisel kuvatakse saadaoleva olekuga kaubad lehel **Olek**. Nende kaupade katvuse sätete loomiseks valige varude oleku ID saadaolevate varude olekute jaoks. Katvuse sätete põhjal saate arvutada kaubavajadused ning ennustada saadaolevate kaupade pakkumist ja nõudlust koondplaanimise käigus. Kauba katvuse seadistust ei saa luua blokeeritud varude olekuga. Kauba katvuse parameetrite loomiseks või muutmiseks võite ka kasutada lehte **Kauba laovarud**.

## <a name="change-inventory-statuses"></a>Varude olekute muutmine

Varude olekuid saate muuta kas lehel **Laoseis asukoha järgi** või kasutades perioodilist ülesannet *Varude oleku muutmine*.

- Kui kasutate perioodilist ülesannet *Varude oleku muutmine*, saate valida, milliseid kirjeid kaasata ja määrata ülesande käivitamine partiis soovitud intervalliga.
- Varude oleku muutmiseks kindla protsessina avage leht **Laoseis asukoha järgi**, valige vastavad kirjed ja valige seejärel nupp **Varude oleku muutmine**.

> [!NOTE]
> Funktsioon *Dimensioonide jälgimisega juhitava kauba laoseisu muutmine* võimaldab teil muuta laoseisu, mida juhivad jälgimise dimensioonid, ja värskendada ainult valitud kirjeid. [Funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil saate funktsiooni vastavalt vajadusele lubada. Kui funktsioon on lubatud, saate teha järgmist.
>
> - Lehel **Laoseis asukoha järgi** saate nuppu **Kuva dimensioonid** kasutades kuvatud dimensioonide põhjal ridu grupeerida ja muuta valitud ridade olekut.
> - Lehel **Laoseis asukoha järgi** saate valida mitu kirjet ja seejärel kasutada nuppu **Varude oleku muutmine**, et neid kõiki korraga muuta.
> - Perioodilise ülesande **Varude oleku muutmine** abil on võimalik filtreerida jälgimise dimensioonide järgi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
