---
title: Arvutuse lisamine toote konfiguratsioonimudelile
description: See protseduur näitab, kuidas lisada toote konfiguratsioonimudelile uut arvutust.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987050"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Arvutuse lisamine toote konfiguratsioonimudelile

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas lisada toote konfiguratsioonimudelile uut arvutust. See näitab, kuidas saate koostada loogikaavaldise, määrates tehtemärgiga „If” kõlari kõrguseks 10 valgete kõlarite ja 15 kõigi muude korpuse viimistluste puhul. See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.


## <a name="add-a-calculation"></a>Arvutuse lisamine

## <a name="create-calculation-expression"></a>Arvutusavaldise koostamine
1. Klõpsake käsku Muuda avaldist.
2. Sisestage väljale ConstraintBody tekst If[CabinetFinish=="White", 10, 15].
3. Klõpsake suvandit Kinnita.
4. Klõpsake valikut Sule.
5. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]