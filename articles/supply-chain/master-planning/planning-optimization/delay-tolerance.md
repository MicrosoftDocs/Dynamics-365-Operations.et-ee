---
title: Viivituse kõikumine (negatiivsed päevad)
description: See artikkel annab teavet viivituse kõikumise arvutamise kohta ja selle kohta, kuidas see mõjutab plaanitud tellimuse loomist plaanimise optimeerimises.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4bd6042f9dd33ba15773b251911e965cb870c5aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865117"
---
# <a name="delay-tolerance-negative-days"></a>Viivituse kõikumine (negatiivsed päevad)

[!include [banner](../../includes/banner.md)]

Viivituse kõikumise funktsioon võimaldab planeerimise optimeerimisel arvestada laovarude gruppidele seatud **negatiivsete päevade** väärtust. Seda kasutatakse koondplaneerimisel rakendatud viivituse kõikumise perioodi pikendamiseks. Sel viisil saate vältida uute tarnetellimuste loomist, kui olemasolev pakkumine suudab nõudlust pärast lühikest viivitust katta. Selle funktsiooni eesmärk on määrata, kas antud nõudlusele on mõtet luua uus tarnetellimus.

## <a name="turn-on-the-feature-in-your-system"></a>Funktsiooni sisselülitamine teie süsteemis

Et teha viivituse kõikumise funktsioon süsteemis kättesaadavaks, minge [Funktsioonihaldus](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ja lülitage sisse *Planeeritud tellimuste negatiivsete päevade* funktsioon.

## <a name="delay-tolerance-in-planning-optimization"></a>Viivituse kõikumine plaanimise optimeerimises

Viivituse kõikumine näitab nende päevade arvu, mis on pärast täitmisaega, millal soovite enne uue varude täiendamist oodata, kui olemasolev tarne on juba planeeritud. Viivituse kõikumine määratletakse kalendripäevade, mitte tööpäevade abil.

Koondplaneerimise ajal, kui süsteem arvutab viivituse kõikumise, arvestab see sätet **Negatiivsed päevad**. **Negatiivsed päevad** saate määrata lehel **Kauba laovarud** või lehel **Laovarude grupid**.

Süsteem seob viivituse kõikumise arvutamise *varaseima täiendamiskuupäevaga*, mis on võrdne tänase kuupäeva ja täitmisajaga. Viivituse kõikumine arvutatakse järgmise valemi abil, kus *max()* leiab kahest väärtusest suurema:

*max(varaseim täienduspäev, nõudetähtaeg)* – *nõudetähtaeg* + *negatiivsed päevad*

See valem tagab, et koondplaneerimine ei loo uusi tarnetellimusi, kui toote täitmisaja jooksul on piisavalt tarneid.

> [!NOTE]
> Viivituse kõikumise arvutamine plaanimise optimeerimises kasutab alati dünaamilist negatiivsete päevade arvutust integreeritud koondplaneerimisest. Säte **Kasuta dünaamilisi negatiivseid päevi** lehel **koondplaneerimise parameetrite** ei mõjuta seda käitumist.

Kui olemasolev pakkumine tähendab nõudluse viivitust, mis on arvutatud viivituse kõikumisest väiksem või sellega võrdne, seob plaanimise optimeerimine olemasoleva pakkumise nõudlusega. Mõnel juhul on parem nõudlust edasi lükata, kui lõpetada ülepakkumisega.

Järgmised alamjaotised pakuvad näiteid, mis näitavad, kuidas viivituse kõikumine mõjutab planeeritud tellimuste loomist plaanimise optimeerimises.

### <a name="example-1"></a>Näide 1

Toote konfiguratsioon on järgmine:

- **Täitmisaeg:** *10*
- **Negatiivsed päevad:** *2*

Tootel on järgmine pakkumine ja nõudlus:

- **Tänane nõudlus:** müügitellimus kogusele 10
- **Tarne 12 päevaga:** ostutellimus kogusele 10

Olemasolev pakkumine võib katta nõudluse 12 päeva jooksul ja see periood võrdub viivituse kõikumisega. Seetõttu ei looda koondplaneerimise käitamisel plaanitud tellimusi.

### <a name="example-2"></a>Näide 2

Toote konfiguratsioon on järgmine:

- **Täitmisaeg:** *10*
- **Negatiivsed päevad:** *0*

Tootel on järgmine pakkumine ja nõudlus:

- **Tänane nõudlus:** müügitellimus kogusele 10
- **Tarne 12 päevaga:** ostutellimus kogusele 10

Olemasolev pakkumine saab nõudlust katta alles 12 päeva pärast. Kuid viivituse lubatud kõikumine on 10 päeva. Seepärast luuakse koondplaneerimise käitamisel plaanitud tellimus kogusele 10.

### <a name="example-3"></a>Näide 3

Toote konfiguratsioon on järgmine:

- **Täitmisaeg:** *10*
- **Negatiivsed päevad:** *2*

Tootel on järgmine pakkumine ja nõudlus:

- **Nõudlus 11 päevale:** müügitellimus kogusele 10
- **Tarne 14 päevaga:** ostutellimus kogusele 10

Olemasolev pakkumine saab nõudlust katta alles kolme päeva pärast. Kuid viivituse lubatud kõikumine on kaks päeva. (Sel juhul hõlmab viivituse kõikumine ainult kahte negatiivset päeva. Nõudluse kuupäeva ei kaasatud, kuna see on pärast toote täitmisaega.) Seepärast luuakse koondplaneerimise käitamisel plaanitud tellimus kogusele 10.
