---
title: Tarnehinna hankeparameetrid
description: See teema kirjeldab, kuidas seadistada asjakohaseid hankeparameetreid, kui kasutate Tarnehinna moodulit.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020979"
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
