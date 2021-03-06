---
title: Põhivara väärtusmudeli ja kulumiraamatu ühendamine
description: 'Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.'
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f027a856dbd596ede84c39e30ee2227aab9329f2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826734"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Põhivara väärtusmudeli ja kulumiraamatu ühendamine

[!include [banner](../includes/banner.md)]

Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.

Uued raamatu funktsioonid põhinevad varasema väärtusmudeli funktsioonidel, kui hõlmab ka kõiki funktsioone, mis olid varasemalt antud ainult kulumiraamatutes. [![Raamat väärtusmudeli ja kulumiraamatu funktsioonide ühendamisena](./media/fixed-assets.png)](./media/fixed-assets.png) Selle ühendamise tõttu saate nüüd kasutada lehtede, päringute ja aruannete üksikut kogumit kõikide teie põhivara protsesside jaoks. Selles teemas olevates tabelites kirjeldatakse kulumiraamatute ja väärtusmudelite varasemaid funktsioone koos raamatute uute funktsioonidega.

## <a name="setup"></a>Häälestus
Vaikimisi sisestavad raamatud nii pearaamatusse (PR) kui ka põhivara alammoodulisse. Raamatutel on uus valik **Pearaamatusse sisestamine**, mis võimaldab teil keelata PR-sse sisestamise ja sisestada ainult põhivara alammoodulisse. See funktsioon sarnaneb kulumiraamatute varasemale sisestamise käitumisele. Töölehe nimede seadistusel on uus sisestamiskiht, mille nimetus on Pole. Sisestamiskiht lisati spetsiifiliselt põhivara kannetele. Sisestamaks kandeid raamatutele, mis ei sisesta pearaamatusse, peate kasutama töölehe nime, mille sisestamiskiht on määratud valikul **Pole**.

| &nbsp;                                           | Kulumiraamat               | Väärtusmudel                     | Raamat (Uus)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Pearaamatusse sisestamine                                   | Mitte kunagi                           | Alati                          | Valik pearaamatusse sisestamiseks                                |
| Sisestamiskihid                                   | Pole kohaldatav                  | 3: Praegune, Toimingud ja Maks | 11: Praegune, Toimingud, Maks, 7 kohandatud kihti ja Pole |
| Töölehe nimed                                    | Kulumiraamatu töölehtede nimed | PR – töölehe nimed              | PR – töölehe nimed                                      |
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