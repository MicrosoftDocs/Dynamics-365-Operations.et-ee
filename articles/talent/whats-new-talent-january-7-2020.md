---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (7. jaanuar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460931"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (7. jaanuar 2020)

Selles artiklis kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2697. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Ei saa kustutada töötajaid, kellel puuduvad tööhõivekirjed – (386157)

See muudatus lisab vormi **Ilma töösuhteta töötajad** kustutamisvõimaluse. Töötajad kuvatakse sellel vormil, kui töötajaga pole ühtegi tulevast, aktiivset või ajaloolist töösuhet. Selles versioonis on kustutamine lubatud ainult süsteemiadministraatoritele. Samas järgmise nädala väljalaskes turvalisust täiendatakse, et lubada kõikidel personaliassisteni rolliga kasutajatel eemaldada ilma töösuhteta töötajaid. Samuti saate teha neid muudatusi käsitsi, järgides järgmisi samme.

1. Avage suvand **Turvakonfiguratsioon**.
2. Vahekaardil **Privileegid** filtreerige loendit **Privileegid** suvandi **Töötajate haldamine** alusel.
3. Valige veerus **Viited** suvand **Kuvamenüü üksused**.
4. Valige veerus **Kuvamenüü üksused** suvand **HcmWOrkersWithoutEmployment**.
5. Määrake luba **Kustuta** olekusse Luba.
6. Valige vahekaart **Avaldamata objektid**.
7. Valige **Avalda kõik**.
