---
title: Partii atribuudid
description: Selles teemas antakse teavet partii atribuutide kohta. Partii atribuudid on toormaterjalide ja varude partiid moodustavate valmistoodete omadused. See teema selgitab ka partiiatribuutide määramist ja seda, kuidas neilt partiide reserveerimisel otsida saab.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ceb971e7468245297f2359317533b123a3a4f83a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565348"
---
# <a name="batch-attributes"></a>Partii atribuudid

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet partii atribuutide kohta. Partii atribuudid on toormaterjalide ja varude partiid moodustavate valmistoodete omadused. See teema selgitab ka partiiatribuutide määramist ja seda, kuidas neilt partiide reserveerimisel otsida saab.

Partii atribuudid on toormaterjalide ja varude partiid moodustavate valmistoodete omadused. Partii atribuudid võivad erineda olenevalt teguritest, nagu keskkonnatingimused, partii tootmiseks kasutatavate toormaterjalide kvaliteet või valmistoote tulemus. Kasutatavate partii atribuutide arv ja tüübid võivad valdkonniti olulisel määral erineda. Siin on toodud kaks näidet partii atribuutide kasutamisest.

-   Juustutööstuses võivad piimal, mis on üks juustu tootmiseks kasutatavaid toormaterjale, olla atribuudid, nagu rasvasisaldus ja massiprotsent. Piimast toodetud juustul võivad olla teised atribuudid, näiteks niiskus ja vanus.
-   Terasetööstuses võivad toodetud raual olla atribuudid, nagu magneesiumi-, hõbeda- ja tsingisisalduse protsendid.

Atribuutide arvu ja tüüpide paremini haldamiseks saate kasutada partii atribuudigruppe. Nii ei pea te iga atribuuti eraldi lisama.

## <a name="assign-batch-attributes"></a>Partii atribuutide määramine
Saate määrata partii atribuudid varude partiides hoitavatele üksikutele toodetele või kindlate klientidega seostatud toodetele. Enne partii atribuudi määramist peate määrama selle toote tasemel. Tootel peab olema jälgimisdimensioonigrupis määratud partiidimensiooni väärtuseks **Aktiivne**. Partii atribuudi määramiseks üksikule tootele kasutage tootekohast lehte. Kui atribuut on kliendi jaoks loodud toote kohane, kasutage kliendikohast lehte. Tootele atribuudi lisamisel saate määratleda ka muud parameetrid. Järgmisena on toodud mõned näited.

-   Atribuudi tüübiga **Täisarv** või **Murd** miinimum- ja maksimumvahemikud.
-   Atribuudi, mille tüüp on **Täisarv** või **Murd**, hälbetegevused. Kui atribuudi väärtus jääb väljapoole miinimum- ja maksimumvahemikku, saab tegevus olla kas hoiatus- või tõrketeade.
-   Atribuudi sihtväärtus. See väärtus on atribuudi optimaalne väärtus ja see rakendub kõigile atribuuditüüpidele.

Pääsete juurde mooduli Tooteteabe haldus lehel **Väljastatud tooted** valitud toodete lehtedele. Pärast tootele partii atribuutide määramist saate lehel **Varude partii atribuudid** lisada atribuutidele kindlad väärtused.

## <a name="reserve-batches"></a>Partiide reserveerimine
Saate otsida partii atribuute, kui reserveerite partiisid müügitellimuse jaoks, et täita kliendi tellimust, või kui komplekteerite ja reserveerite partiisid tootmistellimuse jaoks. Otsing aitab leida varude partii, mis sisaldab teie soovitud partiiatribuutidega toodet. Kui olete partii(de) asukoha(d) tuvastanud, saate reserveerida toote lähtevarude kandereale.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]