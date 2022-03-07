---
title: Rahavoo prognoosimise häälestuse tõrkeotsing
description: Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel. Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 39860a1960706aae7d223c8d2e810d39edc41b11deb80026925e6655f8e23ee8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747175"
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

Kontrollige, et üksuse kaupluse mõõtmised „Cash flow measure V2“ ja „LedgerCovLiquidityMeasurement“ oleksid konfigureeritud. Lisateavet selle kohta, kuidas töötada andmeüksuse salvega leiate [Power BI integratsioonist Üksuse salvega](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Kontrollige, et kõik sisu vaatamiseks vajalikud Power BI sammud on lõpule viidud. Lisateabe saamiseks vt [Sularaha ülevaate Power BI sisu](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Kas üksuse kaupluse üksused on värskendatud?

Andmete ajakohasuse ja täpsuse tagamiseks peate üksusi aeg-ajalt värskendama. Konkreetse üksuse käsitsi värskendamiseks avage jaotis **Süsteemihaldus \> Häälestus \> Üksuse kauplus**, valige üksus ja seejärel tehke valik **Värskenda**. Andmeid saab värskendada ka automaatselt. Määrake lehe **Üksuse kauplus** suvandi **Automaatne värskendamine lubatud** väärtuseks **Jah**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Millist arvutusmeetodit tuleks kasutada rahavoo prognoosimisel?

Rahavoo prognoosi arvutusmeetodil on kaks olulist valikuvalikut. Valik **Uus** arvutab rahavoo prognoosi uutele dokumentidele ja neile dokumentidele, mis onpeale viimase pakett-töö käitamist muutunud. See valik käivitub kiiremini, sest see töötleb väiksemat dokumentide alamkogumit. Valik **Kokku** arvutab rahavoo prognoosi ümber iga süsteemi dokumendi jaoks. See valik võtab rohkem aega, kuna selle lõpetamiseks on rohkem tööd.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Kuidas parandada rahavoo prognoosi korduva pakett töö jõudlust?

Soovitame uue käivitada oma rahavoo prognoos iga päev üks kord tipptunni väliselt kasutades arvutusmeetodit **Uus** . Soovitame seda lähenemist kasutada kuus päeva nädalas. Seejärel käivitage likviidsuse prognoos iga nädal, kasutades **Kokku** arvutusmeetodit kõige vähema tegevusega päevadel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

