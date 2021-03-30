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
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af7bbb500de25e0a796147fae42cd7d943be9df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205222"
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

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Veoarvete vastendamine veose arvetega, kasutades automaatset ja käsitsi vastavusseviimist

*Vastendamine* on igale veoarvele vastavate veose arvete otsimise protsess. Seda saab teha, vastendades arveread ükshaaval (käsitsi vastendamine) või vastendades kõik saadaolevad arved korraga (automaatne vastendamine).

### <a name="auto-matching"></a>Automaatne vastendamine

Kui vastendate mitu veoarvet sama veose arvega, toimib automaatse vastendamise protsess järgmiselt.

1. Kõik veoarved, mida ei vastendata, sorditakse summa alusel suurima summaga esimesena.
1. Veoarveid vastendatakse ükshaaval, kuni veoarvel puudub positiivne summa.
1. Sõltuvalt auditi koondandmete seadistusest ja veose arvete jääksummast määratakse järelejäänud summa.

### <a name="manual-matching"></a>Käsitsi vastavusse viimine

Vastendamiseks on saadaval kõik positiivsete summadega veoarved. Sarnaselt automaatsele vastendamisele, saab kasutaja vastendada veoarved ainult negatiivsete summadega veoste arvetega, mis pole täielikult vastendatud.

### <a name="example"></a>Näide

Oletame, et teil on veoarve (FB) summaks 1500 ja olete loonud kolm veose arvet ühe arv reaga iga arve jaoks järgmiste sätetega.

- Algne veoarve (FB): summa 1500
- Arve 1 (Inv1): summa 1000
- Arve 2 (Inv2): summa 600
- Arve 3 (Inv3): summa –100

#### <a name="automatic-matching-result"></a>Automaatse vastendamise tulemus

Automaatne vastendamine käivitab järgmise järjestuse.

1. Sordi kõik veoarved summa alusel kahanevalt: Inv1 -> Inv2 -> Inv3.
1. Vastenda Inv1 FB-ga. Inv1-le on vastendatud 1000 ja FB-le on järele jäänud summa 500, seega on olekuks *Osaliselt vastendatud*.
1. Vastenda Inv2 FB-ga. Inv2-le on vastendatud 500 ja FB-le on järele jäänud summa 0, seega on olekuks *Täielikult vastendatud*.
1. Kuna FB on nüüd täielikult vastendatud, siis arvet Inv3 ei töödelda.

#### <a name="manual-matching-result"></a>Käsitsi vastendamise tulemus

Käsitsi vastendamiseks varieeruvad tulemused olenevalt vastendamise järjestusest, nagu näidatud järgmistel näidisjuhtumitel.

##### <a name="manual-matching-case-1"></a>Käsitsi vastendamise juhtum 1

Üks moodus käsitsi vastendamiseks on jätkata järgmiselt.

1. Vastenda FB Inv1-ga. FB-le on järele jäänud summa 500, seega on olekuks *Osaliselt vastendatud*.
1. Vastenda Inv2 FB-ga. Inv2-le on vastendatud 500 ja FB-le on järele jäänud summa 0, seega on olekuks *Täielikult vastendatud*.
1. Inv3 käsitsi vastendamisel ei leia te vastendamata veose arveid.

See juhtum on põhimõtteliselt sama, mis automaatne vastendamine

##### <a name="manual-matching-case-2"></a>Käsitsi vastendamise juhtum 2

Teine moodus käsitsi vastendamiseks on jätkata järgmiselt.

1. Vastenda Inv3 FB-ga. Nüüd on FB jääksumma 1600, mis on sama, mis negatiivse 100 lahutamisel 1500-st. Nii FB kui ka Inv3 vastendatud kogus on –100.
1. Vastendage Inv1 ja Inv2 FB-ga üksteise järel. FB on täielikult vastendatud.

Nagu see näide näitab, tuleks veose arveid vastendada negatiivsete summadega ainult käsitsi. See tagab, et veose arveid ja negatiivseid summasid oleks võimalik vastendada veose arvega, mis ei ole täielikult vastendatud, kuna see võimaldab teil kontrollida sobiva järjestuse järjekorda.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]