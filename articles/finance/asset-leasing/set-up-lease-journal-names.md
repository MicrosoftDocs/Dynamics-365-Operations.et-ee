---
title: Renditöölehe nimede seadistamine
description: Selles teemas selgitatakse renditöölehe nimede määratlemist. Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse.
author: moaamer
ms.date: 04/12/2021
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
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880882"
---
# <a name="set-up-lease-journal-names"></a>Renditöölehe nimede seadistamine

[!include [banner](../includes/banner.md)]

Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse. Ainult need töölehe nimed, mis on määratud töölehe tüübile **Vara rentimine** kuvatakse väljadel **Esialgne tuvastamine** ja **Kuu töölehe nimi** lehel **Vara rentimise parameetrid**. Ainult töölehe tüüpi **hankija arve kirjendamine** saab määrata väljale **Arve töölehe nimi**.

Renditöölehe nimede konfigureerimiseks toimige järgmiselt.

1. Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.
2. Valige tööleht vahekaardi **Üldine** väljal **Esialgse tuvastamise töölehe nimi**. Kõik esialgse tuvastamise töölehe kirjed sisestatakse sellele töölehe nimele.
3. Valige tööleht väljal **Arve töölehe nimi**. Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Jah**, siis sisestatakse rendi ja kulude maksete arved sellele töölehe nimele.
4. Valige tööleht väljal **Renditöölehe nimi**. Kõik kulumi-, intressi- ja lühiajalise ümberklassifitseerimise kanded sisestatakse sellele töölehe nimele. Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Ei**, siis sisestatakse rendimaksete ja kulude maksete kirjed samuti sellele töölehe nimele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
