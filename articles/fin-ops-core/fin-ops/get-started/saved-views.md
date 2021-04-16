---
title: Salvestatud vaated
description: Selles teemas kirjeldatakse, kuidas kasutada salvestatud vaadete funktsioone.
author: jasongre
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 25b59400cdd62f8728f03683d51c86c671edd9de
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744611"
---
# <a name="saved-views"></a>Salvestatud vaated

[!include [banner](../includes/banner.md)]


## <a name="introduction"></a>Sissejuhatus

Isikupärastamine on tähtis element, mis võimaldab kasutajatel ja organisatsioonidel optimeerida kasutuskogemust nende vajaduste kohaselt. Lisateavet isikupärastamise kohta vt teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

Tavapärane isikupärastamise võimaldab kasutajatel ühe lehekülje jaoks ainult ühte isikupärastamise kogumit kasutada. **Salvestatud vaated** funktsioon laiendab isikupärastamise võimalusi mitmel olulisel viisil.

- Vaated võimaldavad kasutajatel iga vormi puhul mitut isikupärastamise kogumit kasutada, mille vahel nad saavad vajaduse korral kiiresti vahetada. See võimaldab kasutajal luua lehe jaoks mitu optimeeritud vaadet, mis on kohandatud konkreetse äriülesande täitmise jaoks. 
- Kindlat tüüpi lehtede jaoks loodud vaated võivad sisaldada ka kasutaja lisatud filtreid või sortimisi, mis võimaldab kasutajatel kiiresti naasta tavaliselt filtreeritud andmekomplektide juurde. Lisateabe saamiseks vaadake jaotist [Millised lehed toetavad vaateid?](saved-views.md#what-pages-support-views). 
- Vaateid saab kasutajatele avaldada kindlates turberollides ja konkreetsetes juriidilistes isikutes. Seetõttu saab iga kasutaja, kel on määratletud roll ja juurdepääs konkreetsele juriidilisele isikule, juurdepääsu ja seda vaadet kasutada isegi, kui sellel kasutajal ei ole isikupärastamise õigusi. Selline avaldamise lahendus laseb organisatsioonidel määratleda ettevõtte standardvaateid, mis on nende äritegevuse jaoks optimeeritud. Lisateavet vt jaotisest [Isikupärastamise haldamine organisatsiooni tasemel vaadete kaudu](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Erinevalt tavapärasest isikupärastamisest ei salvestata vaateid automaatselt, kui kasutaja isikupärastab või loendit filtreerib. Selgesõnalised salvestamised on kohustuslikud, et anda kasutajatele paindlikkus vaate loomisel enne või pärast selle vaatega seotud muudatuste tegemist. See nõue tagab ka tahtmatu vaate definitsioonide muutmise filtrite või isikupärastamise tõttu, mis ei ole mõeldud pikaajaliseks kasutamiseks. Kaubad, mida süsteem automaatselt talletab tavapärase lehekülje kasutuse osana (nt veeru laiused või sektsioonide laiendatud või ahendatud olek), salvestatakse vaate kohta.
- Vaateid saab lisada tööruumidesse paanidena, loenditena või linkidena. Seega saab filtreeritud andmekogumit tööruumis vaadata ja kasutajad saavad paani või lingi abil seostada selle isikupärastamiskomplektiga, mis on selle andmekogumi jaoks asjakohane.

## <a name="switching-between-views"></a>Vaatelt vaatele lülitamine

Pärast seda, kui vaated on keskkonna jaoks saadaval, kasutab iga vaateid toetava lehe ülemine osa ahendatud vaate valimise juhtelementi, mis kuvab praeguse vaate nime.

Vaate valijal on kaks suurust. 

- **Suured vaate valijad** — lehtedel, millel on olulisel kohal loend, on mõne põhjuse tõttu suuremad vaate valijad. Kõige tähtsam põhjus on, et suurem vaate valija näitab lehti, kus vaade võib sisaldada kasutaja määratletud filtreid. Kuna filtrid on vaadetesse kaasatud, on suurem valija suurus samuti õigustatud, kuna vaate nimi on sageli ekraanil kuvatud andmete parim kirjeldus ja eeldatakse, et kasutajad kasutavad nende lehetüüpide puhul eri vaateid sagedamini.
- **Väikese vaate valijad** — kõigil muudel täisekraani lehekülgedel (välja arvatud tööruumid ja armatuurlaud) on väiksem vaatevalija, mis kuvatakse lehe pealdise kõrval. Nende lehtede vaated hõlmavad ainult isikupärastamisi ja mitte kasutaja määratletud filtreid. Nendel lehtedel on pealdis või kirje pealkiri sageli kõige olulisem teave lehe ülaosas. Vaate valija Väiksem suurus tähendab ka seda, et nendel lehtedel eeldatakse vähem eri vaadete vahel lülitamist. 
 
Kui valite vaate nime, avaneb vaate valija ja kuvatakse lehe jaoks saadaolevate vaadete loend.

- **Standardne vaade** — **Standardne** vaade on lehe algkuju vaade, millele pole rakendatud ühtegi isikupärastamist.
- **Isiklikud vaated** — tabalukkudeta vaated tähistavad teie isiklikke vaateid. Need on vaated, mille olete ise loonud või mille on teile andnud administraator.
- **Lukustatud vaated** — mõne vaate (nt **Standardne** vaade ja kõik teie rollile avaldatud vaated) kõrval on vaate valijas tabaluku sümbol. See sümbol näitab, et te ei saa neid vaateid redigeerida. Siiski salvestatakse automaatselt lehekülje kasutust peegeldavad muudatused. Need muudatused hõlmavad tabeli veeru laiuse muudatusi ja FastTab laiendatud või ahendatud olekule tehtud muudatusi. Sellegipoolest arvestage, et kui teil on isikupärastamise privileegid, saate tegevuse **Salvesta nimega** kaudu luua lukustatud vaate põhjal isikliku vaate.
- **Uued vaated** — avaldatud vaated, mida pole veel avatud, on tähistatud vaate nimest vasakul asuva tärniga.

Teisele vaatele lülitamiseks avage esmalt vaate valija ja seejärel valige vaade, mida soovite laadida. 

## <a name="creating-and-modifying-views"></a>Vaadete loomine ja muutmine

Erinevalt tavapärasest isikupärastamisest, vaateid ei salvestata automaatselt, kui kasutaja isikupärastab lehe või kui kasutaja rakendab loendile filtri või sordib seda. Nende muudatuste salvestamiseks vaate jaoks on vajalik selgesõnaline tegevus. See nõue annab kasutajatele paindlikkuse vaate loomisel enne või pärast selle vaatega seotud muudatuste tegemist. Sellega tagatakse ka, et ühekordsed filtrid või isikupärastamine ei muudaks definitsioone. Tavapärased lehekülje kasutused kaubad (nt veeru laiused või sektsioonide laiendatud või ahendatud olek), salvestatakse automaaselt praegusele vaatele (isegi lukustatud vaadetele).

Veendumaks, et vaate praegune olek oleks teada, kuvatakse praeguse vaate nime kõrval tärn (\*), kui hakkate vaadet isikupärastama või seda filtreerima. See sümbol näitab, et vaatate antud vaate salvestamata, muudetud versiooni.

Kui soovite neid muudatusi salvestada, toimige järgmiselt.

1. Valige vaate nimi, et avada vaate valija.
2. Olemasoleva vaate muutmiseks valige **Salvesta**. Pidage meeles, et toiming ei ole lukustatud vaadete jaoks saadaval. 
3. Uue vaate loomiseks tehke järgmist.

    1. Valige **Salvesta nimega**. 
    2. Sisestage vaate nimi ja (valikuliselt) kirjeldus.
    3. Valige käsk **Salvesta**.

## <a name="changing-the-default-view"></a>Vaikevaate muutmine

Vaikevaade on vaade, mida süsteem püüab avada, kui esimest korda lehte avate. Peaksite vaikevaate seadistama vaatele, mida eeldatavasti kõige rohkem kasutate. 

> [!NOTE]
> Ettevõtete vahel on üks globaalne vaikevaade. Vaikevaadet muutes avatakse see vaikimisi, sõltumata juriidilisest isikust, kellega seotud olete. 

Lehe vaikevaate muutmiseks tehke järgmist.

1. Lülitage vaatele, mida kasutate vaikimisi. 
2. Valige vaate nimi, et avada vaate valija. 
3. Klõpsake valikut **Veel** ja seejärel **Kinnita vaikevariandina**.

Teine võimalus on muuta uue vaate loomisel (kasutades tegevust **Salvesta nimega**) uus vaade vaikevaateks, kasutades enne vaate salvestamist suvandit **Kinnita vaikeväärtusena**.

Pange tähele, et mõnel juhul ei käivitu lehe esmakordsel avamisel vaikevaatega seostatud päring. Näiteks kui avate lehe läbi paani, jooksutatakse paani päring hoolimata vaikevaatega seostatud päringust. Lisaks, kui avate lehe, mille **Standardsel** vaatel on juba määratletud päring, jooksutatakse algne päring esimesena vaikevaate päringu asemel. Sellisel juhul kuvatakse vaate laadimisel teade. Kui vahetate vaateid pärast lehe laadimist, peaks vaate päringut saama ootuspäraselt käivitada. Versioonist 10.0.10 või hilisemast on teavitava sõnumiga kaasas manustatud tegevus, mis võimaldab laadida vaikevaate päringut otse.

## <a name="managing-personal-views"></a>Isiklike vaadete haldamine

Dialoogiboks **Halda mu vaateid** pakub teile isiklike vaadete ja vaate valijas olevate vaadete järjekorra põhilisi haldamisvõimalusi. Selle lehe avamiseks valige vaate nimi, et avada vaate valija rippmenüü, klõpsake valikut **Veel** ja seejärel käsku **Halda mu vaateid**.

Selle lehe jaoks saadaolevate vaadete loendi jaoks on olemas järgmised tegevused.

- **Vaikevaate muutmine** — kasutage tegevust **Kinnita vaikevariandina**, et muuta praegu valitud vaade selle lehe vaikevaateks.
- **Vaadete taasjärjestamine** — kasutage tegevusi **Nihuta üles** ja **Nihuta alla**, et korrastada oma vaated soovitud järjekorda.
- **Vaate ümbernimetamine** — kasutage tegevust **Nimeta ümber**, et muuta praegu valitud isikliku vaate nime. See tegevus on lukustatud vaadete puhul välja lülitatud. 
- **Vaate kustutamine** — kasutage tegevust **Kustuta**, et kustutada praegu valitud vaade lehelt jäädavalt. Pärast eemaldamist pole võimalik vaadet taastada.

Kõik selles dialoogiboksis tehtud muudatused jõustuvad pärast nupu **Salvesta** vajutamist.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Isikupärastamise haldamine organisatsiooni tasemel vaadete kaudu

Et aidata teil mõista, kuidas salvestatud vaated aitavad parandada isikupärastamise haldamist organisatsiooni tasemel, kirjeldatakse selles jaotises erinevusi isikupärastamise halduses koos ja ilma **Salvestatud vaadete** funktsioonita.

Ilma vaadeteta, rakendaksid administraatorid isikupärastamise sätteid lehe jaoks kasutajale või kasutajate rühmale Isikupärastamise lehe abil. Kui nendel kasutajatel olid olemas isikupärastamise õigused, rakendati need isikupärastamised sellele lehele. Siiski polnud võimalik takistada kasutajatel lehe edasist isikupärastamist, mis tähendas, et organisatsioon ei saanud kasutajatele kooskõlastatud kasutajaliidest tagada. Kui mõnel kasutajal ei olnud isikupärastamise õigusi, ei laaditud nende jaoks administraatori antud isikupärastamisi. Veelgi enam, kui organisatsiooni palgati uued kasutajad, pidid administraatorid isikupärastamiste kogumid kasutaja jaoks käsitsi laadima. Polnud automaatseid mehhanisme, mis täpsustaksid, et konkreetne isikupärastamise hulk peaks olema saadaval kasutajatele selles rollis.

**Salvestatud vaadete** funktsiooniga on isikupärastamise organisatsiooniline haldamine palju lihtsam peamiselt seetõttu, et vaateid saab avaldada kasutajate gruppidele. Pärast vaate avaldamist saavad kõik kasutajad, kellel on üks määratletud turberollidest ja juurdepääs ühele määratud juriidilistes isikutes, näha ja kasutada vaadet, kuigi sel kasutajal ei ole isikupärastamise õigusi. Kuigi igal kasutajal on avaldatud vaate koopia, milles on automaatselt rakendatud lehe kasutuse kaubad, ei saa ükski kasutaja salvestada avaldatud vaatesse isikupärastamist ega päringuvärskendusi. Teisisõnu on avaldatud vaated lukus. Lisaks, kui uutele kasutajatele määratakse rollid juriidilistes isikutes, kellele avaldati vaateid, näevad nad automaatselt oma rollidega ja juriidiliste isikutega seostatud vaateid. Administraatorilt ei nõuta täiendavat tegevust. Samuti, kui kasutajad muudavad organisatsioonis rolle või kui neile antakse juurdepääs teistele juriidilistele isikutele, ei pruugi nad enam neile varem avaldatud vaadetele juurde pääseda. Jällegi ei nõuta administraatorilt täiendavat tegevust.

Avaldatud vaate värskendusi saab kasutajatele hõlpsalt levitada, avaldades vaate vastavatele turberollidele ja juriidilistele isikutele uuesti.

Avaldamise lahendus võimaldab organisatsioonidel määratleda ettevõtte standardvaateid, mis on nende äritegevuse jaoks optimeeritud ning teatud turberollidega kasutajatele suunatud.

## <a name="publishing-views"></a>Vaadete avaldamine

Avaldamisprotsessi käigus saab vaateid määrata ühe või mitme juriidilise isiku ühe või mitme turberolli jaoks. Seetõttu saavad kõik kasutajad, kellel on juurdepääs juriidilisele isikule ja määratud üks nendest rollidest, pääseda juurde ja kasutada vaateid. Kasutaja ei saa vaateid redigeerida. Vaikimisi on süsteemiadministraatoritel juurdepääs vaate valija rippmenüüs olevale tegevusele **Avalda**. Siiski saab ka teistele teie organisatsiooni usaldusväärsetele kasutajatele anda vaadete avaldamisele juurdepääsu uue rolli **Salvestatud vaadete administraator** kaudu.

Vaate avaldamiseks tehke järgmist.

1. Looge ja salvestage isiklik koopia vaatest, mida soovite avaldada. 
2. Kui see vaade on laaditud, valige vaate nimi, et avada rippmenüüst vaate valija. 
3. Valige nupp **Veel** ja seejärel käsk **Avalda**. Avaneb dialoogiboks Avaldamine.
4. Sisestage vaate nimi. Sisestatud nimi on nimi, mida selle vaate saanud kasutajad näevad oma vaate valijates. Lehekülje avaldatud vaadete nimed peavad olema kordumatud. Korduvad nimed lubatud isegi juhul, kui rollide või juriidiliste isikute loendid, millele vaated on rakendatud, on erinevad.
5. **Uuendus 10.0.17 või hilisem:** kui funktsioon **(Eelversioon) Organisatsiooni vaadete tõlketugi** on sisse lülitatud, saate lisada oma vaate nime tõlked nii paljudes keeltes, kui teie organisatsioon vajab, valides nupu **Tõlked** välja **Nimi** kõrval. Sel juhul kuvatakse vaate nimi kasutajatele nende praeguses keeles. Saate määrata ka vaikekeele, et määratleda tõlge, mis kuvatakse näidatakse kasutajatele, kes kasutavad keeli, mille jaoks pole tõlget olemas.
5. Valikuline: sisestage vaate kirjeldus, et seda vaadet nägevad kasutajad mõistaks vaate eesmärki paremini. 
6. Määratlege, kas vaade tuleks valitud kasutajatele vaikevaatena avaldada. Vaate vaikimisi vaateks muutmine tähendab, et kasutajad näevad seda vaadet järgmine kord, kui nad sihtlehe avavad. Muudaetakse kõigi sihtkasutajate ühtset globaalset vaikevaadet. Kasutajad saavad endiselt muuta oma vaikevaadet pärast avaldamist.
7. Lisage turberollid, mis kehtivad kasutajatele, kellele see vaade mõeldud on. 
8. Määratlege, kas soovite avaldada vaate iga valitud turberolli alamrollile. Kui te seda teete, märkige ruut **Lisa alamrollid** vastava turberollide real. Võtke arvesse, et see märkeruut ei ole saadaval rollidel, millel pole alamrolle.
9. Lisage juriidilised isikud, kellele see vaade peaks kättesaadav olema. 
10. Valige **Avalda**.

Arvestage sellega, et teatud keskkondades võib aega kuluda (kuni tund), enne kui kasutajad avaldatud vaadet näevad.

> [!NOTE]
> Arvestage järgmiste ootustega, kui avaldate vaate juriidilisele isikule või kui avaldate vaate vaikevaateks.
> - Kui avaldate vaate vaikevaatena kõigile või mõnele juriidilisele isikule, muudate iga sihtkasutaja ühtset globaalset vaikevaadet. Kui kasutajal on rolle, kus vaikevaatena avaldatakse mitu vaadet, kasutatakse kasutaja vaikevaatena viimast avaldatud vaadet. 
> - Kui avaldate vaate juriidilisele isikule, kuid te ei avalda seda vaikevaatena, näevad kasutajad esialgu vaate valija vaadet (ainult määratud juriidiliste isikute puhul). Pärast vaate esmakordset laadimist on see alati kasutaja vastava lehe vaatevalijas sõltumata juriidilisest isikust. 

## <a name="modifying-a-published-view"></a>Avaldatud vaate muutmine

Pärast vaate avaldamist võite soovi korral seda muuta. Kuigi te ei saa avaldatud vaates muudatusi reaalajas teha, kuna nende vaadete redigeerimine on kõikide kasutajate (sh avaldajate) jaoks lukus, saate värskenduste tegemiseks vaate uuesti avaldada.

Kui muudatused, mida soovite avaldatud vaates teha, hõlmavad ainult avaldamise parameetreid (vaate nimi ja kirjeldus või turberollid, millele vaade avaldatakse), tehke järgmist.

1. Avage nende parameetrite avaldatud vaade, mida soovite värskendada. 
2. Valige vaate valija rippmenüüst käsk **Avalda uuesti**. Kui kasutate versiooni 10.0.12 või varasemat, peate olemasoleva vaate värskendamiseks valima käsud **Avalda** ja **Jah**.
3. Värskendage vaate nime, kirjeldust, turberolle ja juriidilisi isikuid. 
4. Valige **Avalda**. Kui valisite selle avaldatud vaate vaikevaatena, on see kasutajate vaikevaade pärast uuesti avaldamist. 

Kui avaldatud vaate muudatused hõlmavad vaatega seostatud isikupärastamiste või filtrite muudatusi, toimige järgmiselt.

1. Laadige avaldatud vaade, mida soovite muuta. 
2. Tehke kohaliku mustandi vajalikud muudatused.
3. Valige vaate valija rippmenüüst käsk **Avalda uuesti**.
4. Valige **Jah**, kui soovite vaadet koos salvestamata muudatustega avaldada. 
5. Korrigeerige muutmist vajavaid avaldamise parameetreid ja seejärel valige käsk **Avalda**. 

## <a name="managing-published-views"></a>Avaldatud vaadete haldamine

Nagu isiklike vaadete haldamise puhulgi, annab dialoogiboks **Halda mu vaateid** avaldamise privileegidega kasutajatele lehe avaldatud vaadete põhilised haldamisvõimalused (lisaks nende isiklikele vaadetele). Selle lehe avamiseks valige vaate nimi, et avada vaate valija rippmenüü, klõpsake valikut **Veel** ja seejärel käsku **Halda mu vaateid**.

Kuigi kõikidel kasutajatel on vahekaart **Minu vaated**, mis näitab nende isiklikke vaateid, on avaldamise privileegidega kasutajatel ka vahekaarti **Organisatsiooni vaated**, mis kuvab kõiki selle lehe jaoks avaldatud ja mitteavaldatud vaateid. Kuna vaateid võivad avaldada mitu kasutajat, on võimalus avaldatud vaadete täielikku loendit hallata oluline hoolimata sellest, kas olite kasutaja, kes tegelikult vaate avaldas.

Lehe kõikide avaldatud vaadete loendi jaoks on olemas järgmised tegevused. 

- **Avalda uuesti** — kasutage tegevust **Avalda uuesti**, et avaldada vaade uuesti pärast avaldamise parameetrite (nimi, kirjeldus, turberollid või juriidilised isikud) muutmist.
- **Avalda** — kasutage tegevust **Avalda** hetkel avaldamata vaate avaldamiseks. 
- **Tühista avaldamine** — kasutage tegevust **Tühista avaldamine**, et teha vaade passiivseks. Vaade on endiselt süsteemis saadaval, kuid kasutajad ei näe seda vaate valijas enne, kui vaade on uuesti avaldatud.
- **Salvesta isiklikuna** – kasutage tegevust **Salvesta isiklikuna** avaldatud vaatest isikliku mustandkoopia loomiseks. See võimalus aitab teil mõista teile avaldamata või veel avaldamata vaate sisu. Samuti saate seda kasutada vaate redigeerimiseks ja uuesti avaldamiseks.
- **Kustuta** – kasutage tegevust **Kustuta**, et avaldatud või avaldamata vaade jäädavalt kustutada. See tegevus eemaldab vaate kõikidelt süsteemis olevatelt kasutajatelt. Avaldatud vaadete eemaldamine jõustub pärast nupu **Salvesta** valimist. Pärast vaate kustutamist ei saa seda taastada. 

## <a name="managing-views-globally"></a>Vaadete globaalne haldamine

Kuigi vastavalt käesolevas teemas mainitule esitatakse mõned haldusvõimalused igal lehel, siis saavad **süsteemi administraatorid** ja **salvestatud süsteemi administraatorid** hallata vaateid ka terviklikumalt lehel **Isikupärastamine**. Lehel on eelkõige järgmised jaotised ja võimalused. 

- **Avaldatud vaated** – jaotises on loetletud kõik teie organisatsiooni jaoks avaldatud vaated. Siin saate pärast sihtkohti kuvavate turberollide või juriidiliste isikute muutmist vaate uuesti avaldada. Saate neid vaateid ka eksportida, kustutada või avaldamise tühistada. Saate vaatest isikliku koopia loomiseks kasutada tegevust **Salvesta isiklikuna**, et saaksite vaadet uuendada või saada selle sisust parema ülevaate. 
- **Avaldamata vaated** — selles jaotises loetletakse kõik teie süsteemi organisatsiooni vaated, mis pole praegu avaldatud. Need vaated tulevad enamasti süsteemi läbi impordi valiku. Saate neid vaateid avaldada, eksportida või kustutada. Versioonis 10.0.12 lisatud tegevus **Kiiravaldamine** võimaldab avaldada ühe tegevuse raames mitu antud jaotise vaadet, kasutades olemasolevaid turberolli ja juriidilise isiku konfiguratsioone. Saate nendest vaadetest isiklike koopiate loomiseks kasutada tegevust **Salvesta isiklikuna**, et saaksite nende sisust parema ülevaate.
- **Isiklikud vaated** – jaotises on loetletud kõik vaated, mis on loodud süsteemi kasutajate poolt. Siin saate avaldada organisatsioonile isikliku vaate või kopeerida ühe või mitu neist vaadetest teistele kasutajatele. Saate neid vaateid vajadusel ka eksportida või kustutada.
- **Kasutaja sätted** — valige kasutaja, kes saab vaadata või kohandada kasutaja võimalust kasutada isikupärastamist kas kogu süsteemis või kindlatel lehtedel, mida kasutaja on külastanud. Saate vaadata ja suhelda kasutaja süsteemi isikupärastatud osadega. Saate kustutada kõik selle kasutaja isikupärastatud osad või lähtestada kasutaja viiktekstid. Kui viikteksti funktsioon lähtestatakse, kõik hüpikaknad, mis juurutasid uusi funktsioone ja mida kasutajad on varem välja lülitanud, kuvatakse uuesti järgmisel korral, kui kasutaja nende funktsioonidega kokku puutub.
- **Süsteemi sätted** — saate ajutiselt välja lülitada süsteemis olevad kõigi kasutajate kõik isikupärastamised. Sel juhul ei rakendata ühtegi isikupärastamist ühtegi kasutaja jaoks ja kõik lehed lähtestatakse nende vaikeolekusse. Kui lülitate isikupärastamise hiljem uuesti sisse, rakendatakse kõik isikupärastamised uuesti. Saate ka kõigi kasutajate isikupärastamised süsteemist jäädavalt kustutada. Kustutatud isikupärastamisi ei ole võimalik taastada. Seega veenduge enne seda ülesannet, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.

Kasutajad, kellel on juurdepääs lehele **Isikupärastamine**, saavad tegumiriba nupu **Impordi vaated** abil ka isiklikke ja organisatsiooni vaateid importida. Organisatsiooni vaadete jaoks saate valida suvandi **Avalda kohe**, et teha vaated kasutajatele kättesaadavaks ilma täiendava selgesõnalise avaldamiseta.

## <a name="known-issues"></a>Teadaolevad probleemid
Salvestatud vaadetega teadaolevate probleemide loendi leiate jaotisest [Koostevormid, mis kasutavad täielikult salvestatud vaateid](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kuidas lubada salvestatud vaateid minu keskkonnas?

> [!NOTE]
> Funktsioon **Salvestatud vaated** nõuab, et rakenduses Finance and Operations oleks isikustamise süsteem lubatud. Kui kogu keskkonnale on isikupärastamine välja lülitatud, keelatakse vaated isegi siis, kui järgite alltoodud juhiseid. 

Saate funktsiooni **Salvestatud vaade** sisse ja välja lülitada mis tahes keskkonna funktsioonihalduses. Kui see on sisse lülitatud, on salvestatud vaated kõigil järgnevatel kasutajaseanssidele kättesaadavad.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Mis juhtub olemasolevate isikupärastamistega, kui vaated on lubatud? 

Kui vaated on lubatud, salvestatakse kõik kasutaja ja vormi olemasolevad isikupärastamised uude vaatesse nimega **Minu vaade**, mis määratakse automaatselt vaikevaateks. See aitab tagada, et kasutuskogemus oleks järjepidev enne ja pärast vaadete lubamist, välja arvatud vormidel kuvata vaate valija juhtelemendi puhul.

### <a name="what-pages-support-views"></a>Millised lehed toetavad vaateid? 

Vaated on saadaval enamiku, kuid mitte kõigi lehtede jaoks. Täpsemalt, vaated on praegu saadaval kõigi täisekraanlehtede jaoks, välja arvatud armatuurlaudade ja tööruumide jaoks. Lehed, mis pole täisekraanlehed, sh dialoogiboksid, rippmenüü dialoogid, otsingud, täiustatud eelvaated, ei toeta praegu vaateid. Vaadete toetust täiendavate lehetüüpide jaoks, näiteks tööruumide ja dialoogibokside jaoks, võidakse kaaluda tulevase värskenduse puhul.

### <a name="who-is-allowed-to-publish-views"></a>Kellel on lubatud vaateid avaldada?

Vaadete avaldamise õigus on ainult süsteemiadministraatoritel ja kasutajatel, kes on määratud rolli **Salvestatud vaadete administraator**. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Miks ma ei saa selle vaatega filtreid salvestada? 

On paar põhjust, miks tundub, et filtrit ei salvestata vaatega. 

- Leht ei pruugi toetada filtrite salvestamist vaate määratluse osana. Pange tähele, et ainult suurte vaate valijatega lehed lubavad isikupärastamiste ja päringu muudatuste salvestamist vaatena. Lisateavet vaadake jaotisest **Vaadete vahetamine**. 
- Kõnealune leht ei pruugi vaateid õigesti toetada, sest see võib ignoreerida vaata päringuid täielikult või toimida ajutises tabelis, mille andmed ei ole kinnistatud. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Millised andmed lehe külastamisel kuvatakse?

Väikeste vaate valijatega lehtedel (vaatamiseks saab salvestada ainult isikupärastamised) näete samu andmeid, mis on lehe külastamisel alati näha olnud. 

Suurte vaate valijatega lehtedel (vaatamiseks saab salvestada nii isikupärastamisi kui ka päringuid) näete tavaliselt andmeid, mis on ühendatud teie vaikevaatega seostatud päringuga. On kaks peamist erandit.

- Kui liigute paanilt lehele, käivitub paani päring hoolimata vaikevaatega seotud päringust. Kui lõite selle paani pärast vaadete lubamist, paani valimine avab lehe koos selle paaniga seostatud vaatega.
- Kui liigute lehele ja sisenemiskoht hõlmab päringut, käivitub algne päring esimesena vaikevaate päringu asemel. Kui selline olukord esineb, kuvatakse teile tavaliselt vaate laadimise ajal asjakohane teade. Samuti saate kinnitada, kui lülitate sellele vaatele pärast lehe laadimist, kuna see peaks sellegipoolest võimaldama vaate päringu käivitumise.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
