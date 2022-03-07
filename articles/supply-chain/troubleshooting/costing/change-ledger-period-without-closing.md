---
title: Pearaamatu perioodi oleku muutmisel lao sulgemiseta kuvatakse hoiatused või tõrked
description: Pearaamatu perioodi oleku muutmisel lao sulgemiseta kuvatakse hoiatused või tõrked
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476106"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Pearaamatu perioodi oleku muutmisel lao sulgemiseta kuvatakse hoiatused või tõrked

Microsoft kehtestas järgmised kinnitused, et vältida probleeme, mis on põhjustatud vale perioodi lõpu protsessist omahinna arvutamisel. Kui ilmneb mõni järgmistest tõrketeadetest, vaadake [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3), et saada lisateavet nende probleemide lahendamise kohta.

- Olete käivitamas ümberarvutust kuupäevaga %1 (10.02.2019). Viimane registreeritud ümberarvutus teostati eelmises perioodis kuupäevaga %2 (20-01-2019). Kuupäevaga %3 (31-01-2019) sobiva perioodi lõpuga varude sulgemist ei ole registreeritud. Ärge unustage käitada lao sulgemist %3 (31-01-2019), mis ühtib perioodi lõpuga. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on täidetud.

- Olete muutmas pearaamatu perioodi väärtuselt %1 väärtusele %2. Kuupäevaga %3 sobiva perioodi lõpuga varude sulgemist ei ole registreeritud. Käivitage enne oleku muutmist lao sulgemine kuupäevaga %3, mis ühtib perioodi lõpuga. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on täidetud. Juriidilisest isikust teavitatud %4. Praegu on see informatiivne, kuid tulevikus peate seda tegevust tegema.

- Konto struktuuri %1 on muudetud. Ühte või mitut põhikontot %2 pole enam olemas. Need põhikontod on nõutud kuupäevaks %3 kuupäevaga %4. Palun lisage need põhikontod konto struktuuri %1, enne kui saate %3 tööd jätkata. Praegu on see informatiivne, kuid tulevikus peate seda tegevust tegema.

- Olete käivitamas lao sulgemist kuupäevaga %1 (31-01-2019). Perioodi lõpukuupäevaga %2 (31-01-2019) sobivat omahinna tagasiarvestust ei ole registreeritud. Palun teostage perioodi lõpukuupäevaga %3 (31-01-2019) sobiv omahinna tagasiarvestus. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on täidetud.

- Olete käivitamas omahinna ümberarvutust kuupäevaga %1 (28-02-2019). Viimane registreeritud omahinna ümberarvutus teostati eelmises perioodis kuupäevaga %2 (31-01-2019). Perioodi lõpukuupäevaga %3 (31-01-2019) sobivat varude sulgemist ei ole registreeritud.

Ärge unustage käitada perioodi lõpukuupäevaga %3 (31-01-2019) ühtivat lao sulgemist. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni varude sulgemine on teostatud.