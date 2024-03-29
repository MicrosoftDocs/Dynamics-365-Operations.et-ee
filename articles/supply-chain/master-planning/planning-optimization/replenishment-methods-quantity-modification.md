---
title: Varude täiendamise meetodid ja koguse muutmine
description: See artikkel annab teavet täiendamismeetodite kohta. Lisaks selgitatakse, kuidas toote mitme tellimuse kogus mõjutab tulemust.
author: t-benebo
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0fe6c1f49bc0f6887f1b29118c1fee7a6222f
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739752"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Varude täiendamise meetodid ja koguse muutmine

[!include [banner](../../includes/banner.md)]

See artikkel annab teavet täiendamismeetodite kohta. Lisaks selgitatakse, kuidas toote mitme tellimuse kogus mõjutab tulemust.

Varude täiendamise meetodeid nimetatakse ka laovarude meetoditeks ja partii suuruse muutmise meetoditeks.

## <a name="coverage-codes"></a>Planeerimise koodid

Koondplaneerimise konfigureerimise abil saab kasutada erinevaid täiendamise meetodeid. Varude täiendusmeetodid on meetodid, mida süsteem kasutab tootele esitatavate nõuete arvutamiseks. Varude täiendamise meetodeid määratletakse laovarude tähistega, mida saate seadistada kas laovarude grupis või tootes.

Kasutada saab järgmisi laovarude koode:

- **Periood** – varude täiendamise meetod, mis koondab toote nõudluse teatud perioodi jooksul ühte tellimusse. Tellimus planeeritakse perioodi esimesele päevale ja selle kogus vastab netosummale määratud perioodi jooksul. Periood algab toote esimese nõudega ja katab määratud pikkusega aja jooksul. Järgmine periood algab toote järgmiste nõuetega. *Perioodi* laovarude koodi kasutatakse sageli mitteaimatavate varude joonistamiseks, hooajast mõjutatud toodete või kallite toodete jaoks. Järgmisel joonisel on toodud näide.

    ![Perioodi laovarude koodi kasutamise näide.](./media/coverage-code-period.png "Perioodi laovarude koodi kasutamise näide")

- **Nõue** – varude täiendamise meetod, mille puhul süsteem loob tootele vajaduse korral plaanitud ostu-, edastamis- või tootmistellimuse. Seda meetodit kasutatakse kallite toodete puhul, millel on vahelduv nõudlus. *Nõude* laovarude koodi kasutatakse sageli konfigureeritavate toodete või tellimuse järgi valmistatavate stsenaariumide puhul. Järgmisel joonisel on toodud näide.

    ![Nõude laovarude koodi kasutamise näide.](./media/coverage-code-requirement.png "Nõude laovarude koodi kasutamise näide")

- **Min./Max.** – Varude täiendamise meetod põhineb laovarude tasemel. See määratleb varude täiendamise kindla tasemeni, kui prognoositav vaba kaubavaru tase on allpool konkreetset künnist. Varude täiendamise kogus on maksimaalse taseme ja prognoositava vaba taseme vaheline erinevus. Väljad *Min./Max.* varude koodi kasutatakse sageli prognoositavate varude joonistamiseks, kõrgete jooksukaupade või odavamate toodete jaoks. Järgmisel joonisel on toodud näide.

    ![Min./Max. laovarude koodi kasutamise näide.](./media/coverage-code-min-max.png "Min./Max. laovarude koodi kasutamise näide")

- **Käsitsi** – varude täienduse meetodi puhul ei soovita süsteem toote ostmist, üleandmist ega tootmistellimusi. Selle asemel vastutab toote planeerija toote täiendamiseks vajalike tellimuste loomise eest. *Käsitsi* laovarude koodi kasutatakse sageli toodete puhul, mille jaoks süsteemi loodud plaanitud tellimusi ei taheta.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Tellimuse koguse mõju tellimuse vaikesätetest

Väljaantud toote lehel **Tellimuse vaikesätted** saate kiirkaartidel **Ostutellimus**, **Laovarud** ja **Müügitellimus** määrata kõik järgmised koguse sätted. (Kiirkaarti **Laovarud** kasutatakse nii üleviimis- kui ka tootmistellimuste puhul.)

- **Mitu** – plaanitud tellimused on selle koguse kordse väärtusega.

    Näiteks kui välja **Mitu** väärtuseks on seatud *5*, võib tellimus olla koguses 5, 10, 15, 20 jne.

- **Minimaalne tellimuse kogus** – plaanitud tellimused ei ole määratud väärtusest väiksemad.

    Näiteks kui välja **Min. tellimuse kogus** väärtuseks on seatud *10*, luuakse plaanitud tellimus kogusele 10, isegi kui nõudluse täitmiseks on vaja ainult nelja tellimust.

- **Maksimaalne tellimuse kogus** – plaanitud tellimused ei üle määratud väärtust. Kui nõudlus on suurem kui **Maksimaalne tellimuse kogus**, luuakse selle katmiseks mitu plaanitud tellimust.

    Näiteks kui välja **Maksimaalne tellimuse kogus** väärtuseks on seatud *100* ja nõudlus on 450, luuakse neli plaanitud tellimust kogusega 100 ja üks plaanitud tellimus kogusega 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Näited varude täiendamisest, mis kasutavad välja Min./Max. laovarude kood

Kui te ei määra lehel **Tellimuse vaikesäte** toote väärtust väljal **Mitu** ja kasutate välja *Min./Max.* Varude täiendamise meetod, koondplaneerimine täiendab varusid kindla tasemeni, kui prognoositud vaba kaubavaru tase on allpool kindlat läve.

Kui määratlete tootele mitmekordse koguse, kuvatakse väljad *Min./Max.* täiendusmeetod muudab oma käitumist ja arvestab **Mitu** väärtust.

See tähendab, et koondplaneerimine täiendab varusid endiselt määratletud maksimaalse tasemeni, kui prognoositud vaba kaubavaru on määratletud minimaalsest tasemest väiksem. Täienduskogus peab siiski olema **Mitu** väärtuse kordne.

Kui varude täiendamise kogus (erinevus maksimaalse taseme ja prognoositava vaba laovaru taseme vahel) ei ole määratletud kordse koguse kordne, kasutab koondplaneerimine esimest võimalikku väärtust, mis koos prognoositud vaba kaubavaru tasemega on allpool maksimaalset taset. Kui summa on minimaalsest tasemest väiksem, kasutab koondplaneerimine esimest väärtust, mis koos prognoositud vaba kaubavaruga on maksimaalsest tasemest kõrgemal.

Järgmistes alajaotistes on toodud mõned näited, mis näitavad, kuidas toote mitmekordne tellimuse kogus mõjutab välja *Min./Max.* varude täiendamise meetod.

### <a name="example-1"></a>Näide 1

Toote konfiguratsioon on järgmine:

- **Laovarude kood**: *Min./Max.*
- **Miinimum:** *15*
- **Maksimum:** *22*
- **Mitu:** *0*

Tootel on 10 vaba kaubavaru tükki ja muud nõudlust ega pakkumist ei ole.

Koondplaneerimise käivitamisel luuakse varude täiendamiseks maksimumkoguseni planeeritud tellimus 12 tüki kohta.

### <a name="example-2"></a>Näide 2

Toote konfiguratsioon on järgmine:

- **Laovarude kood**: *Min./Max.*
- **Miinimum:** *15*
- **Maksimum:** *22*
- **Mitu:** *5*

Tootel on 10 vaba kaubavaru tükki ja muud nõudlust ega pakkumist ei ole.

Koondplaneerimise käivitamisel luuakse 10 tüki plaanitud tellimust (kuna 15 täiendusühikut pluss 10 vaba kaubavaru tükki ületavad maksimumkoguse).

### <a name="example-3"></a>Näide 3

Toote konfiguratsioon on järgmine:

- **Laovarude kood**: *Min./Max.*
- **Miinimum:** *21*
- **Maksimum:** *24*
- **Mitu:** *5*

Tootel on 10 vaba kaubavaru tükki ja muud nõudlust ega pakkumist ei ole.

Koondplaneerimise käivitamisel luuakse 15 tüki plaanitud tellimust (kuna 10 täiendusühikut pluss 10 vaba kaubavaru tükki on vähem, kui miinimumkogus).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
