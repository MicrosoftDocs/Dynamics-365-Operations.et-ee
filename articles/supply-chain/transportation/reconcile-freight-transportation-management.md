---
title: Veose vastavusseviimine transpordihalduses
description: Selles artiklis selgitatakse veose vastavusseviimise protsessi.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSFBDetailReconcile, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8472094ba532d531b15dc4e9f120646b2c3bbe96
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017295"
---
# <a name="reconcile-freight-in-transportation-management"></a>Veose vastavusseviimine transpordihalduses

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse veose vastavusseviimise protsessi.

Veose vastavusseviimine võib toimuda käsitsi või olla seadistatud toimuma automaatselt. Veose automaatse vastavusseviimise kasutamiseks tuleb seadistada auditi koondandmed, milles saate määratleda kriteeriumid, mis määravad, millised veoarved automaatselt vastendatakse.

## <a name="the-freight-reconciliation-process"></a>Veose vastavusseviimise protsess
Veohinnad arvutab hinnamootor, mis on seotud vastava vedajaga. Koorma kinnitamisel koostatakse veoarve ja veohinnad kantakse sellele üle. Veohinnad jaotatakse vastavale lähtedokumendile (ostutellimus, müügitellimus ja/või üleviimistellimus) muude kuludena, olenevalt tavapärase arveldusprotsessi puhul kasutatavast seadistusest. Kauba vastavusseviimise protsess (mida nimetatakse ka vastendusprotsessiks) alustatakse kohe, kui veoarve vedajalt saabub. Arve võib võtta vastu elektrooniliselt või paberkandjal. Kui arve saadakse paberkandjal, võite koostada elektroonilise arve, kasutades mallina veoarvet. 

[![Veose vastavusseviimise protsess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Käsitsi vastavusseviimine
Kui viite veose vastavusse käsitsi, tuleb vastendada iga arve rida veoarve reaga või arveldatava koorma ridadega. Selline vastendamine toimub lehel **Veoarve ja arvete võrdlemine**. Kui arve real olev summa ei vasta veoarve summale, tuleb valida vahe jaoks vastavusseviimise põhjus. Kui vastavusseviimisel on mitu põhjust, võite vastendamata summa nende vahel ära jagada. Vastavusseviimise põhjus määrab, kuidas vahesummad pearaamatusse sisestatakse. Kui arvestatakse kogu arve summat, esitatakse see kinnitamiseks ja seejärel tööleht sisestatakse. Järgmine illustratsioon näitab, kuidas koostada veose arvet ja veost vastavusse viia. 
[![Veose vastavusseviimise ülesanded](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automaatne vastavusseviimine
Automaatse vastavusseviimise kasutamiseks tuleb määrata vastavusseviimise graafik ning kasutatavad arved ja vedajad. Vastendamine arve ridadel ja veoarvetel toimub auditi koondandmete ja veose arve tüübi seadistusele. Pärast automaatse vastavusseviimise käitamist tuleb tegeleda arvetega, millele süsteem vastet ei leia. Neid arveid peab siis käsitsi töötlema, enne kui saate kõik arved maksmiseks sisestada.



