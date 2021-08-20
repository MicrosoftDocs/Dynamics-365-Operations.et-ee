---
title: Toote konfiguratsioonimudeli koosluse haldamine
description: Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 173022d40a5c1354cbe05c171a8921e733d908d065b10889f9cbe0e87f3e98fa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781461"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Toote konfiguratsioonimudeli koosluse haldamine

[!include [banner](../../includes/banner.md)]

Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit. Tipptasemel kõlari mudelit demoettevõttes USMF kasutatakse selle protseduuri loomiseks.

## <a name="add-a-bom-line"></a>Koosluse rea lisamine

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Otsige loendist ja valige soovitud kirje.
    * Valige selle protseduuri jaoks Tipptasemel kõlar.  
1. Valige loendis link valitud reas.
1. Laiendage jaotist **Koosluse read**.
1. Valige **Lisa**.
1. Sisestage väärtus väljale **Nimi**.
1. Sisestage väärtus väljale **Kirjeldus**.
1. Valige käsk **Salvesta**.

## <a name="add-bom-line-details"></a>Koosluse rea üksikasjade lisamine

1. Valige **koosluse rea üksikasjad**.
2. Sisestage või valige väärtus väljale **Kauba kood**.
    * Näiteks võite valida kauba M0055.  
    * Iga koosluse rea atribuudi puhul saab valida, kas see võtab endale fikseeritud väärtuse või see vastendatakse atribuudiga.  
3. Märkige ruut **Määra**.
4. Valige suvand *Jah* väljal **Kalkulatsioon**.
    * Kui määrate atribuudi **Arvutus** väärtuseks *Jah*, lisatakse koosluse rida kuluarvutustesse.  
5. Valige vahekaart **Häälestus**.
6. Märkige ruut **Määra**.
7. Sisestage arv väljale **Kogus**.
    * Koguse väli määrab, kui palju kaupa kooslusse lisatakse. See võib olla ilmne atribuudi vastendamise kandidaat.  
8. Valige vahekaart **Mõõtmed**.
    * Kontrollige, kas mõni tootedimensioon on aktiivne ja seetõttu peab sellele olema määratud väärtus või atribuut.  
9. Valige nupp **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]