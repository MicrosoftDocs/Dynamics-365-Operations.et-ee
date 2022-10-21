---
title: Arve hõivamise lahenduse installimine
description: See artikkel annab teavet selle kohta, kuidas installida arve hõivamise lahendus ja integreerida see Microsoft Dynamics 365 finantsiga.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690980"
---
# <a name="install-the-invoice-capture-solution"></a>Arve hõivamise lahenduse installimine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Kui installisite lahenduse privaatses eelvaates, peate vana lahenduse enne jätkamist desinstallima.

## <a name="prerequisites"></a>Eeltingimused

Enne arve hõivamise lahenduse installimist peate lõpule täitma järgmised eeltingimused:

1. Registreerige rakendus ja lisage Microsoftile () kliendisaladus Azure Active Directory oma Azure AD Azure’i kordustellimuse all. Lisateavet vt teemast Veebirakenduse [registreerimine AAD-ga](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Märkige rakenduse (kliendi **) ID**, **·** **kliendi saladus ja rentniku ID** väärtused üles, sest neid on vaja hiljem.

2. Registreerige Azure’i rakendus Dynamics 365 finantskeskkonnas. Lisateavet vt teemast Välise rakenduse [registreerimine](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Lahenduse installimine ja häälestamine

Arve hõivamise lahenduse installimiseks minge ja AppSource valige link [Dynamics 365 arve hõivamise eelvaate versiooni jaoks](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Kui installimine on lõpule viidud, näete lahenduse installituna valitud keskkonnas Power Apps.

Seadistuse lõpuleviimiseks järgige neid samme.

1. Laadige alla [abilahendus](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) järgmiste üksikasjade häälestamiseks.

    - Suhtlus keskkonna Microsoft Power Platform ja finantskeskkonna vahel
    - Kanali kasutatav Dataverse ühenduse Office 365 viide ja Outlooki viide

2. Minge Power Apps oma keskkonda ja valige suvand **Impordi lahendus**.
3. Valige **sirvimine**, valige allalaaditud abilahenduse pakett ja seejärel valige **Edasi**.
4. Valige **Edasi**.
5. Määrake olemasolev ühendus või looge uus ühendus, valides uue **ühenduse**.
6. Pärast paketi edukat importimist avage **Dynamics 365 arve hõivamine – installitööriistad**.
7. Käivitage pilvevoog arve hõivamise lahenduse ja finantside vahelise ühenduse Microsoft Power Platform häälestamiseks.
8. Valige **käivitamine** ja määrake järgmised parameetrid:

    - **Dynamics 365 finantside URL** – finantskeskkonna URL, millega soovite integreerida.
    - **Rentniku ID – finantskeskkonna rentniku ID**.
    - **Kliendi ID** – Azure’i rakenduse ID, mis registreeriti.
    - **Kliendi saladus** – kliendi saladus, mis loodi Azure’i rakenduse jaoks.
