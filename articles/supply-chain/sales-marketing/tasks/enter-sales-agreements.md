---
title: Müügilepingute sisestamine
description: Siin teemas selgitatakse, kuidas koostada müügilepingut, mis kohustab ühe teie klientidest ostma teatud aja jooksul toodet kokkulepitud summas, saades vastutasuks erisoodustusi.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee2c1494842c5fd2aa598546ba655c33d6fd3f16
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568299"
---
# <a name="enter-sales-agreements"></a>Müügilepingute sisestamine

[!include [banner](../../includes/banner.md)]

Siin teemas selgitatakse, kuidas koostada müügilepingut, mis kohustab ühe teie klientidest ostma teatud aja jooksul toodet kokkulepitud summas, saades vastutasuks erisoodustusi. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="set-up-sales-agreement-header"></a>Müügilepingu päise seadistus
1. Navigeerimispaanil avage **Moodulid > Müük ja turundus > Müügilepingud > Müügilepingud**.
2. Valige suvand **Uus**.
3. Väljal **Kliendi konto** valige rippmenüüst soovitud kirje.
4. **Müügilepingu klassifikatsioon** väljal valige ripploendist soovitud kirje.
5. Laiendage jaotist **Üldine**.
6. Tehke väljal **Vaikimisi kohustus** valik **Toote väärtuse kohustus**. Kohustuse tüüp on kohustuslik kriteerium, mis tuleb leppele määrata, et määrata kindlaks, kuidas lepingut täidetakse. Neli eelmääratud tüüpi võimaldavad teil määrata kliendi kohustuse eesmärgi koguse või väärtuse kujul. Koguse kohustusetüüpi saab rakendada ainult kindlale tootele, kuid väärtusel põhinevad tüübid rakenduvad nii kindlate kui määramata toodete müügile.  
7. Väljal **Expiration date** (Aegumiskuupäev) määrake kuupäev tulevikus, mil soovite, et lepe aeguks.
8. Valige nupp **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Toote väärtuse kohustuse ridade seadistus
1. Valige **Lisa rida**.
2. Väljal **Kaubakood** valige rippmenüüst soovitud kirje. Kohustuse tüüp, mille olete lepingu jaoks valinud, mõjutab teavet, mida saate lepingu ridadele sisestada. Näiteks tuleb teil väärtusel põhineva lepingu korral täpsustada kogu netosummat (kokkulepitud valuutas), mille väärtuses klient kohustub teilt kaupa ostma. Selles näites pole väljad **Quantity** (Kogus) ja **Unit** (Ühik) real kättesaadavad, kuna koostate lepingu, millele vastavalt tuleb kliendil osta toodet kindlas väärtuses.   
3. Sisestage väljale **Net amount** (Netosumma) rahasumma, mille väärtuses klient on kohustunud ostma.
4. Väljale **Discount percent** (Allahindluse protsent) sisestage protsentuaalne väärtus, mis rakendub kliendi selle leppega seotud müügitellimuse ridadele.
5. Laiendage jaotist **Rea üksikasjad**.
6. Valige **Jah** väljal **Maksimum jõustatud**.
    - Valik **Max is enforced** (Rakendatakse maksimum) tähendab, et müügitellimuse kõigi ridade, mis kasutavad kohustuse erihindu, allahindlusi ja/või maksetingimusi, kogusumma ei tohi ületada kohustuses täpsustatud summat.  
    - Väljastussummade miinimum ja maksimum määravad väärtuste vahemiku, mis tuleb iga müügitellimusega, mis valitud lepingut kasutab, müüa.   
7. Laiendage osa **Müügilepingu päis**. Kui leppe olekuks on määratud **Kehtiv**, ei saa müügitellimusi selle leppega seostada ja seetõttu ei osale need selle leppe täitmises. Selles etapis saate olekut käsitsi muuta. Siiski muudetaks olekut tavaliselt siis, kui leppe kliendi jaoks kinnitate.  
8. Valige toimingupaanil valik **Müügileping**.
9. Valige **Kinnitus**. Veenduge, et valiku **Märgi lepe kehtivaks** all oleks märgitud suvand **Jah**.  
10. Tehke väljal **Aruande printimine** valik **Jah**.
11. Valige nupp **OK**.
12. Sulgege leht. Leping kehtib nüüd. Saate alustada kliendi tellimuste lepinguga seostamist kooskõlastatud sihtmärgiga tasakaalustamiseks.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]