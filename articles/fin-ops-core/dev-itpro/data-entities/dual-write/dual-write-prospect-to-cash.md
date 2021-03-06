---
title: Potentsiaalne klient-raha ja kaksikkirjutamine
description: See teema annab teavet potentsiaalne klient-raha kaksikkirjutamises kohta.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 33ed1c7f69fa92bbd123042a139dd8fd0ee3e73a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754084"
---
# <a name="prospect-to-cash-in-dual-write"></a>Potentsiaalne klient-raha kaksikkirjutamises

[!include [banner](../../includes/banner.md)]



Enamiku ettevõtete oluline eesmärk on muuta potentsiaalsed kliendid klientideks ja seejärel säilitada nende klientidega pidev ärisuhe. Rakendustes Microsoft Dynamics 365 toimub potentsiaalne klient-raha protsess pakkumiste või tellimuste töötlemise töövoogude kaudu ning finantsid lepitakse kokku ja kinnitatakse. Potentsiaalse kliendi-raha integreerimine kaksikkirjutamisega loob töövoo, mis võtab pakkumise ja tellimuse, mis on pärit kas Dynamics 365 Salesist või Dynamics 365 Supply Chain Management-st, ja teeb pakkumise ja tellimuse kättesaadavaks mõlemas rakenduses.

Rakendusliidestes pääsete juurde reaalaja töötlemisolekutele ja arveteabele. Seetõttu saate hõlpsalt hallata selliseid funktsioone nagu toote ladustamine, laoseisu käitlemine ja täitmine Supply Chain Managementis, ilma et peaksite pakkumised ja tellimused uuesti looma.

![Kaksikkirjutamise andmevoog järjestuses potentsiaalne klient-raha](../dual-write/media/dual-write-prospect-to-cash[1].png)

Lisateavet kliendi ja kontaktide integreerimise kohta vt [Integreeritud kliendi koondandmed](customer-mapping.md). Lisateavet toote integreerimise kohta vt [Ühendatud toote kasutusfunktsionaalsus](product-mapping.md).

> [!NOTE]
> Rakenduses Dynamics 365 Sales viitavad nii potentsiaalne klient kui ka klient kirjele tabelis **Konto**, kus veerg **Suhtetüüp** on kas **Potentsiaalne klient** või **Klient**. Kui teie äriloogika hõlmab kvalifikatsiooniprotsessi **Konto**, kus kirje **Konto** luuakse ja kvalifitseerub esmalt potentsiaalse kliendina ja seejärel kliendina, sünkroonitakse kirje rakendusega Finance and Operations ainult siis, kui see on klient (`RelationshipType=Customer`). Kui soovite, et rida **Konto** sünkroonitaks potentsiaalse kliendina, vajate potentsiaalse kliendi andmete integreerimiseks kohandatud vastendust.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügipakkumiste sünkroonimist peate uuendama järgmised sätted.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

Müükides avage jaotis **Sätted \> Administreerimine \> Süsteemisätted \> Müügid** ja veenduge, et kasutusel on järgmised sätted.

- Süsteemisuvand **Kasuta süsteemi hinnaarvutust** on seatud väärtusele **Jah**.
- Veerg **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="sites-and-warehouses"></a>Saidid ja laod

Supply Chain Managementi puhul on veerud **Sait** ja **Ladu** vajalikud pakkumise ridade ja tellimuse ridade jaoks. Kui seate saidi ja lao vaiketellimuse sätte, seatakse need veerud automaatselt, kui lisate toote pakkumise reale või tellimuse reale. 

### <a name="number-sequences-for-quotations-and-orders"></a>Pakkumiste ja tellimuste numbrijärjestused

Supply Chain Managementi ja Müügi numbrijärjestused ei ole ühendatud, kui pakkumised ja tellimused luuakse ja sünkroonitakse Müükides ja Tarneahelahalduses. Kui müügitellimus, mis on loodud Müükides, sünkroonitakse Supply Chain Managementiga, on sellel Supply Chain Managementis sama müügitellimuse number. Tagamaks, et müügitellimuse numbrit ei dubleerita, peate kahes rakenduses kasutama erinevaid numbrijärjestussüsteeme.

Näiteks on Supply Chain Managementi numbrijärjestus **1, 2, 3, 4, 5,...** ja Müükide numbrijärjestus on **100, 99, 98,...**. Kui loote Müükides 100 müügitellimust, luuakse lõpuks tellimuse number, mis on juba olemas Supply Chain Managementis. Teisisõnu lõpuks kaks numbrijärjestust kattuvad, kui müügitellimused on loodud Supply Chain Managementis ja Müükides. Selle asemel võite kasutada Supply Chain Managementis numbrijärjestust **F1, F2, F3,...** ja Müükides numbrijärjestust **C1, C2, C3,...** . Need numbrijärjestused ei moodusta kunagi dubleeritud müügitellimuse numbreid.

## <a name="sales-quotations"></a>Müügipakkumised

Müügipakkumised võib luua rakenduses Müügid või Supply Chain Management. Kui loote pakkumise Müükides, sünkroonitakse see reaalajas Supply Chain Managementiga. Kui loote pakkumise Supply Chain Managementis, sünkroonitakse see reaalajas Müükidega. Pidage meeles järgmiseid punkte.

+ Toote pakkumisele saate lisada allahindluse. Sel juhul sünkroonitakse allahindlus Supply Chain Managementiga. Päise veergusid **Allahindlus**, **Tasud** ja **Maks** juhitakse seadistusega rakenduses Supply Chain Management. See seadistus ei toeta integreerimise vastendamist. Selle asemel veerge **Hind**, **Allahindlus**, **Tasu** ning **Maks** säilitatakse ja käsitsetakse Supply Chain Managementis.
+ Veerud **Allahindlusprotsent**, **Allahindlus** ja **Veose kogus** müügipakkumise päises on kirjutuskaitstud veerud.
+ Veerud **Veotingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende veergude vastendamiseks peate seadistama väärtuse vastenduse, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel tabelit sünkroonitakse.

Kui kasutate ka lahendust Field Service, veenduge, et oleksite parameetri **Pakkumisrea kiirloomine** uuesti lubanud. Parameetri uuesti lubamine võimaldab teil jätkata pakkumisridade loomist kiirloomise funktsiooni kasutades.
1. Liikuge oma Dynamics 365 Sales'i rakenduse juurde.
2. Valige ülemiselt navigeerimisribalt sätete ikoon.
3. Valige **Täpsemad sätted**.
4. Valige suvand **Süsteemi kohandamine**.
5. Valige menüüelement **Pakkumisrida**.
6. Minge jaotisse **Andmeteenused** ja märkige ruut **Luba kiirloomine**.

## <a name="sales-orders"></a>Müügitellimused

Müügitellimused võib luua rakenduses Müügid või Supply Chain Management. Kui loote müügitellimuse Müükides, sünkroonitakse see reaalajas Supply Chain Managementiga. Samuti kui loote müügitellimuse Supply Chain Managementis, sünkroonitakse see reaalajas Müükidega. Pidage meeles järgmiseid punkte.

+ Sisestatavad tooted Dynamics 365 Salesis kuvatakse tootekategooriatena lahenduses Dynamics 365 Supply Chain Management.
+ Allahindluse arvutamine ja ümardamine:

    - Rakenduse Sales allahindluse arvutamise mudel erineb rakenduse Supply Chain Management allahindluse arvutamise mudelist. Rakenduses Supply Chain Management võib müügirea lõplik allahindluse summa olla allahindluse summade ja allahindluse protsentide kombinatsiooni tulemus. Kui lõplik allahindluse summa jagatakse real oleva kogusega, võib ilmneda ümardamine. Seda ümardamist ei võeta aga arvesse, kui ümardatavat ühikupõhist allahindluse summat sünkroonitakse Müükidega. Selleks et rakenduse Supply Chain Management müügirea kogu allahindluse summa õigesti sünkroonida rakendusega Müügid, tuleb kogusumma sünkroonida rea kogusega jagamata. Seetõttu peate rakenduses Müügid määrama allahindluse arvutamise meetodiks **Rea kaup** .
    - Kui müügitellimus rakenduses Müügid sünkroonitakse rakendusega Supply Chain Management, kasutatakse terve rea allahindluse summat. Kuna rakenduses Supply Chain Management pole ühtegi veergu, millele saab salvestada rea kogu allahindluse summa, jagatakse summa kogusega ja salvestatakse veergu **Rea allahindlus**. Selle jagamisega kaasnev ümardamine talletatakse müügirea veerus **Müügitasud**.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Näide: Müükide sünkroonimine Supply Chain Managementiga

Teil on järgmine müügitellimus:

+ **Sales:** kogus = 3, allahindlus rea kohta = 10.00 USA dollarit
+ **Tarneahelahaldus:** kogus = 3, rea allahindluse summa = $3,33, müügitasu =-$0,01

Kui sünkroonite Supply Chain Managementi Müükidega, saate järgmise tulemuse:

+ **Tarneahelahaldus:** kogus = 3, rea allahindluse summa = $3,33, müügitasu =-$0,01
+ **Sales:** kogus = 3, allahindlus rea kohta = (3 × 3.33) + 0.01 = 10.00 USA dollarit

## <a name="dual-write-solution-for-sales"></a>Kaksikkirjutamise lahendus Müükidele

Tabelile **Tellimus** lisati uued veerud ja need kuvatakse lehel. Enamik neist veergudes kuvatakse rakenduse Sales vahekaardil **Integreerimine**. Lisateavet selle kohta, kuidas olekuveergusid vastendatakse, vaadake: [Müügitellimuse olekuveergude vastendamise seadistamine](sales-status-map.md).

+ Nupud **Loo arve** ja **Tühista tellimus** lehel **Müügitellimus** on Müükides peidetud.
+ Väärtus **Müügitellimuse olek** jääb **Aktiivseks** , et rakendusest Supply Chain Management pärit muudatused saaksid liikuda rakenduse Müügid müügitellimusse. Selle käitumise juhtimiseks seadke suvandi **Olekukood \[Olek\]** vaikeväärtuseks **Aktiivne**.

## <a name="invoices"></a>Arved

Müügiarved luuakse rakenduses Supply Chain Management ja sünkroonitakse rakendusega Müügid. Pidage meeles järgmiseid punkte.

+ Veerg **Arve number** lisati tavelisse **Arve** ja kuvatakse lehel.
+ Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Supply Chain Managementis ja sünkroonitakse Müükidega. Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Supply Chain Managementist.
+ Väärtus **Müügitellimuse olek** asendatakse automaatselt olekuga **Arveldatud**, kui seotud arve Supply Chain Managementist on sünkroonitud Müükidega. Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks. Seetõttu saab müügitellimuse omanik arvet vaadata.
+ Veerud **Veotingimused**, **Tarnetingimused** ja **Tarneviis** ei kuulu vaikevastendustesse. Nende veergude vastendamiseks peate seadistama väärtuse vastenduse, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel tabelit sünkroonitakse.

## <a name="templates"></a>Mallid

Järjestus Potentsiaalne klient sularahaks sisaldab kogumit põhitabeli vastendustest, mis töötavad andmete vastasmõjus koos, nagu on näha järgmises tabelis.

| Finance and Operations rakendused | Klientide kaasamise rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
| Müügiarve päised V2    | arved                          | Tabel Müügiarve päised V2 rakenduses Finance and Operations sisaldab müügtellimuste arveid ja vabas vormis arveid. Dataverse’is rakendatakse topeltkirjutamise jaoks filter, et filtreerida välja kõik vabas vormis arvedokumendid. |
| Müügiarve read V2      | invoicedetails                    |             |
| CDS-i müügitellimuse päised     | müügitellimused                       |             |
| CDS-i müügitellimuse read       | müügitellimuse üksikasjad                 |             |
| Müügitellimuse päritolukoodid    | msdyn\_müügitellimuse päritolu          |             |
| CDS-i müügipakkumise päis  | pakkumised                            |             |
| CDS-i müügipakkumise read   | Pakkumise üksikasjad                      |             |

Siin on seotud põhitabeli potentsiaalne klient sularahaks vastendused.

+ [Kliendi V3 kontodele](customer-mapping.md#customers-v3-to-accounts)
+ [CDS-i kontakti V2 kontaktidele](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Kliendi V3 kontaktidele](customer-mapping.md#customers-v3-to-contacts)
+ [Väljastatud tooted V2 üksusele msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Kõik tooted üksusele msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Hinnakiri](product-mapping.md)

## <a name="limitations"></a>Kitsendused
- Tagastustellimusi ei toetata.
- Kreeditarveid ei toetata.
- Koondandmete jaoks peavad olema määratud finantsdimensioonid (nt klient ja hankija). Kui klient lisatakse pakkumisele või müügitellimusele, liiguvad kliendikirjega seotud finantsdimensioonid automaatselt tellimusse. Praegu ei sisalda topeltkirjutus koondandmete finantsdimensioonide andmeid. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]