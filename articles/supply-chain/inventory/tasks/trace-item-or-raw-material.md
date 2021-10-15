---
title: Kauba või toormaterjali jälgimine
description: See protseduur näitab, kuidas kasutada kauba jälgimist tuvastamiseks, kus kaupu või toormaterjale on kasutatud või kasutatakse.
author: yufeihuang
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c01cabf32542798f70720ab0db7d055fc54cf345
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575820"
---
# <a name="trace-an-item-or-raw-material"></a>Kauba või toormaterjali jälgimine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas kasutada kauba jälgimist tuvastamiseks, kus kaupu või toormaterjale on kasutatud või kasutatakse. Selle protseduuri abil saate kauba tuvastada, liikuda tagasi selle allika juurde ja seejärel edasi läbi tootmise ja valmis toote müügi. Seda protsessi saab kasutada sellest mõjutatud klientide, müügitellimuste ja muu uurimiseks. Protseduur kasutab demoettevõtte USP2 andmeid.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Kauba jälgimine tagasisuunas, kasutades teadaolevat partiinumbrit
1. Avage **Navigeerimispaneelil** **Moodulid > Varuhaldus > Päringud ja aruanded > Jälgimisdimensioonid > Kauba jälgimine**.
2. Tehke väljal **Kaubanumber** valik P9100.
3. Klõpsake loendis valitud real olevat linki.
4. Tehke väljal **Edasi või tagasi** valik Tagasi.
5. Tehke väljal **Partiinumber** valik 12-344-01.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake valikut **OK**.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Kauba tuvastamine, selle jälgimine edasisuunas ja analüüsimine

Puu ülemine sõlm kajastab valitud kauba ja partii laos olevat kogust. Peate laiendama puu sõlmesid, et leida kaup, mille puhul tuleb edastamise jälgimine käivitada.   
1. Laiendage puus allpool kirjeldatud sõlmesid ja valige sejärel viimane sõlm.
    
    Laiendage valikuid: P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101 ja valige seejärel see sõlm.     
2. Laiendage puus allpool kirjeldatud sõlme ja seejärel valige see sõlm.
    
    Alustades äsja valitud sõlmest, laiendage valikuid M9103 ● Production line B-000050 ● 09.12.2015  ● -160,00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01 ja valige seejärel see sõlm.  
3. Klõpsake valikut **Jälgi sõlmest**.
4. Klõpsake nuppu **Edasi**.
5. Klõpsake **Tegumiribal** valikut **Jälgimine**.
    
    On mitu jälgimise suvandit, mis annavad teavet jälgitava kauba mõjutatud klientide kohta ning saadetud ja saatmata kaubaga seotud müügitellimuste kohta.   
6. Klõpsake **Kliendid**.
7. Sulgege leht.
8. Klõpsake **Tegumiribal** valikut **Jälgimine**.
9. Klõpsake nuppu **Saadetud müügitellimused**.
10. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]