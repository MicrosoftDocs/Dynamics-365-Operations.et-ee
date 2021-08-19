---
title: Töökäsu projekti seadistus
description: Selles teemas selgitatakse töökäskude projekti seadistamist varahalduses.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb897ca0a7e9c45ee55244189bb1b487fbddf0714ad3ea0cac26eb7bac36a07f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754079"
---
# <a name="work-order-project-setup"></a>Töökäsu projekti seadistus

[!include [banner](../../includes/banner.md)]

 

**Varahalduse** moodulis on projekti seos nõutav iga töökäsu töö puhul. Töökäsu tööga seotud projekt võimaldab teil jälgida kulusid erinevate varahaldusega seotud projektidele, nagu näiteks sisemiste hooldustööde projektid, teenusehalduse projektid ja investeerimisprojektid. 

## <a name="project-setup-for-a-work-order-job"></a>Töökäsu töö projekti seadistus

Kui loote töökäsu töö töökäsule, määratlevad projekti seadistus moodulis **Projektjuhtimine ja raamatupidamine** ning töökäskude projekti seadistus moodulis **Varahaldus**, kuidas projekte saab kasutada kulukontrolliks selle töökäsu tööl valitud varal. Selles lõigus kirjeldatakse projekti seadistuse järgmisi osi, mida kasutatakse töökäsus: põhiprojekt (projekti ID), projekti tüüp, projekti tegevused ja finantsdimensioonid:

- Töökäsu töö loomisel töökäsul luuakse selle jaoks automaatselt kordumatu projekti ID ja seotud projekti tegevus. Kui aga töökäsu mitu töökäsu tööd hõlmavad sama vara, siis kasutatakse neil sama projekti ID-d. Teisisõnu luuakse töötellimuse iga vara kohta üks projekti ID.

    - Töökäsu töö põhiprojekti (projekti ID) leiab põhiprojekti seadistusest. (Lisateavet põhiprojekti häälestuse kohta vt järgmisest jaotisest.) Näiteks kui seote kliendi või funktsionaalse asukoha kindla põhiprojektiga, kasutatakse põhiprojekti iga kord, kui loote selle kliendi või selle funktsionaalse asukoha jaoks töökäsu. Kui te ei seosta kindlat projekti ID-d näiteks funktsionaalse asukohaga, kasutatakse järgmist vastavat põhiprojekti töökäsu projekti seadistuses.
    - Iga projekti ID puhul on nõutav projektitüüp. Projektitüübi leiate projektigrupi seadistuse seadistusest. (Lisateavet projektigrupi seadistuse kohta vt järgmisest jaotisest.) Kui projektigrupi seadistuses ei leita ühtegi vastet, kasutatakse projektigrupi seadistust peamise projekti jaoks.
    - Projekti tegevuste prognooside ja töölehtede jaoks seadistatud seadistus kopeeritakse põhiprojektist töökäsu projekti. Kui valikud **Tund**, **Kulu** ja **Kaup** on seatud väärtusele **Jah** projekti puhul, mida kasutatakse põhiprojektina, on projekti tegevus kohustuslik prognoosidel ja töölehtedel. (Nende valikute juurde pääsemiseks valige **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja seejärel valige projekt, mida kasutatakse põhiprojektina. Valikud jaotises **Nõua tegevust töölehtedel** on kiirkaardil **Seadistus**.)

- Finantsdimensioonid kopeeritakse varast ja ühendatakse põhiprojektiga.

Järgmine jaotis selgitab, kuidas seadistada põhiprojekte ja projektigruppe. Põhiprojekti ja põhigruppe kasutatakse töökäskude kontrollimiseks. Neid kasutatakse ka töökäskude aruandluses.

## <a name="set-up-work-order-projects"></a>Töökäsu projektide seadistamine

Enne töökäskude loomise alustamist peate seadistama töökäsu projektid. Lehekülg **Töökäsu projekti seadistus** (**Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Projekti seadistus**) sisaldab kahte vahekaarti: **Põhiprojekt** ja **projektigrupp**.

Vahekaardil **Põhiprojekt** saate seadistada projekti seoseid, mida saab kasutada, kui töökäsu töös valitud varal pole projekti seadistatud. Põhiprojekti seadistus ei ole kohustuslik, kui teie ettevõte kasutab vara projekte. See on asjakohane ainult siis, kui soovite kasutada töökäsu projekte vara projektide asemel. Sel juhul peate seadistama vähemalt ühe põhiprojekti.

Vahekaardil **Projektigrupp** saate seadistada projektigruppe, mida saab seostada töökäsu tüüpide, varatüüpide ja varadega.

Projektigruppe saab kasutada kindla kategooria (gruppide) loomiseks, mida kasutatakse kulude kontrollimiseks. Näiteks luues projektigruppe kindlate varatüüpide või töökäsu tüüpide jaoks, saate hoolduskulusid üksikasjalikult jälgida tüübi järgi.

Projektigrupid pole kohustuslikud. Kui te ei seadista projektigruppe, kasutatakse projektigrupi määratlemiseks põhiprojekti ning põhiprojekti projektigrupist luuakse alamprojekt.

Seadistus võimaldab täielikku integreerumist mooduliga **Projektihaldus ja raamatupidamine**. Seetõttu saate jälgida kulusid, mis on seotud töökäskudega seotud projektides. Järgmine toiming kirjeldab töökäsu projektide seadistust.

1. Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Projekti seadistus**.
2. Valige lehel **Põhiprojekt** valik **Lisa**.
3. Valige väljades **Töökäsu tüüp**, **Funktsionaalne asukoht**, **Vara tüüp** ja **Vara** väärtused, mida vajate. Iga lisatud rea puhul saate seadistada ainult ühe või mitu välja. Teie määratud väljade arv määratleb kombinatsiooni, mida kasutatakse projekti ID valimisel varahalduses. 

    Kui valite funktsionaalse asukoha, kaasatakse seotud alamasukohad automaatselt. Kui valite vara, saate samale varale luua rohkem töökäsu projekti seadistamise ridu, kuid saate valida selle vara jaoks erinevaid projekte.

4. Väljal **projekti ID** valige projekt, mis peaks olema seotud sammus 3 loodud seadistusega.
5. Kui projekti seadistus peaks kehtima ainult piiratud perioodil, valige lõppkuupäev väljal **Lõppkuupäev**. Muidu valige **Puudub**.

    Vaikimisi on alguskuupäevaks seadistatud kuupäev, mil lisate lehele töökäsu projekti. Seda kontrollib väli **Kehtiv alates**, mis on vaikimisi peidetud. Välja **Kehtiv alates** kuvamiseks valige **Kuva** \> **Kõik**. Seejärel saate välja **Kehtiv alates** kasutada koos väljaga **Lõppkuupäev**, et seadistada töökäsu projektile piiratud kehtivusaeg.

    ![Töökäskude projekti seadistuse leht.](media/17-setup-for-work-orders.png)

6. Valige lehel **Põhiprojekt** valik **Lisa**.
7. Väljal **Töökäsu tüüp** valige töökäsu tüüp.
8. Kui soovite, et projektigrupi seos oleks täpsem, valige väljal **Varatüüp** või vara väljal **Vara**.
9. Valige väljal **Projektigrupp** projektigrupp, mis peaks olema seotud töökäsu tüübiga. Näiteks töökäsu tüüp, mille nimi on **Ennetav hooldus**, võib olla seotud projektigrupiga nimega **Eelmine hooldus** või **Sisemine**. Teise võimalusena võidakse töökäsu tüüpi **Investeering**, mida kasutatakse investeeringute ja põhivaraga seotud töökäskude puhul, seostada projektigrupi nimega **Invest** või **Investeering**.
10. Valige käsk **Salvesta**.

![Töökäskude projekti seadistuse leht, töökäsu lisamine.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Iga kord, kui luuakse töökäsu rida, otsib varahaldus projektigrupi, mis peaks olema seotud töökäsu tööprojektiga. Otsing põhineb selles teemas kirjeldatud seadistusel. Igal projektigrupil on seotud projektitüüp. Projektigrupid, millel on projektitüüp **Aja- ja materjalikulu** või **Fikseeritud hind**, kehtivad ainult kliendi kontoga seotud varade puhul.
>
> Põhiprojektide ja projektigruppide puhul, kui süsteem valib saadaoleva töökäsu projekti või projektigrupi, põhineb valik kirjetel, mille lõite eelmise protseduuri abil. Varahaldus läbib kirjeid, mis on seotud töökäsu projektiga, et kontrollida võimalikku vastet. Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena. Teisisõnu kontrollib varahaldus töökäsu põhiprojektile esmalt võimalikku vastet väljale **Vara**. Kui vastet ei leita, otsib see vastet väljale **Varatüüp**. Kui vastet ei leita, kontrollib see vastet väljale **Funktsionaalne asukoht**. Nagu näete lehe **Töökäsu projekti seadistus** paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule. Kui vastet ei leita, kasutatakse vaikimisi kirjet, kus on valitud ainult projekti ID. Seotud projektigrupi leidmise protsess on sarnane. Varahaldus kontrollib esmalt välja **Vara** võimalikku vastet, seejärel välja **Varatüüp** ja seejärel välja **Töökäsu tüüp**. Kui vastet ei leita, kasutatakse vaikimisi kirjet, kus on valitud ainult projektigruppi.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]