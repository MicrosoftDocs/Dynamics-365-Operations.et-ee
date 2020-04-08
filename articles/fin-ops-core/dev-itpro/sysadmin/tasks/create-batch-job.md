---
title: Pakktöö loomine
description: Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143669"
---
# <a name="create-a-batch-job"></a>Pakktöö loomine

[!include [banner](../../includes/banner.md)]

Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks. Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate. Kasutage pakett-töö loomiseks järgmist protseduuri. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-the-batch-job"></a>Pakett-töö loomine
1. Avage **Navigatsioonipaan > Moodulid > Süsteemihaldus > Päringud > Pakett-tööd**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Töö kirjeldus**.
4. Sisestage väljale **Plaanitud alguskuupäev/kellaaeg** kuupäev ja kellaaeg.
5. Klõpsake valikut **Salvesta**.

## <a name="create-a-recurrence"></a>Korduvuse loomine
1. Klõpsake tegumiribal valikut **Pakett-töö**.
2. Klõpsake valikul **Korduvus**. Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.  
3. Klõpsake valikut **OK**.

## <a name="add-alerts"></a>Teatiste lisamine
1. Klõpsake tegumiribal valikut **Pakett-töö**.
2. Klõpsake valikut **Teatised**. Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse. Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.   
3. Klõpsake valikut **OK**.

## <a name="adjust-batch-job-status"></a>Pakett-töö oleku reguleerimine
1. Avage **Süsteemihaldus > Päringud > Pakett-tööd**.
2. Valige sobiv pakett-töö.
3. Klõpsake tegumiribal valikut **Pakett-töö > Funktsioonid > Muuda olekut**.
4. Valige asjassepuutuv olek.
    - **Kinnipeetud**: seadke pakett-töö olekuks **kinnipeetud** nii, et see on pakett-töö toiminguajastist kinni peetud. Sama kui *peatus*.
    - **Ootel**: seadistage pakett-töö olekuks **ootel**, et see ootaks pakett-töö ajasti poolt üleskorjamist. Sama kui *mine*.
5. Klõpsake valikut **OK**.
