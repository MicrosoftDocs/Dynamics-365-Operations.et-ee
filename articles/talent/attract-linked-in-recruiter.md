---
title: Hankimine tööriistaga LinkedIn Recruiter
description: Selles teemas kirjeldatakse masinõppe kasutamist töökohtade ja töökoha kandidaatide soovituste saamiseks.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304001"
---
# <a name="sourcing-with-linkedin-recruiter"></a>Hankimine tööriistaga LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn on maailma suurim talentide andmebaas ja tihti esmane süsteem, mida tööandjad kasutavad oma täidetavatele töökohtadele kandidaatide leidmiseks ja nendega suhtlemiseks. LinkedIn Recruiteri integreerimine rakendusega Dynamics 365 for Talent: Attract muudab kasutajatele palkamise ja andmete sünkroonimise kahe süsteemi vahel lihtsamaks.

> [!NOTE]
> Teil on vaja, et tervikliku palkamise lisamooduli ja LinkedIn Recruiteri kohad suudaksid kasutada LinkedIn Recruiteri integratsiooni Attractiga.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiteri häälestamine Attractiga 

Enne, kui saate LinkedIn Recruiteri võimalusi kasutada, peate konfigureerima lepingu tasandil või ettevõtte tasandil ligipääsu oma Attracti eksemplariga. Konfiguratsiooniprotsessi lõpuleviimiseks peate töötama kasutajaga, kes on teie LinkedIn Recruiteri lepingu administraator. LinkedIn Recruiteri konfigureerimiseks Attractiga toimige järgmiselt.

1.  Logige Attracti administraatorina sisse ja valige **Administraatori sätted**.

2.  Klõpsake vasakul paanil vahekaarti **LinkedIni integreerimine**.

[![Attracti administraatori vaade LinkedIn Recruiteri integreerimise käivitamiseks](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Klõpsake seadistuse käivitamiseks **Ühenda** ja teid juhatatakse läbi LinkedIni sisselogimise protsessi.

4.  Kui teil on töökohad mitmes LinkedIni lepingus, valige leping, mida soovite Attracti süsteemiga ühendada. Kui teil on töökoht ainult ühes LinkedIni lepingus, ei ole seda toimingut vaja.

5.  Nüüd laaditakse LinkedIni vidin teie administraatori sätetesse, kus see näitab integratsioonide loendit. Klõpsake **Recruiter süsteemi ühendamine** all valikut **Taotlus**.

[![Attracti administraatori vaade LinkedIn Recruiteri integreerimise taotlemiseks](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Pärast Attractilt integratsiooni taotlemist, kuvatakse seda kui **Partner valmis** ja see on **Recruiteri administraatori sätted** alt sisselülitamiseks valmis. Kui näete sellel lehel teadet **Teavita partnerit**, oodake paar sekundit, klõpsake teatel **Teavita partnerit** ja seejärel värskendage lehekülge. Nüüd peaks olema kuvatud teade **Partner valmis**.

[![Attracti administraatori vaade, mis näitab, et Attracti pool taotlusest on täidetud](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Järgmise etapi läbimiseks peab teil olema oma LinkedIn Recruiteri lepingu administraatori privileeg.

7.  Logige administraatori kontoga LinkedIni sisse ja minge üleval paremal asuva LinkedIn Recruiteri juurde. 

8. Klõpsake ekraani ülaosas olevas menüüs **Rohkem** valikule **Administraatori sätted** ja seejärel klõpsake **ATS** vahekaardil.

Attracti süsteem loetletakse koos mõne valikuga, mida saab sisse lülitada.

9. Kui soovite **In-ATS indikaatorile** ja **In-ATS profiilividinale** lubada ainult 1 klõpsuga eksportimise, valige **Ettevõtte tasemel juurdepääs**. Kui soovite lubada kõik ettevõttetasemel juurdepääsu funktsioonid ja InMaili ajaloo, märkuste ajaloo ning InMaili lühiprofiili juurdepääsu, valige suvand **Lepingu tasemel juurdepääs**.

10. Lülitage soovitud juurdepääsutase sisse oma LinkedIn Recruiteri **Administraator-ATS** sätetest.

[![Attracti integratsiooni sisse lülitamine LinkedIn Recruiteri administraatori vaatest](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Minge tagasi Attracti administraatori sätetesse rollis AttractAdmin ja valige vaheleht **LinkedIni integratsioon**. Nüüd peaksite nägema, et LinkedIni vidin laeb ja näitab sisse lülitatud valitud juurdepääsu tasemega **Lubatud**.

[![LinkedIn Recruiteri integreerimine lõpetatud](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>LinkedIn Recruiteri võimaluste kasutamine

Kui LinkedIn Recruiteri võimalused on Attracti administraatori poolt sisse lülitatud, saavad personalijuhid ja värbajad juurdepääsu. Nende võimaluste kasutamiseks ühendage **Kasutajasätete** alt oma LinkedIni konto. Kui nii administraatori kui ka kasutaja sätted on ühendatud, on saadaval mitmeid võimalusi.

### <a name="in-ats-profile-widget"></a>In-ATS profiili vidin

Saate Attractis vaadata kandidaadi LinkedIni profiili. LinkedIni vidin näitab kandidaadi profiili, kui ATS-i andmed kattuvad kasutajate LinkedIni andmetega.

Profiili vaatamiseks minge kas töö või talendikausta kaudu kandidaadi profiili juurde. Profiilividina laadimiseks valige kandidaadi profiilis vahekaart **LinkedIn**. Sellelt lehelt saate kandidaadi ka oma LinkedIn Recruiteri projektidesse salvestada.
1. E-posti ja LinkedIni liikme ID (täpne vaste) vaste leidmisel LinkedInis kuvatakse kandidaadi profiili. Kasutajal on endiselt võimalus profiili suvand linkida/linkimine tühistada.

2. Kui LinkedIn ei leia kandidaati e-posti või liikme ID põhjal, kuvatakse võimalike kandidaatide vastete loend vastavalt kandidaadi nime järgi ja kasutaja saab valida neist ühe ning linkida profiili.  

3. Kui LinkedIn ei leia kandidaadi nime, tuleb teade, et ei leitud ühtki vastet.

### <a name="1-click-export"></a>Ühe klõpsuga eksportimine 

LinkedInist kandidaatide otsimise ajal saate kandidaadid ühe klõpsuga hetkel vabade töökohtade juurde eksportida. Ühe klõpsuga eksportimiseks toimige järgmiselt. Enne nende etappide läbimist kontrollige, et teile on määratud töö personalijuhi või värbaja roll, ja et tööl oleks etapp **Potentsiaalselt sobiv kandidaat**.

1.  Looge töö, määrake sobivad rollid ja aktiveerige töö.

2.  Kui töö on aktiveeritud, liikuge LinkedIn Recruiterisse.

3.  Leidke otsitav kandidaat ja minge tema profiilile.

4.  Kontaktikaardi töö otsimise kasti abil leidke töö Attractis aktiveeritud töö pealkirja või töö ID-d kasutades. Kui te tööd ei leia, klõpsake õige Attracti eksemplari leidmiseks valikul **Muuda ATS**.

5. Pärast töö valimist klõpsake valikul **Ekspordi**. Kandidaat on nüüd Attracti sisse tõmmatud.

6.  Minge Attracti ja avage vastav töö. Eksporditud kandidaadi leiate töö etapist **Potentsiaalselt sobiv kandidaat**.

### <a name="in-ats-indicator"></a>In-ATS indikaator 

LinkedIn värbaja abil saate saate jälgida, kas kandidaat on kandideerinud teie organisatsioonis teistele töödele, vaadata, millistes erinevates tööle kandideerimise etappides nad on ning vaadata LinkedIn Recruiteris Attractist pärit tagasisidet ja kommentaare.

1.  Avage LinkedIn Recruiter ja leidke otsitava kandidaadi profiil.

2.  Kerige alla, et näha kandidaadi profiili jaotist **In-ATS**.

3.  Selle vidinaga saate vaadata LinkedIn Recruiteri vaate seest Attractis oleva kandidaadi kõiki andmeid.

4.  Nendega seotud tööde, viimase oleku ja iga tööga seotud liikumise vaatamiseks valige vahekaart **Tööd ja olekud**.

5.  Intervjueerijate Attracti sisestatud tagasiside vaatamiseks valige vahekaart **Vestluse tagasiside**.

6.  Selle kandidaadi kohta Attracti jäädvustatud märkuste vaatamiseks valige vahekaart **Märkused**.

> [!NOTE]
> Kandidaadi ja avalduse andmeid ei sünkroonita LinkedIni värbajaga, kui kandidaat ei ole potentsiaalne klient.

### <a name="inmail-history"></a>InMaili ajalugu

LinkedIn InMaili ajalugu on saadaval LinkedIn Recruiteri lepingutasandil juurdepääsuga. Kui see on lubatud, saate vaadata oma kogu kandidaadiga seotud InMaili ajalugu. Samuti saate vaadata, kes teie organisatsioonist on kandidaadiga veel InMaile vahetanud, kuid te ei saa vaadata nendevahelisi sõnumeid.

InMaili ajaloo vaatamiseks minge kandidaadi profiilile, vahekaardile **LinkedIn** ja kerige ajaloo vaatamiseks lehe alaserva. Kui teil on olnud kandidaadiga arutelu, saate vaadata InMaili ajalugu. InMaili sõnumid sünkroonitakse Attractiga iga paari tunni järel.

### <a name="notes-history"></a>Märkuste ajalugu 

LinkedIni märkuste ajalugu on saadaval LinkedIn Recruiteri lepingu tasandil juurdepääsuga. Kui see on lubatud, saate vaadata märkusi, mis teie organisatsiooni erinevad värbajad on kandidaadi kohta jäädvustanud.

Märkuste ajaloo vaatamiseks minge kandidaadi profiilile, minge vahekaardile **LinkedIn** ja kerige ajaloo vaatamiseks lehe allserva. Saate vaadata kõiki LinkedIn Recruiterist pärit märkusi kandidaadi kohta.

### <a name="inmail-stub-profile"></a>InMaili lühiprofiil

InMaili lühiprofiil on saadaval LinkedIn Recruiteri lepingutasandil juurdepääsuga. Kui kandidaadid nõustuvad oma LinkedIn profiile jagama mistahes teie organisatsiooni kasutajaga, saate kandidaate Attractis jälgida ning igale kandidaadile luuakse uus kandidaadi kirje. Kui kandidaat on juba olemas süsteemis e-posti aadressiga või on jaganud oma aadressi värbajaga, saate vaadata kandidaadi e-posti aadressi.

Kandidaatide loendi vaatamiseks avage **Talendikaustad**, et näha süsteemi loodud LinkdedIni talentide kausta. See talentide kaust sisaldab kandidaatide loendit ja nende LinkedInist saadud lühiprofiile, mis näitavad kandidaatide eesnime ja perekonnanime. Kandidaadi e-posti aadressi kuvatakse siis, kui kandidaat soovib oma e-posti aadressi jagada.
