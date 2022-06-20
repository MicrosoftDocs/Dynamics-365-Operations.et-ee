---
title: Maksearvete loomine
description: See artikkel selgitab, kuidas luua igakuiseid rendiarveid. Saate luua arved üksikutele rendikirjetele või saate kasutada partiina töötlemist, et luua need mitmele rendikirjele.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0ac9efaf6d068377053ae36951f4ad808fcb2438
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886402"
---
# <a name="create-payment-invoices"></a>Maksearvete loomine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Saate luua igakuised arved üksikutele rendikirjetele või saate kasutada partiina töötlemist, et luua need mitmele rendikirjele. Järgmine toiming näitab, kuidas luua individuaalse rendimakse kanne, kui parameeter **Hankijale tasumine** on lehel **Rendi raamatu häälestus** on sisse lülitatud.

1. Valige lehel **Rendi kokkuvõte** rendikirje ja valige seejärel **Raamatud \> Maksegraafik**.
2. Valige tehtav makse ja valige seejärel käsk **Loo tööleht**. Kuvatakse teade sõnumiga, et valitud makse suhtes loodi tööleht.
3. Valige **Arve töölehed** ja valige seejärel arve, mis tuleb tasuda.
4. Vahekaardil **Read** vaadake läbi töölehe kirje, enne kui selle pearaamatusse sisestate.

    > [!NOTE]
    > Vaikimisi kasutavad loodavad hankija arveread hankija sisestamise profiili lehelt **Ostureskontro parameetrid**.

5. Valige õige tööleht ja valige seejärel arve, mis tuleb tasuda.

    Selle näite puhul on rendi raamatu parameeter **Hankijale tasumine** sisse lülitatud. Seega on arve arve töölehel. Jaotises **Ülevaade** kuvatakse töölehe sisestuse kokkuvõte ja jaotises **Read** kuvatakse tegelike töölehe ridade üksikasjad.
    
   Süsteem lukustab teatud finantsväljade redigeerimise, et vältida hälbeid kannete ja graafikute vahel. Mõned lukustatud väljad on: **Konto**, **Summad**, **Finantsdimensioonid**, **Valuuta** ja **Kande tüüp**. Samuti ei saa te lisada ega kustutada töölehe kirje ridu üheski vara rentimise töölehekirjes, kuna see võib graafikute ja kannete vahel hälbeid põhjustada.

    > [!NOTE]
    > Kui parameeter **Hankijale tasumine** on välja lülitatud, loetletakse makse töölehe kanded rendi raamatu lehel **Vara rentimine** ja süsteem loob arve asemel vara rentimise kande. Rendimakse kanne sisestatakse töölehe nimele, mis on määratud väljal **Igakuine rendi tööleht**.

6. Pärast kande sisestamist saate vaadata kande teavet ja rendikohustise bilansilist väärtust, valides rendi raamatus suvandi **Kohustise tehingud**.

    Maksegraafikus valitakse märkeruut **Tööleht on sisestatud** ja rida kuvab arve töölehe numbri. Pärast makse töölehe ja selle töölehe kirje on loodud, peate kirje enne selle uuesti loomist ümber pöörama.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
