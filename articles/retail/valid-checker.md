---
title: Jaemüügikande süsteemsuskontroll
description: Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni teenuses Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
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
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "302179"
---
# <a name="retail-transaction-consistency-checker"></a>Jaemüügikande süsteemsuskontroll


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni, mis lasti välja teenuse Microsoft Dynamics 365 for Finance and Operations versioonis 8.1.3. Süsteemsuskontroll tuvastab ja isoleerib vastuolulised kanded enne, kui väljavõtte sisestuse protsess need peale võtab.

Retailis võib väljavõtte sisestamine nurjuda, kuna jaemüügikannete tabelites on vastuolulised andmed. Andmete probleemi võivad põhjustada ettenägematud probleemid kassarakenduses (POS) või kolmanda osapoole kassasüsteemidest valesti imporditud kanded. Need vastuolud võivad ilmuda näiteks järgmistel juhtudel. 

  - Päisetabelis olev kande kogusumma ei kattu kande ridade kogusummaga.
  - Päisetabeli ridade arv ei kattu kandetabeli ridade arvuga.
  - Päisetabeli maksud ei kattu ridade maksusummaga. 
  
Kui väljavõtte sisestamise protsess laadib vastuolulised kanded, luuakse vastuolulised müügiarved ja maksetöölehed ning kogu väljavõtte sisestamise protsess nurjub. Sellises olekus väljavõtete taastamine hõlmab keerukaid andmeparandusi mitmes kandetabelis. Jaemüügikande süsteemsuskontroll takistab selliseid probleeme.

Järgmine diagramm illustreerib kande süsteemsuskontrolliga sisestusprotsessi.

![Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga](./media/validchecker.png "Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga")

Pakktöötluse funktsioon **Kinnita kaupluse kanded** kontrollib jaemüügi kandetabelite järjepidevust järgmiste stsenaariumite suhtes.

- Kliendi konto: kontrollib, kas jaemüügi kandetabelites märgitud kliendi konto on peakontori kliendi koondandmetes olemas.
- Ridade arv: kontrollib, kas kande päsietabelis märgitud ridade arv kattub müügikande tabeli ridade arvuga.

## <a name="set-up-the-consistency-checker"></a>Süsteemsuskontrolli seadistamine
Seadistage pakktöötluse funktsiooni „Kontrolli kaupluse kandeid” regulaarne käitamine jaotises **Jaemüük \> Jaemüügi IT \> Kassa sisestamine**. Pakett-tööd saab ajastada kaupluse organisatsiooni hierarhia alusel, sarnaselt protsesside „Väljavõtte arvutamine partiina” ja „Väljavõtte sisestamine partiina” seadistamisega. Soovitame konfigureerida pakktöötluse nii, et seda käitataks mitu korda päevas, ja ajastada käitamise iga P-töö lõpus.

## <a name="results-of-validation-process"></a>Kontrollimisprotsessi tulemused
Pakktöötluse kontrolli tulemused märgistatakse sobivas jaemüügikandes. Jaemüügikande kirje väljal **Kinnitamise olek** on märge **Õnnestus** või **Tõrge** ning viimase kontrollimise kuupäev kuvatakse väljal **Viimase kinnitamise aeg**.

Kontrollimistõrkega seotud täpsema tõrketeksti vaatamiseks valige asjakohane jaemüügikande kirje ja seejärel klõpsake nuppu **Valideerimistõrked**.

Kandeid, mille kontroll nurjub või mis ei ole veel kontrollitud, ei lisata väljavõtetesse. Protsessi „Väljavõtte arvutamine” ajal teavitatakse kasutajaid, kui teatud kandeid ei saanud väljavõttesse kaasata.

Ainus viis valideerimistõrke lahendamiseks on võtta ühendust Microsofti toega. Tulevases versioonis lisatakse funktsioonid, mis võimaldavad kasutajatel nurjunud kirjeid kasutajaliidese kaudu parandada. Samuti tulevad saadavale logimise ja auditeerimise funktsioonid, mis võimaldavad muudatuste ajalugu jälgida.

> [!NOTE]
> Tulevases versioonis lisatakse täiendavad kinnitusreeglid, mis toetavad rohkem stsenaariume.
