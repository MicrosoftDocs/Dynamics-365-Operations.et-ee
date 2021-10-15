---
title: Finance Insights häälestusprobleemide tõrkeotsing
description: Selles teemas loetletakse probleemid, mis võivad ilmneda Finance Insights võimaluste kasutamisel. See selgitab ka nende probleemide lahendamist.
author: panolte
ms.date: 08/20/2021
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
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512886"
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

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Sümptom: Miks ei kuva rahaprognoosi vahekaart rahavoo prognoosi tööruumis andmeid?

### <a name="resolution"></a>Lahendus

Likviidsuse prognoosimise funktsioon sularaha ja panga halduses ja Finance Insights likviidsuse prognoosimise funktsioon finantsülevaadetes peavad olema seadistatud ja lubatud andmete õigesti kuvamiseks tööruumis **Rahavoo prognoos**.

Kõigepealt seadistage ja lubage likviidsuse prognoosimine ja likviidsuse kontod. Lisateavet vt teemast [Rahavoo planeerimine](../cash-bank-management/cash-flow-forecasting.md). Kui see seadistus on lõpule viidud, kuid te ei näe eeldatud tulemusi, siis vaadake [Rahavoo prognoosimise häälestuse tõrkeotsingut](../cash-bank-management/cash-flow-forecasting-tsg.md) lisateabe saamiseks.

Seejärel kinnitage, et Finance Insights likviidsuse prognoosimise funktsioon (**Sularaha ja pangahalduse \> Seadistus \> FInance Insights \> Likviidsuse prognoosid**) on lubatud ja et AI-mudeli koolitus on lõpetatud. Kui koolitus pole lõpetatud, valige **Prognoosi nüüd** mudeli koolitusprotsessi käivitamiseks.
