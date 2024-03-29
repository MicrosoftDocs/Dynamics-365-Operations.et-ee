---
title: Töö asukoha tüübid
description: See artikkel kirjeldab, kuidas luua Varahalduses funktsiooni asukohatüüpe.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c44e503900bd157d7f0159cdf2b2d0c1fb3393f
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015779"
---
# <a name="functional-location-types"></a>Töö asukoha tüübid

[!include [banner](../../includes/banner.md)]

 

See artikkel kirjeldab, kuidas luua Varahalduses funktsiooni asukohatüüpe. Töö asukoha tüüpe kasutatakse töö asukohtade nõuete haldamiseks, sealhulgas selle kohta, kuidas varasid töö asukohta paigaldada. Saate seadistada varade tüüpe, hoolduskavu, töö asukoha atribuute ja vara atribuutide nõudeid, mida kasutatakse töö asukohas, mis kasutab konkreetseid töö asukoha tüüpe. Kui loote töö asukoha, on töö asukoha tüüp kohustuslik.

>[!NOTE] 
>Töö asukohtadega töötamiseks peate looma töö vaikeasukoha, mida saate kasutada ainult uute varade loomiseks. Selle töö vaikeasukoha jaoks peate looma töö vaikeasukoha tüübi, mis on tõeliselt lihtne ja lubab installida mitu vara töö vaikeasukohta. Lisateavet töö asukohtade seadistamise kohta lugege teemast [Töö asukohtade loomine](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Uue töö vaikeasukoha tüübi loomine

See protseduur näitab, kuidas luua töö vaikeasukohas kasutatavat töö vaikeasukoha vaiketüüpi.

1. Valige **Varahaldus** > **Seadistus** > **Töö asukohad** > **Töö asukoha tüübid**.
2. Valige uue töö asukoha tüübi loomiseks **Uus**.
3. Sisestage töö asukoha tüübi ID väljal **Töö asukoha tüüp**, näiteks „Vaikeväärtus” ja nimi väljale **Nimi**.
4. Valige väljal **Töö asukoha töötsükli mudel** töötsükli mudel.
5. Valige „Jah" tumblernupul **Mitu vara**, et lubada seda tüüpi kasutades rohkem vara installida töö asukohta (töö vaikeasukoht).

Luuakse ainult töö vaikeasukohas kasutatav töö vaikeasukoha tüüp. Sellele töö vaikeasukoha tüübile ei tohi lisada ühtegi muud nõuet ega piirangut.


## <a name="create-functional-location-types"></a>Töö asukohatüüpide loomine

1. Valige **Varahaldus** > **Seadistus** > **Töö asukohad** > **Töö asukoha tüübid**.
2. Valige uue töö asukoha tüübi loomiseks **Uus**.
3. Sisestage töö asukoha tüübi ID väljal **Töö asukoha tüüp** ja nimi väljale **Nimi**.
4. Valige väljal **Töö asukoha töötsükli mudel** töötsükli mudel. Lisateabe saamiseks töö asukoha töötsükli mudelite kohta lugege teemast [Töö asukoha töötsükli olekud](../setup-for-functional-locations/functional-location-stages.md).
5. Valige „Jah" tumblernupul **Mitu vara**, kui selle töö asukoha tüübi abil peaks olema võimalik installida mitu vara töö asukohta. Kui valite suvandi „Ei”, saate selle töö asukoha tüübi abil installida ainult *ühe* vara funktsionaalsesse asukohta.
6. Kui soovite, et seda tüüpi töö asukohta installitud varad kasutaksid automaatselt töö asukohaga seotud finantsdimensioone, valige „Jah” tumblernupul **Uuenda varade dimensiooni**. See tähendab, et kui muudate finantsdimensioone vormil [Töö asukohtade loomine](../functional-locations/create-functional-locations.md) ja töö asukoht kasutab töö asukoha tüüpi, kui tumblernupul on seatud olekusse „Jah”, uuendatakse sellesse töö asukohta installitud kõigi varade finantsdimensioonid.
7. Välja **Vara tüüp** kasutatakse juhul, kui soovite töö asukoha jaoks luua automaatselt *ühe* vara sama ID ja sama nimega, nagu on loodaval töö asukohal. Näiteks võib see olla asjakohane, kui loote staatilise töö asukoha (nt ehitis või torustik). Sel juhul valige vara tüüp, mida soovite kasutada automaatselt loodud vara puhul. Pidage meeles, et kui teete sellel väljal valiku, peab tumblernupp **Mitu vara** olema väärtusega „Ei”.
8. Valige kiirkaardil **Varatüübid** varatüübid, mis tuleks siduda töö asukoha tüübiga. Valige **Lisa rida** ja valige vara tüüp. Kui lisate siin varatüüpe, saab töö asukohta selle töö asukoha tüübiga installidaainult neid varasid, mis kasutavad neid varatüüpe. Kui kiirkaardil **Varatüübid** pole ühtegi varatüüpi valitud, võidakse installida kõik varatüübid.
9. Kiirkaardil **hooldusplaanid** valige hoolduskavad, mis tuleks automaatselt seadistada uutele töö asukohtadele, kasutades seda töö asukoha tüüpi. Valige **Lisa rida** ja valige hoolduskavad. Kui lisate hoolduskavad siia, saab seda töö asukoha tüüpi kasutades kasutada ainult neid kavu töö asukohas kasutada.
10. Seadistage kiirkaardil **Vara atribuudinõuded** vara atribuudid, mis tuleks uues töö asukohas automaatselt seadistada selle töö asukoha tüübi abil. Valige **Lisa rida** ja valige atribuut. Need atribuudinõuded toimivad juhistena. Neid ei kontrollita varas seadistatud atribuutide suhtes (**·** > **·** > **Varade** haldus Varad Kõik > valige vara loendilehel >**Üldine** > **Atribuudid**). Atribuutide nõuded kuvatakse, kui installite vara töö asukohtades.
11. Kiirkaardil **Lubatud tüübid** valige töö asukoha tüübid, mis peaksid kehtima peamise töö asukohatüübiga seotud töö asukoha alamtüübiga, mis kasutab valitud töö asukoha tüüpi.
12. Kiirkaardil **Atribuudid** valige töö asukoha atribuudid, mis tuleks automaatselt seadistada uutele töö asukohtadele, kasutades seda töö asukoha tüüpi. Valige **Lisa rida** ja valige atribuut.


>[!NOTE] 
>Kiirkaardil **Üldine** saate ülevaate töö asukoha tüübi jaoks seadistatud varatüüpide, hoolduskavade, vara atribuudinõuete, lubatud tüüpide, atribuutide ja töö asukohtade arvust. Väljal **Töö asukohad** kuvatakse töö asukoha tüübi töö asukohtade arv. Nupu **Kopeeri** abil saate kopeerida sätted töö asukoha tüübist valitud töö asukoha tüüpi.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]