---
title: Retaili tootekategooriate ja toodete haldamine
description: Selles teemas kirjeldatakse, kuidas tootejuhid saavad kasutada Retaili tootekategooriaid Retaili tootehierarhia ja väljastatud toote üksikasjade vaheliste seoste haldamiseks.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344681"
---
# <a name="manage-retail-product-categories-and-products"></a>Retaili tootekategooriate ja toodete haldamine

[!include [banner](./includes/banner.md)]

Selles teemas kirjeldatakse täiustatud viisi jaemüügi tootekategooriate ja toodete haldamiseks rakendusesMicrosoft Dynamics 365 for Retail. Täiustused võimaldavad tootejuhtidel vaadata tooteatribuutide üldist struktuuri Retaili tootehierarhia ja väljastatud toote üksikasjade vahel.

Lisateavet Retaili tootekategooriate haldamise kohta vaadake tööruumi **Kategooria ja toote haldus** tööruumi paanilt **Retaili tootehierarhia**.

Pange tähele kuvatava lehe **Retaili tootehierarhia** täiustatud struktuuri. Retaili varasemates versioonides olid toote atribuudid jagatud kohaldatava ulatuse alusel *toote põhiatribuutideks* ja *Retaili tooteatribuutideks*. Retaili tooteatribuudid on kohaldatava ulatuse järgi *globaalsed*. Teisisõnu: antud Retaili tooteatribuudi puhul jagatakse sama väärtust kõigi juriidiliste isikute lõikes. See-eest toote põhiatribuudid on *juriidilise isiku põhised*. Teisisõnu: antud toote põhiatribuudi korral võib väärtus juriidiliste isikute lõikes erineda, olenevalt iga juriidilise isiku ärivajadustest.

Retaili tootekategooria täiustatud struktuuris on tooteatribuudid loogiliselt eraldatud nende kohalduvuse alusel grupis, peegeldades väljastatud toote üksikasjade vormi struktuuri.

![Väljade grupeerimine atribuutide kohaldatavuse ulatuse põhjal](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul.

Atribuutide haldamiseks kõigi juriidiliste isikute lõikes valige **Kuva kõigi juriidiliste isikute puhul** (või **Redigeeri kõigi juriidiliste isikute puhul**).

![Kuvamine/redigeerimine kõigi juriidiliste isikute puhul](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Konkreetse juriidilise isiku atribuutide haldamiseks valige **Kuva konkreetse juriidilise isiku puhul** (või **Redigeeri konkreetse juriidilise isiku puhul**).

![Kuvamine/redigeerimine konkreetse juriidilise isiku puhul](media/ToggleToEditForAllLegalEntities.PNG)

Lisaks saab tootejuht täiustatud Retaili tootekategooria struktuuris määrata nüüd vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil. Seejärel pärivad tooted loomise ajal need tooteatribuudi vaikeväärtused, põhinedes nende atribuutide seosel individuaalse kategooriaga Retaili tootehierarhiast. Neid päritud tooteatribuute saab ka iga toote puhul muuta, et need oleksid konkreetse äri vajadustega kooskõlas.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Atribuutide valimine toodete värskendamiseks Retaili hierarhia lehelt

Saate uut tooteatribuutide täiustatud struktuuri kasutada selleks, et valida, millised värskendatud tooteatribuudid tuleb seotud toodetele tõugata. Valige lehe **Retaili tootehierarhia** tegumiribalt **Kategooria** ja seejärel dialoogiboksi **Värskenda tooteid** avamiseks **Värskenda tooteid**.

![Dialoogiboks Värskenda tooteid](media/NewUpdateProductsEnhancedView.PNG)
