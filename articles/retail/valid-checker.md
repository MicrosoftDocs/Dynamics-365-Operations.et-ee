---
title: Jaemüügikande süsteemsuskontroll
description: Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni teenuses Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: b956565ac15b3d7b638cedaadc20923ee87b9c61
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622593"
---
# <a name="retail-transaction-consistency-checker"></a>Jaemüügikande süsteemsuskontroll


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni. Süsteemsuskontroll tuvastab ja isoleerib vastuolulised kanded enne, kui väljavõtte sisestuse protsess need peale võtab.

Retailis võib väljavõtte sisestamine nurjuda, kuna jaemüügikannete tabelites on vastuolulised andmed. Andmete probleemi võivad põhjustada ettenägematud probleemid kassarakenduses (POS) või kolmanda osapoole kassasüsteemidest valesti imporditud kanded. Need vastuolud võivad ilmuda näiteks järgmistel juhtudel. 

- Päisetabelis olev kande kogusumma ei kattu kande ridade kogusummaga.
- Päisetabeli ridade arv ei kattu kandetabeli ridade arvuga.
- Päisetabeli maksud ei kattu ridade maksusummaga. 

Kui väljavõtte sisestamise protsess laadib vastuolulised kanded, luuakse vastuolulised müügiarved ja maksetöölehed ning kogu väljavõtte sisestamise protsess nurjub. Sellises olekus väljavõtete taastamine hõlmab keerukaid andmeparandusi mitmes kandetabelis. Jaemüügikande süsteemsuskontroll takistab selliseid probleeme.

Järgmine diagramm illustreerib kande süsteemsuskontrolliga sisestusprotsessi.

![Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga](./media/validchecker.png "Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga")

Pakktöötluse funktsioon **Kinnita kaupluse kanded** kontrollib jaemüügi kandetabelite järjepidevust järgmiste stsenaariumide suhtes.

- **Kliendi konto** – kontrollib, kas jaemüügi kandetabelites märgitud kliendikonto on peakontori kliendi koondandmetes olemas.
- **Ridade arv** – kontrollib, kas kande päisetabelis märgitud ridade arv kattub müügikande tabeli ridade arvuga.
- **Hind sisaldab maksu** – kontrollib kas parameeter **Hind sisaldab maksu** on kõigil kanderidadel ühtne.
- **Maksesumma** – kontrollib kas maksekirjed ühtivad makse summaga päises.
- **Brutosumma** – kontrollib, kas päises olev brutosumma vastab ridadel olevate netosummade kogusummale pluss maksusummale.
- **Netosumma** – kontrollib, kas päises olev netosumma vastab ridadel olevate netosummade kogusummale.
- **Üle-/alamakse** – kontrollib, ega päises oleva brutosumma ja maksesumma vahe ei ületa üle-/alamakse konfiguratsiooni maksimumi.
- **Allahindluse summa** – kontrollib, kas allahindluse summa allahindlustabelites ja allahindluse summa jaemüügi kanderidade tabelites on ühtne ja kas päises olev allahindluse summa päises on ridadel olevate allahindluse summade kogusumma.
- **Rea allahindlus** – kontrollib, kas rea kandereal olev rea allahindlus on kandereale vastavas allahindluse tabelis olevate kõigi ridade summa.
- **Kinkekaardi kaup** – Retail ei toeta kinkekaardikaupade tagastamist. Kinkekaardil oleva saldo saab aga sularahaks teisendada. Väljavõtte sisestamise protsess nurjub iga kinkekaardikauba puhul, mida töödeldakse sularahaks teisendamise rea asemel tagastusreana. Kinkekaardikaupade valideerimisprotsess aitab tagada, et ainsad tagastatavad kinkekaardi reakaubad jaemüügi kandetabelites oleksid kinkekaardi sularahaks teisendamise read.
- **Negatiivne hind** – kontrollib, ega kuskil pole negatiivse hinna kanderidu.
- **Kaup ja variant** – kontrollib, kas kanderidadel olevad kaubad ja variandid on olemas ka kauba ja variandi põhifailis.
- **Maksusumma** – kontrollib, kas maksukirjed vastavad ridadel olevatele maksusummadele.
- **Seerianumber** – kontrollib, kas seerianumber on seerianumbriga kontrollitavate ridade puhul kanderidadel olemas.
- **Märk** – kontrollib, kas koguse ja netosumma märk on kõigil kanderidadel sama.
- **Ärikuupäev** – kontrollib, kas kõigi jaemüügikannete ärikuupäevade finantsperioodid on avatud.

## <a name="set-up-the-consistency-checker"></a>Süsteemsuskontrolli seadistamine

Seadistage pakktöötluse funktsiooni „Kontrolli kaupluse kandeid” regulaarne käitamine jaotises **Jaemüük \> Jaemüügi IT \> Kassa sisestamine**. Pakett-tööd saab ajastada kaupluse organisatsiooni hierarhia alusel, sarnaselt protsesside „Väljavõtte arvutamine partiina” ja „Väljavõtte sisestamine partiina” seadistamisega. Soovitame konfigureerida pakktöötluse nii, et seda käitataks mitu korda päevas, ja ajastada käitamise iga P-töö lõpus.

## <a name="results-of-validation-process"></a>Kontrollimisprotsessi tulemused

Pakktöötluse kontrolli tulemused märgistatakse sobivas jaemüügikandes. Jaemüügikande kirje väljal **Kinnitamise olek** on märge **Õnnestus** või **Tõrge** ning viimase kontrollimise kuupäev kuvatakse väljal **Viimase kinnitamise aeg**.

Kontrollimistõrkega seotud täpsema tõrketeksti vaatamiseks valige asjakohane jaemüügikande kirje ja seejärel klõpsake nuppu **Valideerimistõrked**.

Kandeid, mille kontroll nurjub või mis ei ole veel kontrollitud, ei lisata väljavõtetesse. Protsessi „Väljavõtte arvutamine” ajal teavitatakse kasutajaid, kui teatud kandeid ei saanud väljavõttesse kaasata.

Ainus viis valideerimistõrke lahendamiseks on võtta ühendust Microsofti toega. Tulevases versioonis lisatakse funktsioonid, mis võimaldavad kasutajatel nurjunud kirjeid kasutajaliidese kaudu parandada. Samuti tulevad saadavale logimise ja auditeerimise funktsioonid, mis võimaldavad muudatuste ajalugu jälgida.

> [!NOTE]
> Tulevases versioonis lisatakse täiendavad kinnitusreeglid, mis toetavad rohkem stsenaariume.
