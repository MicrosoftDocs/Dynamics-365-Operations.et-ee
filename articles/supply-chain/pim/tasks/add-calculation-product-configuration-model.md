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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32bc2ac5815c2739147664f1e1df2528178db51e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213396"
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

