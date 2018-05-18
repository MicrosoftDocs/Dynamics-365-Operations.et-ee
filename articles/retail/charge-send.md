---
title: "Tellimuse lähetamine muust kauplusest"
description: Selles teemas kirjeldatakse tasu saatmise funktsiooni.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: 41434614b01f9a00f2b8a56765ecb90ee07e3d90
ms.contentlocale: et-ee
ms.lasthandoff: 03/05/2018

---

# <a name="ship-an-order-from-a-different-store"></a>Tellimuse lähetamine muust kauplusest

[!include [banner](includes/banner.md)]

Dynamics 365 for Retaili tasu saatmise funktsiooniga saate teha klienditellimuse ühes kaupluses ja lähetada selle teisest kauplusest. Kassas vormistatavad klienditellimused toetavad mitmesuguseid täitmisvalikuid. Täitmisvalikud on muuhulgas järgmised.
-   Kättesaamine samast kauplusest muul kuupäeval.
-   Kättesaamine muust kauplusest samal või muul kuupäeval.
-   Lähetamine kauplusele määratud vaikelaost ja tarnimine konkreetsel kuupäeval.

Tasu saatmise funktsioon kasutab järgmisi kassa operatsioone: Läheta kõik tooted ja Läheta valitud tooted. See võimaldab kassapidajal valida lähtekoha, kust saab tellimuse või selle rea täita. Vaikimisi on lähtekoht kauplusega seotud lähetav ladu. Müüja saab siiski asukohta muuta ja valida mis tahes kaupluse, mis on määratletud kauplusele määratud kaupluselokaatori grupis. 

See ei mõjuta sihtaadresside valimise võimalust. 

Tarneviisid, mida saab tellimuse rea täitmiseks kasutada, põhinevad toodete ja aadresside jaoks sobivatel tarneviisidel. Kuna sobivate tarneviiside reegleid talletatakse ainult kaupluse halduses (HQ), teeb kassaklient reaalajas kõne tarnerea jaoks sobivate tarneviiside toomiseks. 


