---
title: "Kasutuskogemuse isikupärastamine"
description: "See artikkel selgitab, kuidas Microsoft Dynamics 365 for Operationsit isikupärastada."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 734bf8a5cd71d218942e1a57fbb6af8fef4dc998
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="personalize-the-user-experience"></a>Kasutuskogemuse isikupärastamine

[!include[banner](../includes/banner.md)]


See artikkel selgitab, kuidas Microsoft Dynamics 365 for Operationsit isikupärastada.

Microsoft Dynamics 365 for Operationsis on mitut tüüpi isikupärastamisi. Mõned isikupärastamised on valikud, mille teete seadistuslehe suvandite loendis. Mõned isikupärastamised on varjatud, näiteks jälgib Dynamics 365 for Operations ruudustike veergude laiusi, kui neid korrigeerite, ja kiirkaartide laiendatud/ahendatud olekut. Muud isikupärastamised on selgesõnalised. Selgesõnaliste isikupärastamiste puhul sisenete interaktiivsesse isikupärastamise režiimi ja muudate lehe välimust, hallates otse, kuidas elemendid lehel kuvatakse või kuidas need käituvad. 

Igat tüüpi isikupärastamised, mille kasutaja rakenduses Dynamics 365 for Operations teeb, on ainult sellele kasutajale ega olene ettevõttest, millega kasutaja suhtleb. Kasutaja lehele tehtud muudatused ei mõjuta süsteemi teisi kasutajaid.

## <a name="systemwide-options-for-the-current-user"></a>Süsteemiülesed suvandid praegusele kasutajale
Navigeerimisribal leiate hammasrattapildi, mida nimetatakse menüünupuks **Sätted**. Menüü **Sätted** avamisel kuvatakse mitu valikut. Suvandi **Sätted** valimine avab kasutaja lehe **Suvandid**. Sealt leiate neli suvandite vahekaarti: **Visuaalne**, **Eelistused**, **Konto** ja **Töövoog**.

-   **Visuaalne:**kasutage värvikujunduse ja lehtede elementide vaikesuuruste valimiseks.
-   **Eelistused:** siin saate valida vaikeväärtused iga kord, kui avate rakenduse Dynamics 365 for Operations, sh ettevõtte, esialgse lehe ja vaikevaate/redigeerimisrežiimi (mis määrab igal avamisel, kas leht on vaatamiseks lukus või redigeerimiseks avatud). Samuti leiate keele, ajavööndi ja kuupäeva, kellaaja ning numbrivormingute suvandid. Lisaks sisaldab see leht mitmesuguseid eelistusi, mis erinevat väljaanneti.
-   **Konto:**kasutage oma kasutaja ID ja muude kontoga seotud suvandite jaoks.
-   **Töövoog:**siin saate valida töövooga seotud suvandeid.

## <a name="implicit-personalizations"></a>Varjatud isikupärastamised
Varjatud isikupärastamised on need isikupärastamised, mida teete, suheldes teatud juhtnuppudega, mis jätavad oma praeguse nähtava oleku meelde. 

**Ruudustiku veerud:** saate korrigeerida veeru laiust loendis, valides veerupäisest vasakul või paremal oleva suuruse muutise riba ja libistades seda soovitud laiuse saavutamiseks vasakule või paremale. Dynamics 365 for Operations talletab soovitud laiuse ja kuvab selle veeru selle laiusega iga kord, kui avate lehe selle loendiga. 

**Kiirkaardid:** mõnel lehel on laiendatavad jaotised, mida nimetatakse kiirkaartideks. Dynamics 365 for Operations talletab, milliseid kiirkaarte olete laiendanud ja milliseid kiirkaarte ahendanud. Iga kord, kui lehele naasete, laiendatakse või ahendatakse neid samu kiirkaarte nende viimase kasutamise alusel. Selles artiklis selgitame, kuidas muuta kiirkaardi jaotiste järjekorda. Mõnel juhul võib kiirkaardi ahendamine jõudlust parandada, sest Dynamics 365 for Operations ei pea selle kiirkaardi teavet tooma, kuni kiirkaarti ei laiendata. 

**Kiirinfo:** mõnel lehel on jaotis, mida nimetatakse kiirinfo paaniks. See paan sisaldab kirjutuskaitstud teavet, mis on seotud lehe praeguse teemaga. Igat kiirinfo paani jaotist nimetatakse kiirinfoks. Saate kiirinfot laiendada või ahendada ja Dynamics 365 for Operations talletab teie eelistuse Mõnel juhul võib kiirinfo ahendamine jõudlust parandada, sest Dynamics 365 for Operations ei pea kiirinfo teavet tooma, kuni kiirinfot ei laiendata.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Selgesõnalised isikupärastamised tööriistariba Isikupärastamine kasutades
Igal inimesel ja ettevõttel on erinev vaatenurk sellele, milline teave nende jaoks kõige olulisem on või millist teavet ei ole vaja sel moel ettevõtte juhtimisel. Võimalus kohandada seda, kuidas teave on järjestatud, kuid see suhtleb või kuidas see peidetud on, on võtmeküsimuseks Dynamics 365 for Operationsi kasutamisel isikliku ja tootliku kogemuse saamiseks. 

Selged isikupärastamised on isikupärastamised, mille teete selgelt kavatsusega elemendi või lehe välimust või käitumist muuta, valides isikupärastamise menüü. Kõige põhilisem selge isikupärastamise tüüp on see, kui paremklõpsate elementi ja teete valiku **Isikupärastamine**. (Arvestage sellega, et mitte kõiki lehel olevaid elemente ei saa isikupärastada.) Kui valite selle isikupärastamise viisi, näete elemendi atribuudi akent. 

[![Elemendi atribuutide isikupärastamine](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Saate isikupärastada oma lehel oleva elemendi sel viisil, kui soovite lihtsalt muuta elemendi silti, peita elementi, et seda lehel ei kuvataks (see ei muuda andmeid, teile lihtsalt ei kuvata neid), lisada andmed kirikaardi kokkuvõtte ossa (kui element on kiirkaardil), jätta selle välja tabeldusklahviga vahele või teha nii, et andmeid ei saaks muuta, märkides need valikuga Ära muuda. 

Kui soovite elemente teisaldada või peita või teha mitu muudatust, saate kasutada tööriistariba Isikupärastamine, mis on saadaval elementide aknas Atribuut, kui valite suvandi **Vormi isikupärastamine**. Tööriistariba Isikupärastamine on saadaval ka vormi tegevuspaanil, vahekaardi **Suvandid** jaotises Isikupärastamisgrupp. Valige suvand **Vormi isikupärastamine** ja näete tööriistariba Isikupärastamine. 

[![Isikupärastamise tööriistariba](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Isikupärastamise tööriistaribal on mitu isikupärastamistoimingut. Valige tööriist **Vali**, kui soovite valida ja muuta korraga mitme elemendi atribuute. Esmalt klõpsake tööriista Vali ja siis elementi, mille atribuute muuta soovite. Elemendi valimisel avaneb elemendi atribuutide aken ja saate muuta selle elemendi mis tahes atribuute. Saate protsessi vormi muude isikupärastatavate elementide jaoks korrata. Mõnel juhul valite elemendi ja näete, et mõned atribuudid ei ole muudetavad. See tähendab, et praeguse elemendi kasutamise alusel ei saa Dynamics 365 for Operations lasta teil atribuuti muuta. Näiteks ei saa te peita nõutavat välja. 

Valige tööriist **Teisalda**, kui soovite valida ja teisaldada elementi erinevasse asukohta praeguses elementidegrupis. (Te ei saa teisaldada elementi selle emagrupist väljapoole). Esmalt klõpsake tööriista Teisalda ja siis elementi, mida teisaldada soovite. Kui klõpsate elementi, mida soovite teisaldada, skannib Dynamics 365 for Operations vormi mõistmaks, kuhu seda elementi teisaldada saab, ja loob pukseerimistsoonide loetelu, mis osutab värvilise paksu reaga piirkondadele, kuhu saab elemendi pukseerida, kui lohistate elementi praeguses grupis. 

Valige tööriist **Peida**, elemendi valimiseks ja peitmiseks. Elemendi peitmiseks valige lihtsalt tööriist Peida ja klõpsake elementi, mida peita soovite. Kui valite tööriista Peida, muudetakse kõik praegu peidetud elemendid nähtavaks ja neid näidatakse varjutatud konteineris, nii et saate valida elemendi selle nähtavaks tegemiseks. Valige tööriist Vali nägemaks, kuidas leht valitud peidetud elementidega välja näeb. Valige tööriist **Kokkuvõte**, kui soovite, et numbrilist või stringivälja näidataks kiirkaardi kokkuvõtte alal. Tööriist Kokkuvõte rakendub ainult väljadele, mis sisalduvad kiirkaardi jaotises. Kui valite tööriista Kokkuvõte, näitab Dynamics 365 for Operations kõiki välju, mis on valitud kokkuvõtte väljadena, sulgedes need varjutatud konteinerisse. Saate välju kiirkaardi kokkuvõttesse interaktiivselt lisada ja neid sealt eemaldada, klõpsates välja. 

Valige tööriist **Jäta vahele**, et eemaldada element lehe klaviatuuri vahekaardi järjestusest. Kui valite tööriista Jäta vahele, näidatakse kõiki praegu vahele jäetud elemente varjutatud konteineris, nii et saate neid uuesti valida, et muuta need vahekaardi järjestuse osaks, valides vahele jäetud elemendi. 

Valige tööriist **Redigeeri**, kui soovite lisada elemendile märke Redigeeritav või Ei ole redigeeritav. Kui valite tööriista Redigeeri, näidatakse kõiki praegu mitteredigeeritavaid elemente varjutatud konteinetis, nii et saate neid valida, et muuta need redigeeritavaks. Arvestage sellega, et mõned väljad on nõutavad ja neid ei saa mitteredigeeritavateks muuta. Nende väljade kõrval kuvatakse tabalukuikoon. 

Valige tööriist **Lisa**, et lisada väli lehele. Tööriistaga Lisa ei saa te luua uut välja, kuid saate lisada välju, mis on osa praeguse lehe määratlusest, kuid mida lehel ei näidata. Kui valite tööriista Lisa, peate esmalt valima grupi või ala, kuhu soovite välja lisada. Dialoogikast kuvab teie valitud jaotisega seotud väljade loendi. Sellest dialoogikastist saate valida lisamiseks ühe või mitu välja ja klõpsata nuppu Lisa. Kui soovite hiljem varem lisatud välja eemaldada, korrake protsessi, kuid lihtsalt kustutage varem lisatud väli. 

Valige nupp **Halda**, et näha praeguse lehe kõikide isikupärastamistega seotud haldamissuvandite loendit. 

Valige suvand **Tühjenda** lehe lähtestamiseks vaikesätetele, installitud olekusse. Kõik praeguse lehe isikupärastamised kustutatakse. Tagasivõtmise toimingut ei ole, nii et kasutage seda suvandit ainult siis, kui olete kindel, et soovite lehe lähtestada. 

Valige suvand **Impordi**, et kasutada isikupärastamist isikupärastamise failist, mille teie või keegi teine on lehele varem loonud. Isikupärastamise importimine kustutab kogu lehel mis tahes isikupärastamised ja kasutab hoopis kõiki valitud faili isikupärastamisi. Kui soovite isikupärastamist salvestada või ühiskasutusse anda, valige suvand **Ekspordi**, et salvestada isikupärastamised faili. 

Valige nupp **Sulge**, et sulgeda tööriistariba ja viia leht uuesti selle eelmisesse interaktiivsesse olekusse. 

Tööriistaribaga Isikupärastamine on salvestamine varjatud. Teie isikupärastamised jõustuvad kohe, kui need teete, ja ei ole vaja klõpsata nuppu **Salvesta**. Mõnel juhul näete tööriista valimisel elemendi kõrval tabalukuikooni. See tähendab, et selleks, et leht toimiks õigesti, ei saa te muuta valitud tööriistaga seotud atribuute. Kui tööriistariba Isikupärastamine on avatud, muutub leht mitteinteraktiivseks. Te ei saa andmeid sisestada ega jaotisi laiendada või ahendada.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Selgesõnaline isikupärastamine: tööruumile paani või loendi lisamine
Mõnel loenditega lehel on toimingupaanil vahekaardi Suvandid jaotises Isikupärastamisgrupp saadaval täiendav isikupärastamise funktsioon. Valige suvand **Lisa tööruumi**, et avada ripploend, mis annab teile võimaluse näidatata praeguses loendis olevat teavet (filtreeritud ja sorditud või vaikimisi) tööruumis loendi või kokkuvõttepaanina (seda saab kasutada loendis olevate kaupade arvu näitamiseks). 

[![Lisa tööruumi](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Tööruumile loendi lisamiseks sortige või filtreerige esmalt loendi teavet, nagu soovite seda oma tööruumis näha, ja seejärel valige dialoog Lisa tööruumi. Järgmisena valige soovitud tööruum ja valige ripploendit Esitlus suvand **Loend**. Kui valite suvandi **Loend**, avaneb dialoog, mis võimaldab teil valida veerud, mida sooviksite loendis näha, ja loendi silt, nagu see tööruumis kuvatakse. 

Tööruumile paani lisamiseks filtreerige esmalt loendit, et esitada andmed, mida soovite kokku võtta (või millele soovite kiiret juurdepääsu). Seejärel avage rippdialoog Lisa tööruumi. Järgmisena valige soovitud tööruum ja valige ripploendist Esitlus suvand **Paan**. Kui valite suvandi **Paan**, avaneb dialoog, mis võimaldab teil lisada paani sildi ja otsuatada, kas paan näitab loendust. Tööruumi paigutatud paan võimaldab teil avada praegust lehte tööruumist ja näidata paaniga seotud teabe loendit. 

Kui loend või paan on tööruumi lisatud, saate selle tööruumi avada ja loendi või paani uuesti tellida grupist, kuhu see paigutatud oli.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Selgesõnaline isikupärastamine: kokkuvõtte lisamine tööruumist armatuurlauale
Mõned tööruumid sisaldavad arvpaane (paane, millel on numbrid), mida tahaksite näha ka oma armatuurlaual. Paremklõpsake tööruumis arvpaani ja valige suvand **Isikupärasta**. Valige suvand **Kinnita armatuurlauale**. Järgmine kord, kui navigeerite valitud armatuurlauale (ja värskendate seda), näete seda arvu selle tööruumi navigeerimispaani all armatuurlaual.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Selgesõnaline isikupärastamine: armatuurlaua isikupärastamine
Armatuurlaud on tihti esimene leht, mida näete Dynamics 365 for Operationsi avamisel. Saate armatuurlauda isikupärastada nimetama ümber tööruumi navigeerimispaane, näitama ainult paane, mida näha soovite, paane pmber nimetama või korraldama paane eelistatud järjekorda. Armatuurlaya isikupärastamiseks valige mis tahes paan ja paremklõpsake kontekstimenüü avamiseks. Valige kontekstimenüüs suvand **Isikupärasta**. Kui valitud paan on see, mida soovite peita või ümbe nimetada või vahele jätta, saate teha selle muudatuse otse kuvatavas aknas Atribuut. Kui soovite paane ümber korraldada, siis valige aknas Atribuut suvand **Vormi isikupärastamine**, et avada tööriistariba Isikupärastamine. Seejärel saate kasutada paanide ümberkorraldamiseks tööriista Teisalda.

## <a name="administration-of-personalization"></a>Isikupärastamise haldamine
On võimalik isikupärastada leht ja ühiskasutada seda teiste kasutajatega, eksportides lihtsalt isikupärastatud leht ja paludes teistel kasutajatel isikupärastatud lehele navigeerida ja importida loodud isikupärastatud fail. Kui kasutajal on administraatori privileegid, saab ta hallata ka teiste kasutajate isikupärastamisi lehel **Isikupärastamise seadistus**. Navigeerige lehele b. Lehel **Isikupärastamine** leiate kaks vahekaarti, üks on tähistatud sildiga **Süsteem** ja teine sildiga**Kasutajad**. 

**Süsteem:** siin saate ajutiselt keelata või välja lülitada kõik süsteemi isikupärastamised. See ei kustuta isikupärastamisi, vaid lähtestab kõik vormid nende vaikeolekusse. Hiljem saate isikupärastamise uuesti lubada, et kõik isikupärastamised igale kasutajate vormile uuesti rakendada. Samuti saate kustutada kõikide kasutajate kõik isikupärastamised. Arvestage sellega, et kui kustutate isikupärastamisi, siis puudub võimalus isikupärastamiste automaatseks uuesti lubamiseks süsteemist. Veendute, et olete eksportinud isikupärastamised, mida soovite võib-olla hiljem importida, enne kui selle toimingu teete. 

**Kasutajad:** siin saate iga kasutaja puhul otsustada, kas ta saab läbi viia selgesõnalist või varjatud isikupärastamist. Samuti saate otsustada, kas iga kasutaja saab läbi viia varjatud või selgesõnalist isikupärastamist kindlas vormis. Lõpuks saate importida või eksportida või kustutada iga kasutaja isikupärastamise. 

**Märkus.** Algses väljaandes võimaldab isikupärastamise haldus kasutaja haldamist ainult kasutaja alusel.




