---
title: "Tellimuse lähetamine muust kauplusest"
description: Selles teemas kirjeldatakse tasu saatmise funktsiooni.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: et-ee
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a>Tellimuse lähetamine muust kauplusest

Dynamics 365 for Retaili tasu saatmise funktsiooniga saate teha klienditellimuse ühes kaupluses ja lähetada selle teisest kauplusest. Kassas vormistatavad klienditellimused toetavad mitmesuguseid täitmisvalikuid. Täitmisvalikud on muuhulgas järgmised.
-   Kättesaamine samast kauplusest muul kuupäeval.
-   Kättesaamine muust kauplusest samal või muul kuupäeval.
-   Lähetamine kauplusele määratud vaikelaost ja tarnimine konkreetsel kuupäeval.

Tasu saatmise funktsioon kasutab järgmisi kassa operatsioone: Läheta kõik tooted ja Läheta valitud tooted. See võimaldab kassapidajal valida lähtekoha, kust saab tellimuse või selle rea täita. Vaikimisi on lähtekoht kauplusega seotud lähetav ladu. Müüja saab siiski asukohta muuta ja valida mis tahes kaupluse, mis on määratletud kauplusele määratud kaupluselokaatori grupis. 

See ei mõjuta sihtaadresside valimise võimalust. 

Tarneviisid, mida saab tellimuse rea täitmiseks kasutada, põhinevad toodete ja aadresside jaoks sobivatel tarneviisidel. Kuna sobivate tarneviiside reegleid talletatakse ainult kaupluse halduses (HQ), teeb kassaklient reaalajas kõne tarnerea jaoks sobivate tarneviiside toomiseks. 


