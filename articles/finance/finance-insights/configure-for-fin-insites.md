---
title: Finance'i statistika konfiguratsioon
description: See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.
author: ShivamPandey-msft
ms.date: 01/27/2022
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
ms.openlocfilehash: b9bad6445e9e77688f66c6c4186422d7a898edd7
ms.sourcegitcommit: 7fc0a9a6440ac087292e9e76c26c67f56154b9e6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/28/2022
ms.locfileid: "8051366"
---
# <a name="configuration-for-finance-insights"></a>Finance'i statistika konfiguratsioon

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights ühendab Microsofti Dynamics 365 Finance Dataverse funktsioonid Azure'iga ja AI Builder pakub teie asutusele võimsaid prognoosimisvahendeid. See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi. Selle teema protseduuride edukaks lõpuleviimiseks peab teil olema süsteemiadministraator ja süsteemikohandaja juurdepääs [Power Portali halduskeskuses](https://admin.powerplatform.microsoft.com/), süsteemiadministraatori juurdepääs rakenduses Dynamics 365 Finance ja juurdepääs elutsükliliste teenuste (LCS) keskkondade Microsoft Dynamics loomisele.

> [!NOTE]
> Järgmised protseduurid Finance Insightsi häälestamiseks kehtivad versiooni 10.0.21 ja uuemate Dynamics 365 Finance versioonide puhul.

## <a name="deploy-dynamics-365-finance"></a>Rakenduse Dynamics 365 Finance juurutamine

Keskkonna juurutamiseks tehke järgmist.

1. Looge või värskendage Dynamics 365 Finance LCS-is keskkonda. Keskkond nõuab rakenduse versiooni 10.0.21 või uuemat versiooni.

    > [!NOTE]
    > Keskkond peab olema kõrge kättesaadavusega (HA) keskkond. (Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Kui konfigureerite finance'i ülevaateid liivakastikeskkonnas, peate võib-olla enne prognooside töötamist kopeerima tootmisandmed sellesse keskkonda. Ennustuse mudel kasutab prognooside koostamiseks mitmeid aastaid andmeid. Contoso demoandmed ei sisalda piisavalt ajaloolisi andmeid ennustusmudeli adekvaatseks koolitamiseks. 

## <a name="configure-your-azure-ad-tenant"></a>Rentniku konfigureerimine Azure AD

Azure Active Directory(Azure AD) peab olema konfigureeritud nii, et seda saaks kasutada ja Dataverse rakendusi kasutada Microsoft Power Platform. See konfiguratsioon nõuab, et LCS-i väljal Projekti turberoll **määratakse kasutajale** kas **projekti omaniku** roll või **keskkonnahalduri** roll.

Veenduge, et järgmine häälestus on lõpule viidud.

- Power Portali halduskeskuses on **juurdepääs süsteemiadministraatori** ja **süsteemikohandaja** juurdepääsule.
- Dynamics 365 Finance Lisandmoodulit Finance insights installivale kasutajale rakendatakse või samaväärset litsentsi.

Järgmised Azure AD rakendused on registreeritud rakenduses Azure AD.

|  Avaldus                             | Rakenduse kood                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>Dataverse konfigureerimine

Kasutage järgmisi samme Finance Insights Dataverse konfigureerimiseks.

- Avage keskkonnaleht LCS-is ja kontrollige, et **Power Platform integreerimisjaotis** on juba seadistatud.

    - Kui Dataverse see on juba seadistatud, Dataverse tuleks loetleda finantskeskkonnaga lingitud keskkonnanimi.
    - Kui Dataverse pole veel häälestatud, valige **Häälestus**. Keskkonna seadistamine Dataverse võib võtta kuni tund. Kui seadistus on edukalt lõpule viidud, Dataverse tuleks loetleda keskkonnanimi, mis on lingitud rahanduskeskkonnas.
    - Kui see integratsioon on seadistatud olemasoleva Microsoft Power Platform keskkonnaga, võtke ühendust oma administraatoriga, et veenduda, et lingitud keskkond pole keelatud olekus.

        Lisateavet vt teemast [Integrationi lubamine Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Haldussaidile Microsoft Power Platform juurdepääsemiseks minge veebisaidile <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Finance insights lisandmooduli konfigureerimine

Kui olete varem installinud lisandmooduli Finance Insights, desinstallige see enne järgmise toimingu sooritamist.

> [!NOTE]
> Kui olete andmejärve lisandmooduli LCS-i juba installinud, kasutab Finance Insights seda prognooside jaoks vajalike andmete salvestamiseks. Kui te pole veel LCS-i andmejärve lisandmoodulit installinud, loob lisandmoodul Finance insights teile hallatava andmejärve.

Järgige neid samme Finance insights lisandmooduli installimiseks.

1. Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.
2. Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
3. Valige **Finance insights** lisandmoodul.
4. Nõustuge tingimustega ja seejärel valige **Installi**.

Lisandmooduli installimiseks võib aega kuluda mitu minutit.

## <a name="one-last-thing"></a>Veel üks asi...

Kui lisandmoodul on edukalt installitud, võib kuluda kuni tund, enne kui saate lubada rakenduse funktsioonihalduse **tööruumis** Finance Insightsi funktsioonid Dynamics 365 Finance. Kui te ei soovi nii kaua oodata, saate ülevaate ettevalmistamise olekukontrolli **protsessi käsitsi käivitada**. 

1. Dynamics 365 Finance Avage jaotises **Süsteemihalduse \> häälestusprotsesside \> automatiseerimine**.
2. peal **Taustaprotsessid** vahekaart, leia **Insightsi ettevalmistamise oleku kontroll** ja valige **Muuda**.
3. Määrake **Järgmine hukkamine** välja 30 minutit enne praegust kellaaega.

   See muudatus peaks sundima **Insightsi ettevalmistamise oleku kontroll** protsessi kohe käivitada.

   Pärast **Insightsi ettevalmistamise oleku kontroll** protsess on edukalt käivitatud, saate lubada rakenduses Finance Insighti funktsioonid **Funktsioonide haldamine** tööruum.

> [!NOTE]
> Kui **Insightsi ettevalmistamise oleku kontroll** protsess ei käivitu, minge aadressile **Süsteemi haldus** > **Päringud** > **Partiitööd**. Aastal **Protsessiautomaatika küsitlussüsteem** muutke väärtuseks **Ootan** protsessi algatamiseks. 
> 
## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui olete huvitatud tagasiside andmisest või kui vajate tuge, saatke e-kiri aadressile [Finantsstatistika (eelvaade)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
