---
title: MIttevastavuste toimingud
description: See teema kirjeldab, kuidas luua ja kasutada mittevastavuste toiminguid.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022200"
---
# <a name="operations-for-nonconformances"></a>MIttevastavuste toimingud

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua ja kasutada mittevastavuste toiminguid.

Kasutage lehte **Toimingud** klassifikatsiooni määratlemiseks tööle, mida saab teha kinnitatud mittevastavuse puhul. Kui määrate mittevastavusele seotud toimingu, saate pakkuda üksikasjalikku teavet, nagu teavet toimingu tegemiseks nõutava seotud materjali, töötundide ja toimingute lisakulude kohta. Seda teavet kasutatakse toimingu eeldatava maksumuse arvutamiseks. Üksikasjalikku teavet ja eeldatavat omahinda kasutatakse viitena. Kvaliteediga seotud toimingud erinevad toimingutest, mida saab määrata tootmisprotsessile.

> [!NOTE]
> Ehkki saate jälgida mittevastavusega seotud operatsioonides kasutatavaid kulusid, aega ja kaupu, on teie sisestatavad andmed ainult formaalsed. See ei ole automaatselt integreeritud pearaamatu, varude alammooduli ega **Kellaaeg ja kohalviibimine** mooduliga.

## <a name="examples-of-operations"></a>Toimingute näited

Te töötate tootmisettevõttes. Mittevastavus loodi ja kiideti heaks kaupadele, mille kvaliteeditest ebaõnnestus. Loodi parandus, mis näitas, et probleem oli seotud masina laagri veaga. Selle laagri asendamiseks on vaja mitut etappi ja vastutust iga toimingu eest jälgitakse. Näiteks võivad olla nõutavad järgmised sammud:

1. Tootmisliin on peatatud ja teostatakse puhastamist.
1. Hoolduspersonal asendab laagri.
1. Kvaliteedi tagamise personal kontrollib masinat enne selle tagasi sisselülitamist.

Selle näite korral saab luua järgmisi toiminguid, mis tähistavad tööd, mida tuleb teha:

- Peatage tootmisliin.
- Tootmisliini puhastamine.
- Masina hoolduse tegemine.
- Kontrollige masinat.

## <a name="create-an-operation"></a>Toimingu loomine

1. Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Toimingud**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Toiming** – sisestage toimingu kordumatu kood või nimi.
    - **Kirjeldus** – Sisestage toimingu detailne kirjeldus.
    - **Tüüp** – Kui toimingut saab kasutada ainult mittevastavustega, mis on seotud kindlat tüüpi tellimusega, valige tellimuse tüüp (*Ostutellimus* või *Müügitellimus*).

1. Sulgege leht.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise ülevaade](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Mittevastavuste loomine ja töötlemine](tasks/create-process-non-conformance.md)
- [Mittevastavuste kinnitamise eest vastutavad töötajad](quality-responsible-workers.md)
- [Mittevastavuste garantiitsoonid](quality-quarantine-zones.md)
- [Mittevastavuste diagnostika tüübid](quality-diagnostic-types.md)
- [Kvaliteeditasud mittevastavustele](quality-charges.md)
- [Mittevastavuste probleemitüübid](quality-operations.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
