---
title: Vestluse plaanimine ja tagasiside
description: Selles teemas antakse teavet vestluse plaanimise ja tagasiside tegevuste kohta rakenduses Attract.
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: shielas
ms.openlocfilehash: 39b14f3ca855ca283a7484e480ff2547623938ef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517793"
---
# <a name="interview-scheduling-and-feedback"></a>Vestluse plaanimine ja tagasiside

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Tegevus Plaanur

Andmeedastaja tegevus on valikuline ja koosneb kahest osast: kandidaadi saadavuspäring ning graafik. Kandidaadi kättesaadavuse komponent võimaldab kasutada kandidaadi kättesaadavuse küsimiseks meili. Graafiku komponent võimaldab planeerida töövestlusi kandidaadi ja värbamistöörühma vahel.

Graafiku tegevuse seadistamiseks nii, et see sisaldaks või piiraks plaanitud kandidaate, valige väärtus väljast **Plaanitavad kandidaadid**. Saadaval on valikud **Kõik kandidaadid**, **Väliskandidaadid** ja **Sisekandidaadid**. Näiteks kui soovite plaanimise esimeses etapis jätta vahele sisekandidaadid, saate määrata graafiku tegevuse ainult väliskandidaatidele, määrates valiku **Plaanitavad kandidaadid** valikule **Väliskandidaadid**.

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

    Kui suvand **Soovitused** on valitud, kuvatakse soovitused ja vestluseruudustik eeltäidetakse. Näete kõigi valitud intervjueerijate praegust saadavust kalendris. Samuti saate vaadata kandidaadi kalendrit, kui tegemist on sisemise kandidaadiga. Intervjueerijate ja sisekandidaatide kohta saate vaadata aega, millal nad on hõivatud, nende töötunde, kontorist väljas olemise aega ja ühtlasi tuvastada, kas nad on märkinud kalendrisse teatud aegadele, et töötavad mujal. 

3. Kui soovitusi pole saadaval, klõpsake veerus **Intervjueerijad** ajavahemikul, sisestage vestluse pealkiri ja üksikasjad ning sisestage vajaduse korral asukohaandmed. Saate lisada vestlusele lingi **Skype for Business**.

4. Intervjueerijate lisamiseks klõpsake ruudustiku veergu **Lisa intervjueerijaid**, et valida üks või mitu intervjueerijat. Vestluse saate lõimest eemaldada, kasutades nuppu (...).
    
5. Kui vestlused on plaanitud teise ajavööndisse, valige paremal ülal asuvast ripploendist linn/ajavöönd. Intervjueerija saadavusruudustikku värskendatakse uue ajavööndi kajastamiseks. Ajavööndi valik kuvab nüüd ka vaate **Vestluse kokkuvõte**, mida jagatakse intervjueerijate ja kandidaadiga. 

6. Klõpsake käsku **Saada intervjueerijatele**, et saata koosolekukutsed kaasatud intervjueerijatele.

    Kui vestlusetaotlused on intervjueerijatele saadetud, saavad nad vastata otse saadud meilikutses.

    >[!NOTE]
    > Kõik üks-ühele intervjuude meeldetuletused saadetakse küsitlejatele iga 24 tunni tagant, kui intervjueerija ei vastanud (nõustunud või keeldunud) vestluse taotlusele.

    > Ühegi paneelivestluse puhul pole vestlusetaotluse jaoks automaatseid meeldetuletusi. Meeldetuletuse käivitamiseks käsitsi redigeerige intervjuu ja kasutage **värskendada ja saata** valikut, et saata taotlus tagasi küsitlejatele.

    Intervjueerija vastused talletatakse ja kuvatakse Attractis. Kui intervjueerija keeldub vestlusest, teavitatakse teid, et saaksite muudatuse teha. Vastuse kuvamiseks **Andmeedastaja** ruudustikuvaates klõpsake mulliikooni.

[![Attracti värbajavaade intervjueerija vastusest](./media/schedule-interviewer-response2.png)](./media/schedule-interviewer-response2.png)

7. Kui vestluse graafik on kandidaadiga jagamiseks valmis, klõpsake käsku **Saada kandidaadile**. Saate intervjueerijate nimed ja pesad kandidaadi jaoks peita või kuvada.

8. Valige meilimall ja saatke vestluse kokkuvõte kandidaadile. Kandidaat saab seda teavet vaadata nii meilis kui ka kandidaadiportaalis.
    
>[!NOTE] 
> Kandidaadi saadavus kuvatakse kalendris ainult siis, kui kandidaat on sisemine. Samuti saab ainult sisemist kandidaati kasutada vestluse graafikusoovituste täiustamiseks. Praegu ei saa kandidaadid (ei välised ega sisemised) meili teel koosolekukutset, vaid ainult vestluste kokkuvõtte.

Kandidaadid saavad meili kokkuvõttega vestluslõimest. See meil sisaldab faili .ics, mille saab salvestada isiklikku kalendrisse hõlpsamaks juurdepääsuks ja teatiste saamiseks intervjuu kohta.

>[!TIP] 
> Kui saadate intervjuu graafiku kandidaadile uuesti, saavad nad uue faili .ics. Soovitame värskendada meilimalle iga kandidaadi intervjuu kokkuvõtte jaoks, et tagada, et kandidaadid kustutavad varem lisatud intervjuu sündmused ega näed kalendris duplikaate. 

## <a name="feedback-activity"></a>Tagasiside tegevus

Tagasisidetegevus on töömallis valikuline. See tegevus võimaldab vestlusel osalejatel sisestada kandidaadile soovitusi või tagasisidet. 

Selleks et kaasata või piirata kandidaate, kelle kohta soovite tagasisidet anda, valige väärtus väljast **Kelle kohta peavad intervjueerijad andma tagasisidet**.  Saadaval on valikud **Kõik kandidaadid**, **Väliskandidaadid** ja **Sisekandidaadid**. Näiteks kui soovite plaanimise esimeses etapis jätta vahele sisekandidaadid, määrake väli **Kelle kohta peavad intervjueerijad andma tagasisidet** väärtusele **Väliskandidaadid**.

Kui valite välja **Tuleta tagasisides osalejad värbamistöörühmast**, sisestatakse värbaja, värbamisjuht ja intervjueerijad automaatselt tagasisidetegevusse. Organisatsioonid võivad lubada intervjueerijatel enne tagasiside andmist vaadata teiste inimeste tagasisidet. Organisatsioonid võivad ka lubada pärast tagasiside andmist intervjueerijatel seda muuta. Töömalli osana tuletatakse eelmääratud konfiguratsiooni põhjal intervjueerijatele meelde esitada hiljuti korraldatud vestluste puhul tagasisidet. Värbamisjuht või värbaja saab intervjueerijale tagasiside andmise kohta ka käsitsi meeldetuletuse saata.

## <a name="interview-activity"></a>Tegevus Töövestlus

Vestlustegevus on valikuline ja koosneb kolmest osast: **kandidaadi saadavuspäring**, **graafik** ja **tagasiside**. Kasutage vestluse tegevust töömallis, kui soovite kõiki kandidaadi saadavuspäringuid, graafikuid ja tagasisidet protsessi osana, mitte kasutada neid eraldi tegevustena.

Intervjueeritavate kandidaatide lisamiseks või piiramiseks valige väärtus väljas **Intervjueeritavad**. Saadaval on valikud **Kõik kandidaadid**, **Väliskandidaadid** ja **Sisekandidaadid**. Näiteks kui soovite intervjueerimise esimeses etapis jätta vahele sisekandidaadid, määrake väli **Intervjueeritavad** väärtusele **Väliskandidaadid**.
