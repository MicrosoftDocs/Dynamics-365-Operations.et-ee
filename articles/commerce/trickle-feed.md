---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Commerce'is.
author: analpert
ms.date: 01/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67b66cd4bf2a77f3ab7f33f691156e38cc13770a
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964625"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks

[!include [banner](includes/banner.md)]

Versioonis Microsoft Dynamics 365 Commerce 10.0.5 ja uuemas on soovitatav viia kõik väljavõtte sisestamisprotsessid üle vähehaaval toimuvale väljavõtte sisestusprotsessile. Vähehaaval toimuva funktsiooni kasutamisega on seotud olulised jõudluse ja ärieelised. Müügikandeid töödeldakse kogu päeva jooksul. Makse- ja sularahahalduse kandeid töödeldakse finantsaruandes päeva lõpus. Vähehaaval toimuv funktsioon võimaldab müügitellimuste, arvete ja maksete pidevat töötlemist. Seetõttu uuendatakse ja tuvastatakse varusid, tulu ja makseid peaaegu reaalajas.

## <a name="use-trickle-feed-based-posting"></a>Vähehaaval toimuva sisestamise kasutamine

> [!IMPORTANT]
> Enne vähehaaval toimuva sisestamise lubamist peate kontrollima, et ei oleks arvutatud ja sisestamata väljavõtteid. Enne funktsiooni lubamist sisestage kõik väljavõtted. Avatud väljavõtteid saate kontrollida tööruumis **Kaupluse finantsandmed**.

Jaemüügikannete vähehaaval toimuva sisestamise lubamiseks lubage tööruumis **Funktsooonihaldus** funktsioon **Retaili väljavõtted – vähehaaval toimuv**. Väljavõtted tükeldatakse kaheks tüübiks: kandeväljavõtted ja finantsaruanded.

### <a name="transactional-statements"></a>Kandeväljavõtted

Kandeväljavõtete töötlemise eesmärk on nende käitamine suurel sagedusel kogu päeva jooksul, et dokumendid loodaks siis, kui kanded laaditakse Commerce’i peakontorisse. Kanded laaditakse kauplustest Commerce'i peakontorisse **P-töö** käivitamisel. Peate käitama ka töö **Kinnita kaupluse kanded**, et kandeid kinnitatakse nii, et kandeväljavõte saab need kätte.

Ajastage järgmised tööd suure sagedusega käivituma.

- Kandeväljavõtte arvutamiseks käivitage töö **Kandeväljavõtete arvutamine partiina** (**Retail ja Commerce \> Retaili ja Commerce'i IT \> Kassa sisestamine \> Kandeväljavõtete arvutamine partiina**). See töö saab kätte kõik sisestamata ja kinnitatud kanded ning lisab need uuele kandeväljavõttele.
- Kandeväljavõtte sisestamiseks partiina käivitage töö **Kandeväljavõtete sisestamine partiina** (**Retail ja Commerce \> Retaili ja Commerce'i IT \> Kassa sisestamine \> Kandeväljavõtete sisestamine partiina**). See töö käivitab tõrkeid mittesisaldavate sisestamata väljavõtete sisestamisprotsessi ja loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded. 

### <a name="financial-statements"></a>Finantsaruanded

Finantsaruande töötlemine on mõeldud päeva lõpetamise protsessina. Seda tüüpi väljavõtte töötlemine toetab ainult **Vahetuse** sulgemismeetodit ja tuvastab ainult suletud vahetused. Väljavõtted on piiratud finantstehingute vastavusseviimisega. Need loovad töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks maksete ja töölehtede jaoks muude sularahahalduse kannete puhul.

Finantsaruanded võimaldavad ka järgmiste kannete ülevaatamist: päevakassa kanded, maksete kanded, panka hoiustatud maksevahendi kanded ja seifi hoiustatud maksevahendi kanded. Maksevahendi üksikasjade leht on nähtav ainult siis, kui on valitud finantsaruanne.

![Pilt, kus kuvatakse sisestatud väljavõtete vormi maksevahendi üksikasjade jaotis ainult siis, kui on valitud finantsaruanne.](./media/Trickle-feed-posted-statements-transaction-view.png)

Ajastage järgmiste finantsaruande tööde algus- ja lõppajad päeva eeldatava lõpu alusel.

- Finantsaruande arvutamiseks käivitage töö **Finantsaruannete arvutamine partiina** (**Retail ja Commerce \> Retaili ja Commerce'i IT \> Kassa sisestamine \>Finantsaruannete arvutamine partiina**). See töö kogub kõik sisestamata finantskanded ja lisab need uude finantsaruandesse.
- Finantsaruannete sisestamiseks partiina käivitage töö **Finantsaruannete sisestamine partiina** (**Retail ja Commerce \> Retaili ja Commerce'i IT \> Kassa sisestamine \>Finantsaruannete sisestamine partiina**).

### <a name="manually-create-statements"></a>Väljavõtete käsitsi loomine

Kandeväljavõtte ja finantsaruande tüüpe saab luua ka käsitsi. 

1. Avage **Retail ja Commerce \> Kanalid \> Kauplused** ja klõpsake valikut **Väljavõtted**. 
2. Valige **Uus** ja seejärel valige loodav väljavõtte tüüp. Lehel **Väljavõtted** kuvatakse valitud väljavõtte tüübi kohta asjakohased andmed ja jaotises **Väljavõttegrupp** olevad tegevused kuvavad asjakohased tegevused.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
