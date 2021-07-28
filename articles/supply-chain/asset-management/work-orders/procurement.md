---
title: Hange
description: Selles teemas selgitatakse hanget varahalduses.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f3e01dd85cbe8e2b2c9095431f3e0aead817a5a5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352758"
---
# <a name="procurement"></a>Hange

[!include [banner](../../includes/banner.md)]

Varahalduses saate ülevaate ostutaotlustega ja ostutellimustega seotud töökäskude kohta. Samuti on võimalik luua ostutellimus või ostutaotlus töökäsust.

Loendis **Töökäsu ostutaotlus** (**Varahaldus** > **Tavaline** > **Hange** > **Töökäsu ostutaotlus**) on kuvatud töökäskudega seotud ostutaotlused. Kui valite sellelt lehelt töökäsu töö, saate kasutada toimingupaani vahekaardi **Töökäsu ostutaotlus** grupi **Kuva** nuppe, et sooritada mitmesuguseid toiminguid:

- Seotud ostutaotluse avamiseks valige **Ostutaotlus**. 
- Seotud töökäsu avamiseks valige **Töökäsk**.
- Et saada ülevaadet sellest, kus varahalduses valitud real olevat kaupa kasutatakse, valige varade, hooldustöö tüübi vaikesätete, varuosade ja töökäskude puhul väärtus **Üksus, kus kasutatud**. Lisateavet selle ülevaate kohta vt teemast [Üksus, kus kasutatud](../controlling-and-reporting/item-where-used.md).

Alloleval joonisel kuvatakse loendilehe **Töökäsu ostutaotlus** näide.

![Joonis 1.](media/08-work-orders.png)


Loendis **Töökäsu ost** (**Varahaldus** > **Tavaline** > **Hange** > **Töökäsu ost**) on kuvatud töökäskudega seotud ostutellimused. Kui valite sellelt lehelt töökäsu töö, saate kasutada toimingupaani vahekaardi **Töökäsu ost** grupi **Kuva** nuppe, et sooritada mitmesuguseid toiminguid:

- Seotud ostutellimuse avamiseks valige **Ostutellimus**. 
- Seotud töökäsu avamiseks valige **Töökäsk**.
- Et saada ülevaadet sellest, kus varahalduses valitud real olevat kaupa kasutatakse, valige varade, hooldustöö tüübi vaikesätete, varuosade ja töökäskude puhul väärtus **Üksus, kus kasutatud**. Lisateavet selle ülevaate kohta vt teemast [Üksus, kus kasutatud](../controlling-and-reporting/item-where-used.md).

Alloleval joonisel kuvatakse loendilehe **Töökäsu ost** näide.

![Joonis 2.](media/09-work-orders.png)


Nii loendilehel **Töötellimuse ost** kui ka loendilehel **Töötellimuse ostutaotlus** kuvatakse iga rea paremal küljel tarnekuupäeva kontrolliga seotud sümbol. Kui sümbolina on kuvatud punases ringis hüüumärk, tähendab see, et seotud ostutellimuse või ostutaotluse tarne võib hilineda.

Ostutellimuse puhul kasutatakse võimaliku viivituse arvutamiseks ostutellimuse reaga seotud kuupäeva. Selle kuupäeva vaatamiseks valige lehel **Ostutellimus** ostutellimuse rida. Kuupäev kuvatakse kiirkaardi **Rea üksikasjad** vahekaardi **Seadistus** väljal **Kinnitatud tarnekuupäev**. Kui välja **Kinnitatud tarnekuupäev** ei ole määratud, kasutatakse arvutamiseks kiirkaardi **Ostutellimuse päis** välja **Tarnekuupäev**. Ühte neist kuupäevadest võrreldakse töökäsu või töökäsu töö vaba kuupäevaga järgnevas järjestuses:

1. Töökäsu tegelik alguskuupäev  

2. Seotud töökäsu töö planeeritud alguskuupäev 

3. Töökäsu planeeritud alguskuupäev 

4. Töötellimuse eeldatav alguskuupäev või 

Ostutaotluse puhul kasutatakse võimaliku viivituse arvutamiseks lehe **Ostutaotlused** kiirkaardi **Ostutaotluse päis** väljal **Nõutav kuupäev** toodud kuupäeva. Sellel väljal toodud kuupäeva võrreldakse töökäsu või töökäsu töö vaba kuupäevaga samas järjestuses, mida kasutatakse ostutellimuse puhul.


## <a name="create-a-purchase-order-from-a-work-order"></a>Ostutellimuse loomine töökäsu põhjal

Loendilehel **Kõik töökäsud** saate valida töökäsu töö ja seejärel luua seotud ostutellimuse või seotud ostutaotluse. Nii aitate tagada ostutellimuse või ostutaotluse ja töökäsu vahelise projektiseose olemasolu.

1. Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk, mille jaoks ostutellimus luua, ja seejärel valige **Redigeeri**.

3. Kiirkaardil **Töökäsu hooldustööd** valige töökäsu töö, mille jaoks soovite ostutellimuse luua.

4. Valige **Kaubatoimingud** > **Ostutellimus töökäsu tööst**.

5. Klõpsake loendi **Projekti ostutellimused** lehel käsku **Uus**.

6. Loo ostutellimus.

>[!NOTE]
>Seostuva ostutellimuse loomiseks järgige samu juhiseid. Kuid etapis 4 valige **Kaubatoimingud** > **Ostutaotlus töökäsu tööst**.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Töökäsku ja ostutellimuse või ostutaotluse vaheline projekti seos

Ostutellimuse rida või ostutaotluse rida on seotud töökäsu tööga töökäsu projekti ja seotud projekti tegevuse numbri kaudu. Kui loote ostutellimuse või ostutaotluse töökäsu tööst, on seotud projekti tegevuse number kohustuslik. Projekti tegevuse number sisestatakse ostutellimusele või ostutaotlusele automaatselt, kui seotud töökäsu kõik töökäsu tööd on sama hooldustöötüübiga. Projekti tegevuse number tuleb ostutellimusele või ostutaotlusele sisestada käsitsi, kui töökäsu töödel on erinevad hooldustöötüübid.

Ostutellimuse reaga seotud tegevuse numbri vaatamiseks või sisestamiseks valige loendilehel **Töökäsu ost** ostutellimuse kirje ja seejärel valige veerus **Ostutellimus** ostutellimuse link. Välja **Tegevuse number** leiate kiirkaardi **Rea üksikasjad** vahekaardilt **Projekt**.

Alltoodud illustratsioon kujutab lehe **Ostutellimus** näidet, millel on fookuses **Tegevuse number**.

![Joonis 3.](media/10-work-orders.png)

Töökäsu ostutaotluse reaga seotud tegevuse numbri vaatamiseks või sisestamiseks toimiga sarnaselt ning valige loendilehel **Töökäsu ostutaotlus** ostutaotluse kirje ja seejärel valige veerus **Ostutaotlus** ostutaotluse link. Välja **Tegevuse number** leiate kiirkaardi **Rea üksikasjad** vahekaardilt **Projekt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]