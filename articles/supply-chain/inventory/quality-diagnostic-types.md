---
title: Mittevastavuste diagnostika tüübid
description: See teema kirjeldab, kuidas kasutada ja luua diagnostika tüüpe, mida mittevastavuste puhul kasutada saab.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 560627bf5ecd38f3fc79448629390acb549e40fb1388958d9eac094517925039
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781509"
---
# <a name="diagnostic-types-for-nonconformances"></a>Mittevastavuste diagnostika tüübid

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas kasutada ja luua diagnostika tüüpe, mida mittevastavuste puhul kasutada saab.

Kasutage lehte **Diagnostika tüübid** diagnostikatoimingute klassifikatsiooni määratlemiseks. Seejärel, kui loote mittevastavuse paranduse, valite diagnostika. Parandus määratleb, mis tüüpi diagnostilist tegevust tuleks kinnitatud mittevastavuse korral kasutada ja kes peaks seda tegema. Samuti määratleb see nõutava lõpetamise kuupäeva ja plaanitud lõpetamise kuupäeva.

## <a name="examples-of-diagnostic-types"></a>Diagnostikatüüpide näited

Te töötate tootmisettevõttes ja mitmel kaubal on kvaliteeditestid nurjunud. Need kaubad teisaldatakse vahelattu ja märgitakse mittevastavateks toodeteks. Luuakse mittevastavuse kirje Microsoft Dynamics 365 Supply Chain Management, et jälgida üksikasju probleemi lahendamise kaudu.

Sel juhul tekivad kvaliteediprobleemid, kuna esemeid pakkiva masina laagrid on kulunud ja kuumenevad üle. Selle probleemi parandus on asendada masina osad.

Kui konfigureerite diagnostika tüüpe, saate luua mitmeid kirjeid, millest igaüks esindab erinevat tüüpi probleeme, mis masinal võivad olla. Võite luua ka ühe üldise diagnostika tüübi, mis esindab masina parandamist.

## <a name="create-a-diagnostic-type"></a>Looge diagnostika tüüp

1. Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Diagnostika tüübid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Diagnostika** – Sisestage meediumitüübi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage diagnostika tüübi detailne kirjeldus.

1. Sulgege leht.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise ülevaade](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Mittevastavuste kinnitamise eest vastutavad töötajad](quality-responsible-workers.md)
- [Mittevastavuste garantiitsoonid](quality-quarantine-zones.md)
- [Mittevastavuste probleemitüübid](quality-problem-types.md)
- [Kvaliteeditasud mittevastavustele](quality-charges.md)
- [MIttevastavuste toimingud](quality-operations.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
