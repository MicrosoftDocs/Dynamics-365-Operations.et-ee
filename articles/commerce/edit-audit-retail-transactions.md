---
title: Kaupluse kannete redigeerimine ja auditeerimine
description: Selles teemas kirjeldatakse kaupluse kannete redigeerimise ja auditeerimise funktsiooni.
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
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004385"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Kaupluse kannete redigeerimine ja auditeerimine

[!include [banner](includes/banner.md)]



Dynamics 365 Commerce'i kliendid kasutavad nii esimese kui ka kolmanda osapoole kassarakendusi. Esimese osapoole kassarakendusega lisatakse kaupluse kanded kanalitest peakontorisse pakktöötluse kaudu. Kolmanda osapoole rakendustega lisatakse kanded peakontorisse integratsiooni kaudu. Mõlemal juhul tuleb pärast kannete lisamist peakontorisse teostada süsteemsuskontrolli protsess, mis teeb kannetele mitu kontrolli, et peakontorisse sisestatavasse väljavõttesse lisataks ainult kinnituse läbinud kanded. 

Kaubanduse kannete kinnitamine nurjub eri põhjustel. Näiteks võib integratsioonikoodi või kassarakenduse programmiviga põhjustada vastuolulisi andmeid. Samuti võib vastuolulisi andmeid põhjustada kasutaja viga (nt toote kustutamine pärast kanaliga sünkroonimist või rahandusperioodi sulgemine ilma selle perioodi kandeid sisestamata).

Kuigi need kanded märgitakse lipuga ja jäetakse väljavõtetest välja, võivad kanded häirida kasutaja igapäevast protsessi, millega ta sisestab igapäevast müügiteavet finantssüsteemi.

Kaubanduses saate redigeerida konkreetseid nurjunud kinnitusega kandeid, kuid samal ajal säilitada kõigi muudatuste auditi. 

## <a name="edit-and-audit-transactions"></a>Kannete redigeerimine ja auditeerimine

Retaili versioonis 10.0.5 on sularaha- ja vedamiskanded (nt müük ja tagastused) ainsad kanded, mida saab redigeerida. Klienditellimuste või võrgutellimuste redigeerimist ei toetata. Retaili versioonis 10.0.6 ja uuemas toetatakse ka sularahahalduse kannete redigeerimist.

1. Installige Dynamicsi Exceli lisandmoodul.

2. Avage tööruum **Kaupluse rahandus**. Paanil **Kande kinnitamise tõrked** kuvatakse eelfiltreeritud vaade kandevormist, mille üks või mitu kinnitusreeglit nurjusid.
 
3. Avage vorm. Klõpsake kirjet, mille kinnitamine nurjus, klõpsake valikut **Office'i lisandmoodul** ja siis klõpsake valikut **Redigeeri valitud kannet**. Avatakse valitud kande üksikasjadega Exceli fail, kus on järgmised töölehed.

    - Read: sellel töölehel on kande päise- ja tooteread ning seotud andmed.
    - Maksed: sellel töölehel on kande makseridade üksikasjad.
    - Allahindlused: sellel töölehel on kande allahindlusega seotud üksikasjad.
    - Maksud: sellel töölehel on kande maksudega seotud üksikasjad.
    - Tasud: sellel töölehel on kande tasudega seotud andmed.

4. Exceli failis saate muuta asjakohaseid välju ja seejärel laadida andmed uuesti üles peakontorisse, kasutades Dynamicsi Exceli lisandmooduli avaldamisfunktsiooni. Pärast avaldamist kajastatakse muudatused süsteemis. Avaldamise ajal ei läbi kasutajate muudatused ühtegi kinnitamist.

5. Muudatuste täieliku kontrolljälje vaatamiseks klõpsake päises **Jaemüügikanne** (päisetaseme muudatuste nägemiseks) ning asjakohase kande lehe asjakohases jaotises ja kirjes valikut **Kuva kontrolljälg**. Kõik müügiridadega seotud muudatused on näiteks nähtavad lehel **Müügikanded**, maksetega seotud muudatused on nähtavad lehel **Maksekanded** jne. Auditi andmed, mida muudatuste puhul hallatakse, on järgmised.

   - Muutmise kuupäev ja kellaaeg
   - Väli 
   - Varasem väärtus
   - Uus väärtus
   - Muutja:

6. Pärast muudatuste tegemist ja avaldamist käivitage uuesti suvand **Kinnita kaupluse kanded**, et kontrollida, kas teie tehtud muudatused on süsteemsed ja kehtivad.

> [!NOTE]
> Saate redigeerida ainult kinnituse mitteläbinud kandeid. Kui soovite redigeerida kinnituse läbinud kandeid, määrake muudetava kande kinnitamise olekuks **Tõrge** või **Pole** ja siis saate seda redigeerida. 


## <a name="bulk-edit-transactions"></a>Kannete hulgiredigeerimine

Retaili versioonis 10.0.6 ja uuemates toetatakse kannete hulgiredigeerimist väljavõtte tasemel. 

1. Avage Exceli lisandmooduli abil väljavõte, milles on kanded, mida soovite muuta. Selleks täitke eespool nimetatud juhised 1–3.

2. Valige üks allolevatest suvanditest.

    - **Redigeeri sularaha- ja vedamiskandeid**. See suvand võimaldab teil redigeerida kõiki väljavõttes sisalduvaid sularaha- ja vedamiskandeid. Saadaval on järgmised Exceli töölehed.
    
       - **Kanne**: sellel töölehel on kogu müügikannete päisetaseme teave.
       - **Müügikanne**: sellel töölehel on kogu müügikannete reataseme teave.
       - **Maksekanded**: sellel töölehel on kogu müügikannete makseridade teave.
       - **Allahindluskanded**: sellel töölehel on kogu müügikannete allahindlusridade teave.
       - **Maksukanded**: sellel töölehel on kogu müügikannete maksuridade teave.
       - **Tasukanded**: sellel töölehel on kogu müügikannete tasuridade teave.

    - **Muuda kassahalduskandeid**. See suvand võimaldab teil redigeerida kõiki väljavõttes sisalduvaid kassahalduskandeid. Saadaval on järgmised Exceli töölehed.
     
       - **Kanne**: sellel töölehel on kogu kassahalduskannete päisetaseme teave.
       - **Panka hoiustatud maksevahendi kanded**: sellel töölehel on kõik panka hoiustamise kande üksikasjad.
       - **Seifi maksevahendi kanded**: sellel töölehel on kõik seifi hoiustamise kande üksikasjad.
       - **Päevakassa**: sellel töölehel on kõik päevakassa kande üksikasjad.
       - **Tulu/kulu kanne**: sellel töölehel on kõik tulu/-kulu kande rea üksikasjad.
       - **Maksekanded**: sellel töölehel on kogu toimingu **Arve tasumine** ja samuti tulu/kulu kande maksega seotud teave.

3.  Kui avaldate hulgiredigeeritud kandeid, siis kinnitamisi ei tehta. Peate veenduma, et kõik teie muudatused on täpsed ja andmete kvaliteet on kõigil töölehtedel tagatud. Kui soovite näiteks muuta kande kuupäeva, et hallata stsenaariume, kus avatud kannete rahandus- või laovarude periood suletakse, peate muutma kuupäeva kõigil Exceli töölehtedel, millel on veerg **Ärikuupäev**. Kannete kinnitamiseks pärast nende redigeerimist saate lehel **Väljavõtted** kasutada valikut **Kinnita kanded uuesti**.
