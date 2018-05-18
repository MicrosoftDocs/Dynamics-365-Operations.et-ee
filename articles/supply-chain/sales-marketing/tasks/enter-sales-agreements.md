--- 
title: "Müügilepingute sisestamine"
description: "See protseduur näitab teile, kuidas koostada müügilepingut, mis kohustab ühe teie klientidest ostma teatud aja jooksul toodet kokkulepitud summas, saades vastutasuks erisoodustusi."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: a0d49068d2c6a62bf7912c2fd7cccd53308bd196
ms.contentlocale: et-ee
ms.lasthandoff: 02/13/2018

---
# <a name="enter-sales-agreements"></a>Müügilepingute sisestamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab teile, kuidas koostada müügilepingut, mis kohustab ühe teie klientidest ostma teatud aja jooksul toodet kokkulepitud summas, saades vastutasuks erisoodustusi. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="set-up-sales-agreement-header"></a>Müügilepingu päise seadistus
1. Avage Müük ja turundus > Müügilepingud > Müügilepingud.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake väljal Sales agreement classification (Müügilepingu klassifikatsioon) otsingu avamiseks ripploendi nuppu.
7. Klõpsake loendis valitud real olevat linki.
8. Laiendage jaotist Üldine.
9. Tehke väljal Default commitment (Vaikimisi kohustus) valik Product value commitment (Toote väärtuse kohustus).
    * Kohustuse tüüp on kohustuslik kriteerium, mis tuleb leppele määrata, et määrata kindlaks, kuidas lepingut täidetakse. Neli eelmääratud tüüpi võimaldavad teil määrata kliendi kohustuse eesmärgi koguse või väärtuse kujul. Koguse kohustusetüüpi saab rakendada ainult kindlale tootele, kuid väärtusel põhinevad tüübid rakenduvad nii kindlate kui määramata toodete müügile.  
10. Väljal Expiration date (Aegumiskuupäev) määrake kuupäev tulevikus, mil soovite, et lepe aeguks.
11. Klõpsake nuppu OK.

## <a name="set-up-product-value-commitment-lines"></a>Toote väärtuse kohustuse ridade seadistus
1. Klõpsake käsku Lisa rida.
2. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
    * Kohustuse tüüp, mille olete lepingu jaoks valinud, mõjutab teavet, mida saate lepingu ridadele sisestada. Näiteks tuleb teil väärtusel põhineva lepingu korral täpsustada kogu netosummat (kokkulepitud valuutas), mille väärtuses klient kohustub teilt kaupa ostma. Selles näites ei ole koguse ja ühiku väljad real kättesaadavad, kuna koostate lepingu, millele vastavalt tuleb kliendil osta toodet kindlas väärtuses.   
5. Sisestage väljale Net amount (Netosumma) rahasumma, mille väärtuses klient on kohustunud ostma.
6. Väljale Discount percent (Allahindluse protsent) sisestage protsentuaalne väärtus, mis rakendub kliendi selle leppega seotud müügitellimuse ridadele.
7. Laiendage jaotis Rea üksikasjad.
8. Valige Yes (Jah) väljal Max is enforced (Maksimum rakendatud).
    * Valik Max is enforced (Rakendatakse maksimum) tähendab, et müügitellimuse kõigi ridade, mis kasutavad kohustuse erihindu, allahindlusi ja/või maksetingimusi, kogusumma ei tohi ületada kohustuses täpsustatud summat.  
    * Väljastussummade miinimum ja maksimum määravad väärtuste vahemiku, mis tuleb iga müügitellimusega, mis valitud lepingut kasutab, müüa.   
9. Laiendage müügilepingu päiseosa.
    * Kui leppe olekuks on määratud Effective (Kehtiv), ei saa müügitellimusi selle leppega seostada ja seetõttu ei osale need selle leppe täitmises. Selles etapis saate olekut käsitsi muuta. Siiski muudetaks olekut tavaliselt siis, kui leppe kliendi jaoks kinnitate.  
10. Klõpsake tegumiribal valikut Müügileping.
11. Klõpsake suvandit Kinnitus.
    * Veenduge, et valiku Mark agreement as effective (Märgi lepe kehtivaks) all oleks märgitud Yes (Jah).  
12. Tehke väljal Print report (Aruande printimine) valik Yes (Jah).
13. Klõpsake nuppu OK.
14. Sulgege leht.
    * See leping kehtib nüüd ja saate alustada kliendi tellimuste lepinguga seostamist kooskõlastatud sihtmärgiga tasakaalustamiseks.  


