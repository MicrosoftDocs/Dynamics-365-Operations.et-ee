---
title: Hüvitisruudustike häälestamine
description: Tasuruudustikke kasutatakse põhipalgaplaanide palgastruktuuri määratlemiseks ja säilitamiseks.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9119c15cf80b9ebb9bed83ac438f24249aa4aa2f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691669"
---
# <a name="set-up-compensation-grids"></a>Hüvitisruudustike häälestamine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tasuruudustikke kasutatakse põhipalgaplaanide palgastruktuuri määratlemiseks ja säilitamiseks. Tasuruudustikke saab mitme plaani vahel jagada või uue tasuplaani loomisel kopeerida.  Enne tasuruudustiku koostamist tuleb seadistada tasemed ja viitepunktid. Selles näites loome uue tasuruudustiku tüübi Tase, kasutades tasemete ja viitepunktide demoandmeid. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="set-up-information-about-the-compensation-grid"></a>Seadistage teave tasuruudustiku kohta.
1. Avage **Inimressursid** > **Hüvitus** > **Põhipalk** > **Hüvituse ruudustikud**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Ruudustik**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige suvand väljalt **Tüüp**.
6. Valige või sisestage väärtus väljal **Viite** seadistus.
7. Väljale **Valuuta** sisestage või valige väärtus.
8. Väljale **Jõustumiskuupäev** sisestage kuupäev.

## <a name="add-levels-to-the-compensation-structure"></a>Tasustruktuurile tasemete lisamine
1. Klõpsake valikut **Tasustruktuur**.
2. Märkige loendis valitud rida.
3. Valige või sisestage väärtus väljal **Tase**.
4. Klõpsake valikut **Uus**.
5. Märkige loendis valitud rida.
6. Valige või sisestage väärtus väljal **Tase**.
7. Klõpsake valikut **Uus**.
8. Märkige loendis valitud rida.
9. Valige või sisestage väärtus väljal **Tase**.
10. Klõpsake valikut **Uus**.
11. Märkige loendis valitud rida.
12. Valige või sisestage väärtus väljal **Tase**.
13. Klõpsake valikut **Uus**.
14. Märkige loendis valitud rida.
15. Valige või sisestage väärtus väljal **Tase**.

## <a name="fill-in-the-compensation-structure-with-values"></a>Tasustruktuuri täitmine väärtustega
1. Märkige loendis valitud rida.
    * Sellel ajal saab tasuväärtused igale tabel väljale sisestada või kasutada hulgimuutmise funktsiooni, et täita hõlpsasti mitu välja ja teha põhiarvutusi.  
2. Klõpsake valikut **Massmuudatus**.
    * Selle tabeli puhul rakendame kõigepealt esimese taseme keskpunkti väärtuse kõigile tabeli väljadele. See on tasutabeli alus.  
3. Valige suvand väljal **Korrigeerimise tüüp**.
4. Sisestage arv väljale **Korrigeerimissumma**.
5. Märkige või tühjendage loendis kõik read.
6. Klõpsake käsku **Rakenda ruudustikule**.
    * Nüüd kasutame hulgimuutmise funktsiooni, muutes iga järgmise taseme summasid teatud protsendi või summa võrra. Selles näites on astmete keskpunktide vahe 12,5%.  
7. Valige suvand väljal **Korrigeerimise tüüp**.
8. Sisestage arv väljale **Korrigeerimissumma**.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake käsku **Rakenda ruudustikule**.
    * Nüüd kasutame hulgimuutmise funktsiooni, et kohandada iga taseme miinimum- ja maksimumpunkti. Selles näites kasutatakse erinevust 50%, seega kohandatakse miinimumpunkti –20% ja maksimumpunkti +20% võrra.  
11. Sisestage arv väljale **Korrigeerimissumma**.
12. Valige või sisestage väärtus väljal **Viitepunkt**.
13. Märkige või tühjendage loendis kõik read.
14. Klõpsake käsku **Rakenda ruudustikule**.
15. Sisestage arv väljale **Korrigeerimissumma**.
16. Valige või sisestage väärtus väljal **Viitepunkt**.
17. Märkige või tühjendage loendis kõik read.
18. Klõpsake käsku **Rakenda ruudustikule**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
