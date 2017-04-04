---
title: Teabe leidmiseks kasutada otsingud
description: "Microsoft Dynamics 365 toiminguteks, paljudes valdkondades on otsingud, mis aitavad kergesti leida õige või soovitud väärtus. Mitmeid laiendusi on lisatud otsingud, et muuta need kontrollimised veelgi rohkem kasutada ja teha kasutajad tootlikumaks. Selle teema saab õppida neid uue otsingu funktsioone ja saavad mõned vihjed saada optimaalselt kokku otsingud süsteemis."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Teabe leidmiseks kasutada otsingud

Microsoft Dynamics 365 toiminguteks, paljudes valdkondades on otsingud, mis aitavad kergesti leida õige või soovitud väärtus. Mitmeid laiendusi on lisatud otsingud, et muuta need kontrollimised veelgi rohkem kasutada ja teha kasutajad tootlikumaks. Selle teema saab õppida neid uue otsingu funktsioone ja saavad mõned vihjed saada optimaalselt kokku otsingud süsteemis.  

<a name="responsive-lookups"></a>Tundlik otsingud
------------------

Varasemates versioonides Dynamics 365 toiminguteks, otsingu juhtelemendi kasutamisel, kasutaja on selgesõnaliselt tegutsemise rippmenüüst menüü avamiseks. See vist tippige tärn (\*) filtreerida otsingu juhtelemendi praeguse väärtuse juhtelemendi nupu rippmenüü või kasutades on **Alt**+**alla nool** klaviatuuri otsetee. Otsingu kontroll on muudetud kooskõlas praeguse veebi tasakaalustamiseks järgmiselt:

-   Otsing rippmenüüst avab automaatselt pärast väikest pausi liigitada, rippmenüüst menüü sisu keelatud vastavalt otsingu juhtelemendi väärtuse.
    -   Pange tähele, et automaatse avamise rippmenüüst pärast tüpiseerimise tärniga vana käitumine (\*) on taunitud.
-   Pärast otsingu vaikimisi on avatud, toimub järgmiselt:
    -   Kursor jääb see otsing kontrolli (mitte keskenduda siirdunud rippmenüüst menüü), et muuta juhtelemendi väärtusega. Siiski kasutaja saate kasutada ka **nool üles** ja **alla nool** on vaikimisi ridade muuta ja sisestada praeguse rea valimiseks on vaikimisi.
    -   Sisu on vaikimisi korrigeerib pärast mis tahes muudatustest otsingu juhtelemendi väärtusega.

Võtame näiteks otsinguvälja nimega **linna**. 

Kui fookus on selle **linna** välja, saab hakata otsima linna, mis on kirjutanud mõned tähed, nagu "col."  Pärast tippimist, otsingu avatakse automaatselt, filtri abil neis linnades, mis algavad "col". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Sel hetkel kursor on endiselt otsinguväljal. Kui tipite väärtus on "colum", siis otsingu sisu automaatset kohandamist, Viimane väärtuse kontrollimisel. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Kuigi fookus on veel otsing kontrolli, saate ka selle **nool üles** või **alla nool** abil esile rida, mille soovite valida. Kui vajutate **Enter** esiletõstetud rea valida otsingu ja juhtelemendi väärtusega värskendatakse. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Kirjutades üle ID-d
Andmete sisestamisel on loomulik kasutajad tuvastada üksuse, nt kliendi või hankija nime asemel on identifikaator, mis tähistab ettevõtte seisukohalt. Dynamics 365 puhul palju (kuid mitte kõik) otsingud võimaldavad nüüd kontekstipõhine andmesisestuse uuemas versioonis. See võimas funktsioon võimaldab kasutaja ID-d või vastava nime otsingu juhtelemendi tüüpi. 

Võtame näiteks selle **kliendi konto** välja müügitellimuse loomisel. Sellel väljal kuvatakse selle **konto ID** klient, kuid kasutaja tavaliselt eelistavad sisestamiseks on **konto nimi** asemel on **konto ID** selle välja, kui loote müügitellimuse, nagu "Metsa Wholesales" asemel "US-003."

Kui kasutaja sisestada mõne **konto ID** otsingu juhtelemendi selle vaikimisi automaatselt avab eelmises osas kirjeldatud ja kasutaja näeksid otsingu, nagu allpool näidatud.

[![Kontekstuaalne otsing kui sisestate kliendi konto ID](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Siiski kasutaja saab sisestada ka nüüd alguses on **konto nimi** ka. Kui see on avastatud, siis kasutajale kuvatakse järgmine otsing. Teade kuidas **nimi** veeru teisaldatakse tuleb esimeses veerus otsingu ja kuidas otsingu sortida ja filtreerida vastavalt selle **nimi** veerg.

[![Kontekstuaalne otsing kliendi nime sisestamisel](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Kasutades võrku veerupäised täpsemaks filtreerimiseks ja sortimiseks
Otsing täiustused arutati eelmises kahes osas oluliselt parandada kasutaja võimet liikuda ridade põhjal "algab" otsing otsingu ning **ID** või **nimi** otsingu välja. Siiski on olukordi, kus täiustatud filtreerimine (või sortimine) on vaja leida õige rida. Sel juhul peab kasutaja kasutama filtreerimine ja sortimine suvandid koordinaatvõrgu veeru päised otsingu sees. Võtame näiteks müügitellimuse reale sisestada töötaja, kes vajab leida paremal "kaabel" tootega. Kirjutades "traat" on **kaubakood** kontroll ei ole kasulik, kui ei ole nimed, mis algavad "kaablit." 

![emptyitemlookup](./media/emptyitemlookup.png) 

Selle asemel peab kasutaja otsingu juhtelemendi väärtust ning avada otsing vaikimisi koordinaatvõrgu veeru päist, kasutades vaikimisi filter, nagu allpool näidatud. Hiir (või puudutage) kasutaja saab lihtsalt klõpsake (või puudutage) veeru pealkirja filtreerimise ja sorteerimise Valikud veeru. Klaviatuuri kasutaja, kasutaja peab lihtsalt vajutage **Alt**+**alla****noole** teist korda fookuse rippmenüüst menüü, mille kasutaja saab õige veerule sakk ja vajutage **Ctrl**+**G** koordinaatvõrgu veeru päise rippmenüüst menüü avamiseks. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Pärast filtri rakendamist (vt kujutist allpool), kasutaja saab leida ning valige rida nagu tavaliselt. 

![filtereditemlookup](./media/filtereditemlookup.png)


