---
title: Sisestamisdefinitsiooni näited
description: Selles artiklis on näited selle kohta, kuidas ostutellimuse pandiõiguse ja eelarve jaotamise puhul sisestamisdefinitsioone kasutatakse.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6b2b505acb211f9fb5506234953eba9f3ec2a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865768"
---
# <a name="posting-definition-examples"></a>Sisestamisdefinitsioonide näited

[!include [banner](../includes/banner.md)]

Selles artiklis on näited selle kohta, kuidas ostutellimuse pandiõiguse ja eelarve jaotamise puhul sisestamisdefinitsioone kasutatakse.

Enne selle artikli lugemist peaksite tutvuma sisestamisdefinitsioonide ja kande sisestamisdefinitsiooniga. Lisateavet vaadake teemast [Sisestamisdefinitsioonid](posting-definitions.md). Lehel **Sisestamisdefinitsioonid** saate seadistada järgmised näited. Iga näide sisaldab järgmisi jaotisi.

-   Sisestamisdefinitsioon – vastendamise kriteeriumid
-   Sisestamisdefinitsioon – loodud kanded
-   Kontode, dimensiooniväärtuste ja summadega kanded
-   Sisestamisdefinitsioonist loodud pearaamatukirjed

Kui sisestamisdefinitsiooni paanil **Vastendamiskriteeriumid** olevate kontode ja dimensiooniväärtuste ning kande kontode ja dimensiooniväärtuste vahel ilmneb vastendus, luuakse pearaamatukirjed sisestamisdefinitsiooni paani **Loodud kanded** alusel. 
> [!NOTE]
> Sisestamisdefinitsiooni saab seostada konkreetse kande tüübiga lehel **Kande sisestamisdefinitsioonid**. Pärast sisestamisdefinitsiooni seostamist kande tüübiga ja valiku **Kasuta sisestamisdefinitsioone** tegemist lehel **Pearaamatu parameetrid** peavad kõik valitud kande tüübiga kanded kasutama sisestamisdefinitsioone.

## <a name="example-purchase-order-encumbrances"></a>Näide: ostutellimuse pandiõigus
Kui lubate pandiõiguse protsessi, valides lehel **Pearaamatu parameetrid** suvandi **Luba pandiõiguse protsess**, tuleb pandiõiguste pearaamatusse kandmiseks kasutada kõigi reserveeritavate kontode puhul sisestamisdefinitsioone. Enamasti reserveeritakse bilansis kõik kulukontod. 

Pandiõiguste sisestamisdefinitsioonid seadistatakse mooduli **Ostmine** jaoks lehel **Sisestamisdefinitsioonid**. Seejärel saate lehe **Kande sisestamisdefinitsioonid** alal **Ostmine** valida kandetüübi **Ostutellimus**, et seostada sisestamisdefinitsiooni ostutellimustega. 

Kõik ostutellimuse pandiõiguste pearaamatukanded peavad olema tasakaalus (st deebetid peavad võrduma kreedititega) kande igas kordumatus dimensioonis.

### <a name="posting-definition--match-criteria"></a>Sisestamisdefinitsioon – vastendamise kriteeriumid

| Konto struktuur       | Kattuva konto number | Prioriteet  |
|-------------------------|----------------------|----------|
| Konto struktuur – kasum ja kahjum | \*                   | 1        |

<em>Tühi väärtus väljal **Kattuva konto number</em>* tähendab, et kõik kattuvad kontod määratletud kontostruktuuris on vastendusreegli osa.

### <a name="posting-definition--generated-entries"></a>Sisestamisdefinitsioon – loodud kanded

| Konto struktuur | Loodud konto number                    | Loodud deebet/kreedit |
|-------------------|---------------------------------------------|------------------------|
| Saldo           | 300143 – (pandiõiguse konto)             | Sama                   |
| Saldo           | 300144 – (pandiõiguse konto reserveerimine) | Tasakaalustamine              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Kontode, dimensiooniväärtuste ja summadega kanded

Kontod ja dimensiooniväärtused tulevad kas ostutellimuse reale sisestatud arvestuse jaotustelt või hankijate, kaupade, kategooriate ja dimensioonimallide vaikesätete põhjal automaatselt loodud kontodest ja dimensioonidest.

| Konto + dimensioonid           | Debiteeri  | Krediit | Kommentaar |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Training | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Sisestamisdefinitsioonist loodud pearaamatukirjed

Genereeritud pearaamatukirjed luuakse pandiõiguste registreerimiseks.

| Konto + dimensioonid           | Debiteeri  | Krediit | Kommentaar |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Training | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Training |        | 250,00 |         |

Selles näites vastab iga konto, mis on osa jaotisest Konto struktuur – kasum ja kahjum, sisestamisdefinitsiooni kriteeriumitele. Üksuse 606500-OU\_1-OU\_3566-Training hindamisel luuakse seega genereeritud kirjed kontode kohta, mis on määratletud sisestamisdefinitsiooni paanil **Loodud kirjed**.

## <a name="example-budget-appropriations"></a>Näide: eelarveeraldised
Kui lubate eelarveeraldise, valides lehel **Pearaamatu parameetrid** suvandi **Luba eelarveeraldis**, tuleb eelarve registrikirjete registreerimiseks pearaamatusse kasutada sisestamisdefinitsioone. Kui eelarve juhtimise konfiguratsioon on aktiivne ja sisse lülitatud, saab sisestamisdefinitsioone ja kande sisestamisdefinitsioone kasutada eraldiste, paranduste, ülekannete, projektide, põhivarade ning tarne- ja nõudlusprognooside kirjete pearaamatusse registreerimise toetamiseks. 

Selleks et seadistada sisestamisdefinitsioon eelarve registrikannete jaoks, mille eelarvetüüp on **Algne eelarve** ja mille puhul on eraldised lubatud, valige lehel **Sisestamisdefinitsioonid** moodul **Eelarve**. Seejärel saate lehe **Kande sisestamisdefinitsioonid** alal **Eelarve** kasutada eelarvekoode, et seostada sisestamisdefinitsioonid eelarve registrikannetega, mille eelarvetüüp on **Algne eelarve**. 

Kui eelarveeraldised ja sisestamisdefinitsioonid on lubatud, registreeritakse eelarve registrikirjed eelarve juhtimisse ja pearaamatusse.

### <a name="posting-definition--match-criteria"></a>Sisestamisdefinitsioon – vastendamise kriteeriumid

| Konto struktuur       | Kattuva konto number | Prioriteet  |
|-------------------------|----------------------|----------|
| Konto struktuur – kasum ja kahjum | \*                   | 1        |

<em>Tühi väärtus väljal **Kattuva konto number</em>* tähendab, et kõik kattuvad kontod määratletud kontostruktuuris on vastendusreegli osa.

### <a name="posting-definition--generated-entries"></a>Sisestamisdefinitsioon – loodud kanded

| Konto struktuur | Loodud konto number              | Loodud deebet/kreedit |
|-------------------|---------------------------------------|------------------------|
| Konto struktuur | 300145 – (eeldatava tulu konto) | Sama                   |
| Konto struktuur | 300146 – (eraldisekonto)     | Tasakaalustamine              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Kontode, dimensiooniväärtuste ja summadega kanded

Saate sisestada kontod, dimensiooniväärtused ja eelarve konto kirje summad lehel **Eelarve registrikirje**.

| Konto + dimensioonid           | Debiteeri | Krediit | Kommentaar |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Training |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Sisestamisdefinitsioonist loodud pearaamatukirjed

Genereeritud pearaamatukirjed luuakse algse eelarve registreerimiseks igas dimensioonis.

| Konto + dimensioonid           | Debiteeri  | Krediit | Kommentaar |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Training |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Training | 250,00 |        |         |

Selles näites vastab iga konto, mis on osa jaotisest Konto struktuur – kasum ja kahjum, sisestamisdefinitsiooni kriteeriumitele. Üksuse 606400-OU\_1-OU\_3566-Training hindamisel luuakse seega genereeritud pearaamatukirjed.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
