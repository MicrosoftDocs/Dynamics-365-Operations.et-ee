---
title: Mittevastavuste probleemitüübid
description: See teema kirjeldab, kuidas luua ja kasutada mittevastavuste probleemitüüpe.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26705dd12f478f4ca6046c7265d4ae3cb1d08c69
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568803"
---
# <a name="problem-types-for-nonconformances"></a>Mittevastavuste probleemitüübid

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua ja kasutada mittevastavuste probleemitüüpe.

Kasutage lehte **Probleemi tüübid**, et määratleda erinevate mittevastavustüüpide jaoks tekkida võivate kvaliteediprobleemide klassifikatsioon. Iga loodud probleemitüübi jaoks peate määrama mittevastavuste tüübid, millega probleemitüüpi saab kasutada. Saate seadistada järgmisi mittevastavuste tüüpe:

- **Sisemine** – Seda tüüpi mittevastavused on seotud vaba kaubavaruga (nt kvaliteettellimused või garantiitellimused).
- **Klient** – Seda tüüpi mittevastavused on seotud müügitellimustega.
- **Hankija** – Seda tüüpi mittevastavused on seotud ostutellimustega.
- **Teenuse taotlus** – Seda tüüpi mittevastavused on seotud teenusetellimustega.
- **Tootmine** – Seda tüüpi mittevastavused on seotud partiitellimuste või tootmistellimustega.
- **Kaastoote tootmine** – Seda tüüpi mittevastavused on seotud kaastoodete partiitellimustega.

Uue probleemitüübi loomisel valige tegevuspaanil **Mittevastavuse tüübid**, et luua loend ühest või enamast mittevastavuse tüübist, mis on probleemi tüübi jaoks autoriseeritud. Näiteks võib defektikoodiga seotud probleemitüüp kehtida kõigile mittevastavuse tüüpidele. Siiski võib kliendikaebustega seotud probleemitüüpi rakenduda ainult **Klient** ja **Teenuse taotlus** mittevastavuse tüüpidele.

## <a name="examples-of-problem-types"></a>Probleemitüüpide näited

Siin on mõned näited probleemi tüüpide stsenaariumidest, mida saab kasutada erinevate mittevastavuse tüüpidega:

- **Klient:** Klient esitas kaebuse, klient tegi tagastuse või ei täidetud kvaliteedispetsifikatsioone.
- **Hankija:** Toode on kahjustatud, kvaliteedispetsifikatsioone ei täidetud või saadi vale toode.
- **Teenuse taotlus:** Kvaliteedispetsifikatsioone ei täidetud, klient esitas kaebuse või nõutakse masina hooldust.
- **Tootmine:** Ei täidetud kvaliteedispetsifikatsioone, nõutakse masina hooldust või toode sai kahjustada.
- **Kaastoote tootmine:** Ei täidetud kvaliteedispetsifikatsioone, nõutakse masina hooldust või toode sai kahjustada.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Probleemi tüübi loomine ja selle mittevastavuse tüüpidele määramine

1. Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Probleemi tüübid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Probleemi tüüp** – Sisestage probleemitüübi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage probleemi tüübi detailne kirjeldus.

1. Kui uus rida on endiselt valitud, valige tegevuspaanil **mittevastavuse tüübid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel seadistage uue rea jaoks **Mittevastavuse tüüp** väli mittevastavuse tüübi jaoks, mida soovite probleemi tüübi jaoks lubada.
1. Korrake eelmist sammu iga täiendava mittevastavuse tüübi korral, mida soovite probleemi tüübile autoriseerida.
1. Sulgege lehed.

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
