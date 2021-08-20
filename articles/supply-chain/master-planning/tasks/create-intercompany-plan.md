---
title: Kontsernisisese plaani loomine
description: See protseduur näitab, kuidas luua kontsernisisest plaani.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da2859a3cd63a497ffe62eb6d8831726d2d85d878de2158e911fe7066daa3fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746180"
---
# <a name="create-an-intercompany-plan"></a>Kontsernisisese plaani loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua kontsernisisest plaani. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

## <a name="set-up-an-intercompany-planning-group"></a>Kontsernisisese plaanimisgrupi seadistamine

1. Paanil **Navigeerimispaan** avage **Moodulid > Koondplaneerimine > Kontsernisisesed plaanimisgrupid**.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Nimi väärtuse 10 järgi.
3. Märkige loendis valitud rida.
4. Valige **Kustuta**. See etapp on vajalik kontsernisisese plaanimistsükli lühendamiseks.   Kontsernisisene plaanimine käivitab kõigis ettevõtetes koondplaneerimise plaanimisgrupis, alustades madalaimast plaanimisjärjestusest.  
5. Valige **Jah**.
6. Sulgege leht.

## <a name="create-an-intercompany-master-plan"></a>Kontsernisisese põhiplaani loomine

1. Paanil **Navigeerimispaan** avage **Moodulid > Koondplaneerimine > Tööruumid > Koondplaneerimine**.
2. Valige **Kontsernisisene koondplaneerimine**.  
3. Väljal **Kontsernisisene plaanimisgrupp** valige rippmenüü nuppu, et avada otsing.
4. Valige loendis link valitud reas. Valige kontsernisisene plaanimisgrupp 10.  
5. Väljale **Kontsernisisese plaanimise iteratsioonide arv** sisestage "2". Kontsernisisesel plaanimisgrupil 10 on kaks liiget. Selleks, et lisada lähteettevõtte (USMF) viivitused klientettevõtte (DEMF) ees, on vaja käivitada kontsernisisene plaanimine mõlemal ettevõttel kaks korda. Esimene iteratsioon lisab nõudluse ja tuvastab viivitused lähteettevõttes (USMF). Teine iteratsioon lisab viivitused USMF-ilt DEMF-ile.  
6. Väljal **Esimene iteratsioon** valige "Taasloomine".
7. Väljal **Järgnevad iteratsioonid** valige "Taasloomine".
8. Väljale **Lõimede arv** sisestage arv. See tähistab planeerimises kasutatavate paralleelsete lõimede arvu.  
9. Valige nupp **OK**.

## <a name="view-the-result-of-the-plan"></a>Plaani tulemuse vaatamine

1. Väljal **Plaan** valige ripploendi nuppu, et avada otsing.
2. Valige loendis link valitud reas. Valige valiku StaticPlan linki. Peate olema ettevõttes USMF.  
3. Valige **Plaanitud tellimused**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]