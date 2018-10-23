---
title: "Laotöö juhtimine töömallide ja asukohadirektiividega"
description: "Selles teemas kirjeldatakse, kuidas kasutada töömalle ja asukohakorraldust määramaks, kuidas ja kus laos tööd tehakse."
author: perlynne
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4428613441424c81f4fd7dd92bbf842c62ce860
ms.openlocfilehash: 74e7c36fb912f35252d6e40d17477ac2962cbc23
ms.contentlocale: et-ee
ms.lasthandoff: 09/22/2018

---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Laotöö juhtimine töömallide ja asukohadirektiividega

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada töömalle ja asukohakorraldust määramaks, kuidas ja kus laos tööd tehakse.

Juhised, mille laotöötajad mobiilsesse seadmesse saavad, määravad töömallid, mille seadistate teenuses Microsoft Dynamics 365 for Finance and Operations, et määratleda erinevaid laoprotsesse ja ülesandeid. Töömallid määravad, kuidas igas laoprotsessis tööd tehakse. Linkides töömallidega asukohakorralduse, saate tagada, et töö toimub ladude kindlatel füüsilistel aladel.

## <a name="work-templates"></a>Töömallid
Leht **Töömallid** võimaldab teil määratleda tööüksuse toimingud, mida tuleb laos teha. Tavaliselt koosnevad lao tööüksuse toimingud paarist tegevusest: laotöötaja komplekteerib ühes kohas vaba kaubavaru ja viib komplekteeritud kaubavarud teise kohta. 

Töömallid koosnevad päisest ja seostatud ridadest. Iga töömall on kindlale *töö tellimuse tüübile*. Paljud töötellimuse tüübid on seotud lähtedokumentidega, nagu ostu- või müügitellimused. Kuid muud töötellimuse tüübid esindavad eraldiseisvaid laoprotsesse, nagu tsükliline inventuur. *Töökausta ID* võimaldab tööd gruppidesse korraldada. 

Töö päise määratluses olevaid sätteid saab kasutada selleks, et määrata, millal tuleb luua uus tööüksus. Näiteks saate määrata komplekteerimisridade maksimaalse arvu ja maksimaalse eeldatava komplekteerimisaja. Kui müügitellimuse komplekteerimisprotsessi töö ületab kummgi nendest väärtustest, jaotatakse see töö kaheks tööüksuseks. 

Tööread näitavad füüsilisi ülesandeid, mis on töö jätkamiseks nõutavad. Näiteks väljamineva laoprotsessi jaoks võib olla töörida kaupade komplekteerimise kohta laos ja teine rida nende kaupade panemise kohta koondusalale. Seal võib olla täiendav rida kaupade komplekteerimise kohta koondusalalt ja teine rida kaupade laadimisest autosse osana laadimisprotsessist. Saate määrata töömallide ridadele *korralduse koodi*. Korralduse kood lingitakse asukohakorraldusega ja see aitab seega tagada, et laotööd töödeldakse laos õiges kohas. 

Saate seadistada päringu, et juhtida, millal konkreetset töömalli kasutatakse. Näiteks saate määrata piirangu, nii et kindlat malli saab kasutada ainult kindlas laos töötamisel. Teise võimalusena võib teil olla mitu malli, mida kasutatakse töö loomiseks väljamineva müügitellimuse töötlemisel olenevalt müügi allikast. Süsteem kasutab välja **Seerianumber** saadaolevate töömallide hindamise järjekorra määramiseks. Seega kui teil on väga konkreetne päring kindla töömalli kohta, andke sellele väike järjekorranumber. Seda päringut hinnatakse siis muudest, üldisematest päringutest enne. 

Tööprotsessi lõpetamiseks või peatamiseks saate kasutada töörea sätet **Peata töö**. Sellisel juhul ei pea tööd tegev töötaja läbima järgmist töörea etappi. Järgmise etapi juurde liikumiseks peab see või mõni teine töötaja uuesti töö valima. Samuti saate erldada ülesanded tööüksuses, kasutades töömalliridadel erinevat *tööklassi ID-d*.

## <a name="location-directives"></a>Asukoha korraldus
Asukoha korraldused on reeglid, mis aitavad tuvastada komplekteerimise ja mahapanemise asukohti varude liigutamisel. Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kuhu komplekteeritud kaubad maha pannakse. Asukoha korraldus koosneb päisest ja seotud ridadest ning loote need lehel **Asukoha korraldus**. 

Päises peab iga asukoha korraldus olema seotud *töö tellimuse tüübiga*, mis määrab laokande tüübi, mille jaoks korraldust kasutatakse, nt müügitellimused, täiendamine või toormaterjalide komplekteerimine. *Töö tüüp* määrab, kas asukoha korraldust kasutatakse töö komplekteerimiseks või mahapanekuks või mõneks muuks laoprotsessiks, nagu inventuur või varude oleku muutmine. Peate määrama ka *koha* ja *lao*. Päises määratavat *korralduse koodi* saab kasutada asukoha korralduse linkimiseks ühe või mitme töömalliga. 

Töömallide puhul saate seadistada päringu, et määrata, millal kindlat asukoha korraldust kasutatakse. Näiteks saate määrata, et kui e-kaubandus on müügitellimuse allikas, tuleb varud komplekteerida lao spetsiaalsel alal. Süsteem kasutab välja **Seerianumber** saadaolevate asukohakorralduste hindamise järjekorra määramiseks. 

Asukohakorralduse read seavad asukoha leidmise reeglite rakendusele lisapiiranguid. Saate määrata minimaalse ja maksimaalse koguse, millele korraldus vastama peab, ja saate määrata, et korraldus on kindlale laoühikule. Näiteks kui mõõtühikuks on kaubaalused, saab määratud asukohta maha panna ainult kaubaalustel kaupu. Samuti saate määrata, kas kogust saab mitme asukoha vahel jagada. Nagu asukohakorralduse päisel, on ka asukohakorralduse real seerianumber, mis määrab ridade hindamise järjekorra. 

Asukohakorraldustel on veel üks üksikasjade tase: *asukohakorralduse toimingud*. Saate määratleda igale reale mitu asukoha korralduse tegevust. Järjekorranumbrit kasutatakse selleks, et määrata tegevuste järjekord. Sellel tasemel saate seadistada päringu määratlemaks, kuidas leida laos parim asukoht. Saate kasutada ka eelmääratletud sätteid **Strateegia**, et leida optimaalne asukoht.

## <a name="location-directives-configuration-details"></a>Asukohakorralduste konfiguratsiooni üksikasjad 

 ### <a name="sequence-number"></a>Järjekorranumber
 
See number on asukohakorralduse töötlemise järjestus valitud tellimuse tüübi puhul. Saate seda muuta, kasutades menüüvalikuid **Liiguta üles** ja **Liiguta alla**.
 
 ### <a name="work-type"></a>Töö tüüp
 
See on tehtava töö tüüp. Saadaoleva töö tüüp põhineb väljal **Töökäsu tüüp** valitud varude kande tüübil.
-   **Mahapanek** – töö tüüp **Mahapanek** tähendab, et asukohakorraldus otsib parimat asukohta süsteemi kas vastuvõtmisest, tootmisest või varude korrigeerimisest sissetulevate varude paigutamiseks või leidmiseks. Selle abil saab ka määratleda mahapaneku vaheasukohta või laadimisdokki lähetamisasukohta.
-   **Komplekteerimine** töö tüüp **Komplekteerimine** tähendab, et ladu otsib parimat asukohta, millest varud füüsiliselt reserveerida (töö luua). Komplekteerimise saab lõpule viia (komplekteerimise töörea võib sulgeda) isegi siis, kui töö pole lõpule viidud. Kasutaja saab lõpule viia füüsilise komplekteerimise, mis on komplekteerimisetapp. Seejärel saab kasutaja töö mobiilsest seadmest tühistada ja hiljem lõpule viia. Lõpliku mahapaneku lõpuleviimisel siiski töö päis suletakse. 
-   **Inventuur, Korrigeerimised, Kohandatud, Varude olekumuudatus, Litsentsiplaadi koostamine, Printimine, Oleku muutmine, Paki pesastatud litsentsiplaatidesse** – neid ei saa kasutada üheski asukohakorralduse seadistuses. See on loetelu, seega pole ükski filter seotud töökäsu tüübiga. 

### <a name="directive-code"></a>Korralduse kood

Valige korralduse kood töömalli või täiendusmalliga seostamiseks. Vormil **Korralduse kood** saate luua uusi koode, mida saab kasutada töömalli täiendamismalli ja asukohakorraldue vaheliste seoste loomisel. Selle abil saab luua ka seose mis tahes töömalli rea ja asukohakorralduse (nt laadimisdoki või vaheasukoha) vahel.

Pange tähele, et kui kood on määratud, ei otsi süsteem töö loomisel asukohakorraldust järjenumbri, vaid korralduse koodi järgi. See tähendab, et saate täpsemalt määrata, millises asukohas malli teatud töömalli etapi, nt materjalide ajastamine, puhul kasutatakse. 

### <a name="site"></a>Sait

Tegevuskoht on kohustuslik väli, kuna asukohakorraldus vajab kehtivat tegevuskohta ja ladu. 

### <a name="warehouse"></a>Ladu

Ladu on kohustuslik väli, kuna asukohakorraldus vajab kehtivat tegevuskohta ja ladu.

### <a name="multiple-sku"></a>Mitu SKU-d

See võimaldab asukohas mitut varude arvestusühikut (SKU), nt laadimisdokk. Kui valite suvandi **Mitu SKU-d**, määratakse mahapaneku asukoht töös (mida eeldatakse), kuid see suudab käsitleda ainult mitme kauba mahapanekut (kui töö sisaldab erinevaid komplekteeritavaid ja mahapandavaid SKU-sid, mitte ühe SKU mahapanekut). Kui te suvandit **Mitu SKU-d** ei vali, määratakse mahapaneku asukoht ainult siis kui mahapanekul on ainult üht tüüpi SKU-d. Mõlema toimingu kasutamiseks peate määrama kaks rida, üks olekuga Mitu SKU-d sees ja teine olekuga Mitu SKU-d väljas. Neil peab olema sama struktuur ja seadistus. Mahapanekutoimingute puhul peavad teil olema identsed asukohakorraldused, isegi kui te töö ID-s üht ja mitut SKU-d ei erista. Samuti peate seadistama komplekteerimise, kui teil on tellimus rohkem kui ühe kaubaga.

### <a name="sequence-number"></a>Järjekorranumber

Sisestage asukohakorralduse rea töötlemise järjestus valitud töötüübi puhul. Järjestust saate vajaduse korral ka muuta, kasutades käske **Liiguta üles** ja **Liiguta alla**.

### <a name="fromto-quantity"></a>Alates kogusest / kuni koguseni

See võimaldab määrata kogusevahemiku, mille puhul tuleb valida ruudustiku keskosa seeria. Saate määrata kogusevahemiku vastavas ühikus.

### <a name="unit"></a>Üksus

Saate määrata minimaalse ja maksimaalse koguse, millele korraldus vastama peab, ja saate määrata, et korraldus on kindlale laoühikule. Rea ühikuvälja kasutatakse ainult koguse hindamiseks.

Asukohakorralduse rea kohaldatavuse kontrollimisel põhineb see kogusel, mille ühik on määratud asukohakorralduse real. Iga kord, kui asukohakorralduse rida luuakse, püüab süsteem teisendada nõudluse ühiku real määratud ühikusse. Kui mõõtühiku teisendust pole olemas, jätkatakse järgmise reaga. 

### <a name="locate-quantity"></a>Koguse asukoha määramine

Seda suvandit kasutatakse ainult koguse mahapanekuks/leidmiseks laos. See on ainult mahapaneku töötüübi jaoks. Kehtivad väärtused on järgmised.

-   **Litsentsiplaadi kogus** – hindamisel, kas kogus on vahemikus Alates ja Kuni, kasutage kogust vastuvõetaval litsentsiplaadil.
-   **Ühikuna määratud kogus** – hindamisel, kas kogus on vahemikus Alates ja Kuni, kasutage konkreetse kande ajal ühikuna määratavat kogust.
-   **Jääkkogus** – hindamisel, kas kogus on vahemikus Alates ja Kuni, kasutage kogust, mis jääb parasjagu sisseregistreeritava ostutellimuse real vastuvõtmiseks järelejäävat kogust.
-   **Eeldatav kogus** – hindamisel, kas kogus on vahemikus Alates ja Kuni, kasutage ostutellimuse rea kogukogust olenemata sellest, mis on juba vastu võetud.

### <a name="restrict-by-unit"></a>Piira ühiku alusel

See võimaldab asukohakorralduse rea teha ühele või mitmele mõõtühikule kohaseks. Kui soovite koguse reserveerimisel reserveerida kaubaaluseid ainult kindlatest asukohtadest, piirab ruudustiku keskosa seeria selle konkreetse seeria valikuga PL, nii et ükski kaubaalusest väiksem kogus seeriat ei vali. Valige ühikute seadistamiseks suvand **Piira ühiku alusel**. Saate piirata rea ka rohkem kui ühe ühikuga. See toimib ainult komplekteerimistüüpi asukohakorraldustega. 

### <a name="round-up-to-unit"></a>Ümarda ühikuni

Väli toimib koos väljaga **Piira ühikuga**. Kui asukohakorralduse rea **Piira ühikuga** sätteks on seatud Kast, siis suvandi **Ümarda ühikuni** valimimne näitab, et toormaterjali komplekteerimise korralduse põhjal loodud töö tuleb ümaradada mitme käsitlemisühiku kordseni (määratud väljal **Piira ühikuga**). Pange tähele, et see toimib ainult toormaterjali komplekteerimise puhul ja ainult koos komplekteerimistüüpi asukohakorraldusega.

### <a name="locate-packing-qty"></a>Pakkimiskoguse leidmine

Kui müügitellimusel, üleviimistellimusel või tootmistellimusel on määratud pakkimiskogus, valib süsteem ainult asukohad, milles on pakkimiskogus olemas. See toimib ainult komplekteerimistüüpi asukohakorraldustega.

### <a name="allow-split"></a>Luba tükeldamine

See määrab, kas asukohakorraldusel on lubatud vastuvõetav kogus või mitmes laoasukohas reserveeritav kogus tükeldada või kas tö loomiseks tuleb kogu kogus leida ühest asukohast või reserveerida ühest asukohast. 

### <a name="sequence-number"></a>Järjekorranumber

See number on asukohakorralduse töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust muuta. Siiski olge järjekorranumbrite kasutamisel ettevaatlik, kuna töötlemine toimub alati järjest. 

### <a name="name"></a>Nimi

Saate sisestada asukohakorralduse toimingu nime. Olge nime määramisel täpne.

### <a name="fixed-location-usage"></a>Fikseeritud asukoha kasutamine 

-   **Fikseeritud ja fikseerimata asukohad** – asukohakorraldus kaalub kõiki asukohti.
-   **Ainult toote fikseeritud asukohad** – asukohakorraldus kaalub ainult toodete fikseeritud asukohti.
-   **Ainult tootevariandi fikseeritud asukohad** – asukohakorraldus kaalub ainult tootevariantide fikseeritud asukohti.

### <a name="allow-negative-inventory"></a>Luba negatiivne laovaru

Selle suvandi valimisel lubatakse asukohakorraldustes määratud laoasukohas negatiivsed varud. 

### <a name="batch-enabled"></a>Partii on lubatud 

Selle suvandi valimisel kasutatakse partiiloaga kaupade puhul partiistrateegiaid. Kui jõutakse reani, kus suvand **Partii on lubatud** on määratud koos mittepartiikaubaga, jätkub töötlus järgmise toimingureaga. 

### <a name="strategy"></a>Strateegia

-   **Konsolideeri** – seda strateegiat kasutatakse kaupade konsolideerimiseks kindlas asukohas, kui sarnased kaubad on juba saadaval. See toimib ainult mahapanekutüüpi asukohakorraldusega. Mahapaneku üldine seadistus määrab konsolideerimise esimesel toimingureal ja seejärel püütakse teisel maha panna ilma konsolideerimata. Kaupade konsolideerimine muudab hilisema komplekteerimise tõhusamaks.
-   **Vastenda pakkimiskogus** – selle strateegia abil kontrollitakse, kas komplekteerimisasukohas on määratud pakkimiskogus olemas. See toimib ainult komplekteerimistüüpi asukohakorraldusega. 
-   **FEFO partii reserveerimine** – seda strateegiat kasutatakse siis, kui varud leitakse partii aegumiskuupäeva abil ja eraldatakse partii reserveerimiseks. Seda strateegiat saate kasutada ainult partiiloaga kaupade puhul. See toimib ainult komplekteerimistüüpi asukohakorraldusega. 
-   **Täieliku LP-ni ümardamine** – seda strateegiat kasutatakse varude koguse ümardamiseks, et see vastaks litsentsiplaadi (LP) kogusele, mis on määratud komplekteeritavatele kaupadele. Saate seda strateegiat kasutada ainult komplekteerimistüüpi asukohakorralduse täiendamistüübi puhul. 
-   **Tühi asukoht ilma sissetuleva tööta** – seda strateegiat kasutatakse tühjade asukohtade leidmiseks. Asukoht loetakse tühjaks, kui sel ei ole füüsilist laoseisu ja eeldatavat sissetulevat tööd. Seda strateegiat kasutatakse ainult mahapanekutüüpi asukohakorralduse puhul. 

### <a name="example-of-the-use-of-location-directives"></a>Asukoha korralduste kasutamise näide

Selle näite puhul kaaluge ostutellimuse protsessi, kus asukohakorraldus peab leidma laos äsja vastuvõtudokis registreeritud laokaupade jaoks vaba ruumi. Esiteks peate leidma vaba ruumi laos, konsolideerides olemasoleva vaba kaubavaruga. Kui konsolideerimine ei ole võimalik, peate leidma tühja asukoha. 

Selle stsenaariumi puhul peate määratlema kaks asukohakorralduse toimingut. Esimene tegevus järjekorras peab kasutama strateegiat **Konsolideeri** ja teine strateegiat **Tühi asukoht sissetuleva tööta**. Kui te ei määratle kolmandat toimingut ületäitmisstsenaariumi käsitlemiseks, on võimalikud kaks tulemust, kui laos ei ole enam ruumi: töö saab luua isegi siis, kui asukohti ei määratleta, või töö loomise protsess võib nurjuda. Tulemuse määrab lehe **Asukoha korralduse tõrked** seadistus, kus saate otsustada, kas valida suvand **Peata töö asukoha korralduse tõrke korral** igale töö tellimuse tüübile.

