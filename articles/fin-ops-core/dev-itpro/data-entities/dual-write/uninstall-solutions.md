---
title: Topeltkirjutusega rakenduste orkestratsioonilahenduste desinstallimine
description: See artikkel kirjeldab, kuidas desinstallida topeltkirjutusega rakenduse orkestratsiooni lahendusi.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: fd9dc98ec1323a2ef262a330a400a6bd3833e554
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288726"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Topeltkirjutusega rakenduste orkestratsioonilahenduste desinstallimine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas desinstallida topeltkirjutusega rakenduse orkestratsiooni lahendusi.

Mõned kliendid installivad tahtmatult topeltkirjutusega rakenduse orkestratsioonipaketi, mis installib oma keskkonnas mitu Microsoft Dataverse lahendust. Lisalahenduste installimine pakendisse võib põhjustada ootamatuid ja ootamatuid probleeme.

Topeltkirjutusega rakenduse orkestratsioonipaketi installimisega seotud probleemide lahendamiseks desinstallige soovimatud topeltkirjutuslahendused järgmises järjekorras:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (kui on)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (lahenduse desinstallimiseks peate koos Microsoftiga avama tugipileti).
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Kui osapoole ja globaalse aadressiraamatu lahendused installiti, desinstallige lahendused järgmises järjekorras:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainextended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Osapool
1. Dynamics365Company_managed
1. Valuuta vahetuskursi määrad
1. msdyn_AssetCommon
1. FieldServiceCommon
