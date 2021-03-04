---
title: Teabe leidmiseks otsingute abil
description: Paljudel väljadel otsingud, mis saavad aidata teil hõlpsalt õiget või soovitud väärtust leida. Otsingutele on lisatud mitmed täiustused, mis muudavad need juhtelemendid kasutatavamaks ja kasutajad produktiivsemaks. Selles teemas saate teada nende uute otsingufunktsioonide kohta ja saate mõned näpunäited, et süsteemis otsinguid optimaalselt kasutada.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a555db8ced5981abf1f3f58f16b77e1c263dcfa2
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693637"
---
# <a name="find-information-by-using-lookups"></a>Teabe leidmiseks otsingute abil

[!include [banner](../includes/banner.md)]

Paljudel väljadel otsingud, mis saavad aidata teil hõlpsalt õiget või soovitud väärtust leida. Otsingutele on lisatud mitmed täiustused, mis muudavad need juhtelemendid kasutatavamaks ja kasutajad produktiivsemaks. Selles teemas saate teada nende uute otsingufunktsioonide kohta ja saate mõned näpunäited, et süsteemis otsinguid optimaalselt kasutada.

## <a name="responsive-lookups"></a>Hästi reageerivad otsingud

Varasemates versioonides otsingu juhtelemendiga suheldes peaks kasutaja tegema rippmenüü avamiseks selge toimingu. Selleks võib sisestada juhtelementi tärni (\*), et filtreerida otsingut juhtelemendi praeguse väärtuse põhjal, klõpsates rippmenüü nuppu või kasutades kiirklahvi **Alt**+**Allanool**. Otsingu juhtelemente on muudetud järgmistel viisidel, et paremini ühtida praeguste veebitavadega.

- Otsingu rippmenüüd avanevad nüüd automaatselt pärast väikest pausi tippimisel ja rippmenüü sisu filtreeritakse otsingu juhtelemendi väärtuse põhjal.

    Pange tähele, et rippmenüü automaatse avanemise vana käitumine pärast tärni (\*) sisestamist on aegunud.

- Pärast otsingu rippmenüü avamist toimub järgmine.

    - Kursor püsib otsingu juhtelemendis (selle asemel, et fookus liiguks rippmenüüsse), et saaksite jätkata juhtelemendi väärtusele muudatuste tegemist. Samas saab kasutaja endiselt kasutada klahve **Ülesnool** ja **Allanool**, et muuta rippmenüüs olevaid ridu, ja sisestusklahvi, et valida praegune rippmenüüs olev rida.
    - Rippmenüü sisu reguleeritakse pärast otsingu juhtelemendi väärtusele mis tahes muudatuste tegemist.

Näiteks kaaluge otsinguvälja nimega **Linn**.

Kui fookus on väljal **Linn**, saate alustada soovitud linna otsimist, sisestades mõned tähed, nagu „col”. Pärast tippimise lõpetamist avaneb automaatselt otsing, kus on filtreeritud need linnad, mis algavad tähejadaga „col”.

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

Sellel hetkel on kursor endiselt otsinguväljal. Kui jätkate tippimist, et väärtus oleks „veer”, reguleerub otsingusisu automaatselt, et kajastada kõige värskemat väärtust juhtelemendis.

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

Isegi kui fookus on ikka otsingu juhtelemendis, saate kasutada ka klahve **Ülesnool** või **Allanool**, et tõsta esile rida, mida soovite valida. Kui vajutate klahvi **Enter**, valitakse otsingust esiletõstetud rida ja juhtelemendi väärtust värskendatakse.

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Rohkemate andmete kui vaid ID-de sisestamine

Andmete sisestamisel on loomulik, et nime osas proovivad kasutajad olemit tähistava identifikaatori asemel tuvastada olemit, nagu klient või hankija. Paljud (kuid mitte kõik) otsingud lubavad nüüd kontekstilist andmesisestust. See mitmekülgne funktsioon võimaldab kasutajal sisestada otsingu juhtelementi ID või vastava nime.

Näiteks müügitellimuse loomisel arvestage välja **Kliendi konto**. See väli näitab kliendi puhul suvandit **Konto ID**, kuid tavaliselt eelistab kasutaja müügitellimuse loomisel sisestada väärtuse **Konto ID** asemel väärtust **Konto nimi**, näiteks väärtuse „US-003” asemel väärtust „Hulgimüük”.

Kui kasutaja alustas otsingu juhtelementi suvandi **Konto ID** sisestamisega, avaneks rippmenüü automaatselt, nagu on kirjeldatud eelmises jaotises ja kasutaja näeks otsingut sellisena, nagu allpool on näidatud.

[![Kontekstuaalne otsing kliendi konto ID sisestamisel](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Siiski saab kasutaja nüüd sisestada ka suvandi **Konto nimi** alguse. Selle tuvastamisel näeb kasutaja seejärel järgmist otsingut. Pange tähele, kuidas veerg **Nimi** teisaldatakse otsingus esimesse veergu ja kuidas otsingut sorditakse ja filtreeritakse veeru **Nimi** põhjal.

[![Kontekstuaalne otsing kliendi nime sisestamisel](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Täpsema filtreerimise ja sortimise jaoks ruudustiku veerupäiste kasutamine

Eelmises kahes jaotises kirjeldatud otsingu täiustused parandavad suuresti kasutaja võimet navigeerida otsingu ridades, põhinedes otsingu välja **ID** või **Nimi** otsingule „algab väärtusega”. Samas on olukordi, kus õige rea leidmiseks on vajalik täpsem filtreerimine (või sortimine). Sellistes olukordades peab kasutaja kasutama otsingus ruudustiku veerupäistes olevaid filtreerimis- ja sortimissuvandeid. Näiteks arvestage müügitellimuse rida sisestavat töötajat, kes peab tootena määrama õige „kaabli” asukoha. Sõna „kaabel” sisestamine juhtelementi **Kaubakood** ei ole abiks, kuna puuduvad tootenimed, mis algavad sõnaga „kaabel”.

![emptyitemlookup](./media/emptyitemlookup.png)

Selle asemel peab kasutaja eemaldama otsingu juhtelemendi väärtuse, avama otsingu rippmenüü ja filtreerima rippmenüü, kasutades ruudustiku veeru päist, nagu allpool on näidatud. Hiirt (või puudutamist) kasutav kasutaja saab lihtsalt klõpsata (või puudutada) mis tahes veerupäist, et saada juurdepääs selle veeru filtreerimise ja sortimise suvanditele. Klaviatuuri kasutaja peab lihtsalt vajutama teist korda klahvikombinatsiooni **Alt**+**Alla** **Allanool**, et liigutada fookus rippmenüüle, pärast mida saab kasutaja tabeldusklahvi abil õigesse veergu liikuda ja vajutada seejärel klahvikombinatsiooni **Ctrl**+**G**, et avada ruudustiku veeru päise rippmenüüd.

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Pärast filtri rakendamist (vaadake allolevat pilti) saab kasutaja leida ja valida rea tavapärasel viisil.

![filtereditemlookup](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]