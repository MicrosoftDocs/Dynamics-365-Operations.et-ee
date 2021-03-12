---
title: Tootekategooriate ja toodete haldamine
description: Selles teemas kirjeldatakse, kuidas tootejuhid saavad kasutada tootekategooriaid Commerce'i tootehierarhia ja väljastatud toote üksikasjade vaheliste seoste haldamiseks.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cee79d6937afeec1e607abde49d52790c51e98a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001070"
---
# <a name="manage-product-categories-and-products"></a>Tootekategooriate ja toodete haldamine

[!include [banner](./includes/banner.md)]

Selles teemas kirjeldatakse täiustatud viisi tootekategooriate ja toodete haldamiseks rakenduses Dynamics 365 Commerce. Täiustused võimaldavad tootejuhtidel vaadata tooteatribuutide üldist struktuuri tootehierarhia ja väljastatud toote üksikasjade vahel.

Lisateavet tootekategooriate haldamise kohta vaadake tööruumi **Kategooria ja toote haldus** tööruumi paanilt **Commerce'i tootehierarhia**.

Pange tähele kuvatava lehe **Commerce'i tootehierarhia** täiustatud struktuuri. Rakenduse varasemates versioonides olid toote atribuudid jagatud kohaldatava ulatuse alusel *toote põhiatribuutideks* ja *Retaili tooteatribuutideks*. Retaili tooteatribuudid on kohaldatava ulatuse järgi *globaalsed*. Teisisõnu: antud tooteatribuudi puhul jagatakse sama väärtust kõigi juriidiliste isikute lõikes. See-eest toote põhiatribuudid on *juriidilise isiku põhised*. Teisisõnu: antud toote põhiatribuudi korral võib väärtus juriidiliste isikute lõikes erineda, olenevalt iga juriidilise isiku ärivajadustest.

Tootekategooria täiustatud struktuuris on tooteatribuudid loogiliselt eraldatud nende kohalduvuse alusel grupis, peegeldades väljastatud toote üksikasjade vormi struktuuri.

![Väljade grupeerimine atribuutide kohaldatavuse ulatuse põhjal](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul.

Atribuutide haldamiseks kõigi juriidiliste isikute lõikes valige **Kuva kõigi juriidiliste isikute puhul** (või **Redigeeri kõigi juriidiliste isikute puhul**).

![Kuvamine/redigeerimine kõigi juriidiliste isikute puhul](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Konkreetse juriidilise isiku atribuutide haldamiseks valige **Kuva konkreetse juriidilise isiku puhul** (või **Redigeeri konkreetse juriidilise isiku puhul**).

![Kuvamine/redigeerimine konkreetse juriidilise isiku puhul](media/ToggleToEditForAllLegalEntities.PNG)

Lisaks saab tootejuht täiustatud tootekategooria struktuuris määrata nüüd vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil. Seejärel pärivad tooted loomise ajal need tooteatribuudi vaikeväärtused, põhinedes nende atribuutide seosel individuaalse kategooriaga tootehierarhiast. Neid päritud tooteatribuute saab ka iga toote puhul muuta, et need oleksid konkreetse äri vajadustega kooskõlas.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Atribuutide valimine toodete värskendamiseks Commerce'i tootehierarhia lehelt

Saate uut tooteatribuutide täiustatud struktuuri kasutada selleks, et valida, millised värskendatud tooteatribuudid tuleb seotud toodetele tõugata. Valige lehe **Commerce'i tootehierarhia** tegumiribalt **Kategooria** ja seejärel dialoogiboksi **Värskenda tooteid** avamiseks **Värskenda tooteid**.

![Dialoogiboks Värskenda tooteid](media/NewUpdateProductsEnhancedView.PNG)
