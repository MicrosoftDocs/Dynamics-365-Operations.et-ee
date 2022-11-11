---
title: Nõudlusepõhine planeerimine
description: Artikkel kirjeldab, kuidas luua planeeritud tellimusi kaupadele, mis on seadistatud dekodeerimispunktidena.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740298"
---
# <a name="demand-driven-planning"></a>Nõudlusepõhine planeerimine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Artikkel kirjeldab, kuidas luua planeeritud tellimusi kaupadele, mis on seadistatud dekodeerimispunktidena.

## <a name="net-flow-and-qualified-demand"></a>Netovoog ja kvalifitseeritud nõudlus

Koondplaneerimise ajal rakendab süsteem netovoo kontseptsiooni, et luua tegelik vaba kaubavaru, lisaks tellimusel oleval laovarul (olemasolevad tarnetellimused, mida ei ole veel vastu võetud) põhinev tegelik vaba kaubavaru, miinus see, *mida nimetatakse kvalifitseeritud eelolevaks müügiks, nagu näidatud järgmises illustratsioonis* *.* Kui süsteem määrab, millisesse puhvertsooni kaup kuulub ja millisesse tellitud kogusesse see peaks kuuluma, siis annab see hinnangu netovoole, mitte tegelikule vabale kaubavarule.

![Voo arvutamise diagrammi näide.](media/ddmrp-net-flow-example.png "Voo arvutamise diagrammi näide")

Kui plaanitud tellimus käivitatakse planeerimise käivitamisel, on tellitud kogus maksimaalne tase miinus netovoog. Tellimuse prioriteedi määramiseks kasutab süsteem vajadusekuupäevade [asemel prioriteedipõhist](priority-based-planning.md) planeerimisfunktsiooni. Nõudlusepõhiste materjalinõuete planeerimine (DDMRP) määrab tellitud kogusel põhineva plaanitud tellimuse prioriteedi maksimaalse laoseisu protsendina. Eelmise näite korral on tellitud kogus 53% maksimaalsest kogusest. Varude täiendamise tellimuse prioriteet on seega 53. (Konteksti puhul on 0 kõrgeim prioriteet ja 100 on madalaim prioriteet.)

*Kvalifitseeritud* nõudlus on tähtajani jääv nõudlus pluss tänane nõudlus ja tulevikus kvalifitseeritud tellimused. Järgmine näide näitab tänase (12. juuni) ja järgmise kolme päeva nõudluse tasemeid. DDMRP võimaldab teil seadistada tellimuse läve, et tuvastada nõudlus, mis ületab tavalist ootust. Kui läveks on seatud 25 tk, kvalifitseeruvad kaks joonisel näidatud tulevasest kuupäevast tellimuse lõppkuupäevadeks. Peate iga toote jaoks **tellimuse** läve individuaalselt määrama, kasutades selle laovarude lehte, [nagu kirjeldatud dekodeerimispunkti kaubale puhvrite häälestamises](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Kvalifitseeritud nõudluse arvutamise diagrammi näide.](media/ddmrp-net-qualified-demand-example.png "Kvalifitseeritud nõudluse arvutamise diagrammi näide")

Kuna tähtajani ei ole nõudlust, saate nüüd lisada tänase nõudluse (18) kahe tellimuse kogusele (29 ja 26), et saada kvalifitseeritud nõudlus 73. Kuigi 23. juunil on nõudlus olemas, pange tähele, et seda ei kaasata netovoo arvutamisse, sest DDMRP käivitab plaanitud tellimuse erinevalt traditsioonilistest laovarude plaanimise gruppidest.

## <a name="generating-planned-orders-with-ddmrp"></a>Plaanitud tellimuste loomine DDMRP-ga

Kui kauba netovoog langeb järeltellimuse punktist allapoole, loob süsteem planeerimise käivitamisel uue plaanitud tellimuse. Kui kasutate DDMRP-i, käitatakse planeerimist tavaliselt iga päev. Seega kontrollite varude tasemeid kord päevas, et määrata, milliseid kaupu tuleb täiendada.

Järgmine näide näitab näidet olukorrast, kus teil on tellimus 20. juunil 18 tükki, 29 tükki 21. juunil, 26 tükki 22. juunil ja 20 tükki 23. juunil. Kuna lävi on seatud 25 tükile, on kaks neist tellimustest märgitud tükiks. Sellest kaubast on vaba 220 tükki.

![Planeerimis näide 1.](media/ddmrp-planning-example-1.png "Planeerimis näide 1")

Kui käivitate nüüd koondplaneerimise, loob see plaanitud tellimuse, kui netovoog langeb ümbertellimuse punktist madalamale (selles näites on 219 tükki).

![Planeerimis näide 2.](media/ddmrp-planning-example-2.png "Planeerimis näide 2")

Selle näite alusel toodetakse plaanitud ostutellimus kogusest 130, mis võrdub maksimaalse taseme ja netovoo vahega. Plaanitud tellimusele määratakse prioriteet 53,07, mis põhineb selle protsendil maksimaalsest kogusest. Kuna need väärtused leiti 20. juunil, loob süsteem plaanitud tellimuse 20. juunil pluss kauba dekodeeritud täitmisaeg (selles näites viis tööpäeva). Seega, kuna viis tööpäeva on üks nädal alates tänasest, on plaanitud tellimuse kuupäev 27. juuni.

> [!NOTE]
> Koondplaneerimine arvutab dekodeeritud kaubad ainult DDMRP-i kasutades. Kõik muud kaubad arvutatakse standardse materjalinõuete plaanimise (MRP) abil.
