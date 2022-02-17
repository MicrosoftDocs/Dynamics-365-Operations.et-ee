---
title: Finance Insights häälestusprobleemide tõrkeotsing
description: Selles teemas loetletakse probleemid, mis võivad ilmneda Finance Insights võimaluste kasutamisel. See selgitab ka nende probleemide lahendamist.
author: panolte
ms.date: 01/29/2022
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
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: f77cddfdab22bef8af7f62d49723e330c4f13261
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064862"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insights häälestusprobleemide tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas loetletakse probleemid, mis võivad ilmneda Finance Insights võimaluste kasutamisel. See selgitab ka nende probleemide lahendamist.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Sümptom: Miks ei saa vastendada kliendimakse vihjeid andmeintegratsiooni malli sihtveeruga?

### <a name="resolution"></a>Lahendus

Te võite kasutada malli varasema versiooni jaoks. Enne versiooni 10.0.17 väljalaset konfigureerisid eelvaate kliendid **Kliendi makseülevaadete tulemused (CDS fini ja Opsi)** andmeintegratsiooni (DI) malli, kasutades **Makse ennustuse tulemust (eelvaade)**. Pärast versiooniks 10.0.17 ja uuemaks täiendamist peaksite vastendamise lõpule viimiseks kasutama **Kliendi makseülevaate tulemusi (CDS finiks ja ops 10.0.17 ja uuemat versiooni)**. Võimalik, et te ei saa DI-malli sihtveeru vastendada enne, kui andmehalduse üksuse loend on värskendatud ja **Makse ennustuse tulemuse** üksus ilmub selles. Üksuseloendi värskendamiseks ja makseennustuse tulemuse näitamiseks läbite sammud mõlemas, Microsoft Dynamics 365 Finance kui ka Dataverse (varem tuntud kui Common Data Service \[CDS\] haldusportaal).

### <a name="in-finance"></a>Finantsides

Järgige neid samme jaotises „Finantsid” pärast täiendust.

1. Minge jaotisse **Süsteemihaldus \> Tööruumid \> Andmehaldus**.
2. Valige tööruumis **Andmehaldus** paan **Raamistiku parameetrid**.
3. Lehel **Andmete importimise/eksportimise raamistiku parameetrid** valige **Üksuse sätted** ja seejärel valige **Üksuste loendi värskendamine**.
4. Sulgege leht **Andmete importimise/eksportimise raamistiku parameetrid**.
5. Valige tööruumis **Andmehaldus** paan **Andmeüksused**.
6. Otsige „Makse ennustuse tulemus”. Veenduge, et **Makse ennustuse tulemuse** üksus pole eelvaate versioon. Eelvaate versiooni nimi on lõpuga „(eelvaade).” Kui te näete ainult üksuse eelvaate versiooni, võtke ühendust Microsofti toega.

### <a name="in-dataverse"></a>Asukohas Dataverse

Järgige neid samme [Power Platform halduskeskuses](https://admin.powerplatform.microsoft.com/environments) andmete integreerimisprojektide uuendamiseks.

1. Kui kasutate Finance Insights eelvaate versiooni, eemaldage **Kliendi makse vihjete tulemustega (CDS fini ja Ops)** malliga seotud DI-projekt.
2. Järgige samme [andme integraatori projekti loomiseks](create-data-integrate-project.md). Kasutage **Kliendi makse vihjete tulemuste (CDS fini ja ops 10.0.17 ja hilisemaid)** malle.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Sümptom: Kui proovin avada AI Builder kliendi makseprognooside häälestuslehel olevate linkide abil, siis miks kuvatakse järgmine tõrketeade: "Vabandust, on toimunud lahtiühendamine"?

### <a name="resolution"></a>Lahendus

Dynamics 365 Finance kasutajatel peab olema Microsoft Power Apps keskkonna kasutajakonto ja sellel kasutajakontol peab olema süsteemikohandaja roll. Süsteemiadministraator Microsoft Power Apps saab luua kasutajakonto ja määrata rolli. Seejärel saate selle kasutajakonto abil sisse logida <https://make.preview.powerapps.com/> ja linke uuesti proovida.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Sümptom: Miks ei kuva rahaprognoosi vahekaart rahavoo prognoosi tööruumis andmeid?

### <a name="resolution"></a>Lahendus

Likviidsuse prognoosimise funktsioon sularaha ja panga halduses ja Finance Insights likviidsuse prognoosimise funktsioon finantsülevaadetes peavad olema seadistatud ja lubatud andmete õigesti kuvamiseks tööruumis **Rahavoo prognoos**.

Kõigepealt seadistage ja lubage likviidsuse prognoosimine ja likviidsuse kontod. Lisateavet vt teemast [Rahavoo planeerimine](../cash-bank-management/cash-flow-forecasting.md). Kui see seadistus on lõpule viidud, kuid te ei näe eeldatud tulemusi, siis vaadake [Rahavoo prognoosimise häälestuse tõrkeotsingut](../cash-bank-management/cash-flow-forecasting-tsg.md) lisateabe saamiseks.

Seejärel kinnitage, et Finance Insights likviidsuse prognoosimise funktsioon (**Sularaha ja pangahalduse \> Seadistus \> FInance Insights \> Likviidsuse prognoosid**) on lubatud ja et AI-mudeli koolitus on lõpetatud. Kui koolitus pole lõpetatud, valige **Prognoosi nüüd** mudeli koolitusprotsessi käivitamiseks.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Sümptom: miks pole lifecycle'i teenustes Microsoft Dynamics nähtav nupp Installi uus lisandmoodul?

### <a name="resolution"></a>Lahendus

Esmalt veenduge, et keskkonnahalduri **või** projekti omaniku **roll on määratud sisselogitud kasutajale** projekti turberolli **väljal** Elutsükli teenused Microsoft Dynamics(LCS). Uute lisandmoodulite installimiseks on vaja ühte neist projekti turberollidest.

Kui teile on määratud õige projekti turberoll, peate võib-olla **värskendama brauseriakent**, et näha nuppu Installi uus lisandmoodul.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Sümptom: Lisandmoodulit Finance insights ei ole installitud. Miks see nii on?

### <a name="resolution"></a>Lahendus

Järgmised sammud oleks tulnud lõpule viia.

- Veenduge, et teil on **Power Portali halduskeskuses süsteemiadministraator** ja **süsteemikohandaja** juurdepääs.
- Veenduge, et Dynamics 365 Finance lisandmoodulit installivale kasutajale rakendatakse või samaväärset litsentsi.
- Veenduge, et järgmine Azure AD rakendus on registreeritud:Azure AD 

  | Avaldus                  | Rakenduse kood           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Sümptom: tõrge: "Me ei leidnud valitud filtrivahemiku kohta andmeid. Palun valige mõni muu filtrivahemik ja proovige uuesti." 

### <a name="resolution"></a>Lahendus

Kontrollige andmeintegraatori seadistust, et kinnitada, et see toimib ootuspäraselt AI Builder ja muudab andmed tagasi finance'i.  
Lisateavet vt teemast [Create a data integration project](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Sümptom: Kliendi makse ennustuskoolitus ebaõnnestus ja veas AI Builder öeldakse: "Prognoosil peaks mudeli koolitamiseks olema ainult 2 erinevat tulemusväärtust. Kaart kahe tulemusega ja ümberõpe", "Koolitusaruande küsimus: IsNotMinRequiredDistinctNonNullValues".

### <a name="resolution"></a>Lahendus

See tõrge näitab, et viimase aasta jooksul ei ole piisavalt ajaloolisi tehinguid, mis esindavad iga kategooriat **, mida on kirjeldatud kategooriates On-time**, **Late** ja **Very Late**. Selle tõrke lahendamiseks kohandage **väga hilinenud** kandeperioodi. Kui väga hilise kandeperioodi kohandamine **viga ei paranda,** ei ole kliendimaksete ennustused **parim lahendus, mida kasutada, kuna see vajab koolituse eesmärgil andmeid igas kategoorias.**

Lisateavet on õigeaegselt, hiliste **ja** väga hiliste **kategooriate kohandamise** kohta leiate teemast **Kliendimakse prognooside lubamine**. [...](../finance-insights/enable-cust-paymnt-prediction.md)

## <a name="symptom-model-training-failed"></a>Sümptom: mudelikoolitus nurjus

### <a name="resolution"></a>Lahendus

Rahavoogude **prognoosi** mudeli koolitus nõuab andmeid, mis hõlmavad rohkem kui ühte aastat ja sisaldavad rohkem kui 100 tehingut. Need kanded peavad mõjutama likviidsuskontosid, mis sisalduvad rahavoogude prognoosi seadistuses.

Kliendi **makseprognooside** tegemiseks on prognooside tegemiseks vaja vähemalt 100 kliendiarvet ja maksetehingut viimase kuue kuni üheksa kuu jooksul.  
