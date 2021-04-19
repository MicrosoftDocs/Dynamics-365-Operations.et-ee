---
title: Plaanitud käivitamine
description: Selles teemas selgitatakse plaanitud käivitamist varahalduses.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fae899bcfa8bb2566d1a9aee3f0dbe22bc219edf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825634"
---
# <a name="scheduled-execution"></a>Plaanitud käivitamine

[!include [banner](../../includes/banner.md)]

 

Saate plaanitud käivitamise seadistamiseks kasutada töökäsu teenindustasemeid. (Töökäsu teenindustasemete kohta lisainfo saamiseks vt [Teenindustase ja kirjeldus](service-level-and-description.md).) Plaanitud käivitamine pakub hooldustöötajate töö planeerimises paindlikkust, sest saate seadistada üksikasjalikumaid või vähemate üksikasjadega nõudeid sellele ajavahemikule, millal töökäsk peaks lõpule viidama. Näiteks võib hooldustöötaja, kes lõpetab töö tootmishoones oodatus varem liikuda edasi teisele lähedalasuvale tööle, mis on planeeritud selleks nädalaks aga mitte ilmtingimata samaks päevaks. See lähenemine võimaldab töötajate planeerimise ja töö lõpetamise optimeerimist.

Töökäskudega seotud planeeritud käivitamise seadistamine võib olla üldine või spetsiifiline. Võite seadistada üldised read, mis ei ole piiratud konkreetsete töökäsu tüüpidega, vara tüüpidega jne. Alternatiivina võite luua planeeritud käivitamise ridu, mis rakenduvad konkreetsele töökäsu tüübile, vara tüübile, hooldustöö tüübile jne.

1. Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Planeeritud käivitamine**.
2. Planeeritud käivitamise rea loomiseks valige **Uus**.
3. Valige vajalikud väärtused väljadele **Töö asukoht**, **Töökäsu tüüp**, **Vara tüüp**, **Tootja**, **Mudel**, **Hooldustöö tüübi kategooria**, **Hooldustöö tüüp**, **Hooldustöö tüübi variant** ja **Vahetus**.
4. Valige töökäsu teenindustase väljal **Teenindustase**. Kui jätate selle välja tühjaks, teete kõige üldisemat tüüpi planeeritud käivitamise rea. Üldise rea näite leiate järgneva joonise esimesest kirjest. See rida lubab planeerida kõik sellised töökäsud, millel ei ole töökäsu teenindustaset, konkreetsele kuupäevale ja kellaajale.
5. Valige ajavahemik väljal **Planeeritud käivitamine**.
6. Valige käsk **Salvesta**.

![Plaanitud käivitamine](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]