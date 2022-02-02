---
title: Finance Insights häälestusprobleemide tõrkeotsing
description: Selles teemas loetletakse probleemid, mis võivad ilmneda Finance Insights võimaluste kasutamisel. See selgitab ka nende probleemide lahendamist.
author: panolte
ms.date: 11/03/2021
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
ms.openlocfilehash: c1bbdbec2bc0273a73ffc13a4cce024543af5a13
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968832"
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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Sümptom: kui püüan avada kliendi makseennustuse häälestuslehe linkide abil, siis miks kuvatakse järgmine AI Builder tõrketeade: "Kahjuks on katkestatud"?

### <a name="resolution"></a>Lahendus

Dynamics 365 Finance Kasutajatel peab olema Microsoft Power Apps keskkonna kasutajakonto ja kasutajakontol peab olema süsteemi kohandaja roll. Süsteemiadministraator Microsoft Power Apps saab luua kasutajakonto ja määrata rolli. Siis saate selle <https://make.preview.powerapps.com/> kasutajakontoga sisse logida ja proovida linke uuesti proovida.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Sümptom: Miks ei kuva rahaprognoosi vahekaart rahavoo prognoosi tööruumis andmeid?

### <a name="resolution"></a>Lahendus

Likviidsuse prognoosimise funktsioon sularaha ja panga halduses ja Finance Insights likviidsuse prognoosimise funktsioon finantsülevaadetes peavad olema seadistatud ja lubatud andmete õigesti kuvamiseks tööruumis **Rahavoo prognoos**.

Kõigepealt seadistage ja lubage likviidsuse prognoosimine ja likviidsuse kontod. Lisateavet vt teemast [Rahavoo planeerimine](../cash-bank-management/cash-flow-forecasting.md). Kui see seadistus on lõpule viidud, kuid te ei näe eeldatud tulemusi, siis vaadake [Rahavoo prognoosimise häälestuse tõrkeotsingut](../cash-bank-management/cash-flow-forecasting-tsg.md) lisateabe saamiseks.

Seejärel kinnitage, et Finance Insights likviidsuse prognoosimise funktsioon (**Sularaha ja pangahalduse \> Seadistus \> FInance Insights \> Likviidsuse prognoosid**) on lubatud ja et AI-mudeli koolitus on lõpetatud. Kui koolitus pole lõpetatud, valige **Prognoosi nüüd** mudeli koolitusprotsessi käivitamiseks.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Sümptom: miks ei installi elutsükli teenustes uut lisandmooduli Microsoft Dynamics nuppu?

### <a name="resolution"></a>Lahendus

Kõigepealt veenduge, et keskkonnahalduri või projekti omaniku roll on määratud sisse logitud kasutajale projekti turberolli **väljal** **·** **elutsükli** Microsoft Dynamics teenustes (LCS). Uute lisandmoodulite installimisel on vaja üht neist projekti turberollidest.

Kui teile on määratud õige projekti turberoll, peate võib-olla brauseri akent värskendama, et näha nuppu **Installi uus** lisandmoodul.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Sümptom: finantside vihjete lisandmoodulit ei installita. Miks see nii on?

### <a name="resolution"></a>Lahendus

Järgmised sammud peaksid olema lõpule viidud.

- Veenduge, et teil **on** Süsteemiadministraator ja **Süsteemi kohandaja juurdepääs Power** Portali halduskeskusele.
- Dynamics 365 Finance Kontrollige, kas lisandmooduli installinud kasutajale rakendatakse vastav litsents või sellega võrdne litsents.
- Kontrollige, et järgmine Azure AD rakendus on Azure AD registreeritud: 

  | Avaldus                  | Rakenduse kood           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
