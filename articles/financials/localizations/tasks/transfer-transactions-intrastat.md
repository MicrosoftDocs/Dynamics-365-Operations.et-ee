--- 
title: "Kannete ülekandmine Intrastati"
description: Selles protseduuris selgitatakse, kuidas seadistada Intrastati parameetreid ja edastada kandeid Intrastati.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cc21497a6905cdb57bd687b7bff0d9dc810ba9eb
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-transactions-to-the-intrastat"></a>Kannete ülekandmine Intrastati

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris selgitatakse, kuidas seadistada Intrastati parameetreid ja edastada kandeid Intrastati. Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.


## <a name="create-new-and-update-existing-commodity-code"></a>Uue kaubakoodi loomine ja olemasoleva kaubakoodi värskendamine
1. Minge jaotisse Tooteteabe haldus > Seadistus > Kategooriad ja atribuudid > Kategooriahierarhiad.
2. Otsige või valige loendist kirje „Intrastati kaubaartikli koodid."
3. Klõpsake loendis valitud real olevat linki.
4. Valige puustruktuuris väärtus 'kirje'.
    * Valige näiteks Intrastat\Speaker.  
5. Klõpsake nuppu Redigeeri.
6. Laiendage jaotist Väliskaubandus.
7. Sisestage või valige väärtus väljal Lisaühikud.
    * Valige näiteks tk.  
8. Tehke väljal Kaal pole rakendatav valik Jah.
9. Tehke puustruktuuris valik 'Intrastat'.
10. Klõpsake suvandit Uus kategooriasõlm.
11. Sisestage väljale Nimi kaubaartikli nimi.
    * Tippige näiteks Muu kaup.  
12. Sisestage väljale Kood kauba kood.
    * Tippige näiteks väärtus 995 00 00.  
13. Sisestage väärtus väljale Hüüdnimi.
    * Tippige näiteks väärtus Muu.  
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Kaubakoodi määramine toote hierarhiale ja väljastatud tootele
1. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja Nimi väärtusega 'müük'.
2. Klõpsake loendis valitud real olevat linki.
3. Laiendage puustruktuuris väärtust 'kategooria sõlm'.
    * Laiendage näiteks väärtust Sales hierarchy\Home audio.  
4. Valige puustruktuuris 'kauba koodile määratav kategooria'.
    * Tehke näiteks valik Sales hierarchy\Home audio\Speakers.  
5. Laiendage jaotist Kaubakoodid.
6. Klõpsake vahekaarti Lisa.
7. Tehke väljal Vali hierarhia valik 'Intrastat'.
8. Loendist kaubakoodi otsimine ja valimine
    * Tehke näiteks valik 920 20 34 Speaker.  
9. Klõpsake suvandit SelectCodes.
10. Klõpsake nuppu OK.
11. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
12. Valige loendist väljastatud toode, mille saate määrata kauba koodile.
    * Valige näiteks väärtus D0001.  
13. Klõpsake nuppu Redigeeri.
14. Laiendage jaotist Väliskaubandus.
15. Väljale Kaup kauba koodi sisestamine
    * Valige näiteks väärtus 920 20 34 Speaker.    
16. Sisestage väljale Kulude protsent number.
    * Sisestage näiteks väärtus 3.  
17. Väljale Riik/regioon päritoluriigi või -regiooni sisestamine
    * Valige näiteks väärtus AUT.  
18. Laiendage jaotist Varude haldus.
19. Sisestage väljale Netokaal kaal kilodes.
    * Sisestage näiteks väärtus 2,5.  
20. Klõpsake nuppu Salvesta.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Intrastati kandekoodide ja väliskaubanduse parameetrite seadistamine
1. Avage Maks > Seadistus > Väliskaubandus > Kandekoodid
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Kande kood.
    * Sisestage näiteks tagastusena kandekoodile väärtus 21.  
4. Tippige väljale Nimi kandekoodi nimi.
    * Sisestage näiteks väärtus Tagasta.  
5. Valige suvand väljal Statstiline summa.
    * Valige näiteks väärtus Tühi, mis näitab, et kandele tuleb alati esitada statistiline väärtus, mille puhul kandekood 21 on alati null.  
6. Avage Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid
7. Sisestage või valige väärtus väljal Kande kood.
    * Valige näiteks väärtus 11.  
8. Sisestage või valige väärtus väljal Kreeditarve.
    * See väärtus määratleb ka füüsilise tagastuse. Füüsilise tagastuse kreeditarve kantakse Intrastati töölehel vastassuunaga. Näiteks kantakse tagastustellimuse saabumine üle lähetusena.   Muidu käsitletakse kreeditarvet parandusena ja see edastatakse sama suuna ja vastasmärgiga. Näiteks saabumise korrigeerimine edastatakse saabumisena, millel on negatiivne kogus ja aktiivne lipp on seatud olekusse Parandus.  
9. Laiendage jaotist Ülekanne.
10. Tehke väljal Artikliga kaubad valik Jah.
    * Valige see suvand, kui soovite üle kanda ainult kanded, millel on kaubaartikli kood määratud. Kaubaartikli koodita kandeid ei edastata Intrastati.  
11. Valige suvand väljal Kanna üle, kui täidetud on järgmine kriteerium.
    * Tehke näiteks valik Üks valitutest.  
12. Laiendage jaotist Kaubakoodide hierarhia.
13. Klõpsake vahekaarti Riigi/regiooni atribuudid.
14. Klõpsake valikut Uus.
15. Sisestage või valige väärtus väljal Riik/piirkond.
    * Valige näiteks väärtus FRA.  
16. Sisestage riigi ISO-kood väljale Intrastati kood.
    * Tippige näiteks tekst FR.  
17. Valige väljal Riigi/piirkonna tüüp suvand EL.
18. Klõpsake vahekaarti Numbriseeriad.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Tarneviiside ja Intrastatis tasude lisamise reegliste seadistamine
1. Avage Müük ja turundus > Seadistus > Jaotus > Tarneviisid
2. Otsige loendist ja valige soovitud kirje.
    * Valige näiteks 20 Air.  
3. Laiendage jaotist Väliskaubandus.
4. Klõpsake nuppu Redigeeri.
5. Sisestage või valige väärtus väljal Transport.
    * Valige näiteks 02.  
6. Avage Müügireskontro > Tasude seadistamine > Tasude kood.
7. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja Tasude kood väärtusega 'veos'.
8. Laiendage jaotist Väliskaubandus.
9. Klõpsake nuppu Redigeeri.
10. Tehke väljal Intrastati arve väärtus valik Jah.
    * Summa kantakse väljale Arve tasud ja see võetakse kokku väljal Arve summa kantud summaga.    Tehke väljal Intrastati statistiline väärtus valik Jah, kui muudatuste summa tuleb edastada väljale Statistilised tasud ja liita statistilise summaga.  

## <a name="sell-products-for-eu-customers"></a>Toodete müümine EL-i klientidele
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Väljal Kliendi konto EL-i kliendi valimine
    * Valige näiteks „DE-012 Litware Retail“.  
4. Laiendage jaotist Tarne.
5. Sisestage või valige väärtus väljal Tarneviis.
    * Valige näiteks 20 Air.  
6. Klõpsake nuppu OK.
7. Asetage kursor müüsitellimuse ridade esimesele reale.
8. Sisestage või valige väärtus väljal Kaubakood.
    * Valige näiteks 'D001'.  
9. Laiendage jaotis Rea üksikasjad.
10. Klõpsake vahekaarti Väliskaubandus.
    * Väli Transport täidetakse automaatselt valitud tarneviisi alusel.  
11. Sisestage või valige väärtus väljal Sadam.
12. Klõpsake suvandit Finantsid.
    * Vastavalt sätetele lisatakse see summa Intrastati arve väärtusele.  
13. Klõpsake valikut Tasude haldamine.
14. Sisestage või valige väärtus väljal Tasukood.
    * Valige näiteks 'FREIGHT'.  
15. Märkige ruut Säilita.
16. Sisestage arv väljale Tasude väärtus.
    * Sisestage näiteks '10'.  
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.
19. Klõpsake toimingupaanil valikut Arve.
20. Klõpsake valikut Arve.
21. Laiendage jaotis Parameetrid.
22. Valige väljal Kogus väärtus Kõik.
23. Laiendage jaotist Seadistus.
24. Sisestage kuupäev väljale Arve kuupäev.
    * Sisestage näiteks '31.01.2015'.  
25. Klõpsake nuppu OK.
26. Klõpsake nuppu OK.
27. Sulgege leht.
28. Klõpsake valikut Uus.
29. Valige väljal Kliendi konto EL-i klient.
    * Valige näiteks 'DE-013 Trey Wholesales'  
30. Klõpsake nuppu OK.
31. Sisestage või valige väärtus väljal Kaubakood.
    * Valige näiteks 'D0001'.  
32. Klõpsake nuppu Salvesta.
33. Klõpsake valikut Arve.
34. Sisestage kuupäev väljale Arve kuupäev.
    * Sisestage näiteks kuupäev '31.01.2015'.  
35. Klõpsake nuppu OK.
36. Klõpsake nuppu OK.

## <a name="transfer-transactions-to-the-intrastat"></a>Kannete ülekandmine Intrastati
1. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.
2. Klõpsake käsku Ülekanne.
3. Tehke väljal Kliendiarve valik Jah.
4. Klõpsake käsku Filtreeri.
5. Loendis rea märkimine kuupäevaga
6. Sisestage väärtus väljale Kriteeriumid.
    * Sisestage näiteks filter perioodile jaanuar 2015 (täpne väärtus oleneb teie kuupäevavormingust): 01.01.2015..31.01.2015  
7. Klõpsake nuppu OK.
8. Klõpsake nuppu OK.
9. Otsige ja valige loendist edastatud kirje.
10. Klõpsake vahekaarti Üldine.
    * Vaadake üle edastatud andmed, sh sihtkoha/lähtekoha riik/-regioon, päritoluriik, kaal, kogus, kogus lisaühikutes, kaup, kande kood, arvesummad ja statistilised summad.   Vajaduse korral saate andmeid muuta.  


