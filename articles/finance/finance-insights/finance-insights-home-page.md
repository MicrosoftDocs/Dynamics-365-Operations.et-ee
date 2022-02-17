---
title: Finance Insightsi avaleht
description: Finantsülevaated pakuvad konfigureeritavaid ja laiendatavaid mudeleid, mis aitavad teil täpselt ja nutikalt ennustada oma ettevõtte rahavoogu, ennustada, millal saate laekumata nõuete eest tasu, ja luua eelarveplaani, mis võib kiirendada teie eelarve koostamise protsessi. Kõik need funktsioonid põhinevad nutikatel masinõppemudelitel.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05b0de8b0104238a33f006234d4a0e8ba9fcdb2a
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087289"
---
# <a name="finance-insights-home-page"></a>Finance Insightsi avaleht

[!include [banner](../includes/banner.md)]

Finance Insights pakub konfigureeritavaid ja laiendatavaid lahendusi, mis aitavad teil nutikalt prognoosida oma ettevõtte rahavoogu, ennustada, millal võite tasuda tasu tasumata nõuete eest, ja luua eelarve ettepanek, mis aitab kiirendada teie eelarve koostamise protsessi. Need funktsioonid kasutavad teie esitatud andmete abil mudelite loomiseks intelligentseid masinõppemalle (sh kolmanda osapoole andmed, näiteks büroo tarbijaaruande teave). Need intelligentsed võimalused teavitavad otsuste tegemist ja aitavad teil võtta meetmeid, et reageerida tõhusalt praegustele ja eeldatavatele äriprobleemidele. Vastutate kõigi andmete eest, mida kasutatakse finance insightsiga või väljastatakse sellest.

> [!NOTE]
> Finantsülevaated on saadaval juurutamiseks Ameerika Ühendriikides, Kanadas, Ühendkuningriigis, Euroopas, Aasia vaikse ookeani piirkonnas, Jaapanis, Austraalias ja Uus-Meremaal. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.

## <a name="prerequisites"></a>Eeltingimused

Selles jaotises loetletakse finantsülevaadete kasutamise nõuded. Kui see on võimalik, esitatakse täiendavate teabeallikate lingid.

### <a name="system-requirements"></a>Süsteeminõuded

Tier-2 keskkond (mitme kastiga) on nõutav Finance insights eelvaateks. Taustteavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versiooninõuded

See teema kehtib Microsofti Dynamics 365 Finance versiooni 10.0.21 ja uuema versiooni kohta.

### <a name="license-requirements"></a>Litsentsinõuded

Finance Insights kasutab AI Builder krediiti, et luua finantsprognoose. Kõik selleks vajalikud litsentsid sisalduvad rentniku litsentsis. Igale Dynamics 365 Finance üürnikule antakse iga kuu 20 000 AI Builder krediiti. Kui ärivajaduste jaoks on vaja täiendavaid krediiti, saab neid osta otse AI Builder.

### <a name="historical-data-requirements"></a>Ajalooliste andmete nõuded

Kliendi maksmise prognoosimise funktsiooni jaoks kasutatava masinõppemudeli õigesti treenimiseks on nõutav vähemalt ühe aasta jagu kliendiarveid. Rahavoogude prognooside jaoks on soovitatav kasutada kolme aasta ajaloolisi andmeid. Arukate eelarveettepanekute puhul soovitatakse kolmeaastast ajaloolist eelarvet ja/või tegelikke eelarveid.

## <a name="configure-finance-insights"></a>Finance Insightsi konfigureerimine

Enne finance'i ülevaate kasutamist peate täitma konfiguratsioonitoimingud. Lisateavet finantsülevaadete konfigureerimise kohta vt jaotisest [Finantsülevaadete konfigureerimine](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Andmeintegraatori projekti loomine

Peate looma andmeintegraatori projekti, et masinõppemudeli loodavad andmed saaksid liikuda rakendusse Dynamics 365 Finance. Sellise projekti loomise sammud leiate teemast [Andmeintegraatori projekti loomine](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finantsülevaadete võimaluste lubamine

Kui olete konfigureerimise etapid lõpule viinud ja häälestanud demoandmed, peate lülitama sisse ja häälestama kõik võimalused, mida kavatsete kasutada: kliendimaksete prognoosimine, rahavoo prognoosimine ja eelarvesoovitused.

### <a name="enable-customer-payment-predictions"></a>Kliendimaksete prognoosimise lubamine
Kui kasutate kliendimaksete prognoosimise testimiseks demoandmeid, võib olla vajalik, et oma tehisintellekti mudeli loomise õnnestumiseks peate importima täiendavad demoandmed. 

Kliendimaksete prognooside lubamiseks peate täitma sammude kogumi, et luua masinõppemudel, mis kasutab teie organisatsiooni andmeid, et luua prognoose selle kohta, millal kliendid tõenäoliselt tasumata arveid maksavad ja millal konkreetsed arved tõenäoliselt tasutakse. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Kliendimakse prognooside lubamine](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine
Rahavoo prognoosimise lubamiseks peate viima lõpule etappide kogumi, et luua teie organisatsiooni andmeid kasutav masinõppemudel, et luua rahavoo prognoose. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Rahavoo prognooside lubamine](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Eelarvesoovituste lubamine

Eelarvesoovituste funktsioon kasutab masinõppemudelit koos teie organisatsiooni ajalooliste andmetega, et luua eelarvesoovitus. Loodud soovitus võib aidata teil alustada eelarve koostamise protsessi, mis on efektiivsem ja tõhusam kui käsitsi protsess. Selle funktsiooni lubamiseks toodud konkreetsete toimingute kohta leiate teemast [Eelarveettepanekute lubamine](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Finantsülevaate funktsioonide kasutamine

### <a name="using-customer-payment-predictions"></a>Kliendimaksete prognoosimise kasutamine

- Teavet selle kohta, kuidas kliendi makseprognoosid saavad anda teavet, mis on vajalik kogumistegevuste ennetavaks alustamiseks, leiate teemast [Kliendi makseprognooside kasutamine](use-customer-payment-predictions.md).
- Teabe saamiseks, mis aitab teil hinnata prognoosimismudeli tõhusust pärast funktsiooni kasutamise alustamist, vt teemast [Algse kliendimakse prognoosimise mudeli hindamine](evaluate-payment-prediction.md).
- Teavet, mis aitab teil korrigeerida prognoosimise loomiseks kasutatavaid andmeid ja seeläbi parandada selle tõhusust, vt teemast [Prognoosimise mudeli parandamine](improve-model.md).
- Lisateavet tehisintellekti prognoositavate mudelite tulemuste kohta vt teemast [Masinõppemudelite tulemid](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Rahavoo prognooside kasutamine

Rahavoo prognooside võimekus võib aidata teil hinnata oma sularahajääki täpsemalt. Intelligentne rahavoogude prognoosimine põhineb olemasoleval rahavoogude prognoosimise funktsioonil Dynamics 365 Finance. Olemasoleva võimaluse läbivaatamiseks vt teemat [Rahavoo prognoosimine](../cash-bank-management/cash-flow-forecasting.md).

- Rahavoogude prognooside uute võimaluste kohta leiate teavet teemast [Rahavoogude prognoos](cash-flow-forecast-intro.md).
- Teavet välisandmete importimise kohta siin rahavoo prognoosimisse kaasamiseks vt teemast [Rahavoo prognoosimises välisandmete kasutamine](external-data-in-cash-flow.md). 
- Teavet selle kohta, kuidas kasutada tehisintellekti mudelit pikaajalise rahavoo lähedal, vt teemast [Rahavoo positsioon](cash-position.md).
- Teavet rahavoo positsioonide ja rahavoo prognooside hetktõmmistena salvestamise ning hetktõmmise tegelike näitajatega võrdlemise kohta vt teemast [Hetktõmmiste ülevaade](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Eelarvesoovituse kasutamine

Teavet eelarve loomise kiirendamise kohta vt teemast [Eelarvesoovitused](budget-proposals.md). 

## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui olete huvitatud tagasiside andmist või vajate tuge, saatke meilisõnum finance'i [statistikale](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
