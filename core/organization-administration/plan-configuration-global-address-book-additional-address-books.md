---
title: Seadistada globaalse aadressiraamatud
description: "Selles artiklis kirjeldatakse kaalutlused ja otsuseid, mida peate projekteerimise käigus, enne seadistada ja konfigureerida Microsoft Dynamics 365 operatsioonide globaalse ja täiendavad aadressiraamatud. Mõned otsused nõuavad toote mõnes muus valdkonnas (nt organisatsiooni hierarhia) tehtud otsuste kinnitamist."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: abd9ec44530522657f758b35e8f987aa92c3b0e3
ms.lasthandoff: 03/31/2017


---

# <a name="configure-global-address-books"></a>Seadistada globaalse aadressiraamatud

Selles artiklis kirjeldatakse kaalutlused ja otsuseid, mida peate projekteerimise käigus, enne seadistada ja konfigureerida Microsoft Dynamics 365 operatsioonide globaalse ja täiendavad aadressiraamatud. Mõned otsused nõuavad toote mõnes muus valdkonnas (nt organisatsiooni hierarhia) tehtud otsuste kinnitamist.

<a name="global-address-book"></a>Globaalne aadressiraamat
-------------------

Enne kui alustate tööd globaalse aadressiraamatuga, peate määratlema selle jaoks vaikeväärtused. Neid vaikeväärtusi kasutatakse siis kõigi täiendavate aadressiraamatute puhul, mille loote. **Otsused.**

-   Millises järjekorras tuleks nimed kuvada osapoolekirjete puhul tüübiga **Isik**? Näiteks üks järjekord oleks perekonnanimi, teine eesnimi ja eesnimi.
-   Kas osapoolekirjed tuleks aadressiraamatust kustutada, kui rolli kirje kustutatakse? Näiteks kui kliendi kirje kustutatakse, kas osapoole kirje tuleks samuti kustutada?
-   Kas uue kirje loomisel tuleks kasutajaid teavitada, kui globaalsest aadressiraamatust leitakse topeltkirje?
-   Kas osapoole kirje andmetesse tuleks lisada andmete universaalse nummerdussüsteemi (DUNS) number?
-   Kui DUNS-number on osapoole kirjele lisatud, kas siis tuleks kontrollida numbri kordumatust?
-   Kas soovite globaalses aadressiraamatus osapoole kirje loomisel kasutada osapoole tüübi, isiku või organisatsiooni vaikeväärtust?
-   Millistel kasutajarollidel peaks olema juurdepääs osapoole kirjete era-aadressidele ja kontaktandmetele?

## <a name="additional-address-books"></a>Täiendavad aadressiraamatud
Pärast globaalse aadressiraamatu loomist, saate luua vajaduse järgi täiendavaid aadressiraamatuid, näiteks eraldi aadressiraamatu iga ettevõtte jaoks oma organisatsioonis või iga tegevusala jaoks. Näiteks Fabrikam on rahvusvaheline organisatsioon, millel on mitu ettevõtet ja mitu tegevusala. Fabrikam plaanib luua iga tegevusala jaoks aadressiraamatu. Tegevusaladele, millel on mitu asukohta (nt pneumaatiliste tööriistade äri), plaanib Fabrikam luua iga asukoha jaoks aadressiraamatu. Chris, Fabrikami IT-juht, on loonud järgmise loendi vajalikest aadressiraamatutest. Selles loendis kirjeldatakse ka osapoole kirjeid, mida iga aadressiraamat peab sisaldama.

-   **Avaliku sektori lepingud (PubSC)** – kõigi Fabrikami sõlmitud avaliku sektori lepingute kõigi osapoolte kirjed.
-   **Erasektori lepingud (PriSC)** – kõigi Fabrikami sõlmitud erasektori lepingute kõigi osapoolte kirjed.
-   **Elektroonilised tööriistad (ET)** – kõigi elektrooniliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-Japan pakutavate või ostetavate elektrooniliste tööriistadega kokku puutuvad.
-   **Pneumaatilised tööriistad (andmete universaalse nummerdussüsteem)** – kõigi pneumaatiliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-Japan pakutavate või ostetavate pneumaatiliste tööriistadega kokku puutuvad.
-   **Pneumaatilised tööriistad (PTUSA)** – kõigi pneumaatiliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-US pakutavate või ostetavate pneumaatiliste tööriistadega kokku puutuvad.

**Otsus.**

-   Mitu täiendavat aadressiraamatut loote?

### <a name="address-book-security"></a>Aadressiraamatu turve

Saate luua aadressiraamatuid igal ajal ja määrata igal ajal aadressiraamatutele ka turbeparameetreid. Teilt ei nõuta, et määraksite aadressiraamatule turbeprivileegid, kuid kui te seda ei tee, saavad kõik teie organisatsiooni töötajad vaadata kõiki osapoole kirjeid selles aadressiraamatus. Osapoole kirjete turbeprivileege saab määrata aadressiraamatute kaudu. Turbeprivileegid põhinevad töörühmadel. See lähenemine tagab, et aadressiraamatus olevaid osapoole kirjeid saavad vaadata ainult need töötajad, kes on määratud töörühma, millel on aadressiraamatule juurdepääs. Peate valima töörühmad, millel on juurdepääs igale aadressiraamatule. Saate määrata igale aadressiraamatule turbeprivileegid, mis annavad või keelavad juurdepääsu konkreetsete töörühmade jaoks. Kui annate töörühmale aadressiraamatu privileegid, saavad kõik selle töörühma liikmed vaadata selle aadressiraamatu kirjeid. Kui te ei anna töörühmale aadressiraamatu privileege, ei saa selle töörühma liikmed seda aadressiraamatut ega selle sisu vaadata. **Otsus.**

-   Millistel töörühmadel peaks olema juurdepääs igale teie loodavale uuele aadressiraamatule?



