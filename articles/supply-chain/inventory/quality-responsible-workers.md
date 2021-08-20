---
title: Mittevastavuste kinnitamise eest vastutavad töötajad
description: See teema kirjeldab, kuidas konfigureerida mittevastavuste kinnitamise eest vastutavaid töötajaid.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b764baf0983dbca75d52ea9cdd063cebda80a08d39cf3a5c929f15858e2597c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768163"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Mittevastavuste kinnitamise eest vastutavad töötajad

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas konfigureerida mittevastavuste kinnitamise eest vastutavaid töötajaid.

Mittevastavused tuleb heaks kiita, enne kui kasutajad saavad sisestada üksikasju nagu parandused või toimingud. Enne kui kasutajad saavad mittevastavusi kinnitada või tagasi lükata, peab nende kasutaja ID (kasutajakirje) olema lingitud töötaja kirjega. Saate valikuliselt konfigureerida kvaliteedi eest vastutavaid töötajaid ja seejärel lubada ühel töötajal kinnitada töö teise töötaja nimel.

## <a name="enable-a-user-for-nonconformance-processing"></a>Luba kasutajal mittevastavuse töötlemine

Enne kui kasutaja saab mittevastavusi kinnitada või tagasi lükata, peab tema kasutaja ID (kasutajakirje) olema lingitud töötaja kirjega. Kinnitamise väljad saab seejärel automaatselt seadistada ja praeguse kasutaja saab ajatabelisse automaatselt lisada. Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud suvand Dokumenditöötlus.

1. Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.
1. Otsige ja avage kasutaja, kes peaks saama mittevastavusi kinnitada või tagasi lükata.
1. Seadke **Isik** väljale praeguse kasutajakirjega seotud töötaja nimi.
1. Tegevuspaanil valige **Kasutaja suvandid**.
1. Praeguse kasutajakirje **Suvandid** lehel seadke vahekaardil **Eelistused** suvandi **Luba dokumendi käsitlemine** väärtuseks *Jah*.
1. Sulgege lehed.

## <a name="define-workers-that-are-responsible-for-quality"></a>Kvaliteedi eest vastutavate töötajate määratlemine

1. Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kvaliteedi vastutavad töötajad**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljal **Töötaja** valige töötaja, kes sisestab kvaliteediandmed.
4. Väljal **Vastutav töötaja** valige töötaja, kelle nimel valitud töötaja töö sisestab. Kui mittevastavused on loodud ja värskendatud, sisestatakse see töötaja vaikimisi **Töötaja** väljadele.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise ülevaade](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Kvaliteedikulud](quality-charges.md)
- [Mittevastavuste garantiitsoonid](quality-quarantine-zones.md)
- [Mittevastavuste diagnostika tüübid](quality-diagnostic-types.md)
- [Kvaliteeditasud mittevastavustele](quality-charges.md)
- [MIttevastavuste toimingud](quality-operations.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
