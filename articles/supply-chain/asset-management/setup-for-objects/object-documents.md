---
title: Vara dokumendid
description: Selles teemas selgitatakse vara dokumente varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8458c302b506f9f048b7886f55a392d9afceb446
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808372"
---
# <a name="asset-documents"></a>Vara dokumendid

[!include [banner](../../includes/banner.md)]

 

Selles teemas selgitatakse vara dokumente varahalduses.

Varahalduses saate seadistada dokumente nii, et need oleksid automaatselt seotud näiteks töö tüüpide, vara tootjate, vara tüüpide või varadega. See funktsioon on kasulik, kui antakse välja värskendatud dokumendiversioonid. Sel juhul peate lihtsalt värskendatud dokumendi lisama standardasukohta, mida kasutate oma Supply Chain Managementi dokumentide jaoks, ja kinnitama dokumendi loodud vara dokumendikirjega. Seejärel saab värskendatud dokumendile juurde pääseda menüü-üksustest **Kõik varad**, **Aktiivsed varad**, **Minu aktiivsed varad**, **Kõik töökäsud** ja **Aktiivsed töökäsu tööd**. Dokumentide dokumendikirjele kinnitamise protsess kasutab standardset dokumenditöötluse süsteemi.

**Näide 1:** töö tüübiga seotud dokument võib kirjeldada selle töö tüübi protseduuri.

**Näide 2:** vara tüübi, tootja ja mudeli kombinatsiooniga seotud dokument võib olla valitud varatootja mudeli standardkäsiraamat.

## <a name="create-asset-document-relation"></a>Loo vara dokumendi seos

1. Valige **Varahaldus**\>**Häälestus**\>**Vara dokumendid**.
2. Valige **Uus**, et luua vara dokumendikirje.
3. Sõltuvalt sellest, kui täpset seost te dokumendile soovite, tehke asjakohased valikud ühel või mitmel järgmistest väljadest: **Vara tüüp**, **Tootja**, **Mudel**, **Vara**, **Töö tüübi kategooria**, **Töö tüüp**, **Töö tüübi variant** ja **Töö vajadus**. Väljadel **Töö tüübi variant** ja **Töö vajadus** saadaolevad suvandid sõltuvad teie valikust väljal **Töö tüüp**.

    > [!NOTE]
    > Kui süsteem otsib dokumente, mis peaksid olema seotud vara või töökäsuga, vaatab varahaldus läbi kõik vara dokumendikirjed, et kontrollida võimalikku vastet. Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena. Teisisõnu kontrollib varahaldus esmalt **Töö nõuet** väli. Kui vastet ei leita, otsib see vastet väljale **Töö tüübi varianti**. Kui vastet ei leita, kontrollib see vastet väljale **Töö tüüp**. Nagu näete lehe **Vara dokumendid** paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule. Vara või töökäsuga võib seotud olla mitu dokumenti. Vajaduse korral saate hooldustaset muuta hooldustaotluse või töökäsu puhul.

4. Valige suvand **Manused**. Kuvatakse standardse **dokumenditöötluse** leht.
5. Seadistage dokumendid või märkmed, mis tuleks varadokumendi kirjega siduda. Pärast dokumentide sidumist kuvatakse väljal **Manused** kirjega seotud dokumentide arv.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]