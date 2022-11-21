---
title: 'Kuluelementide loomine  '
description: Kuluarvestuses on kuluelementide loomiseks mitu võimalust.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779685"
---
# <a name="create-cost-elements"></a>Kuluelementide loomine   

[!include [banner](../../includes/banner.md)]

Kuluarvestuses on kuluelementide loomiseks mitu võimalust. See protseduur näitab, kuidas luua kuluelemente, importides põhikontod andmekonnektori kaudu. Selle protseduuri loomiseks kasutati demoettevõtet USMF. See protseduur on kuluarvestuse funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-new-cost-elements"></a>Uute kuluelementide loomine
1. Kuluelemendi **dimensioonide > avage > Kuluelemendi dimensioonid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Nimi**.
4. Sisestage **või valige väärtus väljal Andmeühendus** dimensiooni liikmete jaoks.
5. Sisestage väärtus väljale **Kirjeldus**.
6. Klõpsake nuppu **Salvesta**.

## <a name="configure-the-data-connector"></a>Andmekonnektori konfigureerimine
1. Klõpsake käsku **Konfigureeri dimensiooni liikme pakkujat**.
2. Sisestage **või valige väärtus** väljal Kontoplaan.
    * Valige **ühiskasutuses** kontoplaani kasutamiseks jagatud kontoplaan.  
3. Klõpsake valikut **Uus**.
4. Märkige loendis valitud rida.
    * Saate oma kriteeriumide täitmiseks rakendada kontodele filtreid.  
5. Sisestage **või valige väärtus** väljal Põhikontost.
6. Sisestage **või valige väärtus** väljal Põhikontole.
7. Klõpsake valikut **OK**.

## <a name="import-main-accounts"></a>Impordi põhikontod
1. Klõpsake käsku **Impordi dimensiooni liikmed**.
    * Põhikontod imporditakse kuluarvestusse ja neid kasutatakse kuluelementidena.  
2. Klõpsake valikut **OK**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Imporditud kontode vaatamine kuluelementidena
1. Klõpsake dimensiooni **liikmete vaadet**.
    * Kuva imporditud pearaamatukontod kuluelementidena oma ettevõttes, kuhu kuluvoo saab suunata.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
