---
title: Laokoguste reserveerimine
description: Selles teemas kirjeldatakse erinevaid varude reserveerimiseks saadaolevaid suvandeid.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cf6f14e30f84f48428b351287eb1c65915a14c1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571133"
---
# <a name="reserve-inventory-quantities"></a>Laokoguste reserveerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse erinevaid varude reserveerimiseks saadaolevaid suvandeid.

Laokoguseid saab kindlate müügitellimuste jaoks automaatselt reserveerida. See tähendab, et reserveeritud kaubavaru ei saa laost teiste tellimuste jaoks võtta ilma kaubavarude reserveeringu täieliku või osalise tühistamiseta.

Varude reserveerimiseks on mitu põhjust.
-   Esimesena tellitud ja esimesena tarnitud, mis tähendab seda, et kliendid saaksid saadaolevad kaubad kätte tellimuste esitamise järjekorras.
-   Kaupade puudus pikkade või teadmata hankijapoolsete tarneaegade tõttu. Võib-olla soovite tagada, et kindlate klientide või tellimuste tarnitakse esimeste saadaolevate kaupadega.
-   Teatud kliendid, tellimuste tüübid jne on tarnimisel eelistatud.
-   Seeria- või partiinumbritega kaubad. Saate märkida kindlad kaubad, mis on tarnitud või tarnitakse kindlate tellimuste jaoks.
-   Eritellimusega kaubad, mis on reserveeritud kindlate tellimuste jaoks.
-   Tootmistellimused. Näiteks saate märkida kaubad, mis on toodetud ja kohandatud kindlate tellimuste jaoks.

Varusid saab uue tellimuserea loomisel automaatselt reserveerida või igal üksikul tellimusel käsitsi reserveerida. Varusid on võimalik reserveerida tootmisprotsessis erinevates etappides. Ainult ladustatavaid tooteid saab reserveerida. Teenuseid ei saa reserveerida, sest nende puhul ei ole olemas vabu kaubavarusid. Reserveerida saab nii füüsiliselt vabu kaubavarusid kui ka tellitud, kuid veel kätte saamata kaubavarusid. Kui reserveeritakse vabadest kaubavarudest suurem kogus, kuvatakse hoiatus, et nii suurt kogust ei saa reserveerida. Sel juhul valige, kas reserveerite koguse sellest hoolimata või muudate tellitud kogust. Kogust saab reserveerida või muuta. Kui kaupu reserveeritakse rohkem, kui neid on saadaval, kaetakse tekkiv puudujääk järgmisel korral, kui kaubad on tarnimiseks saadaval.

## <a name="inventory-reservation-policies"></a>Varude reserveerimise poliitikad
Varude reserveerimise poliitikad määratakse lehel **Kauba mudeligrupid**, lehel **Varude ja laohalduse parameetrid** ja lehel **Tootmise parameetrid**.
### <a name="policies-on-the-item-model-groups-page"></a>Poliitikad kaubamudeli gruppide lehel

Jaotis **Varude poliitikad** sisaldab järgmiseid reserveerimispoliitikaid.

| &nbsp;                  | &nbsp;                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reserveerimispoliitika**  | **Kirjeldus**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO kuupäevakontrolliga    | Kui valite suvandi **FIFO kuupäevakontrolliga**, kontrollitakse varude reserveerimist FIFO põhimõtte järgi sortimiskuupäevaga. Partiid reserveeritakse kaupade sissetuleku varaseima kuupäeva põhjal esimese sissetuleku, esimese väljamineku (FIFO) põhimõtte järgi.                                                                                                                                                                                                                                                                       |
| Lähetuskuupäevast tagasi | See suvand muutub kättesaadavaks, kui valisite suvandi **FIFO kuupäevakontrolliga**. Kui valite **Lähetuskuupäevast tagasi**, reserveeritakse varusid soovitud lähetuskuupäevast tagasi LIFO-põhimõtte järgi (viimasena sisse, esimesena välja). Kui enne lähetuskuupäeva ei ole ühtegi sissetulekut saadaval, kasutatakse FIFO reserveerimist.                                                                                                                                                                                                           |
| Kauba müügireserveering  | Määrab, kas kauba reserveerimine on manuaalne või automaatne. Kui reserveerimine on automaatne, reserveeritakse varud tellimusridade loomisel. On võimalik teha reserveeringuid koosluste kaubakoodi tasemel (suvand **Automaatne**) või koosluse individuaalsete elementide tasemel (suvand **Koosnevus**). Valiku **Kauba müügireserveering vaikeväärtus** päritakse lehelt **Müügireskontro parameetrid** Sellel lehel määratakse väärtus vahekaardil **Üldine** **jaotise** **Müügi vaikeväärtused** väljal Reserveerimine. |
| Sama partii valimine    | Sama partii reserveerimisel saate reserveerida müügitellimuse rea varusid ühe varupartii suhtes. Kui soovite seda suvandit kasutada, peate määrama ka suvandi **Konsolideeri vajadus** väärtusele **Jah**. On täiendavad sätted, mis on vajalikud jälgimisdimensiooni grupi ja laoala dimensiooni grupi jaoks. Lisateabe saamiseks vaadake [Sama partii reserveerimine müügitellimuse jaoks](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Konsolideeri vajadus | See suvand on sarnane suvandile **Sama partii valimine** ja see konsolideerib varud, mis reserveeris müügitellimuse read üheks nõudeks.                                                                                                                                                                                                                                                                                                                                                                                      |
| FEFO kuupäevakontrolliga    | See suvand võimaldab teil reserveerida partiid, mis on sarnased nende aegumiskuupäevale või parim enne kuupäevale. Samuti peate määrama välja **Komplekteerimise kriteeriumid**, et valida **Aegumiskuupäev** või **Parim enne kuupäev**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Näide suvanditele FIFO kuupäevakontrolliga ja Lähetuskuupäevast tagasi

Selles näites eksisteerivad vabad kaubavarud kaubakoodi A puhul kolme erineva partii numbri jaoks.

| Kaubakood | Partii number | Kogus | Kuupäev             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5        | 2. veebruar 2016 |
| A           | 1001         | 3        | 1. jaanuar 2016  |
| A           | 1002         | 7        | 3. märts 2016    |

Müügitellimus, mille puhul tuleb kasutada automaatset reserveerimist ja mis peab olema tarnitud 4. aprilliks 2016, reserveerib järgmise partii:
-   Kui tühjendatakse märkeruudud **FIFO kuupäevakontrolliga** ja **Lähetuskuupäevast tagasi**, reserveeritakse partii 1000, kuna see on kõige madalama numbriga partii.
-   Kui märkeruut **FIFO kuupäevakontrolliga** on valitud ja märkeruut **Lähetuskuupäevast tagasi** tühjendatud, reserveeritakse partii 1001, kuna see on varaseima sissetulekukuupäevaga (FIFO) partii.
-   Kui nii märkeruut **FIFO kuupäevakontrolliga** kui ka märkeruut **Lähetuskuupäevast tagasi** on valitud, reserveeritakse partii 1002, kuna selle partii sissetulek on kõige lähedasem müügitellimuse tarnekuupäevale.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Poliitikad varude ja laohalduse parameetrilehel.

Lehel **Varude ja laohalduse parameetrid** on kaks suvandit seotud reserveerimistega.
-   Suvand **Reserve ordered items** vahekaardil **Üldine** võimaldab reserveerida kauba sissetulekuid, mis on tellitud kauba väljaminekute suhtes moodulites Müügireskontro, Projektijuhtimine ja raamatupidamine ning Tootmise juhtimine. Selle valiku tühistamisel saate reserveerida ainult füüsiliselt sissetulnud kaupu. Kui konkreetse kauba puhul on lubatud negatiivne laovaru, pole see väli vajalik.
-   Suvand **Kaupade automaatne reserveerimine** vahekaardil **Transport** määrab vaikesätte, kui kaubad reserveeritakse üleviimistellimuste jaoks automaatselt. Vaikesätte saab individuaalsetel üleviimistellimustel alistada.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Varude reserveerimispoliitikad tootmisparameetrite lehel

Välja **Reserveerimine** väärtus vahekaardil **Üldine** lehel **Tootmise parameetrid** määrab tootmisprotsessi vaikepunkti, kus varud tuleb reserveerida. Näiteks saab varud reserveerida, kui tö planeeritakse või kui töö käivitatakse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]