---
title: Veose vastavusseviimine transpordihalduses
description: Selles artiklis selgitatakse veose vastavusseviimise protsessi.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ab7d21d7a75e2c954831a254bb339d9cf5746d9d
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Veose vastavusseviimine transpordihalduses

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse veose vastavusseviimise protsessi.

Veose vastavusseviimine võib toimuda käsitsi või olla seadistatud toimuma automaatselt. Veose automaatse vastavusseviimise kasutamiseks tuleb seadistada auditi koondandmed, milles saate määratleda kriteeriumid, mis määravad, millised veoarved automaatselt vastendatakse.

## <a name="the-freight-reconciliation-process"></a>Veose vastavusseviimise protsess
Veohinnad arvutab hinnamootor, mis on seotud vastava vedajaga. Koorma kinnitamisel koostatakse veoarve ja veohinnad kantakse sellele üle. Veohinnad jaotatakse vastavale lähtedokumendile (ostutellimus, müügitellimus ja/või üleviimistellimus) muude kuludena, olenevalt tavapärase arveldusprotsessi puhul kasutatavast seadistusest. Kauba vastavusseviimise protsess (mida nimetatakse ka vastendusprotsessiks) alustatakse kohe, kui veoarve vedajalt saabub. Arve võib võtta vastu elektrooniliselt või paberkandjal. Kui arve saadakse paberkandjal, võite koostada elektroonilise arve, kasutades mallina veoarvet. 

[![Veose vastavusseviimise protsess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Käsitsi vastavusseviimine
Kui viite veose vastavusse käsitsi, tuleb vastendada iga arve rida veoarve reaga või arveldatava koorma ridadega. Selline vastendamine toimub lehel **Veoarve ja arvete võrdlemine**. Kui arve real olev summa ei vasta veoarve summale, tuleb valida vahe jaoks vastavusseviimise põhjus. Kui vastavusseviimisel on mitu põhjust, võite vastendamata summa nende vahel ära jagada. Vastavusseviimise põhjus määrab, kuidas vahesummad pearaamatusse sisestatakse. Kui arvestatakse kogu arve summat, esitatakse see kinnitamiseks ja seejärel tööleht sisestatakse. Järgmine illustratsioon näitab, kuidas koostada Microsoft Dynamics 365 for Finance and Operationsis veose arvet ja veost vastavusse viia. 
[![Veose vastavusseviimise toiming Dynamics AX-is](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automaatne vastavusseviimine
Automaatse vastavusseviimise kasutamiseks tuleb määrata vastavusseviimise graafik ning kasutatavad arved ja vedajad. Vastendamine arve ridadel ja veoarvetel toimub auditi koondandmete ja veose arve tüübi seadistusele. Pärast automaatse vastavusseviimise käitamist tuleb tegeleda arvetega, millele süsteem vastet ei leia. Neid arveid peab siis käsitsi töötlema, enne kui saate kõik arved maksmiseks sisestada.




