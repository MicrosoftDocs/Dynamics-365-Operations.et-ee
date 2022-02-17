---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas vahetada hankija andmete integreerimist Finance and Operationsi rakenduste ja rakenduse vahel Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 80de21b5e46e4f274626fa311f16e81312a2f5ab
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062746"
---
# <a name="switch-between-vendor-designs"></a>Hankija kujunduste vaheldumisi aktiveerimine

[!include [banner](../../includes/banner.md)]





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

    ![Hankijate loomine kontode tabeli töövoo protsessis.](media/create_process.png)

2. Looge töövooprotsess tabelile **Hankija** ja valige töövooprotsessi mall **Hankijate värskendamine kontode tabelis**. Seejärel valige **OK**. See töövoog käsitseb tabeli **Konto** hankija värskendamise stsenaariumi.
3. Looge töövooprotsess tabelile **Konto** ja valige töövooprotsessi mall **Hankijate loomine hankijate tabelis**.
4. Looge töövooprotsess tabelile **Konto** ja valige töövooprotsessi mall **Hankijate värskendamine hankijate tabelis**.
5. Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest. Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.

    ![Teisendamine taustatöövoo nupuks.](media/background_workflow.png)

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