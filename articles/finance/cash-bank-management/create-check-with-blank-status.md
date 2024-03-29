---
title: Olekuga Tühi tšekkide loomine
description: Selles artiklis selgitatakse, kuidas luua pangakontole tühje tšekke.
author: angelad116
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 86020d9088d8135c83716128a77090608536a78f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804014"
---
# <a name="create-checks-that-have-blank-status"></a>Olekuga Tühi tšekkide loomine

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse tühjade tšekkide loomist. Näiteks võite luua tühja tšeki selleks, et kirjendada tšekki, mis on kahjustatud ja mida ei saa makse tegemiseks kasutada.

Lehel **Tšekid** saate teha tšekkide hooldustoiminguid. Näiteks saate luua uusi tšekinumbreid ja tšekke kustutada. Saate luua ka tšekke, mille olek on **Tühi**. Pärast tühja tšeki loomist ei saa seda süsteemist kustutada ega uuesti kasutada.

> [!NOTE]
> Funktsioon on lehel **Tšekid** saadaval ainult siis, kui lülitate lehel **Funktsioonihaldus** sisse funktsiooni **Lehel Tšekid olekuga Tühi tšekkide loomine**. Kui funktsioon ei ole sisse lülitatud, saab tšekke olekuga **Tühi** luua ainult dialoogiaknas **Tšekiga maksmine** Ostureskontro maksete loomise protsessi käigus.

Lehe **Tšekid** avamiseks avage **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod** ning valige Tegumiribal vahekaardil **Maksete haldamine** grupis **Seostuv teave** üksus **Tšekid**. Teise variandina võite avada **Sularaha- ja pangahaldus \> Päringud ja aruanded \> Tšekid**.

Seejärel valige olekuga **Tühi** tšekkide loomiseks toimingupaanil **Tühjade tšekkide loomine**. Ajal, mil tühje tšekke luuakse, on seotud pangakonto ajutiselt inaktiveeritud. See käitumismudel vähendab ohtu, et makse luuakse samaaegselt tühja tšeki loomisega. Kui töötlemine on lõpule viidud, aktiveeritakse seotud pangakonto uuesti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
