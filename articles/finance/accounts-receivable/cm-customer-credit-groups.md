---
title: Kliendi krediidigrupid
description: Selles teemas kirjeldatakse kliendi krediidigruppe.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b1e93d562e66cb8d4c5819a749459ea8783b1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237538"
---
# <a name="customer-credit-groups"></a>Kliendi krediidigrupid

[!include [banner](../includes/banner.md)]

Saate määratleda kliendigrupid, kellel on jagatud krediidilimiit. Arvestatakse ka kliendiarve kontole määratletud individuaalset krediidilimiiti.

Kliendi krediidigrupi liikmeid saab valida erinevate juriidiliste isikute seast. Kui lisate kliendi krediidigrupi klientide loendisse kliendi, muudetakse iga kliendi krediidilimiidi aegumiskuupäev grupile määratud aegumiskuupäevaks.

Kliendi krediidigruppe saate seadistada lehel **Kliendi krediidigrupid** (**Krediidihaldus \> Kliendi krediidigrupid \> Kliendi krediidigrupid**).

1. Sisestage väljadele **Grupi number** ja **Kirjeldus** grupi identifikaator ja kirjeldus.
2. Sisestage väljadele **Krediidilimiit** ja **Valuuta** see krediidilimiit ja valuuta, mida tuleks kasutada, kui süsteem kontrollib grupi mõne liikme krediidilimiiti.
3. Väljale **Krediidilimiit kuupäevani** sisestage krediidilimiidi aegumise kuupäev. Kliendi krediidigruppidel peab olema aegumiskuupäev.

Kui olete kliendi krediidigrupi seadistamise lõpetanud, saate sellele kliente lisada, määratledes nende juriidilise isiku ja kliendi konto ID. Kui lisate kliendi krediidigrupile uue kliendi, otsib süsteem kõigi juriidiliste isikute seast sama kliendikonto ja palub teil selle kliendi krediidigruppi lisada.

Kasutage menüüd **Aegunud saldod**, et vaadata kõigi kliendi krediidigrupi arveklientide aegumissaldo üksikasju. Leht **Aegumissaldo** näitab arveklientide kontode aegunud saldosid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]