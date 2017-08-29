---
title: "Hankija koostöö klientidega"
description: "See teema kirjeldab, kuidas saate kasutada hankija koostööd rakenduses Finance and Operations, et töötada ostutellimustega ja jälgida veose varusid."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 41436dab710a5fee0fe0800dff1ebefefa841afc
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="vendor-collaboration-with-customers"></a>Hankija koostöö klientidega

[!include[banner](../includes/banner.md)]


See teema kirjeldab, kuidas saate kasutada hankija koostööd rakenduses Finance and Operations, et töötada ostutellimustega ja jälgida veose varusid.

See teema kirjeldab, kuidas saate kasutada hankija koostööd, et töötada klientidega rakenduses Microsoft Finance and Operations. See hõlmab teavet selle kohta, kuidas ostutellimusi jälgida ja neile vastata ning kuidas jälgida veose varusid. Samuti on võimalik arvetega töötamiseks hankija koostööd kasutada. Lisateabe saamiseks vaadake teemat [Hankija koostöö arve tööruum](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Töötamine ostutellimustega
Tööruum **Ostutellimuse kinnitus** võimaldab teil vastata ostutellimusele, mis on saadetud teile ülevaatamiseks. See võimaldab teil vaadata teavet ostutellimuste kohta, mis ootavad kliendipoolset tegevust, ja selliste ostutellimuste kohta, mis on kinnitatud, kuid ikka avatud. Tööruumis **Ostutellimuse kinnitus** on kolm loendit.

-   **Ülevaatamist ootavad ostutellimused** – see loend näitab teile saadetud ostutellimusi ja ootab teilt vastust. Pärast vastamist kaob ostutellimus loendist. Kui klient saadab teile ostutellimuse uue versiooni enne, kui olete eelmisele vastanud, näidatakse ainult värskeimat versiooni.
-   **Kliendi tegevuse ootel** - see loend võimaldab teil näha ostutellimusi, millele olete vastanud, kuid mida klient pole veel kinnitanud. Kui aktsepteerisite ostutellimuse, saate seda jälgida selles loendis, kuni olekuks muudetakse **Kinnitatud**. Kui lükkasite ostutellimuse tagasi või aktsepteerisite selle muudatustega, saate jälgida ostutellimust siin, kuni klient saadab uue versiooni.
-   **Ava kinnitatud ostutellimused** - see loend sisaldab kõiki teie konto ostutellimusi, millel on olek **Kinnitatud**. Kui tooted ja teenused on ostutellimuse suhtes täielikult vastu võetud, kaob ostutellimus loendis.

Järgmine loend näitab nelja lehte, mida saate kasutada töötamiseks ostutellimustega, millest kaks sisaldavad sama teavet kui tööruumis olevad loendid:

-   **Ülevaatamist ootavad ostutellimused** (vaadake eespool)
-   **POstutellimuse hankija kinnitamise ajalugu** – see leht sisaldab kõiki ostutellimusi ja kõiki hankijale saadetud ostutellimuste versioone ja kõiki vastuseid, mis on saadud hankijalt.
-   **Ava kinnitatud ostutellimused** (vt eespool)
-   **Kõik kinnitatud ostutellimused** – see leht sisaldab kõiki kinnitatud ostutellimusi, sealhulgas neid, millel tooted ja teenused on vastu võetud. Saate kasutada seda loendit jälgimaks, milliste ostutellimuste jaoks saate arveid saata.

### <a name="responding-to-purchase-orders"></a>Ostutellimustele vastamine

Ostutellimused, mille klient on teile saatnud, on nähtavad tööruumis **Ostutellimuse kinnitus** ja lehel **Ülevaatamist ootavad ostutellimused**. Pärast ostutellimuse avamist saate valida selle kinnitamise, tagasilükkamise või selle muudatustega kinnitamiseks. Ostutellimuse päises või individuaalsetel ridadel võib olla manuseid. Teil on võimalik manustada teie vastusele teave ostutellimuse päises või individuaalsetel ridadel. Näiteks võite soovitada soovitada kauba asendamise ühele ridadest. Saate eelvaadata ja printide ostutellimuse PDF-failina, kasutades suvandit **Kuva eelvaade / prindi**. Saate peita või näidata järgmiseid dimensiooniveerge, kasutades valiku **Dimensioonide kuvamine** tegevust: Tegevuskoht, Ladu, Värv, Size, Suurus, Konfiguratsioon. Kui kasutate suvandit **Aktsepteeri koos muudatustega**, saate üksikud read kinnitada või tagasi lükata. Samuti saate ridadele teha järgmised muudatused.

-   Muutke kuupäevi või koguseid. Kui soovite värskendada kinnitatud tarnekuupäev kõikidel ridadel, kasutage ostutellimuse päises suvandit **Värskenda tarnekuupäeva**.
-   Ridade tükeldamine erinevate tarnekuupäevade ja -koguste jaoks.
-   Asendage üksus. Selleks sisestage kauba kirjeldus ja kauba number väljale **Väline** jaotises **Rea üksikasjad**.

Te ei saa muuta hinnateavet ega tasusid, kuid saate teha soovitusi nendele muudatuste tegemiseks, kasutades märkusi. Kui teie klient saadab teile ostutellimuse uue versiooni, on sellel versiooni järelliide näitamaks, et tegemist on varasemalt kommunikeeritud ostutellimuse modifitseeritud versiooniga. Leht **Ostutellimuse hankija kinnitamise ajalugu** võimaldab teil jälgida iga tellimuse ajalugu.

## <a name="monitoring-consignment-inventory"></a>Veose varude jälgimine
Kui kasutate veose varusid, saate kasutada hankija koostöö liidest, et kuvada teavet järgmistel lehtedel:

-   **Ostutellimused, mis tarbivad veose varusid** – veose varude jaoks mõeldud ostutellimused luuakse siis, kui klient varude omandiõiguse üle võtab. Need veose ostutellimused kuvatakse ainult lehel **Ostutellimused, mis tarbivad veose varusid**. Need ei ole kaasatud lehele **Kõik kinnitatud ostutellimused**.
-   **Veose varudest saadud tooted** - sellel lehel on esitatud kõik kanded, kus toodete omandiõigus on ülekantud ettevõttele, mis tarbib varusid. Saate kasutada seda teavet, et kliendile arvet esitada.
-   **Veose vaba kaubavaru** – see leht näitab vabu veose varusid, mille omanik on teie ettevõtte ja mis on klientide laos saadaval.


<a name="see-also"></a>Vt ka
--------

[Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md)




