---
title: Rahavoo prognoosimise häälestuse tõrkeotsing
description: Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel. Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985283"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Rahavoo prognoosimise häälestuse tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel. Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Miks kuvatakse rahavoog ainult ühe juriidilise isiku kohta?

Rahavoo prognoosimine konfigureeritakse ja arvutatakse juriidilise isiku kohta. Tulemusi kuvab Power BI aruannete ja rahavoo prognoosimise funktsioon Finance'i ülevaadetes.

Rahavoo prognoosimine tuleb häälestada iga juriidilise isiku kohta, keda puudutavat prognoosi soovite näha. Vaadake üle rahavoo prognoosimise konfiguratsioon kõigis oma juriidilistes isikutes. Teise võimalusena vaadake üle kõigi juriidiliste isikute rahavoo prognoosimist puudutav konfiguratsioon ja veenduge, et see oleks häälestatud nii, nagu soovite.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Miks ei kuva Power BI kõiki rahavoo andmeid?

Enne rahavoo prognooside kuvamist Power BI vaadetes tuleb läbida mitu etappi. Vaadake üle järgmine kontroll-loend ja veenduge, et iga etapp oleks läbitud.

- Häälestage rahavoog iga juriidilise isiku jaoks.
- Määrake pearaamatu parameetrites süsteemivaluuta ja süsteemi vahetuskursi tüüp.
- Määrake pearaamatu arvestusvaluuta ja vahetuskursi tüüp.
- Sisestage kandevaluuta ja arvestusvaluuta vaheline vahetuskurss.
- Sisestage arvestusvaluuta ja süsteemivaluuta vaheline vahetuskurss.
- Sisestage arvestusvaluuta ja iga pangavaluuta vaheline vahetuskurss.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Miks toimis Power BI rahavoog eelmistes versioonides, kuid on nüüd tühi?

Kontrollige, et üksuse kaupluse mõõtmised „Cash flow measure V2“ ja „LedgerCovLiquidityMeasurement“ oleksid konfigureeritud. Lisateavet üksuse kaupluses andmetega töötamise kohta leiate teemast [Power BI integreerimine üksuse kauplusega](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Veenduge, et kõik Power BI sisu kuvamiseks vajalikud etapid oleksid läbitud. Lisateabe saamiseks vt [Sularaha ülevaate Power BI sisu](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Kas üksuse kaupluse üksused on värskendatud?

Andmete ajakohasuse ja täpsuse tagamiseks peate üksusi aeg-ajalt värskendama. Konkreetse üksuse käsitsi värskendamiseks avage jaotis **Süsteemihaldus \> Häälestus \> Üksuse kauplus**, valige üksus ja seejärel tehke valik **Värskenda**. Andmeid saab värskendada ka automaatselt. Määrake lehe **Üksuse kauplus** suvandi **Automaatne värskendamine lubatud** väärtuseks **Jah**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]