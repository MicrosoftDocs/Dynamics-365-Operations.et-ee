---
title: Renditöölehe nimede seadistamine
description: Selles teemas selgitatakse renditöölehe nimede määratlemist. Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a92461e742f1675e4cfda89e6c80c5b087ff5bfb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644893"
---
# <a name="set-up-lease-journal-names"></a>Renditöölehe nimede seadistamine

[!include [banner](../includes/banner.md)]


Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse. Ainult need töölehe nimed, mis on määratud töölehe tüübile **Vara rentimine** kuvatakse väljadel **Esialgne tuvastamine** ja **Kuu töölehe nimi** lehel **Vara rentimise parameetrid**. Ainult töölehe tüüpi **hankija arve kirjendamine** saab määrata väljale **Arve töölehe nimi**.

Süsteem lukustab teatud finantsväljade redigeerimise, et vältida hälbeid kannete ja graafikute vahel. Mõned lukustatud väljad on: **Konto**, **Summad**, **Finantsdimensioonid**, **Valuuta** ja **Kande tüüp**. Samuti ei saa te lisada ega kustutada töölehe kirje ridu üheski vara rentimise töölehekirjes, kuna see võib graafikute ja kannete vahel hälbeid põhjustada.


Liisingutöölehe nimede konfigureerimiseks viige lõpule järgmised sammud.

1. Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.
2. Valige tööleht vahekaardi **Üldine** väljal **Esialgse tuvastamise töölehe nimi**. Kõik esialgse tuvastamise töölehe kirjed sisestatakse sellele töölehe nimele.
3. Valige tööleht väljal **Arve töölehe nimi**. Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Jah**, siis sisestatakse rendi ja kulude maksete arved sellele töölehe nimele.
4. Valige tööleht väljal **Renditöölehe nimi**. Kõik kulumi-, intressi- ja lühiajalise ümberklassifitseerimise kanded sisestatakse sellele töölehe nimele. Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Ei**, siis sisestatakse rendimaksete ja kulude maksete kirjed samuti sellele töölehe nimele.
5. Valige väljal **Liisingu muutmise** töölehe nimi tööleht. Sellele töölehe nimele sisestatakse rendi-, lepingu lõpetamise- ja kahjustuse kanded. Teie valitud töölehe nimele ei tohiks määrata töövoogu ega kinnitamist. Kui liisingu muutmise töölehe nimi on määratlemata, sisestatakse rendi korrigeerimine, lõpetamine ja kahjustuse kanded töölehe nimele, **mis on valitud renditöölehe nime väljal**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
