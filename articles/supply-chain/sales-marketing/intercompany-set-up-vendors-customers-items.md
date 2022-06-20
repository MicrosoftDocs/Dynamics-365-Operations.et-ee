---
title: Hankijate, klientide ja kaupade seadistamine kontserni kaubavahetuse jaoks
description: See artikkel selgitab, kuidas seadistada hankijaid, kliente ja kaupu kontserni kaubavahetuse jaoks.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945751"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Hankijate, klientide ja kaupade seadistamine kontserni kaubavahetuse jaoks

[!include [banner](../../includes/banner.md)]

Ettevõtte ettevalmistamiseks kontserni kaubavahetuse jaoks peate määratlema hankijad ja kliendid, kellega kontsernisiseselt kauplete. Seejärel peate need hankijad ja kliendid seostama kaupadega, mida ostate või müüte.

1. Avage **Hanked \> Hankijad \> Kõik hankijad**.
1. Saate valida hankija, kes määratleb kontsernisisese hankija.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Määrake hankija konto kontsernisisese seadistuse parameetrid. Need parameetrid hõlmavad kliendi juriidilist isikut ja kontot, müügitellimuse poliitikaid, ostutellimuse poliitikaid, väärtuste vastendamist ning ostulepingu ja müügilepingu poliitikaid. Samuti saate määrata, kas kasutada põhiandmete väärtusi hankija kontolt või kliendi kontolt teises juriidilises isikus.
1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige loendilehel **Väljastatud tooted** kaubad, mida hankijale määrata, et kaubad oleks kontserni kaubavahetuses saadaval. Iga kauba jaoks avage leht **Väljastatud toote üksikasjad**. Sisestage hankijakood vahekaardi **Ost** väljale **Hankija**.
1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Saate valida kliendi, mis määratleb kontsernisisese kliendi.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Määrake kliendi konto kontsernisisese seadistuse parameetrid. Need parameetrid hõlmavad hankija juriidilist isikut ja kontot, ostutellimuse poliitikaid, müügitellimuse poliitikaid, väärtuste vastendamist ning müügilepingu ja ostulepingu poliitikaid. Samuti saate määrata, kas kasutada põhiandmete väärtusi kliendi kontolt või hankija kontolt teises juriidilises isikus.
1. Kui olete seadistanud kontsernisisesed parameetrid, **sulgege** kontsernisisene leht valitud kliendi üksikasjade juurde tagasi pöördumiseks.
1. Laiendage **kiirkaarti Mitmesugust** ja määrake käsu **Loo kontsernisisesed tellimused väärtuseks** *Jah*. Kui soovite tellimused tarnida ka otse klientidele, seadke otsetarne **väärtuseks** *Jah*.

    > [!NOTE]
    > Kui ettevõttel on kaupu, mida ladustatakse ja tarnitakse klientidele, siis ei pruugi te soovida kontsernisiseseid tellimusi automaatselt luua, isegi kui teil on kaupa laos. Kui soovite vahel laos olevate kaupade tellimuste automaatse loomise inaktiveerida, seadke käsu Loo **kontsernisisesed tellimused väärtusele** *Ei*.

1. Kui soovite lubada lisaridade loomist müügitellimusel kaudselt, **seadke kaudsete tellimuseridade loomise väärtuseks** *Jah*. SIis saab kasutaja kontsernisisese müügitellimuse põhjal algsele müügitellimusele ridu lisada.

> [!WARNING]
> Kui lubate tellimuseridade loomise kaudselt, lubate kõikide lisamised kontsernisiseselt müügitellimuselt algsele müügitellimusele. Kõik lisamised töödeldakse seejärel kliendi kaudu ning lisatakse tellimusele ja arvele. Lisaks prinditakse ja sisestatakse automaatselt kõik müügiga seotud dokumendid. Lisamisest ei teavitata kasutajad.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
