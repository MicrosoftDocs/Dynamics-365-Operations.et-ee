---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997548"
---
# <a name="switch-between-vendor-designs"></a>Hankija kujunduste vaheldumisi aktiveerimine

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Hankijaandmete voog 

Kui otsustate kasutada üksust **Konto** tüübiga **Organisatsioon** hankijate talletamiseks ja üksust **Kontakt** tüübiga **Isik** hankijate talletamiseks, konfigureerige järgmised töövood. Vastasel juhul ei ole see konfiguratsioon nõutav.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Laiendatud hankija kujunduse kasutamine Organisatsiooni tüübiga hankijate puhul

Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle. Iga malli jaoks luuakse töövoog.

+ Hankijate loomine kontode üksuses
+ Hankijate loomine hankijate üksuses
+ Hankijate värskendamine kontode üksuses
+ Hankijate värskendamine hankijate üksuses

Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.

1. Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Hankijate loomine kontode üksuses**. Seejärel valige **OK**. See töövoog käsitseb üksuse **Konto** hankija loomise stsenaariumi.

    ![Hankijate loomine kontode üksuse töövoo protsessis](media/create_process.png)

2. Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Hankijate värskendamine kontode üksuses**. Seejärel valige **OK**. See töövoog käsitseb üksuse **Konto** hankija värskendamise stsenaariumi.
3. Looge töövooprotsess üksusele **Konto** ja valige töövooprotsessi mall **Hankijate loomine hankijate üksuses**.
4. Looge töövooprotsess üksusele **Konto** ja valige töövooprotsessi mall **Hankijate värskendamine hankijate üksuses**.
5. Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest. Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.

    ![Teisendamine taustatöövoo nupuks](media/background_workflow.png)

6. Aktiveerige töövood, mille lõite üksustele **Konto** ja **Hankija** , et hakata kasutama üksust **Konto** tüübiga **Organisatsioon** hankijate teabe salvestamiseks.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Laiendatud hankija kujunduse kasutamine Isiku tüübiga hankijate puhul

Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle. Iga malli jaoks luuakse töövoog.

+ Isiku tüübiga hankijate loomine hankijate olemis
+ Isiku tüübiga hankijate loomine kontaktide olemis
+ Isiku tüübiga hankijate värskendamine kontaktide olemis
+ Isiku tüübiga hankijate värskendamine hankijate olemis

Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.

1. Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate loomine kontode üksuses**. Seejärel valige **OK**. See töövoog käsitseb üksuse **Kontakt** hankija loomise stsenaariumi.
2. Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate värskendamine kontode üksuses**. Seejärel valige **OK**. See töövoog käsitseb üksuse **Kontakt** hankija värskendamise stsenaariumi.
3. Looge töövooprotsess üksusele **Kontakt** ja valige mall **Isiku tüübiga hankijate loomine hankijate üksuses**.
4. Looge töövooprotsess üksusele **Kontakt** ja valige mall **Isiku tüübiga hankijate värskendamine hankijate üksuses**.
5. Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest. Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.
6. Aktiveerige töövood, mille lõite üksustele **Kontakt** ja **Hankija** , et hakata kasutama üksust **Kontakt** tüübiga **Isik** hankijate teabe salvestamiseks.
