---
title: Kontsernisisene koondplaneerimine
description: See teema selgitab kontsernisisest koondplaneerimist
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548217"
---
# <a name="intercompany-master-scheduling"></a>Kontsernisisene koondplaneerimine

[!include [banner](../../includes/banner.md)]

Kontsernisisene koondplaneerimine on vahend, mille abil saate arvutada vajadusi ja luua mitme kontserni kuuluva ettevõtte vahelised plaanitud kontsernisisesed tellimused. Kontsernisisene koondplaneerimine teostatakse mitme määratletud iteratsiooni abil. Kontsernisisese koondplaneerimise lubamiseks süsteemis Microsoft Dynamics 365 Supply Chain Management peate seadistama igas kontsernisiseses ettevõttes koondplaneerimise. See tähendab mitut iteratsiooni, mille läbimise käigus Microsoft Dynamics 365 Supply Chain Management loob automaatselt kontsernisisese ostutellimuse, mis käivitab kontsernisisese müügitellimuse automaatse loomise ning see omakorda kutsub esile uue nõudluse.

Kontserni koondplaan ja kontsernisisene planeerimiskorraldus seadistatakse iga kontsernisisese ettevõtte puhul vormi **Koondplaneerimine** parameetrites.

Kontserniahelas nõudluse levitamiseks peate plaanitud ostutellimuste automaatse kinnitamise tagamiseks seadistama parameetrid, mis tähendab, et tellimuste tähtaegu ja koguseid ei saa muuta. Saate seadistada laovarude grupi **Kinnituse ajapiiri** või koondplaani **Kinnituse ajapiiri**. Kui **Kinnituse ajapiir** on seadistamata, ei looda kontsernisiseseid ostutellimusi automaatselt. Plaanitud tellimused on ainult esimese koondplaneerimise käivitamise tulemused. Kuna kontsernisisest ostutellimust pole loodud, ei looda siiski kontsernisisest müügitellimust ning seetõttu ei looda rohkem kontsernisiseseid ostutellimusi jne.

Kontsernisisese koondplaneerimise käivitamisel loob Microsoft Dynamics 365 Supply Chain Management iga kontsernisisese ettevõtte jaoks ühe koondplaani, seejärel käivitab teise koondplaani iga kontsernisisese ettevõtte jaoks jne, kuni on sooritatud määratud iteratsioonide arv. Lubatud on maksimaalselt 30 iteratsiooni, kuid mida suurema arvu iteratsioone valite, seda kauem kestab planeerimine.

Kuna koondplaneerimisel ettevõtetes kontrollitakse kontsernisisese plaanimise seeriat, st järjekorda, milles programm määrab koondplaanid kontsernisiseste ettevõtete vahel, saate kontsernisisese koondplaneerimise käivitada ükskõik millisest kontsernisisesest ettevõttest. Kuna kontsernisisene planeerimisjärjestus määratleb koondplaneerimise ettevõtetes sooritamise järjekorra, pole kontsernisisese koondplaneerimise käivitamisel oluline. Igas iteratsioonis teostab praegune ettevõte viimase.

> [!NOTE]
> Levinud praktika kohaselt algatatakse kontsernisisene koondplaneerimine ühes Microsoft Dynamics 365 Supply Chain Management ettevõttes.

**Kontsernisisese koondplaneerimise** lehel saate käivitada koondplaneerimise järjestuse, mis käivitab koondplaneerimise esmakordselt koos kõigi kontsernisiseste ettevõtete jaoks valitud nõuete arvutamise uuendamise põhimõttega. Järgnevad iteratsioonid kasutavad sekundaarset põhimõtet, mille valite järgmise iteratsiooni jaoks, ja seda põhimõtet rakendatakse seni, kuni määratud iteratsioonide arv on saavutatud.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
