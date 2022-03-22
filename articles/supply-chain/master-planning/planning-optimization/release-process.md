---
title: Planeerimise optimeerimise väljaandmise protsess ja väljalaske ajalugu
description: Sellest teemast leiate teavet optimeerimise plaanimise väljalaskeprotsessi ja väljalaskeajaloo kohta.
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f9674bb68d7f577a6efdef3416d1731d743d0555
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087162"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Planeerimise optimeerimise väljaandmise protsess ja väljalaske ajalugu

[!include [banner](../../includes/banner.md)]

Microsoft värskendab plaanimise optimeerimist igakuiselt. Kuid ärinõuete põhjal avaldame aeg-ajalt plaanitud väljaannete vahel täiendavaid värskendusi.

Iga väljalase avaldatakse üksikutes piirkondades, kus plaanimine optimeerimine on saadaval. Protsess kestab tavaliselt kolm päeva.

Planeerimise optimeerimise värskendamise ajal võib üldplaneerimine toimida tavapärasest veidi aeglasemalt.

Planeerimist optimeerimist kasutavad keskkonnad saavad automaatselt uusima versiooni. Kasutajatoimingut pole vaja: teenust värskendatakse automaatselt. Kuid ühtegi murrangulist funktsiooni ei lükata kunagi automaatselt keskkondadesse. Vaikimisi on kõik murranguliseks peetavad muudatused välja lülitatud ja need tuleb [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil selgesõnaliselt sisse lülitada. Seetõttu ei kuvata neid muudatusi keskkondades enne, kui otsustate need lubada.

Kuna teatisi ei kuvata, kui plaanimise optimeerimist teie keskkonnas värskendatakse, saate järgmises tabelis esitatud väljalaskemärkmed üle vaadata, et teha kindlaks, millal muudatused vabastati ja milliseid funktsioone need kasutusele võtsid. Selles tabelis kuvatakse planeerimise optimeerimiseks välja antud muudatused, kas need muudatused on seotud funktsioonihalduse funktsiooniga, ja väljaandmise kuupäev.

| Muutused | Funktsioonihalduse üksikasjad | Väljalaske kuupäevad |
|---|---|---|
| <p>Tootmistellimuste jaoks lisatud plaanimisprioriteedi tugi. | Saadaval versiooniga 10.0.25 osana funktsioonist nimega *Priority driven MRP tugi planeerimise optimeerimiseks*. | 12.–18. november 2021 |
| <p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsioonihaldust pole vaja. | 12.–18. november 2021 |
| <p>Lisatud tugi protsessi aja arvutamise valemitele, kattuvale tootmisprotsessile ja tootmistoimingu numbrile nõudekannetes.</p><p>Täiustatud tõrketeated tootmise planeerimiseks, mis on seotud ajalõega, võimsust ei leitud ja tsüklilist marsruuti.</p><p>Täiustatud järjepidevus nii plaanitud tellimuste kui ka kinnitatud tellimuste tarnekuupäevade ja väljaminemiskuupäevade arvutamisel.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 22.–27. oktoober 2021 |
| <p>Lisatud tugi vanaraua protsendi kaalumiseks töötlemisaja arvutamisel.</p><p>Lisatud tugi operatsiooni numbrile ja materjalide kasutamisele planeerimise ajal. | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 5.–7. oktoober 2021 |
| <p>Lisatud tugi tootmisprotsessi töötüüpidele: **järjekord enne**, **Järjekord pärast** ja **Transpordiaeg**.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 25.–30. september 2021 |
| <p>Lisatud üldplaanide tugi **Ajastamismeetod** seatud väärtusele *Toimingute ajastamine*.</p><p>**Marsruudirühmade** lehel järgige seadete **Aktiveerimine**, **Tööaeg** ja **Mahutavus** märkeruute ridadel, kus on *Seadistuse* või *Protsessi* **Marsruudi/töö tüüp**. </p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | <p>Toimingute ajastamine on saadaval funktsioonihalduses alates versioonist 10.0.20.</p><p>Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*</p>  | 9.-17. september, 2021 |
| Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsioonihaldust pole vaja. | 25.-30. august 2021 |
| <p>Plaanitud tellimustele lisati väli **Täitmisaeg**.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused.</p> | Funktsioonihaldust pole vaja. | 12.-17. august 2021 |
| <p>Lõpmatu võimsuse planeerimisele lisati ressursitüübi nõuded.</p><p>Täiustatud ressursitõhusus ja kalendri tõhusus lõpmatu võimsuse planeerimisel.</p><p>Lisateavet vt teemast [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md). | <p>Saadaval funktsioonihalduses alates versioonist 10.0.20.</p><p>Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*</p> | 6.-12. juuli 2021 |
| Üldised kvaliteediparandused. | Funktsioonihaldust pole vaja. | 6.-12. juuli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
