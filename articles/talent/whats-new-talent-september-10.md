---
title: "Mis on Dynamics 365 for Talent Core HR-is uut või mida on muudetud (10. september 2018)"
description: "Teema kirjeldab funktsioone, mis on Microsoft Dynamics 365 for Talent Core HR-is kas uued või muudetud."
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.contentlocale: et-ee
ms.lasthandoff: 09/12/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Mis on Dynamics 365 for Talent Core HR-is uut või mida on muudetud (10. september 2018)

[!include [banner](includes/banner.md)]

**Järk 8.1.138.0**

Teema kirjeldab funktsioone, mis on Microsoft Dynamics 365 for Talent Core HR-is kas uued või muudetud.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Puhkeajataotlustele teatud aja päevast lubamine (poolikud päevad)

Kui puhkused ja puudumised on seadistatud nii, et puhkeaeg esitatakse päevades, saate nüüd lubada ka pooliku päeva määratluse. Seejärel, kui kasutajad esitavad puhkeajataotlusi, saavad nad määrata, kas soovivad vabaks saada päeva esimese või teise poole.

Vaikimisi on see suvand välja lülitatud. Selleks et töövõtjad saaksid taotleda päeva esimese või teise poole vabaks, peate selle suvandi sisse lülitama akna Personali parameetrid alas **Puhkused ja puudumised**.

Selle funktsiooni turbeprivileeg on Personaliparameetrite haldamine.

## <a name="validation-of-leave-and-absence-entries"></a>Puhkuste ja puudumiste kannete kinnitamine

Olenevalt sellest, kuidas puhkus on konfigureeritud, saavad töövõtjad, kes esitavad oma tööpäevas pikema puhkeajataotluse, hoiatusteate. Teisisõnu hoiatatakse neid, kui nad püüavad võtta mis tahes kuupäeval vabaks rohkem kui täistööpäeva.

See kinnitamine on alati sisse lülitatud. Alati, kui töövõtja ületab päeva määratletud piirväärtuse, saab ta oma puhkeajataotluses hoiatuse.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Tingimuslike väljavõtete lisaväljad töövoogudes

Core HR-is on mitme töövoo jaoks lisatud tingimuslikele väljavõtetele ja kohatäidetele lisaväljad.

Kompensatsiooni, lõpetamise ja ülekande töövoogudele on lisatud järgmised väljad.

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Ametikoht
- Ühendus
- Osakond
- PositionType
- CompLocation
- Ametinimetus
- Töö
- JobType
- JobFamily
- JobFunction

Ametikoha töövoole on lisatud järgmised väljad.

- Ametikoht
- Ühendus
- Osakond
- PositionType
- CompLocation
- Ametinimetus
- Töö
- JobType
- JobFamily
- JobFunction

Tingimuslike väljavõtete ja kohatäidete väljad on saadaval kõigile kasutajatele, kellel on juurdepääs eelnevalt mainitud töövoo konfigureerimisele.

## <a name="navigation-to-attract-from-personnel-management"></a>Personalihaldusest Attracti navigeerimine

Kui Attract pole personalihalduses seadistatud, suunab jaotis **Palgatavad kandidaadid** kasutajad alustama Attractiga, mitte ei kuva teadet „Me ei leidnud siin kuvamiseks midagi”.

## <a name="other-changes"></a>Muud muudatused

Selles versioonis sisaldub mitu täiendavat veaparandust.

- Kui peatöövõtja on palgatud, pole vahekaart **Kompensatsioon** taotluse/toimingu lehel saadaval.
- Taotluse lõpetamisprotsessi kestel ei saa te enne jätkata, kuni kõik nõutud väljad on täidetud.
- Lahendatud on sortimisjärjestuse ja kuupäeva kuvamise probleemid personalijuhtimise analüüsis.
