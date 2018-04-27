---
title: "Ühe kliendimakse kasutamine mitme arve tasakaalustamiseks, mis ulatuvad üle mitme allahindlusperioodi"
description: "See teema näitab, kuidas makstakse mitut arvet, kui igale arvele kehtib skonto. Selle artikli stsenaariumid toovad välja, kuidas võetavad skontod erinevad, olenevalt sellest, millal makse tehakse."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 92a981cbf9803e8adce1efc26a3fcfcb998540da
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="use-a-customer-payment-to-settle-multiple-invoices-that-span-multiple-discount-periods"></a>Ühe kliendimakse kasutamine mitme arve tasakaalustamiseks, mis ulatuvad üle mitme allahindlusperioodi

[!INCLUDE [banner](../includes/banner.md)]

See teema näitab, kuidas makstakse mitut arvet, kui igale arvele kehtib skonto. Selle artikli stsenaariumid toovad välja, kuidas võetavad skontod erinevad, olenevalt sellest, millal makse tehakse.

Fabrikam müüb kliendile 4032 kaupu. Fabrikam pakub skontot 1%, kui arve tasutakse 14 päeva jooksul. Fabrikam pakub osalistele maksetele ka skontosid. Tasakaalustamise parameetrid asuvad lehel **Müügireskontro parameetrid**.

## <a name="invoices"></a>Arved
Kliendil 4032 on kolm arvet kogusummale 3000,00.

-   Arve FTI-10040 summale 1000,00 sisestati 15. mail. See arve sobib 1-protsendise skonto jaoks, kui see tasutakse 14 päeva jooksul.
-   Arve FTI-10041 summale 1000,00 sisestati 25. juunil. See arve sobib 1-protsendise skonto jaoks, kui see tasutakse 14 päeva jooksul.
-   Arve FTI-10042 summale 1000,00 sisestati 25. juunil. See arve sobib 2-protsendise skonto jaoks, kui see tasutakse viie päeva jooksul, ja 1-protsendise allahindluse jaoks, kui see tasutakse 14 päeva jooksul.

## <a name="settle-all-invoices-on-june-29"></a>Kõigi arvete tasakaalustamine 29. juunil
Kui Arnie loob maksetöölehe, et need arved 29. juunil täielikult tasakaalustada, on makse 2970,00. Allahindluste kogusumma on 30,00. Arnie loob makse kliendile 4032 ja seejärel avab lehe **Kannete tasakaalustamine**. Lehel **Kannete tasakaalustamine** märgib Arnie tasakaalustamiseks kõik kolm arverida.

-   Makse arve FTI 10040 eest on 1000,00. Skontot ei arvestata.
-   Makse arve FTI 10041 eest on 990,00. Arvestatakse allahindlust 1 protsent ehk 10,00.
-   Makse arve FTI 10042 eest on 980,00. Arvestatakse allahindlust 2 protsent ehk 20,00.

| Märge                     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valitud                 | Tavaline            | FTI‑10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1 000,00                             |                                       | USA dollar      | 1 000,00         |
| Valitud                 | Tavaline            | FTI‑10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1 000,00                             |                                       | USA dollar      | 990.00           |
| Valitud ja esile tõstetud | Tavaline            | FTI‑10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1 000,00                             |                                       | USA dollar      | 980.00           |

Pärast makse sisestamist on kliendi saldo on 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Kõigi arvete tasakaalustamine 1. juulil
Kui Arnie loob maksetöölehe, et need arved 1. juulil täielikult tasakaalustada, on makse 2980,00. Arnie loob makse kliendile 4032 ja seejärel avab lehe **Kannete tasakaalustamine**. Lehel **Kannete tasakaalustamine** märgib Arnie tasakaalustamiseks kõik kolm arverida.

-   Makse arve FTI 10040 eest on 1000,00. Skontot ei arvestata.
-   Makse arve FTI 10041 eest on 990,00. Arvestatakse allahindlust 1 protsent ehk 10,00.
-   Makse arve FTI 10042 eest on 990,00. Arvestatakse allahindlust 1 protsent ehk 10,00. Kuigi 1. juuli on pärast perioodi, mis kvalifitseerub 2-protsendise allahindluse saamiseks, jääb see siiski 1-protsendise allahindluse saamise perioodi.

| Märge                     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valitud                 | Tavaline            | FTI‑10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1 000,00                             |                                       | USA dollar      | 1 000,00         |
| Valitud                 | Tavaline            | FTI‑10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1 000,00                             |                                       | USA dollar      | 990.00           |
| Valitud ja esile tõstetud | Tavaline            | FTI‑10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1 000,00                             |                                       | USA dollar      | 990.00           |

## <a name="partial-settlement-on-june-29"></a>Osaline tasakaalustamine 29. juunil
Klient 4032 saab tasuda osa summast, näiteks pool igast arvest. Arnie loob makse kliendile 4032 ja seejärel avab lehe **Kannete tasakaalustamine**. Lehel **Kannete tasakaalustamine** märgib Arnie tasakaalustamiseks kõik kolm arverida. Igal real sisestab ta kliendi antud juhiste põhjal tasakaalustatava summa. Kui Arnie valib mõne rea, näeb ta selle rea allahindluse summat ja arvesse minevat skonto summat. Kuna klient tasub pool arvest, näeb Arnie, et väärtus väljal **Skonto summa** arve FTI-10042 puhul on **20,00**, kuid välja **Arvestatud skonto** väärtus on **10,00**. Maksesumma on 1485,00.

| Märge                     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valitud                 | Tavaline            | FTI‑10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1 000,00                             |                                       | USA dollar      | 500,00           |
| Valitud                 | Tavaline            | FTI‑10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1 000,00                             |                                       | USA dollar      | 495.00           |
| Valitud ja esile tõstetud | Tavaline            | FTI‑10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1 000,00                             |                                       | USA dollar      | 490.00           |

Arnie saate maksesumma 1485,00 ka käsitsi sisestada enne lehe **Kannete tasakaalustamine** avamist. Kui Arnie sisestab maksesumma käsitsi ja seejärel märgib kõik kolm kannet, kuid ei korrigeeri iga kande puhul välja **Tasakaalustatav summa** väärtust, saab ta lehe sulgemisel järgmise teate.

> Märgitud kannete kogusummade erineb töölehe summast. Kas muuta töölehe summat?

Kui Arnie soovib, et maksesumma oleks vaid 1485,00, klõpsab ta suvandit **Ei** ja seejärel sisestab töölehe. Kanded tasakaalustatakse järgmiselt.

1.  Arve FTI-10040 on täielikult tasakaalustatud summale 1000,00, kuna see oli sisestatud 15. mail ja on vanim arve. Skontot ei arvestata. Maksekande jääksumma on 485,00.
2.  Arve FTI-10041 ei ole üldse tasakaalustatud. Arved FTI-10041 ja FTI-10042 sisestati samal kuupäeval. Siiski on 1-protsendine allahindlus saadaval arvele FTI-10041 ja 2-protsendine allahindlus arvele FTI-10042. Kuna arvele FTI-10042 on saadaval parem allahindlus, tasakaalustatakse ülejäänud 485,00 arvega FTI-10042.
3.  Arve FTI-10042 tasakaalustatakse ülejäänud summaga 485,00. Fabrikam pakub osalisi allahindlusi. Selles näites on allahindlus 9,90 (= 485,00 ÷ 0,98 × 0,02). Summa (485,00) on jagatud 0,98-ga, sest allahindlus on 2 protsenti (seega maksab klient 98 protsenti arvest). Seejärel korrutatakse tulemus skonto protsendiga, mis on 2. Makse 485,00 pluss allahindlus 9,90 võrdub 494,90. Algse arve summa oli 1000,00. Seega on kande saldo 505,10 (= 1000,00 – 494,90).

Arnie vaatab seda teavet lehel **Kliendi kanded**.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo  | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI‑10040  | Arve          | 5/15/2015 | 10040   | 1 000,00                             |                                       | 0,00     | USA dollar      |
| FTI‑10041  | Arve          | 25.06.2015 | 10041   | 1 000,00                             |                                       | 1 000,00 | USA dollar      |
| FTI‑10042  | Arve          | 25.06.2015 | 10042   | 1 000,00                             |                                       | 505.10   | USA dollar      |
| ARP‑10040  | Makse          | 6/29/2015 |         |                                      | 1,485.00                              | 0,00     | USA dollar      |
| DISC‑10040 | Skonto    | 6/29/2015 |         |                                      | 9.90                                  | 0,00     | USA dollar      |






