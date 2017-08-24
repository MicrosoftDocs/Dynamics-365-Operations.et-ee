--- 
title: "Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele"
description: "See protseduur näitab, kuidas seadistada atribuudipõhist hinnakujundust."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada atribuudipõhist hinnakujundust. Eeltingimusena peab teil olema tootekonfiguratsiooni mudel, millel on vähemalt üks komponent ja atribuut. Selles näites kasutatakse demoettevõtte USMF tipptasemel kõlari tootemudelit. Tavaliselt kasutab seda protseduuri tootejuht.


## <a name="create-a-new-price-model"></a>Uue hinnamudeli loomine
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Toote konfiguratsioonimudelid.
3. Valige loendist tipptasemel kõlari rida, kuid ärge klõpsake nime linki.
4. Klõpsake tegumiribal valikut Mudel.
5. Klõpsake valikut Hinnamudelid.
6. Klõpsake valikut Uus.
7. Tippige väärtus väljale Hinnamudeli nimi.
    * Kasutage nime, mille abil on mudelit kerge tuvastada.  
8. Sisestage väljale Kirjeldus soovitud väärtus.
9. Klõpsake nuppu Salvesta.

## <a name="add-price-elements"></a>Hinnaelementide lisamine
1. Klõpsake nuppu Redigeeri.
    * Igal tootemudeli komponendil võib olla baashinna element ja mis tahes arv hinnaavaldise reegleid. Saate lisada hindu ka erinevates valuutades.  
2. Tippige väärtus väljale Baashinna avaldis.
    * Tippige näiteks 100.   Baashinna avaldis võib olla arvväärtus või koosneda aritmeetilisest tehtest, mis sisaldab vähemalt ühte atribuuti.  
3. Klõpsake vahekaarti Lisa.
4. Tippige Rosewood väljale Nimi.
    * Hinnaavaldise nimi aitab tuvastada, mida hinnaelement tähistab. Selles näites loome hinnaelemendi Rosewoodi kõlari korpuse viimistluse valikule.  
5. Klõpsake nuppu Muuda tingimust.
    * Hinnatingimus aitab tagada hinnaavaldise elemendi lisamise müügihinda ainult juhul, kui on olemas konkreetne atribuutide kombinatsioon.  
6. Sisestage väljale ConstraintBody tekst CabinetFinish=="Rosewood".
7. Klõpsake nuppu OK.
8. Tippige väärtus väljale Avaldis.
    * Tippige näiteks 50.  
9. Sulgege leht.
10. Sulgege leht.


