--- 
title: Klientide ja kliendi pangakontode seadistamine ISO20022 otsekorralduste jaoks
description: "See ülesanne annab ülevaate kliendi pangakonto ja kliendi otsekorralduse loa seadistamise kohta, mis on nõutav ISO20022 otsekorralduse kliendi maksefaili loomiseks."
author: mrolecki
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 22fadf126dfa884520bc2fe6f94bc3fe3b612f77
ms.openlocfilehash: 86c3f62e17d4955c12d09b512624eb5f576a9cd3
ms.contentlocale: et-ee
ms.lasthandoff: 10/31/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Klientide ja kliendi pangakontode seadistamine ISO20022 otsekorralduste jaoks

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See ülesanne annab ülevaate kliendi pangakonto ja kliendi otsekorralduse loa seadistamise kohta, mis on nõutav ISO20022 otsekorralduse kliendi maksefaili loomiseks. Olenevalt seadistatud kliendi maksevormingutest võib olla kliendi või kliendi pangakonto puhul vaja lisateavet, mida see protseduur ei sisalda. 

Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmaseks aadressiks on Saksamaa, andmeid.



See on neljas viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.


## <a name="set-up-a-customer-bank-account"></a>Kliendi pangakonto seadistamine
1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Konto väärtuse DE-010 järgi.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake toimingupaanil suvandit Klient.
5. Klõpsake valikut Pangakontod.
6. Klõpsake valikut Uus.
7. Sisestage väärtus väljale Pangakonto.
8. Sisestage väärtus väljale Nimi.
    * Näiteks sisestage EUR-pank.  
9. Sisestage väärtus väljale Pangagrupid või valige see.
10. Sisestage väärtus väljale IBAN.
    * Näiteks sisestage DE36200400000628808808.  
11. Sisestage väärtus väljale SWIFT-kood.
    * Näiteks sisestage COBADEFFXXX.  Pange tähele, et SWIFT \ BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.  
12. Klõpsake nuppu Salvesta.
13. Sulgege leht.
14. Klõpsake nuppu Redigeeri.
15. Laiendage jaotist Makse vaikeandmed.
16. Sisestage väärtus väljale Pangakonto või valige see.

## <a name="add-a-direct-debit-mandate"></a>Otsekorralduse loa lisamine
1. Laiendage jaotist Otsekorralduse load.
2. Klõpsake vahekaarti Lisa.
3. Sisestage väärtus väljale Kreeditori pangakonto või valige see.
    * Valige näiteks DEMF OPER.  
4. Sisestage kuupäev väljale Allkirjastamise kuupäev.
5. Kuupäevavärskenduse kinnitamiseks klõpsake nuppu Jah.
6. Sisestage väärtus väljale Allkirjastamise koht või valige see.
7. Sisestage number väljale Eeldatav maksete arv.
8. Klõpsake nuppu OK.
9. Klõpsake nuppu Salvesta.


