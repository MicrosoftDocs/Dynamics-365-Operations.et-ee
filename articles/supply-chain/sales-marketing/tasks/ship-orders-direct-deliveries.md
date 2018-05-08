--- 
title: "Tellimuste lähetamine otsetarnetena"
description: "Selles protseduuris näitlikustatakse, kuidas müügitellimuse jaoks otsetarnet luua."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Tellimuste lähetamine otsetarnetena

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näitlikustatakse, kuidas müügitellimuse jaoks otsetarnet luua. Otsetarnet kasutatakse siis, kui soovite saata kaubad kliendile otse oma hankijalt, ilma et tarniksite need esmalt oma lattu. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Teise alamülesande „Loo töölaualt otsetarneid” edukaks lõpuleviimiseks veenduge, et kaubal, mille müügitellimuselt valite, on väljastatud tooteetaloni kiirkaardil Ost määratud vaikehankija.


## <a name="set-an-individual-order-for-direct-delivery"></a>Eraldi otsetarne tellimuse määramine
1. Avage Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
    * Kui kasutate USMF-i, saate valida konto US-001.  
4. Klõpsake nuppu OK.
5. Sisestage või valige väärtus väljal Kaubakood.
    * USMF-i kasutamisel saate valida kauba T0020.  
6. Klõpsake nuppu Salvesta.
7. Klõpsake toimingupaanil valikut Müügitellimus.
8. Klõpsake valikut Otsetarne.
    * Lehel Tarne loomine on kõik avatud müügitellimuse read müügitellimuselt kopeeritud kujul. Saate vaadata tellimuse üksikasju ja vajaduse korral muuta üksikasju nagu ostu kogus ja hinnatingimused, enne otsetarne loomist.  
9. Valige väljal Kaasa kõik väärtus Jah.
    * Kui soovite luua otsetarne ainult müügitellimuse ridade alamkogumile, valige need eraldi.  
    * Hankija konto väljal võib juba olla või mitte olla hankija number. Kui tootele on (seotud kauba laovarudes) seadistatud vaikehankija, kopeeritakse reale see hankija. Vastasel korral tuleb hankija sisestada käsitsi. Selles näites valime järgmises sammus uue hankija, isegi juhul, kui mõni on juba lisatud.   
10. Sisestage väärtus väljale Hankija konto või valige see.
    * Kui kasutate USMF-i, saate valida konto 1001.  
11. Klõpsake nuppu OK.
    * Saate teate, et ostutellimus on nüüd loodud.   
12. Laiendage jaotis Rea üksikasjad.
13. Klõpsake vahekaarti Tarne.
    * Otsetarne välja väärtuseks on nüüd määratud Jah.  
    * Otsetarne olek näitab koostatud ostutellimust.   
14. Klõpsake toimingupaanil valikut Üldine.
15. Klõpsake valikut Seotud tellimused.
16. Klõpsake, et järgida linki väljal Ostutellimus.
17. Laiendage jaotis Rea üksikasjad.
18. Klõpsake vahekaarti Aadress.
    * Pange tähele, et selle ostutellimuse rea tarneaadress on kliendi tarneaadress ja mitte teie ettevõtte aadress.  
    * Kui muudate tarneaadressi ostutellimuse real või algse müügitellimuse real, muudetakse automaatselt vastava tellimuse rea aadressi.  
19. Klõpsake vahekaarti Tarne.
    * Sarnaselt müügitellimuse reale on ka seotud ostutellimuse rea tüübiks määratud Otsetarne.  
    * Ostutellimuse rea tarnekuupäevaks ja kinnitatud tarnekuupäevaks on määratud vastavalt nõutav sissetulekukuupäev ja algse müügitellimuse rea kinnitatud sissetulekukuupäev.   
    * Kui neid kuupäevi ostu- või müügireal muudate, muudetakse automaatselt vastava tellimuse kuupäevi.     
    * Ostutellimus, mis on määratud edastama kaupu otse kliendile, on seotud algse müügitellimusega erilise seose abil. See seos kehtestab reegli, et müügitellimuse saatelehte ei saa uuendada müügitellimuselt endalt ning seda tuleb teha ostutellimuse abil. Kuid arve tuleb esitada kliendile müügitellimuselt.  
20. Klõpsake toimingupaanil valikut Ost.
21. Klõpsake suvandit Kinnitus.
22. Klõpsake nuppu OK.
23. Klõpsake toimingupaanil valikut Vastuvõtt.
24. Klõpsake valikut Toote sissetulek.
25. Sisestage väärtus väljale Toote sissetulek.
26. Klõpsake nuppu OK.
27. Klõpsake toimingupaanil valikut Üldine.
28. Klõpsake valikut Seotud tellimused.
29. Märkige loendis valitud rida.
    * Pärast ostutellimuse vastuvõetuks märkimist (teisisõnu: pärast seda, kui hankija on saatnud kauba teie kliendi aadressile) määratakse algse müügitellimuse olekuks automaatselt Tarnitud.  
    * Nüüd saab müügitellimuse eest arve esitada.    
30. Klõpsake nuppu OK.
31. Sulgege leht.
32. Klõpsake nuppu OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Otsetarnete loomine töölaualt
1. Sulgege leht.
2. Sulgege leht.
3. Avage Kõik müügitellimused.
4. Klõpsake valikut Uus.
5. Valige või sisestage väärtus väljal Kliendi konto.
6. Klõpsake nuppu OK.
7. Sisestage või valige väärtus väljal Kaubakood.
8. Laiendage jaotis Rea üksikasjad.
9. Klõpsake vahekaarti Tarne.
    * Selle asemel, et luua müügitellimuse töötlemise käigus otsetarne (nagu eelmises protseduuris) võite otsustada anda selle ülesande edasi ostuspetsialistile. Müügitellimuse rea lisamiseks otsetarne käsitsusprotsessi tuleb märkida rida otsetarneks.  
10. Tehke väljal Otsetarne valik Jah.
    *   Kaup on juba vaikimisi otsetarneks seadistatud; väljale määratakse tellimuse rea sisestamisel automaatselt valik Jah. Saate seadistada kauba otsetarneks väljastatud toote etalonile, määrates otsetarne valikuks Jah ja valides otsetarne vaikelao.  
    * Kuna ostutellimust pole veel koostatud, on otsetarne olekuks määratud Tarnitakse otse.   
11. Sulgege leht.
12. Sulgege leht.
13. Minge jaotisse Otsetarne.
    * Otsetarne leht toimib töölauana, mis annab ostuagendile ülevaate kõigist müügitellimuse ridadest, mis tuleb otse tarnida, ja võimaldab tal koostada vastavaid ostutellimusi. Lisaks saab ta vaadata avatud otsetarne tellimusi ja kinnitatud tellimusi vahekaartidel Kinnitus ja Tarne.   
14. Klõpsake valikut Loo otsetarne.
15. Klõpsake vahekaarti Kinnitus.
    * Pärast otsetarne tellimuse koostamist teisaldatakse see automaatselt vahekaardile Kinnitus. Saate kinnitada tellimuse otse sellelt lehelt. Kui ost on kinnitatud, teisaldatakse see automaatselt vahekaardile Tarne, millelt saate registreerida selle sissetuleku.  


