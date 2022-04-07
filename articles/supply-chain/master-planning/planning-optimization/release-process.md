---
title: Planeerimise optimeerimise väljaandmise protsess ja väljalaske ajalugu
description: Sellest teemast leiate teavet optimeerimise plaanimise väljalaskeprotsessi ja väljalaskeajaloo kohta.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 673543ff2c9abefbca0529f35ce20bb26156acc4
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469697"
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
| <p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused.<p>[Optimeerimise tsentraliseeritud kalendri hoolduse plaanimine](../supply-chain-calendars-master-planning.md)<p>[Optimeerimise soovituste plaanimine olemasoleva tarne optimeerimiseks](../action-messages.md)<p>[Plaanimise optimeerimise tugi allhankeks](../../production-control/manage-subcontract-work-production.md) | Funktsioonihaldust pole vaja. | 7. märts 11.2022 |
| <p>Lisatud plaanimise prioriteedi tugi tootmistellimustele. | Saadaval versiooniga 10.0.25 *funktsiooni nimega Prioriteedipõhine MRP tugi plaanimise optimeerimise osana*. | 12. november 18, 2021 |
| <p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsioonihaldust pole vaja. | 12. november 18, 2021 |
| <p>Lisatud tugi protsessiaja arvutamise valemitele, kattuvale tootmisprotsessile ja vajadusekannete tootmisoperatsiooni numbrile.</p><p>Täiustatud tõrketeated tootmise planeerimisel, mis on seotud ajalõpuga, võimsust ei leitud ja tsükliline protsess.</p><p>Täiustatud ühtsus sissetuleku- ja väljaminekkuupäevade arvutamisel nii plaanitud kui ka kindla tellimuse puhul.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 22. oktoober 27.09.2021 |
| <p>Lisatud tugi praagi protsendi arvestamiseks töötlemisaja arvutamisel.</p><p>Lisati operatsiooninumbri ja materjalide kasutuse tugi planeerimise ajal. | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 5. oktoober 7. oktoober 2021 |
| <p>Lisatud tugi tootmisprotsessi töötüüpidele: **ootel enne**, **ootel pärast** ja **transpordiaega**.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 25. september 30.2021 |
| <p>Lisatud üldplaanide tugi **Ajastamismeetod** seatud väärtusele *Toimingute ajastamine*.</p><p>**Marsruudirühmade** lehel järgige seadete **Aktiveerimine**, **Tööaeg** ja **Mahutavus** märkeruute ridadel, kus on *Seadistuse* või *Protsessi* **Marsruudi/töö tüüp**. </p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | <p>Toimingute ajastamine on saadaval funktsioonihalduses alates versioonist 10.0.20.</p><p>Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*</p>  | 9.-17. september, 2021 |
| Üldjõudluse, kvaliteedi ja stabiilsuse täiustused. | Funktsioonihaldust pole vaja. | 25.-30. august 2021 |
| <p>Plaanitud tellimustele lisati väli **Täitmisaeg**.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused.</p> | Funktsioonihaldust pole vaja. | 12.-17. august 2021 |
| <p>Lõpmatu võimsuse planeerimisele lisati ressursitüübi nõuded.</p><p>Täiustatud ressursitõhusus ja kalendri tõhusus lõpmatu võimsuse planeerimisel.</p><p>Lisateavet vt teemast [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md). | <p>Saadaval funktsioonihalduses alates versioonist 10.0.20.</p><p>Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*</p> | 6.-12. juuli 2021 |
| Üldised kvaliteediparandused. | Funktsioonihaldust pole vaja. | 6.-12. juuli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
