---
title: Saate häälestada vaikekirjeldused automaatseks sisestamiseks
description: See artikkel selgitab, kuidas seadistada vaiketeksti, mida kasutatakse raamatupidamiskirjete kirjeldamiseks, mis sisestatakse automaatselt pearaamatusse. Saate seadistada vaikimisi kirjeldusteksti, kasutades vabateksti või valides fikseeritud muutujad.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904495"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Saate häälestada vaikekirjeldused automaatseks sisestamiseks

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada vaiketeksti, mida kasutatakse raamatupidamiskirjete kirjeldamiseks, mis sisestatakse automaatselt pearaamatusse. Saate seadistada vaikimisi kirjeldusteksti, kasutades vabateksti või valides fikseeritud muutujad.

> [!NOTE]
> Mõnes riigis või regioonis saate mõne kandetüübi puhul kaasata ka nende kandetüüpidega seotud väljade teksti. Kandetüüpide ning riikide ja [regioonide loendi leiate jaotisest Valikuline. Jaotisest Valikuline leiate lisateavet jaotisest Valikuline.](#optional-add-other-text-to-default-descriptions) Lisa vaikekirjeldustele teine tekst selles artiklis.

## <a name="set-up-default-descriptions"></a>Vaikekirjelduste seadistamine

1. Valige **Organisatsiooni haldus** \> **Seadistus** \> **Vaikekirjeldused**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljal **Kirjeldus** valige kandetüüp, mille jaoks vaikekirjeldus luuakse.
4. Väljal **Keel** valige keel, millele see kirjeldus kehtib.
5. Väljal **Tekst** sisestage vaikekirjeldus. Saate teksti tippida väljale või kasutada ühte või mitut järgmist vabas vormis muutujat.

    - **%1** – lisage kande kuupäev.
    - **%2** – lisage identifikaator, mis vastab pearaamatusse sisestatava dokumendi tüübile. Näiteks arvetega seotud kandetüüpide puhul lisab muutuja **%2** arvenumbri.
    - **%3** – lisage identifikaator, mis on seotud pearaamatusse sisestatava dokumendi tüübiga. Näiteks arvetega seotud kandetüüpide puhul lisab muutuja **%3** kliendikonto numbri.

## <a name="optional-add-other-text-to-default-descriptions"></a>Valikuline: muu teksti lisamine vaikekirjeldustele

Teatud riikides või piirkondades saate mõne kandetüübi puhul kasutada vaikekirjeldustes teksti, mis pärineb nende kandetüüpidega seotud andmete väljadelt. Järgmistes loendites on näidatud kandetüübid ning riigid ja piirkonnad, mille puhul see valik saadaval on.

**Kandetüübid**

Saate lisada muud teksti kandetüüpide vaikekirjeldustele, mis on seotud järgmiste dokumenditüüpidega.

- Kliendiarved
- Kliendi kreeditarved
- Kliendi sularahamaksed
- Müüja maksed
- Müügitellimused
- Ostutellimused
- Laotöölehed
- Koondplaneerimine (MRP)
- Põhivarad

**Riigid ja piirkonnad**

See valik on saadaval järgmistes riikides ja piirkondades:

- Brasiilia
- Hiina
- Tšehhi Vabariik
- Ida-Euroopa
- Ungari
- India
- Jaapan
- Leedu
- Läti
- Poola
- Venemaa

### <a name="add-text-to-default-descriptions"></a>Muu teksti lisamine vaikekirjeldustele

Kui olete selles artiklis varasemas jaotises [Vaikekirjelduste](#set-up-default-descriptions) häälestamise sammud läbinud, järgige neid samme, et lisada vaikekirjeldustele muu tekst.

1. Valige kiirkaardil **Parameetrid** valik **Lisa**.
2. Valige väljal **Viitetabel** andmebaasi tabel, millest parameetriandmed kirjeldusse lisada.
3. Valige väljal **Viiteväli** väli, millest parameetriandmed kirjeldusse lisada.
4. Parameetrite lisamiseks korrake samme 1 kuni 3.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
