---
title: Toote konfiguratsioonimudeli koosluse haldamine
description: Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12eb2d8fcdae5d60efa19e5443a01ab9bd104267
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258799"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Toote konfiguratsioonimudeli koosluse haldamine

[!include [banner](../../includes/banner.md)]

Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit. Tipptasemel kõlari mudelit demoettevõttes USMF kasutatakse selle protseduuri loomiseks.


## <a name="add-a-bom-line"></a>Koosluse rea lisamine
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Toote konfiguratsioonimudelid.
3. Otsige loendist ja valige soovitud kirje.
    * Valige selle protseduuri jaoks Tipptasemel kõlar.  
4. Klõpsake loendis valitud real olevat linki.
5. Laiendage jaotist Koosluse read.
6. Klõpsake vahekaarti Lisa.
7. Sisestage väärtus väljale Nimi.
8. Sisestage väljale Kirjeldus soovitud väärtus.
9. Klõpsake nuppu Salvesta.

## <a name="add-bom-line-details"></a>Koosluse rea üksikasjade lisamine
1. Klõpsake valikut Koosluse rea üksikasjad.
2. Sisestage või valige väärtus väljal Kaubakood.
    * Näiteks võite valida kauba M0055.  
    * Iga koosluse rea atribuudi puhul saab valida, kas see võtab endale fikseeritud väärtuse või see vastendatakse atribuudiga.  
3. Märkige ruut Määra.
4. Tehke väljal Arvutus valik Jah.
    * Kui määrate arvutuse atribuudi väärtuseks Jah, lisatakse koosluse rida kuluarvutustesse.  
5. Klõpsake vahekaarti Seadistus.
6. Märkige ruut Määra.
7. Sisestage arv väljale Kogus.
    * Koguse väli määrab, kui palju kaupa kooslusse lisatakse. See võib olla ilmne atribuudi vastendamise kandidaat.  
8. Klõpsake vahekaarti Dimensioon.
    * Kontrollige, kas mõni tootedimensioon on aktiivne ja seetõttu peab sellele olema määratud väärtus või atribuut.  
9. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]