---
title: Talenti kliendi ühendus katkeb
description: See teema selgitab, mida teha, kui kliendi ühendus tema keskkonnaga katkeb ja põhjus pole teada.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "859916"
---
# <a name="talent-client-disconnects"></a>Talenti kliendi ühendus katkeb

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad** 

Probleem võib esineda kõigis keskkondades.
 
**Sümptom** 

Kliendi ühendus tema keskkonnaga katkeb ja põhjus pole teada. Klient saab ühe järgmistest tõrketeadetest:

- Teie ühendus on katkenud. Töötamiseks jätkamises klõpsake nuppu Sule.
- Näib, et olete kaotanud võrguühenduse. Uuesti proovimiseks klõpsake nuppu Proovi uuesti.

**Punane lipp**

See probleem ilmneb tihti siis, kui kasutajad on juurutusetapis, võrdlevad teavet töö- ja katsekeskkondade vahel ning unustavad, et nad liiguvad seansside vahel. Kui kasutajad on selles etapis, ilmneb tõenäoliselt see probleem.

**Väljastamine** 

**Brauserite tüübid:** Google Chrome, Internet Explorer ja Microsoft Edge

Rakenduse Microsoft Dynamics 365 for Talent platvorm katkestab kasutajate ühendused, kui ühel kasutajal on korraga samas brauseritüübis avatud kaks erinevat seanssi. (Nt, kasutaja A vaatab Chrome’is nii keskkonda 1 kui ka keskkonda 2.) Pole oluline, kas kasutajad avavad erinevad brauseriaknad või erinevad vahekaardid. Kui samu kasutajamandaate kasutatakse korraga ja samas brauseritüübis nii keskkonda 1 kui ka keskkonda 2 sisselogimiseks, katkestab Talent ühe seansi ühenduse.

**Lahendus**

Veenduge, et korraga oleks ühes brauseritüübis avatud ainult üks keskkond. Kasutajad saavad samas keskkonnas avada mitu seanssi (s.t samas brauseris mitu vahekaarti).

Kasutajad, kes soovivad korraga hüpata kahe keskkonna vahel, peavad kummagi keskkonna avama erinevas brauseritüübis. (Nt, kasutaja A saab vaadata keskkonda 1 Chrome’is ja keskkonda 2 Microsoft Edge’is.)
