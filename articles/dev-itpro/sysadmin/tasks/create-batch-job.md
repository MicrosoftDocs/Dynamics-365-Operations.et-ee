---
title: Pakktöö loomine
description: Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313355"
---
# <a name="create-a-batch-job"></a>Pakktöö loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks. Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate. Kasutage pakett-töö loomiseks järgmist protseduuri. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-the-batch-job"></a>Pakett-töö loomine
1. Avage Süsteemihaldus > Päringud > Pakett-tööd.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Töö kirjeldus.
4. Sisestage väljale Plaanitud alguskuupäev ja -kellaaeg kuupäev ja kellaaeg.
5. Klõpsake nuppu Salvesta.

## <a name="create-a-recurrence"></a>Korduvuse loomine
1. Klõpsake tegumiribal valikut Pakett-töö.
2. Klõpsake valikut Korduvus.
    * Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.  
3. Klõpsake nuppu OK.

## <a name="add-alerts"></a>Teatiste lisamine
1. Klõpsake tegumiribal valikut Pakett-töö.
2. Klõpsake valikut Teatised.
    * Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse. Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.   
3. Klõpsake nuppu OK.

