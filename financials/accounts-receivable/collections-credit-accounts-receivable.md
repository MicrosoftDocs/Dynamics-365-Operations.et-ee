---
title: "Kreedit ja sissenõuded moodulis Müügireskontro"
description: "Kontode saadaolevad kogusid andmeid haldab üks keskne vaade, kasutades Microsoft Dynamics 365 toimingute kogud leht. Krediidiosakonna juhatajad saavad kasutada seda keskset vaadet sissenõuete haldamiseks. Inkassaatorid saavad alustada sissenõudmise protsessi klientide loendist, mis luuakse eelmääratud sissenõude kriteeriume kasutades, või lehelt Kliendid.."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: d6722a788ed5a89d894ed937129aa1662c2eaebe
ms.lasthandoff: 03/31/2017


---

# <a name="credit-and-collections-in-accounts-receivable"></a>Kreedit ja sissenõuded moodulis Müügireskontro

Kontode saadaolevad kogusid andmeid haldab üks keskne vaade, kasutades Microsoft Dynamics 365 toimingute kogud leht. Krediidiosakonna juhatajad saavad kasutada seda keskset vaadet sissenõuete haldamiseks. Inkassaatorid saavad alustada sissenõudmise protsessi klientide loendist, mis luuakse eelmääratud sissenõude kriteeriume kasutades, või lehelt Kliendid..

Enne sissenõuete seadistamist või nendega töötamist peaksite teadma järgmisi põhimõtteid.
-   Kliendi aegumise hetktõmmised sisaldavad aegunud saldoteavet teatud ajahetkel
-   Sissenõuete kliendikaustad aitavad teil oma tööd korraldada
-   Inkassaatoritel võivad olla oma kliendikaustad
-   Loendilehtedel korraldatakse sissenõuete kliendid, tegevused ja juhtumid
-   Kogu kliendi sissenõuete teave on ühel lehel ja saate tegevusi sellelt lehelt teha
-   Intresside ja tasude puhul saab loobumise, ennistamise või tühistamise teha ühe etapina
-   Mahakandmiskanded saab luua ühe etapina
-   Ebapiisavate vahendite (NSF) maksed saab töödelda ühe etapina

Järgmised jaotised kirjeldavad iga põhimõtet.

## <a name="customer-aging-snapshots"></a>Kliendi aegumise hetktõmmised 
Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel. See teave kuvatakse loendilehel Aegunud saldod ja lehel Sissenõuded. Enne kui saate teavet loendilehtedel Sissenõuded vaadata, tuleb luua aegumise hetktõmmis. 

Iga kliendi puhul sisaldab aegumise hetktõmmis aegumise hetktõmmise päist ja üksikasjalikke kirjeid, mis vastavad igale aegumisperioodile aegumisperioodi definitsioonis. 

Aegumise hetktõmmise päis sisaldab tasumisele kuuluvat kogusummat, krediidilimiiti, saatelehe summat, müügitellimuse summat, vaidlustatud kannete arvu ja kliendikonto vaidlustatud kannete kogusummat. Kõik kliendi kanded kaasatakse nende summade arvutusse. Tasumisele kuuluv kogusumma, krediidilimiit, saatelehe summa ja müügitellimuse summa kuvatakse lehe Sissenõuded kiirkaardil Krediiditeave. 

Aegumise hetktõmmise üksikasjalik kirje luuakse iga aegumisperioodi kohta aegumisperioodi definitsioonis. Iga aegumisperioodi hetktõmmise üksikasjade kirje sisaldab aegumisperioodi ID-d ja aegumisperioodi jäävate kuupäevadega kannete kogusummat. Kanded määratakse aegumisperioodile, näiteks 30 päeva üle tähtaja. Kuupäev on seotud aegumise hetktõmmise loomisel määratud aegumiskuupäevaga. See teave kuvatakse loendilehel Aegunud saldod ja lehe Sissenõuded kiirinfos Aegunud saldod.

## <a name="collections-customer-pools"></a> Sissenõuete kliendikaustad 
Kliendikaustad päringud, mis määratlevad kliendikirjete grupi, mida saab sissenõuete või aegumisprotsesside jaoks kuvada ja hallata. Kliendikaustadega saate filtreerida teavet loendilehtedel Aegunud saldod, Sissenõuete tegevused ja Sissenõuete juhtumid. Kliendikaustadega saate ka filtreerida kliendikontosid, mis kaasatakse aegumise hetktõmmiste loomisel.

## <a name="collections-agents"></a>Inkassaatorid
Vaikimisi Microsoft Dynamics 365 toimingute kasutajad saate vaadata kõikide klientide teavet kollektsioonide nimekiri lehekülgedel. Inkassaatorikirjete abil saate määrata kliendikaustad, mis on saadaval sissenõuete loendilehtedel ja lehel Sissenõuded oleva teabe filtreerimiseks. 

Inkassaator on isik, kes teeb koostööd klientidega, et makseid kogutaks õigeaegselt. Microsoft Dynamics 365 operatsioonide kogud ained on töötajaid, kes määratakse kasutajatele kasutaja seadistuse lehel.

## <a name="collections-list-pages"></a> Sissenõuete loendilehed 
Järgmiste loendilehtede abil saate sissenõuete teavet korraldada.
-   Aegunud saldod – loendilehe veergudel kuvatakse kliendisaldod ja aegunud summad aegumisperioodi järgi. See teave salvestatakse aegumise hetktõmmisesse. Aegumisperioodid on määratud kasutatava aegumisperioodi definitsiooniga. Aegumisperioodi definitsioon võetakse kliendikaustast, kui see on kaustale määratletud. Kui kliendikaustal ei ole aegumisperioodi definitsiooni, kasutatakse lehel Müügireskontro parameetrid määratud aegumisperioodi vaikedefinitsiooni. Kui aegumisperioodi vaikedefinitsiooni ei ole määratud, kasutatakse esimest aegumisperioodi definitsiooni lehel Aegumisperioodi definitsioonid.
-   Sissenõuete tegevused – loendilehe veerud, kus kuvatakse sissenõuete tegevustena määratletud tegevused. Need tegevused on loodud lehel Sissenõuded. Kasutage tegevusi, et jälgida sissenõuetega seoses tehtavat tööd.
-   Sissenõuete juhtumid – loendilehe veerud, kus kuvatakse teavet juhtumite kohta, millel on juhtumikategooria juhtumitüübiga Sissenõuded.

> [!NOTE]
> Enne kui saate teavet neil loendilehtedel vaadata, tuleb luua aegumise hetktõmmis. Teave kuvatakse ainult klientide puhul, kelle kohta on loodud aegumise hetktõmmis. Loendilehel kuvatavaid kirjeid saab täiendavalt filtreerida järgmiselt.
<li>Vaikimisi Microsoft Dynamics 365 toimingute kasutajale on juurdepääs kõigile klientidele, kes on vananevas hetktõmmise.</li>
<li>Kliendikaustade olemasolul peab kasutaja olema seadistatud inkasaatorina, et kasutada kaustu sissenõuete loendilehtedel oleva teabe filtreerimiseks. Teave on piiratud klientidega, kes kuuluvad valitud kliendikausta.</li>
<li>Kui kasutaja on seadistatud inkassaatorina, on loendilehel saadaval ainult selle inkassaatori jaoks valitud kaustad. Kui inkassaatori puhul on lehel Inkassaator märgitud ruut Luba inkassaatoril vaadata kõiki kliendikaustu, on kõik kaustad selle inkassaatori jaoks saadaval.</li>


## <a name="collections-page"></a> Leht Sissenõuded
Lehel Sissenõuded saate vaadata ja hallata kliendi sissenõudeteavet, -tegevusi ja -juhtumeid ning nendega tegevusi teha. 

Ülemisel paanil kuvatakse valitud kliendi juhtudel. Keskmisel paanil kuvatakse kliendi kanded. Alumisel paanil kuvatakse kliendi tegevused. Saate luua sissenõudejuhtumid, et jälgida sissenõudeteavet ühe või mitme kande ja tegevuse kohta. Ülemise ja alumise paani teavet saab juhtumi alusel filtreerida. 

Kiirinfodes kuvatakse valitud kliendi aegunud saldod ja krediidilimiit. See teave salvestatakse aegumise hetktõmmisesse. Vajaduse korral saate aegumise hetktõmmist värskendada. 

Toimingupaanil on nupud, mis kuvavad valitud kliendi, juhtumi, kande või tegevusega seotud teavet. Saate teha ka üldisi tegevusi, näiteks muuta kande sissenõuete olekut, saata meiliteavitusi oma meiliteenuse pakkuja integratsiooni kaudu, anda klientidele hüvitisi, töödelda NSF-makseid ja kanda kogumatuid saldosid maha.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Intressi ja tasude nõudest loobumine, selle ennistamine või tühistamine
Saate loobuda täielike viivisearvete või tasude ja kandeintresside, mis on osa viivisearvest, nõudest, neid ennistada või tühistada. Saate seda teha loendilehe Kõik kliendid toimingupaani vahekaardil Sissenõudmine, klõpsates suvandit Viivisearve, Kandeintress või Tasu. 

Need korrigeerimised mõjutavad ainult viivisearveid ning neis sisalduvat intressi ja tasusid. Kasutage kõigi tasude, mida klient võlgneb, mahakandmiseks jaotise „Mahakandmiskannete loomine ühe etapina” etappe.

## <a name="create-writeoff-transactions"></a>Writeoff kannete loomine
Saate maha kanda lootusetuid võlgu, klõpsates vormil Sissenõuded ning loendilehtedel Aegunud saldod, Kliendid ja Avatud kliendiarved suvandit Mahakandmine. 

Kliendi kannete mahakandmisel märgitakse kliendi kõik kanded automaatselt tasakaalustamiseks. Mahakantav summa sõltub märgitud kannete netosummast. Mahakandmise kanne luuakse päevaraamatus ja see võib sisaldada kuni kolme tüüpi tööleheridu.

-   Esimest tüüpi tööleherida sisaldab kliendi mahakandmiskirjet. Kui märgitud kanded sisaldavad mitut valuutakoodi, dimensiooni ja sisestusreeglite kombinatsiooni, luuakse iga kombinatsiooni kohta eraldi tööleherida.
-   Teist tüüpi tööleherida sisaldab pearaamatu mahakandmiskirjet. Kui märgitud kanded sisaldavad mitut valuutakoodi, dimensiooni ja sisestusreeglite kombinatsiooni, luuakse iga kombinatsiooni kohta eraldi tööleherida.
-   Kolmandat tüüpi tööleherida sisaldab pearaamatu mahakandmisteavet käibemaksu kohta. See tööleherida luuakse ainult siis, kui lehel Müügireskontro parameetrid on märgitud ruut Eraldi käibemaks. Kui märgitud kanded sisaldavad mitut tasumisele kuuluva käibemaksu konto, dimensiooni ja käibemaksukoodi kombinatsiooni, luuakse iga kombinatsiooni kohta eraldi tööleherida.

Mahakandmiskanne luuakse kandevaluutas.
Ebapiisavate vahendite (NSF) maksete töötlemine  
--------------------------------------------

Saate töödelda NSF-makseid, klõpsates lehel Sissenõuded nuppu NSF-makse. Selle nupu klõpsamisel tühistatakse makse. Kui kliendile kehtib NSF-tasu, luuakse maksetöölehel tasukanne. Tasu summa põhineb automaatsete tasude seadistusel. Automaatsed tasud, mida kohaldatakse NSF-maksetele, on määratud tasude grupis, mis on valitud seotud pangakonto lehel Pangakontod.




