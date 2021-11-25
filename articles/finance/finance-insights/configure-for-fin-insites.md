---
title: Finantsülevaadete konfiguratsioon
description: See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752974"
---
# <a name="configuration-for-finance-insights"></a>Finantsülevaadete konfiguratsioon

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finantsülevaated kombineerivad rakenduse Microsoft Dynamics 365 Finance funktsioonid teenustega Dataverse, Azure ja AI Builder, et pakkuda võimsaid prognoosimise tööriistu teie organisatsioonile. See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi. Selle teema protseduuride edukaks lõpetamiseks peab teil olema Süsteemiadministraatori ja Süsteemi kohandaja juurdepääs Power Portali halduskeskuses, süsteemiadministraatori juurdepääs sellele ja juurdepääs elutsükli [...](https://admin.powerplatform.microsoft.com/)Dynamics 365 Finance teenustes Microsoft Dynamics (LCS) keskkondade loomisele.

> [!NOTE]
> Finantside vihjete häälestamise järgmised protseduurid kehtivad versiooni Dynamics 365 Finance 10.0.21 ja uuemate versioonide puhul.

## <a name="deploy-dynamics-365-finance"></a>Rakenduse Dynamics 365 Finance juurutamine

Keskkonna juurutamiseks tehke järgmist.

1. Looge või uuendage LCS-i Dynamics 365 Finance keskkonda. Keskkond nõuab rakenduse versiooni 10.0.21 või uuemat versiooni.

    > [!NOTE]
    > Keskkond peab olema suure kättesaadavusega (HA) keskkond. (Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Kui konfigureerite finantsülevaateid vihjete kaustas, peate võib-olla tootmisandmed enne prognooside tööd kopeerima. Ennustuse mudel kasutab prognooside koostamiseks mitmeid aastaid andmeid. Contoso demoandmed ei sisalda piisavalt ajaloolisi andmeid ennustuse mudeli aktsepteerimiseks. 

## <a name="configure-dataverse"></a>Dataverse konfigureerimine

Kasutage järgmisi samme Finance Insights Dataverse konfigureerimiseks.

- Avage keskkonnaleht LCS-is ja kontrollige, et **Power Platform integreerimisjaotis** on juba seadistatud.

    - Kui see on juba seadistatud, tuleks loetleda Dataverse keskkonnaga Finance lingitud keskkonna nimi.
    - Kui seda pole veel häälestatud, valige **häälestus**. Keskkonna seadistus Dataverse võib võtta aega kuni tund. Kui seadistus on edukalt lõpule Dataverse viidud, tuleks loetleda finantskeskkonnaga lingitud keskkonna nimi.

## <a name="configure-the-finance-insights-add-in"></a>Finance insights lisandmooduli konfigureerimine

Kui installisite eelnevalt finantside vihjete lisandmooduli, desinstallige see enne järgmise protseduuri lõpule viimist.

> [!NOTE]
> Kui olete juba installinud andmete lisamise LCS-i, kasutavad finantside vihjed seda prognooside jaoks vajalike andmete salvestamiseks. Kui te pole veel LCS-i data add-ina installinud, loob finantside vihjete lisandmoodul teie eest hallatud andmed.

Järgige neid samme Finance insights lisandmooduli installimiseks.

1. Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.
2. Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
3. Valige **Finance insights** lisandmoodul.
4. Nõustu tingimustega ja vali installi **·**.

Lisandmooduli installimiseks võib aega kuluda mitu minutit.

## <a name="one-last-thing"></a>Üks viimane asjandus...

Pärast lisandmooduli edukat installimist võib selle aega võtta kuni tund, enne kui saate funktsioonihalduse tööruumis lubada finantsülevaate **·** Dynamics 365 Finance funktsioone. Kui te ei soovi nii kaua oodata, saate ülevaatete ettevalmistamise **olekukontrolli käsitsi** käivitada. 

1. Süsteemis Dynamics 365 Finance avage **süsteemihalduse \> seadistusprotsessi \>** automatiseerimine.
2. Leidke **·** taustaprotsesside vahekaardilt **Vihjete ettevalmistamise oleku kontroll** ja valige käsk **·** Redigeeri.
3. Seadke järgmise **käivitamise välja** väärtuseks 30 minutit enne praegust kellaaega.

   See muudatus peaks muutma **vihjete ettevalmistamise olekukontrolli** protsessi kohe käivituma.

   Kui **vihjete ettevalmistamise oleku** kontrollprotsess on edukalt käitatud, saate funktsioonihalduse tööruumi finantsülevaadete **funktsioonid** lubada.

## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui olete tagasiside pakkumisest huvitatud või teil on vaja tuge, saatke finantside vihjetele [meilisõnum](mailto:fiap@microsoft.com) (eelvaade).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
