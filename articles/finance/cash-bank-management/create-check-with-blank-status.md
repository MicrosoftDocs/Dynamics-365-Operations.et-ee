---
title: Olekuga Tühi tšekkide loomine
description: Selles teemas selgitatakse, kuidas luua pangakontole tühje tšekke.
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b3a0fbb26f135e567bf6af7b2f10b39a28be4c9e
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717212"
---
# <a name="create-checks-that-have-blank-status"></a>Olekuga Tühi tšekkide loomine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse tühjade tšekkide loomist. Näiteks võite luua tühja tšeki selleks, et kirjendada tšekki, mis on kahjustatud ja mida ei saa makse tegemiseks kasutada.

Lehel **Tšekid** saate teha tšekkide hooldustoiminguid. Näiteks saate luua uusi tšekinumbreid ja tšekke kustutada. Saate luua ka tšekke, mille olek on **Tühi**. Pärast tühja tšeki loomist ei saa seda süsteemist kustutada ega uuesti kasutada.

> [!NOTE]
> Funktsioon on lehel **Tšekid** saadaval ainult siis, kui lülitate lehel **Funktsioonihaldus** sisse funktsiooni **Lehel Tšekid olekuga Tühi tšekkide loomine**. Kui funktsioon ei ole sisse lülitatud, saab tšekke olekuga **Tühi** luua ainult dialoogiaknas **Tšekiga maksmine** Ostureskontro maksete loomise protsessi käigus.

Lehe **Tšekid** avamiseks avage **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod** ning valige Tegumiribal vahekaardil **Maksete haldamine** grupis **Seostuv teave** üksus **Tšekid**. Teise variandina võite avada **Sularaha- ja pangahaldus \> Päringud ja aruanded \> Tšekid**.

Seejärel valige olekuga **Tühi** tšeki loomiseks tegumiribal **Tühjade tšekkide loomine**. Kui süsteem loob tühja tšekki, on seotud pangakonto ajutiselt inaktiveeritud. See käitumismudel vähendab ohtu, et makse luuakse samaaegselt tühja tšeki loomisega. Kui töötlemine on lõpule viidud, aktiveeritakse seotud pangakonto uuesti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
