---
title: E-kirjade mallid
description: Selles teemas kirjeldatakse meilimalle, mida saate rakenduses Microsoft Dynamics 365 for Talent - Attract luua ja kasutada.
author: josaw
manager: AnnBe
ms.date: 10/19/2018
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
ms.openlocfilehash: 85581968d9d242460117693174acbf906463997f
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---

# <a name="email-templates"></a>E-kirjade mallid
[!include[banner](../includes/banner.md)]

Meilimallide teeki kasutades saavad administraatorid luua ühtse teema ja kaubamärgi kõigile läbi rakenduse Microsoft Dynamics 365 for Talent: Attract saadetavatele meilidele. Administraatorid saavad ka teiste kasutajate kasutatavat meilisisu mallide kogu kureerida. Värbamistöörühm saab neid malle oma töövoos kasutada meilide tõhusamaks saatmiseks. Mõned meilid on Attractis konfigureeritud automaatseks saatmiseks ja administraator saab kasutada meilimallide teeki nende meilide sisu kohandamiseks.

## <a name="global-template-configurations"></a>Üldise malli konfigureerimine

Kogu meilisuhtlusele ühtse tootjakohanduse loomiseks peab administraator esmalt kõigile meilimallidele määrama üldise päise ja jaluse. Halduskeskuse vahekaardi **Meilimalli sätted** jaotises **Päis** saab administraator üles laadida kujutise kõigi meilide päise või bännerina kasutamiseks. Kujutis võib olla ettevõtte logo, Pilt võib olla ettevõtte logo, kirja päismik või mõni muu esindav kujutis. Soovitame, et laius oleks vahemikus 25 kuni 800 pikslit ja kõrgus vahemikus 25 ja 150 pikslit, sest need mõõtmed on optimaalsed enamikele meiliklientidele, nagu näiteks Microsoft Outlook. Kujutis peab olema JPEG-, JPG, PNG või SVG fail ja faili suurus peab olema väiksem kui 1 megabait (MB). Pärast pildi üles laadimist luuakse ja kuvatakse päise eelvaade. Kui päise kujutis tuleb eemaldada või vahetada, saab administraator kasutada eelvaate kohal asuvad valikut **Eemaldada**.

Jaotisesse **Jalus** saab administraator sisestada ettevõtte privaatsuspoliitika, kontaktide ja kasutustingimuste linke. Need lingid lisatakse automaatselt loodavasse jalusesse. Seejärel kuvatakse jaluse eelvaade.

Salvestage kindlasti enne halduskeskuse sulgemist oma muudatused.

> [!NOTE] 
> Päis ja jalus on kõigi meilide globaalsätted. Seetõttu on nad näha kõigis läbi Attracti saadetud meilides. Kui sätteid ei ole konfigureeritud, jäetakse päis ja jalus kõigist meilidest välja.

## <a name="email-template-library"></a>Meilimallide teek 

Pärast globaalse malli konfiguratsiooni seadistamist saab administraator alustada mallide loomist ja kureerimist kõigile läbi Attracti saadetavatele meilidele. Meilimallide teek on saadaval ainult administraatoritele. Teegi avamiseks valige peamisest navigeerimise menüüst vahekaart **Meilimallid**. Teek on liigitatud erinevate Attracti tegevuste järgi, mille tõttu meile saadetakse, näiteks nagu planeerimine, hindamine ja töö loomine. Administraator võib valida mistahes kategooria, et näha kõiki selle tegevusega seotud meilitüüpe. Näiteks valige **Planeerimine**, et näha erinevat tüüpi planeerimisprotsessi käigus saadetavaid meile ja kõiki malle, mis on igat tüüpi meili jaoks saadaval. Kategooria iga alajaotis esindab meili tüüpi.

Teatud tüüpi meilidel võib olla rohkem kui üks adressaat. Näiteks kategooria **Planeerimine** meilid, mis saadetakse siis, kui vaja on vestluse ajakava kokkuvõtet, saadetakse nii kandidaadile kui ka intervjueerijale. Igal jaotisel on kaks peamist veergu: **Malli nimi** ja **Saaja**. Jaotise iga rida esindab ühte meili tüübi malli. Algul ilmub iga malli reale lukuga sümbol. See sümbol näitab, et mall on Attractiga kaasa tulnud standardne mall ja seda ei saa kustutada. Iga malli juures saab administraator selle malli koopia saamiseks kasutada ellipsnuppu (**...**), määrata see vaikimisi malliks või kustutada see. Kui mall on seatud vaikimisi malliks, võib toimuda üks kahest käitumisest. Käitumist näitab malli reale ilmuv märk või märgid:

- **Vaikimisi** – see märk näitab, et mall on saadetava meili vaikemall ja sellele lisatakse andmeid, kui kasutaja saadab seda konkreetset tüüpi meili.
- **Vaikimisi** + **Automaatselt saadetav** – märgikombinatsioon näitab, et mall on süsteemi loodud ja automaatselt saadetavate meilide aktiivne mall.

Malli redigeerimiseks valige rida ja muutke malli.

> [!NOTE]
> Igal kindlat tüüpi meili saajal on vaikemall. Kõik Attracti standardsed mallid on määratud vaikemallideks, kuni administraator loob kindlat tüüpi meilidele uue malli ja määrab selle vaikemalliks.

## <a name="create-a-template"></a>Loo mall

Malli loomiseks valige meilimallide teegi paremast ülanurgast **+ Uus mall**. Selle meilitüübi valimiseks, millele te malli loote, valige saaja, protsess ja sündmus meili saatmiseks. Seejärel valige **Loo**.

Mall avatakse redigeerimisvaates ja te saate mallile nime panna. Näiteks kui mall on mõeldud USA ülikooli kandidaatidele, kuid sisu on kirjutatud prantsuse keeles, võite sisestada pealkirjaks **Ülikool\_USA\_Prantsuse**. Mistahes malli pealkiri, teema ja sisu toetavad teisi keeli peale inglise keele.

Malli välja **Kellele** ei saa muuta, sest olete malli luues saaja juba valinud.

Isikuid nagu **Värbaja** või **Personalijuht** saate lisada koopia (Cc) reale. Kui meil on saadetud, asendatakse need rollid töö kontekstis automaatselt asjakohaste kasutajatega.

Teema ja sisu sisu toetavad kohatäited. Kohatäiteid saate lisada trükkides **\#** ja valides seejärel automaatteksti ripploendist sobiva kohatäite. Saadaolevate kohatäitjate loend kuvatakse lehekülje parema küljel. Kui meil on saadetud, asendatakse kohatäited töö ja saaja kontekstis automaatselt. Näiteks kandidaatidele saadetava meili mall sisaldab kohatäidet \#{Kandidaadi\_nimi}. Kui meil saadetakse kandidaadile, kelle nimi on Cameron, asendatakse kohatäide nimega Cameron.

Sisu toimetaja on RTF-redaktor, mis võimaldab teil teksti kujundada ja vormindada. Samuti võimaldab see sisestada hüperlinke ja ankruid.

Pärast teatud tüüpi meilile malli loomist valige malli rea ellipsnupp (**...**) ja määrake see vaikemalliks.

## <a name="consume-templates"></a>Kasutusmallid

Kui värbamistöörühm saadab meili, saab kasutada administraatori loodud malle. Kui kasutaja saadetavale meilile on loodud mitu malli, ilmub meili koostamise töövoo rippmenüü. Vaikemall sisestatakse automaatselt, kuid kasutaja saab valida mõne muu malli.

> [!NOTE] 
> Automaatselt saadetavatele meilidele saab luua mitu malli. Siiski, aktiivseks malliks saab määrata ainult ühe malli. Sest seda protsessi käivitavad sündmused, saab ainult administraator määrata, millist malli tuleks kasutada. See põhineb mallide teegi märkide **Vaikimisi** ja **Automaatselt saadetav** märkidest.

