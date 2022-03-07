---
title: Hankijate, klientide ja kaupade seadistamine kontserni kaubavahetuse jaoks
description: See teemaselgitab hankijate, klientide ja kaupade seadistamist kontserni kaubavahetuse jaoks
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 062b8fe956fef0f8172d26aac3df54b93e1941ef
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548209"
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
1. Lehel **Kliendid**, kiirkaardil **Arve ja kohaletoimetamine** valige märkeruut **Loo kontsernisisesed tellimused**. Kui soovite, et tellimused tarnitakse otse klientidele, märkige ruut **Otsetarne**.

    > [!NOTE]
    > Kui ettevõttel on kaupu, mida ladustatakse ja tarnitakse klientidele, siis ei pruugi te soovida kontsernisiseseid tellimusi automaatselt luua, isegi kui teil on kaupa laos. Kui soovite tellimuste automaatse loomise inaktiveerida selliste kaupade puhul, mida teil on laos aeg-ajalt, jätke ruut **Loo kontsernisisesed tellimused** tühjaks.

1. Kui soovite lubada lisaridade loomist müügitellimusele kaudselt, märkige ruut **Loo kaudse tellimuse read**. SIis saab kasutaja kontsernisisese müügitellimuse põhjal algsele müügitellimusele ridu lisada.

> [!WARNING]
> Kui lubate tellimuseridade loomise kaudselt, lubate kõikide lisamised kontsernisiseselt müügitellimuselt algsele müügitellimusele. Kõik lisamised töödeldakse seejärel kliendi kaudu ning lisatakse tellimusele ja arvele. Lisaks prinditakse ja sisestatakse automaatselt kõik müügiga seotud dokumendid. Lisamisest ei teavitata kasutajad.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
