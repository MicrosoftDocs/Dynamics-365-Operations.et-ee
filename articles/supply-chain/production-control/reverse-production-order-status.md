---
title: Tootmistellimuse oleku ennistamine
description: See artikkel kirjeldab, kuidas tootmistellimuse olekut tühistada.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d50cbcb4031d5c9f2c814883afd1fb38777d2ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903952"
---
# <a name="reverse-the-production-order-status"></a>Tootmistellimuse oleku ennistamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas tootmistellimuse olekut tühistada. 

Tootmistellimuse oleku ennistamisel viiakse tellimuse ja kõik protsessidega seotud operatsioonid tootmistsüklis ühe etapi võrra tagasi. Näiteks on tootmistellimuse olek **Planeeritud** ja te muudate olekuks tagasi **Loodud**. Sellisel juhul peab süsteem esmalt muutma olekuks **Hinnanguline**, mis on olekule **Plaanitud** vahetult eelnev olek. Seejärel saate oleku muuta soovitud väärtusele – **Loodud**. **Märkus.** Kui tellimus on jõudnud olekusse **Kinnita lõpetamine**, saate selle siiski tagasi viia varasemale olekule. Siiski peate hindamise ja operatsioonide planeerimise, töö planeerimise või mõlemat tüüpi planeerimised uuesti käivitama, et tellimuse teavet värskendada. See etapp on vajalik, kuna lähtestada tuleb ka kõik allesjäänud kauba tarbimise ja operatsiooniressursi tarbimise reserveeringud. Artikli ülejäänud osas selgitatakse, mis juhtub, kui ennistate tootmistellimuse oleku järgmistel viisidel.

-   Olekust **Hinnanguline** olekusse **Loodud**
-   Olekust **Planeeritud** olekusse **Hinnanguline**
-   Olekust **Väljastatud** olekusse **Planeeritud**
-   Olekust **Alustatud** olekuks **Väljastatud**

## <a name="from-estimated-to-created"></a>Olekust Hinnanguline olekusse Loodud
Tootmistellimuse oleku ennistamisel väärtuselt **Hinnanguline** väärtusele **Loodud** eemaldatakse kauba tarbimine, mis arvutati kaupade kohta koosluses. Kustutatakse tootmiserea varude kanded tootmisreal ja tootmistellimuse koosluseridade välja **Jäägi olek** lähtestatakse väärtusele **Lõpetatud**. Kui suvandid **Tuletatud ostud** ja **Tuletatud tootmine** on valitud, kustutatakse kõik aluseks olevad ostutellimused või tootmistellimused. Kui hindasite tootmistellimuse kulusid või reserveerisite käsitsi kaupu, nii et neid saaks tootmises kasutada, eemaldatakse need kanded.

## <a name="from-scheduled-to-estimated"></a>Olekust Planeeritud olekusse Hinnanguline
Tootmistellimuse oleku ennistamisel väärtuselt **Planeeritud** väärtusele **Hinnanguline** eemaldatakse planeeritud algus- ja lõppkuupäevad ning algus- ja lõppkellaajad. Eemaldatakse planeerimisel tehtud võimsuse reserveeringud ning kustutatakse tööde planeerimisel loodud tööd. Lähtestatakse lehel **Tootmistellimuse üksikasjad** kogu operatsioonide planeerimise ja tööde planeerimise kohta talletatav teave.

## <a name="from-released-to-scheduled"></a>Olekust Väljastatud olekusse Planeeritud
Tootmistellimuse oleku ennistamisel väärtuselt **Väljastatud** väärtusele **Planeeritud** muutub ainult olekuvälja väärtus.

## <a name="from-started-to-released"></a>Olekust Alustatud olekuks Väljastatud
Tootmistellimuse oleku ennistamisel väärtuselt **Alustatud** väärtusele **Väljastatud** ennistatakse kõik lõpetatuna kinnitatud kaubad. Kui materjal on komplekteeritud või tootmisele on tehtud sissetulevaid ja väljaminevaid tarneid, ennistatakse need sätted. Tootmistellimuse koosluseridade väli **Jäägi olek** muutub väärtuselt **Lõpetatud** väärtusele **Materjali tarbimine**. Kui kellaaeg on registreeritud või kogused tootmisprotsessi operatsioonide jaoks lõpetatuna kinnitatud, ennistatakse need sätted. Tootmistellimuse väli **Jäägi olek** muutub väärtuselt **Lõpetatud** väärtusele **Protsessi tarbimine**. Ennistatakse sätted kõigi kaupade puhul, mis on sisestatud pooleliolevatena või lõpetamata toodanguna. Lehel **Tootmistellimuse üksikasjad** ennistatakse väljad, millel kuvatakse alustatud või lõpetatuna kinnitatud kogus. Ennistatakse ka nende kannete kuupäevad.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]