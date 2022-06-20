---
title: Tarbijahinnaindeksi graafik
description: See artikkel selgitab, kuidas luua tarbijahinna indeksi (CPI) graafikute loend, mida saate Internetist, et määrata kordustellimuse arvelduses laiendustasu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904869"
---
# <a name="consumer-price-index-schedule"></a>Tarbijahinnaindeksi graafik

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas luua, kustutada, üle vaadata ja töödelda tarbijahinna indeksi (CPI) plaane. CPI graafikut saab kasutada arveldusgraafiku ridadena lisatavate tarbekaupade ja teenuste hindade määramiseks. CPI graafikut saab seejärel kasutada koos laienduse ja allahindluse hinnakujundusega arveldusgraafikul või saab seda käsitsi töödelda arveldusgraafiku arveldussummade värskendamiseks. Saate sisestada CPI-graafikud käsitsi või importida neid CPI-graafiku liitüksuse abil.

CPI-graafiku lisamiseks järgige neid samme.

1. Valige tarbijahinna **indeksi graafiku** lehel **uus**.
2. Sisestage **väljale Tarbijahinna indeksi** graafik kordumatu nimi.
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. Valige vahekaardil **Tarbijahinna indeksi** graafik suvand **Lisa**.
5. Määrake väljal **Tarbijahinna indeks** kuupäev kuupäev, mil uus CPI graafik muutub aktiivseks.
6. Sisestage **väljale Tarbijahinna indeksi** graafik sammus 2 sisestatud nimi.
7. Valige käsk **Salvesta**.

CPI graafiku kuupäeva kustutamiseks järgige neid samme.

1. Valige tarbijahinna **indeksi** graafiku lehel üks või mitu rida, mida soovite kustutada, ja valige käsk **Eemalda**.
2. Kogu CPI-graafiku kustutamiseks klõpsake tegevuspaanil käsku **Kustuta**. Te ei saa valitud CPI-graafikut kustutada, kui see on seostatud mis tahes arveldusgraafikuga.
3. Tegevuspaanil valige suvand **Protsess** valitud CPI-graafikuid kasutav arveldusgraafikute värskendamiseks. Arveldusgraafiku hindade värskendamiseks kasutatakse viimaseid CPI kuupäevi ja graafiku summasid.
4. Tarbijahinna **indeksi protsessi** kiirkaardil **vaadake üle värskendatud arveldusgraafiku number**, **kaubakood**, arvelduse alguskuupäev, **arvelduse** lõppkuupäev, **·** **laienduskuupäev** **ja laiendussagedusväljad.**

Pärast CPI graafikute seadistamist saab neid kasutada arveldusgraafikute laiendus- ja allahindlushindade muudatusteks.

## <a name="cpi-calculation"></a>CPI arvutamine

Nende näidete puhul on periood 1. jaanuar 2020 kuni 31. detsember 2022. CPI alusmäär (CPI väärtus lepingu käivitamisel) on 105,65. 1. jaanuaril 2021 on praegune CPI 110,5. 1. jaanuaril 2022 on praegune CPI 114,25. Algsumma on $1,000.

**Näide 1**

Korduva lepingu **arveldusparameetrite lehel seate** tarbija hinnaindeksi **arvutamise välja väärtuseks** Baaskliendi **hinnaindeks**.

1. jaanuari 2021 puhul arvutatakse esimene laiendussumma algsumma põhjal järgmiselt:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1,000 = 1 045,91

1. jaanuari 2022 perioodi laiendussumma arvutatakse järgmiselt:

1000 + (114,25 – 105,65) &divide; 105,65 &times; 1,000 = 1 081,40

**Näide 2**

Korduva lepingu **arveldusparameetrite lehel seate** välja Tarbija hinnaindeksi **arvutamine väärtuseks** Enne **tarbimishinna indeksit**.

1. jaanuari 2021 puhul arvutatakse esimene laiendussumma algsumma põhjal järgmiselt:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1,000 = 1 045,91

1. jaanuari 2022 perioodi laiendussumma arvutatakse esimesel laiendussummal põhinevalt järgmiselt:

1045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1,045,91 = 1 081,40

> [!NOTE]
> Eskaleerimine kasutab alati viimast CPI väärtust, olenemata indeksi kuupäevast. Näiteks kui laiendus on septembris, kuid CPI viimane väärtus on juuli, kasutatakse juuliindeksit. Pärast septembriindeksi sisestamist ei korrigeerita.

## <a name="prorated-escalation"></a>Plussidunud eskaleerimine

Kui eskaleerimine toimub arveldusperioodi keskel, on summa ergastatud. Arveldusperiood on näiteks 1. august 2020 – 31. juuli 2021. CPI kuupäeva 1. septembril 2019 on CPI väärtus 244. CPI kuupäeval 1. septembril 2020 on see CPI väärtus 250. Kui eelmine määr on 1000, kasutatakse arveldussumma arvutamiseks perioodi jooksul järgmisi valemeid:

* *CPI muudatused* = (250 – 244) &divide; 244 = 2,459%
* *Praegune määr* = 1000 &times; 2,459% = 1024,59
* *Päevade arv praeguse* määraga = 31. juuli 2021 – 1. september 2020 = 334
* *Eelmine määr* = 1000
* *Päevade arv eelmises määras* = 31. august 2020 – 1. august 2020 = 31. august
* *Arveldusperioodi päevade* koguarv = 31. juuli 2021 – 1. august 2020 + 1 = 365.
* *Selle perioodi arveldussumma* = (1000 &times; 31 &divide; 365) + (1024,59 &times; 334 &divide; 365) = 1022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Laiendamine, mis kasutab CPI-d ja protsenti

Laiendamist saab teha CPI-d kasutades. CPI pluss 3-protsendiline laiendus algab 1. jaanuaril 2020 ja sellel on iga-aastane sagedus.

- Summa, mis on esitatud 1. jaanuarile 2019 kuni 31. detsembrini 2020, on 4000.
- Laiendamist vajav arveldusperiood on 1. jaanuar 2020 kuni 31. detsember 2020.
- CPI kuupäeva 1. detsembril 2018 on CPI väärtus 205,3. CPI kuupäeva 1. detsembril 2019 on CPI väärtus 219,6.

Kui eelmine määr on 4000, arvutatakse selle perioodi arveldussumma järgmiselt:

- *CPI muudatused* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Praegune määr* = (4000 &times; 6,965%) – 4000 = 278,60.
- *Protsentuaalsed* muutused = (4000 &times; 1,03) – 4000 = 120
- *Arveldussumma* = 4000 + 278,6 + 120 = 4398,6
