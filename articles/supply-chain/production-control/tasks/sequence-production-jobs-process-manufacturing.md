---
title: Tootmistööde järjestamine tootmisprotsessiks
description: See protseduur kasutab värvitooteid näitena näitamaks, kuidas järjestada plaanitud tellimusi vastavalt värvi ja suuruse prioriteedile.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 461893c355ac2ebf8124591f93d025cae49081fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810967"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Tootmistööde järjestamine tootmisprotsessiks

[!include [banner](../../includes/banner.md)]

See protseduur kasutab värvitooteid näitena näitamaks, kuidas järjestada plaanitud tellimusi vastavalt värvi ja suuruse prioriteedile. Selle protseduuri loomiseks kasutati demoettevõtte USPI-i andmeid. See protseduur on mõeldud tootmisplaanijale.


## <a name="run-master-planning-for-uspi"></a>Koondplaneerimise käitamine USPI jaoks
1. Avage Koondplaneerimine > Koondplaneerimine > Käivita > Koondplaneerimine.
2. Klõpsake väljal Koondplaan otsingu avamiseks ripploendi nuppu.
3. Klõpsake loendis valitud real olevat linki.
    * Tehke valik MasterPlan.  
4. Klõpsake nuppu OK.
    * See käivitab koondplaneerimise, sh jada protsessi. Protsessiks võib kuluda mõni minut.  

## <a name="view-planned-orders-for-the-paint-products"></a>Värvitoodete plaanitud tellimuste vaatamine
1. Avage Koondplaneerimine > Koondplaneerimine > Plaanitud tellimused.
2. Laiendage kiirinfor Kauba üksikasjad.
3. Laiendage kiirinfot Graafiku üksikasjad.
4. Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
    * Tehke valik MasterPlan.  
6. Klõpsake loendis valitud real olevat linki.
7. Kasutage kiirfiltrit, et filtreerida väli Kaubakood väärtuse P300 alusel.
    * Avage ja kerimige paremale, et näha tellimuse kuupäeva ja tarnekuupäeva. Pange tähele, et nendel kaupadel on tellimuse kuupäev täna ja plaanitud tellimuste tarnekuupäevad ei ole järjestatud värvi ja pakendi suuruse prioriteedi järgi, nagu on näidatud toote nimes. Toote nime ja prioriteedi nägemiseks hõljutage kursorit kaubakoodil.  

## <a name="sequence-planned-orders-for-paint"></a>Seeria plaanitud tellimused värvi jaoks
1. Sulgege leht.
2. Avage Koondplaneerimine > Koondplaneerimine > Järjestatud plaanitud tellimused.
3. Laiendage kiirinfor Kauba üksikasjad.
4. Laiendage kiirinfot Graafiku üksikasjad.
    * Märkus. Siin näete, et plaanitud tellimuste alguskuupäevad/-kellaajad on järjestatud vastavalt värvi ja pakendi suuruse järgi 28-päevase ajavahemiku jooksul. Need perioodid määratletakse numbriga väljal Kampaania. Seeria plaanitud tellimuse vorm toimib nagu tavaline plaanitud tellimuse vorm ja tootmise plaanija saab kinnitada siin plaanitud tellimused.  
5. Märkige kõik read.
6. Klõpsake suvandit Nõustu.
    * See värskendab plaanitud tellimused valitud toimingute järjestusega, milleks on kas Edasi lükata või Varasem.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Plaanitud tellimuste seeria kinnitamine
1. Sulgege leht.
2. Avage Koondplaneerimine > Koondplaneerimine > Plaanitud tellimused.
3. Laiendage kiirinfor Kauba üksikasjad.
4. Laiendage kiirinfot Graafiku üksikasjad.
5. Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
    * Tehke valik MasterPlan.  
7. Klõpsake loendis valitud real olevat linki.
8. Kasutage kiirfiltrit, et filtreerida väli Kaubakood väärtuse P300 alusel.
    * Pange tähele, et tellimused on nüüd järjestatud vastavalt värvi ja suuruse prioriteedile ning plaanitud tellimused algavad varaseimal tellimuse kuupäeval ja tarnekuupäeval. Kinnitage veerg Tellimuse kuupäev või Alguskuupäev kiiinfos Graafiku üksikasjad.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]