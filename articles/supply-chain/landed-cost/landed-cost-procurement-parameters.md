---
title: Tarnehinna hankeparameetrid
description: See teema kirjeldab, kuidas seadistada asjakohaseid hankeparameetreid, kui kasutate Tarnehinna moodulit.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6e0ceb84423d7adc9c37da1b0b35a486627c0ce3
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690410"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Tarnehinna hankeparameetrid

[!include [banner](../../includes/banner.md)]

**Hankeparameetrite** lehel on mõned sätted, mis on eriti asjakohased, kui kasutate **Tarnehinna** moodulit. Kasutage **Tellimuseridade värskendamine** dialoogiboksi, mis on avatud **Hankeparameetrite** lehel, et määrata, kas ostutellimuse päises tehtud muudatuste korral tuleks ostutellimuse read automaatselt uuendada.

Selle seadistamise lõpetamiseks järgige järgmisi etappe.

1. Minge **Hanked \> Seadistus \> Hangete parameetrid**.
1. Vahekaardil **Üldine**, valige link **Uuenda tellimuse ridu**.
1. Dialoogiaknas **Tellimuse ridade värskendamine** loetletakse tellimuse päise väljad, mida saab rakendada ka tellimuseridade seotud väljade automaatseks värskendamiseks. Seadistage iga loendi väli ühele järgmistest väärtustest:

    - **Alati** - Tellimuse read uuendatakse tellimuse päise uuendamisel automaatselt.
    - **Mitte kunagi** - Tellimuse ridu ei uuendata kunagi tellimuse päise uuendamisel automaatselt.
    - **Küsi** - Kasutajalt küsitakse, kas tellimuse ridu tuleks uuendada.
