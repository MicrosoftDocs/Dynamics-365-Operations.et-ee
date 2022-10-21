---
title: Planeerimise optimeerimise väljaandmise protsess ja väljalaske ajalugu
description: See artikkel annab teavet planeerimise optimeerimise väljalaske protsessi ja vabastamise ajaloo kohta.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682556"
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
| <p>[Partii likvideerimiskoodid](../../inventory/batch-disposition-codes.md)</p><p>Kaasa koondplaanidesse vaba kaubavaru ja laokannete parameetrid</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse parendused</p> | Funktsioonihaldus pole nõutav | 10. oktoober 14. oktoober 2022 |
| <p>[Piiratud võimsusega ressursside plaanimine](finite-capacity.md)</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse parendused</p> | Funktsioonihaldus pole nõutav | 19.09.23, 2022 |
| Üldjõudluse, kvaliteedi ja stabiilsuse parendused | Funktsioonihaldus pole nõutav | 29. august – 3. september 2022 |
| <p>[Tsentraliseeritud kalendri hooldus](../supply-chain-calendars-master-planning.md)</p><p>[Soovitused olemasoleva tarne optimeerimiseks](../action-messages.md)</p><p>[Allhanke tugi](../../production-control/manage-subcontract-work-production.md)</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse parendused</p> | Funktsioonihaldus pole nõutav | 7. märts 11.2022 |
| Tootmistellimuste prioriteedi toe plaanimine | Saadaval versiooniga 10.0.25 *funktsiooni nimega Prioriteedipõhine MRP tugi plaanimise optimeerimise osana*. | 12. november 18, 2021 |
| Üldjõudluse, kvaliteedi ja stabiilsuse parendused | Funktsioonihaldus pole nõutav | 12. november 18, 2021 |
| <p>Protsessiaja arvutamise valemite, kattumisega tootmisprotsessi ja vajadusekannete tootmisoperatsiooni numbri tugi</p><p>Täiustatud tõrketeated tootmise planeerimisel, mis on seotud ajalõpuga, võimsust ei leitud ja tsükliline protsess</p><p>Täiustatud ühtsus sissetulekukuupäevade ja väljaminekkuupäevade arvutamisel nii plaanitud kui ka kindla tellimuse puhul</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse parendused</p> | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 22. oktoober 27.09.2021 |
| <p>Tugi praagi protsendi arvestamiseks töötlemisaja arvutamisel</p><p>Operatsiooninumbri ja materjalide kasutamise tugi planeerimisel</p> | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 5. oktoober 7. oktoober 2021 |
| <p>Tootmisprotsessi töötüüpide tugi: ootel **enne**, järjekord **pärast** ja **transpordiaeg**</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse parendused</p> | Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine* | 25. september 30.2021 |
| <p>Koondplaanide tugi, kus planeerimismeetodi **väärtuseks** on seatud *Operatsioonide planeerimine*</p><p>Kas soovite **protsessigruppide** lehel arvesse kirjutada märkeruudud **Aktiveerimine**,**Tööaeg** ja Võimsus **ridade** jaoks, **mille protsessi/töö** *tüüp on Häälestus või* *Protsess?* </p><p>Üldjõudluse, kvaliteedi ja stabiilsuse parendused</p> | <p>Operatsioonide planeerimine on funktsioonihalduses saadaval versioonist 10.0.20</p><p>Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*</p> | 9.-17. september, 2021 |
| Üldjõudluse, kvaliteedi ja stabiilsuse parendused | Funktsioonihaldus pole nõutav | 25.-30. august 2021 |
| <p>Plaanitud tellimustele lisati väli **Täitmisaeg**.</p><p>Üldjõudluse, kvaliteedi ja stabiilsuse täiustused.</p> | Funktsioonihaldus pole nõutav | 12.-17. august 2021 |
| <p>Lisatud ressursitüübi nõuded piiramatu võimsuse planeerimiseks</p><p>Täiustatud ressursiefektiivsus ja kalendri efektiivsus piiramatu võimsuse planeerimisel</p><p>Lisateavet vt piiramatu võimsusega [plaanimine.](infinite-capacity-planning.md)</p> | <p>Funktsioonihalduses saadaval versiooni 10.0.20 alusel</p><p>Funktsiooni nimi: *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*</p> | 6.-12. juuli 2021 |
| Üldised kvaliteediparandused | Funktsioonihaldus pole nõutav | 6.-12. juuli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
