---
title: Rendiraamatute seadistamine
description: Selles teemas kirjeldatakse rendiraamatutes hoitavat teavet. Rendiraamatud sisaldavad arvestuspõhimõtteid, mis määravad, kuidas rendilepingut süsteemis arvestatakse.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442564"
---
# <a name="set-up-lease-books"></a>Rendiraamatute seadistamine

[!include [banner](../includes/banner.md)]

Rendiraamatud sisaldavad arvestuspõhimõtteid, mis määravad, kuidas rendilepingut süsteemis arvestatakse. Lisaks sularahapõhisele raamatupidamisele toetab vara rentimine järgmiseid standardeid.

- Üldtunnustatud raamatupidamispõhimõtted Ameerika Ühendriikides (USA RAAMATUPIDAMISTAVA)
- Raamatupidamisstandardite kodeerimise teema 842 (ASC 842)
- ASC 840
- Rahvusvaheline finantsaruandluse Standard 16 (IFRS 16)
- Rahvusvaheline raamatupidamisstandard 17 (IAS 17)

Rendiraamatu loomiseks toimige järgmiselt.

1. Avage **Vara rentimine \> Seadistus \> Rendiraamatud**.
2. Raamatu lisamiseks valige **Uus**.
3. Seadistage järgmised väljad.

    | Nimi                                     | Kirjeldus |
    |------------------------------------------|-------------|
    | Sisestamiskiht                            | Valige kasutatav sisestamiskiht. Iga rendilepinguga seotud raamat seadistatakse kindla sisestuskihi jaoks. Igal sisestuskihil on erinevad sisestamise eesmärgid. |
    | Rendi tüüp                               | Valige, kas rendileping tuleb klassifitseerida automaatselt või kas see peaks olema eelmääratletud kui kapitali- või kasutusrent. |
    | Raamatupidamisraamistik                     | Valige raamatuga seotud raamistik. |
    | Rendiperioodi/kasuliku tööea häälestus          | Süsteem liigitab rendi kapitalirendiks, kui rendi tüüp on seadistatud **Automaatseks** ja kui rendiperiood vara kasuliku tööea jooksul on suurem kui siin väljal määratletud protsent või sellega võrdne.  |
    | Praeguse väärtuse / vara õiglase väärtuse häälestamine   | Sisestage täisarv, et määratleda lävi, mis määrab rendi tüübi. Kui tulevaste minimaalsete rendimaksete praegune väärtus on suurem kui kasutaja määratud väärtus raamatu seadistusest ja kui raamatu rendi klassifikatsioon on seadistatud automaatseks, klassifitseerib süsteem rendi kapitalirendina. |
    | Lühiajaline künnis                     | Sisestage kuude arv lühiajaliste rendilepingute lävena kasutamiseks. Kui rendileping on siin sisestatud kuude arvust lühem või sellega võrdne, klassifitseerib süsteem rendi lühiajalise rendina ja rakendatakse edasilükatud rendi käsitlust. |
    | Väikese väärtuse künnis                      | Sisestage summa, mida kasutatakse väikese väärtusega rendilepingute lävena. Kui vara õiglane väärtus on väiksem või võrdne siia sisestatud väärtusega, klassifitseerib süsteem rendi väikese väärtusega rendina ja rakendatakse edasilükatud rendi käsitlust. |
    | Tasumine hankijale                            | Seadke see suvand väärtusele **Jah**, et lubada rendimaksete sisestamist arvena igale rendilepingul määratud hankija kontole. Kui rendimakse sisestatakse, krediteeritakse hankija kontot. Kui see valik on seadistatud väärtusele **Ei**, krediteeritakse selle asemel konto, mis on määratud **Rendimakse** sisestustüübile lehel **Rendi sisestamise parameetrid**. |
