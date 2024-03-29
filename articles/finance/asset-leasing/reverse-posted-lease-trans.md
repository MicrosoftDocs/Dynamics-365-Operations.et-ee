---
title: Sisestatud rendikannete tühistamine
description: See artikkel selgitab, kuidas sisestatud rendikannet tühistada. Kõiki vara rentimise kaudu loodud kandeid saab tühistada.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4f23b6cca6ddf4da7a0232a5bc61785dbd451d55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908063"
---
# <a name="reverse-posted-lease-transactions"></a>Sisestatud rendikannete tühistamine

[!include [banner](../includes/banner.md)]

Kõiki vara rentimise kaudu loodud kandeid saab tühistada. Kanded, mis on tühistatud vara rentimise jaotuse kaudu värskendavad teie rendilepingu andmeid. Seetõttu värskendavad nad ka rendikohustise ja kasutamisõiguse esemeks oleva vara bilansilist väärtust.

Rendi tühistamise kande loomiseks toimige järgmiselt.

1. Valige kas lehel **Vara kanded** või **Kohustuste kanded** kanne ja seejärel valige käsk **Tühista kanne**.
2. Kuvatavas dialoogiboksis saate redigeerida kuupäeva, millal tühistamise kanne sisestatakse. Vaikimisi on väli **Kuupäev** seadistatud valitud kande sisestamise kuupäevale. Tühistamise kirjet ei saa sisestada enne valitud kande algset sisestamiskuupäeva.
3. Valige nupp **OK**. Sisestatakse töölehe kirje, mis tühistab valitud kirje. Tühistamine kuvatakse kas lehel **Vara kanded** või **Kohustuste kanded** ja lehel kuvatav praeguse saldo netosumma värskendatakse.

Kui valite käsu **Tühista jälitus**, kuvatakse dialoogiboks, kus kuvatakse nii algsed kui ka tühistatud kanded, koos lingitud numbriga, mida nimetatakse *jälgimisnumbriks*. Tühistamise lihtsustamiseks ja nähtavuse parandamiseks saate tühistamisi jälgida ka rendigraafikute abil.

Väli **Viimase töölehe number** lehel **Graafik** näitab kannete töölehe numbreid. Kande tühistamisel värskendatakse see väli tühistamistehingu töölehe numbriga. Lisaks valitakse märkeruut **Tühistatud**, mis näitab, et kanne on tühistatud ja valitakse väli **Sisestatud**.

## <a name="revoke-a-reversed-transaction"></a>Tühistatud tehingu taastamine

Tühistatud tehingu taastamiseks toimige järgmiselt.

1. Valige algne kanne kas lehel **Graafik** või **Kanded**.
2. Järgige üht neist sammudest.

    - Kui valisite kande lehel **Graafik**, järgige töölehe loomise etappe jaotises [Igakuiste töölehe kannete loomine partiis](create-monthly-journals-batch.md). Peate töölehe käsitsi sisestama.
    - Kui valisite kande lehel **Kanded**, valige **Tühista kanne**. Kuvatakse teade, mis teatab, et see tühistamine on varasema tühistamise tagasi võtmine ja saate redigeerida selle tühistamise sisestamiskuupäeva. Kuid valideerimised mõjutavad kuupäevi, mida saab väljale **Kuupäev** sisestada. 

3. Valige nupp **OK**. Sisestatakse töölehe kirje, mis tühistab valitud kirje. Tühistamine kuvatakse lehel **Kanded** ja taastatakse kogu praegune saldo selleks, mis see oli enne esimest tühistamist. Seetõttu muutub tühistamise mõju saldole olematuks.

Kui valite käsu **Tühista jälitus**, kuvatakse dialoogiboks, kus kuvatakse nii algsed kui ka tühistatud kanded, koos lingitud jälgimisnumbriga.

Saate tühistusi ka vastaval lehel **Graafikud** jälgida. Kustutatakse väli **Tühistatud**, samas kui valitakse väli **Töölehele sisestatud**. Lisaks värskendatakse väli **Viimane töölehe number** tühistamise kande töölehe numbriga ja väli **Töölehe number** värskendatakse tühistamise töölehe numbriga.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
