---
title: Rendi sisestamise tüübid
description: Selles teemas kirjeldatakse vara rentimise kannete jaoks kasutatavaid sisestamise tüüpe.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ceb4fbeb4dbf2f535e05a9d46c84169435d2803b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442575"
---
# <a name="lease-posting-types"></a>Rendi sisestamise tüübid

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse vara rentimise kannete jaoks kasutatavaid sisestamise tüüpe.

## <a name="lease-asset"></a>Rendivara

Konto on seostatud kasutamisõiguse esemeks oleva varaga. Seda kontot debiteeritakse, kui rendikirje algselt tuvastatakse uue rendi raamatupidamise standardites, raamatupidamise standardite kodeerimise teemas 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardis 16 (IFRS 16). Muudetud rendikirje puhul võidakse seda kontot kas debiteerida või krediteerida, sõltuvalt sellest, kas muudatus suurendab või vähendab rendikohustist.

**Töölehe kirjete näide:** esialgne tuvastamine<br>
**Deebet:** renditav vara XXX<br>
**Kreedit:** rendikohustis XXX

## <a name="lease-liability"></a>Rendikohustis

Konto on seostatud rendikohustisega, mis tekib, kui maksed diskonteeritakse uute IFRS 16 ja ASC 842 standardite alusel. See konto krediteeritakse, kui rendikirje uute standardite alusel esmakordselt tuvastatakse. See debiteeritakse rendimaksete ja krediteeritakse intressi laekumiste suhtes.

**Töölehe kirjete näide:** esialgne tuvastamine<br>
**Deebet:** renditav vara XXX<br>
**Kreedit:** rendikohustis XXX

**Töölehe kirjete näide:** intressi laekumine<br>
**Deebet:** intressikulu XXX<br>
**Kreedit:** rendikohustis XXX

**Töölehe kirjete näide:** rendimakse<br>
**Deebet:** rendikohustis XXX<br>
**Kreedit:** hankija reskontro / rendimakse XXX

## <a name="short-term-lease-liability"></a>Lühiajalise rendilepingu kohustis

Konto on seostatud lühiajalise rendikohustisega, kui sisestatakse lühiajalise rendikohustise ümberklassifitseerimise töölehe kirje. Seda kontot krediteeritakse kuu viimasel päeval lühiajalise kohustise amortiseerimise graafikuga. Samas järgmise kuu esimesel päeval sama summa debiteeritakse.

**Töölehe kirjete näide:** lühiajalise rendikohustise ümberklassifitseerimine<br>
**Deebet:** rendikohustis XXX<br>
**Kreedit:** lühiajaline rendikohustis XXX<br>
**Deebet:** lühiajaline rendikohustis XXX<br>
**Kreedit:** rendikohustis XXX

## <a name="depreciation-expense"></a>Kulumi kulu

Konto on seostatud kuluga, mis on seotud kasutamisõiguse esemeks oleva vara kulumiga vastavalt standardile IFRS 16, ASC 842 ja kapitalirendi tingimustel vastavalt standardile IAS 17 ja ASC 840. Seda kontot debiteeritakse, kui kasutamisõiguse esemeks olev vara iga kuu kantakse kulumisse.

**Töölehe kirjete näide:** kulumi laekumine<br>
**Deebet:** kulumi kulu XXX<br>
**Kreedit:** kogunenud kulum XXX

## <a name="gainloss-on-lease-modification"></a>Kasum/kahjum rendi muutmisel

Konto on seostatud mis tahes kasumi või kahjumiga, mis tulenevad rendi muudatustest. Rendi muutumise ajal võib tekkida kasum, kui muudatus vähendab rendikohustist summa võrra, mis ületab kasutamisõiguse esemeks oleva vara bilansilist väärtust.

Näiteks on rendikirjel praegu rendikohustise bilansiline väärtus 150 000 eurot ja kasutamisõiguse esemeks oleva vara bilansiline väärtus 100 000 eurot. Renti muudetakse ja see muudatus tekitab uue tulevaste minimaalsete rendimaksete praeguse väärtuse (PVFMLP) 40 000 eurot. Seega rendikohustist debiteeritakse summas 110 000 eurot (150 000 – 40 000). Kuna kasutamisõiguse esemeks oleva vara väärtus on ainult 100 000 eurot, vähendab see vara väärtuse alla nulli (0). Seetõttu on raamatupidamise juhendis sätestatud, et ülejäänu tuleks kirjendada kasumi kontole. Sellisel juhul on töölehe lõplikuks kirjeks rendikohustise deebet summas 110 000 eurot, rendi vara kreedit summas 100 000 eurot ja kasumi konto kreedit summas 10 000 eurot.

**Töölehe kirjete näide:** rendi muutmine<br>
**Deebet:** rendikohustis XXX<br>
**Kreedit:** renditav vara XXX<br>
**Kreedit:** kasum XXX

## <a name="accumulated-depreciation"></a>Akumuleeritud kulum

Konto on seotud kasutamisõiguse esemeks oleva vara kontrakontoga. Seda kontot krediteeritakse kulumi kulu sisestamisel.

**Töölehe kirjete näide:** kulumi laekumine<br>
**Deebet:** kulumi kulu XXX<br>
**Kreedit:** kogunenud kulum XXX

## <a name="retained-earnings"></a>Jaotamata kasum

Konto on seostatud kinnipeetud tuludega. Seda kontot on võimalik kas debiteerida või krediteerida ülemineku korrigeerimise töölehe kirjel, kasutades täielikku tagasiulatuvat meetodit või kumulatiivset järelkulu valiku A meetodil. Erinevus esialgse kasutamisõiguse esemeks oleva vara ja rendikohustise vahel kirjendatakse kinnipeetud tuludena. Harvadel juhtudel võib jaotamata kasumit mõjutada ka rendi muutmine, kui rendi klassifikatsioon muutub finantseerimisest kasutusele, et hinnata kasutamisõiguse esemeks olev vara üles või alla, et see oleks kapitalirendiga võrdne.

**Töölehe kirjete näidis:** siirde korrigeerimine (täielikult tagasiulatuv või kumulatiivse järelkulu valiku A meetod)<br>
**Deebet:** rendikohustis XXX<br>
**Kreedit:** renditav vara XXX<br>
**Kreedit:** jaotamata kasum XXX

## <a name="variable-payment"></a>Muutuv makse

Konto on seotud muutuvate rendimaksetega, mis luuakse indeksi ümberhindamise poolt vastavalt standardite ASC 842, ASC 840 ja IAS 17 liisingutele. Rendi maksegraafikus on muutuvad maksed lisatud veergu **Muutuv makse**. Seda konto debiteeritakse, kui arve luuakse maksegraafiku rea suhtes, mis sisaldab muutuvat makset.

**Töölehe kirjete näide:** rendimakse<br>
**Deebet:** rendikohustis XXX<br>
**Deebet:** muutuv makse XXX<br>
**Kreedit:** hankija reskontro / rendimakse XXX

## <a name="deferred-rent-asset-liability"></a>Edasilükatud rendi vara (kohustis)

Konto on seostatud edasilükatud rendi varaga või kohustisega, mis on loodud edasilükatud rendi töötlemise rendi poolt. Seda kontot debiteeritakse, kui arve sisestatakse edasilükatud üüri töötlemise rendikirjega, kui rendimakse summa on suurem kui perioodi lineaarse rendi kulu. See krediteeritakse, kui rendimakse on väiksem kui perioodi lineaarse rendi kulu.

**Töölehe kirjete näide:** rendimakse (edasilükatud rendi töötlemise rent)<br>
**Deebet:** rendikulu XXX<br>
**Kreedit:** edasilükatud rendi kohustis XXX<br>
**Kreedit:** hankija reskontro / rendimakse XXX

## <a name="lease-expense"></a>Rendikulu

Konto on seostatud rendi kuluga, kui rent on klassifitseeritud kui edasilükatud rent. Seda kontot debiteeritakse, kui arve sisestatakse edasilükatud üüri töötlemise suhtes.

**Töölehe kirjete näide:** rendimakse (edasilükatud rendi töötlemise rent)<br>
**Deebet:** rendikulu XXX<br>
**Kreedit:** edasilükatud rendi kohustis XXX<br>
**Kreedit:** hankija reskontro / rendimakse XXX

## <a name="impairment-expense"></a>Väärtuse languse kulu

Konto sisestatakse siis, kui rent on mõjutatud. Seda kontot debiteeritakse, samas kui kasutamisõiguse esemeks oleva vara konto on otse krediteeritud.

**Töölehe kirjete näide:** rendimakse<br>
**Deebet:** väärtuse languse kulu XXX<br>
**Kreedit:** kasutamisõiguse esemeks olev vara XXX

## <a name="lease-payment"></a>Rendimakse

Konto sisestatakse, kui **Hankijale maksmine** parameetrid on välja lülitatud. Kui parameeter on välja lülitatud, krediteeritakse hankija tasutava asemel seda kontot.

**Töölehe kirjete näide:** rendimakse<br>
**Deebet:** rendikohustis XXX<br>
**Krediteerimine:** rendimakse XXX

## <a name="expense-type-postings"></a>Kulutüübi sisestused

Iga kulutüübi jaoks valitud konto debiteeritakse, kui selle kulu tüübi jaoks on loodud makse. Näiteks debiteeritakse kulutüübi **Kindlustus** jaoks määratud kontot iga kord, kui kindlustuse täitekulu ajakavast loodud arve või makse tööleht.

**Töölehe kirjete näide:** kindlustuse makse<br>
**Deebet:** kindlustuse kulutüübi konto XXX<br>
**Kreedit:** nihkekonto XXX

> [!NOTE]
> Nihkekonto valitakse täitekulu maksegraafikule rendi tasemel. Selle nihkekonto saab seostada hankija või pearaamatu konto.
