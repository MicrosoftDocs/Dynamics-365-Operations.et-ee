---
title: Kandidaadi allikate jälgimine Attractis
description: Selles teemas antakse teavet kandidaatide profiilide ja avalduste allikate jälgimise kohta.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460911"
---
# <a name="track-candidate-sources-in-attract"></a>Kandidaadi allikate jälgimine Attractis

[!include [banner](includes/banner.md)]

> [!NOTE] 
> Selles teemas märgitud funktsioonid on saadaval eelväljaandes. Sisu ja funktsioonid võivad muutuda. Selle funktsiooni kasutamiseks paluge administraatoril see lubada, kasutades Attractis **administraatori sätteid**. Tulevases väljaandes pakutakse allika jälgimise aruandeid. Lisateavet leiate teemast [Juurdepääs eelvaatefunktsioonidele rakenduses Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

Kui kandidaadid töökohale kandideerivad, jälgib rakendus Attract automaatselt nende avalduste allikat, pakkudes teile väärtuslikku abiteavet värbamisprotsessi jaoks. Värbajad ja personalijuhid võivad kandidaadi käsitsi tööle või talendikausta lisamisel valida ka avalduse allika.

Saate vaadata avalduse allikat vahekaardil **Tegevus** avalduste tegevuse üksikasjade alt ja vahekaardi **Profiil** talendikaustades olevas avalduste ajaloos. Kandidaadi profiili võite leida vahekaardi **Profiil** avaldustes ja talendikaustades olevates kandidaatide üksikasjades.

> [!NOTE] 
> Protsessimallid leiate [tervikliku värbamise lisandmoodulist](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Eelkonfigureeritud allikad

Vaikallikate loend sisaldab tavapäraseid avalduste allikaid. Mõnel allika tüübil, näiteks **Tööportaal** ja **Suhtlusvõrk**, on täiendavad allika üksikasjad. Näiteks kuuluvad allika tüübi **Suhtlusvõrk** alla Facebook ja Twitter. Allika tüüp **Viitamine** võimaldab teil viitajaks määrata ettevõttesisese töötaja. Vaikeallikate loendisse kuuluvad järgmised eelkonfigureeritud allikad.

-   Attracti karjäärisait

-   Tööbüroo

-   Karjäärimess

-   Ettevõtte turundus

-   Konverentsid ja ärimessid

-   Kutseliit

-   Tööportaal

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Ajakirjad ja trükised

-   Suhtlusvõrk

    -   Facebook

    -   Twitter

-   Ülikoolis värbamine

-   LinkedIn

-   Töökuulutus ajalehes

-   Viitamine

-   Värbaja lisatud

-   Muud

## <a name="customize-the-source-list"></a>Allikate loendi kohandamine 

Saate allikate loendit täiendada, et kaasata täiendavaid avalduste allikaid. Loendi kohandamiseks järgige juhiseid teemas [Suvandikomplektide laiendamine Attractis](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Redigeerige olemit **TalentSource**, et lisada täiendavaid allikaid. 

Kasutajaliidese kahjustamise vältimiseks ärge redigeerige ega muutke olemi **TalentCategory** loetelu (enum) väärtusi (mitte nimesid) järgmiste üksuste puhul.

- **Viitamine**
- **LinkedIn**
- **Muud**

Selle asemel saate laiendada olemi **TalentSource** loetelu (enum), et lisada muid allika tüüpe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]