---
title: Pakkumistel ja pakkumiskutsetel põhinevad plaanid
description: See artikkel kirjeldab, kuidas seadistada koondplaneerimist, et arvestada pakkumiskutseid ja pakkumiskutseid plaanitud tellimuste loomisel.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690161"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Pakkumistel ja pakkumiskutsetel põhinev plaan

[!include [banner](../../includes/banner.md)]

Pakkumised ja pakkumiskutsed tähistavad võimalikke või isegi tõenäoliselt tulevasi tellimusi. Seetõttu on mõtet neid koondplaneerimise käigus arvestada, nii et lisatarnet saab planeerida olemasolevate pakkumiskutsete alusel ja tõenäosuse, et iga pakkumine muutub tegelikuks tellimuseks. See artikkel kirjeldab, kuidas seadistada koondplaneerimist pakkumiste ja pakkumiskutsete arvesse võtma, kui see loob plaanitud tellimusi.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Koondplaneerimise loomine müügipakkumiste ja/või pakkumiskutsete kaalumiseks

Kasutage järgmist protseduuri, et seadistada koondplaneerimine müügipakkumiste ja/või pakkumiskutsete kaalumiseks.

1. Minge koondplaneerimise **seadistusplaanide \>\> koondplaanide \> juurde**.
1. Valige loendipaanil olemasolev plaan või valige **uue** plaani loomiseks tegevuspaanil uus.
1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Kaasa müügipakkumised** – häälestage see valik valikule *Jah*, et kaaluda müügipakkusi praeguse plaani käivitamisel. Seadke väärtuseks Ei *, et* neid eirata.
    - **Tõenäosuse** protsent – määrake minimaalne usaldustase, mis on vajalik pakkumise kaasamiseks koondplaneerimisse. Koondplaneerimise arvutusse kaasatakse kõik pakkumised, mis loodi võimalustest, mis on selle tõenäosuse protsendi või suurema tõenäosusega. Kõigi pakkumiste kaasamiseks (sh pakkumised, millele ei ole määratud tõenäosust või millega ei ole seotud ühtegi võimalust), seadke selle välja väärtuseks *0* (null). Lisateavet pakkumiste tõenäosuste kohta vt järgmisest jaotisest.
    - **Kaasa pakkumiskutsed –** häälestage see valik valikule *Jah*, et praeguse plaani käivitamisel pakkumiskutseid arvestada. Seadke väärtuseks Ei *, et* neid eirata. Kui otsustate pakkumiskutseid arvestada, loob süsteem neile plaanitud ostutellimused, kuid hankijat ei määrata enne, kui pakkumiskutse on lahendatud. Pakkumiskutsete jaoks loodud plaanitud ostutellimused võivad mõjutada teiste plaanitud tellimuste kogust.

1. Jätkake oma koondplaani seadistamist tavapärasel viisil.

## <a name="assign-and-view-probabilities-for-quotations"></a>Määrake ja vaadake pakkumiste tõenäosusi

Nagu eelmises jaotises mainitud, kaalub koondplaan ainult pakkumisi, mis vastavad või ületavad plaanile määratud tõenäosusläve (kui lävi on määratud). Tõenäosus pole aga iga pakkumise puhul otseselt seatud. Selle asemel pärineb see võimalusest, mida kasutati pakkumise loomiseks. Seetõttu ei **ole otse leheküljel Kõigil pakkumistel loodud pakkumistele määratud tõenäosust või nendega seostatud võimalust ning neid ei loeta koondplaneerimisel mitte kunagi arvesse (** kui tõenäosuse %**välja** väärtuseks ei ole seatud 0 *null*\[).\] Tõenäosuse otstarbel tuleb pakkumine luua võimalusest.

### <a name="create-a-quotation-from-an-opportunity"></a>Pakkumise loomine võimalusest

Kasutage järgmist protseduuri võimalusele tõenäosuse määramiseks ja seejärel looge pakkumine sellest võimalusest.

1. Minge müügi ja **turunduse suhete \> võimaluste \> kõigisse \> võimalustesse**.
1. Valige olemasolev võimalus või valige tegevuspaanil **uus** võimalus.
1. Sisestage võimaluse lehekülg, et tuvastada võimalus nii, nagu soovite. Seadke tõenäosusväljale **kindlasti** sobiv väärtus. Ainult koondplaanid, mis on seadistatud otsima selle või suurema väärtuse tõenäosusi, kaaluvad sellest võimalusest loodud pakkumisi.
1. Valige toimingupaanil nupp **Salvesta**.
1. Tegevuspaani vahekaardil **Võimalus grupis** **Uus valige Müügipakkumine** **·** **või Projektipakkumine, sõltuvalt sellest, millist tüüpi pakkumist soovite luua.**
1. Dialoogiboksis Pakkumise **loomine seadke** väljad vastavalt vajadusele ja seejärel valige **OK**.
1. Luuakse ja avatakse uus pakkumine. Kasutage funktsiooni **Ridade** kiirkaardil tööriistariba, et lisada müügiridu või projektiridu, nagu on pakkumise sisu määratlemiseks nõutud.
1. Valige toimingupaanil nupp **Salvesta**. Seejärel sulgege pakkumine.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Pakkumisele määratud tõenäosuse kuvamine

Ainus viis pakkumisele määratud tõenäosuse vaatamiseks on avada võimalus, mida kasutati pakkumise loomiseks, nagu kirjeldatud järgmises protseduuris.

1. Minge müügi **ja turunduse \> müügipakkumistesse \> Kõik pakkumised**.
1. Kui võimaluse **ID veergu** ei kuvata (see on vaikeinstallis peidetud), järgige neid samme selle ajutiseks näitamiseks. (Teise võimalusena säilitage **Võimaluse ID** veerg on saadaval, looge salvestatud [vaade,](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) mis seda sisaldab.)

    1. Valige ja hoidke all (või paremklõpsake) ruudustikus ning valige käsk Lisa **veerud**.
    1. Leidke dialoogiboksis **Veergude** lisamine rida, **kus välja väärtuseks** *on seatud Võimalus*, **ja märkige selle** rea puhul ruut Vali.
    1. Valige **suvand** Värskenda, et lisada valitud veerg kõigile **pakkumiste** lehele.

1. Otsige ruudustikust üles vastava pakkumise rida. Seejärel valige **veerus Võimaluse ID** selle rea väärtus.

    > [!NOTE]
    > Kui otsite projektipakkumist, peate võib-olla valima veeru Pakkumise **tüübi** päise ja filtri tühjendama. Vaikeinstallis on see filter seadistatud nii, et kuvataks ainult müügipakkumised.

1. Seotud võimalus on avatud. Nüüd saate vaadata ja redigeerida tõenäosuse **väärtust** vastavalt vajadusele.
