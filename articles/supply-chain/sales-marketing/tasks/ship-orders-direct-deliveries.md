---
title: Tellimuste lähetamine otsetarnetena
description: Selles teemas näidatakse, kuidas luua müügitellimuse otsetarnet.
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31cb26479ccb74dfb58fd5590cd60d7b7c64c292
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426673"
---
# <a name="ship-orders-as-direct-deliveries"></a>Tellimuste lähetamine otsetarnetena

[!include [banner](../../includes/banner.md)]

Selles teemas näidatakse, kuidas luua müügitellimuse otsetarnet. Otsetarnet kasutatakse siis, kui soovite saata kaubad kliendile otse oma hankijalt, ilma et tarniksite need esmalt oma lattu. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Teise alamülesande „Loo töölaualt otsetarneid” edukaks lõpuleviimiseks veenduge, et kaubal, mille müügitellimuselt valite, on väljastatud tooteetaloni kiirkaardil Ost määratud vaikehankija.

## <a name="set-an-individual-order-for-direct-delivery"></a>Eraldi otsetarne tellimuse määramine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Sisestage või valige väärtus väljale **Kliendi konto**, seejärel valige **OK**
4. Sisestage või valige väärtused väljadel **Üksuse number** ja **Sait**, seejärel valige **Salvesta**.
5. Valige toimingupaanil **Müügitellimus**, seejärel valige **Otsetarne**. Lehel Tarne loomine on kõik avatud müügitellimuse read müügitellimuselt kopeeritud kujul. Saate vaadata tellimuse üksikasju ja vajaduse korral muuta üksikasju nagu ostu kogus ja hinnatingimused, enne otsetarne loomist.  
6. Valige **Jah** väljal **Kaasa kõik**.
    - Kui soovite luua otsetarne ainult müügitellimuse ridade alamkogumile, valige need eraldi.  
    - Väli **Hankija konto** võib juba hankija numbrit sisaldada või mitte sisaldada. Kui tootele on (seotud kauba laovarudes) seadistatud vaikehankija, kopeeritakse reale see hankija. Vastasel korral tuleb hankija sisestada käsitsi. Selles näites valime järgmises etapis uue hankija, isegi juhul, kui mõni on juba lisatud.   
7. Sisestage või valige väärtus väljale **Hankija konto**, seejärel valige **OK** Saate teate, et ostutellimus on nüüd loodud.   
8. Laiendage jaotist **Rea üksikasjad**.
9. Valige vahekaart **Tarne** ja kontrollige, et väli **Otsetarne** oleks määratud olekusse **Jah**.
10. Valige toimingupaanil **Üldine**.
11. Valige **Seotud tellimused**.
12. Valige link väljal **Ostutellimus**.
13. Laiendage jaotist **Rea üksikasjad** ja valige vahekaart **Aadress**.
    - Selle ostutellimuse rea tarneaadress on kliendi tarneaadress ja mitte teie ettevõtte aadress.  
    - Kui muudate tarneaadressi ostutellimuse real või algse müügitellimuse real, muudetakse automaatselt vastava tellimuse rea aadressi.  
14. Valige vahekaart **Tarne**.
    - Sarnaselt müügitellimuse reale on ka seotud ostutellimuse rea tüübiks määratud Otsetarne.  
    - Ostutellimuse rea tarnekuupäevaks ja kinnitatud tarnekuupäevaks on määratud vastavalt nõutav sissetulekukuupäev ja algse müügitellimuse rea kinnitatud sissetulekukuupäev.   
    - Kui neid kuupäevi ostu- või müügireal muudate, muudetakse automaatselt vastava tellimuse kuupäevi.     
    - Ostutellimus, mille järgi tarnitakse kaup otse kliendile, on seotud algse müügitellimusega erilise seostamise teel. See seos kehtestab reegli, et müügitellimuse saatelehte ei saa uuendada müügitellimuselt endalt ning seda tuleb teha ostutellimuse abil. Kuid arve tuleb esitada kliendile müügitellimuselt.  
15. Valige toimingupaanil **Ostmine**.
16. Valige **Kinnitus**.
17. Valige nupp **OK**.
18. Valige toimingupaanil **Vastuvõtmine**.
19. Valige **Toote sissetulek**.
20. Sisestage väärtus väljale **Toote sissetulek**.
21. Valige nupp **OK**.
22. Valige toimingupaanil **Üldine**.
23. Valige **Seotud tellimused** ja tõstke esile soovitud kirje.
    - Pärast ostutellimuse vastuvõetuks märkimist (teisisõnu: pärast seda, kui hankija on saatnud kauba teie kliendi aadressile) määratakse algse müügitellimuse olekuks automaatselt Tarnitud.  
    - Nüüd saab müügitellimuse eest arve esitada.    
24. Valige nupp **OK**.
25. Sulgege leht.
26. Valige nupp **OK**. Sulgege leheküljed ja naaske avalehele.

## <a name="create-direct-deliveries-from-the-workbench"></a>Otsetarnete loomine töölaualt
1. Avage **Navigeerimine > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Sisestage või valige väärtus väljale **Kliendi konto**, seejärel valige **OK**
4. Sisestage või valige väärtused väljadel **Kauba kood** ja **Sait**.
5. Laiendage jaotist **Rea üksikasjad** ja seejärel valige vahekaart **Tarne**.Selle asemel, et luua müügitellimuste töötlemise osana otsetarne, nagu eelmises protseduuris, võite selle ülesande ostuspetsialistile üle anda. Müügitellimuse rea lisamiseks otsetarne käsitsusprotsessi tuleb märkida rida otsetarneks.  
6. Valige **Jah** väljal **Otsetarne**.
    - Kaup on juba vaikimisi otsetarneks seadistatud; väljale määratakse tellimuse rea sisestamisel automaatselt valik Jah. Saate seadistada kauba otsetarneks väljastatud toote etalonile, määrates otsetarne valikuks Jah ja valides otsetarne vaikelao.  
    - Kuna seda ostutellimust ei ole veel loodud, on otsetarne olekuks määratud „Tarnitakse otse“.   
7. Valige käsk **Salvesta**.
8. Sulgege leheküljed, kuni naasete avalehele.
9. Sisestage otsinguribale `Direct delivery`.
    - Otsetarne leht toimib töölauana, mis annab ostuagendile ülevaate kõigist müügitellimuse ridadest, mis tuleb otse tarnida, ja võimaldab tal koostada vastavaid ostutellimusi. Lisaks saab ta vaadata avatud otsetarne tellimusi ja kinnitatud tellimusi vahekaartidel Kinnitus ja Tarne.  
    - Pärast otsetarne tellimuse koostamist teisaldatakse see automaatselt vahekaardile Kinnitus. Saate kinnitada tellimuse otse sellelt lehelt. Kui ost on kinnitatud, teisaldatakse see automaatselt vahekaardile Tarne, millelt saate registreerida selle sissetuleku.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]