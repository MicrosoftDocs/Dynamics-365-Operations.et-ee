---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750590"
---
# <a name="switch-between-vendor-designs"></a>Hankija kujunduste vaheldumisi aktiveerimine

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Hankijaandmete voog 

Kui otsustate kasutada tabelit **Konto** tüübiga **Organisatsioon** hankijate talletamiseks ja tabelit **Kontakt** tüübiga **Isik** hankijate talletamiseks, konfigureerige järgmised töövood. Vastasel juhul ei ole see konfiguratsioon nõutav.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Laiendatud hankija kujunduse kasutamine Organisatsiooni tüübiga hankijate puhul

Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle. Iga malli jaoks luuakse töövoog.

+ Hankijate loomine kontode tabelis
+ Hankijate loomine hankijate tabelis
+ Hankijate värskendamine kontode tabelis
+ Hankijate värskendamine hankijate tabelis

Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.

1. Looge töövooprotsess tabelile **Hankija** ja valige töövooprotsessi mall **Hankijate loomine kontode tabelis**. Seejärel valige **OK**. See töövoog käsitseb tabeli **Konto** hankija loomise stsenaariumi.

    ![Hankijate loomine kontode tabeli töövoo protsessis](media/create_process.png)

2. Looge töövooprotsess tabelile **Hankija** ja valige töövooprotsessi mall **Hankijate värskendamine kontode tabelis**. Seejärel valige **OK**. See töövoog käsitseb tabeli **Konto** hankija värskendamise stsenaariumi.
3. Looge töövooprotsess tabelile **Konto** ja valige töövooprotsessi mall **Hankijate loomine hankijate tabelis**.
4. Looge töövooprotsess tabelile **Konto** ja valige töövooprotsessi mall **Hankijate värskendamine hankijate tabelis**.
5. Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest. Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.

    ![Teisendamine taustatöövoo nupuks](media/background_workflow.png)

6. Aktiveerige töövood, mille lõite tabelitele **Konto** ja **Hankija**, et hakata kasutama tabelit **Konto** tüübiga **Organisatsioon** hankijate teabe salvestamiseks.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Laiendatud hankija kujunduse kasutamine Isiku tüübiga hankijate puhul

Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle. Iga malli jaoks luuakse töövoog.

+ Isiku tüübiga hankijate loomine hankijate tabelis
+ Isiku tüübiga hankijate loomine kontaktide tabelis
+ Isiku tüübiga hankijate värskendamine kontaktide tabelis
+ Isiku tüübiga hankijate värskendamine hankijate tabelis

Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.

1. Looge töövooprotsess tabelile **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate loomine kontaktide tabelis**. Seejärel valige **OK**. See töövoog käsitseb tabeli **Kontakt** hankija loomise stsenaariumi.
2. Looge töövooprotsess tabelile **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate värskendamine kontaktide tabelis**. Seejärel valige **OK**. See töövoog käsitseb tabeli **Kontakt** hankija värskendamise stsenaariumi.
3. Looge töövooprotsess tabelile **Kontakt** ja valige mall **Isiku tüübiga hankijate loomine hankijate tabelis**.
4. Looge töövooprotsess tabelile **Kontakt** ja valige mall **Isiku tüübiga hankijate värskendamine hankijate tabelis**.
5. Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest. Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.
6. Aktiveerige töövood, mille lõite tabelitele **Kontakt** ja **Hankija**, et hakata kasutama tabelit **Kontakt** tüübiga **Isik** hankijate teabe salvestamiseks.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]