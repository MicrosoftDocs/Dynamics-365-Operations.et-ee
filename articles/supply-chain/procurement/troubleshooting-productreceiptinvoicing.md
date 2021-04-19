---
title: Toote sissetulekute ja arvelduse tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada toote sissetulekute ja arveldusega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3522a024261ff6dfffb53f2101139460be7669e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832006"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Toote sissetulekute ja arvelduse tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada toote sissetulekute ja arveldusega töötamisel tekkivaid probleeme.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Ma ei saa sisestada rohkem kui üht arvet ostutellimuse reale, millel on kategooriapõhised kaubad.

Kui soovite arveid sisestada, on kogus kohustuslik. Kui rea terve kogus on arveldatud ainult osalise summana, ei saa te ülejäänud summat teises arves arveldada.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Ostutellimuse kinnitamise ajal kuvatakse tõrge „Objekti viide ei ole seatud” või hankija arve sisestamisel ilmneb erand „Kutsumise sihtmärgi puhul ilmnes erand”.

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Ma ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida.

Te ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida, kui toote sissetuleku ridadel on eri aruandluskuupäevad.

Rakenduse Microsoft Dynamics 365 Supply Chain Management varasemates versioonides oli selles olukorras konsolideerimine lubatud. Kuid selle tava puhul tekivad tihti vead. Loodavate ostutellimuse ridade aruandluskuupäev ei tohi erineda selliste toote sissetuleku ridade aruandluskuupäevast, mille põhjal need ostutellimuse read loodi. (Ostutellimuse ridade aruandluskuupäev ühtib ostutellimuse päises oleva aruandluskuupäevaga.) Seetõttu pole mitme toote sissetuleku konsolideerimine üheks ostutellimuseks enam lubatud.

Aruandluskuupäeva kasutatakse näiteks eelarvereservi ja pandiõiguse puhul. Seetõttu tuleks see säilitada toote sissetulekust ostutellimusele ülemineku ajal.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Toote sissetulekute tühistamise korral saab kandeid sisestada peatatud pearaamatukontole.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui toote sissetulek tühistatakse, lubab süsteem sisestada kandeid peatatud pearaamatukontodele, kuigi põhikontod on peatatud.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Veenduge, et lehe **Ostureskontro parameetrid** vahekaardil **Üldine** oleks suvandi **Sisesta toote sissetulek pearaamatusse** väärtuseks seatud *Jah*.
1. Looge ostutellimus ja lisage tellimuse rida, mille toote kogus on *1000*.
1. Kinnitage ostutellimus.
1. Sisestage toote sissetulek ja kontrollige kandeid.
1. Peatage asjakohased põhikontod *200140* ja *140200*.
1. Tühistage sisestatud toote sissetulek.
1. Pange tähele, et peatatud pearaamatukontodele saab kandeid sisestada.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kandeid saab toote sissetulekute tühistamise korral peatatud pearaamatukontodele sisestada, kuna selline olukord lubab teha õigeid sisestusi.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Toote sissetuleku kandenumbrit tarbitakse isegi siis, kui toote sissetuleku käigus ei looda ühtegi finantskannet.

Kui suvandi **Kumuleerimise kohustus toote sissetulekul** väärtuseks on kauba mudeligrupi puhul seatud *Ei*, siis pearaamatusse sisestusi ei tehta. Sellegi poolest kirjendatakse füüsiline sündmus raamatupidamise otstarbel alammoodulis ja selle sündmuse jaoks on vaja kandenumbrit. See kandenumber on laokannetes viidatud kandenumber.

Me soovitame seada suvandi **Kumuleerimise kohustus toote sissetulekul** väärtuseks *Jah*, nagu on kirjeldatud ajaveebipostituses [Lisakulude sisestamine toote sissetuleku ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Säte „Sisesta pearaamatu kulude kontole” pole sisse lülitatud.

### <a name="issue-description"></a>Probleemi kirjeldus

Probleem ilmneb siis, kui ostutellimust arveldatakse olukorras, kus suvandi **Sisesta pearaamatu kulude kontole** väärtuseks on seatud *Jah* vahekaardil **Arve**, mis asub lehel **Ostureskontro parameetrid**.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
1. Seadke vahekaardil **Arve** suvandi **Sisesta pearaamatu kulude kontole** väärtuseks *Jah*.
1. Avage **Varude haldus \> Seadistus \> Sisestus \> Sisestus**.
1. Tehke kindlaks, et te olete vahekaardil **Ostutellimus** kõik toote ostukulu read kustutanud.
1. Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.
1. Looge ostutellimus. Valige väljal **Hankija konto** suvand *1001 Acme Office Supplies*.
1. Lisage järgmiste sätetega ostutellimuse rida.

    - **Kauba kood:** *D0011 Laser Projector*
    - **Koht:** *1*
    - **Ladu:** *11*
    - **Kogus:** *4*

1. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevus** suvand **Kinnita**.
1. Tehke toimingupaani vahekaardil **Vastuvõtmine** grupis **Loo** valik **Toote sissetulek**.
1. Sisestage dialoogiboksis **Toote sissetuleku sisestamine** väljale **Toote sissetulek** suvaline number ja seejärel valige **OK**.
1. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
1. Sisestage väljale **Number** arve numbrina suvaline arv.
1. Värskendage vastavusseviimise olekut ja sisestage.
1. Pange tähele, et te saate nüüd ostutellimuse põhjal arvet luues järgmise tõrke: „Toote ostukulu kandetüübi kontonumbrit pole olemas”.

### <a name="issue-resolution"></a>Probleemi lahendamine

See sõltub arvete ja arvegruppide parameetrite seadistusest. Lisateavet leiate ajaveebipostitusest [Raamatupidamine ostukulu ja varude muudatuste puhul](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]