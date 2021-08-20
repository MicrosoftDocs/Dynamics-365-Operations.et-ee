---
title: Pakktöö loomine
description: Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.
author: maertenm
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac91c907f4c2cfa03b9750cb3995851e319a3827f42442402f7c02824209b3b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733705"
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]