---
title: Tellimuste lähetamine teisest poest kasutades tasu saatmise funktsiooni
description: Selles teemas kirjeldatakse tasu saatmise funktsiooni.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 37ef0234df4ee983c44c183fe884c73b17eb0e06
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219025"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Tellimuste lähetamine teisest poest kasutades tasu saatmise funktsiooni

[!include [banner](includes/banner.md)]

Commerce'i tasu saatmise funktsiooniga saate teha klienditellimuse ühes kaupluses ja lähetada selle teisest kauplusest.

Kassas vormistatavad klienditellimused toetavad mitmesuguseid täitmisvalikuid. Täitmisvalikud on muuhulgas järgmised.

- Kättesaamine samast kauplusest muul kuupäeval.
- Kättesaamine muust kauplusest samal või muul kuupäeval.
- Lähetamine kauplusele määratud vaikelaost ja tarnimine konkreetsel kuupäeval.

Tasu saatmise funktsioon kasutab järgmisi kassa operatsioone: Läheta kõik tooted ja Läheta valitud tooted. See võimaldab kassapidajal valida lähtekoha, kust saab tellimuse või selle rea täita. Vaikimisi on lähtekoht kauplusega seotud lähetav ladu. Müüja saab siiski asukohta muuta ja valida mis tahes kaupluse, mis on määratletud kauplusele määratud kaupluselokaatori grupis.

See ei mõjuta sihtaadresside valimise võimalust.

Tarneviisid, mida saab tellimuse rea täitmiseks kasutada, põhinevad toodete ja aadresside jaoks sobivatel tarneviisidel. Kuna sobivate tarneviiside reegleid talletatakse ainult Headquarteris (HQ), teeb kassaklient reaalajas kõne tarnerea jaoks sobivate tarneviiside toomiseks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]