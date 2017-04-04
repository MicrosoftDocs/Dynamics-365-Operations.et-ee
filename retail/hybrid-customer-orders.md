---
title: "Hübriid klienditellimuste"
description: "Hübriid kliendi tellimusel on ühe tellimuse, mis sisaldab tooteid, mis võivad kanda poest välja Kliendi ning tooteid, mis on kiirenenud või saata hiljem."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hübriid klienditellimuste

Hübriid kliendi tellimusel on ühe tellimuse, mis sisaldab tooteid, mis võivad kanda poest välja Kliendi ning tooteid, mis on kiirenenud või saata hiljem.

Microsoft Dynamics 365 toiminguteks - jaemüük, saate valida kas teostada kõik toodete või valitud tooted kliendi tellimuse täita. Märgitud ridade nagu teha automaatselt arve tellimus on loodud toode samamoodi see on sama küsimuses on tuleb korjata üles pärast seda, kui tellimus loodi. Tasumisele kuuluv summa Hybrid määratakse tellimuste lisamine tagatisraha protsendimäära kohta valida ja laeva toote read ridade teostada täies ulatuses. Hübriid kaustade, vaheldumisi redigeerimisrežiim kliendi tellimuse ja cash and carry režiim järgmiselt:

-   Kui kõik ostukorvis tooteid on **tarne teostamiseks**, käsitletakse tellimus Cash and Carry tehinguna.
-   Kui Ostukorv on tühi või osaliselt read on seatud ühe **valida** või **laeva üleandmise**, tellimus vaadatakse kliendi tellimuse kanne.

Kui ka ostukorvi valitud ja **valida valitud**, **laeva valitud**, või **teha valitud** on valitud, ainult konkreetse ostukorvi rea on seatud selle kohaletoimetamise viis. Sel juhul peale voolu töö jätkub nagu tavaliselt. Siiski kui **valida valitud**, **valitud laeva**, või **teha valitud** ilma ostukorvi rida on valitud, uus leht avaneb, kus on loetletud kõik ostukorvi read valitud. Selles aknas saate valida mitu rida korraga kehtestamise kohaletoimetamise viis. Selle meetodi kasutamisel ridade valimiseks alistab eelmise saatmisviis, reale määratud.

<a name="see-also"></a>Vt ka
--------

[Kliendi tellimuste ülevaade](customer-orders-overview.md)


