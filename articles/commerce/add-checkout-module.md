---
title: Maksmise moodul
description: Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 389e3e9d631574eac499f7c6146e2776b8126a52
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761101"
---
# <a name="checkout-module"></a>Maksmise moodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.

## <a name="overview"></a>Ülevaade

Maksmise moodul on spetsiaalne konteiner, mis majutab kõiki tellimuse loomiseks vajalikke mooduleid. See esitab samm-sammulise voo, mida klient ostu sooritamiseks kogu asjakohase teabe sisestamiseks kasutab. See hõivab tarneaadressi, tarneviisi ja arveldusteavet. Samuti esitatakse tellimuse kokkuvõte ja muud kliendi tellimusega seotud andmed.

Maksmise moodul renderdab andmeid ostukorvi ID põhjal. See ostukorvi ID salvestatakse brauseriküpsisena. Ostukorvi ID on nõutav, et renderdada maksmise mooduli teavet, nagu tellimuse kaubad, kogusumma ja allahindlused. 

Järgmisel pildil on näide Fabrikami maksmise moodulist maksmise lehel.

![Maksmise mooduli näide](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Maksmise mooduli atribuudid

Kassa moodul näitab tellimuse kokkuvõtet ja pakub tellimuse esitamise funktsionaalsust. Kõigi tellimuse esitamiseks vajalike kliendi andmete kogumiseks tuleb kassamoodulile lisada täiendavaid mooduleid. Seetõttu on jaemüüjatel paindlikkus vastavalt oma vajadustele kassavoole kohandatud mooduleid lisada või välistada.

| Atribuudi nimi | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Kassa pealkiri | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Maksmise mooduli pealkiri. |
| Tellimuse kokkuvõtte pealkiri | Pealkirja tekst | Mooduli tellimuse kokkuvõtte jaotise pealkiri. |
| Ostukorvi reakaupade pealkiri | Pealkirja tekst | Maksmise moodulis kuvatavate ostukorvi reakaupade pealkiri. |
| Kuva reakauba saatekulud | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse reakaupade puhul rakenduvad saatekulud ostukorvi ridadel. Kui funktsioon **Päisekulu ilma proportsionaalse jaotamiseta** on Commerce'i peakontoris sisse lülitatud, rakendatakse saatekulu päisetasemel, mitte reatasemel. See funktsioon lisati Commerce'i versioonis 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Tarneaadress** – see moodul võimaldab kliendil lisada või valida tellimuse tarneaadressi. Lisateavet selle mooduli kohta leiate teemast [Tarneaadressi moodul](ship-address-module.md).

    Järgmisel pildil on näide tarneaadressi moodulist maksmise lehel.

    ![Tarneaadressi mooduli näide](./media/ecommerce-shippingaddress.PNG)

- **Tarnevalikud** – see moodul võimaldab kliendil valida tellimuse tarneviisi. Lisateavet selle mooduli kohta leiate teemast [Tarnevalikute moodul](delivery-options-module.md).

    Järgmisel pildil on näide tarnevalikute moodulist maksmise lehel.
 
    ![Tarnevalikute mooduli näide](./media/ecommerce-deliveryoptions.PNG)

- **Maksmise jaotise konteiner** – see moodul on konteiner, kuhu saate lisada mitu moodulit, et luua jaotis maksmise voo sees. Näiteks saate panna sellesse konteinerisse kõik maksmisega seotud moodulid, et need kuvataks ühe jaotisena. See moodul mõjutab ainult voo paigutust.

- **Kinkekaart** – see moodul võimaldab kliendil tasuda tellimuse eest kinkekaardiga. Lisateavet selle mooduli kohta leiate teemast [Kinkekaardi moodul](add-giftcard.md).

- **Püsikliendi punktid** – see moodul võimaldab kliendil tasuda tellimuse eest püsikliendi punktidega. See esitab saadaolevate punktide ja aeguvate punktide kokkuvõtte ja võimaldab klientidel valida lunastamiseks punktide arvu. Kui klient ei ole sisse logitud või ei ole püsikliendis programmi liige või kui ostukorvi kogusumma on 0 (null), peidetakse see moodul automaatselt.

- **Makse** – see moodul võimaldab kliendil tasuda tellimuse eest krediit- või deebetkaardiga. Kliendid saavad sisestada ka valitud makseviisi jaoks arveaadressi. Lisateavet selle mooduli kohta leiate teemast [Maksemoodul](payment-module.md).

    Järgmisel pildil on näide kinkekaardi, boonuspunktide ja maksemoodulitest maksmise lehel.

    ![Kinkekaardi, boonuspunktide ja maksemoodulite näide maksmise lehel](./media/ecommerce-payments.PNG)

- **Kontaktteave** – see moodul võimaldab kliendil lisada või muuta tellimuse kontaktandmeid (meiliaadress).

- **Tekstiplokk** – see moodul sisaldab mis tahes teateid, mida juhib sisuhaldussüsteem (CMS). Näiteks võib see sisaldada teadet, mis ütleb: „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam." 

- **Maksmise tingimused** – sellest mooduli kuvatakse rikastekst, mis sisaldab tingimusi ja märkeruutu kliendi sisendi jaoks. Märkeruut on valikuline ja konfigureeritav. Moodul salvestab sisendi ja seda saab kasutada kontrolliks enne tellimuse esitamise käivitamist, kuid see ei sisaldu tellimuse kokkuvõtte teabes. Seda moodulit saab lisada ettevõtte vajaduste järgi tellimuse konteinerisse, maksmise jaotise konteinerisse või tingimuste pessa. Kui see lisatakse maksmise konteinerisse või maksmise jaotise konteineri pesasse, kuvatakse see maksmiseprotsessi etapina. Kui see lisatakse tingimuste pessa, kuvatakse see tellimuse esitamise nupu lähedal.

    Järgmisel pildil on näide tingimustest maksmise lehel.

    ![Tingimuste näide maksmise lehel](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Enamik maksmise teabest, näiteks tarneaadress ja tarnemeetod, salvestatakse ostukorvis ja töödeldakse tellimuse osana. Ainus erand on krediitkaardi teave. See teave töödeldakse otse Adyeni makseühenduse abil. Makse on autoriseeritud, kuid raha ei võeta enne, kui tellimus on täidetud.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Lehele maksmise mooduli lisamine ja vajalike atribuutide seadistamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Maksma siirdumine**.
1. Avage jaotis **Fragmendi nimi**, sisestage **Maksma siirdumise fragmendi** nimi ja seejärel valige **OK**.
1. Valige pesa **Maksmise moodul**.
1. Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.
1. Valige pesas **Maksmise teave** kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisamoodul** moodulid **Tarneaadress**, **Tarnevalikud**, **Maksmise jaotise konteiner** ja **Kontaktteave** ning valige seejärel **OK**.
1. Valige moodulis **Maksmise jaotise konteiner** kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodulid **Kinkekaart**, **Püsiklient** ja **Maksmine** ning seejärel **OK**. Sel viisil saate kindlustada, et kõik maksmisviisid ilmuvad jaotises koos.
1. Lisage pesas **Tingimused** moodul **Maksmise tingimused**, kui see on vajalik. Konfigureerige mooduli atribuutide paanil tingimuste tekst nii nagu vaja.
1. Valige **Salvesta** ja seejärel fragmendi eelvaate kuvamiseks **Eelvaade**. Osasid mooduleid, millel ei ole ostukorvi konteksti, ei pruugita eelvaates renderdada.
1. Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Looge mall, mis kasutab uut maksmise fragmenti.
1. Looge maksmise leht, mis kasutab uut malli.

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksemoodul](payment-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnevalikute moodul](delivery-options-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)
