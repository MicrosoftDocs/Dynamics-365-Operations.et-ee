---
title: Kulukande üksused
description: See artikkel annab teavet kulukannete üksuste kohta, mis võimaldavad jaotatud kulu väärtuse kuluala sisu vahel jaotamismeetodi valimise kaudu.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166799"
---
# <a name="cost-transaction-entities"></a>Kulukande üksused

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Jaotamine

Väljaminev kulu võimaldab kulude väärtuse tükeldada kuluala sisu vahel (reisimine, saatmiskonteinerid jne) jaotamismeetodi valimise kaudu. Maksmismeetod seadistatakse ärireeglitel põhinevate automaatsete kulude konfiguratsiooni osana. Reisirea loomisel tõmmati see kulu osana läbi.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigureerige vastendamine andmeüksustega kasutamiseks

Kui kulu luuakse välisest allikast, nt ekspediitorist, ei saa see väline allikas määrata kulu väärtuse määramiseks eelistatud meetodit. Jaotuse vastendamine määrab igale kulutüübi koodile vaikejaotuse meetodi. Vastendamise **tabelile** Dynamics 365 Supply Chain Management pääseb juurde Microsofti vastendamise vastendamise lehelt (**väljaminev \>\> kuluarvestuse häälestuse vastendamine).**

Kui vastendamise kombinatsioon on määratud ja kulutüübi koodiga ühtiv kulu luuakse kulukande üksuse abil, kasutatakse vastendatud jagamismeetodit üksusele antud mis tahes väärtuse asemel.

Kui vastendamistabelis pole ühtegi väärtust, kuid üksusele on esitatud väärtus, kasutatakse esitatud väärtust.

Kui vastendamistabelis ega üksusele edastatud kirjes pole ühtegi väärtust, loomine nurjub.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Apportionmenti vastendamine (ITMApportionmentMapping)

Vastendamise üksus (`ITMApportionmentMapping`) loob jagamise vastendamise seosed ja võimaldab kasutajatel kirjeid luua või värskendada.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Jaotamismeetod | ITMApportionmentMapping.ApportionmentMethod | Int | Nr | Nr |
| Kulutüübi kood | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Jah** | Nr |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Reisi kulud (ITMCostTransVoyageEntity)

Reisi kuluüksus (`ITMCostTransVoyageEntity`) loob reisi kulukanded, mida rakendatakse reisi tasemel. Impordiprotsessi ajal kasutab süsteem üksusesse kaasatud kategooria- ja ja jaotatud meetodi väärtusi, et määrata, **·** **kuidas** kulu väärtus reisi sisu vahel jagatakse.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Jaotamismeetod | Rakendus ITMCostTrans.ApportionmentMethod | Int | Nr | Nr |
| Omahind | ITMCostTrans.CostValue | Numbriline(32, 6) | Nr | Nr |
| Valuuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr | **Jah** |
| Rea number | ITMCostTrans.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Seostatud kulutüüp | Kood ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr | Nr |
| Minimaalne kulu | ItMCostTrans.MinCostAmount | Numbriline(32, 6) | Nr | Nr |
| Kategooria | ItMCostTrans.ShipCostCategory | Int | Nr | Nr |
| Kulutüübi kood | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr | Nr |
| Ettevõte | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Reis | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Kauba käibemaksugrupp | Grupp ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr | Nr |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Konteineri kulude lähetamine (ITMCostTransShippingContainerEntity)

Saadetise konteineri kuluüksus (`ITMCostTransShippingContainerEntity`) loob konteineri saatmise kulud, mida rakendatakse konteineri saatmise tasemel. Impordiprotsessi ajal kasutab süsteem üksusesse kaasatud kategooria ja jaotatud meetodi väärtusi, et määrata, **·** **kuidas** kulu väärtus jagatakse lähetamiskonteineri sisu vahel.

Väljad **Liit**, **Leg** ja **Lingitud** on spetsiifilised kirjetele, kus **kuluala väärtus** konteinerit *lähetab*. Seetõttu ei ole neid muude kulualade andmeüksustes.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Agregaat | ItMCostTrans.AggregatedCost | Int | Nr | Nr |
| Jaotamismeetod | Rakendus ITMCostTrans.ApportionmentMethod | Int | Nr | Nr |
| Omahind | ITMCostTrans.CostValue | Numbriline(32, 6) | Nr | Nr |
| Valuuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr | **Jah** |
| Rea number | ITMCostTrans.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Seostatud kulutüüp | Kood ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr | Nr |
| Seostatud etapp | ItMCostTrans.LinkLegId | Nvarchar(20) | Nr | Nr |
| Minimaalne kulu | ItMCostTrans.MinCostAmount | Numbriline(32, 6) | Nr | Nr |
| Saadetise konteiner | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Kategooria | ItMCostTrans.ShipCostCategory | Int | Nr | Nr |
| Kulutüübi kood | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr | Nr |
| Ettevõte | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Reis | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Etapp | ItMCostTrans.ShipLegId | Nvarchar(20) | Nr | Nr |
| Kauba käibemaksugrupp | Grupp ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr | Nr |

## <a name="folio-costs-itmcosttransfolioentity"></a>Foolio kulud (ITMCostTransFokandeEntity)

Foolio kuluüksus (`ITMCostTransFolioEntity`) loob kulukande kirjed, mis kehtivad foolio tasemel. Impordiprotsessi ajal kasutab süsteem kategooria ja jaotatud meetodi väärtuseid, mis üksusesse kaasatakse määramaks, **·** **kuidas** kulu väärtus jagatakse iga foolio sisu vahel.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Jaotamismeetod | Rakendus ITMCostTrans.ApportionmentMethod | Int | Nr | Nr |
| Omahind | ITMCostTrans.CostValue | Numbriline(32, 6) | Nr | Nr |
| Valuuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr | **Jah** |
| Rea number | ITMCostTrans.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Seostatud kulutüüp | Kood ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr | Nr |
| Minimaalne kulu | ItMCostTrans.MinCostAmount | Numbriline(32, 6) | Nr | Nr |
| Kategooria | ItMCostTrans.ShipCostCategory | Int | Nr | Nr |
| Kulutüübi kood | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr | Nr |
| Ettevõte | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Foolio | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Kauba käibemaksugrupp | Grupp ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr | Nr |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Ostutellimuse kulud (ITMCostTransPurchaseEntity)

Ostutellimuse kuluüksus () loob`ITMCostTransPurchaseEntity` kulukanded, mis rakenduvad sisseostja tellimuse päisele. Impordiprotsessi ajal kasutab süsteem kategooria ja jaotatud meetodi väärtuseid, mis üksusesse kaasatakse määramaks, **·** **kuidas** kulu väärtus jagatakse iga foolio sisu vahel.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Jaotamismeetod | Rakendus ITMCostTrans.ApportionmentMethod | Int | Nr | Nr |
| Omahind | ITMCostTrans.CostValue | Numbriline(32, 6) | Nr | Nr |
| Valuuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr | **Jah** |
| Rea number | ITMCostTrans.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Seostatud kulutüüp | Kood ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr | Nr |
| Minimaalne kulu | ItMCostTrans.MinCostAmount | Numbriline(32, 6) | Nr | Nr |
| Ostutellimus | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Kategooria | ItMCostTrans.ShipCostCategory | Int | Nr | Nr |
| Kulutüübi kood | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr | Nr |
| Ettevõte | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Kauba käibemaksugrupp | Grupp ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr | Nr |

## <a name="item-costs-itmcosttransitementity"></a>Kaubakulud (ITMCostTransItemEntity)

Kauba kuluüksus (`ITMCostTransItemEntity`) loob kaubatasemele rakenduvad kulukanded. See üksus on seotud ostutellimuse ridade kaupadega. Kulu väärtust rakendatakse reale täielikult.

Väljad **Korrigeerimissumma** **ja** Väärtuse korrigeerimine on omased reataseme kulualadele. Seetõttu ei ole neid muude kulualade andmeüksustes.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Korrigeerimissumma | ITMCostTrans.AdjustmentAmount | Numbriline(32, 6) | Nr | Nr |
| Omahind | ITMCostTrans.CostValue | Numbriline(32, 6) | Nr | Nr |
| Valuuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr | **Jah** |
| Rea number | ITMCostTrans.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Seostatud kulutüüp | Kood ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr | Nr |
| Minimaalne kulu | ItMCostTrans.MinCostAmount | Numbriline(32, 6) | Nr | Nr |
| Ostutellimus | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Ostutellimuse rea number | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Kategooria | ItMCostTrans.ShipCostCategory | Int | Nr | Nr |
| Kulutüübi kood | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr | Nr |
| Ettevõte | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Kauba käibemaksugrupp | Grupp ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr | Nr |
| Väärtuse korrigeerimine | ITMCostTrans.ValueAdjustmentMethod | Int | Nr | Nr |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Üleviimisrea kulud (ITMCostTransTransferLineEntity)

Ülekanderea kuluüksus (`ITMCostTransTransferLineEntity`) loob kulukanded, mis rakenduvad üleviimistellimuse rea tasemele. Nende kulude väärtus rakendatakse täielikult üleviimistellimuse reale.

Väljad **Korrigeerimissumma** **ja** Väärtuse korrigeerimine on omased reataseme kulualadele. Seetõttu ei ole neid muude kulualade andmeüksustes.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Korrigeerimissumma | ITMCostTrans.AdjustmentAmount | Numbriline(32, 6) | Nr | Nr |
| Omahind | ITMCostTrans.CostValue | Numbriline(32, 6) | Nr | Nr |
| Valuuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr | **Jah** |
| Rea number | ITMCostTrans.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Seostatud kulutüüp | Kood ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr | Nr |
| Minimaalne kulu | ItMCostTrans.MinCostAmount | Numbriline(32, 6) | Nr | Nr |
| Kategooria | ItMCostTrans.ShipCostCategory | Int | Nr | Nr |
| Kulutüübi kood | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr | Nr |
| Ettevõte | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Üleviimistellimus | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Üleviimistellimuse rea number | Kood ITMCostTrans.TransRecId | Nvarchar(20) | **Jah** | Nr |
| Kauba käibemaksugrupp | Grupp ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr | Nr |
| Väärtuse korrigeerimine | ITMCostTrans.ValueAdjustmentMethod | Int | Nr | Nr |

### <a name="transaction-table"></a>Kande tabel

Kulukande kirje seostatakse kulualaga kandetabeli numbri () määramise kaudu`TransTableId`. Kui on vaja kindla tabeli ID-sid, jagatakse üksused nendel väärtustel põhinevalt, nii et üksus on olemas iga kuluala kohta.

Kandetabeli () väärtus`TransTableId` on kulukande üksuse valikus vaikimisi.

### <a name="calculated-fields"></a>Arvutatud väljad

Järgmised väljad pole kulukande üksuse kasutamisel sisestamiseks ja värskendamiseks saadaval, kuna need väljad seatakse ainult siis, kui reisikirjega tehakse konkreetseid toiminguid:

- **Eeldatav omahind** – see väli seatakse, kui reisi (ostutellimus) või üleviimise kohta sisestatakse arve.
- **Eeldatav omahind** – see väli seatakse arve sisestamisel reisiks (ostutellimus) või ülekanne vastu võetud.
- **Tegelik kulu** – see väli seatakse hankija arve sisestamisel. See on seotud kuluga.

### <a name="find-auto-costs"></a>Otsi automaatseid kulusid

Nupp **Otsi** automaatsed kulud, mis on saadaval iga kuluala jaoks (reisimine, konteineri lähetamine jne) võimaldab uuendada selle kuluala kulukandeid konfiguratsioonitabelite teabest. Kui valite kulualale nupu, kustutab süsteem selle kuluala olemasolevad kulud ja loob praeguse kuluseadistustabelite konfiguratsiooni põhjal uued kirjed.

Kulukande kirjed, mis luuakse andmeüksuse abil, märgistatakse impordina. Neid kirjeid ei kustutata, kui **valite** automaatsete kulude otsimise, sest neid ei looda uuesti automaatse kulu seadistamise tabelitest. Kuid imporditud kulukande kirjet saab siiski kustutada.

### <a name="linked-fields"></a>Lingitud väljad

Iga kulukande saab seostada teise kirjega samas kulualas. See seos luuakse lingitud **kulutüübi välja** kaudu. See võimaldab omahinna arvutamist protsendina muust kulust.

Lingitud **kulutüübi** välja saab kinnitada ainult siis, kui viidatud kirjet töödeldakse esimesena või kui see on juba tabelis olemas. Sama nõue kehtib ka väljal **Lingitud liik**, mida kasutatakse ainult konteineri saatmiskulu ala kulude puhul.
