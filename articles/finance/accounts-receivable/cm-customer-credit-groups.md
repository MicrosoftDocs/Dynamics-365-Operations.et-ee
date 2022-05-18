---
title: Kliendi krediidigrupid
description: Selles teemas kirjeldatakse kliendi krediidigruppe.
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0815aa41b034d8ba5c9b09f4003ff3df7311190a
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735488"
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
