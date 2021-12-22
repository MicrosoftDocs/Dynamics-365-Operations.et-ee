---
title: Saate häälestada maksukoode.
description: See teema kirjeldab, kuidas maksukoode maksuarvutusteenuses seadistada.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883898"
---
# <a name="set-up-tax-codes"></a>Saate häälestada maksukoode.

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas maksukoode maksuarvutuse teenuses seadistada. See sisaldab lihtsa stsenaariumi seadistust, et maksukoodi tööd teha ja teavet kompleksstsenaariumide täpsemate maksukoodide funktsioonide kohta.

> [!IMPORTANT]
> Maksukoodide seadistus maksuarvutuse teenuses on juriidiline isik -prognoositav. Selle seadistuse saate lõpetada regulatiivses konfiguratsiooniteenuses (RCS) ainult üks kord. Maksukoodid sünkroonitakse Microsoftiga automaatselt, kui lubate finantsis valitud Dynamics 365 Finance juriidilisele isikule maksu arvutamise teenust.

## <a name="simple-setup"></a>Lihtseadistus

Järgige neid samme, et kasutada maksukoodi lihtsas stsenaariumis, nt stsenaariumis, kus on ainult üks maksumäär.

1. Logige sisse [regulatiivsesse konfigureerimisteenusesse](https://marketing.configure.global.dynamics.com/).
2. Minge **tööruumide** \> **globaliseerimisfunktsiooni** \> **maksuarvutusse.**
3. Valige funktsioon ja versioon, mida soovite seadistada, ning valige käsk **Redigeeri**.
4. Vahekaardil **Üldine** valige **konfiguratsiooni** versioon.
5. Vahekaardil **Maksukoodid** valige **Lisa** ning sisestage maksukood ja kirjeldus.
6. Valige **arvutuse päritolu**. Arvutuse päritolu on valitud maksukonfiguratsiooni versioonis määratletud meetodite grupp. Valige selle lihtstsenaariumi **puhul netosumma järgi**.
7. Valige käsk **Salvesta**. Vastavalt valitud kalkulatsiooni päritolule muutuvad kättesaadavaks veel välju.
8. Valige **kiirkaardil** Määrad **suvand** Lisa, et lisada sellele maksukoodile üks maksumäär.
9. Valige käsk **Salvesta**.

## <a name="calculation-origin"></a>Arvutuse päritolu

Arvutuse päritolu määratleb, kuidas maksu baassummat ja maksusummat arvutatakse. See on konfigureeritud maksukonfiguratsiooniga elektroonilise aruandluse **tööruumis**. Kalkulatsiooni alusväljal on **saadaval järgmised** väärtused:

- netosumma järgi
- brutosumma järgi
- Koguse järgi
- Marginaali järgi
- Maks maksult

### <a name="by-net-amount"></a>netosumma järgi

Kui valite väljal Arvutuse alus netosumma, arvutatakse maksusumma protsendina ostu- või **·** **müügisummast**, jättes muud maksukoodid välja.

Näiteks maksumääraks on 25 protsenti, arve real kuvatakse 10 kauba kogus 1,00 igaüks ja kliendile lubatakse 10-protsendiline rea allahindlus. Sellisel juhul arvutatakse summad järgmiselt:

- **netosumma:** (10 × 1,00) – 10 protsenti = 9,00, 
- **Käibemaks:** 9,00 × 25 protsenti = 2,25 
- **Arve kogusumma:** 9,00 + 2,25 = 11,25.

### <a name="by-gross-amount"></a>brutosumma järgi

Kui **valite väljal** Arvutuse alus **brutosumma**, arvutatakse maksusumma protsendina müügi brutosummast. Brutosumma on rea netosumma pluss kõik rea maksud ja tasud, v.a üks maks, kus välja Arvutuse alus väärtuseks **on** seatud **Brutosumma**.

Näiteks on maksuamet kehtestatud kaubale erimaksud. Maksusummad lisatakse netosummale enne maksu arvutamist. Kasutatakse järgmisi maksukoode:

- **Maks 1** – määr on 10 protsenti ja **kasutatakse netosumma arvutamise** meetodit.
- **Maks 2** – määr on 20 protsenti ja **kasutatakse netosumma arvutamise** meetodit.
- **Maksumäär** – määr on 25 protsenti ja kasutatakse **brutosumma** arvutamise meetodit.

Kui netosumma on 10,00, on maksu 1 summa 1.00 (10.00 × 10 protsenti) ja maksu 2 summa 2.00 (10.00 × 20 protsenti). Sellisel juhul arvutatakse summad järgmiselt: 

- **brutosumma: netosumma + maksu** 1 summa + maksu 2 summa = 10,00 + 1,00 + 2,00 = 13,00, 
- **Maksusumma:** 13,00 × 25 protsenti = 3,25 
- **kogumaksud ja** -maks: 1,00 + 2,00 + 3,25 = 6,25, 
- **Arve kogusumma:** 10,00 + 6,25 = 16,25.

### <a name="by-quantity"></a>Koguse järgi

Kui valite väljal Arvutuse alus koguse, arvutatakse maksusumma fikseeritud summana ühiku kohta ja korrutatakse **dokumendireale** **sisestatud** kogusega. Summa ühiku kohta on määratud **kiirkaardil** Määrad.

Näiteks on maksukoodiks seadistatud 1,20 ühiku kohta. Müügiarve real müüakse 25 kaubaühikut. Sellisel juhul arvutatakse maksusumma 25,00 × 1,20 = 30,00.

### <a name="by-margin"></a>Marginaali järgi

Kui **valite** marginaali **alusel väljal Arvutuse** alus, arvutatakse maksusumma protsendina müügimarginaalist. Müügimarginaal on müügisumma miinus omahind. Seda arvutusmeetodit rakendatakse ainult müügikannete puhul.

Näiteks maksumääraks on 25 protsenti, arve real kuvatakse 10 kauba kogus 10,00 ühiku kohta ja kauba kulu on 6. Sellisel juhul arvutatakse summad järgmiselt:

- **Müügimarginaal:** 10 × (10,00 – 6,00) = 40,00
- **Maksusumma:** 40,00 × 25 protsenti = 10,00
- **Arve kogusumma:** 100,00 + 10,00 = 110,00.

### <a name="tax-on-tax"></a>Maks maksult

Kui valite maksult väljal Arvutuse alus, arvutatakse käibemaks protsendina sama dokumendirea kõikidest **teistest** **maksusummadest**.

Kasutatakse näiteks järgmisi maksukoode:

- **Maks 1** – määr on 10 protsenti ja **kasutatakse netosumma arvutamise** meetodit.
- **Maks 2** – määr on 20 protsenti ja **kasutatakse netosumma arvutamise** meetodit.
- **Maks** tollilt – määr on 25 protsenti ja **kasutatakse** maksuarvutusmeetodit.

Sellisel juhul arvutatakse summad järgmiselt:

- **Netosumma:** 10,00 
- **Maks 1:** 10,00 × 10 protsenti = 1,00, 
- **maks 2:** 10,00 × 20 protsenti = 2,00, 
- **Maks maksult:** 3,00 × 25 protsenti = 0,75
- **Käibemaks kokku:** 1,00 + 2,00 + 0,75 = 3,75. 
- **Arve kogusumma:** 10,00 + 3,75 = 13,75.

## <a name="advanced-functionality"></a>Täpsemad funktsioonid

See jaotis selgitab kompleksstsenaariumide maksukoodi häälestuse mõningaid täpsemaid funktsioone.

### <a name="tax-exemption"></a>Maksuvabastus

Kui seate kiirkaardil Üldine valiku Maksuvabastus väärtuseks Jah, alistatakse maksusumma **alati** **·** **0 (null) hoolimata tegelikust** maksumäärast.

Saate seada **maksuvabastuse** põhjuse määramiseks maksuvabastuse koodi välja. 

Saate lubada koondandmete otsingu vabastatud **koodi** väljal. Sel viisil saate valida finantsis määratletud maksuvaba koodi väärtuste hulgast. Lisateavet koondandmete otsingu lubamise kohta vt [maksuarvestuse konfiguratsiooni jaoks koondandmete otsingu](tax-service-set-up-environment-master-data-lookup.md) lubamine.

Näiteks on maksumääraks 25 protsenti ja maksukoodil on **maksuvabastuse** suvandi **väärtuseks** seatud Jah. Arve real kuvatakse kogus 10 üksust 1,00-st igaüks ja kliendile on lubatud 10-protsendine rea allahindlus. Sellisel juhul arvutatakse summad järgmiselt:

- **netosumma:** (10 × 1,00) – 10 protsenti = 9,00, 
- **Käibemaks:** 0,00 
- **Arve kogusumma:** 9,00 + 0,00 = 9,00.

### <a name="use-tax"></a>Kasutusmaks

Kui seate kiirkaardil Üldine valiku Kasutusmaks väärtuseks Jah, sisestatakse maksusumma hankija summakonto asemel **kasutusmaksu** **·** **·** **·** **makstavale** kontole.

Näiteks on maksumääraks 25 protsenti ja maksukoodil on valik Kasutusmaks **seatud** **väärtusele** Jah. Arve real kuvatakse kogus 10 üksust 1,00-st igaüks ja kliendile on lubatud 10-protsendine rea allahindlus. Sellisel juhul arvutatakse summad järgmiselt:

- **netosumma:** (10 × 1,00) – 10 protsenti = 9,00, 
- **Kasutusmaks:** 9,00 × 25 protsenti = 2,25
- **Arve kogusumma:** 9,00 + 0,00 = 9,00.

> [!IMPORTANT]
> Kui nii suvand On vabastus kui ka valik Kasutusmaks on maksukoodis seatud väärtusele Jah, tuvastatakse kood müügikannete puhul maksuvabana ja kasutatakse ostukannete **puhul** **·** **maksu**.

### <a name="reverse-charges"></a>Pöördtasud

Kui seate kiirkaardil Üldine valiku Pöördtasu väärtuseks Jah, saab **maksumäära konfigureerida** **·** **negatiivsena**. Pöördtasu stsenaariumi puhul on soovitatav seadistada kaks maksukoodi: üks, mille maksumäär on positiivne ja teine, mille maksumäär on negatiivne. Mõlemal maksukoodil peab olema sama määra väärtus ja negatiivse maksumääraga maksukoodi puhul tuleb suvand **On Pöördtasu** seada **väärtusele** Jah. Lisateavet finantsis pöördtasu lahenduse kohta vt [Pöördtasu mehhanism VAT/GST skeem](emea-reverse-charge.md).

Näiteks määratletakse kaks maksukoodi ühel arvereal. Üks maksumäär on 25 protsenti. Muu maksumäär on -25 protsenti ja suvand On Pöördtasu on seatud **teise** **maksukoodi** puhul väärtusele Jah. Arve real kuvatakse kogus 10 üksust 1,00-st. Sellisel juhul arvutatakse summad järgmiselt:

- **netosumma:** (10 × 1,00) = 10,00, 
- **Maksukood 1:** 10,00 × 25 protsenti = 2,50
- **Maksukood 2:** 10 × -25 protsenti = -2,50
- **Arve kogusumma:** 10,00 + 2,50 -2,50 = 10,00.

### <a name="exclusion-from-base-amount-calculations"></a>Baassumma arvutustest väljajätmine

Kui seate kiirkaardil Üldine suvandi Välista baassumma arvutamisest valikule Jah, jäetakse maksukoodi arvutatud maksusumma maksu baassummast välja muude maksukoodi arvutuste jaoks hinnas **kaasatavas** **·** **stsenaariumis**.

Lisateavet vt hindade maksu [arvutamisest, kui hinnad sisaldavad makse on](global-exclude-from-tax-base-amount-calculation.md) lubatud.

### <a name="rates"></a>Määrad

**Kiirkaardil Määr saate maksu** baassummade erinevate vahemike jaoks määratleda erinevaid maksumäärasid. Maksusumma arvutamiseks kasutab maksuarvestuse teenus alati määra, mis vastab maksu baassummale.

Näiteks võib maksumäärad konfigureerida nii, nagu näidatud järgmises tabelis.

| Vähim summa | Maksimaalne summa | Maksumäär   |
| -------------- | -------------- | ---------- |
| 0              | 1000          | 10 protsenti |
| 1000          | 5000          | 15 protsenti |
| 5000          | 10,000         | 20 protsenti |
| 10,000         | 0              | 30 protsenti |

Sellisel juhul arvutatakse maksusumma järgmiselt:

- Kui maksu baassumma on 300,00, siis on maksumäär 10 protsenti ja maksusumma on 300,00 × 10 protsenti = 30,00.
- Kui maksu baassumma on 3000,00, siis on maksumäär 15 protsenti ja maksusumma on 3000,00 × 15 protsenti = 450,00.
- Kui maksu baassumma on 6000,00, siis on maksumäär 20 ja maksusumma 6000,00 × 10 protsenti = 1200,00.
- Kui maksu baassumma 20,000.00, siis on maksumääraks 30 protsenti ja maksusumma 30 20,000.00 × = 6000,00.

> [!NOTE]
> Kui maksu baassumma võib ühtima nii ühel real oleva maksimumsumma kui ka teisel real oleva miinimumsummaga, kasutab alus maksumäära, mis vastab minimaalsele baassummale. Näiteks kui maksu baassumma on 1000,00, siis on maksumäär 15 protsenti ja maksusumma on 1000,00 × 15 protsenti = 150,00.

### <a name="limits"></a>Limiidid

Kiirkaardil Limiidid saate määrata maksulimiidid arvutatud maksusumma alistamiseks, kui maksusumma langeb **miinimum**-/maksimumvahemikku.

- Kui arvutatud maksusumma on suurem kui maksimaalne maksusumma, mis on konfigureeritud kiirkaardil Piirangud, võrdub lõplik maksusumma **maksimaalse** maksusummaga.
- Kui arvutatud maksusumma on väiksem kui minimaalne maksusumma, mis on konfigureeritud kiirkaardil Limiidid, on **lõplik** maksusumma 0 (null).

Näiteks maksulimiidid konfigureeritakse järgmiselt:

- **Minimaalne maksusumma:** 100 
- **Maksimaalne maksusumma:** 1000

Kui arvutatud maksusumma on 2000, on lõplik maksusumma 1000.

Kui arvutatud maksusumma on 500, on lõplik maksusumma 500.

Kui arvutatud maksusumma on 80, on lõplik maksusumma 0 (null).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
