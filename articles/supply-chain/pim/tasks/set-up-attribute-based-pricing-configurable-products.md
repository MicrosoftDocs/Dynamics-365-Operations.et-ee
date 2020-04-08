---
title: Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele
description: Selles teemas selgitatakse, kuidas seadistada atribuutidepõhist hinnastamist.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d23030b79670e31cc237b9ca53b0b3881678786f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149822"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada atribuutidepõhist hinnastamist. Eeltingimusena peab teil olema tootekonfiguratsiooni mudel, millel on vähemalt üks komponent ja atribuut. Selles näites kasutatakse demoettevõtte USMF tipptasemel kõlari tootemudelit. Tavaliselt kasutab seda protseduuri tootejuht.


## <a name="create-a-new-price-model"></a>Uue hinnamudeli loomine
1. Valige avalehel **Tootevariandi mudeli määratlus**.
2. Valige **Toote konfiguratsioonimudelid** jaotisest **lingid**.
3. Valige loendist rida **Kvaliteetkõlar**, aga ärge valige linki nimele.
4. Valige toiminguplaanil **Mudel**.
5. Valige **Hinnamudelid**.
6. Valige suvand **Uus**.
7. Sisestage väärtus väljale **Hinnamudeli nimi**. Kasutage nime, mille abil on mudelit kerge tuvastada.  
8. Sisestage väärtus väljale **Kirjeldus**.
9. Valige käsk **Salvesta**.

## <a name="add-price-elements"></a>Hinnaelementide lisamine
1. Valige suvand **Redigeeri**. Igal tootemudeli komponendil võib olla baashinna element ja mis tahes arv hinnaavaldise reegleid. Saate lisada hindu ka erinevates valuutades.  
2. Sisestage väärtus väljale **Baashinna väljend**. Tippige näiteks 100. Baashinna avaldis võib olla arvväärtus või koosneda aritmeetilisest tehtest, mis sisaldab vähemalt ühte atribuuti.  
3. Valige **Lisa**.
4. Väljale **Nimi** sisestage `Rosewood`. Hinnaavaldise nimi aitab tuvastada, mida hinnaelement tähistab. Selles näites loome hinnaelemendi Rosewoodi kõlari korpuse viimistluse valikule.  
5. Valige **Tingimuse redigeerimine**. Hinnatingimus aitab tagada hinnaavaldise elemendi lisamise müügihinda ainult juhul, kui on olemas konkreetne atribuutide kombinatsioon.  
6. Sisestage **ConstraintBody** väljale `CabinetFinish=="Rosewood"`.
7. Valige nupp **OK**.
8. Sisestage väärtus väljale **Avaldis**. Sisestage näiteks `50`. 
9. Sulgege leht.

