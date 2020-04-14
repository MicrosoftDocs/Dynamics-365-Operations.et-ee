---
title: Potentsiaalne klient-raha ja kaksikkirjutamine
description: See teema annab teavet potentsiaalne klient-raha kaksikkirjutamises kohta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 12a0e07d1c60a359b3ba6c0d20176927ffe89431
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172804"
---
# <a name="prospect-to-cash-in-dual-write"></a>Potentsiaalne klient-raha kaksikkirjutamises

[!include [banner](../../includes/banner.md)]



Enamiku ettevõtete oluline eesmärk on muuta potentsiaalsed kliendid klientideks ja seejärel säilitada nende klientidega pidev ärisuhe. Rakendustes Microsoft Dynamics 365 toimub potentsiaalne klient-raha protsess pakkumiste või tellimuste töötlemise töövoogude kaudu ning finantsid lepitakse kokku ja kinnitatakse. Potentsiaalse kliendi-raha integreerimine kaksikkirjutamisega loob töövoo, mis võtab pakkumise ja tellimuse, mis on pärit kas Dynamics 365 Salesist või Dynamics 365 Supply Chain Management-st, ja teeb pakkumise ja tellimuse kättesaadavaks mõlemas rakenduses.

Rakendusliidestes pääsete juurde reaalaja töötlemisolekutele ja arveteabele. Seetõttu saate hõlpsalt hallata selliseid funktsioone nagu toote ladustamine, laoseisu käitlemine ja täitmine Supply Chain Managementis, ilma et peaksite pakkumised ja tellimused uuesti looma.

![Kaksikkirjutamise andmevoog järjestuses potentsiaalne klient-raha](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügipakkumiste sünkroonimist peate uuendama järgmised sätted.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

Müükides avage jaotis **Sätted \> Administreerimine \> Süsteemisätted \> Müügid** ja veenduge, et kasutusel on järgmised sätted.

- Süsteemisuvand **Kasuta süsteemi hinnaarvutust** on seatud väärtusele **Jah**.
- Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="sites-and-warehouses"></a>Saidid ja laod

Supplu Chain Managementi puhul on **Saidi** ja **Lao** väljad vajalikud pakkumise ridade ja tellimuse ridade jaoks. Kui seate saidi ja lao vaiketellimuse sätte, seatakse need väljad automaatselt, kui lisate toote pakkumise reale või tellimuse reale. 

### <a name="number-sequences-for-quotations-and-orders"></a>Pakkumiste ja tellimuste numbrijärjestused

Supply Chain Managementi ja Müügi numbrijärjestused ei ole ühendatud, kui pakkumised ja tellimused luuakse ja sünkroonitakse Müükides ja Tarneahelahalduses. Kui müügitellimus, mis on loodud Müükides, sünkroonitakse Supply Chain Managementiga, on sellel Supply Chain Managementis sama müügitellimuse number. Tagamaks, et müügitellimuse numbrit ei dubleerita, peate kahes rakenduses kasutama erinevaid numbrijärjestussüsteeme.

Näiteks on Supply Chain Managementi numbrijärjestus **1, 2, 3, 4, 5,...** ja Müükide numbrijärjestus on **100, 99, 98,...**. Kui loote Müükides 100 müügitellimust, luuakse lõpuks tellimuse number, mis on juba olemas Supply Chain Managementis. Teisisõnu lõpuks kaks numbrijärjestust kattuvad, kui müügitellimused on loodud Supply Chain Managementis ja Müükides. Selle asemel võite kasutada Supply Chain Managementis numbrijärjestust **F1, F2, F3,...** ja Müükides numbrijärjestust **C1, C2, C3,...** . Need numbrijärjestused ei moodusta kunagi dubleeritud müügitellimuse numbreid.

## <a name="sales-quotations"></a>Müügipakkumised

Müügipakkumised võib luua rakenduses Müügid või Supply Chain Management. Kui loote pakkumise Müükides, sünkroonitakse see reaalajas Supply Chain Managementiga. Kui loote pakkumise Supply Chain Managementis, sünkroonitakse see reaalajas Müükidega. Pidage meeles järgmiseid punkte.

+ Toote pakkumisele saate lisada allahindluse. Sel juhul sünkroonitakse allahindlus Supply Chain Managementiga. Päise välju **Allahindlus**, **Tasud** ja **Maks** juhitakse seadistusega rakenduses Supply Chain Management. See seadistus ei toeta integreerimise vastendamist. Seeasemel välju **Hind**, **Allahindlus**, **Tasu**ning **Maks** säilitatakse ja käsitsetakse Supply Chain Managementis.
+ Väljad **Allahindluse %**, **Allahindlus**ja **Veose kogus** müügipakkumise päises on kirjutuskaitstud väljad.
+ Väljad **Veotingimused**, **Tarnetingimused**, **Saatmisviis**ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtusvastenduse, mis on vastab andmetele neis organisatsioonides, mille vahel üksust sünkroonitakse.

## <a name="sales-orders"></a>Müügitellimused

Müügitellimused võib luua rakenduses Müügid või Supply Chain Management. Kui loote müügitellimuse Müükides, sünkroonitakse see reaalajas Supply Chain Managementiga. Samuti kui loote müügitellimuse Supply Chain Managementis, sünkroonitakse see reaalajas Müükidega. Pidage meeles järgmiseid punkte.

+ Tellimusi saate aktiveerida ja sünkroonida Müükides ainult siis, kui kõik tellimuses olevad tooted pärinevad rakendusest Finance and Operations . Seetõttu ei saa seal olla sissekirjutatud tooteid.
+ Allahindluse arvutamine ja ümardamine:

    - Rakenduse Sales allahindluse arvutamise mudel erineb rakenduse Supply Chain Management allahindluse arvutamise mudelist. Rakenduses Supply Chain Management võib müügirea lõplik allahindluse summa olla allahindluse summade ja allahindluse protsentide kombinatsiooni tulemus. Kui lõplik allahindluse summa jagatakse real oleva kogusega, võib ilmneda ümardamine. Seda ümardamist ei võeta aga arvesse, kui ümardatavat ühikupõhist allahindluse summat sünkroonitakse Müükidega. Selleks et rakenduse Supply Chain Management müügirea kogu allahindluse summa õigesti sünkroonida rakendusega Müügid, tuleb kogusumma sünkroonida rea kogusega jagamata. Seetõttu peate rakenduses Müügid määrama allahindluse arvutamise meetodiks **Rea kaup** .
    - Kui müügitellimus rakenduses Müügid sünkroonitakse rakendusega Supply Chain Management, kasutatakse terve rea allahindluse summat. Kuna rakenduses Supply Chain Management pole ühtegi välja, millele saab salvestada rea kogu allahindluse summa, jagatakse summa kogusega ja salvestatakse väljale **Rea allahindlus**. Selle jagamisega kaasnev ümardamine talletatakse müügirea väljale **Müügitasud** .

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Näide: Müükide sünkroonimine Supply Chain Managementiga

Teil on järgmine müügitellimus:

+ **Sales:** kogus = 3, allahindlus rea kohta = 10.00 USA dollarit
+ **Tarneahelahaldus:** kogus = 3, rea allahindluse summa = $3,33, müügitasu =-$0,01

Kui sünkroonite Supply Chain Managementi Müükidega, saate järgmise tulemuse:

+ **Tarneahelahaldus:** kogus = 3, rea allahindluse summa = $3,33, müügitasu =-$0,01
+ **Sales:** kogus = 3, allahindlus rea kohta = (3 × 3.33) + 0.01 = 10.00 USA dollarit

## <a name="dual-write-solution-for-sales"></a>Kaksikkirjutamise lahendus Müükidele

Üksusele **Tellimus** lisati uued väljad ja need kuvatakse lehel. Enamik neist väljadest kuvatakse Müükide vahekaardil **Integreerimine** . Seal on mõned eriväljad:

+ Väljal **Töötlemisolek** kuvatakse tellimuse töötlemise olek rakenduses Supply Chain Management. See väli on lukus ja näitab ainult Supply Chain Managementi tellimuse olekut. Saadaval on järgmised väärtused:

    + **Aktiivne**: olek pärast rakenduses Sales tellimuse aktiveerimist nupuga **Aktiveeri**.
    + **Kinnitatud**
    + **Tarnitud**
    + **Arveldatud**
    + **Osaliselt tarnitud**
    + **Osaliselt arvele kantud**
    + **Komplekteeritud**
    + **Tühistatud**

    Järgmine tabel näitab, kuidas töötlemisolek on vastendatud **CRM-i olekukoodi** väärtusega.

    | Töötlemise olek           | CRM-i olekukood    |
    |-----------------------------|--------------------|
    | Aktiivne                      | Uus/Lahtine/Ootel |
    | Kinnitatud/komplekteeritud            | Pooleli        |
    | Osaliselt tarnitud         | Osaline            |
    | Tarnitud                   | Valmis           |
    | Arveldatud/Osaliselt arveldatud | Arveldatud           |
    | Tühistatud                    | Raha puudub           |

+ Nupud **Loo arve** ja **Tühista tellimus** lehel **Müügitellimus** on Müükides peidetud.
+ Väärtus **Müügitellimuse olek** jääb **Aktiivseks** , et rakendusest Supply Chain Management pärit muudatused saaksid liikuda rakenduse Müügid müügitellimusse. Selle käitumise juhtimiseks seadke **\[olekukoodi  oleku\]** vaikeväärtuseks **Aktiivne**.

## <a name="invoices"></a>Arved

Müügiarved luuakse rakenduses Supply Chain Management ja sünkroonitakse rakendusega Müügid. Pidage meeles järgmiseid punkte.

+ Väli **Arve number** lisati üksusesse **Arve** ja kuvatakse lehel.
+ Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Supply Chain Managementis ja sünkroonitakse Müükidega. Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Supply Chain Managementist.
+ Väärtus **Müügitellimuse olek** asendatakse automaatselt olekuga **Arveldatud**, kui seotud arve Supply Chain Managementist on sünkroonitud Müükidega. Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks. Seetõttu saab müügitellimuse omanik arvet vaadata.
+ Väljad **Veotingimused**, **Tarnetingimused** ja **Tarneviis** ei kuulu vaikevastendustesse. Nende väljade vastendamiseks peate seadistama väärtusvastenduse, mis on vastab andmetele neis organisatsioonides, mille vahel üksust sünkroonitakse.

## <a name="templates"></a>Mallid

Järjestus Potentsiaalne klient-raha sisaldab kogumit põhiüksuste kaartidest, mis töötavad andmete vastasmõjus koos, nagu on näha järgmises tabelis.

| Finance and Operations rakendused | Mudeljuhitud Dynamics 365 rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
| Müügiarve päised V2    | arved                          |             |
| Müügiarve read V2      | invoicedetails                    |             |
| CDS-i müügitellimuse päised     | müügitellimused                       |             |
| CDS-i müügitellimuse read       | müügitellimuse üksikasjad                 |             |
| Müügitellimuse päritolukoodid    | msdyn\_müügitellimuse päritolu          |             |
| CDS-i müügipakkumise päis  | pakkumised                            |             |
| CDS-i müügipakkumise read   | Pakkumise üksikasjad                      |             |

Siin on seotud põhiüksuse potentsiaalne klient-raha vastendused:

+ [Kliendi V3 kontodele](customer-mapping.md#customers-v3-to-accounts)
+ [CDS-i kontakti V2 kontaktidele](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Kliendi V3 kontaktidele](customer-mapping.md#customers-v3-to-contacts)
+ [Väljastatud tooted V2 üksusele msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Kõik tooted üksusele msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Hinnakiri](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
