---
title: Kassa ekraanipaigutuste konfigureerimine
description: "Selles teemas käsitletakse Microsoft Dynamics 365 for Operationsi jaemüügikassa ekraanipaigutusi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: efded720c40feb8a4541b52b40b88c377e32594e
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Kassa ekraanipaigutuste konfigureerimine

[!include[banner](includes/banner.md)]


Selles teemas käsitletakse Microsoft Dynamics 365 for Operationsi jaemüügikassa ekraanipaigutusi.

Microsoft Dynamics 365 for Operationsi jaemüügikassa kasutajaliidest saab konfigureerida kauplustele, registritele ja/või kasutajatele määratud visuaalsete profiilide ja ekraanipaigutuste kombinatsiooni abil.

## <a name="visual-profile"></a>Visuaalne profiil
Visuaalsed profiilid määratakse registritele ja neid kasutatakse kasutajate vahel jagatavate registripõhiste visuaalsete elementide määramiseks. Kõigil kasutajatel, kes registrisse logivad, on sama kujundus, värvid ja pildid. 

**Profiili number** – profiili number on visuaalse profiili ainuidentifikaator. 

**Kirjeldus** – kirjeldus võimaldab määrata kirjeldava nime, mis aitab tuvastada teie olukorra jaoks sobiva profiili.

**Kujundus** – kasutajad saavad valida heleda või tumeda rakenduse kujunduse. Need sätted mõjutavad fonti ja taustavärve kogu rakenduses.

**Rõhuvärv** – rõhuvärvi kasutatakse kogu kassas teatud visuaalsete elementide (nt paanide, käsunuppude või hüperlinkide) eristamiseks või esiletõstmiseks. Tavaliselt eeldavad need elemendid kasutajatoimingut.

**Päise värv** – päise värv võimaldab kasutajal konfigureerida lehe päise värvi jaemüüja tootjakohanduste vajaduste järgi. See funktsioon on saadaval ainult Dynamics 365 for Operationsi versioonis 1611.

**Sisselogimise taustad** – kasutajad saavad määrata sisselogimisekraani taustapildi. Taustapiltide failid peaksid olema võimalikult väikesed, kuna suurte failide talletamine ja laadimine võib mõjutada rakenduse toimimist ja jõudlust.

**Rakenduse taust** – kassas saab ühevärvilise kujunduse asemel kogu rakenduses taustana ka pilti kasutada. Nagu sisselogimistaustade puhul, soovitatakse kasutada võimalikult väikseid faile.

## <a name="screen-layouts"></a>Ekraani paigutused
Ekraanipaigutuse konfiguratsioon määratleb juhtelementide toimingud, sisu ja paigutuse kassa tervitusekraanil ning kande ekraanil. 

**Tervitusekraan** – enamasti on tervitusekraan leht, mida kasutajad näevad, kui nad alguses kassasse sisse logivad. Tervitusekraan võib koosneda kaubamärgipildist ja nupupaneelidest, millelt pääseb kassatoimingute juurde. Tavaliselt paigutatakse siia toimingud, mis ei ole jooksva kande põhised. 

**Kandeekraan** – kandeekraan on kassa põhiekraan müügikannete ja tellimuste töötlemiseks. Kandeekraani saab konfigureerida ekraanipaigutuse kujundaja abil. 

**Vaikeavakuva** – mõned jaemüüjad eelistavad, et kassapidaja läheks pärast sisselogimist kohe kandeekraanile. Vaikeavakuva seadistus võimaldab kasutajal seda iga ekraanipaigutuse puhul määrata.

### <a name="assignment"></a>Määramine

Ekraanipaigutusi saab määrata kaupluse, registri või kasutaja tasandil. Kasutaja määramine tühistab registri ja kaupluse määramise ning registri määramine tühistab kaupluse määramise. Lihtsas stsenaariumis, kus kõik kasutajad kasutavad sama paigutust, olenemata registrist või rollist, saab ekraanipaigutuse määrata ainult kaupluses. Kui teatud registrid või kasutajad nõuavad spetsiaalseid paigutusi, saab neid vastavalt määrata.

### <a name="layout-sizes"></a>Paigutuse suurused

See funktsioon kehtib ainult Dynamics 365 for Operationsi versioonis 1611. Kuna paljudel juhtudel saab ekraanipaigutusi kasutada mitme ekraani suuruse ja eraldusvõimega, saavad kasutajad nende paigutust ja sisu igaühe puhul konfigureerida. Kassarakendus valib käivitamisel automaatselt seadmele lähima paigutuse suuruse. Ekraanipaigutus võib sisaldada ka nii täis- kui ka kompaktseadmete konfiguratsioone. See konfiguratsioon võimaldab määrata kasutaja ühele ekraanipaigutusele, mis töötab kaupluses mitmesuguste suuruse ja vormi tegurite lõikes. 

**Modern POS – täispaigutus** – täispaigutused sobivad tavaliselt kõige paremini suurematele ekraanidele, näiteks arvutikuvaritele või tahvelarvutitele. Kasutajad saavad valida, milliseid kasutajaliidese elemente kaasata, määrata nende suuruse ja paigutuse ning konfigureerida nende üksikasjalikke omadusi. Täispaigutused toetavad nii vertikaal- kui ka horisontaalkonfiguratsioone. 

**Modern POS – kompaktne** – kompaktsed paigutused sobivad tavaliselt kõige paremini telefonidele või väikestele tahvelarvutitele. Kompaktsete seadmete puhul on kujundusvõimalused piiratud. Kasutajad saavad konfigureerida sissetuleku ja kogusummade paanide veerge ja välju.

### <a name="screen-layout-designer"></a>Ekraani paigutuse kujundaja

Iga paigutuse suurust ekraanipaigutuses tuleb konfigureerida ekraanipaigutuse kujundaja abil. Kujundaja võimaldab kasutajatel määrata ja konfigureerida ekraani Kanne kasutajaliidese elemente. Ekraanipaigutuse kujundaja kasutab ClickOnce’i rakenduse uusima versiooni allalaadimiseks, installimiseks ja käivitamiseks iga kord, kui kasutaja sellele juurde pääseb. Veenduge, et kontrolliksite brauserinõudeid ClickOnce’i kasutamiseks – mõned brauserid (nt Chrome) nõuavad laiendusi. 

**Numbriklahvistik** – numbriklahvistik on kassa ekraani Kanne peamine kasutaja sisestusvahend. Selle saab konfigureerida kuvama terve ekraaniklahvistiku, mis on ideaalne puuteekraanide puhul, või ainult sisestusvälja, mida saab kasutada koos füüsilise klaviatuuriga. Numbriklahvistiku sätted on saadaval ainult tervikpaigutuses. Dynamics 365 for Operationsi versioonis 1611 on kompaktpaigutuste puhul ekraanil Kanne saadaval alati täielik numbriklahvistik.

**Kogusummade paneel** – kogusummade paneeli saab konfigureerida ühes või kahes veerus kuvama välju nagu ridade arv, allahindluse summa, tasud, vahesumma ja maksud. Dynamics 365 for Operationsi versioonis 1611 toetavad kompaktpaigutused ainult ühe kogusummade veergu. 

**Sissetulek** – sissetuleku paan sisaldab müügiridu, makseridu ja tarneteavet kassas töödeldavate toodete ning teenuste kohta. Kasutajad saavad määrata veerge, laiusi ja paigutust. Dynamics 365 for Operationsi versiooni 1611 kompaktpaigutuses saate konfigureerida ka lisateavet, mis kuvatakse real põhirea all. 

**Kliendikaart** – kliendikaart näitab praegu kandega seotud kliendi andmeid. Kliendikaardi saab konfigureerida lisateavet peitma või kuvama. 

**Vahekaardi juhtelement** – vahekaardi juhtelemendi saab paigutada ekraanipaigutuse peale ja teised juhtelemendid (nt numbriklahvistiku, kliendikaardi või nupupaneelid) saab paigutada vahekaardi sisse. Vahekaardi juhtelement on konteiner, mis aitab kasutajatel ekraanile rohkem sisu paigutada. Vahekaardi juhtelement on saadaval ainult täispaigutuste puhul. 

**Pilt** – pildi juhtelementi saab kasutada kaupluse logo või muu tootjakohanduse teabe kuvamiseks kandekuval. Pildi juhtelement on saadaval ainult täispaigutuste puhul. 

**Soovitatud tooted** – kui soovitatud toodete juhtelement on keskkonna jaoks konfigureeritud, näitab see masinõppel põhinevaid tootesoovitusi. Dynamics 365 for Operationsi versioonis 1611 on soovitatud toodete juhtelement saadaval ainult täispaigutuste puhul. **Kohandatud juhtelement **– kohandatud juhtelement toimib ekraanipaigutuses kohatäitena, mis võimaldab kasutajatel kohandatud sisu jaoks ruumi reserveerida. Kohandatud juhtelement on saadaval ainult täispaigutuste puhul.

<a name="see-also"></a>Vt ka
--------

[Jaemüügikassa paigutuse kujundaja installimine](install-pos-layout-designer.md)




