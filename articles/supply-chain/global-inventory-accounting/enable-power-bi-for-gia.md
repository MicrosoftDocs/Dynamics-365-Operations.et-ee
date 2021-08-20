---
title: Global Inventory Accounting teenuses Power BI lubamine
description: See teema kirjeldab, kuidas lubada Microsoft Power BI teenuses Global Inventory Accounting.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 562b56a85ad2f40cb673f8f2101bf92c39853d1f1a087d0498b6f7d19d1cca01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773341"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Global Inventory Accounting teenuses Power BI lubamine

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Oma [PowerBI.com](https://powerbi.com/) kontolt rakenduse Microsoft Dynamics 365 tööruumi saate kinnitada paanid, armatuurlaudad ja aruanded.

## <a name="prerequisites"></a>Eeltingimused

Power BI aruandluse lubamiseks peavad olema täidetud järgmised eeltingimused.

- Te peate olema Dynamics 365 rakenduse süsteemiadministraator.
- Teil peab olema [PowerBI.com](https://powerbi.com/) konto.
- Kontol peab olema vähemalt üks töölaud ja üks Power BI aruanne.
- Peate olema Azure Active Directory (Azure AD) konto administraator.
- Azure AD domeen peab olema sama domeen, mida kasutate oma [PowerBI.com](https://powerbi.com/) konto jaoks.

## <a name="setup"></a>Seadistus

Power BI integratsiooni seadistamiseks läbige need etapid.

1. Logige sisse rakendusse [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Minge **ühiskasutuse varateeki**, valige varatüübiks **Power BI aruandemudel** ja laadige alla **Global Inventory Accounting** pakett. 
1. Logige sisse [PowerBI.com](https://app.powerbi.com/) ja laadige üles **Global Inventory Accounting** Power BI aruande fail järgmiste sammude abil.

    1. Valige suvand **Uus**.
    1. Valige **Laadi fail üles**.
    1. Valige **Global Inventory Accounting** Power BI aruande fail.

1. Konfigureerige **Global Inventory Accounting** Power BI aruanne järgmiste sammude abil.

    1. Minge tööruumi **Minu tööruum**, leidkeGlobal Inventory Accounting andmekogum ja seejärel valige menüü **Suvandid** käsk **Sätted**.
    1. **Globaalse laoarvestuse sätetes** laiendage **Parameetrid** ja uuendage kõiki parameetreid vastavalt vajadusele.

1. Registreerige rakendus vastavalt jaotisele [PowerBI.com integreerimise konfigureerimine](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integreerige **Global Inventory Accounting** Power BI aruande fail teenusesse Dynamics 365 Supply Chain Management järgmiste sammude abil.

    1. Valige suvandid **Süsteemihaldus \> Häälestus \> PowerBI.com konfiguratsioon**.
    1. Valige suvand **Redigeeri**.
    1. Valige **Luba PowerBI.Com integreerimine**.
    1. Sisestage väljale **Avalduse ID** rakenduse ID.
    1. Sisestage väljale **Avalduse võti** rakenduse võti.
    1. Valige käsk **Salvesta**.

1. Värskendage lehekülge nii, et ilmuks Power BI sisselogimise dialoogiaken.
1. Valige vahekaardil **Valikud** suvand **Ava aruandekataloog** ja seejärel valige varasemalt üleslaaditud **Global Inventory Accounting** Power BI aruande fail.
1. Värskendage lehte. Peaksite nägema, et teie aruanne on lisatud.
1. Valige **Power BI aruanded** all link **Global Inventory Accounting**.

Lisateabe saamiseks vt [PowerBI.com integratsiooni konfigureerimine](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
