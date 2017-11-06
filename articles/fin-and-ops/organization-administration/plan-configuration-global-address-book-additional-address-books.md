---
title: "Globaalse aadressiraamatu ja täiendavate aadressiraamatute konfigureerimise plaan"
description: "Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui Microsoft Dynamics 365 for Finance and Operationsis globaalse aadressiraamatu ning mis tahes täiendava aadressiraamatu seadistate ja konfigureerite. Mõned otsused nõuavad toote mõnes muus valdkonnas (nt organisatsiooni hierarhia) tehtud otsuste kinnitamist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>Globaalse aadressiraamatu ja täiendavate aadressiraamatute konfigureerimise plaan

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui Microsoft Dynamics 365 for Finance and Operationsis globaalse aadressiraamatu ning mis tahes täiendava aadressiraamatu seadistate ja konfigureerite. Mõned otsused nõuavad toote mõnes muus valdkonnas (nt organisatsiooni hierarhia) tehtud otsuste kinnitamist.

<a name="global-address-book"></a>Globaalne aadressiraamat
-------------------

Enne kui alustate tööd globaalse aadressiraamatuga, peate määratlema selle jaoks vaikeväärtused. Neid vaikeväärtusi kasutatakse siis kõigi täiendavate aadressiraamatute puhul, mille loote. 

**Otsused.**

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

Saate luua aadressiraamatuid igal ajal ja määrata igal ajal aadressiraamatutele ka turbeparameetreid. Teilt ei nõuta, et määraksite aadressiraamatule turbeprivileegid, kuid kui te seda ei tee, saavad kõik teie organisatsiooni töötajad vaadata kõiki osapoole kirjeid selles aadressiraamatus. Osapoole kirjete turbeprivileege saab määrata aadressiraamatute kaudu. Turbeprivileegid põhinevad töörühmadel. See lähenemine tagab, et aadressiraamatus olevaid osapoole kirjeid saavad vaadata ainult need töötajad, kes on määratud töörühma, millel on aadressiraamatule juurdepääs. Peate valima töörühmad, millel on juurdepääs igale aadressiraamatule. Saate määrata igale aadressiraamatule turbeprivileegid, mis annavad või keelavad juurdepääsu konkreetsete töörühmade jaoks. Kui annate töörühmale aadressiraamatu privileegid, saavad kõik selle töörühma liikmed vaadata selle aadressiraamatu kirjeid. Kui te ei anna töörühmale aadressiraamatu privileege, ei saa selle töörühma liikmed seda aadressiraamatut ega selle sisu vaadata. 

**Otsus.**

-   Millistel töörühmadel peaks olema juurdepääs igale teie loodavale uuele aadressiraamatule?




