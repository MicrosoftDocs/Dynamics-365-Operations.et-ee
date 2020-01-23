---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (14. veebruar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899216"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (14. veebruar 2019)

Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis
See versioon sisaldab väikesi veaparandusi.

## <a name="changes-in-onboarding"></a>Muutused kasutuselevõtus
See versioon sisaldab väikesi veaparandusi.
 
## <a name="changes-in-core-hr"></a>Core HR-i muudatused 
**Järk 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Töövõtja põhipalga üksus ei ekspordi kõiki kirjeid
Selle muudatusega ekspordib üksus **Töövõtja põhipalk** nüüd kõik kirjed. Üksust saab kasutada olemasolevate põhipalga kirjete loomiseks ja värskendamiseks töövõtjate jaoks. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Töösuhte lõppkuupäev ei arvesta töövõtja eelistatud ajavööndi sätteid
Töösuhte lõppkuupäevad arvestavad nüüd ettevõttega töösuhte loomisel või lõpetamisel kasutaja eelistatud ajavööndit.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Ühendkuningriigi aadresse kuvatakse lehel Analüütika Ida-Šveitsi aadressidena
Selles versioonis on tehtud muudatus, mis parandab aadresside joondusvea jaotise **Personalihaldus** aruandes Töötajate arv asukoha järgi.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Lõpetamise kood pole ametikoha lõpetamisel töötaja ametikoha määramiskirjes täidetud
Tehti muudatus, mis seab töötaja ametikoha määramise lõpetamisel vaikeväärtuseks koodi Lõpetamise põhjus.

### <a name="new-entity-created-for-job-compensation-levels"></a>Töö hüvitustasemete jaoks loodud uus kirje
Loodi uus andmehaldusraamistiku (DMF) üksus. Üksus tagab iga süsteemis määratletud töö hüvitustasemete, turuväärtuste ja uuringuteabe loomise ja värskendamise.
