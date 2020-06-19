---
title: Salvestatud vaated
description: Selles teemas kirjeldatakse, kuidas kasutada salvestatud vaadete funktsioone.
author: jasongre
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: f6b7f1c64c273f52dc1d414185ba54efdfb8e5c0
ms.sourcegitcommit: dc67232c9aa3223d42f22cc1f7aafbd121e7e616
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/30/2020
ms.locfileid: "3412327"
---
# <a name="saved-views"></a>Salvestatud vaated

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Sissejuhatus
Isikupärastamine on tähtis element, mis võimaldab kasutajatel ja organisatsioonidel optimeerida kasutuskogemust nende vajaduste kohaselt. Lisateavet isikupärastamise kohta vt teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

Tavapärase isikupärastamise puhul said kasutajad ühe vormi jaoks ainult ühte isikupärastamise kogumit kasutada. Salvestatud vaated laiendavad isikupärastamise võimalusi mitmel olulisel viisil.

-    Vaated võimaldavad kasutajatel iga vormi puhul mitut isikupärastamise kogumit kasutada, mille vahel nad saavad vajaduse korral kiiresti vahetada. See võimaldab kasutajal luua lehe jaoks mitu optimeeritud vaadet, mis on kohandatud konkreetse äriülesande täitmise jaoks. 

-    Kindlat tüüpi lehtede jaoks loodud vaated võivad sisaldada ka kasutaja lisatud filtreid või sortimisi, mis võimaldab kasutajatel kiiresti naasta tavaliselt filtreeritud andmekomplektide juurde. Lisateabe saamiseks vaadake jaotist [Millised lehed toetavad vaateid?](saved-views.md#what-pages-support-views). 

-    Vaateid saab kasutajatele avaldada kindlates turberollides ja konkreetsetes juriidilistes isikutes. Seetõttu saab iga kasutaja, kel on määratletud roll ja juurdepääs konkreetsele juriidilisele isikule, juurdepääsu ja seda vaadet kasutada, kuigi see kasutaja ei pruugi saada seda isikupärastada. Selline avaldamise lahendus laseb organisatsioonidel määratleda ettevõtte standardvaateid, mis on nende äritegevuse jaoks optimeeritud. Lisateavet vt jaotisest [Isikupärastamise haldamine organisatsiooni tasemel vaadete kaudu](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Erinevalt tavapärasest isikupärastamisest ei salvestata vaateid automaatselt, kui kasutaja sõneselgelt isikupärastab või loendit filtreerib. Käsitsi salvestamine on vajalik, et tagada paindlikkus vaate loomisel enne või pärast vaatega seotud muudatuste tegemist ja et tagada, et vaate määratlust ei muudeta kogemata filtrite või isikupärastamistega, mis pole pikaajaliseks kasutuseks mõeldud.  

-    Vaateid saab lisada tööruumidesse paanidena, loenditena või linkidena. Seega saab filtreeritud andmekogumit tööruumis vaadata ja kasutajad saavad paani või lingi abil seostada selle isikupärastamiskomplektiga, mis on selle andmekogumi jaoks asjakohane.

## <a name="switching-between-views"></a>Vaatelt vaatele lülitamine
Pärast seda, kui vaated on keskkonna jaoks lubatud, kasutab iga vaateid toetav leht praeguse vaate nime näitava vormi ülaosas ahendatud vaate valimise juhtelementi.  

Vaate valijal on kaks suurust. 

-   **Suured vaate valijad**: lehtedel, millel on olulisel kohal loend, on mõne põhjuse tõttu suuremad vaate valijad. Kõige tähtsam põhjus on, et suurem vaate valija näitab lehti, kus vaade võib sisaldada kasutaja määratletud filtreid. Kuna filtrid on vaadetesse kaasatud, on suurem valija suurus samuti õigustatud, kuna vaate nimi on sageli ekraanil kuvatud andmete parim kirjeldus ja eeldatakse, et kasutajad kasutavad nende lehetüüpide puhul eri vaateid sagedamini.  
 
-   **Väikese vaate valijad**: Kõigil muudel täislehe vormidel (välja arvatud tööruumid ja armatuurlaud) on väiksem vaatevalija, mis kuvatakse lehe pealdise kõrval. Nende lehtede vaated hõlmavad ainult isikupärastamisi (ja mitte kasutaja määratletud filtreid). Nendel lehtedel on vormi pealdis või kirje pealkiri sageli kõige olulisem teave vormi ülaosas. Väiksem suurus tähendab ka seda, et nendel lehtedel eeldatakse vähem eri vaadete vahel lülitamist. 
 
Kui klõpsate vaate nime, avaneb vaate valija ja kuvatakse selle lehe jaoks saadaolevate vaadete loend.

-    **Standardvaade**: vaade **Standardne** (varem vaade **Klassikaline**) on lehe valmisvaade, kus ei rakendata ühtki otsest isikupärastamist.
-    **Isiklikud vaated**: tabalukkudeta vaated tähistavad teie isiklikke vaateid. Need on vaated, mille olete ise loonud või mille on teile andnud administraator.  
-    **Lukustatud vaated**: mõne vaate (nt **Standardne** vaade ja kõik teie rollile avaldatud vaated) kõrval on vaate valijas tabaluku sümbol. See sümbol näitab, et te ei saa neid vaateid redigeerida. Siiski salvestatakse automaatselt lehekülje kasutust peegeldavad kaudsed isikupärastused. Need kaudsed isikupärastused hõlmavad ruudustiku veerulaiuse muutmist või kiirkaardi laiendamist või ahendamist. Sellegipoolest arvestage, et kui teil on isikupärastamise privileegid, saate tegevuse **Salvesta nimega** kaudu luua lukustatud vaate põhjal isikliku vaate.
-    **Uued vaated**: avaldatud vaated, mida pole veel avatud, on tähistatud vaate nimest vasakul asuva tärniga.  

Teisele vaatele lülitamiseks avage esmalt vaate valija ja seejärel valige vaade, mida soovite laadida. 

## <a name="creating-and-modifying-views"></a>Vaadete loomine ja muutmine
Erinevalt tavapärasest isikupärastamisest ei salvestata vaateid automaatselt, kui kasutaja sõneselgelt isikupärastab (või loendit filtreerib). Nende muudatuste salvestamiseks vaate jaoks on vajalik selgesõnaline tegevus. See tagab kasutajale paindlikkuse vaate loomisel enne või pärast vaatega seotud muudatuste tegemist ja tagab, et vaate määratlust ei muudeta kogemata ühekordsete filtrite või isikupärastamistega. Pange tähele, et varjatud isikupärastamised (näiteks kiirkaardi laiendamine või ahendamine või ruudustiku veeru laiuse muutmine) salvestatakse praeguse vaate jaoks automaatselt, isegi lukustatud vaadete puhul. 

Tagamaks, et vaate praegune olek oleks teada, kui alustate vaate muutmist sõnaselge isikupärastamise või filtreerimisega, kuvatakse praeguse vaate nime kõrval tärn, mis tähistab, et vaatate vaate salvestamata muudetud versiooni.

Kui soovite neid muudatusi salvestada, toimige järgmiselt.
1.  Valige vaate nimi, et avada vaate valija.
2.  Olemasoleva vaate muutmiseks tehke järgmist.
     1. Valige käsk **Salvesta**. Pange tähele, et see tegevus pole lukustatud vaadete puhul lubatud. 
3.  Uue vaate loomiseks tehke järgmist.
     1.    Valige **Salvesta nimega**. 
     2.    Sisestage vaate nimi ja (valikuliselt) kirjeldus.
     3.    Valige käsk **Salvesta**.

## <a name="changing-the-default-view"></a>Vaikevaate muutmine
Vaikevaade on vaade, mida süsteem püüab avada, kui esimest korda lehele liigute. Peaksite selle seadistama vaatele, mida eeldatavasti kõige rohkem kasutate.  

Lehe vaikevaate muutmiseks tehke järgmist. 
1.  Lülitage vaatele, mida kasutate vaikimisi. 
2.  Valige vaate nimi, et avada vaate valija. 
3.  Klõpsake valikut **Veel** ja seejärel **Kinnita vaikevariandina**.  

Teine võimalus on muuta uue vaate loomisel (kasutades tegevust **Salvesta nimega**) uus vaade vaikevaateks, kasutades enne vaate salvestamist suvandit **Kinnita vaikeväärtusena**.

Pange tähele, et mõnel juhul ei käivitu lehele esimest korda liikumisel vaikevaatega seostatud päring. Näiteks kui liigute läbi paani lehele, käivitatakse paani päring hoolimata vaikevaatega seostatud päringust. Samuti, kui liigute lehele, mille standardsel vaatel on juba määratletud päring, käivitub algne päring esimesena vaikevaate päringu asemel. Kui see juhtub, kuvatakse teile vaate laadimise ajal asjakohane teade. Vaate vahetamine pärast seda, kui leht on lõpetanud laadimise, peaks võimaldama vaate päringu ootuspärase käivitumise. Alates versioonist 10.0.10 Platform Update 34, on teavitava sõnumiga kaasas manustatud tegevus, mis võimaldab laadida vaikevaate päringut otse.

## <a name="managing-personal-views"></a>Isiklike vaadete haldamine 
Dialoogiboks **Halda mu vaateid** pakub teile isiklike vaadete ja vaate valijas olevate vaadete järjekorra põhilisi haldamisvõimalusi. Selle lehe avamiseks klõpsake vaate nime, et avada vaate valija rippmenüü, klõpsake valikut **Veel**ja seejärel käsku **Halda mu vaateid**.  

Selle lehe jaoks saadaolevate vaadete loendi jaoks on olemas järgmised tegevused.  
-    **Vaikevaate muutmine**: kasutage tegevust **Kinnita vaikevariandina**, et muuta praegu esiletõstetud vaade selle lehe vaikevaateks.  
-    **Vaadete taasjärjestamine**: kasutage tegevusi **Nihuta üles** ja **Nihuta alla**, et korrastada oma vaated soovitud järjekorda.  
-    **Vaate ümbernimetamine**: kasutage tegevust **Nimeta ümber**, et muuta praegu esiletõstetud isikliku vaate nime. See tegevus on lukustatud vaadete puhul välja lülitatud. 
-    **Vaate kustutamine**: kasutage tegevust **Eemalda**, et kustutada praegu esiletõstetud vaade lehelt jäädavalt. Pärast eemaldamist pole võimalik vaadet taastada.  

Kõik selles dialoogiboksis tehtud muudatused jõustuvad pärast nupu **Salvesta** vajutamist.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Isikupärastamise haldamine organisatsiooni tasemel vaadete kaudu
Et aidata teil mõista, kuidas salvestatud vaated aitavad parandada isikupärastamise haldamist organisatsiooni tasemel, kirjeldatakse selles jaotises erinevusi isikupärastamise halduses koos ja ilma salvestatud vaadete funktsioonita.

Ilma vaadeteta, rakendaksid administraatorid isikupärastamise sätteid lehe jaoks kasutajale või kasutajate rühmale Isikupärastamise lehe abil. Kui nendel kasutajatel olid olemas isikupärastamise õigused, rakendati need isikupärastamised sellele lehele. Siiski polnud võimalik takistada kasutajatel lehe edasist isikupärastamist, mis tähendas, et organisatsioon ei saanud kasutajatele kooskõlastatud kasutajaliidest tagada. Kui mõnel kasutajal ei olnud isikupärastamise õigusi, ei laaditud nende jaoks administraatori antud isikupärastamisi. Veelgi enam, kui organisatsiooni palgati uued kasutajad, pidid administraatorid isikupärastamiste kogumid kasutaja jaoks käsitsi laadima. Polnud automaatseid mehhanisme, mis täpsustaksid, et konkreetne isikupärastamise hulk peaks olema saadaval kasutajatele selles rollis.

Salvestatud vaadete funktsiooniga on isikupärastamise organisatsiooniline haldamine märkimisväärselt lihtsam peamiselt seetõttu, et vaateid saab avaldada kasutajate gruppidele. Pärast vaate avaldamist saavad kõik kasutajad, kellel on üks määratletud turberollidest ja juurdepääs ühele määratud juriidilistes isikutes, näha ja kasutada vaadet, kuigi see kasutaja ei pruugi saada seda isikupärastada. Kuigi igal kasutajal on avaldatud vaate koopia, milles on automaatselt rakendatud lehe kasutus (varjatud isikupärastamine), ei saa ükski kasutaja salvestada avaldatud vaatesse otsest isikupärastamist ega päringuvärskendusi. Teisisõnu on avaldatud vaated lukus. Lisaks, kui uutele kasutajatele antakse rollid juriidilistes isikutes, kellele avaldati vaateid, näevad nad automaatselt oma rollidega ja juriidiliste isikutega seostatud vaateid. Administraatorilt täiendavat tegevust ei nõuta. Samuti, kui kasutajad muudavad organisatsioonis rolle või kui neile antakse juurdepääs teistele juriidilistele isikutele, ei pruugi nad enam neile varem avaldatud vaadetele juurde pääseda. Jällegi ei nõuta administraatorilt täiendavat tegevust.

Avaldatud vaate värskendusi saab kasutajatele hõlpsalt levitada, avaldades vaate vastavatele turberollidele ja juriidilistele isikutele uuesti.

Avaldamise lahendus võimaldab organisatsioonidel määratleda ettevõtte standardvaateid, mis on nende äritegevuse jaoks optimeeritud ning teatud turberollidega kasutajatele suunatud.  

## <a name="publishing-views"></a>Vaadete avaldamine
Avaldamisprotsessi käigus saab vaateid määrata ühe või mitme juriidilise isiku ühe või mitme turberolli jaoks. Seetõttu saavad kõik kasutajad, kellel on juurdepääs juriidilisele isikule ja kellele on määratud üks nendest rollidest, pääseda juurde ja kasutada vaateid, kuigi nad ei saa neid redigeerida. Süsteemiadministraatoritel on juurdepääs vaate valija rippmenüüs olevale tegevusele **Avalda**. Siiski saab ka teistele teie organisatsiooni usaldusväärsetele kasutajatele anda vaadete avaldamisele juurdepääsu uue rolli **Salvestatud vaadete administraator** kaudu.

Vaate avaldamiseks tehke järgmist. 
1.  Looge ja salvestage isiklik koopia vaatest, mida soovite avaldada. 
2.  Kui see vaade on laaditud, valige vaate nimi, et avada rippmenüüst vaate valija. 
3.  Valige nupp **Veel** ja seejärel käsk **Avalda**. Avaneb dialoogiboks Avaldamine.  
4.  Sisestage vaate nimi ja (valikuliselt) kirjeldus. Sisestatud nimi on nimi, mida selle vaate saanud kasutajad näevad oma vaate valijates. Lehekülje avaldatud vaadete nimed peavad olema kordumatud. Korduvad nimed lubatud isegi juhul, kui rollide või juriidiliste isikute loendid, millele vaated on rakendatud, on erinevad.
5.  Lisage turberollid, mis kehtivad kasutajatele, kellele see vaade mõeldud on.
6. Lisage juriidilised isikud, kellele see vaade peaks kättesaadav olema. 
7. [10.0.9 / Platform Update 33 või uuem] Määratlege, kas vaade tuleks valitud kasutajatele vaikevaatena avaldada. Vaate vaikimisi kuvamine tähendab, et kasutajad näevad seda vaadet järgmine kord, kui nad sihtlehe avavad. See muudab nende kasutajate vaikevaadet. Kasutajad saavad siiski pärast avaldamise toimumist oma vaikevaadet muuta.    
8.  Valige **Avalda**.

Arvestage sellega, et teatud keskkondades võib aega kuluda (kuni tund), enne kui kasutajad avaldatud vaadet näevad.

## <a name="modifying-a-published-view"></a>Avaldatud vaate muutmine
Mõnikord võite pärast vaate avaldamist avastada, et soovite avaldatud vaates muudatusi teha. Kuigi te ei saa avaldatud vaates muudatusi reaalajas teha, kuna nende vaadete redigeerimine on kõikide kasutajate (sh avaldajate) jaoks lukus, saate värskenduste tegemiseks vaate uuesti avaldada.  

Kui muudatused, mida soovite avaldatud vaates teha, hõlmavad ainult avaldamise parameetreid (vaate nimi ja kirjeldus või turberollid, millele vaade avaldatakse), tehke järgmist. 
1.  Avage nende parameetrite avaldatud vaade, mida soovite värskendada. 
2.  Valige vaate valija rippmenüüst käsk **Avalda**. 
3.  Valige nupp **Jah**, kui soovite olemasolevat vaadet värskendada (või **Ei**, kui soovite seda avaldada teise nimega).
4.  Värskendage vaate nime, kirjeldust ja/või turberolle. 
5.  Valige **Avalda**. 
6.  [10.0.8 / Platform Update 32 või varasem] Kui olete avaldatud vaate nime värskendanud, peate veel kustutama vana nimega avaldatud vaate (lisateabe saamiseks vaadake teemat **Avaldatud vaadete haldamine**). 
7. [10.0.9 / Platform Update 33 või uuem] Kui algselt valisite selle avaldatud vaate vaikevaateks, on see taas nende kasutajate vaikevaade pärast uuesti avaldamist.  

Kui avaldatud vaate muudatused hõlmavad vaatega seostatud isikupärastamiste või filtrite muutmist, toimige järgmiselt. 
1.  Laadige avaldatud vaade, mida soovite muuta. 
2.  Salvestage avaldatud vaate koopia, et luua avaldatud vaate kohalik mustand. 
3.  Muutke kohalikku mustandit vajaduse kohaselt.
4.  Avaldage vaade esialgse nimega. 

## <a name="managing-published-views"></a>Avaldatud vaadete haldamine
Nagu isiklike vaadete haldamise puhulgi, annab dialoogiboks **Halda mu vaateid** avaldamise privileegidega kasutajatele lehe avaldatud vaadete põhilised haldamisvõimalused (lisaks nende isiklikele vaadetele). Selle lehe avamiseks valige vaate nimi, et avada vaate valija rippmenüü, klõpsake valikut **Veel**ja seejärel käsku **Halda mu vaateid**.

Kuigi kõik kasutajad näevad vahekaarti **Minu vaated**, mis näitab nende isiklikke vaateid, näevad avaldamise privileegidega kasutajad ka vahekaarti **Avaldatud**, mis kuvab kõiki selle lehe jaoks avaldatud vaateid. Kuna vaateid võivad avaldada mitu kasutajat, on võimalus avaldatud vaadete täielikku loendit hallata oluline hoolimata sellest, kas olite kasutaja, kes tegelikult vaate avaldas.

Lehe kõikide avaldatud vaadete loendi jaoks on olemas järgmised tegevused. 

-    **Avalda** – kasutage tegevust **Avalda**, et avaldada vaade uuesti pärast avaldamise parameetrite (nimi, kirjeldus, turberollid või juriidilised isikud) muutmist.
-    **Salvesta isiklikuna** – kasutage tegevust **Salvesta isiklikuna** avaldatud vaatest isikliku mustandkoopia loomiseks. See võimalus aitab teil mõista teile avaldamata või veel avaldamata vaate sisu. Samuti saate seda kasutada vaate redigeerimiseks ja uuesti avaldamiseks. See võimalus lisati versioonis 10.0.12.  
-    **Eemalda** – kasutage tegevust **Eemalda**, et avaldatud vaade jäädavalt kustutada. See tegevus eemaldab vaate kõikidelt süsteemis olevatelt kasutajatelt. Avaldatud vaadete eemaldamine jõustub pärast nupu **Salvesta** valimist.

## <a name="managing-views-globally"></a>Vaadete globaalne haldamine
Kuigi vastavalt käesolevas teemas mainitule esitatakse mõned haldusvõimalused igal lehel, siis saavad **süsteemi administraatorid** ja **salvestatud süsteemi administraatorid** hallata vaateid ka terviklikumalt lehel **Isikupärastamine**. Lehel on eelkõige järgmised jaotised ja võimalused. 

- **Avaldatud vaated** – jaotises on loetletud kõik teie organisatsiooni jaoks avaldatud vaated. Siin saate pärast sihtkohti kuvavate turberollide või juriidiliste isikute muutmist vaate uuesti avaldada. Saate eksportida või kustutada ka ühe või mitu avaldatud vaadet. Versioonis 10.0.12 ja hilisemates versioonides saate vaatest isikliku koopia loomiseks kasutada tegevust **Salvesta isiklikuna**, et saaksite vaadet uuendada või saada selle sisust parema ülevaate. 
- **Avaldamata vaated** – jaotises on loetletud kõik vaated, mis on imporditud teie süsteemi, kuid pole veel avaldatud. Saate neid vaateid avaldada, eksportida või kustutada. Versioonis 10.0.12 lisatud tegevus **Kiiravaldamine** võimaldab avaldada ühe tegevuse raames mitu antud jaotise vaadet, kasutades olemasolevaid turberolli ja juriidilise isiku konfiguratsioone. Versioonis 10.0.12 ja hilisemates versioonides saate nendest vaadetest isiklike koopiate loomiseks kasutada tegevust **Salvesta isiklikuna**, et saaksite nende sisust parema ülevaate.   
- **Isiklikud vaated** – jaotises on loetletud kõik vaated, mis on loodud süsteemi kasutajate poolt. Siin saate avaldada organisatsioonile isikliku vaate või kopeerida ühe või mitu neist vaadetest teistele kasutajatele. Saate neid vaateid vajadusel ka eksportida või kustutada.
- **Kasutajad** – saate valida kasutaja, et kuvada loend lehtedest, mida kasutaja on külastanud. Seejärel saate muuta valitud kasutaja võimalust kasutada isikupärastamist kindlatel lehtedel või terves süsteemis. Samuti saate kasutaja jaoks isikupärastamise importida, eksportida või eemaldada. Lisaks saate lähtestada kasutaja funktsiooni viiktekstid. Seejärel, kui kasutaja on varem välja lülitanud kõik hüpikaknad, mis juurutasid uusi funktsioone, kuvatakse need hüpikaknad uuesti järgmisel korral, kui kasutaja nende funktsioonidega kokku puutub.
- **Süsteem** – saate ajutiselt välja lülitada süsteemis olevad kõigi kasutajate kõik isikupärastamised. Sel juhul kustutatakse kõik isikupärastamised kõigi kasutajate jaoks ja kõik lehed lähtestatakse nende vaikeolekusse. Kui lülitate isikupärastamise hiljem uuesti sisse, rakendatakse kõik isikupärastamised uuesti. Saate ka kõigi kasutajate isikupärastamised süsteemist jäädavalt kustutada. Kustutatud isikupärastamisi ei ole võimalik taastada. Seega veenduge enne seda ülesannet, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.

Kasutajad, kellel on juurdepääs lehele **Isikupärastamine**, saavad tegumiriba nupu **Impordi vaated** abil ka isiklikke ja mallivaateid importida. Versioonis 10.0.12 ja hilisemates versioonides on lisatud mehhanism vaadete koheseks avaldamiseks nende importimisel.  

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kuidas lubada salvestatud vaateid minu keskkonnas? 
> [!NOTE]
> Funktsioon **Salvestatud vaated** nõuab, et rakenduses Finance and Operations oleks isikustamise süsteem lubatud. Kui kogu keskkonnale on isikupärastamine välja lülitatud, keelatakse vaated isegi siis, kui järgite alltoodud juhiseid. 

**10.0.9 / platvormivärskendus 33 ja hilisem** Funktsioon **Salvestatud vaated** on kõikides keskkondades saadaval otse funktsioonihalduses. Sarnaselt teistele eelvaate funktsioonidele kehtib selle funktsiooni tootmisse lubamisele [täiendav kasutustingimuste leping](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / platvormiuuendus 32 ja varasem** Funktsiooni **Salvestatud vaated** saab lubada 1. taseme (arendamine/testimine) ja 2. taseme (liivakast) keskkondades, et pakkuda täiendavat testimist ja kujundusmuudatusi, järgides alltoodud juhiseid.

1.  **Luba lend**: Käivitage järgmine SQL-lause: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Lähtesta IIS**, et tühjendada staatilise eelväljaande vahemälu. 

3.  **Leia funktsioon**: avage tööruum **Funktsiooni haldus**. Kui **Salvestatud vaated** ei ilmu loendis, valige **Kontrolli värskendusi**.   

4.  **Luba funktsioon**: leidke funktsioon **Salvestatud vaated** funktsioonide loendist ja valige üksikasjade paanilt suvand **Luba nüüd**.

Kõik järgmised kasutajaseansid algavad lubatud salvestatud vaadetega.


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

Suurte vaate valijatega lehtedel (vaatamiseks saab salvestada isikupärastamisi ja päringuid) näete peamiselt andmeid, mis on ühendatud teie vaikevaatega seostatud päringuga. Sellele kehtib kaks peamist erandit. - Kui liigute paanilt lehele, käivitub paani päring hoolimata vaikevaatega seotud päringust. Kui lõite selle paani pärast vaadete lubamist, paani valimine avab lehe koos selle paaniga seostatud vaatega.   
     - Kui liigute lehele ja sisenemiskoht hõlmab päringut, käivitub algne päring esimesena vaikevaate päringu asemel. Kui selline olukord esineb, kuvatakse teile tavaliselt vaate laadimise ajal asjakohane teade. Samuti saate kinnitada, kui lülitate sellele vaatele pärast lehe laadimist, kuna see peaks sellegipoolest võimaldama vaate päringu käivitumise.  


