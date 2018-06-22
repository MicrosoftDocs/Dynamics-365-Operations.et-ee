---
title: "Asukoha ja osapoole seosetüüpide lisamine"
description: "Selles teemas kirjeldatakse uue asukoha ja osapoole seosetüübi loomist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: bd8c5a18d69e1952d32675d759b8b2a997844822
ms.contentlocale: et-ee
ms.lasthandoff: 05/21/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a>Uute asukoharollide ja osapoole seosetüüpide lisamine 

## <a name="add-new-location-roles"></a>Uute asukoharollide lisamine

Aadressile ja kontaktteabele uute asukoharollide lisamiseks on kaks võimalust.

-  Lisamine lehelt **Aadressi ja kontaktteabe eesmärk**. Uus roll salvestatakse tabelisse **LogisticsLocationRole** tüübiga 0, mis näitab, et roll pole loetelus **LogisticsLocationRoleType** määratletud süsteemiroll. Kasutaja saab seda rolli kasutada aadressi või kontaktteabe loomisel.

    ![Aadressi ja kontaktteabe eesmärk](media/Address-Contact.PNG)

-  Saate lisada selle loetelu **LogisticsLocationRoleType** laiendisse ja lasta selle asustada andmebaasi sünkroonimisprotsessi kaudu.

    1.  Looge loetelule **LogisticsLocationRoleType** laiend ja lisage laiendis uus roll. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Saate luua uuele rollile uue ressursifaili ja seejärel määrata selle atribuutidele väärtuse.
     
     ![Uus ressursifail](media/Resource.PNG)
        
    3.  Saate luua andmete asustamise klassi ja esitada ohjemeetodi uue rolli asustamiseks. 

        ![Andmete asustamine](media/Dirdata.PNG)

    4.  Uue asukoharolli testasustamiseks saate luua käitatava klassi ja kutsuda DirDataPopulation::insertLogisticsLocationRoles() asukohas Main(). Kui see protsess on lõpule jõudnud, peaksite nägema uut rolli tabelis **LogisticsLocationRole** tüübiga \> 0. Uus roll kuvatakse lehel **Aadressi ja kontaktteabe eesmärk**.

        ![Uue asukoha sisestamine](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a>Uute osapoole seosetüüpide lisamine 

Uue seosetüübi lisamiseks on kaks võimalust.

-   Lisamine lehe **Seosetüübid** kaudu. Uus seos salvestatakse tabelisse **DirRelationshipTypeTable**, systemtype = 0.

    ![Seosetüübid](media/Relationship.PNG)

-  Saate lisada selle loetelu **DirSystemRelationshipType** laiendisse ja lasta selle asustada andmebaasi sünkroonimisprotsessi kaudu.

    1.  Looge loetelule **DirSystemRelationshipType** laiend ja lisage uus seosetüüp.

    2. Looge uuele tüübile lähtestaja. Mitu näidet leiate põhikoodist, üks neist on **DirRelationshipTypeChildInitialize**. See on osapoole seosetüübi Tütar lähtestajaklass. Saate alustada oma lähtestajaga, kopeerides ja kleepides selle koodi ning seejärel värskendades esiletõstetud alasid.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Uue seosetüübi testasustamiseks saate luua käitatava klassi ja kutsuda DirDataPopulation::insertDirRelationshipTypes() asukohas Main(). Peaksite uut seosetüüpi nägema tabelis **DirRelationshipTypeTable** ja uus seosetüüp on saadaval lehel **Seosetüübid**.

        ![Käitatav klass](media/Runnable.PNG)

