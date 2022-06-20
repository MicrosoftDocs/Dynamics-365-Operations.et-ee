---
title: Tarnehinna hankeparameetrid
description: See artikkel kirjeldab, kuidas seadistada asjakohased hankeparameetrid, kui kasutate väljaminev kulumoodulit.
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
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905975"
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
