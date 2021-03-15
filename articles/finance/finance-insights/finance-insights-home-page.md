---
title: Finantsülevaadete avaleht (eelversioon)
description: Finantsülevaated pakuvad konfigureeritavaid ja laiendatavaid mudeleid, mis aitavad teil täpselt ja nutikalt ennustada oma ettevõtte rahavoogu, ennustada, millal saate laekumata nõuete eest tasu, ja luua eelarveplaani, mis võib kiirendada teie eelarve koostamise protsessi. Kõik need funktsioonid põhinevad nutikatel masinõppemudelitel.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9920d24ea92196331ea318cab2f67501801937bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995086"
---
# <a name="finance-insights-home-page-preview"></a>Finantsülevaadete avaleht (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finantsülevaated pakuvad konfigureeritavaid ja laiendatavaid mudeleid, mis aitavad teil täpselt ja nutikalt ennustada oma ettevõtte rahavoogu, ennustada, millal saate laekumata nõuete eest tasu, ja luua eelarveplaani, mis võib kiirendada teie eelarve koostamise protsessi. Kõik need funktsioonid põhinevad nutikatel masinõppemudelitel. Kui need uued võimalused on kombineeritud hankija maksete ja kogumite automaatikaga, pakuvad need rikkalikku ja nutikat finantssüsteemi, mis juhib otsustusprotsessi ja aitab teil võtta meetmeid, et tõhusalt reageerida praegustele ja oodatavatele ettevõtluse väljakutsetele.

Finantsülevaadete eelversioon on proovimiseks saadaval juurutustes Ameerika Ühendriikides, Euroopas ja Ühendkuningriigis. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.

Eelversiooni funktsioone saab ja tuleb sisse lülitada ainult järgu 2 liivakasti keskkondades. Liivakasti keskkonnas loodud seadistust ja tehisintellekti (AI) mudeleid ei saa töökeskkonda migreerida. Lisateavet leiate teemast [Microsoft Dynamics 365 eelversioonide täiendavad kasutustingimused](https://docs.microsoft.com/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.).

## <a name="prerequisites"></a>Eeltingimused

Selles jaotises loetletakse finantsülevaadete kasutamise nõuded. Kui see on võimalik, esitatakse täiendavate teabeallikate lingid.

### <a name="legal-requirements"></a>Juriidilised nõuded

Eelversiooni programmi rakendamiseks täitke [rakenduse Dynamics 365 Finance finantsülevaadete eelversiooni leping](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Süsteeminõuded

Finantsülevaadete eelversiooni jaoks on nõutav järgu 2 liivakasti keskkond (mitme kastiga). Taustteavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

### <a name="version-requirements"></a>Versiooninõuded

See dokument kehtib rakenduse Finance and Operations versioonile 10.0.11 (platvormi värskendus 35) ja hilisematele versioonidele.

### <a name="historical-data-requirements"></a>Ajalooliste andmete nõuded

Kliendi maksmise prognoosimise funktsiooni jaoks kasutatava masinõppemudeli õigesti treenimiseks on nõutav vähemalt ühe aasta jagu kliendiarveid.

Demosüsteemide jaoks, millel on Contos demoandmete komplekt, on saadaval näidisandmed.

### <a name="role-and-permission-requirements"></a>Rolli ja õiguste nõuded

Keskkondades Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps ja Azure tehakse muudatusi. Nende keskkondade puhul on nõutavad õiged load. Allpool on mõned näited muudatustest, mis tehakse.

- Teenuses Microsoft Power Platform luuakse uus keskkond.
- Azure’is luuakse uus talletamise konto, võtme seif ja rakendus.
- Active Directory rentniku administraator peab andma AI Builderi rakendusele loa andmejärvele juurdepääsuks.
- Funktsioon lülitatakse sisse rakenduses Dynamics 365.

Selle protsessi läbimisel on kasu keskkondades Azure, Microsoft Dataverse ja LCS ressursside loomise ja haldamise protsessi tundmisest.

## <a name="configure-finance-insights"></a>Finantsülevaadete konfigureerimine

Enne finantsülevaadete kasutamist peate täitma mõned konfigureerimise etapid. Lisateavet finantsülevaadete konfigureerimise kohta vt jaotisest [Finantsülevaadete konfigureerimine](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Andmeintegraatori projekti loomine

Peate looma andmeintegraatori projekti, et masinõppemudeli loodavad andmed saaksid liikuda rakendusse Dynamics 365 Finance. Sellise projekti loomise sammud leiate teemast [Andmeintegraatori projekti loomine](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finantsülevaadete võimaluste lubamine

Kui olete konfigureerimise etapid lõpule viinud ja häälestanud demoandmed, peate lülitama sisse ja häälestama kõik võimalused, mida kavatsete kasutada: kliendimaksete prognoosimine, rahavoo prognoosimine ja eelarvesoovitused.

### <a name="enable-customer-payment-predictions"></a>Kliendimaksete prognoosimise lubamine
Kui kasutate kliendimaksete prognoosimise testimiseks demoandmeid, võib olla vajalik, et oma tehisintellekti mudeli loomise õnnestumiseks peate importima täiendavad demoandmed. Lisateavet demoandmete importimise kohta vt teemast [Maksmise prognoosideks demoandmete häälestamine](set-up-demo-data.md).

Kliendimaksete prognooside lubamiseks peate viima lõpule etappide kogumi, et luua teie organisatsiooni andmeid kasutav masinõppemudel, et luua prognoose, millal kliendid tõenäoliselt tasuvad laekumata arved ja millal konkreetsed arved tõenäoliselt tasutakse. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Kliendimakse prognooside lubamine](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine
Rahavoo prognoosimise lubamiseks peate viima lõpule etappide kogumi, et luua teie organisatsiooni andmeid kasutav masinõppemudel, et luua rahavoo prognoose. Lisateavet ja konkreetseid lõpule viimise etappe vt teemast [Rahavoo prognooside lubamine](enable-cash-flow-forecasting.md). 

### <a name="set-up-and-use-cash-flow-forecasting"></a>Rahavoo prognoosimise häälestamine ja kasutamine
Lisateavet rahavoo häälestamise ja kasutamise kohta vt teemast [Rahavoo prognoosimise lubamine](enable-cash-flow-forecasting.md). Lisateavet selle võimaluse kasutamise kohta vt teemast [Rahavoo prognoosimine](cash-flow-forecast-intro.md).

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
- Teavet selle kohta, kuidas kasutada tehisintellekti mudelit pikaajalise rahavoo projekteerimiseks, vt teemast [Rahavoo prognooside ülevaade](cash-position.md).
- Teavet rahavoo positsioonide ja rahavoo prognooside hetktõmmistena salvestamise ning hetktõmmise tegelike näitajatega võrdlemise kohta vt teemast [Hetktõmmiste ülevaade](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Eelarvesoovituse kasutamine

Teavet eelarve loomise kiirendamise kohta vt teemast [Eelarvesoovitused](budget-proposals.md). 

Eelarvesoovituse demoandmed.

## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui soovite anda tagasisidet või vajate tuge, saatke meil [kliendimaksete ülevaadetele (eelversioon)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Privaatsusavaldus

Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]