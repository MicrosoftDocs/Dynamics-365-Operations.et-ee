---
title: Käibemaksuarvutusmeetodid valimine väljal Päritolu
description: See artikkel selgitab käibemaksukoodide lehe välja Päritolu valikuid ja seda, kuidas käibemaks arvutatakse, tuginedes tehtud käibemaksukoodi valikule.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be935b80e06158d9634989ba03747f4a59247f8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204926"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Käibemaksuarvutusmeetodid valimine väljal Päritolu

[!include [banner](../includes/banner.md)]

See artikkel selgitab käibemaksukoodide lehe välja Päritolu valikuid ja seda, kuidas käibemaks arvutatakse, tuginedes tehtud käibemaksukoodi valikule.

Iga lehel Käibemaksukoodid loodud käibemaksukoodi puhul peate valima arvutamismeetodi, mida rakendatakse väljal Päritolu olevale käibemaksu baassummale.

## <a name="percentage-of-net-amount"></a>Protsent netosummast
Välja Päritolu vaikeväärtus on Arvutamismeetod Protsent netosummast. Käibemaks arvutatakse protsendina ostu- või müügisummast, mis ei sisalda muid käibemakse.
### <a name="example"></a>Näide

maksumäär on 25%. Arve real kuvatakse kogus (10 kaupa, igaüks hinnaga 1.00), ja kliendile pakutakse 10% rea allahindlust. Netosumma: (10 x 1,00) – 10% = 9,00, käibemaks: 9,00 x 25% = 2,25, kogusumma: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Protsent brutosummast
Kui valite meetodi Protsent brutosummast, arvutatakse käibemaks protsendina müügi brutosummast. Brutosumma on rea netosumma pluss kõik rea maksud ja tasud, välja arvatud maks, mille välja Päritolu väärtus on Protsent brutosummast.
### <a name="example"></a>Näide

Maksuamet on kehtestanud kaubale eri lõivud. Lõivusummad lisati netosummale enne käibemaksu arvutamist. Võtame arvesse järgmisi käibemaksukoode.
-   LÕIV 1 = 10%, kasutades arvutusmeetodit Protsent netosummast
-   LÕIV 2 = 20%, kasutades arvutusmeetodit Protsent netosummast
-   KÄIBEMAKS = 25%, kasutades arvutusmeetodit Protsent brutosummast

Kui netosumma on 10,00, siis LÕIV 1 = 1,00 (10,00 × 10%) ja LÕIV 2 = 2,00 (10,00 × 20%). Summad on järgmised. Brutosumma: netosumma + LÕIVU 1 summa + LÕIVU 2 summa (10,00 + 1,00 + 2,00) = 13,00, KÄIBEMAKS: 13,00 × 25% = 3,25, LÕIVUD ja KÄIBEMAKS kokku: 1,00 + 2,00 + 3,25 = 6,25, kogusumma: 10,00 + 6,25 = 16,25

| **Märkus.**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kande puhul saab kasutada ainult üht maksukoodi, mille välja Päritolu väärtus on Protsent brutosummast. Kui kande kohta määratakse mitu sellist maksukoodi, kuvatakse tõrge, et käibemaksu ei saa arvutada. |


<a name="percentage-of-sales-tax"></a>Protsent käibemaksust
-----------------------

Kui valite väljal Päritolu väärtuse Protsent käibemaksust, arvutatakse käibemaks protsendina käibemaksust, mis on valitud väljal Käibemaks käibemaksult. Esimesena arvutatakse käibemaks, mis on valitud väljal Käibemaks käibemaksult. Teine käibemaks arvutatakse seejärel esimese käibemaksusumma alusel.
### <a name="example"></a>Näide

Võtame arvesse järgmisi käibemaksukoode.
-   LÕIV 1 = 10%, kasutades meetodit Protsent netosummast
-   LÕIV 2 = 20%, kasutades meetodit Protsent käibemaksust, nii et väljal Käibemaks käibemaksult on valitud väärtus Lõiv 1.
-   KÄIBEMAKS = 25%, kasutades meetodit Protsent brutosummast

Netosumma: 10,00, LÕIV 1: 10,00 × 10% = 1,00, LÕIV 2: 1,00 × 20% = 0,20, brutosumma: 10,00 + 1,00 + 0,20 = 11,20, KÄIBEMAKS: 11,20 × 25% = 2,80, LÕIVUD ja KÄIBEMAKS kokku: 1,00 + 0,20 + 2,80 = 4,00, kogusumma: 10,00 + 4,00 = 14,00

| **Märkus.**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mitmetasandiline maks pole maksuarvutustes võimalik. Maksu ei saa arvutada maksu põhjal, mis on teise maksu põhjal juba arvutatud. Kandes saab arvutada maksukoodide põhjal mitu ühetasemelist maksu. |

## <a name="amount-per-unit"></a> Summa ühiku kohta
Kui valite väljal Päritolu suvandi Summa ühiku kohta, arvutatakse käibemaks ühiku kohta fikseeritud summana korrutatuna dokumendireale sisestatud kogusega. Ühik tuleb valida väljal Ühik. Summa ühiku kohta on määratud lehel Käibemaksukoodi väärtused.
### <a name="example"></a>Näide

Käibemaksukoodi seadistatakse järgmiselt: 1,20 USD ühiku kohta = kast. Müügiarve real on kaupa müüdud 25 kasti. Käibemaks arvutatakse järgmiselt: 25 × 1,20 = 30,00

| **Märkus.**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kui kanne sisestatakse muus kui käibemaksukoodi jaoks määratud ühikus, teisendatakse see automaatselt ühikuteisenduste alusel, mis on seadistatud lehel Ühikuteisendused. |

###  <a name="amount-per-unit-additional-option"></a> Summa ühiku kohta, lisavalik

Vahekaardil Kalkulatsioon saate valida, kas ühikusumma kohta arvutatav maks arvutatakse enne muid maksukoode ja lisatakse netosummale enne muude maksukoodide arvutamist, mille puhul välja Päritolu väärtus on Protsent netosummast.

### <a name="examples"></a>Näited

Oletame, et arvutame kannetel kaks maksukoodi.

-   LÕIV: Päritolu = Summa ühiku kohta ja käibemaks, väärtuseks on määratud 5,00 ühiku (tk) kohta.
-   KÄIBEMAKS: Päritolu = nagu allolevates näidetes on näidatud, on väärtuseks seatud 25%

Müüme kaupa 1 tüki ühikuhinnaga 10,00.
#### <a name="example-1"></a>Näide 1

KÄIBEMAKS: Päritolu = meetod Protsent brutosummast. Suvandil Arvuta enne käibemaksu pole mõju, kuna KÄIBEMAKS arvutatakse protsendina brutosummast. LÕIV: 1 × 5,00 = 5,00, brutosumma: 10,00 + 5,00 = 15,00, KÄIBEMAKS: 15,00 × 25% = 3,75, käibemaks kokku: 5,00 + 3,75 = 8,75, kogusumma: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Näide 2

KÄIBEMAKS: Päritolu = Protsent netosummast . Suvand Arvuta enne käibemaksu pole LÕIVU arvutamiseks valitud. Netosumma: 10,00, LÕIV: 1 × 5,00 = 5,00, KÄIBEMAKS: 10,00 × 25% = 2,50, käibemaks kokku: 5,00 + 2,50 = 7,50, kogusumma: 10,00 + 7,50 = 17,50.

#### <a name="example-3"></a>Näide 3

KÄIBEMAKS: Päritolu = Protsent netosummast . Suvand Arvuta enne käibemaksu on LÕIVU arvutamiseks valitud. Netosumma: 10,00, LÕIV: 1 × 5,00 = 5,00, KÄIBEMAKS: (10,00 + 5,00) × 25% = 3,75, käibemaks kokku: 5,00 + 3,75 = 8,75, kogusumma: 10,00 + 8,75 = 18,75.

#### <a name="example-4"></a>Näide 4

Näite 3 ja näite 1 tulemus on sama, sest kasutatakse ainult ühte lõivu. Oletame, et teil on kaks LÕIVU, millest vaid üks on kaasatud käibemaksu arvutamisel netosummasse: LÕIV 1: 5,00, kasutades meetodit Summa ühiku kohta ja suvand Arvuta enne käibemaksu on valitud. LÕIV 2: 2,50, kasutades meetodit Summa ühiku kohta ja suvand Arvuta enne käibemaksu pole valitud. Käibemaks: 25%, kasutades meetodit Protsent netosummast. Netosumma: 10,00, LÕIV 1: 1 × 5,00 = 5,00, LÕIV 2: 1 × 2,50 = 2,50, netosumma käibemaksu jaoks: 10,00 + 5,00 = 15,00, KÄIBEMAKS: 15,00 × 25% = 3,75, käibemaks kokku, k.a lõivud: 5,00 + 2,50 + 3,75 = 11,25, kogusumma: 10,00 + 11,25 = 21,25, 25% KÄIBEMAKS arvutatakse netosumma (10,00) + LÕIVU 1 (5,00) = 15,00 summana. LÕIV 2 lisatakse maksusummale pärast käibemaksu arvutamist.

## <a name="calculated-percentage-of-net-amount"></a> Arvutatud protsent netosummast
Arvutatud protsent netosummast käsitleb maksuarvutust teisiti, olenevalt dokumendi või töölehe parameetri Summad sisaldavad käibemaksu sättest.
### <a name="example-1"></a>Näide 1

Dokumendi/töölehe suvandi Summad sisaldavad käibemaksu sätteks on valitud Jah. Kanderea summa: 10,00, maksumäär: 25%, käibemaks: kanderea summa × maksumäär (10,00 × 25%) = 2,50, maksubaasi summa (päritolu summa): kanderea summa – käibemaks (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Näide 2

Dokumendi/töölehe suvandi Summad sisaldavad käibemaksu sätteks on valitud Ei. Kanderea summa: 10,00, maksumäär: 25%, käibemaks: (kanderea summa × maksumäär) / (100 – maksumäär) (10,00 × 25%) / (100% – 25%) = 3,33, maksubaasi summa (päritolu summa): kanderea summa = 10,00



<a name="additional-resources"></a>Lisaressursid
--------

[Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal](marginal-base-field.md)

[Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]