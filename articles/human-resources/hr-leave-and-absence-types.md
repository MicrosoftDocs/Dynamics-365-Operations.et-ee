---
title: Puhkuste ja puudumiste tüüpide konfigureerimine
description: Seadistage puhkuse tüübid, mida töötajad saavad rakenduses Dynamics 365 Human Resources valida.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198046"
---
# <a name="configure-leave-and-absence-types"></a>Puhkuste ja puudumiste tüüpide konfigureerimine

Rakenduse Dynamics 365 Human Resources puhkuse tüübid määratlevad puhkuste tüübid, millest töötajal on võimalik teada anda. Saate kohandada puhkuse tüüpe vastavalt teie organisatsiooni vajadustele. Puhkuse tüübid hõlmavad järgmisi.

- Tasustatav puhkus
- Tasustamata puhkus
- Tasustatav puhkus
- Haiguspuhkus
- Meditsiiniline puhkus
- Perekondlik puhkus
- Lühiajaline invaliidsus
- Lähedase kaotuse puhkus

## <a name="add-a-leave-type"></a>Puhkuse tüübi lisamine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste tüübid**.

3. Valige suvand **Uus**.

4. Sisestage puhkuse tüübi nimi suvandis **Tüüp**, valige töövoog suvandist **Töövoo ID** ja sisestage kirjeldus suvandisse **Kirjeldus**.

5. Jaotises **Üldine** valige suvand **Puudub**, **Plaanipärane** või **Plaaniväline** ripploendis **Kategooria**.

6. Valige tulukood ripploendist **Tulukood**.

7. Jaotises **Põhjuse kood nõutav** valige, kas soovite nõuda põhjuse koodi. Kui soovite põhjuse koode nõuda, peate võib-olla need lisama. Jaotises **Põhjuse koodid** valige suvand **Lisa**, valige põhjuse kood ja seejärel valige selle kõrval märkeruut **Lubatud**.

8. Jaotises **Valitud rollide juurdepääsu piiramine** valige, kas soovite juurdepääsu piirata. Seejärel valige turberollid jaotises **Selle puhkuse tüübi turberollid**. Turberollid määratletakse töövoos, mille valisite selles toimingus varem jaotises **Töövoo ID**.

9. Valige käsk **Salvesta**.

## <a name="configure-leave-type-rules"></a>Puhkuse tüübi reeglite konfigureerimine

1. Määrake puhkuse tüübi ümardamise suvandid. Valikud hõlmavad suvandeid **Puudub**, **Üles**, **Alla** ja **Lähim**. Saate määrata ka puhkuse tüübi ümardamise täpsuse.

2. Määrake puhkuse tüübiks **Puhkuse parandused**. Kui valite selle suvandi, kasutab rakendus Human Resources pühade arvu, mis langevate tööpäevadele, et määratleda, kuidas lisada puhkuse tüübile vaba aeg. Näiteks kui jõulupüha langeb esmaspäevale, lahutab rakendus Human Resources lisandumiste töötlemisel puhkuse tüübist ühe päeva.

   Pühad määrate tööajakalendris. Lisateavet vt teemast [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)
   
## <a name="configure-preview-features"></a>Eelvaatefunktsioonide konfigureerimine

Kui olete puhkuste ja puudumiste jaoks lubanud eelvaate funktsioonid, peate konfigureerima ka nende sätted.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Valige edasikantava summa edastamiseks puhkuse tüüp. Saate luua ka uue edasikantava puhkuse tüübi. 

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkuste ja puudumiste plaani loomine](hr-leave-and-absence-plans.md)
- [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)
