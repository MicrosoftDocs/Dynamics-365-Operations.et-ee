---
title: Ostutellimuse loomine ühekordse tarnija jaoks
description: Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e6c8283290564d930418c1832bbd285532445ff0e69db8f78d13542c8232e97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720296"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Ostutellimuse loomine ühekordse tarnija jaoks

[!include [banner](../../includes/banner.md)]

Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale. Hankija luuakse automaatselt koos ostutellimusega, hankija kontot pole vaja käsitsi luua. Ostutellimused loob tavaliselt ostuagent. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Eeltingimuseks on, et ühekordse hankija konto on seadistatud lehel Ostureskontro parameetrid.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Ostutellimuse loomine ühekordse tarnija jaoks
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Tehke väljal Ühekordne hankija valik Jah.
    * Hankija konto luuakse automaatselt ja määratakse ostutellimusele. Hankija konto luuakse lehe Ostureskontro parameetrid vahekaardil Üldine määratud malli põhjal.  
4. Sisestage väljale Nimi hankija nimi.
5. Klõpsake nuppu OK.
    * Ostutellimuse saab nüüd lõpetada ja seda saab töödelda, nagu iga teist tellimust. Selle tegemiseks pole mingeid erijuhiseid. Arvel kajastub tellimusega koos loodud hankija kontol toimuv kanne ja seejärel töödeldakse makse.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]