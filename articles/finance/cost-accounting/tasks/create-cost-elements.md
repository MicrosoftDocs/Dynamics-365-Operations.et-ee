---
title: 'Kuluelementide loomine  '
description: Kuluarvestuses on kuluelementide loomiseks mitu võimalust.
author: kfend
ms.date: 08/29/2018
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
ms.openlocfilehash: 9ca826e54171a3dc3582dc5ceb716ac009d45674
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280716"
---
# <a name="create-cost-elements"></a>Kuluelementide loomine   

[!include [banner](../../includes/banner.md)]

Kuluarvestuses on kuluelementide loomiseks mitu võimalust. See protseduur näitab, kuidas luua kuluelemente, importides põhikontod andmekonnektori kaudu. Selle protseduuri loomiseks kasutati demoettevõtet USMF. See protseduur on kuluarvestuse funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-new-cost-elements"></a>Uute kuluelementide loomine
1. Avage Kuluarvestus > Dimensioonid > Kuluelemendi dimensioonid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Klõpsake nuppu Salvesta.

## <a name="configure-the-data-connector"></a>Andmekonnektori konfigureerimine
1. Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.
2. Sisestage väärtus väljale Kontoplaan või valige see.
    * Jagatud kontoplaani kasutamiseks valige Jagatud.  
3. Klõpsake valikut Uus.
4. Märkige loendis valitud rida.
    * Saate oma kriteeriumide täitmiseks rakendada kontodele filtreid.  
5. Sisestage väärtus väljale Põhikontolt või valige see.
6. Sisestage väärtus väljale Põhikontole või valige see.
7. Klõpsake nuppu OK.

## <a name="import-main-accounts"></a>Impordi põhikontod
1. Klõpsake valikut Dimensiooniliikmete importimine.
    * Põhikontod imporditakse kuluarvestusse ja neid kasutatakse kuluelementidena.  
2. Klõpsake nuppu OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Imporditud kontode vaatamine kuluelementidena
1. Klõpsake valikut Dimensiooniliikmete kuvamine.
    * Kuva imporditud pearaamatukontod kuluelementidena oma ettevõttes, kuhu kuluvoo saab suunata.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
