---
title: Vestluse plaanimine ja tagasiside
description: Selles teemas antakse teavet vestluse plaanimise ja tagasiside tegevuste kohta rakenduses Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2019
ms.locfileid: "374884"
---
# <a name="interview-scheduling-and-feedback"></a>Vestluse plaanimine ja tagasiside

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Tegevus Plaanur

Andmeedastaja tegevus on valikuline ja koosneb kahest osast: kandidaadi saadavuspäring ning graafik. Kandidaadi kättesaadavuse komponent võimaldab kasutada kandidaadi kättesaadavuse küsimiseks meili. Graafiku komponent võimaldab planeerida töövestlusi kandidaadi ja värbamistöörühma vahel.

### <a name="candidate-availability-request"></a>Kandidaadi saadavuspäring

Kandidaatidele nende kättesaadavuse kohta küsimiseks meilisõnumi saatmiseks valige väli **Küsi kandidaadi kättesaadavust**. Kui see väli on valimata, siis seda etappi tööle värbamise protsessis ei kuvata.

Saadavuspäringu saatmiseks klõpsake käsku **Saada päring**, valige saadavuse kuupäevad ja meilimall ning saatke meil kandidaadile.

[![Attracti värbajavaade kandidaadi saadavuspäringu saatmiseks](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Kui kandidaat saab meili päringule vastamiseks, saab ta kandidaadiportaali sisse logida, valida oma saadavusele vastavad kuupäevad ja klõpsata nuppu **Edasta**.

### <a name="schedule"></a>Planeeri
Vestluse andmeedastaja jaoks on saadaval mitu konfiguratsiooni, mille abil vestluslõim kiiresti luua ning see intervjueerijatele ja kandidaadile saata.

1. Klõpsake nuppu **Loo graafik** ja sisestage boksi **Lisa intervjueerijaid** kõik intervjueerijad, kes peavad kuuluma vestluslõime.
[![Attracti värbajavaade vestluslõime plaanimise alustamiseks](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Kui kandidaat on vestluse saadavuse päringule vastanud, täidetakse väli **Vestluse kuupäev** tema tehtud valikuga. Vajaduse korral saate valida teise kuupäeva.
    
    Kui valite välja **Tee sellest paneelvestlus**, teisaldatakse vasakul olev intervjueerijate grupp vestluse loomiseks üksikusse paneelilõime. Seejärel peate määratlema vestluste seeria.
    
    Vestluse graafik tuleks korraldada nii, et see sobiks kõige paremini osalejate saadavusega. Kui kandidaat on sisemine, saate nende kättesaadavuse lisada graafikusoovituse osana.
    
    Veebikohtumise pidamiseks valige väli **Lisa Skype’i koosolek** ja iga vestlussündmus saab lingi **Skype for Business**.

2. Valige iga vestlussündmuse kestus ja klõpsake **OK** graafiku loomiseks.

    Kui suvand **Soovitused** on valitud, kuvatakse soovitused ja vestluseruudustik eeltäidetakse. Näete kõiki valitud intervjueerijate praegust saadavust kalendris. Samuti saate vaadata kandidaadi kalendrit, kui tegemist on sisemise kandidaadiga.

3. Kui soovitusi pole saadaval, klõpsake veerus **Intervjueerijad** ajavahemikul, sisestage vestluse pealkiri ja üksikasjad ning sisestage vajaduse korral asukohaandmed. Saate lisada vestlusele lingi **Skype for Business**.

4. Intervjueerijate lisamiseks klõpsake ruudustiku veergu **Lisa intervjueerijaid**, et valida üks või mitu intervjueerijat. Vestluse saate lõimest eemaldada, kasutades nuppu (...).
    
5. Kui vestlused on plaanitud teise ajavööndisse, valige paremal ülal asuvast ripploendist linn/ajavöönd. Intervjueerija saadavusruudustikku värskendatakse uue ajavööndi kajastamiseks. Ajavööndi valik kuvab nüüd ka vaate **Vestluse kokkuvõte**, mida jagatakse intervjueerijate ja kandidaadiga. 

6. Klõpsake käsku **Saada intervjueerijatele**, et saata koosolekukutsed kaasatud intervjueerijatele.

    Kui vestlusetaotlused on intervjueerijatele saadetud, saavad nad vastata otse saadud meilikutses.

    >[!NOTE]
    > Kõik üks-ühele intervjuude meeldetuletused saadetakse küsitlejatele iga 24 tunni tagant, kui intervjueerija ei vastanud (nõustunud või keeldunud) vestluse taotlusele.

    > Ühegi paneelivestluse puhul pole vestlusetaotluse jaoks automaatseid meeldetuletusi. Meeldetuletuse käivitamiseks käsitsi redigeerige intervjuu ja kasutage **värskendada ja saata** valikut, et saata taotlus tagasi küsitlejatele.

    Intervjueerija vastused talletatakse ja kuvatakse Attractis. Kui intervjueerija keeldub vestlusest, teavitatakse teid, et saaksite muudatuse teha. Vastuse kuvamiseks **Andmeedastaja** ruudustikuvaates klõpsake mulliikooni.

[![Attracti värbajavaade intervjueerija vastusest](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Kui vestluse graafik on kandidaadiga jagamiseks valmis, klõpsake käsku **Saada kandidaadile**. Saate intervjueerijate nimed ja pesad kandidaadi jaoks peita või kuvada.

8. Valige meilimall ja saatke vestluse kokkuvõte kandidaadile. Kandidaat saab seda teavet vaadata nii meilis kui ka kandidaadiportaalis.
    
>[!NOTE] 
> Kandidaadi saadavus kuvatakse kalendris ainult siis, kui kandidaat on sisemine. Samuti saab ainult sisemist kandidaati kasutada vestluse graafikusoovituste täiustamiseks. Praegu ei saa kandidaadid (ei välised ega sisemised) meili teel koosolekukutset, vaid ainult vestluste kokkuvõtte.

## <a name="feedback-activity"></a>Tegevus Tagasiside

Tagasisidetegevus on töömallis valikuline. See tegevus võimaldab vestlusel osalejatel sisestada kandidaadile soovitusi või tagasisidet. Kui valitud on väli **Tuleta tagasisides osalejad värbamistöörühmast**, sisestatakse värbaja, värbamisjuht ja intervjueerijad automaatselt tagasisidetegevusse. Organisatsioonid võivad lubada intervjueerijatel enne tagasiside andmist vaadata teiste inimeste tagasisidet. Organisatsioonid võivad ka lubada pärast tagasiside andmist intervjueerijatel seda muuta. Töömalli osana tuletatakse eelmääratud konfiguratsiooni põhjal intervjueerijatele meelde esitada hiljuti korraldatud vestluste puhul tagasisidet. Värbamisjuht või värbaja saab intervjueerijale tagasiside andmise kohta ka käsitsi meeldetuletuse saata.

## <a name="interview-activity"></a>Tegevus Töövestlus

Vestlustegevus on valikuline ja koosneb kolmest osast: kandidaadi saadavuspäring, graafik ning tagasiside. Kasutage töömallis vestlustegevust, kui soovite kandidaadi saadavuspäringu, graafiku ja tagasiside määrata protsessi osaks, mitte kasutada neid ükshaaval värbamisprotsessi osana.
