---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (20. märts 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d69294b64c841c5486d694b129cf6c0f26fd93fd
ms.sourcegitcommit: c131672b02407a99aafd38957d04816a82997264
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/22/2019
ms.locfileid: "892434"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-20-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (20. märts 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="setting-the-audience-on-activities"></a>Tegevustele sihtgrupi määramine
Süsteemi tegevustele saab nüüd sihtgrupi määrata. Töötlemisega seotud tegevusi (nagu intervjuu, graafik ja EEO) saab määrata kõigi kandidaatide, sisekandidaatide ja väliste kandidaatide peale. Kohandatud tegevusi, näiteks Microsoft Forms, YouTube videod ja veebisisu saab pakkuda kõigile kandidaatidele, sisekandidaatidele, välistele kandidaatidele või värbamistöörühmale.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Karjäärisaidi töö avastamise parandamine: otsingumootori optimeerimine
See funktsioon võimaldab otsingumootori robotitel jõuda Attracti karjäärisaidi tööpostitusteni ja neid indekseerida. See aitab kandidaatidel leida Attracti karjäärisaidile postitatud töid populaarsete otsingumootorite abil.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Kuva sisselogimise vihjet kandidaatidele kes unustavad oma mandaadid
Kui kandidaat unustab talle salvestatud või e-postiga saadetud linki avades tööle kandideerimisel kasutatud sotsiaalvõrgustike mandaadid, näevad nad nüüd vihjet pakkuja nime ja kasutajanimega (varjatuna). See aitab neil oma töö kandideerimisele juurdepääsu saamiseks õigeid mandaate kasutada.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Aita sisekandidaatidel avastada ettevõttesiseseid töid
Parandati viga, kus välised kandidaadid said töö näha värbaja või personalijuhi nime. Nüüd saavad töö värbamismeeskonna liikmeid näha ainult sisemised kandidaadid. Samuti on sisekandidaatidel lihtsam näha ja kandideerida ainult ettevõttesisestele töödele. Kui kandidaat püüab saada juurdepääsu lingile, et näha või kandideerida ainult ettevõttesisesele tööle, tuleb neil end autentida Azure Active Directory mandaatidega. Sisekandidaatid saavad ka värbamismeeskonna liikmega ühendust võtta, et väljendada oma huvi töö vastu või selle kohta rohkem teada saada. See võimalus on kõigi tööde juures saadaval ainult sisekandidaatidele. Lisainfo saamiseks vt [Karjäärisaidi funktsionaalsus Attractis](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Nimetage hõbemedalistid, et määrata tulevastele ametikohtadele suure väärtusega kandidaadid
Värbajad ja personalijuhid peavad tihti jooksvat nimekirja kandidaatidest, kes olid ametikohale sobivad, kuid kellele ei saadud pakkumist teha, sest ametikoht oli juba täidetud. Sellised kandidaadid, keda nimetatakse hõbemedalistideks, on väärtuslikud, sest nad aitavad vähendada värbamisaega järgmisel korral, kui sarnane ametikoht vabaneb. Attract võimaldab nüüd värbajatel ja personalijuhtidel nimetada hõbemedaliste kandidaatide nimekirjas, kui kandidaat on läinud edasi pakkumise etappi. Hõbemedalistide tähis ilmub töö kandidaatide nimekirja, kuid ka talendikausta vaatesse, kui need kandidaadid kuuluvad mõne värbaja või personalijuhi talendikausta. Lisaks kuvatakse tähist töö ajaloos kandidaadi talendikausta profiili osana. Selle funktsiooni eelvaadet näete, kui administraator selle sisse lülitab, kasutades [halduskeskuse funktsioonide haldust](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Kandidaatide lisamine talendikaustadesse
Nüüd on kandidaate talendikausta lihtsam lisada, kasutades kandidaatide nimekirjas uus tegevust. Valides ikooni **Lisa talendikausta**, saab värbaja või personalijuht valida oma talendikaustade loendist ja lisada kerge vaevaga talendikaustadesse kandidaate otse töö kandidaatide nimekirjast.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Konfigureerige, kas konkreetsele tööle kandideerimiseks on vajalik elulookirjeldus.
Põhinedes klientide tagasisidele, on nüüd värbajatel võimalik määrata, kas üleslaetud faili vormis elulookirjeldust on konkreetsele tööle kandideerides vaja. See konfiguratsioon on kandideerimistegevuse osa, mis on värbamisprotsessis juurdepääsetav. Kui see on lubatud, palutakse igal potentsiaalsel kandidaadil ametikohale kandideerimise käigus laadida üles oma elulookirjeldus. Kandideerimisavaldust ei peeta täielikuks, kui elulookirjeldust ei ole üles laaditud. See aitab vähendada müra kandidaatide kaustas, kindlustades et iga kandidaat annab piisavalt infot, mis võimaldab värbajal neid hinnata.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidaadid saavad tööle kandideerida oma LinkedIn profiili kasutades
Kandidaadid, kellel on juba LinkedIn portaalis oma kehtiv ja värskendatud profiil, saavad seda profiili kasutades töödele kandideerida vaid ühe klõpsuga.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Jälgige, kuidas kandidaadi profiil on süsteemist tulnud ja kust teie kandidaadid neid töid avastavad, millele nad kandideerivad
Nüüd saate välja uurida, kuidas konkreetsete kandidaatide profiil Attracti jõudis, vaadates kandidaadi või talendikausta profiili **profiili** lehel kandidaadi üksikasjade all profiili allikat. Samuti saate välja uurida, kuidas mistahes kandidaat töö avastas, vaadates kandideerimistegevuse voos **Rakenduse tegevuse** all antud kandideerimise allikat. See info on saadaval ka talendikausta profiili töö ajaloo all. VKui värbajad või personalijuhid lisavad kandidaate käsitsi, palutakse ka neil määrata kandideerimise või kandidaadi profiili allikas. Kui kandidaat erimest korda kandideerib, on nende profiili allikas sama, kui nende kandideerimise päritolu. Selle funktsiooni eelvaadet näete, kui administraator selle sisse lülitab, kasutades [halduskeskuse funktsioonide haldust](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature). Pange tähele, et olemasolevatel kandidaatidel ja kandideerijatel ei ole allika andmeid. Siiski saavad värbajad need andmed käsitsi lisada.

## <a name="changes-in-onboard"></a>Muutused Onboardis

Selles versioonis on väikesed rakenduse Dynamics 365 Talent: Onboard veaparandused.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attracti integreerimine viskab kandideerimistele topeltkirje vea
Selles uuenduses on topeltkirjete probleem lahendatud. Probleem kerkib esile **Personalijuhtimise** tööruumi avamisel.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Nimeseeriat muutes ei saa vormi sulgeda
Töötaja vormil nimeseeria muutmisel tekkinud probleemi lahendamiseks on tehtud muudatusi.

## <a name="coming-soon"></a>Peagi tulekul

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Täpsem hüvitusturve (fikseeritud ja muutuv)
Paljudes ettevõtetes on hüvitise ja eeliste halduritel juurdepääs ainult teatud hüvituskirjetele. Need võivad olla juhtkonna või piirkonna töövõtjate omad. Selle muudatusega saab personaliosakond ettevõttesiseselt hüvitusplaane hallata ja säilitada erinevate töövõtjate gruppide jaoks. Saate fikseeritud ja muutuvatele plaanidele määrata turberolle, mis määravad plaanide juurdepääsu ja plaanidega seotud töövõtja andmed, näiteks palga või lisakulumikirjed. Ainult juurdepääsu saanud rollid saavad töödelda nende töötajate hüvitisi.

###  <a name="email-support-for-alerts"></a>E-posti tugi teatistele
Platvormi värskendusega 24 saavad kasutajad luua teavituse reegleid, mis saadavad kontaktidele automaatselt sündmuse käivitatud meiliteateid.

### <a name="duplicate-employee-check-interface-changes"></a>Topelt töötajate kontroll: kasutajaliidese muudatused
Selle muudatusega tuvastatakse nimeväljade sisestamisel duplikaadid ja olek näitab leitud duplikaatide arvu. Võite uue lehe avamiseks valida antud lingi, et hinnata, kas kasutada tuvastatud vastet. Andmesisestuse katkestamise vältimiseks ei avane duplikaatide vorm automaatselt.


