---
title: Viivituse kõikumine (negatiivsed päevad)
description: See artikkel annab teavet viivituse kõikumise arvutamise kohta ja selle kohta, kuidas see mõjutab plaanitud tellimuse loomist plaanimise optimeerimises.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: fa4d2d1506546cacf5f9a7ec936f17601c5727d2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335371"
---
# <a name="delay-tolerance-negative-days"></a>Viivituse kõikumine (negatiivsed päevad)

[!include [banner](../../includes/banner.md)]

Viivituse hälbe funktsioon võimaldab planeerimise optimeerimisel **arvestada** negatiivsete päevade väärtust, mis on seadistatud laovarude gruppidele, kauba laovarudele ja/või koondplaanidele. Seda kasutatakse koondplaneerimisel rakendatud viivituse kõikumise perioodi pikendamiseks. Sel viisil saate vältida uute tarnetellimuste loomist, kui olemasolev pakkumine suudab nõudlust pärast lühikest viivitust katta. Selle funktsiooni eesmärk on määrata, kas antud nõudlusele on mõtet luua uus tarnetellimus.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Viivituse kõikumise funktsioonide sisse- või väljalülitamine

Viivituse kõikumise funktsioonide süsteemi kättesaadavaks miseks minge Funktsioonihaldusse [ja](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lülitage sisse järgmised funktsioonid:

- *Negatiivsed päevad planeerimise optimeerimiseks* – see funktsioon lubab laovarude gruppide ja kauba laovarude negatiivsed päevad. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada.
- *Tellimusele tarnimise automatiseerimise koostamine* – see funktsioon võimaldab koondplaanide negatiivsete päevade sätteid. (Lisateavet vt teemast [Teha tellimusele tarnimise automatiseerimine](../make-to-order-supply-automation.md).)

## <a name="delay-tolerance-in-planning-optimization"></a>Viivituse kõikumine plaanimise optimeerimises

Viivituse kõikumine näitab nende päevade arvu, mis on pärast täitmisaega, millal soovite enne uue varude täiendamist oodata, kui olemasolev tarne on juba planeeritud. Viivituse kõikumine määratletakse kalendripäevade, mitte tööpäevade abil.

Koondplaneerimise ajal, kui süsteem arvutab viivituse kõikumise, arvestab see sätet **Negatiivsed päevad**. Negatiivsete päevade **väärtuse saate** seada laovarude **gruppide** lehel, kauba **laovarude** lehel või koondplaanide **lehel**. Kui negatiivsed päevad on määratud rohkem kui ühel tasemel, rakendab süsteem järgmise hierarhia otsustamaks, millist sätet kasutada:

- Kui negatiivsed päevad on koondplaanide **lehel** lubatud, alistab see säte plaani käitamisel kõik negatiivsete päevade sätted.
- Kui negatiivsed päevad on konfigureeritud kauba **laovarude** lehel, alistab see säte laovarude grupi sätte.
- Laovarude gruppide lehel konfigureeritud negatiivsed **päevad** kehtivad ainult juhul, kui vastava kauba või plaani jaoks pole negatiivseid päevi konfigureeritud.

Süsteem seob viivituse kõikumise arvutamise *varaseima täiendamiskuupäevaga*, mis on võrdne tänase kuupäeva ja täitmisajaga. Viivituse kõikumine arvutatakse järgmise valemi abil, *kus max()* leiab kahest väärtusest suurema:

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
