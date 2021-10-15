---
title: Tasud mittevastavusega toimingute eest
description: See teema kirjeldab, kuidas luua kvaliteeditasusid, mida saab kasutada mittevastavuse toimingute puhul.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3306f3f9215ab03f408b8026f335dcf496515a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580956"
---
# <a name="charges-for-nonconformance-operations"></a>Tasud mittevastavusega toimingute eest

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua kvaliteeditasusid, mida saab kasutada mittevastavuse toimingute puhul.

Kasutage lehte **Kvaliteedikulud**, et määratleda tasude klassifikatsioon, mida kasutatakse mittevastavustega seotud toimingutes. Tasud võimaldavad teil jälgida üksikasju tasude kohta, mida võlgnete kliendile nõuetele mittevastavate toodete eest või mida hankija võlgneb teile mittevastavate toodete eest. Võite kasutada ka tasusid kulude jälgimiseks, mis on vajalikud välistele hankijatele või teenustele toimingu sooritamiseks.

## <a name="examples-of-quality-charges"></a>Kvaliteeditasude näited

Te töötate tootmisettevõttes. Teie ettevõttel on lepingud mitme hankijaga. Nendes lepingutes esitatakse kaupadele tähtajalise saadetise, kahjude ja toote kvaliteedi normid. Näiteks on mitmel kliendil teie ettevõttega sõlmitud kokkulepped tagastuste, kahjude ja toote kvaliteedi kohta.

Tasustruktuur määratakse igale lepingule ja täpsustatakse lepingus. Saate konfigureerida kvaliteeditasud liigendatult erinevat tüüpi tasude eristamiseks, nagu *Kahjud*, *Hilinenud saadetis* ja *Kvaliteet*. Seejärel mittevastavuse loomisel lisate ühe või mitu toimingu. Iga toimingu puhul valite **Tasud**, et määratleda tasude üksikasjad.

## <a name="create-a-quality-charge"></a>Kvaliteeditasu loomine

1. Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Kvaliteeditasud**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Tasude kood** – sisestage kvaliteeditasu kordumatu ID või nimi.
    - **Kirjeldus** – sisestage kvaliteeditasu detailne kirjeldus.

1. Sulgege leht.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Mittevastavuse toimingule kvaliteeditasu lisamine

Mittevastavustele toimingute lisamise ja nende kulude lisamise üksikasju vt [Mittevastavuse toimingud](quality-operations.md).

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise ülevaade](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Mittevastavuste kinnitamise eest vastutavad töötajad](quality-responsible-workers.md)
- [Mittevastavuste garantiitsoonid](quality-quarantine-zones.md)
- [Mittevastavuste diagnostika tüübid](quality-diagnostic-types.md)
- [Kvaliteeditasud mittevastavustele](quality-charges.md)
- [MIttevastavuste toimingud](quality-operations.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
