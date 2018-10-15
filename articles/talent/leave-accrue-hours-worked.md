---
title: "Töötundidel põhinev kumulatiivne puhkuseaeg"
description: "Selles teemas kirjeldatakse puhkuseplaanide konfigureerimist töötundidel põhineva kumulatiivse puhkuseaja arvestamiseks."
author: Jcart1106
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f6489b84c71f2ac5a492b2d19cf087a05de8a599
ms.contentlocale: et-ee
ms.lasthandoff: 09/21/2018

---

# <a name="accrue-time-off-based-on-hours-worked"></a>Töötundidel põhinev kumulatiivne puhkuseaeg

[!include [banner](includes/banner.md)]


## <a name="overview"></a>Ülevaade

Tunnipalgaliste töötajatega organisatsioonid saavad puhkuseaega anda töötundide, mitte tööstaaži alusel organisatsioonis. Töötundide andmeid talletatakse tavaliselt aja ja kohaloleku süsteemis. Talent: Core HR-is saab need tavalised töötunnid ja ületunnitöö importida ning kasutada neid töövõtja preemia alusena.

## <a name="leave-plans"></a>Puhkuseplaanid

Puhkuseplaanis saab arvestuse tüüp olla kas töötatud kuude või töötundide arv. Kui valitud on töötunnid, saab arvestamisks kasutada kaht töötunni tüüpi: tavaline ja ületunnitöö.

Puhkuseplaani seadistamiseks kasutama töötunde tehke järgmist.

1. Klõpsake lehel **Puhkuse- ja puudumisplaanid** suvandit **Loo uus plaan**.
2. Sisestage puhkuseplaani nimi.
3. Valige plaani arvestussagedus.
5. Valige plaani alguskuupäev.
6. Valige arvestusperioodi alus ja kohaldatavusel ka töövõtjakohane kuupäev.
7. Arvestuse ajakava jaoks valige arvestuse tüübiks **Töötatudtunnid**.
8. Valige arvestuseks kasutatav tundide tüüp.
9. Sisestage töötundide arv ja seostatud arvestussumma, minimaalne saldo ja maksimaalne edasikande või hüvitise summa.

Töötunniplaanide arvestuse töötlus kasutab arvestatavate tundide määramiseks arvestussagedust koos arvestusperioodi alusega.

## <a name="annual-accrual-frequency"></a>Iga-aastane arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018–12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018–12/31/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Igakuine arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018–8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018–8/31/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Poolekuine arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8/16/2018–8/31/2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8/16/2018–8/31/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Iganädalane arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018–8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018–8/31/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Töövõtjale määratud puhkuseplaanid

Plaanide puhul, kus arvestustüübina on määratletud töötunnid, kuvatakse töövõtjale määratud puhkuseplaanid, kihi alus ja tundide tüüp. Aktiivsete plaanide puhul kuvatakse viiteks ka tegelik töötundide arv arvestusperioodiks tänase kuupäeva seisuga. 

## <a name="loading-data"></a>Andmete laadimine

Tegelikud töötunnid saab importida andmehalduses üksusega Töötunnid puhkuste ja puudumiste eest. Töögraafikute kasutamisel kontrollib import, ega tavalised töötunnid ei ületa kalendris määratletud päevale planeeritud tunde. Import kontrollib ka, ega antud päeval töötatud tundide arv ei ületa 24. 

Puhkusearvestuse protsessis kasutatavate tegelike tundide importimiseks on vaja järgmist teavet.

+ Personalinumber 
+ Töötamise kuupäev
+ Tüüp
+ Tunnid

Ühe kuupäevaga saab olla seostatud ainult üks tüüp.

| PERSONALINUMBER       | TÖÖTAMISKUUPÄEV           | TÜÜP                  | TUNNID                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Tavaline               | 8                    |       
| 000337                | 8/7/2018             | Tavaline               | 8                    |
| 000337                | 8/7/2018             | Ületunnitöö              | 3                    |
| 000337                | 8/8/2018             | Tavaline               | 8                    |
| 000337                | 8/7/2018             | Tavaline               | 8                    |
| 000337                | 8/9/2018             | Tavaline               | 8                    |

