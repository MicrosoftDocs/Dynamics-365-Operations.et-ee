---
title: Põhivara väärtusmudeli ja kulumiraamatu ühendamine
description: 'Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.'
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9b11edcbf03b0917e35d9cef03834629b7b67fad
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674922"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Põhivara väärtusmudeli ja kulumiraamatu ühendamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse põhivarade praeguse raamatu funktsioone. See funktsioon põhineb väärtusmudeli funktsionaalsusel, mis oli saadaval varasemates versioonides, kuid sisaldab ka kõiki funktsioone, mida varem pakuti ainult amortisatsiooniraamatutes.

Raamatufunktsiooni abil saate kasutada ühtset lehekülgede, päringute ja aruannete komplekti kõigi organisatsiooni põhivaraprotsesside kohta. Selles teemas olevates tabelites kirjeldatakse kulumiraamatute ja väärtusmudelite varasemaid funktsioone koos raamatute uute funktsioonidega.

## <a name="setup"></a>Häälestus
Vaikimisi sisestavad raamatud nii pearaamatusse (PR) kui ka põhivara alammoodulisse. Raamatutel on uus valik **Pearaamatusse sisestamine**, mis võimaldab teil keelata pearaamatusse sisestamise ja sisestada ainult põhivara alammoodulisse. See funktsioon sarnaneb kulumiraamatute varasemale sisestamise käitumisele. Töölehe nimede seadistusel on uus sisestamiskiht, mille nimetus on Pole. Sisestamiskiht lisati spetsiifiliselt põhivara kannetele. Sisestamaks kandeid raamatutele, mis ei sisesta pearaamatusse, peate kasutama töölehe nime, mille sisestamiskiht on määratud valikul **Pole**.


| &nbsp;                                           | Kulumiraamat               | Väärtusmudel                     | Raamat (Uus)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Pearaamatusse sisestamine                                   | Mitte kunagi                           | Alati                          | Pearaamatusse sisestamise valikud                                |
| Sisestamiskihid                                   | Pole kohaldatav                  | 3: Praegune, Toimingud ja Maks | 11: Praegune, Toimingud, Maks, 7 kohandatud kihti ja Pole |
| Töölehe nimed                                    | Kulumiraamatu töölehtede nimed | Pearaamat - töölehe nimed              | Pearaamat - töölehe nimed                                      |
| Tuletatud raamatud                                    | Pole lubatud                     | Lubatud                         | Lubatud                                                 |
| Kulumireeglite alistamine vara tasandil | Lubatud                         | Pole lubatud                     | Lubatud                                                 |

## <a name="processes"></a>Protsessid
Protsessid kasutavad nüüd ühist lehte. Mõned protsessid on lubatud ainult juhul, kui valik **Pearaamatusse sisestamine** on raamatu seadistuses määratud valikule **Ei**.

| &nbsp;                                           | Kulumiraamat               | Väärtusmudel                     | Raamat (Uus)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Kande kirje              | Kulumiraamatu tööleht | Põhivara tööleht | Põhivara tööleht                      |
| Lisakulum             | Lubatud                   | Pole lubatud         | Lubatud                                  |
| Kustuta kannete ajalugu | Lubatud                   | Pole lubatud         | Lubatud, kui te ei sisestata pearaamatusse |
| Massvärskendus                    | Lubatud                   | Pole lubatud         | Lubatud, kui te ei sisestata pearaamatusse |

## <a name="inquiries-and-reports"></a>Päringud ja aruanded
Päringud ja aruanded toetavad kõiki raamatuid. Aruanded, mis ei ole lisatud järgmisesse tabelisse, toetasid varasemalt nii kulumiraamatuid kui ka väärtusmudeleid ja toetavad nüüd jätkuvalt kõiki raamatu tüüpe. Väli **Sisestamiskiht** on lisatud ka aruannetesse, et saaksite hõlpsamalt tuvastada kande sisestused.

| &nbsp;                                           | Kulumiraamat               | Väärtusmudel                     | Raamat (Uus)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Päringud                             | Kulumiraamatu kanded | Põhivarakanded | Põhivarakanded |
| Põhivara aruanne                 | Pole lubatud                    | Lubatud                  | Lubatud                  |
| Põhivara alus                     | Lubatud                        | Pole lubatud              | Lubatud                  |
| Põhivara seotavus kvartali keskel | Lubatud                        | Pole lubatud              | Lubatud                  |

## <a name="upgrade"></a>Täiendamine
Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri. Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse. Siiski liigutatakse kulumiraamatud raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**. Kulumiraamatu töölehe nimed liigutatakse pearaamatu töölehele, mille nimel on sisestamiskiht määratud sättele **Pole**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
