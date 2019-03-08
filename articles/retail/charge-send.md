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
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: e5351086c56d13ef98937aec066be00cdf88fd37
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354065"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Tellimuste lähetamine teisest poest kasutades tasu saatmise funktsiooni

[!include [banner](includes/banner.md)]

Dynamics 365 for Retaili tasu saatmise funktsiooniga saate teha klienditellimuse ühes kaupluses ja lähetada selle teisest kauplusest.

Kassas vormistatavad klienditellimused toetavad mitmesuguseid täitmisvalikuid. Täitmisvalikud on muuhulgas järgmised.

- Kättesaamine samast kauplusest muul kuupäeval.
- Kättesaamine muust kauplusest samal või muul kuupäeval.
- Lähetamine kauplusele määratud vaikelaost ja tarnimine konkreetsel kuupäeval.

Tasu saatmise funktsioon kasutab järgmisi kassa operatsioone: Läheta kõik tooted ja Läheta valitud tooted. See võimaldab kassapidajal valida lähtekoha, kust saab tellimuse või selle rea täita. Vaikimisi on lähtekoht kauplusega seotud lähetav ladu. Müüja saab siiski asukohta muuta ja valida mis tahes kaupluse, mis on määratletud kauplusele määratud kaupluselokaatori grupis.

See ei mõjuta sihtaadresside valimise võimalust.

Tarneviisid, mida saab tellimuse rea täitmiseks kasutada, põhinevad toodete ja aadresside jaoks sobivatel tarneviisidel. Kuna sobivate tarneviiside reegleid talletatakse ainult kaupluse halduses (HQ), teeb kassaklient reaalajas kõne tarnerea jaoks sobivate tarneviiside toomiseks.
