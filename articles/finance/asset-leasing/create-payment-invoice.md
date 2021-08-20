---
title: Maksearvete loomine
description: Selles teemas kirjeldatakse igakuiste rendiarvete loomist. Saate luua arved üksikutele rendikirjetele või saate kasutada partiina töötlemist, et luua need mitmele rendikirjele.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 94657a1c423fafb89d2fe2c16937947e0d898771ddb30a029d0938cc17aaf7d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716665"
---
# <a name="create-payment-invoices"></a>Maksearvete loomine

[!include [banner](../includes/banner.md)]

Saate luua igakuised arved üksikutele rendikirjetele või saate kasutada partiina töötlemist, et luua need mitmele rendikirjele. Järgmine toiming näitab, kuidas luua individuaalse rendimakse kanne, kui parameeter **Hankijale tasumine** on lehel **Rendi raamatu häälestus** on sisse lülitatud.

1. Valige lehel **Rendi kokkuvõte** rendikirje ja valige seejärel **Raamatud \> Maksegraafik**.
2. Valige tehtav makse ja valige seejärel käsk **Loo tööleht**. Kuvatakse teade sõnumiga, et valitud makse suhtes loodi tööleht.
3. Valige **Arve töölehed** ja valige seejärel arve, mis tuleb tasuda.
4. Vahekaardil **Read** vaadake läbi töölehe kirje, enne kui selle pearaamatusse sisestate.

    > [!NOTE]
    > Vaikimisi kasutavad loodavad hankija arveread hankija sisestamise profiili lehelt **Ostureskontro parameetrid**.

5. Valige õige tööleht ja valige seejärel arve, mis tuleb tasuda.

    Selle näite puhul on rendi raamatu parameeter **Hankijale tasumine** sisse lülitatud. Seega on arve arve töölehel. Jaotises **Ülevaade** kuvatakse töölehe sisestuse kokkuvõte ja jaotises **Read** kuvatakse tegelike töölehe ridade üksikasjad.

    > [!NOTE]
    > Kui parameeter **Hankijale tasumine** on välja lülitatud, loetletakse makse töölehe kanded rendi raamatu lehel **Vara rentimine** ja süsteem loob arve asemel vara rentimise kande. Rendimakse kanne sisestatakse töölehe nimele, mis on määratud väljal **Igakuine rendi tööleht**.

6. Pärast kande sisestamist saate vaadata kande teavet ja rendikohustise bilansilist väärtust, valides rendi raamatus suvandi **Kohustise tehingud**.

    Maksegraafikus valitakse märkeruut **Tööleht on sisestatud** ja rida kuvab arve töölehe numbri. Pärast makse töölehe ja selle töölehe kirje on loodud, peate kirje enne selle uuesti loomist ümber pöörama.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
