---
title: Global Inventory Accounting toetatavad äridokumendid
description: Selles teemas loetletakse äridokumendid, mida toetab Global Inventory Accounting. See annab üksikasjaliku näite ostutellimuste dokumentidest.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 44081be35c6737aa0d16b6e11a5fc8f94b41e872
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674445"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Global Inventory Accounting toetatavad äridokumendid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Kui Global Inventory Accounting lisandmoodul on täielikult seadistatud, on see valmis töötlema Microsoft Dynamics 365 Supply Chain Management sisestatud varudega seotud dokumente.

## <a name="supported-business-documents"></a>Toetatud äridokumendid

Äridokumente on kahte tüüpi.

- **Töölehega dokumendid** – nendeks dokumentideks on toote sissetuleku-, ostuarve-, saatelehe- ja müügiarvedokumendid.
- **Tööleheta dokumendid** – nendeks dokumentideks on inventuuri, liikumise ja laokorrektsiooni dokumendid.

Selles teemas hiljem kasutatakse protsessi illustreerimiseks näitena ostutellimusi.

Järgmises tabelis loetletakse dokumendid, mida praegune väljaanne toetab.

| Document type      | Dokument         |
|--------------------|-----------------|
| Ostutellimus     | Toote sissetulek |
| Ostutellimus     | Arve         |
| Müügitellimus        | Saateleht    |
| Müügitellimus        | Arve         |
| Laotöölehed | Liikumine        |
| Laotöölehed | Korrigeerimine      |
| Laotöölehed | Inventuur        |
| Laotöölehed | Ülekanne        |
| Üleviimistellimus     | Saadetis        |
| Üleviimistellimus     | Vastuvõtmine         |

> [!IMPORTANT]
> Global Inventory Accounting töötleb asünkroonselt dokumente, mis on sisestatud teenusesse Supply Chain Management. Problemaatiliste dokumentidele tõrketeateid ei kuvata.

## <a name="example-purchase-order"></a>Näidis: ostutellimus

### <a name="product-receipt"></a>Toote sissetulek

Sisestage toote tšekid tavapärasel viisil. Valige leheküljel **Kõik ostutellimused** ostutellimus ja seejärel valige tegevuspaanil vahekaardil **Vastuvõtmine** suvand **Toote kviitung**, et avada leht **Toote kviitungi tööleht**. Igale reale luuakse operatsiooni sündmus ja Global Inventroy Accounting sündmus. Seepärast valige vahekaart **Read** ja seejärel valige **Ladu \> Sündused ja mõõtmised**, et avada leht **Sündmused ja mõõtmised**.

Global Inventory Accounting on sündmustel ja mõõtmistel põhinev raamatupidamissüsteem. **Sündmuste ja mõõtmiste** lehel kuvatakse mõõtmisterea võrgustikul mõõtmiste loend. Igal mõõtmisel on dimensioonide loend.

Iga töösündmuse puhul on kaks mõõtmise tüüpi:

- **Töömõõtmised** – need mõõtmised kirjeldavad äridokumente üldises mõistes. Üks mõõtmine on toote kogus kasutades dokumendis kirjeldatud mõõtühikuid. On ka mõõtmisi, mis mõjutavad laoväärtust, nt laiendatud hind, allahindlus, allahindluse protsent ja rea tasu.
- **Ressursi arvestusmõõtmised** – need mõõtmised on pärit laoregistri perspektiivist. Need kirjeldavad dokumendi mõju laovarudele varude mõõtühiku järgi. Kui laoregistreerimisi on mitu, on ressursiarvestuse mõõtmistel mitu rida.

Dimensioonid on korraldatud järgmiselt:

- **Duaalsus** – see kirjeldab agente, kes osalevad majandussündmustel. Välised äridokumentide puhul kirjeldavad esmadimensioonid juriidilist isikut, kuhu dokument sisestatakse, samas kui duaalsed dimensioonid kirjeldavad hankijat, klienti jne. Sisemiste äridokumentide (nt üleviimistellimused) puhul kirjeldavad duaalsed dimensioonid vastasladu.
- **Dimensiooni tüüp** – dimensioonitüübid liigitavad dimensioone.
- **Dimensioon** - dimensiooni nimi.
- **Dimensiooni väärtus** - dimensiooni väärtus.

### <a name="global-inventory-accounting-event"></a>Global Inventory Accounting sündmus

Global Inventory Accounting võtab sisendina tegevussündmused ja mõõtmised. Siis on vajalik iga seotud pearaamatu raamatupidamine, mis põhineb seotud valuutal ja konventsioonil. Global Inventory Accounting sündmuse vaatamiseks saate valida **Globaalse laoarvestuse sündmused ja mõõtmised**. Global Inventory Accounting sündmus järgib sama metodoloogiat nagu töösündmused, kuid kasutab erinevaid mõõtmisi. On kolm peamist mõõtmise tüüpi: toote omahind, toote kulu ja dispersioon.

Alampearaamatu kontosid kasutatakse mõõtmiste edasiseks klassifitseerimiseks. Võib olla mitu pearaamatut. Need pearaamatud on seotud juriidilise isikuga, kuhu dokument sisestatakse. Iga pearaamatu sündmuste ja mõõtmiste vaatamiseks saate muuta välja **Pearaamat** väärtust.

### <a name="cost-element"></a>Kuluelement

Pearaamatuga seotud kuluelemendi poliitika alusel määrab süsteem kuluelemendi igale inventeeritud töösündmuse mõõtmisele, mis mõjutab varude kulu. Need mõõtmised hõlmavad laiendatud hinda, allahindlust, allahindluse protsenti ja rea hinda.

### <a name="measurement-line-details"></a>Mõõtmise rea üksikasjad

Vahekaart **Ülevaade** näitab seotud poliitikate üksikasju. Kuluobjekti dimensioonid näitavad kuluobjekti poliitikal põhinevat kuluobjekti. Kindlate identifitseerimise dimensioonide puhul kuvatakse partiinumber, kui kuluvoo eelduseks on *Kindel – partii*.

### <a name="purchase-invoice"></a>Ostuarve

Pange arve üles tavalisel viisil. Seejärel valige tegevuspaani vahekaardil **Arve** grupis **Töölehed** **Arve**, et avada arve tööleht. Igale reale luuakse operatsiooni sündmus ja Global Inventory Accounting sündmus. Seepärast valige vahekaart **Read** ja seejärel valige **Ladu \> Sündused ja mõõtmised**, et avada leht **Sündmused ja mõõtmised**. **Sündmuste ja mõõtmiste** lehel kuvatakse sama mõõtmise tüüp. Kuna lehel kuvatakse erinev mõõdu roll ja mõõdu muutja, on mõju agendile (juriidiline isik) erinev.

Global Inventory Accounting sündmuse vaatamiseks valige **Globaalse laoarvestuse sündmused ja mõõtmised**. Varude kogus ja kulu voogu nüüd saadud *kaupade arveldamata varude* alampearaamatu kontolt ja alampearaamatu kontole *Ostetud kauba kulu*.
