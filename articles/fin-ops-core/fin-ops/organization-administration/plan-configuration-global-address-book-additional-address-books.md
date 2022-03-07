---
title: Globaalse aadressiraamatu ja muude aadressiraamatute plaanimine
description: Selles teemas kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b3f6a74c217b0cc7cec784ca6a964ab2caae0c7e9438aee2cc82987a508d63
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771892"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Plaan globaalse aadressiraamatu ja muude aadressiraamatute jaoks

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui globaalse aadressiraamatu ning mis tahes täiendava aadressiraamatu seadistate ja konfigureerite. Mõned otsused nõuavad toote mõnes muus valdkonnas (nt organisatsiooni hierarhia) tehtud otsuste kinnitamist.

## <a name="global-address-book"></a>Globaalne aadressiraamat

Enne kui alustate tööd globaalse aadressiraamatuga, peate määratlema selle jaoks vaikeväärtused. Neid vaikeväärtusi kasutatakse siis kõigi täiendavate aadressiraamatute puhul, mille loote.

**Otsused**

- Millises järjekorras tuleks nimed kuvada osapoolekirjete puhul tüübiga **Isik**? Näiteks üks järjekord oleks perekonnanimi, teine eesnimi ja eesnimi.
- Kas osapoolekirjed tuleks aadressiraamatust kustutada, kui rolli kirje kustutatakse? Näiteks kui kliendi kirje kustutatakse, kas osapoole kirje tuleks samuti kustutada?
- Kas uue kirje loomisel tuleks kasutajaid teavitada, kui globaalsest aadressiraamatust leitakse topeltkirje?
- Kas osapoole kirje andmetesse tuleks lisada andmete universaalse nummerdussüsteemi (DUNS) number?
- Kui DUNS-number on osapoole kirjele lisatud, kas siis tuleks kontrollida numbri kordumatust?
- Kas soovite globaalses aadressiraamatus osapoole kirje loomisel kasutada osapoole tüübi, isiku või organisatsiooni vaikeväärtust?
- Millistel kasutajarollidel peaks olema juurdepääs osapoole kirjete era-aadressidele ja kontaktandmetele?

## <a name="additional-address-books"></a>Täiendavad aadressiraamatud

Pärast globaalse aadressiraamatu loomist, saate luua vajaduse järgi täiendavaid aadressiraamatuid, näiteks eraldi aadressiraamatu iga ettevõtte jaoks oma organisatsioonis või iga tegevusala jaoks. Näiteks Fabrikam on rahvusvaheline organisatsioon, millel on mitu ettevõtet ja mitu tegevusala. Fabrikam plaanib luua iga tegevusala jaoks aadressiraamatu. Tegevusaladele, millel on mitu asukohta (nt pneumaatiliste tööriistade äri), plaanib Fabrikam luua iga asukoha jaoks aadressiraamatu. Chris, Fabrikami IT-juht, on loonud järgmise loendi vajalikest aadressiraamatutest. Selles loendis kirjeldatakse ka osapoole kirjeid, mida iga aadressiraamat peab sisaldama.

- **Avaliku sektori lepingud (PubSC)** – kõigi Fabrikami sõlmitud avaliku sektori lepingute kõigi osapoolte kirjed.
- **Erasektori lepingud (PriSC)** – kõigi Fabrikami sõlmitud erasektori lepingute kõigi osapoolte kirjed.
- **Elektroonilised tööriistad (ET)** – kõigi elektrooniliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-Japan pakutavate või ostetavate elektrooniliste tööriistadega kokku puutuvad.
- **Pneumaatilised tööriistad (andmete universaalse nummerdussüsteem)** – kõigi pneumaatiliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-Japan pakutavate või ostetavate pneumaatiliste tööriistadega kokku puutuvad.
- **Pneumaatilised tööriistad (PTUSA)** – kõigi pneumaatiliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-US pakutavate või ostetavate pneumaatiliste tööriistadega kokku puutuvad.

**Otsus.**

- Mitu täiendavat aadressiraamatut loote?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]