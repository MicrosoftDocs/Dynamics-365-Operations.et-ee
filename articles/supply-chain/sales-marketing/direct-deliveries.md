---
title: Otsetarned
description: Artikkel sisaldab teavet otsetarnete kohta. Otsetarned on tarned, mis saadetakse hankijalt otse teie kliendile.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7dd562a67f891c6943db00a6f8cf514bec19677
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572573"
---
# <a name="direct-deliveries"></a>Otsetarned

[!include [banner](../includes/banner.md)]

Artikkel sisaldab teavet otsetarnete kohta. Otsetarned on tarned, mis saadetakse hankijalt otse teie kliendile.

Otsetarned säästavad tarneaega ja vähendavad varude hoidmisega seotud kulusid, kuna te ei hoia tooteid enne kliendile tarnimist oma laos.  

Otsetarneid saab luua lehelt **Müügitellimus**. Looge esmalt müügitellimus ja tellimuse read. Seejärel tehke tegumiriba vahekaardil **Müügitellimus** valik **Otsetarne**. Lõpuks määrake read, mida tuleb käsitleda otsetarnena. Luuakse link otsetarne müügitellimuse ridade ja vastavate ostutellimuste ridade vahel.  

**Märkus.** Kui osa tellitud kogusest on juba tarnitud, tuleb järelejääv kogus ära jagada. Looge otse tarnitavale kogusele uus rida ja lahutage see kogus algsel real olevast kogusest. Näiteks kui algne kogus oli 15 ja viis ühikut on tarnitud, tuleb luua uus rida järelejäänud 10 ühiku jaoks ning seejärel vähendada algset kogust selle summa võrra.  

Pärast müügitellimuse ridade ja ostutellimuse ridade vahelise otsetarne lingi loomist saate värskendada müügitellimust saatelehe abil. Värskendage saatelehte või arvet ostutellimuses. Müügitellimuse arvet saate värskendada lehel **Müügitellimus**. Arve värskendamisel ei tohi muuta müügitellimuse kogust nii, et sellel on suurem kogus kui vastuvõetuna registreeritud. Näiteks müügitellimuse real on 10 ühikut, kuid saatelehega on värskendatud vaid viis müügitellimuse real olevat ühikut. Kui teete müügitellimuse arve värskendamisel loendis **Kogus** valiku **Kõik**, värskendatakse arvet vaid kaupade puhul, mis on füüsiliselt kätte saadud või töölehega värskendatud. Tervet müügitellimuse rida ei värskendata.

## <a name="delivery-date"></a>Tarnekuupäev
Kui värskendate müügitellimuse real välja **Nõutav vastuvõtukuupäev**, muudetakse ka välja **Tarnekuupäev** vastaval ostutellimuse real. Samamoodi, kui uuendate ostutellimuse real välja **Kinnitatud**, värskendatakse ka väljad **Kinnitatud vastuvõtukuupäev** ja **Kinnitatud lähetuskuupäev** vastaval müügitellimuse real.

## <a name="delivery-address"></a>Tarneaadress
Ostutellimuse tarneaadress on tavaliselt ettevõtte aadress. Kui aga loote otsetarne, sisestate tarneaadressiks kliendi aadressi. Kui muudate ostutellimuse real tarneaadressi tarne tüübiga **Otsetarne**, värskendatakse ka vastava müügitellimuse rea tarneaadressi. Kui muudate tarneaadressi müügitellimuse real, värskendatakse ka ostutellimuse rea tarneaadressi.

## <a name="deleting-order-lines"></a>Tellimuse ridade kustutamine
Kui proovite kustutada müügitellimuse rida tarnetüübiga **Otsetarne**, ütleb teateaken, et ostutellimuse read on kustutatava reaga seotud. Kui müügitellimuse rida on osaliselt tarnitud, ei saa müügitellimuse rida või sellega ühendatud ostutellimuste ridu kustutada.

## <a name="warehouse"></a>Ladu
Kui loote otsetellimuse, ei saabu kaup, mida müüte, kunagi füüsiliselt teie lattu. Teil tuleb siiski müügitellimuse real ladu määrata. Samamoodi võivad kauba mudeligrupis olla määratud komplekteerimisnõuded. Kui müügitellimus on otsetarne, eiratakse neid nõudeid, kuna kaup ei saabu füüsiliselt kunagi teie lattu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]