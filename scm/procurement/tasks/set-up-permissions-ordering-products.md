--- 
title: "Teise isiku nimel toodete tellimise õiguste seadistamine"
description: "See protseduur näitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8f12f9eb949034f9bef91d93f31a0f3373e39e98
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Teise isiku nimel toodete tellimise õiguste seadistamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada. Teisisõnu saab ostutaotluse "ettevalmistaja" luua nõude teisele "nõude esitajale". See protseduur demonstreerib ka seda, kuidas anda töötajale õigus tellida kaupu ja teenuseid erinevate juriidiliste isikute või tootmisüksuste kaudu. Tavaliselt teeb need toimingud ostujuht. Saate seda protseduuri kasutada demoettevõtte USMF või oma andmeid kasutades.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Õiguse andmine ostutaotluste sisestamiseks teise töötaja nimel
1. Valige Hanked > Seadistus > Poliitikad > Ostutaotluse õigused.
    * Veenduge, et väljal Praegune vaade oleks määratud väärtus Ettevalmistajalt.  Vasakul paanil olevas loendis on näidatud inimesed, kellele saab anda loa koostada teiste inimeste nimel ostutaotlusi.  
2. Valige isik, kellele õigus anda (ettevalmistaja).
3. Klõpsake vahekaarti Lisa.
4. Otsige üles ja valige inimene, kes nõude esitajana lisada.
    * Nõude esitaja on isik, kelle nimel ettevalmistaja saab taotlusi koostada.  
    * Tehke väljal Autoriseerimine valik Konkreetne, kui ettevalmistaja peaks saama valitud töötaja nimel ostutaotlusi koostada. Valige Aruandlus, kui koostaja peaks saama koostada ostutaotlusi ka kõikide nende töötajate nimel, kes sellele töötajale alluvad.  
5. Sisestage kuupäev väljale Jõustunud.
6. Sisestage kuupäev väljale Aegumine.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Ettevalmistajate vaatamine, kellel on õigus koostada valitud töötaja eest ostutaotlusi
1. Tehke väljal Praegune vaade valik Nõude esitajalt.
    * Selles vaates on loend ettevalmistajatest, kellele on antud õigus valitud töötaja nimel ostutaotlusi koostada.  
2. Otsige kiirfiltri abil üles töötaja, kelle just nõude esitajana lisasite.
3. Valige nõude esitaja.
    * Loendis Ettevalmistaja on inimesed, kellel on õigus tellida kaupu vasakul paanil valitud nõude esitaja nimel.   Siin saate lisada veel ettevalmistajaid.   Selles vaates saate anda nõude esitajale ka õiguse koostada taotlusi juriidilistes isikutes ja tootmisüksustes, mis ei ole selle inimese peamised juriidilised isikud või tootmisüksused.  


