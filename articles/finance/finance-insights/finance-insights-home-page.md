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
ms.openlocfilehash: 2f04ef1a0de815596f629fede25a247c58e026f4
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643873"
---
# <a name="finance-insights-home-page"></a>Finance Insightsi avaleht

[!include [banner](../includes/banner.md)]

Finantside vihjed annavad konfigureeritavaid ja laiendatavaid lahendusi, mis aitavad nutikalt prognoosida ettevõtte rahavoog, prognoosida, millal võite saada tasu laekumata müügireskontro eest, ja luua eelarvesoovitusi, mis aitavad eelarvete protsessi kiirendada. Need funktsioonid kasutavad nutikaid masina õppemalle, et koostada mudeleid, kasutades teie poolt pakutavaid andmeid (sh kolmanda osapoole andmed, nt büroo tarbearuande teave). Need nutikad võimalused aitavad otsustusprotsessi teavitada ja aitab teil reageerida efektiivselt praegustele ja eeldatavatele äritegevusega seotud küsimustele. Vastutate finantside vihjetega kasutatavate või väljastamisandmete eest.

> [!NOTE]
> Finantsülevaated on saadaval juurutamiseks Ameerika Ühendriikides, Kanadas, Suurbritannias, Euroopas, Aasia-vaikses, Jaapanis, Austraalias ja Uus-Meremaal. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.

## <a name="prerequisites"></a>Eeltingimused

Selles jaotises loetletakse finantsülevaadete kasutamise nõuded. Kui see on võimalik, esitatakse täiendavate teabeallikate lingid.

### <a name="system-requirements"></a>Süsteeminõuded

Tier-2 keskkond (mitme kastiga) on nõutav Finance insights eelvaateks. Taustteavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versiooninõuded

See artikkel kehtib versioonile Microsoft Dynamics 365 Finantsversioon 10.0.21 ja uuemale versioonile.

### <a name="license-requirements"></a>Litsentsinõuded

Finantsülevaated kasutavad AI Builder krediiti finantsprognooside loomiseks. Kõik selle jaoks vajalikud litsentsid kaasatakse rentnikulitsentsile. Igale Dynamics 365 finants rentnikule antakse igal kuul 20 000 AI Builder ainepunktide kogust. Kui ärivajaduste korral on vaja lisakrediiti, saab neid osta otse asukohast AI Builder.

### <a name="historical-data-requirements"></a>Ajalooliste andmete nõuded

Kliendi maksmise prognoosimise funktsiooni jaoks kasutatava masinõppemudeli õigesti treenimiseks on nõutav vähemalt ühe aasta jagu kliendiarveid. Likviidsuse prognoosimiseks on soovitatav kasutada kolme aasta jooksul andmeid. Nutikate eelarveettepanekute jaoks on soovitatav kasutada kolme aasta jooksul ajaloolist eelarvet ja/või tegelikke eelarveid.

## <a name="configure-finance-insights"></a>Finance Insightsi konfigureerimine

Enne finantsülevaate kasutamist peate lõpule viima konfiguratsiooni etapid. Lisateavet finantsülevaadete konfigureerimise kohta vt jaotisest [Finantsülevaadete konfigureerimine](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Andmeintegraatori projekti loomine

Teil on vaja luua andmeintegraatorprojekt, et masina õppemudeli loodud andmed saaksid integreeruda rakendusse Dynamics 365 Finance. Sellise projekti loomise sammud leiate teemast [Andmeintegraatori projekti loomine](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finantsülevaadete võimaluste lubamine

Kui olete konfigureerimise etapid lõpule viinud ja häälestanud demoandmed, peate lülitama sisse ja häälestama kõik võimalused, mida kavatsete kasutada: kliendimaksete prognoosimine, rahavoo prognoosimine ja eelarvesoovitused.

### <a name="enable-customer-payment-predictions"></a>Kliendimaksete prognoosimise lubamine
Kui kasutate kliendimaksete prognoosimise testimiseks demoandmeid, võib olla vajalik, et oma tehisintellekti mudeli loomise õnnestumiseks peate importima täiendavad demoandmed. 

Kliendi makseprognooside lubamiseks peate lõpule määrama sammud masina õppemudeli loomiseks, mis kasutab teie organisatsiooni andmeid prognooside loomiseks selle kohta, millal kliendid tasuvad tõenäoliselt laekumata arveid ja kui makstakse tõenäoliselt konkreetseid arveid. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Kliendimakse prognooside lubamine](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine
Rahavoo prognoosimise lubamiseks peate viima lõpule etappide kogumi, et luua teie organisatsiooni andmeid kasutav masinõppemudel, et luua rahavoo prognoose. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Rahavoo prognooside lubamine](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Eelarvesoovituste lubamine

Eelarvesoovituste funktsioon kasutab masinõppemudelit koos teie organisatsiooni ajalooliste andmetega, et luua eelarvesoovitus. Loodud soovitus võib aidata teil alustada eelarve koostamise protsessi, mis on efektiivsem ja tõhusam kui käsitsi protsess. Funktsiooni lubamise konkreetsete sammude kohta vt Luba [eelarveettepanekud](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Finantsülevaate funktsioonide kasutamine

### <a name="using-customer-payment-predictions"></a>Kliendimaksete prognoosimise kasutamine

- Teavet selle kohta, kuidas kliendi makseennustused saavad esitada teavet, mis on vajalik sissenõude ennetavaks alustamiseks, leiate jaotisest [Kasuta kliendi makseprognoose](use-customer-payment-predictions.md).
- Teabe saamiseks, mis aitab teil hinnata prognoosimismudeli tõhusust pärast funktsiooni kasutamise alustamist, vt teemast [Algse kliendimakse prognoosimise mudeli hindamine](evaluate-payment-prediction.md).
- Teavet, mis aitab teil korrigeerida prognoosimise loomiseks kasutatavaid andmeid ja seeläbi parandada selle tõhusust, vt teemast [Prognoosimise mudeli parandamine](improve-model.md).
- Lisateavet tehisintellekti prognoositavate mudelite tulemuste kohta vt teemast [Masinõppemudelite tulemid](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Rahavoo prognooside kasutamine

Rahavoo prognooside võimekus võib aidata teil hinnata oma sularahajääki täpsemalt. Nutikas likviidsuse prognoosimine on üles ehitatud Dynamics 365 Finance’i olemasolevatele likviidsuse prognoosimise funktsioonidele. Olemasoleva võimaluse läbivaatamiseks vt teemat [Rahavoo prognoosimine](../cash-bank-management/cash-flow-forecasting.md).

- Likviidsuse prognoosi uute võimaluste kohta leiate lisateavet likviidsuse [prognoosist](cash-flow-forecast-intro.md).
- Teavet välisandmete importimise kohta siin rahavoo prognoosimisse kaasamiseks vt teemast [Rahavoo prognoosimises välisandmete kasutamine](external-data-in-cash-flow.md). 
- Teavet selle kohta, kuidas kasutada tehisintellekti mudelit pikaajalise rahavoo lähedal, vt teemast [Rahavoo positsioon](cash-position.md).
- Teavet rahavoo positsioonide ja rahavoo prognooside hetktõmmistena salvestamise ning hetktõmmise tegelike näitajatega võrdlemise kohta vt teemast [Hetktõmmiste ülevaade](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Eelarvesoovituse kasutamine

Teavet eelarve loomise kiirendamise kohta vt teemast [Eelarvesoovitused](budget-proposals.md). 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
