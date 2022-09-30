---
title: Finantsülevaadete konfiguratsioon
description: See artikkel selgitab konfiguratsiooni samme, mis võimaldavad süsteemil kasutada finantsülevaadetes saadaolevaid võimalusi.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573190"
---
# <a name="configuration-for-finance-insights"></a>Finantsülevaadete konfiguratsioon

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finantsülevaated koondavad rakenduse Microsoft Dynamics 365 Finance Dataverse funktsioonid rakendusega Azure AI Builder ja pakuvad organisatsioonile võimast prognoosimise tööriistu. See artikkel selgitab konfiguratsiooni samme, mis võimaldavad süsteemil kasutada finantsülevaadetes saadaolevaid võimalusi. Selle artikli protseduuride [edukaks lõpetamiseks peab teil olema Süsteemiadministraatori ja Süsteemi kohandaja juurdepääs Power Portali](https://admin.powerplatform.microsoft.com/) halduskeskuses, süsteemiadministraatori juurdepääs Dynamics 365 Finantsis ja juurdepääs keskkonnade loomisele elutsükli teenustes Microsoft Dynamics (LCS).

> [!NOTE]
> Finantside vihjete häälestamise järgmised protseduurid kehtivad Dynamics 365 Finance versiooni 10.0.21 ja uuemate versioonide puhul.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 finantside juurutamine

Keskkonna juurutamiseks tehke järgmist.

1. LCS-is looge või värskendage Dynamics 365 finantskeskkonda. Keskkond nõuab rakenduse versiooni 10.0.21 või uuemat versiooni.

    > [!NOTE]
    > Keskkond peab olema suure kättesaadavusega (HA) keskkond. (Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Kui konfigureerite finantsülevaateid vihjete kaustas, peate võib-olla tootmisandmed enne prognooside tööd kopeerima. Ennustuse mudel kasutab prognooside koostamiseks mitmeid aastaid andmeid. Contoso demoandmed ei sisalda piisavalt ajaloolisi andmeid ennustuse mudeli aktsepteerimiseks. 

## <a name="configure-your-azure-ad-tenant"></a>Oma rentniku Azure AD konfigureerimine

Azure Active Directory(Azure AD) peab olema konfigureeritud nii, et seda saab kasutada koos Dataverse rakendusega ja rakendustega Microsoft Power Platform. Selle konfiguratsiooni puhul peab **projekti omaniku** roll **või keskkonnahalduri** **roll olema määratud kasutajale LCS-i projekti** turberolli väljal.

Kontrollige, et järgmine seadistus oleks lõpule viidud:

- Teil on **Süsteemiadministraator** ja **Süsteemi kohandaja** juurdepääs Power Portali halduskeskuses.
- Dynamics 365 Finance või sellega võrdväärset litsentsi rakendatakse finantside vihjete lisandmooduli installi kasutajale.
- Järgmised rakendused Azure AD on registreeritud rakenduses Azure AD.

    |  Avaldus                             | Rakenduse kood                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Avalduse registreerimise kontrollimiseks kontrollige Azure AD kõikide avalduste **loendit**. Lisateavet vt teemast Ettevõtte [avalduste kuvamine](/azure/active-directory/manage-apps/view-applications-portal).
  
    Kui rakendust ei ole registreeritud, pöörduge Azure AD tugiteenuste poole.
  
## <a name="configure-dataverse"></a>Dataverse konfigureerimine

Kasutage järgmisi samme Finance Insights Dataverse konfigureerimiseks.

- Avage keskkonnaleht LCS-is ja kontrollige, et **Power Platform integreerimisjaotis** on juba seadistatud.

    - Kui Dataverse see nimi on juba häälestatud Dataverse, tuleks finantskeskkonnaga lingitud keskkonna nimi loetleda.
    - Kui Dataverse seda pole veel seadistatud, valige häälestus **.** Keskkonna seadistus Dataverse võib aega võtta kuni tund. Kui seadistus on edukalt lõpule viidud Dataverse, tuleks loetleda finantskeskkonnas lingitud keskkonna nimi.
    - Kui selline integratsioon seadistati olemasoleva keskkonnaga Microsoft Power Platform, võtke ühendust oma administraatoriga veendumaks, et lingitud keskkond ei ole keelatud olekus.

        Lisateavet vt integratsiooni [lubamine Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Juurdepääsuks haldussaidile Microsoft Power Platform minge .<https://admin.powerplatform.microsoft.com/environments>

## <a name="configure-the-finance-insights-add-in"></a>Finance insights lisandmooduli konfigureerimine

Kui installisite eelnevalt finantside vihjete lisandmooduli, desinstallige see enne järgmise protseduuri lõpule viimist.

> [!NOTE]
> Kui olete juba installinud andmete lisamise LCS-i, kasutavad finantside vihjed seda prognooside jaoks vajalike andmete salvestamiseks. Kui te pole veel LCS-i data add-ina installinud, loob finantside vihjete lisandmoodul teie eest hallatud andmed.

Järgige neid samme Finance insights lisandmooduli installimiseks.

1. Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.
2. Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
3. Valige **Finance insights** lisandmoodul.
4. Nõustuge tingimustega ja valige seejärel **Installi**.

Lisandmooduli installimiseks võib aega kuluda mitu minutit.

## <a name="one-last-thing"></a>Üks viimane asjandus...

Kui lisandmoodul on edukalt installitud, võib selleks olla aega 1 tund, enne kui saate dynamics 365 Finance funktsioonihalduse tööruumis **finantsülevaate** funktsioone lubada. Kui te ei soovi nii kaua oodata, saate ülevaatete ettevalmistamise **olekukontrolli käsitsi käivitada**. 

1. Rakenduses Dynamics 365 Finance minge süsteemihalduse **seadistusprotsessi \> automatiseerimisprogrammi \>.**
2. Leidke taustaprotsesside **vahekaardilt** Vihjete **ettevalmistamise oleku kontroll ja** valige käsk **Redigeeri**.
3. Seadke järgmise **käivitamise välja** väärtuseks 30 minutit enne praegust kellaaega.

   See muudatus peaks muutma vihjete **ettevalmistamise olekukontrolli** protsessi kohe käivituma.

   Kui vihjete **ettevalmistamise oleku kontrollprotsess** on edukalt käitatud, saate funktsioonihalduse tööruumi finantsülevaadete **funktsioonid lubada**.

> [!NOTE]
> Kui vihjete vabastamise olekukontrolli **protsessi ei käitata, minge süsteemihalduse** päringute **pakett-töödesse** > **·** > **.** Muutke väljal **Automatiseerimise pollimissüsteem** väärtuseks Protsessi **käivitamiseks** ootel. 
> 
## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui olete tagasiside pakkumisest huvitatud või teil on vaja tuge, saatke finantside [vihjetele meilisõnum (eelvaade).](mailto:fiap@microsoft.com)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
