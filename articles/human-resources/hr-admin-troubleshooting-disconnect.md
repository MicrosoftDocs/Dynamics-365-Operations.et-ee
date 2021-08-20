---
title: Kliendi ühendus katkeb
description: See artikkel selgitab, mida teha, kui kliendi ühendus tema keskkonnaga katkeb ja põhjus pole teada.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3ee3bb4547cb9d77b7559ce4ba54b478f63cb045caefefec0583b3f9b03cf53b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770476"
---
# <a name="client-disconnects"></a>Kliendi ühendus katkeb

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Keskkonna üksikasjad** 

Probleem võib esineda kõigis keskkondades.
 
**Sümptom** 

Kliendi ühendus keskkonnaga katkeb ja selle põhjus pole teada. Klient saab ühe järgmistest tõrketeadetest:

- Teie ühendus on katkenud. Töötamiseks jätkamises klõpsake nuppu Sule.
- Näib, et olete kaotanud võrguühenduse. Uuesti proovimiseks klõpsake nuppu Proovi uuesti.

**Punane lipp**

See probleem ilmneb tihti siis, kui kasutajad on juurutusetapis, võrdlevad teavet töö- ja katsekeskkondade vahel ning unustavad, et nad liiguvad seansside vahel. Kui kasutajad on selles etapis, ilmneb tõenäoliselt see probleem.

**Väljastamine** 

**Brauserite tüübid:** Google Chrome, Internet Explorer ja Microsoft Edge

Rakendus Microsoft Dynamics 365 Human Resources katkestab kasutajate ühendused, kui ühel kasutajal on korraga samas brauseritüübis avatud kaks erinevat seanssi. (Nt, kasutaja A vaatab Chrome’is nii keskkonda 1 kui ka keskkonda 2.) Pole oluline, kas kasutajad avavad erinevad brauseriaknad või erinevad vahekaardid. Kui samu kasutajamandaate kasutatakse korraga ja samas brauseritüübis nii keskkonda 1 kui ka keskkonda 2 sisselogimiseks, katkestab Human Resources ühe seansi ühenduse.

**Lahendus**

Veenduge, et korraga oleks ühes brauseritüübis avatud ainult üks keskkond. Kasutajad saavad samas keskkonnas avada mitu seanssi (s.t samas brauseris mitu vahekaarti).

Kasutajad, kes soovivad korraga hüpata kahe keskkonna vahel, peavad kummagi keskkonna avama erinevas brauseritüübis. (Nt, kasutaja A saab vaadata keskkonda 1 Chrome’is ja keskkonda 2 Microsoft Edge’is.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]