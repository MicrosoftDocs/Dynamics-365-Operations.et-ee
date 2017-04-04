---
title: "Vöötkoodi maskide häälestamine"
description: "See teema kirjeldab, kuidas luua vöötkoodi mask märki, vöötkoodi maskid, ja kuidas määrata vöötkoodi vöötkoodide maskid."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Vöötkoodi maskide häälestamine

See teema kirjeldab, kuidas luua vöötkoodi mask märki, vöötkoodi maskid, ja kuidas määrata vöötkoodi vöötkoodide maskid.

<a name="set-up-bar-code-mask-characters"></a>Vöötkoodi maski tähemärkide häälestamine
-------------------------------

Vöötkoodi maskid kasutatakse vöötkoodide loomiseks ja vöötkoode, mis on skaneeritud müügikoha (POS) kiireks tuvastamiseks. Maskid koosneb märke, mis loovad vöötkoodide formaat tähistavad kohatäited. Vöötkoodi mask konfigureerimiseks peate luua vöötkoodi mask märki. Mine **hulgi- ja kaubanduse**&gt;**varud**&gt;**vöötkoode ja sildid**&gt;**varjata märki**. Klõpsake **uus** luua vöötkoodi mask märki. Järgmine kood andmete loomist mask märki.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Toote ID kohatäide                                                                                     |
| **Any number**       | Saab määrata number, et on raske, kodeeritakse vöötkoodi.                                                  |
| **Check digit**      | Näitab, et vöötkoodi formaat maskis vöötkoodi kasutab kontrollarv vöötkoodi kehtivuse kinnitamiseks. |
| **Size digit**       | Näitab mõeldud toote variant, mis sisaldab suurus vöötkoodi suurus.                                 |
| **Color digit**      | Näitab värvi mõeldud toote variant, mis sisaldab värvi vöötkoodi.                               |
| **Style digit**      | Näitab stiilis loodud toote variant, mis sisaldab stiili vöötkoodi.                             |
| **EAN license code** | Kohatäide EAN litsentsi välja EAN litsentsikoodid.                                                       |
| **Hind**            | Näitab hinna puhul hind varjatud vöötkoode.                                                                   |
| **Quantity**         | Näitab kogus kogus/random massina varjatud vöötkoode.                                                |
| **Employee**         | Näitab vöötkoodi segmendi vöötkoodi POS login kasutatakse töötaja ID-numbri.                                  |
| **Customer**         | Näitab kliendi ID segment.                                                                                  |
| **Andmete sisestamisel**       | *Seni teostamata.*                                                                                          |
| **Discount code**    | Näitab soodustust koodi kasutatakse lisada soodustust punkti ostutehing vöötkood             |
| **Kinkekaart**        | Näitab kingitus kaardi number või kasutate maksmiseks kinkekaarti.                                               |
| **Loyalty card**     | Lisab lojaalsust kliendi tehingu ja kasutamist lojaalsus makstes.                             |

## <a name="define-bar-code-masks"></a>Määrata vöötkoodi maskid
Pärast vöötkoodi mask tähemärki on määratud vajalikud vöötkoodi maskid, minge **hulgi- ja kaubanduse**&gt;**varud**&gt;**vöötkoode ja sildid**&gt;**vöötkoodi mask seadistus**. Sellel lehel saate määratleda vöötkoodi maskid, mis kasutavad eelnevalt määratletud märkidest. Luua vöötkoode ja see ka aitab paremini vöötkoodide skannitakse tootjaorganisatsioonid need vöötkoodi maskid kasutatavad.

1.  Klõpsake **uus** luua uue vöötkoodi mask.
2.  Sisestage väärtused on **Mask ID** ja **kirjeldus** väljad ja valige vöötkoodi mask on **tüüp** välja.
3.  Aastal ning **üldise** jao valik langeda on **standard vöötkood** väli ja määrake vöötkoodi eesliide, kui see on vajalik.
4.  Aastal ning **vöötkoodi mask segmendi** jagu, lisada vöötkoodi segmente, mida kasutatakse luua vöötkoodi.

Näiteks luua vöötkoodi mask mask ID "Toode" sooviksite tegutsete järgmiselt:

1.  Valige tüüp "Toode" luua uus kood mask.
2.  Saate valida vöötkoodi standard, näiteks "Code 39".
3.  Anda ette lisada vöötkoodi hõlpsaks tuvastamiseks kasutada. Näiteks "22".
4.  Lisa mask segment. "Toode" mask segment on märgistatud.
5.  Pikkus ette toote segment, näiteks "10". Pikkus tuleks kattu toote-ID, mida kasutatakse poes. Maski kuvatakse eelvaade on **üldise** jagu all **Mask**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Määrata vöötkoodi maskid vöötkoodid
Vöötkoodide maskid määratakse vöötkoodid, enne kui neid kasutada. Jätkata eelmises näites, et määrata vöötkoodi mask vöötkoodi, tehke järgmist:

1.  Mine **organisatsiooni haldamine**&gt;**install**&gt;**koodi**. Klõpsake **uus** luua uue vöötkoodi.
2.  Sisestage väärtused on **vöötkoodi****setup** ja ** seadistamine ** väljad.
3.  Aastal ning **üldise** osa, on **vöötkoodi tüübi** number "Code 39",. Aastal ning **Mask****ID** number varem loodud "Toode" mask,.
4.  All **suuruse**, sisestage "12".
5.  Click **Save**.

Vöötkoodi mask saab nüüd luua toodete jaoks. Eespool nimetatud meetmed on näited, kuidas luua vöötkoodi maskid toodetele, kuid nad ka selgitavad, kuidas luua vöötkoodi maskid mõnda muud toetatud vöötkoodi. Vöötkoodi maskid, liigid ja pikkused kohandatakse teie teatud keskkonnas kasutamiseks.


