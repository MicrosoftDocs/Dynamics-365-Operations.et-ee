---
title: Maksmise moodul
description: Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411180"
---
# <a name="checkout-module"></a>Maksmise moodul


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.

## <a name="overview"></a>Ülevaade

Maksmise moodul on spetsiaalne konteiner, mis majutab kõiki tellimuse loomiseks vajalikke mooduleid. See esitab samm-sammulise voo, mida klient ostu sooritamiseks kogu asjakohase teabe sisestamiseks kasutab. See hõivab tarneaadressi, tarneviisi ja arveldusteavet. Samuti esitatakse tellimuse kokkuvõte ja muud kliendi tellimusega seotud andmed.

Maksmise moodul renderdab andmeid ostukorvi ID põhjal. See ostukorvi ID salvestatakse brauseriküpsisena. Ostukorvi ID on nõutav, et renderdada maksmise mooduli teavet, nagu tellimuse kaubad, kogusumma ja allahindlused. 

Järgmisel pildil on näide Fabrikami maksmise moodulist maksmise lehel.

![Maksmise mooduli näide](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Maksmise mooduli atribuudid

Kassa moodul näitab tellimuse kokkuvõtet ja pakub tellimuse esitamise funktsionaalsust. Kõigi tellimuse esitamiseks vajalike kliendi andmete kogumiseks tuleb kassamoodulile lisada täiendavaid mooduleid. Seetõttu on jaemüüjatel paindlikkus vastavalt oma vajadustele kassavoole kohandatud mooduleid lisada või välistada.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Tarneaadress** – see moodul võimaldab kliendil lisada või valida tellimuse tarneaadressi. Kui klient on sisse logitud, kuvatakse aadress, mis selle kliendi jaoks eelmisel korral salvestati. Seejärel saab klient valida nende aadresside seast. Klient saab lisada ka uue aadressi. Tarneaadressi kasutatakse kõigi kaupade puhul, mis nõuavad tarnet. Seda ei saa üksikute reakaupade puhul kohandada. Tarneaadressi vormingud määratletakse iga riigi või piirkonna kohta ja sellest moodulist tulenevad riigi/piirkonna spetsiifilised reeglid. Kuigi see moodul ei paku aadressi kinnitamist, saab aadressi kinnitamist rakendada kohandamise kaudu. Kui tellimus sisaldav ainult kaupu, millele minnakse poodi järgi, siis see moodul peidetakse automaatselt.

    Järgmisel pildil on näide tarneaadressi moodulist maksmise lehel.

    ![Tarneaadressi mooduli näide](./media/ecommerce-shippingaddress.PNG)

- **Tarnevalikud** – see moodul võimaldab kliendil valida tellimuse tarnevaliku. tarnevalikud põhinevad saatmisaadressil. Kui tarneaadressi muudetakse, tuleb tarnevalikud uuesti hankida. Kui tellimus sisaldav ainult kaupu, millele minnakse poodi järgi, siis see moodul peidetakse automaatselt.

    Järgmisel pildil on näide tarnevalikute moodulist maksmise lehel.

    ![Tarnevalikute mooduli näide](./media/ecommerce-deliveryoptions.PNG)

- **Maksmise jaotise konteiner** – see moodul on konteiner, kuhu saate lisada mitu moodulit, et luua jaotis maksmise voo sees. Näiteks saate panna sellesse konteinerisse kõik maksmisega seotud moodulid, et need kuvataks ühe jaotisena. See moodul mõjutab ainult voo paigutust.
- **Kinkekaart** – see moodul võimaldab kliendil tasuda tellimuse eest kinkekaardiga. See toetab ainult Microsoft Dynamics 365 Commerce’i kinkekaarte. Tellimusele saab rakendada ühe või mitu kinkekaarti. Kui kinkekaardi saldo ei kata ostukorvis olevat summat, saab kinkekaardi kombineerida muu makseviisiga. Kinkekaarte saab lunastada ainult siis, kui klient on sisse logitud.
- **Püsikliendi punktid** – see moodul võimaldab kliendil tasuda tellimuse eest püsikliendi punktidega. See esitab saadaolevate punktide ja aeguvate punktide kokkuvõtte ja võimaldab klientidel valida lunastamiseks punktide arvu. Kui klient ei ole sisse logitud või ei ole püsikliendis programmi liige või kui ostukorvi kogusumma on 0 (null), peidetakse see moodul automaatselt.
- **Makse** – see moodul võimaldab kliendil tasuda tellimuse eest krediitkaardiga. Kui püsikliendi punktid või kinkekaart katab ostukorvi kogusumma või kui see on 0 (null), peidetakse see moodul automaatselt. Krediitkaardi integratsiooni pakub selle mooduli Adyeni makseühendus. Lisateavet selle konnektori kasutamise kohta vaadake teemast [Dynamics 365 Makseühendus Adyenile](dev-itpro/adyen-connector.md).
- **Arveldusaadress** – see moodul võimaldab kliendil esitada arveldusteavet. Seda teavet töötleb koos krediitkaardi teabega Adyen. See moodul sisaldab võimalust, et kliendid kasutavad oma arveldusaadressi tarneaadressina.

    Järgmisel pildil on näide kinkekaardi, boonuspunktide, maksmise ja arveldusaadressi moodulitest maksmise lehel.

    ![Kinkekaardi, boonuspunktide, maksmise ja arveldusaadressi moodulite näide](./media/ecommerce-payments.PNG)

- **Kontaktteave** – see moodul võimaldab kliendil lisada või muuta tellimuse kontaktandmeid (meiliaadress).

- **Tekstiplokk** – see moodul sisaldab mis tahes teateid, mida juhib sisuhaldussüsteem (CMS). Näiteks võib see sisaldada teadet, mis ütleb: „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam." 

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Enamik maksmise teabest, näiteks tarneaadress ja tarnemeetod, salvestatakse ostukorvis ja töödeldakse tellimuse osana. Ainus erand on krediitkaardi teave. See teave töödeldakse otse Adyeni makseühenduse abil. Makse on autoriseeritakse, kuid seda ei nõuta sisse.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Lehele maksmise mooduli lisamine ja vajalike atribuutide seadistamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Lehe fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus lehe fragment** moodul **Maksmine**.
1. Jaotises **Lehe fragmendi nimi** sisestage nimi **Maksmise fragment** ja seejärel valige **OK**.
1. Valige pesa **Maksmise moodul**.
1. Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.
1. Valige pesas **Maksmise teave** kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisamoodul** moodulid **Tarneaadress**, **Tarnevalikud**, **Maksmise jaotise konteiner** ja **Kontaktteave** ning valige seejärel **OK**.
1. Valige moodulis **Maksmise jaotise konteiner** kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodulid **Kinkekaart**, **Püsiklient** ja **Maksmine** ning seejärel **OK**. Sel viisil saate kindlustada, et kõik maksmisviisid ilmuvad jaotises koos.
1. Valige **Salvesta** ja seejärel fragmendi eelvaate kuvamiseks **Eelvaade**. Osasid mooduleid, millel ei ole ostukorvi konteksti, ei pruugita eelvaates renderdada.
1. Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Looge mall, mis kasutab uut maksmise fragmenti.
1. Looge maksmise leht, mis kasutab uut malli.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi moodul](add-cart-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
