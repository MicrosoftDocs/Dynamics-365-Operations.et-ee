---
title: Saate seadistada vaikekirjeldused automaatseks sisestamiseks
description: Selles teemas selgitatakse, kuidas seadistada vaiketeksti, mida kasutatakse automaatselt pearaamatusse sisestatavate raamatupidamiskirjete kirjeldamiseks kasutatavat vaiketeksti. Saate seadistada vaikimisi kirjeldusteksti, kasutades vabateksti või valides fikseeritud muutujad.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5955b796cbc7917eb5500b96c879d1b0819d2edc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204854"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Saate seadistada vaikekirjeldused automaatseks sisestamiseks

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada vaiketeksti, mida kasutatakse automaatselt pearaamatusse sisestatavate raamatupidamiskirjete kirjeldamiseks kasutatavat vaiketeksti. Saate seadistada vaikimisi kirjeldusteksti, kasutades vabateksti või valides fikseeritud muutujad.

> [!NOTE]
> Teatud riikides või piirkondades saate mõne kandetüübi puhul kaasata ka teksti nende kandetüüpidega seotud väljadelt rakenduse Microsoft Dynamics AX andmebaasis. Kandetüüpide ning riikide ja regioonide loendi leiate selle teema jaotisest [Valikuline: muu teksti lisamine vaikekirjeldustele](#optional-add-other-text-to-default-descriptions).

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

Pärast selle teema varasemas jaotises [Vaikekirjelduste seadistamine](#set-up-default-descriptions) toodud sammude läbimist tehke vaikekirjeldustele muu teksti lisamiseks järgmist.

1. Valige kiirkaardil **Parameetrid** valik **Lisa**.
2. Valige väljal **Viitetabel** andmebaasi tabel, millest parameetriandmed kirjeldusse lisada.
3. Valige väljal **Viiteväli** väli, millest parameetriandmed kirjeldusse lisada.
4. Parameetrite lisamiseks korrake samme 1 kuni 3.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]