---
title: "Kasutuskogemuse isikupärastamine"
description: "Selles artiklid selgitatakse, kuidas rakendust Microsoft Dynamics 365 for Finance and Operations isikupärastada."
author: RobinARH
manager: AnnBe
ms.date: 08/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cf2ad9f95035aaf004f2da779a8492ff2d91d399
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="personalize-the-user-experience"></a>Kasutuskogemuse isikupärastamine

[!include[banner](../includes/banner.md)]


Selles artiklid selgitatakse, kuidas rakendust Microsoft Dynamics 365 for Finance and Operations isikupärastada.

Microsoft Dynamics 365 for Finance and Operationsis on mitut tüüpi isikupärastamisi. Mõned isikupärastamised on valikud, mille teete seadistuslehe suvandite loendis. Mõned isikupärastamised on varjatud, näiteks jälgib Finance and Operations ruudustike veergude laiusi, kui neid korrigeerite, ja kiirkaartide laiendatud/ahendatud olekut. Muud isikupärastamised on selgesõnalised. Selgesõnaliste isikupärastamiste puhul sisenete interaktiivsesse isikupärastamise režiimi ja muudate lehe välimust, hallates otse, kuidas elemendid lehel kuvatakse või kuidas need käituvad. 

Igat tüüpi isikupärastamised, mille kasutaja Finance and Operationsis teeb, on ainult sellele kasutajale ega olene ettevõttest, millega kasutaja suhtleb. Kasutaja lehele tehtud muudatused ei mõjuta süsteemi teisi kasutajaid.

## <a name="systemwide-options-for-the-current-user"></a>Süsteemiülesed suvandid praegusele kasutajale
Navigeerimisribal leiate hammasrattapildi, mida nimetatakse menüünupuks **Sätted**. Menüü **Sätted** avamisel kuvatakse mitu valikut. Suvandi **Sätted** valimine avab kasutaja lehe **Suvandid**. Sealt leiate neli suvandimenüüd. 

-   **Visuaalne:** kasutage värvikujunduse ja lehtede elementide vaikesuuruste valimiseks.
-   **Eelistused:** siin saate valida vaikeväärtused iga kord, kui avate rakenduse Finance and Operations, sh ettevõtte, esialgse lehe ja vaikevaate/redigeerimisrežiimi (mis määrab igal avamisel, kas leht on vaatamiseks lukus või redigeerimiseks avatud). Samuti leiate keele, ajavööndi ja kuupäeva, kellaaja ning numbrivormingute suvandid. Lisaks sisaldab see leht mitmesuguseid eelistusi, mis erinevat väljaanneti.
-   **Konto:** kasutage oma kasutaja ID ja muude kontoga seotud suvandite jaoks.
-   **Töövoog:** siin saate valida töövooga seotud suvandeid.

## <a name="implicit-personalizations"></a>Varjatud isikupärastamised
Varjatud isikupärastamised on need isikupärastamised, mida teete, suheldes teatud juhtnuppudega, mis jätavad oma praeguse nähtava oleku meelde. 

**Ruudustiku veerud:** saate korrigeerida veeru laiust loendis, valides veerupäisest vasakul või paremal oleva suuruse muutise riba ja libistades seda soovitud laiuse saavutamiseks vasakule või paremale. Finance and Operations talletab soovitud laiuse ja kuvab selle veeru selle laiusega iga kord, kui avate lehe selle loendiga. 

**Kiirkaardid:** mõnel lehel on laiendatavad jaotised, mida nimetatakse kiirkaartideks. Finance and Operations talletab, milliseid kiirkaarte olete laiendanud ja milliseid kiirkaarte ahendanud. Iga kord, kui lehele naasete, laiendatakse või ahendatakse neid samu kiirkaarte nende viimase kasutamise alusel. Selles artiklis selgitame, kuidas muuta kiirkaardi jaotiste järjekorda. Mõnel juhul võib kiirkaardi ahendamine jõudlust parandada, sest Finance and Operations ei pea selle kiirkaardi teavet tooma, kuni kiirkaarti ei laiendata. 

**Kiirinfo:** mõnel lehel on jaotis, mida nimetatakse kiirinfo paaniks. See paan sisaldab kirjutuskaitstud teavet, mis on seotud lehe praeguse teemaga. Igat kiirinfo paani jaotist nimetatakse kiirinfoks. Saate kiirinfot laiendada või ahendada ja Finance and Operations talletab teie eelistuse Mõnel juhul võib kiirinfo ahendamine jõudlust parandada, sest Finance and Operations ei pea kiirinfo teavet tooma, kuni kiirinfot ei laiendata.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Selgesõnalised isikupärastamised tööriistariba Isikupärastamine kasutades
Igal inimesel ja ettevõttel on erinev vaatenurk sellele, milline teave nende jaoks kõige olulisem on või millist teavet ei ole vaja sel moel ettevõtte juhtimisel. Võimalus kohandada seda, kuidas teave on järjestatud, kuid see suhtleb või kuidas see peidetud on, on võtmeküsimuseks Finance and Operationsi kasutamisel isikliku ja tootliku kogemuse saamiseks. 

Selged isikupärastamised on isikupärastamised, mille teete selgelt kavatsusega elemendi või lehe välimust või käitumist muuta, valides isikupärastamise menüü. Kõige põhilisem selge isikupärastamise tüüp on see, kui paremklõpsate elementi ja teete valiku **Isikupärastamine**. (Arvestage sellega, et mitte kõiki lehel olevaid elemente ei saa isikupärastada.) Kui valite selle isikupärastamise viisi, näete elemendi atribuudi akent. 

[![Elemendi atribuutide isikupärastamine](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Saate isikupärastada oma lehel oleva elemendi sel viisil, kui soovite lihtsalt muuta elemendi silti, peita elementi, et seda lehel ei kuvataks (see ei muuda andmeid, teile lihtsalt ei kuvata neid), lisada andmed kirikaardi kokkuvõtte ossa (kui element on kiirkaardil), jätta selle välja tabeldusklahviga vahele või teha nii, et andmeid ei saaks muuta, märkides need valikuga Ära muuda. 

Kui soovite elemente teisaldada või peita või teha mitu muudatust, saate kasutada tööriistariba Isikupärastamine, mis on saadaval elementide aknas Atribuut, kui valite suvandi **Vormi isikupärastamine**. Tööriistariba Isikupärastamine on saadaval ka vormi tegevuspaanil, vahekaardi **Suvandid** jaotises Isikupärastamisgrupp. Valige **Vormi isikupärastamine** ja näete tööriistariba Isikupärastamine. 

[![Isikupärastamise tööriistariba](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Isikupärastamise tööriistaribal on mitu isikupärastamistoimingut. Valige tööriist **Vali**, kui soovite valida ja muuta korraga mitme elemendi atribuute. Esmalt klõpsake tööriista Vali ja siis elementi, mille atribuute muuta soovite. Elemendi valimisel avaneb elemendi atribuutide aken ja saate muuta selle elemendi mis tahes atribuute. Saate protsessi vormi muude isikupärastatavate elementide jaoks korrata. Mõnel juhul valite elemendi ja näete, et mõned atribuudid ei ole muudetavad. See tähendab, et praeguse elemendi kasutamise alusel ei saa Finance and Operations lasta teil atribuuti muuta. Näiteks ei saa te peita nõutavat välja. 

Valige tööriist **Teisalda**, kui soovite valida ja teisaldada elementi erinevasse asukohta praeguses elementidegrupis. (Te ei saa teisaldada elementi selle emagrupist väljapoole). Esmalt klõpsake tööriista Teisalda ja siis elementi, mida teisaldada soovite. Kui klõpsate elementi, mida soovite teisaldada, skannib Finance and Operations vormi mõistmaks, kuhu seda elementi teisaldada saab, ja loob pukseerimistsoonide loetelu, mis osutab värvilise paksu reaga piirkondadele, kuhu saab elemendi pukseerida, kui lohistate elementi praeguses grupis. 

Valige tööriist **Peida**, elemendi valimiseks ja peitmiseks. Elemendi peitmiseks valige lihtsalt tööriist Peida ja klõpsake elementi, mida peita soovite. Kui valite tööriista Peida, muudetakse kõik praegu peidetud elemendid nähtavaks ja neid näidatakse varjutatud konteineris, nii et saate valida elemendi selle nähtavaks tegemiseks. Valige tööriist Vali nägemaks, kuidas leht valitud peidetud elementidega välja näeb. Valige tööriist **Kokkuvõte**, kui soovite, et numbrilist või stringivälja näidataks kiirkaardi kokkuvõtte alal. Tööriist Kokkuvõte rakendub ainult väljadele, mis sisalduvad kiirkaardi jaotises. Kui valite tööriista Kokkuvõte, näitab Finance and Operations kõiki välju, mis on valitud kokkuvõtte väljadena, sulgedes need varjutatud konteinerisse. Saate välju kiirkaardi kokkuvõttesse interaktiivselt lisada ja neid sealt eemaldada, klõpsates välja. 

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
Armatuurlaud on tihti esimene leht, mida näete Finance and Operationsi avamisel. Saate armatuurlauda isikupärastada nimetama ümber tööruumi navigeerimispaane, näitama ainult paane, mida näha soovite, paane pmber nimetama või korraldama paane eelistatud järjekorda. Armatuurlaya isikupärastamiseks valige mis tahes paan ja paremklõpsake kontekstimenüü avamiseks. Valige kontekstimenüüs suvand **Isikupärasta**. Kui valitud paan on see, mida soovite peita või ümbe nimetada või vahele jätta, saate teha selle muudatuse otse kuvatavas aknas Atribuut. Kui soovite paane ümber korraldada, siis valige aknas Atribuut suvand **Vormi isikupärastamine**, et avada tööriistariba Isikupärastamine. Seejärel saate kasutada paanide ümberkorraldamiseks tööriista Teisalda.

## <a name="administration-of-personalization"></a>Isikupärastamise haldamine
Pärast lehe isikupärastamist võite oma isikupärastamisi oma isikupärastatud lehe eksportimise teel teiste kasutajatega jagada. Seejärel võite paluda teistel kasutajatel isikupärastatud lehele minna ja importida teie loodud isikupärastamise fail.

Administraatori õigustega kasutaja saab lehel **Isikupärastamine** hallata ka teiste kasutajate isikupärastamisi. Sellel lehel on neli menüüd. 

- **Süsteem** – saate ajutiselt keelata või välja lülitada kõik süsteemi isikupärastamised. Sel juhul ei kustuta te isikupärastamisi. Selle asemel lähtestate lihtsalt kõik lehed vaikeolekusse. Kui hiljem isikupärastamise uuesti lubate, rakendatakse kõik isikupärastamised igale kasutaja lehele uuesti. Samuti saate kustutada kõikide kasutajate kõik isikupärastamised. Arvestage sellega, et kui kustutate isikupärastamisi, siis puudub võimalus isikupärastamiste automaatseks uuesti lubamiseks süsteemist. Seega veenduge enne seda sammu, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.
- **Kasutajad** – saate määrata, kas iga kasutaja saab teha varjatud või selget isikupärastamist. Samuti saate määrata, kas iga kasutaja saab teha konkreetsel lehel varjatud või selget isikupärastamist. Lõpuks saate importida või eksportida või kustutada iga kasutaja isikupärastamise.
- **Impordi** – saate importida vähemalt ühe kasutaja isikupärastamise. Seda vahekaarti kasutatakse pärast lehe või tööruumi isikupärastamist ja selle eksportimist isikupärastamise failina. Isikupärastamise faili importimiseks ja selle rakendamiseks vähemalt ühele kasutajale valige kõigi kasutajate loendist eraldi kasutajad või filtreerige konkreetse rolli järgi ja valige selles rollis olevad kasutajad. Kui olete valinud kasutajad, kes teie isikupärastamist kasutavad, klõpsake nuppu **Impordi** ja valige isikupärastamise fail. Isikupärastamine kinnitatakse ja rakendatakse valitud kasutajatele järgmisel korral, kui nad valitud lehe avavad.
- **Eemalda** – saate kustutada vähemalt ühe kasutaja lehe või tööruumi isikupärastamised. Valige kõigepealt leht või tööruum, mille isikupärastamised tuleks eemaldada. Seejärel valige kõigi kasutajate loendist eraldi kasutajad või filtreerige konkreetse rolli järgi ja valige siis selles rollis olevad kasutajad. Kui olete valinud nii lehe kui ka tööruumi ja kasutajad, klõpsake nuppu **Eemalda**. Kõik isikupärastamised, mille valitud kasutajad on valitud lehele või tööruumile rakendanud, eemaldatakse. Seda tegevust ei saa tagasi võtta. Kuid kui lehel või tööruumil on salvestatud isikupärastamine, saab selle isikupärastamise uuesti importida.

## <a name="personalization-of-inventory-dimensions"></a>Varude dimensioonide isikupärastamine.

Lehel varude dimensioonide häälestuse isikupärastamisel võtke arvesse suvandi **Kuva dimensiooni** abil loodud sätteid. Näiteks kui kasutate isikupärastamist partiinumbri varude dimensiooni veeru peitmiseks ja veerg kuvatakse lehe järgmisel avamisel uuesti, võib põhjuseks olla dimensioonikuva säte, mis määrab selle, milliseid varude dimensiooni veerge kuvatakse. 

Dimensiooni kuvasätted kehtivad kõigile lehtede ja need sätted alistavad eraldi lehtedel isikupärastatud varude dimensiooniväljade sätted. 

Partiinumbri varude dimensiooni näite puhul tuleks see dimensioon eemaldada suvandist **Dimensioonide kuvamine**, et tabelis seda veergu ei kuvataks. See muudatus kehtiks mitte ainult ühe kindla lehekülje, vaid kõikide lehekülgede puhul..

