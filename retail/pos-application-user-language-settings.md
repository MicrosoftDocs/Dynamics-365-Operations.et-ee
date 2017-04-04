---
title: "Kassa rakenduse ja kasutaja keelesätted"
description: "Selles teemas kirjeldatakse Keeleseadete muutmine jaemüügi kaasaegne POS (MPOS) ja pilve POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Kassa rakenduse ja kasutaja keelesätted

Selles teemas kirjeldatakse Keeleseadete muutmine jaemüügi kaasaegne POS (MPOS) ja pilve POS.

<a name="overview"></a>Ülevaade
========

Jaemüügi kaasaegne POS (MPOS) ja pilve POS toetavad keskkonnad, kus poe ja kasutaja seaded sõltuvad keelesätted ja tõlked. Näiteks poes asuda piirkonnas, kus inglise keel on levinuim oma klientidele, kuid mõned töötajad eelistavad kasutada taotluse Prantsuse tõlked.

## <a name="data-language"></a>Andmete keel
Sõltumata kasutaja seaded, MPOS ja pilve POS näidatakse alati kasutada poe keelesätete kasutatakse andmete tõlked. See tagab, et kõik kasutajad ja külastajad on järjepidev kogemus.  Andmed on näiteks:

-   Tooted
-   atribuudid ja väärtused,
-   kategooriate nimed,
-   prinditud või meilitsi saadetud kannete sissetulekud,
-   makseviiside nimed,
-   rea kuvateated.

Lao keeles kasutatakse ka peamine POS sisselogimine, kuna kasutaja ei ole teada enne sisselogimist. Kui tõlget pole poe keeles saadaval, naaseb tootjaorganisatsioonid ettevõtte keel.

### <a name="configuring-the-stores-language-setting"></a>Kaupluse keelesätte konfigureerimine

Lao keel säte on alates **kõik kauplustes** kohta on **kauplusesse** lehekülg alusel ** üldise &gt;piirkonnasätteid &gt;keel. * Kasutage rippmenüüst ette iga poe keele valimiseks.

## <a name="user-interface-language"></a>Kasutajaliidese keel
POS kasutaja keel säte määratleb kasutatava rakenduse kasutajaliidese tõlked. See hõlmab kõik sildid, menüüd ja nimekirjad, mida ei loeta andmete. Erandiks on tekst, mis kuvatakse POS nuppu võrgustikud. Nuppu võrgud ei toeta tõlked, nii et nad ilmuvad alati tekst nuppu määratletud. Tõlgitud nupud toetamiseks pead koopia ja säilitada eraldi nupp võrkude ja neid vastavalt vajadusele kasutajatele määrata.

### <a name="configuring-the-users-language-setting"></a>Kasutaja keelesätte konfigureerimine

POS kasutaja keel säte on alates **töölised on** kohta on **töötaja** all lehekülg **jaemüügi &gt;keele**.  See ei ole määratud profiili põhitabelis.  Seda sätet kasutatakse tootjaorganisatsioonide. Kui kasutaja keelt ei määrata või määratakse mõni keel, millele ei ole tõlget saadaval, ennistatakse kassas kaupluse keel.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Kasutajaliidese keele** ** **      | **Andmete keel (tooted, kviitungi vormingud, rea kuva jne)** |
| **Ettevõte** | Vaikimisi                    | Vaikimisi                                                           |
| **Kauplus**   | Tühistab ettevõtte          | Tühistab ettevõtte                                                 |
| **User**    | Tühistab kaupluse või ettevõtte | Mitte kunagi                                                             |




