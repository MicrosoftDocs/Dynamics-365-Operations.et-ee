---
title: Ostukasti moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154059"
---
# <a name="buy-box-module"></a>Ostukasti moodul


[!include [banner](includes/banner.md)]

See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Mõiste *ostukast* viitab tavaliselt toote üksikasjade lehe alale, mis on lehe kuvatav osa ehk „above the fold” ja mis sisaldab kõige olulisemat teavet, mis on toote ostu tegemiseks vajalik. (Ala, mida nimetatakse inglise keeles „above the fold”, on nähtav, kui leht esmakordselt laeb, ilma et kasutaja peaks hiirega selle nägemiseks kerima.)

Ostukasti moodul on spetsiaalne konteiner, mida kasutatakse kõigi moodulite majutamiseks, mis on toote üksikasjade lehe ostukasti alal näidatud.

Toote üksikasjade lehe URL sisaldab toote ID-d. Kogu teave, mis on vajalik ostukasti mooduli renderdamiseks, tuletatakse sellest toote ID-st. Kui toote ID-d ei ole, siis ostukasti moodulit ei renderdata lehel õigesti. Seetõttu saab ostukasti moodulit kasutada ainult lehtedel, millel on toote kontekst. Selle kasutamiseks lehel, millel ei ole toote konteksti (nt avaleht või turunduse leht), peate tegema täiendavaid kohandusi.

## <a name="buy-box-module-properties-and-slots"></a>Ostukasti mooduli atribuudid ja pesad 

Toote üksikasjade lehel on ostukast jaotatud kaheks piirkonnaks: meediumipiirkond vasakul ja sisupiirkond paremal. Vaikimisi on meediumipiirkonna veeru ja sisupiirkonna veeru suhe 2:1. Mobiilsetel seadmetel on kaks piirkonda virnastatud, nii et üks piirkond ilmub teise piirkonna all. Kujundusi saab kasutada veeru laiuse ja virnastamise astme kohandamiseks.

Ostukasti moodul annab toote pealkirja, kirjelduse, hinna ja hinnangud. Samuti laseb see klientidel valida toote variante, millel on erinevad toote atribuudid, nagu suurus, stiil ja värv. Kui tootevariant on valitud, värskendatakse ostukasti teisi atribuute (nt toote kirjeldus ja pildid), et näidata variandi teavet. 

Koguse valija on esitatud, et kliendid saaksid määrata ostetavate kaupade koguse. Maksimaalset kogust, mida saab osta, saab määrata saidi sätetes.
 
Ostukastist saavad kliendid teha ka selliseid toiminguid nagu toote lisamine ostukorvi, toote lisamine soovinimekirja ja komplekteerimiskoha valimine. Neid toiminguid saab teha toote või toote variandiga. Toote lisamiseks soovinimekirja peab klient olema sisse logitud.

Kujundusi saab kasutada ostukasti tooteatribuutide ja tegevuste juhtelementide eemaldamiseks või muutmiseks. 

## <a name="module-properties"></a>Mooduli atribuudid

- **Pealkirja silt** – see atribuut määratleb toote pealkirjale pealkirja sildi. Kui ostukast on lehe ülaosas, tuleb see atribuut seada väärtusele **h1**, et vastata juurdepääsetavuse standarditele. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moodulid, mida saab ostukasti moodulis kasutada

- **Meediumigalerii** – seda moodulit kasutatakse toote üksikasjade lehel toote piltide näitamiseks. See võib toetada ühte kuni mitu pilti. See toetab ka pisipilte. Pisipildid saab paigutada kas horisontaalselt (reana pildi all) või vertikaalselt (veeruna pildi kõrval). Meediumigalerii mooduli saab lisada ostukasti mooduli pesale **Meedia**. Hetkel toetab see ainult pilte. 
- **Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused. Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).

## <a name="buy-box-module-settings"></a>Ostukasti mooduli sätted

Ostukasti moodulitel on kolm seadistust, mida saab konfigureerida jaotises **Saidi sätted \> Laiendused**.

- **Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas. See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele. Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.
- **Varude puhver** – seda atribuuti kasutatakse varude puhvri arvu määramiseks. Varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline. Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas. Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Ostukasti moodul toob toote teabe välja Commerce Scale Uniti API-de abil. Kogu teabe toomiseks kasutatakse toote ID-d toote üksikasjade lehel.

## <a name="add-a-buy-box-module-to-a-page"></a>Lehele ostukasti mooduli lisamine

Uuele lehele ostukasti mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge fragment nimega **ostukasti fragment** ja lisage sellele ostukasti moodul.
1. Lisage ostukasti mooduli pesas **Meedia** meediumigalerii moodul.
1. Lisage ostukasti mooduli pesasse **Kaupluse valik** kaupluse valija moodul.
1. Registreerige leht ja avaldage see.
1. Looge toote üksikasjade lehel jaoks mall ja pange sellele nimeks **PDP mall**.
1. Lisage vaikeleht.
1. Lisage vaikelehe pessa **Peamine** ostukasti fragment.
1. Salvestage mall, lõpetage selle redigeerimine ja seejärel avaldage see.
1. Kasutage äsja loodud malli, et luua leht, mille nimi on **PDP leht**.
1. Lisage uue lehe pessa **Peamine** ostukasti fragment.
1. Salvestage ja kuvage lehe eelvaade. Lisage eelvaatelehe URL-ile päringustringi parameeter **?productid=&lt;toote ID&gt;**. Sel viisil kasutatakse eelvaatelehe laadimiseks ja renderdamiseks toote konteksti.
1. Salvestage leht, lõpetage selle redigeerimine ja avaldage see. Toote üksikasjade lehele peaks ilmuma ostukast.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Kaupluse valija moodul](store-selector.md)

[Konteineri moodul](add-container-module.md)

[Ostukorvimoodul](add-cart-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
