---
title: "Põhivara väärtusmudeli ja kulumiraamatu ühendamine"
description: "Varasemates väljaannetes oli kahe hindamise mõiste põhivarade - väärtusmudelid ja kulumiraamatud. 365 Microsoft Dynamics lubamise toimingute 1611 väärtusmudeli funktsiooni ja kulumi raamat funktsioonile on ühendatud sama mõiste, mis on tuntud kui raamat."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c8c005c7f5ede54ce0b6c8114cac69e2551d467
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Põhivara väärtusmudeli ja kulumiraamatu ühendamine

Varasemates väljaannetes oli kahe hindamise mõiste põhivarade - väärtusmudelid ja kulumiraamatud. 365 Microsoft Dynamics lubamise toimingute 1611 väärtusmudeli funktsiooni ja kulumi raamat funktsioonile on ühendatud sama mõiste, mis on tuntud kui raamat.

Uued raamatu funktsioonid põhinevad varasema väärtusmudeli funktsioonidel, kui hõlmab ka kõiki funktsioone, mis olid varasemalt antud ainult kulumiraamatutes. [![Raamatu väärtuse väärtusmudeli ja kulumiraamatu aadressiraamatu funktsioone ühinevad](./media/fixed-assets.png)](./media/fixed-assets.png) tõttu sellest koostest funktsioonis saate lehti, päringute ja aruannete ühtsed oma põhivara protsessidele. Selles teemas olevates tabelites kirjeldatakse kulumiraamatute ja väärtusmudelite varasemaid funktsioone koos raamatute uute funktsioonidega.

## <a name="setup"></a>Häälestus
Vaikimisi sisestavad raamatud nii pearaamatusse (PR) kui ka põhivara alammoodulisse. Raamatutel on uus valik **Pearaamatusse sisestamine**, mis võimaldab teil keelata PR-sse sisestamise ja sisestada ainult põhivara alammoodulisse. See funktsioon sarnaneb kulumiraamatute varasemale sisestamise käitumisele. Töölehe nimede seadistusel on uus sisestamiskiht, mille nimetus on Pole. Sisestamiskiht lisati spetsiifiliselt põhivara kannetele. Sisestamaks kandeid raamatutele, mis ei sisesta pearaamatusse, peate kasutama töölehe nime, mille sisestamiskiht on määratud valikul **Pole**.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Kulumiraamat               | Väärtusmudel                     | Raamat (Uus)                                              |
| Pearaamatusse sisestamine                                   | Mitte kunagi                           | Alati                          | Valik pearaamatusse sisestamiseks                                |
| Sisestamiskihid                                   | Pole kohaldatav                  | 3: Praegune, Toimingud ja Maks | 11: Praegune, Toimingud, Maks, 7 kohandatud kihti ja Pole |
| Töölehe nimed                                    | Kulumiraamatu töölehtede nimed | PR – töölehe nimed              | PR – töölehe nimed                                      |
| Tuletatud raamatud                                    | Pole lubatud                     | Lubatud                         | Lubatud                                                 |
| Kulumireeglite alistamine vara tasandil | Lubatud                         | Pole lubatud                     | Lubatud                                                 |

## <a name="processes"></a>Protsessid
Protsessid kasutavad nüüd ühist lehte. Mõned protsessid on lubatud ainult juhul, kui valik **Pearaamatusse sisestamine** on raamatu seadistuses määratud valikule **Ei**.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Kulumiraamat         | Väärtusmudel         | Raamat (Uus)                               |
| Kande kirje              | Kulumiraamatu tööleht | Põhivara tööleht | Põhivara tööleht                      |
| Lisakulum             | Lubatud                   | Pole lubatud         | Lubatud                                  |
| Kustuta kannete ajalugu | Lubatud                   | Pole lubatud         | Lubatud, kui te ei sisestata pearaamatusse |
| Massvärskendus                    | Lubatud                   | Pole lubatud         | Lubatud, kui te ei sisestata pearaamatusse |

## <a name="inquiries-and-reports"></a>Päringud ja aruanded
Päringud ja aruanded toetavad kõiki raamatuid. Aruanded, mis ei ole lisatud järgmisesse tabelisse, toetasid varasemalt nii kulumiraamatuid kui ka väärtusmudeleid ja toetavad nüüd jätkuvalt kõiki raamatu tüüpe. Väli **Sisestamiskiht** on lisatud ka aruannetesse, et saaksite hõlpsamalt tuvastada kande sisestused.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Kulumiraamat              | Väärtusmudel              | Raamat (Uus)               |
| Päringud                             | Kulumiraamatu kanded | Põhivarakanded | Põhivarakanded |
| Põhivara aruanne                 | Pole lubatud                    | Lubatud                  | Lubatud                  |
| Põhivara alus                     | Lubatud                        | Pole lubatud              | Lubatud                  |
| Põhivara seotavus kvartali keskel | Lubatud                        | Pole lubatud              | Lubatud                  |

## <a name="upgrade"></a>Täiendamine
Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri. Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse. Siiski liigutatakse kulumiraamatud raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**. Kulumiraamatu töölehe nimed liigutatakse pearaamatu töölehele, mille nimel on sisestamiskiht määratud sättele **Pole**.


