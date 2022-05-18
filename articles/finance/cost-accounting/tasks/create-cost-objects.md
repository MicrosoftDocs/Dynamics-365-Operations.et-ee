---
title: 'Kuluobjektide loomine  '
description: See protseduur näitab, kuidas luua kuluobjekte, importides kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734126"
---
# <a name="create-cost-objects"></a>Kuluobjektide loomine   

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua kuluobjekte, importides kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse. Selle protseduuri loomiseks kasutati demoettevõtet USMF. 


## <a name="create-new-cost-objects"></a>Uute kuluobjektide loomine
1. Kuluobjekti **dimensioonide > avage > Kuluobjekti dimensioonid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Nimi**.
4. Sisestage **või valige väärtus väljal Andmeühendus** dimensiooni liikmete jaoks.
5. Sisestage väärtus väljale **Kirjeldus**.
6. Klõpsake nuppu **Salvesta**.

## <a name="configure-the-data-connector"></a>Andmekonnektori konfigureerimine
1. Klõpsake käsku **Konfigureeri dimensiooni liikme pakkujat**.
    * Valige CostCenter dimensiooni CostCenter importimiseks kuluarvestusse.  
2. Valige väljal **Dimensiooni** nimi väärtus Kulukeskus.
3. Klõpsake valikut **OK**.

## <a name="import-cost-centers"></a>Kulukeskuste importimine
1. Klõpsake käsku **Impordi dimensiooni liikmed**.
2. Klõpsake valikut **OK**.

## <a name="view-the-imported-cost-centers"></a>Imporditud kulukeskuste vaatamine
1. Klõpsake dimensiooni **liikmete vaadet**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
