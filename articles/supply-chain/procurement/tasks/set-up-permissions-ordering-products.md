---
title: Teise isiku nimel toodete tellimise õiguste seadistamine
description: See teema selgitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada.
author: kamaybac
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0408085d401a34a409bfe46bc6845a9c81a2eea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811890"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Teise isiku nimel toodete tellimise õiguste seadistamine

[!include [banner](../../includes/banner.md)]

See teema selgitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada. Teisisõnu saab ostutaotluse „ettevalmistaja” luua nõude teisele „nõude esitajale”. See protseduur demonstreerib ka seda, kuidas anda töötajale õigus tellida kaupu ja teenuseid erinevate juriidiliste isikute või tootmisüksuste kaudu. Tavaliselt teeb need toimingud ostujuht. Saate seda protseduuri kasutada demoettevõtte USMF või oma andmeid kasutades.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Õiguse andmine ostutaotluste sisestamiseks teise töötaja nimel
1. Avage navigeerimispaneelil **Moodulid > Hange ja allikad > Seadistus > Poliitikad > Ostutaotluse load**. Veenduge, et väljal **Praegune vaade** oleks määratud väärtus **Ettevalmistajalt**. Vasakul paanil olevas loendis on näidatud inimesed, kellele saab anda loa koostada teiste inimeste nimel ostutaotlusi.  
2. Valige isik, kellele õigus anda (ettevalmistaja).
3. Valige **Lisa**.
4. Otsige üles ja valige inimene, kes nõude esitajana lisada.
    - Nõude esitaja on isik, kelle nimel ettevalmistaja saab taotlusi koostada.  
    - Tehke väljal **Autoriseerimine** valik **Konkreetne**, kui ettevalmistaja peaks saama valitud töötaja nimel ostutaotlusi koostada. Valige **Aruandlus**, kui koostaja peaks saama koostada ostutaotlusi ka kõikide nende töötajate nimel, kes sellele töötajale alluvad.  
5. Sisestage kuupäev väljale **Jõustunud**.
6. Sisestage kuupäev väljale **Aegumine**.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Ettevalmistajate vaatamine, kellel on õigus koostada valitud töötaja eest ostutaotlusi
1. Tehke väljal **Praegune vaade** valik **Nõude esitajalt**. Selles vaates on loend ettevalmistajatest, kellele on antud õigus valitud töötaja nimel ostutaotlusi koostada.  
2. Otsige kiirfiltri abil üles töötaja, kelle just nõude esitajana lisasite.
3. Valige nõude esitaja. Loendis Ettevalmistaja on inimesed, kellel on õigus tellida kaupu vasakul paanil valitud nõude esitaja nimel.  Siin saate lisada veel ettevalmistajaid. Selles vaates saate anda nõude esitajale ka õiguse koostada taotlusi juriidilistes isikutes ja tootmisüksustes, mis ei ole selle inimese peamised juriidilised isikud või tootmisüksused.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]