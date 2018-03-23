---
title: Tootekategooria haldus
description: "Selles teemas kirjeldatakse, kuidas tootejuhid saavad kasutada jaemüügi tootekategooriaid jaemüügi tootehierarhia ja väljastatud toote üksikasjade vaheliste seoste haldamiseks."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: et-ee
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Täiustatud toote ja kategooria haldus

[!include[banner](./includes/banner.md)]

Selles teemas kirjeldatakse täiustatud viisi jaemüügi tootekategooriate ja toodete haldamiseks rakenduses Dynamics 365 for Retail. Need täiustused võimaldavad tootejuhtidel vaadata tooteatribuutide üldist struktuuri jaemüügi tootehierarhia ja väljastatud toote üksikasjade vahel.

Lisateabe saamiseks jaemüügi tootekategooriate haldamise kohta valige tööruumis **Kategooria ja toote haldus** suvand **Jaemüügi tootehierarhia** ja vaadake lehe **Jaemüügi tootekategooria** täiustatud struktuuri.

![Kategooria ja toote halduse tööruum](media/LaunchRetailProductHierarchy.png)

Varasemates versioonides olid toote atribuudid jagatud kohaldatava ulatuse alusel **toote põhiatribuutideks** ja **jaetoote atribuutideks**. **Jaetoote atribuudid** olid kohaldatava ulatuse järgi *globaalsed*, mis tähendab, et antud **jaetoote atribuudi** korral on sama väärtus ühiskasutuses kõigi juriidiliste isikute korral. **Toote põhiatribuudid** on *juriidilise isiku põhised*. Teisisõnu: antud **toote põhiatribuudi** korral võib väärtus juriidiliste isikute lõikes erineda, tuginedes eraldi ettevõtete nõuetele.

Jaemüügi tootekategooria täiustatud struktuuris on tooteatribuudid loogiliselt eraldatud nende kohalduvuse alusel grupis, peegeldades väljastatud toote üksikasjade vormi struktuuri.

![Väljade grupeerimine nende kohaldatavuse ulatuse põhjal](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul. Valige kas **Kuva/redigeeri kõigi juriidiliste isikute puhul** või **Kuva/redigeeri konkreetse juriidilise isiku puhul**.

![Individuaalse ja kõigi juriidiliste isikute vaate vahel valimine](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Individuaalse ja kõigi juriidiliste isikute vaate vahel valimine](media/ToggleToEditForAllLegalEntities.PNG)  

Eelmiste versioonidega võrreldes saab tootejuht uues jaemüügi tootekategooria struktuuris määrata ka vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil. Toote loomise ajal pärib toode need tooteatribuudi vaikeväärtused, põhinedes nende seosel individuaalse kategooriaga jaemüügi tootehierarhiast. Neid päritud tooteatribuute saab ka iga toote puhul muuta, et need vastaksid konkreetsetele ärinõuetele.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Valige atribuudid toodete värskendamiseks jaetoote kategooria vormilt 
 
Saate seda uut tooteatribuutide täiustatud struktuuri kasutada selleks, et valida, millised värskendatud tooteatribuudid tuleb seotud toodetele tõugata. 

![Toodete värskendamise uus täiustatud vaade](media/NewUpdateProductsEnhancedView.PNG) 

Tootejuhid saavad neid tuletatud tooteatribuute iga toote puhul muuta, et need vastaksid konkreetsetele ärinõuetele.


