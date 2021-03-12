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
ms.openlocfilehash: d8c2288a18398f71a75dad6e51d51ba4b09561e6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997671"
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
