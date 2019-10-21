---
title: Hüvitisruudustike häälestamine
description: Tasuruudustikke kasutatakse põhipalgaplaanide palgastruktuuri määratlemiseks ja säilitamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0caebb2dfbff12545610aa6438dccbec84db3f9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190346"
---
# <a name="set-up-compensation-grids"></a>Hüvitisruudustike häälestamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tasuruudustikke kasutatakse põhipalgaplaanide palgastruktuuri määratlemiseks ja säilitamiseks. Tasuruudustikke saab mitme plaani vahel jagada või uue tasuplaani loomisel kopeerida.  Enne tasuruudustiku koostamist tuleb seadistada tasemed ja viitepunktid. Selles näites loome uue tasuruudustiku tüübi Tase, kasutades tasemete ja viitepunktide demoandmeid. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="set-up-information-about-the-compensation-grid"></a>Seadistage teave tasuruudustiku kohta.
1. Avage Personaliarvestus > Hüvitus > Põhipalk > Hüvituse ruudustikud.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Ruudustik.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige suvand väljalt Tüüp.
6. Valige või sisestage väärtus väljal Viite seadistus.
7. Valige või sisestage väärtus väljal Valuuta.
8. Sisestage väärtus väljale Valuuta.
9. Sisestage kuupäev väljale Jõustumiskuupäev.

## <a name="add-levels-to-the-compensation-structure"></a>Tasustruktuurile tasemete lisamine
1. Klõpsake valikut Tasustruktuur.
2. Märkige loendis valitud rida.
3. Valige või sisestage väärtus väljal Tase.
4. Klõpsake Uus.
5. Märkige loendis valitud rida.
6. Valige või sisestage väärtus väljal Tase.
7. Klõpsake Uus.
8. Märkige loendis valitud rida.
9. Valige või sisestage väärtus väljal Tase.
10. Klõpsake Uus.
11. Märkige loendis valitud rida.
12. Valige või sisestage väärtus väljal Tase.
13. Klõpsake Uus.
14. Märkige loendis valitud rida.
15. Valige või sisestage väärtus väljal Tase.

## <a name="fill-in-the-compensation-structure-with-values"></a>Tasustruktuuri täitmine väärtustega
1. Märkige loendis valitud rida.
    * Sellel ajal saab tasuväärtused igale tabel väljale sisestada või kasutada hulgimuutmise funktsiooni, et täita hõlpsasti mitu välja ja teha põhiarvutusi.  
2. Klõpsake valikut Massmuudatus.
    * Selle tabeli puhul rakendame kõigepealt esimese taseme keskpunkti väärtuse kõigile tabeli väljadele. See on tasutabeli alus.  
3. Valige suvand väljal Korrigeerimise tüüp.
4. Sisestage arv väljale Korrigeerimissumma.
5. Märkige või tühjendage loendis kõik read.
6. Klõpsake käsku Rakenda ruudustikule.
    * Nüüd kasutame hulgimuutmise funktsiooni, muutes iga järgmise taseme summasid teatud protsendi või summa võrra. Selles näites on astmete keskpunktide vahe 12,5%.  
7. Valige suvand väljal Korrigeerimise tüüp.
8. Sisestage arv väljale Korrigeerimissumma.
9. Otsige loendist ja valige soovitud kirje.
10. Otsige loendist ja valige soovitud kirje.
11. Otsige loendist ja valige soovitud kirje.
12. Otsige loendist ja valige soovitud kirje.
13. Klõpsake käsku Rakenda ruudustikule.
14. Otsige loendist ja valige soovitud kirje.
15. Otsige loendist ja valige soovitud kirje.
16. Otsige loendist ja valige soovitud kirje.
17. Klõpsake käsku Rakenda ruudustikule.
18. Otsige loendist ja valige soovitud kirje.
19. Otsige loendist ja valige soovitud kirje.
20. Klõpsake käsku Rakenda ruudustikule.
21. Otsige loendist ja valige soovitud kirje.
22. Klõpsake käsku Rakenda ruudustikule.
    * Nüüd kasutame hulgimuutmise funktsiooni, et kohandada iga taseme miinimum- ja maksimumpunkti. Selles näites kasutatakse erinevust 50%, seega kohandatakse miinimumpunkti –20% ja maksimumpunkti +20% võrra.  
23. Sisestage arv väljale Korrigeerimissumma.
24. Valige või sisestage väärtus väljal Viitepunkt.
25. Märkige või tühjendage loendis kõik read.
26. Klõpsake käsku Rakenda ruudustikule.
27. Sisestage arv väljale Korrigeerimissumma.
28. Valige või sisestage väärtus väljal Viitepunkt.
29. Märkige või tühjendage loendis kõik read.
30. Klõpsake käsku Rakenda ruudustikule.

