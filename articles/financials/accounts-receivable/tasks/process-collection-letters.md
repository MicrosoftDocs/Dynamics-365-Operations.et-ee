--- 
title: "Märgukirjade töötlemine"
description: "See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 58dc6176f54a33eda47604b65f5580c21a93fcd7
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="process-collection-letters"></a>Märgukirjade töötlemine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist. See ülesanne kasutab demoettevõtte USMF andmeid.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Märgukirjaseeria häälestamine sisestusreeglis
1. Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.
2. Klõpsake nuppu Redigeeri.
    * Valige ripploendist märgukirjaseeria. Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.  
    * Tabeli piirangu vahekaardil saate muuta seda, kuidas sissenõudekirju töödeldakse. Kui väli on seatud olekusse Jah, luuakse märgukirjad selle sisestusreegli jaoks.  
3. Sulgege leht.

## <a name="create-collection-letters"></a>Sissenõude märgukirjade loomine
1. Avage jaotis Krediit ja sissenõuded > Märgukiri > Märgukirjade loomine.
    * Valige kandetüübid, mille jaoks märgukirjad luuakse. Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.  
2. Valige üks suvand väljalt Märgukiri.
3. Sisestage märgukirja kuupäev.
    * Saadaval on kaks sisestusreeglit: Konto – kasutage viivisearve puhul kliendi kontole määratud sisestusreeglit.   Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.  
    * Valige sisestusreegel, kui määrasite suvandi „Kasuta sisestusreegleid” olekusse „Vali”.  
4. Jaotise kaasamiseks laiendage kirjeid.
5. Klõpsake käsku Filtreeri.
6. Sisestage väljale Kriteeriumid kliendi ID. Näiteks sisestage US-001.
7. Klõpsake nuppu OK.
8. Klõpsake nuppu OK.

## <a name="print-collection-letters"></a>Märgukirjade printimine
1. Avage jaotis Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine.
2. Valige väljal Olek suvand Loodud.
3. Valige väljal Prinditud suvand Printimata.
4. Klõpsake Prindi.
5. Klõpsake märgukirja märkust.
6. Jaotise kaasamiseks laiendage kirjeid.
7. Sisestage sisestamiste äralõikekuupäev
8. Märgukirja printimiseks klõpsake OK.

## <a name="post-the-collection-letter"></a>Märgukirja sisestamine
1. Klõpsake valikut Sisesta.
2. Sisestage märgukirja sisestuskuupäev.
3. Jaotise kaasamiseks laiendage kirjeid.
4. Klõpsake nuppu OK.
5. Valige väljal Olek suvand Sisestatud.
6. Valige suvand väljal Prinditud.


