---
title: Ostutellimuse loomine ühekordse tarnija jaoks
description: Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26c62aa72a7919c780bb709b185b48c97066c538
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836308"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Ostutellimuse loomine ühekordse tarnija jaoks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale. Hankija luuakse automaatselt koos ostutellimusega, hankija kontot pole vaja käsitsi luua. Ostutellimused loob tavaliselt ostuagent. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Eeltingimuseks on, et ühekordse hankija konto on seadistatud lehel Ostureskontro parameetrid.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Ostutellimuse loomine ühekordse tarnija jaoks
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Tehke väljal Ühekordne hankija valik Jah.
    * Hankija konto luuakse automaatselt ja määratakse ostutellimusele. Hankija konto luuakse lehe Ostureskontro parameetrid vahekaardil Üldine määratud malli põhjal.  
4. Sisestage väljale Nimi hankija nimi.
5. Klõpsake nuppu OK.
    * Ostutellimuse saab nüüd lõpetada ja seda saab töödelda, nagu iga teist tellimust. Selle tegemiseks pole mingeid erijuhiseid. Arvel kajastub tellimusega koos loodud hankija kontol toimuv kanne ja seejärel töödeldakse makse. Kui see on tehtud, võib hankija konto kustutada. Seda teeb tavaliselt ostureskontro osakond.  

