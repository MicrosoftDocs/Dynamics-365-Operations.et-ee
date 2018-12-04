--- 
title: "Min-max täiendamisprotsessi seadistamine"
description: "Selles protseduuris kirjeldatakse, kuidas seadistada uut täiendamisprotsessi, mis kasutab minimaalse/maksimaalse täiendamise strateegiat."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>Min-max täiendamisprotsessi seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris kirjeldatakse, kuidas seadistada uut täiendamisprotsessi, mis kasutab minimaalse/maksimaalse täiendamise strateegiat. Kui varud jäävad allapoole minimaalset taset, luuakse töö asukoha täiendamiseks. Protseduur näitab ka seda, kuidas kasutada fikseeritud komplekteerimise asukohti, et lubada uuesti täiendamist isegi siis, kui varud jäävad allapoole minimaalset taset, ja, kuidas lubada täiendamisprotsessi regulaarset käitamist, kasutades pakett-tööd. Neid ülesandeid täidab üldjuhul laohaldur. Saate seda protseduuri käitada demoandmete ettevõttes USMF, kasutades märkustes olevaid näiteväärtusi, või käitada seda oma andmetega. Kui kasutate oma andmeid, veenduge, et teil on ladu, mis on laohaldusprotsessideks lubatud.


## <a name="create-a-fixed-picking-location"></a>Fikseeritud komplekteerimise asukoha loomine
1. Avage Laohaldus > Seadistus > Ladu > Fikseeritud asukohad.
    * See on valikuline ülesanne miinimumi-maksimumi täiendamiseks, kuid kui kasutate fikseeritud komplekteerimise asukohta, võimaldab see varude täiendamist, isegi kui see langeb allapoole minimaalset taset, kuna süsteem suudab määrata, milliseid kaupu on vaja täiendada, isegi, kui ühtki kaupa pole alles.  
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Kaubakood.
    * USMF-i kasutamisel saate valida kauba A0001.  
4. Sisestage või valige väärtus väljal Koht.
    * Kui te kasutate USMF-i, saate valida tegevuskoha 2.  
5. Sisestage või valige väärtus väljal Ladu.
    * Kui kasutate USMF-i, saate valida lao 24.  
6. Sisestage või valige väärtus väljal Asukoht.
    * Kui kasutate USMF-i, saate teha valiku CP-003.  
7. Sulgege leht.

## <a name="create-a-replenishment-location-directive"></a>Täiendamise asukohakorralduse loomine
1. Avage Laohaldus > Seadistus > Asukohakorraldused.
    * Asukohakorraldusi kasutatakse, et määrata, kus tuleb kaubad täiendamisprotsessiks komplekteerida.  
2. Tehke väljal Töötellimuse tüüp valik Täiendamine.
3. Klõpsake valikut Uus.
4. Sisestage väärtus väljale Nimi.
5. Tehke väljal Töö tüüp valik Komplekteeri.
6. Sisestage või valige väärtus väljal Koht.
    * Kui te kasutate USMF-i, saate valida tegevuskoha 2.  
7. Sisestage või valige väärtus väljal Ladu.
    * Kui kasutate USMF-i, saate valida lao 24.  
8. Klõpsake nuppu Salvesta.
9. Klõpsake valikut Uus.
10. Märkige loendis valitud rida.
11. Sisestage number väljale Kuni koguseni.
    * Näiteks saate määrata väärtuseks 9999.  
12. Valige märkeruut Luba tükeldamine.
    * Kui valite selle suvandi, lubab töö loomise protsess töö rea koguste tükeldamist mitme asukoha vahel.  
13. Klõpsake nuppu Salvesta.
14. Klõpsake valikut Uus.
15. Märkige loendis valitud rida.
16. Sisestage väärtus väljale Nimi.
17. Klõpsake nuppu Salvesta.
18. Klõpsake suvandit Redigeeri päringut.
    * Saate seda päringut redigeerida piirangute lisamiseks juhul, kui varusid saab valida täiendamisprotsessis. Näiteks võib juhtuda, et tuleb kasutada varusid ainult lao hulgialalt.  
19. Klõpsake nuppu OK.
20. Sulgege leht.

## <a name="create-a-replenishment-work-template"></a>Täiendamise töömalli loomine
1. Avage Laohaldus > Seadistus > Töö > Töömallid.
    * Töömalli kasutatakse selleks, et juhendada süsteemi, kuidas tuleb min/max-täiendustööd luua. Minimaalselt peab olema töömalli rida komplekteerimiseks ja paigutamiseks. Töömalli kohta öeldakse, et see on kehtetu, kuni kogu vajalik teave on sisestatud.  
2. Tehke väljal Töötellimuse tüüp valik Täiendamine.
3. Klõpsake valikut Uus.
4. Sisestage väärtus väljale Töömall.
5. Klõpsake nuppu Salvesta.
6. Klõpsake valikut Uus.
7. Tehke väljal Töö tüüp valik Komplekteeri.
8. Sisestage või valige väärtus väljal Tööklassi ID.
    * See peaks olema tööklass, mis on seotud varude täiendamisega. Kui kasutate USMF-i, tehke valik Täienda.  
9. Klõpsake valikut Uus.
10. Märkige loendis valitud rida.
11. Valige väljal Töö tüüp suvand Pane.
12. Sisestage või valige väärtus väljal Tööklassi ID.
13. Klõpsake nuppu Salvesta.
14. Sulgege leht.

## <a name="create-a-new-replenishment-template"></a>Uue täiendamismalli loomine
1. Avage Laohaldus > Seadistus > Täiendamine > Täiendamise mallid.
    * Täiendamismalli kasutatakse selleks, et määratleda kaubad ja kogused ning täiendamise asukoht.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Täiendamismall.
    * Andke mallile nimi, mis näitab, et see on mõeldud min/max-täiendamiseks.  
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige märkeruut Voo nõudel reserveerimata koguste kasutamise lubamine.
    * Kui valite selle suvandi, võimaldab see voo nõudluse täiendamisel tarbida koguseid, mis on seotud min/max-täiendamisega. Näiteks võib see olla kasulik, kui min/max-täiendustööd ei tehta kohe, et vältida soovimatute nõudluse täiendustööde loomist.  
6. Klõpsake valikut Uus.
7. Sisestage number väljale Seerianumber.
8. Sisestage väljale Kirjeldus soovitud väärtus.
9. Märkige loendis valitud rida.
10. Sisestage või valige väärtus väljal Täiendamise ühik.
    * Valige näiteks tk. See säte on kohustuslik. See võimaldab teil määrata täiendamistööle erinevad mõõtühikud võrreldes ühikuga, mis on määratud selle malli minimaalse ja maksimaalse laoseisu tasemetele.  
11. Sisestage või valige väärtus väljal Töömall.
    * Valige töömall, mille lõite varem.  
12. Sisestage number väljale Miinimumkogus.
    * Valige miinimumkogus, mis peaks täiendamise käivitama. Määrake väärtuseks näiteks 50. On võimalik jätta selleks väärtuseks null, kui täiendate fikseeritud asukohta ja kui suvand Täienda varusid tühjades fikseeritud asukohtades on seatud väärtusele Jah. Samuti soovitame valida suvandi Täienda varusid ainult fikseeritud asukohtades jõudluspõhjustel.  
13. Sisestage number väljale Maksimumkogus.
    * Valige väärtuseks näiteks 100.  
14. Sisestage või valige väärtus väljal Ühik.
    * Määrake ühik minimaalsetele ja maksimaalsetele kogustele. Näiteks saate määrata selleks tk.  
15. Valige märkeruut Täienda varusid tühjades fikseeritud asukohtades.
    * Valige see märkeruut, et täiendada fikseeritud asukohti, kui need on tühjad. Vastasel juhul täidetakse ainult asukohti, kus on laokogus olemas.  
16. Valige märkeruut Täienda varusid ainult fikseeritud asukohtades.
17. Klõpsake suvandit Vali tooted.
    * See on koht, kus määratleda, milliseid tooteid tuleb täiendada. Kui valitud on suvand Fikseeritud komplekteerimiskohad, peate määratlema ka selle päringu asukohad. Saadaval on nii variandipõhised kui ka tootepõhised päringud.  
18. Valige suvand Kaupade rida.
19. Sisestage väärtus väljale Kriteeriumid.
    * Valige kaubad, mida tuleks täiendada fikseeritud asukohtades. Tippige näiteks tüüp A*, et valida kõik kauba numbrid, mis algavad tähega A.  
20. Klõpsake vahekaarti Lisa.
    * Lisage asukoha üksus (välja arvatud juhul, kui see on juba olemas), et piirata täiendustööd fikseeritud komplekteerimiskohtedega teatud laoalal.  
21. Märkige loendis valitud rida.
22. Määrake välja Tabel olekuks Asukohad.
23. Tehke väljal Väli valik Asukoha profiili ID.
24. Sisestage või valige väärtus väljal Kriteeriumid.
25. Klõpsake nuppu OK.
26. Sulgege leht.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Täiendamisprotsessi pakett-tööna käitamise seadistamine
1. Avage Laohaldus > Täiendamine > Täiendamised.
    * Lehel Täiendused saate seadistada täiendamise käitamise pakett-tööna või nõuda, et see käivitataks käsitsi.  
2. Klõpsake käsku Filtreeri.
3. Märkige loendis valitud rida.
4. Sisestage või valige väärtus väljal Kriteeriumid.
5. Klõpsake nuppu OK.
6. Laiendage jaotist Käivita taustal.
7. Määrake suvandi Pakktöötlus väärtuseks Jah.
8. Klõpsake valikut Korduvus.
9. Valige suvand Lõppkuupäev puudub.
10. Määrake kordumismuster.
    * Valige näiteks päevad.  
11. Klõpsake nuppu OK.
12. Klõpsake nuppu OK.


