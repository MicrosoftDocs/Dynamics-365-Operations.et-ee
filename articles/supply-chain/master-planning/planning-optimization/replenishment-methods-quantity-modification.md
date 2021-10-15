---
title: Varude täiendamise meetodid ja koguse muutmine
description: Selles teemas antakse teavet varude täiendamise meetodite kohta planeerimise optimeerimises. Lisaks selgitatakse, kuidas toote mitme tellimuse kogus mõjutab tulemust.
author: ChristianRytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 017dabb46265769bf727056a9bf1a8c0cfdc99f6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567291"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Varude täiendamise meetodid ja koguse muutmine

[!include [banner](../../includes/banner.md)]

Selles teemas antakse teavet varude täiendamise meetodite kohta planeerimise optimeerimises. Lisaks selgitatakse, kuidas toote mitme tellimuse kogus mõjutab tulemust.

Varude täiendamise meetodeid nimetatakse ka laovarude meetoditeks ja partii suuruse muutmise meetoditeks.

## <a name="coverage-codes"></a>Planeerimise koodid

Planeerimise optimeerimise konfigureerimise abil saab kasutada erinevaid täiendamise meetodeid. Varude täiendusmeetodid on meetodid, mida süsteem kasutab tootele esitatavate nõuete arvutamiseks. Varude täiendamise meetodeid määratletakse laovarude tähistega, mida saate seadistada kas laovarude grupis või tootes.

Planeerimise optimeerimisel saab kasutada järgmisi laovarude tähiseid:

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

Kui te ei määra lehel **Tellimuse vaikesäte** toote väärtust väljal **Mitu** ja kasutate välja *Min./Max.* täiendusmeetod, Planning Optimization täiendab varusid kuni kindla tasemeni, kui prognoositav vaba kogus on alla kindla künnise.

Kui määratlete tootele mitmekordse koguse, kuvatakse väljad *Min./Max.* täiendusmeetod muudab oma käitumist ja arvestab **Mitu** väärtust.

Teisisõnu täiendab plaanimise optimeerimine varusid määratletud maksimumtasemeni, kui eeldatav vaba kaubavaru tase on määratletud miinimumtasemest väiksem. Täienduskogus peab siiski olema **Mitu** väärtuse kordne.

Kui varude täiendamise kogus (erinevus maksimumtaseme ja prognoositud vaba kaubavaru taseme vahel) pole määratletud mitmekordse koguse kordne, kasutab plaanimise optimeerimine esimest võimalikku väärtust, mis koos prognoositud vaba kaubavaru tasemega jääb alla piirnormi. Kui summa on miinimumtasemest väiksem, kasutab plaanimise optimeerimine esimest väärtust, mis koos prognoositava vaba kaubavaruga ületab piirnormi.

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
