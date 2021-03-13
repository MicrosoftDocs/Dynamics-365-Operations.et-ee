---
title: Puhkuste ja puudumiste tüüpide konfigureerimine
description: Seadistage puhkuse tüübid, mida töötajad saavad rakenduses Dynamics 365 Human Resources valida.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b21d4d631bcdf603b38212f5f76bb78937d3d3c
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115072"
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

9. Valige jaotises **Kalendri värv**, millist värvi selle puhkusetüübi puhul puhkuste ja puudumiste kalendrites kuvada. 

10. Valige jaotises **Peatamise suhted**, kas soovite, et see puhkusetüüp peataks mõne teise puhkusetüübi või et selle puhkusetüübi peataks mõni teine puhkusetüüp. Kui puhkusetaotlus esitatakse peatava puhkusetüübi kohta, siis luuakse peatatud puhkusetüübi kohta automaatselt puhkuse peatamise kanne. 

10. Valige käsk **Salvesta**.

## <a name="configure-leave-type-rules"></a>Puhkuse tüübi reeglite konfigureerimine

1. Määrake puhkuse tüübi ümardamise suvandid. Valikud hõlmavad suvandeid **Puudub**, **Üles**, **Alla** ja **Lähim**. Saate määrata ka puhkuse tüübi ümardamise täpsuse.

2. Määrake puhkuse tüübiks **Puhkuse parandused**. Kui valite selle suvandi, kasutab rakendus Human Resources pühade arvu, mis langevate tööpäevadele, et määratleda, kuidas lisada puhkuse tüübile vaba aeg. Näiteks kui jõulupüha langeb esmaspäevale, lahutab rakendus Human Resources lisandumiste töötlemisel puhkuse tüübist ühe päeva.

   Pühad määrate tööajakalendris. Lisateavet vt teemast [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)
   
 3. Seadistage puhkusetüübi kohta **Ülekantav puhkusetüüp**. Selle valiku korral kantakse ülekantavad saldod üle konkreetsele puhkusetüübile. Samuti tuleb ülekantava puhkuse tüüp lisada puhkuse ja puudumiste plaanile. 
 
 4. Määratlege puhkusetüübi kohta **Aegumisreeglid**. Selle valiku konfigureerimisel saate valida päevade või kuude üksuse ja määrata aegumise kestuse. Samuti saate seadistada aegumisreegli kehtivuse alguskuupäeva. Kõik aegumiskuupäeval eksisteerivad puhkusesaldod arvatakse puhkusetüübist maha ning need kajastuvad puhkusesaldos. 
 
 
## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkuste ja puudumiste plaani loomine](hr-leave-and-absence-plans.md)
- [Looge töögraafik](hr-leave-and-absence-working-time-calendar.md)
- [Puhkuse katkestamine](hr-leave-and-absence-suspend-leave.md)

