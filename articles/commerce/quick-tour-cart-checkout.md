---
title: Ostukorvi ja väljaregistreerimise ülevaade
description: See artikkel annab ülevaate ostukorvi ja väljaregistreerimise lehtedest Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: c2fad50b58db8213ecc246376e28b2ae43f77a08
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286434"
---
# <a name="cart-and-checkout-pages-overview"></a>Ostukorvi ja väljaregistreerimise ülevaade

[!include [banner](includes/banner.md)]

See artikkel annab ülevaate ostukorvi ja väljaregistreerimise lehtedest Microsoft Dynamics 365 Commerce.

E-kaubanduse veebisaidi ostukorvi lehel kuvatakse kõik kaubad, mille klient on ostukorvi lisanud. Ostukorvi lehekülg on ehitatud ostukorvi mooduli abil. Ostukorvi moodul on konteiner, mis majutab kõiki mooduleid, mis on vajalikud ostukorvis olevate kaupade esitlemiseks. Ostukorvi moodul saab kasutada ka teisi mooduleid, et näidata tellimuse kokkuvõtet ja kõiki kliendi tellimusele rakendatud kampaania koode.

E-kaubanduse veebisaidi lehe kassas on üksikasjalik voog, mida kliendid järgivad tellimuse esitamiseks vajaliku teabe sisestamisel. Kassa moodul võib sisaldada mooduleid, mis töötlevad kättetoimetamise aadressi, tarne meetodeid, arveldusteavet, tellimuse kokkuvõtet ja muud kliendi tellimustega seotud teavet.

## <a name="cart-page"></a>Ostukorvi leht

Ostukorvi lehekülg toimib ostukorvina ja sisaldab kõiki ostukorvi lisatud kaupu.

Järgmisel joonisel on kujutatud ostukorvi lehe näide, mis loodi mooduliteegi ja kujunduse „Fabrikam” abil.

![Ostukorvi lehe näide.](./media/cart2.PNG)

Ostukorvi lehe põhiosas kuvatakse kõik kaubad, mille klient on ostukorvi lisanud. Kõik kehtivad allahindlused on esitletud. Need allahindlused hõlmavad keerukaid allahindlusi. Näideteks on "Osta 3 toodet ja saad 10% soodsamalt" või "Osta pudel ja seljakott, et saada 10% soodustust". Tellimuse kokkuvõtte moodul näitab summat, mis kuulub tasumisele pärast allahindluste, tarnekulude, maksude jms rakendamist. On olemas ka promokoodi moodul, mis võimaldab kliendil rakendada või eemaldada kampaania koode.

Klient saab sisseoste teha anonüümselt või sisselogitud kasutajana. Kui klient on sisse logitud, säilitatakse ostukorvis olevad kaubad seansside vahel. Sel viisil saab klient jätkata ostlemist mitmest seadmest.

Ostukorvist saab klient minna edasi kassasse. Klient saab käivitada väljaregistreerimise külaliskasutajana või sisselogitud kasutajana.

Lisateavet ostukorvi lehe loomise kohta leiate teemast [Ostukorvi mooduli lisamine lehele](add-cart-module.md).

## <a name="checkout-page"></a>Kassa leht

Kassa leht on koht, kus kliendid sisestavad tellimuse esitamiseks vajaliku teabe.

Järgmisel joonisel on kujutatud kassa lehe näide, mis loodi mooduliteegi abil.

![Kassa lehe näide.](./media/Checkout.PNG)

Kassa lehe põhiosa on see, kus kogutakse kogu tellimuse teave. See teave sisaldab tarneaadressi, kohaletoimetamise valikuid ja makseteavet. Kassas on samm-sammuline voog, sest teave tuleb töödelda kindlas järjekorras. Näiteks tuleb sisestada tarneaadress, enne kui saab tarnekulud arvutada ja makse autoriseerida.

### <a name="shipping-address"></a>Tarneaadress

Tarneaadress on nõutav, kui kaubad tuleb saata. Iga asukoha saatmise aadresside vormingut saab konfigureerida rakenduses Dynamics 365 Commerce. Näiteks kui kaubad saadetakse Ameerika Ühendriikidesse, peab tarneaadress sisaldama tänava aadressi, osariiki ja postiindeksit. Mõned põhilised sisestuse kinnitamised tehakse saatmise aadressi väljade jaoks, nt tähe- ja numbrimärkide, maksimumpikkuse ja numbrite kinnitamine. Kuigi aadressi enda kehtivust ei kontrollita, saab seda kontrollida kohandatud kolmandate osapoolte teenuste abil.

Tarneaadress rakendatakse kõigile ostukorvi kaupadele, mille jaoks on valitud suvand "tarni". Kui kasutate kassa voogu, mille on taganud mooduliteek, ei saa üksikuid ostukorvi tooteid saata erinevatele aadressidele. Kui vajate seda võimalust, saab seda rakendada kassa moodulite kohandamise kaudu.

Kui kättetoimetamise aadress on olemas, kuvatakse rakenduse Dynamics 365 Commerce võrgupoes saadaolevad tarneviisid. Kohaletoimetamise meetodeid ja neid toetavaid aadresse saab konfigureerida rakenduses Commerce.

### <a name="payment"></a>Makse

Järgmine etapp kassa voos on makse. E-kaubanduses saab tellimuste täitmiseks kasutada mitut makseviisi, nt krediitkaarte, kinkekaarte ja boonuspunkte. Kasutada saab ka nende makseviiside kombinatsiooni. Sõltuvalt kasutatavast makseviisist, võidakse nõuda lisateavet. Näiteks krediitkaardi makse nõuab arveldamise aadressi. Krediitkaardi makseid töödeldakse Adyen Payment Connectori abil.

#### <a name="loyalty-points"></a>Boonuspunktid

Kassas olev klient, kes on püsikliendiprogrammi liige ja kes on kogunud boonuspunkte, saab neid boonuspunkte lunastada tellimuse jaoks. Boonuspunktide moodul kuvatakse ainult siis, kui kliendil on olemas püsikliendi liikmelisus. Mitte-liikmetele ja külaliskasutajatele on see moodul peidetud.

#### <a name="gift-cards"></a>Kinkekaardid

Mooduliteek võimaldab sisemisi kinkekaarte lunastada tellimuse jaoks. Sisemise kinkekaardi rakendamiseks peab klient olema sisse logitud. Täiendava turvalisuse tagamiseks soovitame teil voogu kohandada, kasutades sisemiste kinkekaartide jaoks isiklikku tuvastuskoodi (PIN-koodi).

### <a name="signed-in-and-guest-users"></a>Sisselogitud ja külaliskasutajad

Klient saab lõpetada väljeregistreerimise protsessi külaliskasutajana või sisselogitud kasutajana. Kui klient logib sisse, tuuakse automaatselt sisse kontoteave, nt salvestatud tarneaadress ja salvestatud krediitkaardi üksikasjad.

### <a name="order-summary"></a>Tellimuse kokkuvõte

Kassas kuvatakse ostukorvis reaüksuste kokkuvõte, nii et klient saab tellimuse enne esitamist kinnitada. Reaüksuseid ei saa kassa voo ajal redigeerida. Siiski on olemas linki ostukorvi, juhul kui kasutaja soovib tagasi minna ja reaüksusi redigeerida.

Pärast seda, kui klient annab tarne- ja arvelduse teabe, peegeldab tellimuse kokkuvõte summat, mis on tasutud pärast boonuspunktide, kinkekaartide ja muude maksete rakendamist.

### <a name="order-confirmation-and-email"></a>Tellimuse kinnitus ja meil

Kui klient esitab tellimuse, esitatakse kinnituse number. Sel hetkel on makse autoriseeritud, kuid mitte laekunud. Makse laekub ainult siis, kui tellimus on täidetud (st kui see on saadetud või komplekteeritud).

Pärast tellimuse loomist saadetakse kliendile tellimuse kinnituse meilisõnum.

Lisateavet kassa lehe loomise kohta leiate teemast [Kassa mooduli lisamine lehele](add-checkout-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Avalehe ülevaade](quick-tour-home-page.md)

[Toote üksikasjade lehe ülevaade](quick-tour-pdp.md)

[Kontohalduse lehtede ülevaade](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
