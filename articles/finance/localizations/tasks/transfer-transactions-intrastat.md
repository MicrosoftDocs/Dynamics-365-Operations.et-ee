---
title: Kannete ülekandmine Intrastati
description: Selles protseduuris selgitatakse, kuidas seadistada Intrastati parameetreid ja edastada kandeid Intrastati.
author: Anasyash
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c47412c8ae68b396de41f04731b841f592dcba9
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830140"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Kannete ülekandmine Intrastati

[!include [banner](../../includes/banner.md)]

Selles protseduuris selgitatakse, kuidas seadistada Intrastati parameetreid ja edastada kandeid Intrastati. Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.


## <a name="create-new-and-update-existing-commodity-code"></a>Uue kaubakoodi loomine ja olemasoleva kaubakoodi värskendamine
1. Avage navigeerimispaanil **Moodulid > Tooteteabe haldus > Häälestus > Kategooriad ja atribuudid > Kategooria hierarhiad**.
2. Leidke ja valige loendis kirje **Intrastati kaubaartiklikoodid.**
3. Klõpsake loendis valitud real olevat linki.
4. Valige puust kirje. Näiteks valige **Intrastat\Kõlar**.  
5. Klõpsake valikut **Redigeeri**.
6. Laiendage kiirkaarti **Väliskaubandus**.
7. Sisestage või valige väärtus väljale **Lisaühikud**. Näiteks valige **tk**.  
8. Valige **Jah** väljal **Kaal ei ole kohaldatav**.
9. Valige puul **Intrastat**.
10. Klõpsake **Uus kategooria sõlm**.
11. Sisestage väljale **Nimi** kauba nimi. Näiteks, sisestage **Muu kaup**.  
12. Sisestage väljale **Kood** kauba kood. Näiteks, sisestage **995 00 00**.  
13. Sisestage väärtus väljale Hüüdnimi. Näiteks, sisestage **Muu**.  
14. Klõpsake valikut **Salvesta**.
15. Sulgege leht.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Kaubakoodi määramine toote hierarhiale ja väljastatud tootele
1. Kirjete leidmiseks kasutage kiirfiltrit. Näiteks filter väljal **Nimi**, millel on **müügi** väärtus.
2. Klõpsake loendis valitud real olevat linki.
3. Laiendage puus **kategooria sõlm**. Näiteks, laiendage **Müügi hierarhia\Kodused helisüsteemid**.  
4. Valige puus **kategooria, mis määrata kaubakoodile**. Näiteks valige **Müügi hierarhia\Kodused helisüsteemid\Kõlarid.  
5. Laiendage kiirkaarti **Kaubakoodid**.
6. Klõpsake käsku **Lisa**.
7. Valige väljal **Hierarhia valik** suvand **Intrastat**.
8. Otsige loendist ja valige kaubakood. Näiteks, valige **920 20 34 Kõlar**.  
9. Klõpsake sõlme valimiseks paremnoolel.
10. Klõpsake valikut **OK**.
11. Avage navigeerimispaanil **Moodulid > Tooteteabe haldus > Tooted > Vabastatud tooted**.
12. Valige loendist väljastatud toode, mille saate määrata kauba koodile. Näiteks, valige **D0001**.  
13. Klõpsake valikut **Redigeeri**.
14. Laiendage kiirkaarti **Väliskaubandus**.
15. Sisestage väljale **Kaup** kaubakood. Näiteks, valige väärtus **920 20 34 Kõlar**.    
16. Sisestage väljale **Tasude protsent** number. Näiteks, sisestage **3**.  
17. Sisestage või valige väljale **Riik/regioon** päritoluriik või -regioon. Näiteks, valige **AUT**.  
18. Laiendage kiirkarti **Varude haldus**.
19. Sisestage väljale **Netokaal** kaal kilogrammides. Näiteks, sisestage **2,5**.  
20. Klõpsake valikut **Salvesta**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Intrastati kandekoodide ja väliskaubanduse parameetrite seadistamine
1. Avage navigeerimispaanil **Moodulid > Maks > Häälestus > Väliskaubandus > Kandekoodid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Kandekood**. Näiteks sisestage tagastusena kasutatavaks kandekoodiks **21**.  
4. Sisestage väljale **Nimi** kandekoodi nimi. Näiteks, sisestage **Tagastus**.  
5. Valige suvand väljal **Statistiline summa**. Näiteks valige **Tühi**, mis näitab, et tehingukoodiga **21** tehingute aruande statistiline väärtus on alati null.  
6. Avage navigeerimispaanil **Moodulid > Maks > Häälestus > Väliskaubandus > Väliskaubanduse parameetrid**.
7. Sisestage või valige väärtus väljale **Tehingu kood**. Näiteks, valige **11**.  
8. Sisestage või valige väärtus väljale **Kreeditarve**. See väärtus määratleb ka füüsilise tagastuse. Füüsilise tagastuse kreeditarve kantakse Intrastati töölehel vastassuunaga. Näiteks kantakse tagastustellimuse saabumine üle lähetusena.   Muidu käsitletakse kreeditarvet parandusena ja see edastatakse sama suuna ja vastasmärgiga. Näiteks edastatakse saabumise parandus negatiivse summaga saabumisena ja aktiivne lipp seadistatakse olekusse **Parandus**.  
9. Laiendage kiirkaart **Edasta**.
10. Valige **Jah** väljalt **Artiklikoodiga kaubad**. Valige see suvand, kui soovite üle kanda ainult kanded, millel on kaubaartikli kood määratud. Kaubakoodita tehinguid ei edastata Intrastati.  
11. Valige suvand väljal **Edastada, kui vastab järgmise üksuse kriteeriumile**. Näiteks, valige **Üks valitutest**.  
12. Laiendage jaotis **Kaubakoodide hierarhia**.
13. Klõpsake vahekaardil **Riigi/regiooni atribuudid**.
14. Klõpsake valikut **Uus**.
15. Sisestage või valige väärtus väljale **Riik/regioon**. Näiteks, valige väärtus **FRA**.  
16. Sisestage väljale **Intrastati kood** riigi ISO-kood.  Näiteks trükkige **FR**.  
17. Valige väljalt **Riigi/regiooni tüüp** suvand **EL**.
18. Klõpsake vahekaarti Numbriseeriad.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Tarneviiside ja Intrastatis tasude lisamise reegliste seadistamine
1. Avage navigeerimispaanilt **Moodulid > Müük ja turundus > Häälestus > Turustus > Tarneviisid**.
2. Otsige loendist ja valige soovitud kirje. Näiteks, valige **20 Air**.  
3. Laiendage kiirkaarti **Väliskaubandus**.
4. Klõpsake valikut **Redigeeri**.
5. Sisestage või valige väärtus väljale **Transport**. Näiteks, valige **02**.  
6. Avage navigeerimispaanil **Moodulid > Müügireskontro > Kulude seadistamine > Kulude kood**.
7. Kirjete leidmiseks kasutage kiirfiltrit. Näiteks filter tulude koodi väljal **veotasu** väärtusega.
8. Laiendage kiirkaarti **Väliskaubandus**.
9. Klõpsake valikut **Redigeeri**.
10. Valige **Jah** väljal **Intrastati arve väärtus**. Summa kantakse väljale **Arve kulud** ja liidetakse kokku arve summa väljal oleva ülekantud summaga. Valige **Jah** väljal **Intrastati statistiline väärtus**, kui muudatuste summa tuleb üle kanda väljale **Statistilised kulud** ja liita väljaga **Statistiline summa**.  

## <a name="sell-products-for-eu-customers"></a>Toodete müümine EL-i klientidele
1. Avage navigeerimispaanil **Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.
2. Klõpsake valikut **Uus**.
3. Valige väljalt **Kliendi konto** EL-i klient. Näiteks, valige **DE-012 Litware Retail**.  
4. Laiendage kiirkaarti **Tarne**.
5. Sisestage või valige väärtus väljale **Tarneviis**. Näiteks, valige **20 Air**.  
6. Klõpsake valikut **OK**.
7. Valige müügitellimuste ridade esimene rida.
8. Sisestage või valige väärtus väljale **Kauba kood**. Näiteks, valige **D001**.  
9. Laiendage kiirkaarti **Rea üksikasjad**.
10. Klõpsake vahekaarti **Väliskaubandus**.Transport täidetakse valitud tarneviisi põhjal automaatselt.  
11. Sisestage või valige väärtus väljale **Port**.
12. Klõpsake valikut **Finantsid**. Vastavalt seadistustele sisaldub see summa **Intrastati arve väärtuses**.  
13. Klõpsake valikul **Tasude haldamine**.
14. Sisestage või valige väärtus väljale **Kulude kood**. Näiteks, valige **VEOTASU**.  
15. Valige märkeruut **Säilita**.
16. Sisestage arv väljale **Tasude väärtus**. Näiteks, sisestage **10**.  
17. Klõpsake valikut **Salvesta**.
18. Sulgege leht.
19. Klõpsake toimingupaanil valikut **Arve**.
20. Klõpsake **Arve**.
21. Laiendage jaotist **Parameetrid**.
22. Valige väljal **Kogus** suvand **Kõik**.
23. Laiendage kiirkaarti **Häälestus**.
24. Sisestage kuupäev väljale **Arve kuupäev**. Näiteks, sisestage **2015-01-31**.  
25. Klõpsake valikut **OK**.
26. Klõpsake valikut **OK**.
27. Sulgege leht.
28. Klõpsake valikut **Uus**.
29. Valige väljalt **Kliendi konto** EL-i klient. Näiteks, valige **DE-013 Trey Wholesales**.
30. Klõpsake valikut **OK**.
31. Sisestage või valige väärtus väljale **Kauba kood**. Näiteks, valige **D0001**.  
32. Klõpsake valikut **Salvesta**.
33. Klõpsake **Arve**.
34. Sisestage kuupäev väljale **Arve kuupäev**. Näiteks, sisestage kuupäev **2015-01-31**.  
35. Klõpsake valikut **OK**.
36. Klõpsake valikut **OK**.

## <a name="transfer-transactions-to-the-intrastat"></a>Kannete ülekandmine Intrastati
1. Avage navigeerimispaanil **Moodulid > Maks > Deklaratsioonid > Väliskaubandus > Intrastat**.
2. Klõpsake **Edasta**.
3. Valige **Jah** väljal **Kliendiarve**.
4. Klõpsake käsku **Filtreeri**.
5. Märgistage loendis rida **Kuupäev**.
6. Sisestage väärtus väljale **Kriteerium**. Sisestage näiteks filter perioodile jaanuar 2015 (täpne väärtus oleneb teie kuupäevavormingust): 01.01.2015..31.01.2015  
7. Klõpsake valikut **OK**.
8. Klõpsake valikut **OK**.
9. Otsige ja valige loendist edastatud kirje.
10. Klõpsake vahekaarti **Üldine**.
    
Vaadake üle edastatud andmed, sh sihtkoha/lähtekoha riik/-regioon, päritoluriik, kaal, kogus, kogus lisaühikutes, kaup, kande kood, arvesummad ja statistilised summad. Vajaduse korral saate andmeid muuta.  

