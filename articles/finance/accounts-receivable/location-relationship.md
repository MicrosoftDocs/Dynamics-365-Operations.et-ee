---
title: Asukoha ja osapoole seosetüüpide lisamine
description: See artikkel selgitab, kuidas lisada uut asukohta ja osapoole seose tüüpi.
author: ShivamPandey-msft
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2aaf16fac658d26dc2d2a389fd5c1dbb9cbb7649
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874750"
---
# <a name="add-location-and-party-relationship-types"></a>Asukoha ja osapoole seosetüüpide lisamine 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Asukoharollide lisamine

Aadressile ja kontaktteabele uute asukoharollide lisamiseks on kaks võimalust.

-  Lisamine lehelt **Aadressi ja kontaktteabe eesmärk**. Uus roll salvestatakse tabelisse **LogisticsLocationRole** tüübiga 0, mis näitab, et roll pole loetelus **LogisticsLocationRoleType** määratletud süsteemiroll. Kasutaja saab seda rolli kasutada aadressi või kontaktteabe loomisel.

    ![Aadressi ja kontaktteabe eesmärk.](media/Address-Contact.PNG)

-  Saate lisada selle loetelu **LogisticsLocationRoleType** laiendisse ja lasta selle asustada andmebaasi sünkroonimisprotsessi kaudu.

    1.  Looge loetelule **LogisticsLocationRoleType** laiend ja lisage laiendis uus roll. 
  
        ![Loetelu LogisticsLocationRoleType laiend.](media/Logistics.PNG)

    2. Saate luua uuele rollile uue ressursifaili ja seejärel määrata selle atribuutidele väärtuse.
     
     ![Uus ressursifail.](media/Resource.PNG)
        
    3.  Saate luua andmete asustamise klassi ja esitada ohjemeetodi uue rolli asustamiseks. 

        ![Andmete asustamine.](media/Dirdata.PNG)

    4.  Uue asukoharolli katseasustamiseks saate luua käitatava klassi ja kutsuda atribuudi DirDataPopulation::insertLogisticsLocationRoles() asukohas Main(). Kui see protsess on lõpule jõudnud, peaksite nägema uut rolli tabelis **LogisticsLocationRole** tüübiga \> 0. Uus roll kuvatakse lehel **Aadressi ja kontaktteabe eesmärk**.

        ![Uue asukoha sisestamine.](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Osapoole seosetüüpide lisamine 

Uue seosetüübi lisamiseks on kaks võimalust.

-   Lisamine lehe **Seosetüübid** kaudu. Uus seos salvestatakse tabelisse **DirRelationshipTypeTable**, systemtype = 0.

    ![Seosetüübid.](media/Relationship.PNG)

-  Saate lisada selle loetelu **DirSystemRelationshipType** laiendisse ja lasta selle asustada andmebaasi sünkroonimisprotsessi kaudu.

    1.  Looge loetelule **DirSystemRelationshipType** laiend ja lisage uus seosetüüp.

    2. Looge uuele tüübile lähtestaja. Mitu näidet leiate põhikoodist, üks neist on **DirRelationshipTypeChildInitialize**. See on osapoole seosetüübi Tütar lähtestajaklass. Saate alustada oma lähtestajaga, kopeerides ja kleepides selle koodi ning seejärel värskendades esiletõstetud alasid.
    
    ![DirRelationshipChild lähtestaja.](media/DirRelationship.PNG)

    3.  Uue seosetüübi katseasustamiseks saate luua käitatava klassi ja kutsuda atribuudi DirDataPopulation::insertDirRelationshipTypes() asukohas Main(). Peaksite uut seosetüüpi nägema tabelis **DirRelationshipTypeTable** ja uus seosetüüp on saadaval lehel **Seosetüübid**.

        ![Käitatav klass.](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
