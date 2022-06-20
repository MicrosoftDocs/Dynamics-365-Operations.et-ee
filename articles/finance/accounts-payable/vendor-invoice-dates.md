---
title: Hankija arve kuupäevad
description: Selles artiklis kirjeldatakse hankija arvetel kuvatavaid kuupäevi. Lisaks selgitatakse, kuidas süsteemi seadistada nii, et see kohandaks automaatselt postitamiskuupäeva.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 943a84407d022c2c05bc534a35a2b5d44a94653e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876408"
---
# <a name="vendor-invoice-dates"></a>Hankija arve kuupäevad

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse hankija arvetel kuvatavaid kuupäevi. Lisaks selgitatakse, kuidas süsteemi seadistada nii, et see kohandaks automaatselt postitamiskuupäeva.

Lehel **Ootel hankija arve üksikasjad** on arve päises neli kuupäeva: arve saamise kuupäev, arve kuupäev, saatmise kuupäev ja maksetähtaeg. Hankija arve loomisel sisestatakse vaikimisi järgmised kuupäevad.

- **Arve saamise kuupäev** – sellele väljale määratakse praegune süsteemi kuupäev.
- **Saatmise kuupäev** – sellele väljale määratakse praegune süsteemi kuupäev. 
- **Maksmiskuupäev** – sellel väljal olev kuupäev arvutatakse postitamiskuupäeva ja maksetingimuste alusel.
- **Arve kuupäev** – vaikimisi on see väli tühi. Saate selle välja väärtuse siiski sisestada. Sel juhul arvutatakse väljal **Maksetähtaeg** olev kuupäev ümber arve kuupäeva ja maksetingimuste alusel.

Mõnikord võib hankija arve olla pärast perioodi sulgemist pikka aega ootel. Kui see on postitamiseks valmis, kasutatakse endiselt eelmise postitamisperioodi vana postitamiskuupäeva. See periood on aga nüüdseks lõppenud. Seetõttu peab võlgnevuste (AP) ametnik käsitsi muutma kõigi eelnevalt loodud ootel olevate arvete kõik saatmiskuupäevad uueks saatmisperioodiks.

Funktsioon, mida selles artiklis kirjeldatakse, võimaldab teil seadistada süsteemi nii, et see korrigeerib automaatselt sisestuskuupäeva vastavalt ärinõuetele.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameeter hankija arve konteerimiskuupäeva automaatseks kohandamiseks

Järgige neid samme, et võimaldada süsteemil hankija arvete konteerimiskuupäeva automaatselt kohandada.

1.  Avage **Arveldusarve \> Seadistus \> Arveldusarve parameetrid**.
2.  Valige vahekaardi **Pearaamat ja käibemaks** väljal **Kohanda kirjendamiskuupäeva automaatselt** üks järgmistest väärtustest.

    - **Muutuseta** – süsteem ei muuda postitamise ajal automaatselt postitamise kuupäeva. See väärtus on vaikimisi valitud.
    - **Muuda alati postitamiskuupäev süsteemi kuupäevaks** – süsteem muudab postitamise ajal automaatselt postitamiskuupäeva süsteemi kuupäevaks.
    - **Muutke postitamiskuupäev süsteemikuupäevaks, kui postitamiskuupäeva periood on suletud või ootel** – süsteem muudab postitamise ajal postitamiskuupäeva süsteemi kuupäevaks, kuid ainult siis, kui postitamiskuupäeva vastava perioodi olek on **Suletud** või **Ootel**.
    - **Muutke postitamiskuupäev uue perioodi esimeseks päevaks, kui postitamiskuupäeva periood on suletud või ootel** – süsteem muudab postitamiskuupäeva uue avatud perioodi esimeseks päevaks, kuid ainult siis, kui postitamiskuupäeva vastava perioodi olek on **Suletud** või **Ootel**.

> [!NOTE]
> Kui uus automaatselt korrigeeritud sisestuskuupäev on uues rahandusaastas, siis arve sisestuskuupäeva ei uuendata. Kasutajale kuvatakse tõrge "Finantsaasta on muutunud. Palun kontrollige sisestuskuupäeva ja sisestage see uuesti." Arve sisestamise kuupäev tuleb sisestamiseks uuendada uuele finantsaasta kuupäevale.

## <a name="impact-of-posting-date-changes"></a>Postituskuupäeva muutmise mõju

Kui ootel hankija arve konteerimiskuupäeva muudetakse, on muudatusel järgmised mõjud.

- **Tähtaeg**

    - Kui väli **Arve kuupäev** on tühi, arvutatakse maksetähtaeg ümber uue konteerimiskuupäeva ja maksetingimuste alusel.
    - Kui väli **Arve kuupäev** on varasemalt määratud, ei mõjuta konteerimispäeva muudatus maksetähtaega.

- **Skonto kuupäev**

    - Kui väli **Arve kuupäev** on tühi, kasutatakse rahasoodustuse arvutamisel uut postitamiskuupäeva.
    - Kui väli **Arve kuupäev** oli varem määratud, siis sularahasoodustust ei muudeta.

- **Valuutakurss** – vahetuskursi kuupäev määratakse valiku **Värskenda hankija raamatupidamisarvestust arve kuupäeva abil** valikuga **Arve** vahekaardil lehe **Makstavate kontode parameetrid** vahekaardil (**Maksekonto \> Seadistamine \> Makstava konto parameetrid**).

    - Kui see suvand on seatud väärtusele **Jah**, kasutatakse arve kuupäeva ja konteerimiskuupäeva muudatus ei mõjuta vahetuskurssi.
    - Kui see suvand on seatud väärtusele **Ei**, kasutatakse vahetuskursi arvutamiseks postitamiskuupäeva. Kui konteerimiskuupäeva uuendatakse, arvutatakse raamatupidamis- ja aruandlussummad ümber. Seetõttu tuleb sobivuse kinnitamine uuesti läbi viia.

## <a name="validation"></a>Kinnitus

Arve töötlemist mõjutavad lehe **Maksekonto parameetrid** vahekaardil **Arve** (**Maksekonto \> Seadistamine \> Maksekonto parameetrid**) kaks muud välja:

- Kui väli **Kontrolli kasutatud arve numbrit** on seatud väärtusele **Keeldu eelarveaasta jooksul duplikaadid**, kasutab süsteem arvete konteerimise ajal duplikaatide kontrollimiseks konteerimiskuupäeva.
- Kui väli **Nõua hankija arvel dokumendi kuupäeva** on seatud väärtusele **Veavalik**, on väli **Arve kuupäev ootel arve päises** kohustuslik. Kui arve kuupäev on konteerimiskuupäevast hilisem, kuvab süsteem veateate.
