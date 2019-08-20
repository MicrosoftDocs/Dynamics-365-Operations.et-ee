---
title: Varade kriitilisuse tüübid
description: Teemas selgitatakse varade kriitilisuse tüüpe varahalduses.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660038060826ade9301e50143e49b53ba3fcd3ab
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783213"
---
# <a name="asset-criticalities"></a>Varade kriitilisuse

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Teemas selgitatakse varade kriitilisuse tüüpe varahalduses. Varade kriitilisus on seotud varaga ja kantakse töötellimustele üle. Töötellimuse puhul ei saa seda muuta. Varade kriitilisust kasutatakse töökäsu kriitilisuse arvutamiseks töötellimuse planeerimisel. Teisisõnu kasutatakse seda arvutamiseks, millises ulatuses mõjutab vara hooldustöö tootmisgraafikut ja tootlikkust teie ettevõttes. Lisateabe saamiseks häälestuse kohta, mis on seotud töötellimuse planeerimisel reitingusummade arvutamisega, vt teemat [Varahalduse parameetrid](../setup-for-objects/enterprise-asset-management-parameters.md).

Kriitilisuse seadistamiseks looge esmalt kriitilisuse tüübid, mida tuleks kasutada vara seadistuses. Seejärel seadistage vara kriitilisused.

## <a name="set-up-criticality-types"></a>Kriitilisuse tüüpide häälestamine

1. Valige **Varadehaldus**\>**Häälestus**\>**Varad** \>**Kriitilisuse tüübid**.
2. Valige **Uus**, et luua uus kirje.
3. Väljale **Kriitilisus** sisestage number, mis näitab kriitilisust.
4. Väljale **Nimi** sisestage kriitilisuse tüübi nimi.
5. Väljale **Tegur** sisestage tegur. Seda tegurit kasutatakse töökäsu plaanimise arvutamisel, et määrata kriitilisuse kirje, mida tuleks kasutada. (Suurima teguriga kirjet kasutatakse alati.) See säte on asjakohane, juhul kui nagu on näidatud järgmisel joonisel, luuakse kriitilisuse read, millel on sama kriitilisuse väärtus.

    ![Joonis 1](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Vara kriitilisuse häälestus

1. Valige **Varahaldus**\>**Häälestus**\>**Vara kriitilisus**.
2. Valige **Uus**, et luua uus kirje.
3. Sõltuvalt varade kriitilisuse nõutavast üksikasjade tasemest tehke asjakohased valikud väljadel **Funktsionaalne asukoht**, **Vara liik**, **Tootja**, **Mudel**, **Vara**, **Töö tüübi kategooria**, **Töö tüüp**, **Töö tüübi variant** ja **Töö vajadus**.

    > [!NOTE]
    > Varade kriitilisuse valimisel vaatab varahaldus läbi kõik vara kriitilisuse kirjed, et kontrollida võimalikku vastet. Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena. Teisisõnu kontrollib varahaldus esmalt **Töö nõuet**. Kui vastet ei leita, kontrollib see **Töö tüübi varianti**. Kui vastet ei leita, kontrollib see **Töö tüübi** ja nii edasi. Nagu näete lehe paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule. Kui vastet ei leita, kasutatakse „vaikimisi“ kirjet, mille kohta pole valikuid tehtud.

4. Väljal **Kriitilisus** valige üks kriitilisuse väärtustest, mille olete eelneva protsessi käigus loonud.

### <a name="notes-about-criticality-setup"></a>Märkused kriitilisuse seadistuse kohta

- Kui muudate selles seadistuses vara kriitilisust pärast seda, kui olete seda töökäsul juba kasutanud, ei värskendata selle töökäsu kriitilisust vastavalt.
- Töökäsu kriitilisus arvutatakse ümber iga kord, kui töökäsu rida lisatakse või kustutatakse töökäsult.
- Kui töökäsk sisaldab mitut töökäsu tööd, kasutatakse töökäsu puhul alati kõrgeimat kriitilisust vastavalt väljale **Faktor** lehel **Kriitilisuse tüübid**.
- Üldiselt võib vara kriitilisus perioodi jooksul muutuda. Kriitilisust võivad mõjutada uute seadmete ostmine, renoveerimine jne. Kaaluge oma varade kriitilisuse ümberhindamist regulaarsete ajavahemike järel (näiteks kord aastas või igal teisel aastal), et veenduda, kas teie kriitilisuse määratlused vastavad teie praegusele tootmisseadistusele.
