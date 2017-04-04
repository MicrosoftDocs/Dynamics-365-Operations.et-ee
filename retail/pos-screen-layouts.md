---
title: Seadistada ekraani paigutusega POS
description: "See teema pakub teavet ekraani paigutusega Microsoft Dynamics 365 toiminguteks - jaemüügi punkti Müügikoht (POS) kogemusi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Seadistada ekraani paigutusega POS

See teema pakub teavet ekraani paigutusega Microsoft Dynamics 365 toiminguteks - jaemüügi punkti Müügikoht (POS) kogemusi.

Operatsioonide - punkti Retail Müügikoht (POS) kasutajaliidese Microsoft Dynamics 365 saab seadistada kasutades visual profiilid ja ekraani paigutusega, kauplustes, registrite ja/või kasutaja määratud.

## <a name="visual-profile"></a>Visuaalne profiil
Visuaalne profiilid on määratud registrites ja visuaalseid elemente, mis on registri konkreetse ja jagatud kogu kasutajate määramiseks. Kasutaja, kes logib registrisse on sama teema, värve ja pilte. **Profiil arv** -profiil on visuaalne profiili ainuidentifikaator. **Kirjeldus** -kirjeldus saate määrata tähendusrikas nimi, mis aitab tuvastada õige profiili oma olukorrale. **Teema** -saavad kasutajad valida hele või tume rakenduse kujundused. Need sätted mõjutavad kogu rakenduse font ja taust värvid. **Värvi aktsent** -rõhuvärvi kasutatakse kogu tootjaorganisatsioonid eristada või esile teatavad visuaalsed efektid, nagu plaadid, käsunuppude või hüperlinke. Need elemendid on tavaliselt vaidlustatavad. **Päise värv** -päise värv võimaldab kasutajal seadistada värvi päisesse jaemüüja branding vajaduste rahuldamiseks. See funktsioon on ainult saadaval Dynamics 365 toiminguid versiooni 1611. **Logi sisse taust** -kasutaja saab määrata sisselogimine taustapilti. Tausta pildid mahtu tuleks hoida võimalikult väike, nagu ladustamine ja laadimine suuri faile võib olla mõju rakenduse käitumise ja tulemuslikkuse. **Rakenduse taust** -The POS kasutada ka pilti taustana rakenduse asemel tahke kujunduse värvi. Koos taustaga login on soovitatav hoida võimalikult väike faili suurus.

## <a name="screen-layouts"></a>Ekraani paigutused
Ekraani paigutuse konfiguratsioon määrab meetmed, sisu ja Kasutajaliidese juhtelemendid POS Welcome ekraani ja Tehingu ekraani paigutuse. ** Tervituskuva **-enamasti tervituskuva on lehekülg, mida kasutajad näevad, kui nad esimest korda sisse logida POS. Tervituskuva võib koosneda kaubamärgi pilt ja juurdepääsust POS toimingud nuppu võrgud. Tavaliselt paigutatakse siin toiminguid, mis pole seotud kandega. **Tehingu ekraani** -The tehingu ekraan on POS põhikuvale müügi- ja tellimuste töötlemiseks. Tehingu ekraani saab seadistada ekraani paigutuse kujundaja abil. **Vaikimisi start ekraan** -mõned jaemüüjad eelistavad, et kassapidaja liikuda otse Tehingu ekraani pärast sisselogimist. Start ekraani vaikesäte lubab kasutajatel luua iga ekraani paigutuse.

### <a name="assignment"></a>Määramine

Tasandil poe, register või kasutaja saab määrata ekraani paigutusega. Kasutaja alistab registri ja salvestada ülesande, ning registri määramise alistab poe määramine. Lihtne juhul, kui kõik kasutajad saate sama paigutust olenemata registri või rolli, saab määrata ekraani paigutuse ainult poest. Juhul kui teatud registrid või kasutajate nõuab spetsialiseeritud teemasid, neid saab määrata nõuetekohaselt.

### <a name="layout-sizes"></a>Paigutuse suurused

See funktsioon rakendub ainult Dynamics 365 toiminguid versiooni 1611. Sest tihti saab kasutada ekraani paigutusega vahel mitu ekraanisuuruste või eraldusvõimetega kuvamisel, kasutajad saavad konfigureerida kujunduse ja sisu iga. POS rakendus valib automaatselt lähim paigutus suurus seadme käivitamise ajal. Ekraani paigutus võib sisaldada full ja compact konfiguratsioone. See konfiguratsioon võimaldab kasutajal määrata ühe ekraani paigutuse, mis töötab üle erineva suuruse ja vormiarvude jooksul poodi. **Kaasaegne POS - täielik** -täis paigutuste on tavaliselt kõige otstarbekam kasutada suuremate kuvaritega nagu arvuti monitori või tabletid. Kasutajad saavad valida Kasutajaliidese elemendid, määrab nende suuruse ja paigutuse, ning nende üksikasjalikud atribuutide konfigureerimiseks. Täielik küljendeid toetavad vertikaal- ja horisontaalpaigutuse koosseisud. **Kaasaegne POS - kompaktne** -kompaktne paigutusega kõige paremini kasutatakse tavaliselt telefonid või väikesed tabletid. Disaini võimalused on piiratud kompaktne seadmed. Kasutajad saavad konfigureerida veerud ja väljad tarne ja kokkuvõtete paane.

### <a name="screen-layout-designer"></a>Ekraani paigutuse kujundaja

Iga paigutus suuruse ekraani paigutus peab olema konfigureeritud ekraani paigutuse kujundaja abil. Disainer võimaldab määrata ja konfigureerida Kasutajaliidese elemendid Tehingu ekraani. Ekraani paigutus disainer kasutab ClickOnce'i lae, paigaldada ja käivitada rakendus iga kord, kui kasutaja kasutab see uusim versioon. Kontrollige brauseri nõuded ClickOnce'i kasutades — brauseris Chrome, nagu nõuavad laiendid. **Numbriklahvistiku** -numbriklahvistiku on peamine Kasutaja sisendi POS Tehingu ekraani. Seda saab seadistada näitama kogu ekraanil pad, mis on ideaalne puuteekraanide jaoks, või ainult sisendi välja, mida saab kasutada klaviatuuri. Number pad seaded on saadaval ainult täielik paigutuse. Dynamics 365 toiminguid versiooni 1611, kompaktne paigutusega on alati täis numbriklahvistik kättesaadav tehingu ekraanil. **Kogusummad paneeli** - kogusummad paneeli saab seadistada kas üks või kaks veergu, et kuvada väljad, nagu näiteks rida count, hinnaalandi summa, maksud, vahesumma ja maksustamine. Dynamics 365 toiminguid versiooni 1611, kompaktne küljendeid toetavad ainult ühte kogusummade veeru. **Kätte** -** ** saamise paneel sisaldab müügiread, read ja toodete ja teenuste ning POS töödeldud tarneteabe. Kasutajatele saab määrata veergude, laiused ja paigutuse. Kompaktne paigutusega Dynamics 365 toiminguid versiooni 1611, saate konfigureerida ka täiendavat teavet, mis kuvatakse all pealiin rida. **Kliendikaardi** - seotud praegu sellega kaasnevat kliendi kliendi kaart näitab teavet. Kliendi kaardi saab konfigureerida lisateabe kuvamiseks või peitmiseks. **TAB kontrolli** - vahekaardi juhtelement võib asetada ekraani paigutuse ja muud juhtelemendid nagu numbriklahvistiku, kliendikaart, või nuppu võrkude saab paigutada vahekaart. Vahekaardi juhtelement on konteiner, mis aitab kasutajatel mahu rohkem sisu ekraanile. Vahekaardi juhtelement on täis paigutuste saadaval ainult. * Piltide **-pildi juhtelemendi kasutamist näidata poe logo või muu kaubamärgi pilt ekraanil tehingu. Pildi juhtelemendi on ainult saadaval täis paigutuste. **Soovitatavad tooted** - kui konfigureeritud keskkonna kontroll näitab toote soovitusi masinõpet põhjal soovitatud tooteid. Soovitatud tooteid on ainult saadaval täis paigutuste Dynamics 365 toiminguid versiooni 1611. ** Kohandatud juhtelemendi **-kohandatud juhtelement toimib kohatäite jooksul ekraani paigutus võimaldab kasutajatel jätta ruumi jaoks kohandatud sisu. Kohandatud juhtelemendi on ainult saadaval täis paigutuste.

<a name="see-also"></a>Vt ka
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


