---
title: Finantsülevaadete avaleht (eelversioon)
description: Finantsülevaated pakuvad konfigureeritavaid ja laiendatavaid mudeleid, mis aitavad teil täpselt ja nutikalt ennustada oma ettevõtte rahavoogu, ennustada, millal saate laekumata nõuete eest tasu, ja luua eelarveplaani, mis võib kiirendada teie eelarve koostamise protsessi. Kõik need funktsioonid põhinevad nutikatel masinõppemudelitel.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f0d709ef81fd43c009bf36aba2d4be949b1a737c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338225"
---
# <a name="finance-insights-home-page-preview"></a>Finantsülevaadete avaleht (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finantsülevaated pakuvad konfigureeritavaid ja laiendatavaid mudeleid, mis aitavad teil täpselt ja nutikalt ennustada oma ettevõtte rahavoogu, ennustada, millal saate laekumata nõuete eest tasu, ja luua eelarveplaani, mis võib kiirendada teie eelarve koostamise protsessi. Kõik need funktsioonid põhinevad nutikatel masinõppemudelitel. Kui need uued võimalused on kombineeritud hankija maksete ja kogumite automaatikaga, pakuvad need rikkalikku ja nutikat finantssüsteemi, mis juhib otsustusprotsessi ja aitab teil võtta meetmeid, et tõhusalt reageerida praegustele ja oodatavatele ettevõtluse väljakutsetele.

> [!NOTE]
> Finance insights eelversioon on kasutuselevõtu proovimiseks saadaval Ameerika Ühendriikides, Kanadas, Ühendkuningriigis, Euroopas, Aasia ja Vaikse ookeani piirkonnas, Austraalias ja Uus-Meremaal. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge. Finance insights lubamiseks tootmiskeskkondades [Ekspordi rakendusse Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) tuleks esmalt lubada ekspordi võimalused tootmiskeskkonnas.

> [!NOTE]
> Seda funktsiooni pakutakse eelvaate funktsioonide komplektina. Eelvaate funktsioonina ei tohiks te kasutada tulemuseks saadud masinõppe mudeleid, et juhtida või mõjutada oma äriotsuseid või eelarvete ettepanekuid. Selle funktsiooni kasutamist reguleeritakse jaotisega [Lisatingimusted](https://go.microsoft.com/fwlink/?linkid=2105274).

## <a name="prerequisites"></a>Eeltingimused

Selles jaotises loetletakse finantsülevaadete kasutamise nõuded. Kui see on võimalik, esitatakse täiendavate teabeallikate lingid.

### <a name="legal-requirements"></a>Juriidilised nõuded

Eelversiooni programmi rakendamiseks täitke [rakenduse Dynamics 365 Finance finantsülevaadete eelversiooni leping](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Süsteeminõuded

Tier-2 keskkond (mitme kastiga) on nõutav Finance insights eelvaateks. Taustteavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versiooninõuded

See dokument kehtib rakenduse Finance and Operations versioonile 10.0.11 (platvormi värskendus 35) ja hilisematele versioonidele.

### <a name="historical-data-requirements"></a>Ajalooliste andmete nõuded

Kliendi maksmise prognoosimise funktsiooni jaoks kasutatava masinõppemudeli õigesti treenimiseks on nõutav vähemalt ühe aasta jagu kliendiarveid.

### <a name="role-and-permission-requirements"></a>Rolli ja õiguste nõuded

Keskkondades Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps ja Azure tehakse muudatusi. Nende keskkondade puhul on nõutavad õiged load. Allpool on mõned näited muudatustest, mis tehakse.

- Teenuses Microsoft Power Platform luuakse uus keskkond.
- Azure’is luuakse uus talletamise konto, võtme seif ja rakendus.
- Active Directory rentniku administraator peab andma AI Builderi rakendusele loa andmejärvele juurdepääsuks.
- Funktsioon lülitatakse sisse rakenduses Dynamics 365.

Selle protsessi läbimisel on kasu keskkondades Azure, Microsoft Dataverse ja LCS ressursside loomise ja haldamise protsessi tundmisest.

## <a name="configure-finance-insights"></a>Finantsülevaadete konfigureerimine

Enne finantsülevaadete kasutamist peate täitma mõned konfigureerimise etapid. Lisateavet Finance insights`i konfigureerimise kohta leiate teemast:
  - Versioonidele kuni 10.0.19: [Finance insights konfigureerimine (eelvaade) – versioonid kuni 10.0.19](configure-for-fin-insites.md).
  - Versioonidele 10.0.20 ja pärast seda: [Finance insights konfiguratsioon (eelvaade) – versioonid 10.0.20 ja uuemad](configure-for-fin-insites-PubPrvw.md).

## <a name="create-a-data-integrator-project"></a>Andmeintegraatori projekti loomine

Peate looma andmeintegraatori projekti, et masinõppemudeli loodavad andmed saaksid liikuda rakendusse Dynamics 365 Finance. Sellise projekti loomise sammud leiate teemast [Andmeintegraatori projekti loomine](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finantsülevaadete võimaluste lubamine

Kui olete konfigureerimise etapid lõpule viinud ja häälestanud demoandmed, peate lülitama sisse ja häälestama kõik võimalused, mida kavatsete kasutada: kliendimaksete prognoosimine, rahavoo prognoosimine ja eelarvesoovitused.

### <a name="enable-customer-payment-predictions"></a>Kliendimaksete prognoosimise lubamine
Kui kasutate kliendimaksete prognoosimise testimiseks demoandmeid, võib olla vajalik, et oma tehisintellekti mudeli loomise õnnestumiseks peate importima täiendavad demoandmed. 

Kliendimaksete prognooside lubamiseks peate viima lõpule etappide kogumi, et luua teie organisatsiooni andmeid kasutav masinõppemudel, et luua prognoose, millal kliendid tõenäoliselt tasuvad laekumata arved ja millal konkreetsed arved tõenäoliselt tasutakse. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Kliendimakse prognooside lubamine](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine
Rahavoo prognoosimise lubamiseks peate viima lõpule etappide kogumi, et luua teie organisatsiooni andmeid kasutav masinõppemudel, et luua rahavoo prognoose. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Rahavoo prognooside lubamine](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Eelarvesoovituste lubamine

Eelarvesoovituste funktsioon kasutab masinõppemudelit koos teie organisatsiooni ajalooliste andmetega, et luua eelarvesoovitus. Loodud soovitus võib aidata teil alustada eelarve koostamise protsessi, mis on efektiivsem ja tõhusam kui käsitsi protsess. Selle funktsiooni lubamise konkreetseid samme vt teemast [Eelarvesoovituste lubamine](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Finantsülevaate funktsioonide kasutamine

### <a name="using-customer-payment-predictions"></a>Kliendimaksete prognoosimise kasutamine

Nutikas rahavoo prognoosimine on loodud rakenduse Dynamics 365 Finance olemasoleva rahavoo prognoosimise funktsiooni põhjal. Olemasoleva võimaluse läbivaatamiseks vt teemat [Rahavoo prognoosimine](../cash-bank-management/cash-flow-forecasting.md).

- Lisateavet selle kohta, kuidas kliendimakse prognoosid võivad esitada vajalikku teavet, et aktiivselt alustada kogumistegevusi, vt teemast [Kliendimakse prognooside kasutamine](use-customer-payment-predictions.md).
- Teabe saamiseks, mis aitab teil hinnata prognoosimismudeli tõhusust pärast funktsiooni kasutamise alustamist, vt teemast [Algse kliendimakse prognoosimise mudeli hindamine](evaluate-payment-prediction.md).
- Teavet, mis aitab teil korrigeerida prognoosimise loomiseks kasutatavaid andmeid ja seeläbi parandada selle tõhusust, vt teemast [Prognoosimise mudeli parandamine](improve-model.md).

Lisateavet tehisintellekti prognoositavate mudelite tulemuste kohta vt teemast [Masinõppemudelite tulemid](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Rahavoo prognooside kasutamine

Rahavoo prognooside võimekus võib aidata teil hinnata oma sularahajääki täpsemalt. 

- Teavet rahavoo prognooside uute võimaluste kohta vt teemast [Rahavoo prognoos](cash-flow-forecast-intro.md).
- Teavet välisandmete importimise kohta siin rahavoo prognoosimisse kaasamiseks vt teemast [Rahavoo prognoosimises välisandmete kasutamine](external-data-in-cash-flow.md). 
- Teavet selle kohta, kuidas kasutada tehisintellekti mudelit pikaajalise rahavoo lähedal, vt teemast [Rahavoo positsioon](cash-position.md).
- Teavet rahavoo positsioonide ja rahavoo prognooside hetktõmmistena salvestamise ning hetktõmmise tegelike näitajatega võrdlemise kohta vt teemast [Hetktõmmiste ülevaade](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Eelarvesoovituse kasutamine

Teavet eelarve loomise kiirendamise kohta vt teemast [Eelarvesoovitused](budget-proposals.md). 

## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui soovite anda tagasisidet või vajate tuge, saatke meil [kliendimaksete ülevaadetele (eelversioon)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
