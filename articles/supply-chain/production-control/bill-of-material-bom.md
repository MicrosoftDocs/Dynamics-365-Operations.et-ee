---
title: Kooslused ja valemid
description: See teema annab teavet koosluste ja valemite kohta, mis on toodete ja tootevariantide määratlemise keskne osa.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5a24136c9fad3f1de68158cbd14a60b0ebd147b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211694"
---
# <a name="bills-of-materials-and-formulas"></a>Kooslused ja valemid

[!include [banner](../includes/banner.md)]

See teema annab teavet koosluste ja valemite kohta, mis on toodete ja tootevariantide määratlemise keskne osa. Kooslused ja valemid määravad kindla toote jaoks nõutavad materjalid või koostisosad. Valemid määravad ka kindla tootmise kontekstis vastuvõetavad kaastooted ja kõrvalsaadused. 

<a name="bills-of-materials"></a>Kooslused
------------------

Kooslus (BOM) määratleb komponendid, mida on toote tootmiseks vaja. Komponendid võivad olla toormaterjalid, pooltooted või koostisosad. Mõnel juhul võidakse koosluses viidata ka teenustele. Kuid tavaliselt kirjeldavad kooslused vajalikke *materjaliressursse*.  

Kui kooslus on kombineeritud protsessi või tootmisvooga, mis kirjeldab toote koostamiseks vajalikke toiminguid ja ressursse, moodustab see aluse toote eeldatava omahinna arvutamiseks.  

Kooslus on üksik üksus, mida kirjeldatakse järgmise teabega.

-   Koosluse ID
-   Koosluse nimi
-   Koosluse read, mis kirjeldavad komponente ja koostisosi
-   Koosluse versioonid, mis määratlevad toote ja perioodi, mille jaoks kooslust saab kasutada

Üksik kooslus kirjeldab ühte taset, mida tähistatakse kordumatu ID-ga. Komponentidel võivad olla oma kooslused, millele viidatakse koosluse versioonidega. Konkreetse toote täielik koosluste hierarhia saab kuvada ja seda redigeerida koosluse koostajas.

### <a name="formulas-co-products-and-by-products"></a>Valemid, kaastooted ja kõrvalsaadused

Valemid on koosluse alamtüüp, mida kasutatakse tavaliselt tootmisprotsessis. Lisaks komponentidele ja koostisosadele kirjeldab valem kaastooteid ja kõrvalsaadusi. Tegelikus versioonis nõuab kaastoodete ja kõrvalsaaduste määratlus valemiversiooni. Valem määratletakse tavaliselt ühe konkreetse valmis toote kohta (valemi- või plaanimiskaup), mis on valemiversioonis määratletud.

### <a name="boms-in-the-product-lifecycle"></a>Kooslused toote elutsüklis

Toote elutsüklis võidakse luua mitmesugustel põhjustel palju kooslusetüüpe.

-   **Koosluse mustand** – see kooslus annab esialgse prognoosi vajalike materjalide kohta varases kavandamise faasis ja aitab hinnata umbkaudu kulusid ning eeldatavaid toote atribuute. Seda kooslust ei kasutata tavaliselt ettevõtte ressursiplaanimises (ERP-s).
-   **Tehniline kooslus** – seda kooslust kasutatakse tavaliselt olemasolevatel tooteportfellidel põhinevate toodete kavandamisel. Tehnilised kooslused on struktureeritud kavandamisprotsessi hõlbustamiseks ja grupeerivad keerukad tooted tehnilistesse moodulitesse. Lihtsate toodete puhul võib olla võimalik kasutada tehnilisi kooslusi tegelikus tootmisprotsessis. Kuid muude toodete puhul tuleb tehniline kooslus teisendada tegelikuks tootmiskoosluseks. Tehnilised kooslused on koosluste hierarhias tähistatud tavaliselt fiktiivse kooslusena. Kuigi tehnilisi kooslusi saab kasutada tootmisoperatsioonide plaanimiseks ja läbiviimiseks, võib see lähenemine olla ebaotstarbekas, eriti korduvate toimingute puhul, kui luuakse palju tellimusi.
-   **Plaanimiskooslus** – seda kooslust kasutatakse materjalivajaduse plaanimiseks. Komponentide ja koostisosade nõudlus arvutatakse valmistoodete nõudluse põhjal. Nagu kuluarvestuse koosluste puhul, võivad plaanimiskooslused kajastada konkreetset materjalisegu, mida teatud perioodil kasutatakse.
-   **Tootmiskooslus** – see on tegelik kooslus, mida kasutatakse konkreetse tootmise jaoks. Tootmiskooslus peab võtma arvesse tegelikke ressursse, mida toote valmistamiseks kasutatakse. Tootmistellimuse, partiitellimuse või kanbani loomisel ahendatakse mitu koosluste taset, mida kajastavad fiktiivsed kooslused, ühele tasemele ja jaotatakse tellimuse toimingute vahel.
-   **Kuluarvestuse kooslus** – seda kooslust kasutatakse toote eeldatava omahinna arvutamiseks. Näiteks saab kuluarvestuse kooslust kasutada siis, kui kasutatakse standardkulu või arvutatakse antud toote eeldatav plaanitud omahind. Kuluarvestuse kooslused võivad viidata konkreetsele materjalide ja ressursside segule, mida eeldatavasti kasutatakse. Seetõttu saab kuluarvestuse kooslust kasutada eeldatava omahinna näidisväärtuse loomiseks perioodi kohta ja selleks, et aidata vältida hälbeid aja jooksul.

Juurutuses tegelikult kasutatavad koosluste tüübid olenevad rakendusest ning ka äristsenaariumidest ja nõuetest. Lihtsates rakendustes saab plaanimise kooslust, tootmise kooslust ja kuluarvestuse kooslust modelleerida ühe kooslusena. Keskkondades, kus tehnilist lahendust sageli muudetakse ja kus on palju alternatiivseid protsesse, on tõenäoliselt vaja suuremat kooslusetüüpide kogumit.

### <a name="approval-of-boms-and-formulas"></a>Koosluste ja valemite kinnitamine

Iga koosluse ja valemi saab eraldi kinnitada või sellelt kinnituse eemaldada. Tavaliselt kinnitatakse kooslus või valem siis, kui kinnitatakse esimene asjakohane koosluse versioon. Kuid mõne äristsenaariumi puhul võivad need kinnitamised olla protsessis erinevad etapid ja võivad hõlmata erinevaid protsessiomanikke.  

Pange tähele, et kui kooslus on kinnitamata, on kinnitamata ka kõik seotud koosluseversioonid.

## <a name="bom-and-formula-versions"></a>Koosluse ja valemi versioonid
Kindla koosluse või valemi seostamiseks tootevariandiga, mida saab toota, peate looma koosluse versiooni või valemiversiooni. Koosluseversioonid ja valemiversioonid võivad olla piiratud perioodi, koguse, laoala, konkreetsete tootedimensioonide ja muude kriteeriumidega. Valemiversioonidel on täiendavad olulised atribuudid nagu tulu, kaastoote ja kõrvalsaaduse määratlused ja valemi kulujaotuse juhised.

### <a name="approval-of-bom-and-formula-versions"></a>Koosluse ja valemiversioonide kinnitamine

Enne, kui koosluse versiooni plaanimises või tootmisprotsessis kasutada saab, tuleb see kinnitada. Kui koosluse versioon on kinnitatud, saab kinnitada ka seotud koosluse, olenevalt kasutaja valikust ja autentimise õigustest. Arvestage, et koosluse versiooni saab kinnitada ainult juhul, kui seotud kooslus ise on kinnitatud.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Vaikekoosluse või valemiversiooni aktiveerimine

Kindla koosluse või valemi määramiseks koosluse vaikeversiooniks või valemiversiooniks, mida kasutatakse koondplaneerimises või tootmistellimuste loomiseks, tuleb versioon aktiveerida. Kui versioon aktiveeritakse, kontrollitakse versiooni kordumatust antud piirangute (nt periood, laoala või kogus) suhtes. Saate tõrketeate, kui versioon, mida püüate aktiveerida, satub konflikti juba aktiivse versiooniga. Siis tuleb konflikti põhjustav versioon inaktiveerida või muuta versiooni piiranguid (tavaliselt perioodi), et vältida mitmetähenduslikku aktiveerimist.

### <a name="product-change-with-case-management"></a>Toote muutmine juhtumihaldusega

Toote muutmise juhtum uute või muudetud koosluste ja koosluseversioonide kinnitamiseks ja aktiveerimiseks annab lihtsa võimaluse koosluse versiooni piirangute ülevaate kuvamiseks. Saate kinnitada ja aktiveerida ka kõiki kooslusi ja valemeid, mis on ühel aktiveerimiskuupäeval konkreetse muudatusega seotud.

### <a name="alternative-bom-versions"></a>Alternatiivsed koosluseversioonid

Mõnikord ei tohiks aktiivset koosluse või valemi versiooni prognoosides, müügis või põhitoodetes kasutada. Sellisel juhul saab valida konkreetse kinnitatud koosluse nõude (prognoosi rea, müügirea või koosluse rea) osana, kui alternatiivse koosluse või valemi puhul on olemas kinnitatud koosluse või valemi versioon.  

Plaanitud tellimuste, tootmistellimuste või kanbanide loomisel saab planeerija või tööde järelevaataja kasutada igasugust kinnitatud koosluse versiooni, mis vajalikul plaanitud tootmiskuupäeval kehtib, konkreetse toote plaanimiseks või tootmiseks. Kasutatavat koosluse versiooni pole vaja koosluse vaikeversioonina aktiveerida.

## <a name="bom-and-formula-lines"></a>Koosluse ja valemi read
Koosluse rida luuakse iga materjali, teenuse või koostisosa jaoks. Rida määratleb nimetatud tootevariandi plaanitud tarbimise ja mitmesugused plaanitud tarbimisega seotud atribuudid.  

Koosluse ridade tüübid võivad olla järgmised. **Kaup**, **Fiktiivne**, **Kinnistatud tarne**, **Hankija**.

### <a name="item"></a>Kaup

Valge rea tüüp **Kaup** materjalide või teenuste puhul, mida tarbitakse otse ja mis ei nõua edasist koosnevusarvutust ega kinnistatud tarnet.

### <a name="phantom"></a>Fiktiivne

Valige rea tüüp **Fiktiivne**, kui soovite kooslusereal olevaid madalama tasemega kooslusekaupu jaotada. Koondplaneerimises, plaanitud kuluarvutuses või sellise tootmistellimuse prognoosimisel, mis kasutab koosluse ridu tüübiga **Fiktiivne**, asendatakse peamine koosluse rida, mis viitab fiktiivse kooslusega tootevariandile, selle koosluse ridadel nimetatud komponentkaupadega, nagu määratleb selle tootevariandi kehtiv aktiivne koosluse versioon. Kui tootevariandil on kehtiv aktiivne protsess, ühendatakse selle protsessi toimingud ühte põhiprotsessi.  

Arvestage, et fiktiivseid üksusi kasutatakse tavaliselt tehnilise protsessi lihtsustamiseks. Fiktiivsete koosluste rohke kasutamine paljudel tasemetel avaldab mõju jõudlusele, eriti väga paljude kordustega tootmisstsenaariumide puhul. Jõudluse parandamiseks peaksite vältima sügavaid fiktiivsete koosluste hierarhiaid. Kasutage selle asemel eelnevalt jaotatud tootmise kooslusi ja protsesse.

### <a name="pegged-supply"></a>Kinnistatud tarne

Valige rea tüüp**Kinnistatud tarne**, kui soovite luua alamtootmist, koosluse rea sündmuse kanbani või mõne tootevariandi otsest ostutellimust, millele koosluse rida viitab. Alamtootmine, sündmuse kanban või ostutellimus luuakse tootmistellimuse prognoosimisel. Tarbiva tootmistellimuse jaoks reserveeritakse automaatselt vajalikud kaubakogused.

### <a name="vendor"></a>Hankija

Valige rea tüüp **Hankija**, kui tootmisprotsess kasutab allhankijat ja kui soovite allhankija jaoks alamtootmise või ostutellimuse automaatselt luua.  

**Märkus alltöövõtu toimingute kohta koosluses:** teenus või töö, mida teeb allhankija, tuleb luua teenuseüksusena, mida varudes jälgitakse. Teenuseüksus tuleb siduda põhikaubaga koosluse reana. Protsess peab sisaldama allhankija operatsiooniressursile määratud operatsiooni.



