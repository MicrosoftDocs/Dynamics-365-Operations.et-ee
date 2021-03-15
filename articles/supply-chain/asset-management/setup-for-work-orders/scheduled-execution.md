---
title: Plaanitud käivitamine
description: Selles teemas selgitatakse plaanitud käivitamist varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a6d1761202697f62421bbf288c7e22efe559a986
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022403"
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