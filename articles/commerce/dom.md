---
title: Hajutatud tellimuste haldamine (DOM)
description: Selles teemas kirjeldatakse hajutatud tellimuste haldamise (DOM) funktsiooni rakenduses Dynamics 365 Commerce.
author: josaw1
ms.date: 02/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: f19fbe2a9f768a91c495a6a4bcb0e475adb867ae
ms.sourcegitcommit: 8bea5a0c232ac31dcafddfcc0d715c496d8dd445
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102005"
---
# <a name="distributed-order-management-dom"></a>Hajutatud tellimuste haldamine (DOM)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse hajutatud tellimuste haldamise (DOM) funktsiooni rakenduses Microsoft Dynamics 365 Commerce.

DOM on kõiki müügikanaleid hõlmav tellimuste täitmise optimeerimise lahendus, mis aitab maksimeerida tellimuste täitmist tarneahela võrgus. DOM aitab tagada, et tooteid tarnitakse klientidele õiges koguses, õigetest allikatest ja õigel ajal. Samuti võib DOM aidata teil suurendada kasumit, vähendada kulusid ja vastata teenusetaseme nõuetele.

DOM kasutab nii partii tasemel kui ka üksikute tellimuste tasemel optimeerimiseks segaarvu programmeerimist (MIP) ja ennustava analüüsi mudeleid. See suutlikkus võimaldab jaemüüjatel kasutada määratletud reegleid, et tasakaalustada mitmeid vastuolulisi tellimuse täitmise vajadusi. Tänapäevases tarnevõrgus, kus tellimuste täitmine võib toimuda mitme kanali kaudu, peavad organisatsioonid kiiresti kohanema tellimuste muutuste, tarnija saadavusprobleemide ja nõudluse kasvuga. DOM aitab teil maksimeerida tellimuste täitmist ja leida õiged allikad toodete tarnimiseks, lähtudes äripiirangutest ja -eesmärkidest, nagu kulude minimeerimine, täites tellimusi lähimatest allikatest. DOM kasutab tellimuste täitmise optimeerimiseks tellimuste täitmise allikate ja tarnesihtkohtade vahelist kaugust, optimeerimise eesmärkidena määratletud kulutegureid ning piirangutena määratletud reegleid, nagu täitmissõlmedes asuvad varud. DOM võimaldab määratleda mitmeid profiile, mis võimaldavad ettevõtetel käitada erinevaid optimeerimisstrateegiaid olenevalt äri- või tarbesegmendi tüübist. 

Järgmisel joonisel on näha müügitellimuse elutsükkel DOM-i süsteemis.

![Müügitellimuse elutsükkel DOM-i kontekstis.](./media/flow.png "Müügitellimuse elutsükkel DOM-i kontekstis")

## <a name="set-up-dom"></a>DOM-i seadistamine

1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
2. Vahekaardil **Konfiguratsioonivõtmed** laiendage sõlme **Kaubandus** ja seejärel valige märkeruut **Hajutatud tellimuste haldamine**.
3. Valige suvandid **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Häälestus \> DOM-i parameetrid**.
4. Vahekaardil **Üldine** määrake järgmised väärtused.

    - **Luba hajutatud tellimuste haldamine** – määrake see suvand väärtusele **Jah**.
    - **Kinnita Bingi kaartide kasutamine DOM-i jaoks** – määrake see suvand väärtusele **Jah**.

        > [!NOTE]
        > Saate selle suvandi määrata väärtusele **Jah** ainult siis, kui suvand **Luba Bingi kaardid** vahekaardil **Bingi kaardid** lehel **Kaubanduse ühisparameetrid** (**Retail ja Commerce \> Peakontori häälestus \> Parameetrid \> Kaubanduse ühisparameetrid**) on samuti seatud valikule **Jah** ja välja **Bingi kaartide võti** on sisestatud kehtiv võti.
        >
        > Portaal [Bing Maps Dev Center](https://www.bingmapsportal.com/) võimaldab teil piirata juurdepääsu Bing Mapsi API võtmetel määratletud domeenikomplektiga. Selle funktsiooni abil saavad kliendid määratleda täpse viitajaväärtuste või IP-aadresside komplekti, mille suhtes võti valideeritakse. Teie lubatute loendis olevaid taotlusi töödeldakse tavapäraselt, kuid loendisse mittekuuluvad taotlused saavad vastuse, et juurdepääs on keelatud. Domeeniturbe lisamine API-võtmele on valikuline ja senisesse olekusse jäävad võtmed toimivad edasi. Iga võtme lubatute loend on teistest võtmetest sõltumatu, võimaldades teil määrata igale võtmele eraldi reeglid. Hajutatud tellimuste haldamine ei toeta domeenile viitavate atribuutide seadistamist.

    - **Kinnipidamise perioodi kestus päevades** – määrake, kui kaua hoitakse süsteemis täitmisplaane, mida DOM-i käitused loovad. Pakett-töö **DOM-i täitmisandmete kustutamise töö häälestus** kustutab kõik täitmisplaanid, mis on vanemad, kui siin määratud päevade arv.
    - **Tagasilükkamise periood (päevades)** – määrake, kui palju aega peab mööduma, enne tagasi lükatud tellimuse rida saab määrata samasse asukohta.

5. Vahekaardil **Lahendaja** määrake järgmised väärtused.

    - **Automaatse täitmise katsete maksimaalne arv** – määrake, kui mitu korda üritab DOM-i mootor tellimuse rida asukohta vahendada. Kui DOM-i mootor ei suuda tellimuse rida määratud arvu katsetega asukohta vahendada, märgistab see tellimuse rea erandina. Seejärel jätab mootor tulevastes käitustes selle rea vahele, kuni olek käsitsi lähtestatakse.
    - **Kohaliku poe piirkonna raadius** – sisestage väärtus. See väli aitab määrata, kuidas asukohti rühmitatakse ja kauguse osas võrdseteks peetakse. Näiteks kui sisestate väärtuse **100**, peetakse iga poodi või jaotuskeskust 100 miili raadiuses täitmisaadressist kauguse osas võrdseteks.
    - **Lahendaja tüüp** – valige väärtus. Kaubandusega väljastatakse kaks lahendaja tüüpi: **Tootmise lahendaja** ja **Lihtsustatud lahendaja**. Kõikide masinate kohta, mis käitavad DOM-i (ehk kõikide serverite kohta, mis on osa grupist DOMBatch), tuleb valida suvand **Tootmise lahendaja**. Tootmise lahendaja jaoks on vaja spetsiaalset litsentsivõtit, mis vaikimisi litsentsitakse ja juurutatakse tootmiskeskkondades. Uuemates 2+ järgu keskkondades on tootmise lahendaja juba lubatud. Mittetootmiskeskkondade jaoks tuleb see litsentsivõti käsitsi juurutada. Litsentsivõtme käsitsi juurutamiseks järgige allolevaid etappe.

        1. Avage Microsoft Dynamicsi teenuses Lifecycle Services ühiste vahendite teek, valige vahendi tüübiks **Mudel** ja laadige alla fail **DOM-i litsents**.
        1. Käivitage Microsofti Internet Information Servicese (IIS) haldur, paremklõpsake valikut **AOSService’i veebisait** ja seejärel valige suvand **Uuri**. Windows Exploreri aken avaneb veebijuures **\<AOS service root\>\\webroot**. Märkige \<AOS Service root\> tee üles, kuna kasutate seda järgmises etapis.
        1. Kopeerige konfiguratsioonifail kausta **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Minge kaupluse halduse kaubanduse peakontori klientrakendusse ja avage leht **DOM-i parameetrid**. Vahekaardil **Lahendaja** väljal **Lahendaja tüüp** valige suvand **Tootmise lahendaja** ja kinnitage, et tõrketeateid ei kuvataks.

        > [!NOTE]
        > Lihtsustatud lahendaja on selleks, et jaemüüjad saaksid katsetada DOM-i funktsiooni spetsiaalset litsentsi juurutamata. Organisatsioonid ei tohi lihtsustatud lahendajat kasutada tootmiskeskkondades.
        >
        > Tootmise lahendaja parendab jõudlust (nt käituses käsitletavate tellimuste ja tellimuse ridade arv) ja tulemuste ühitamist (kuna tellimuste partii ei pruugi anda mõnes stsenaariumis parimat tulemust). Mõned reeglid, nt **osaliste tellimuste reegel** ja **asukohtade maksimumarvu reegel**, vajavad tootmise lahendajat.

6. Minge tagasi suvandisse **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Häälestus \> DOM-i parameetrid**.
7. Vahekaardil **Numbriseeriad** määrake mitmesugustele DOM-i üksustele vajalikud numbriseeriad.

    > [!NOTE]
    > Enne kui numbriseeriaid saab üksustele määrata, peavad need olema määratud lehel **Numbriseeriad** (**Organisatsiooni haldus \> Numbriseeriad \> Numbriseeriad**).

8. DOM-i funktsioon toetab eri tüüpi DOM-i reeglite defineerimist ja organisatsioonid saavad konfigureerida mitut reeglit, olenevalt oma ärivajadustest. DOM-i reegleid saab defineerida asukohtade grupile või üksikutele asukohtadele ja konkreetsele tootekategooriale, tootele või tootevariandile. DOM-i reeglite jaoks kasutatava asukohtate grupeeringu loomiseks järgige alltoodud etappe.

    1. Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Täitmisgrupid**.
    2. Valige suvand **Uus** ning sisestage uue grupi nimi ja kirjeldus.
    3. Valige käsk **Salvesta**.
    4. Valige suvand **Lisa rida**, et lisada gruppi üks asukoht. Võite ka valida suvandi **Lisa read**, et lisada mitu asukohta.

    > [!NOTE]
    > Rakenduse Commerce versioonis 10.0.12 ja uuemas peab valik **Võimalus määrata asukohti nii, et olek Lähetamine või Pealevõtmine on täitmisgrupis lubatud** olema tööruumis **Funktsioonihaldus** lubatud.
    >
    > See funktsioon lisab lehele **Täitmisgrupp** uued konfiguratsioonid, et saaksite määrata, kas ladu saab kasutada lähetamise jaoks või kas lao/poe kombinatsiooni saab kasutada lähetamise, pealevõtmise või mõlema jaoks. 
    >
    > Kui lubate funktsiooni, värskendatakse asukoha valimiseks saadaolevaid suvandeid, kui loote kassas pealevõtmis- või lähetustellimusi.
    >
    > Selle funktsiooni lubamise tulemusel värskendatakse lehti ka kassas, kui toimingud „Läheta kõik“ või „Läheta valitud“ on valitud.

9. Reeglite määratlemiseks valige suvandid **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Häälestus \> Reeglite haldamine**. Praegu toetatakse järgmisi DOM-i reegleid.

    - **Minimaalsete varude reegel** – see reegli tüüp laseb organisatsioonidel ümbritseda konkreetseid tootekoguseid muul eesmärgil kui tellimuse täitmiseks. Näiteks ei pruugi organisatsioonid tahta, et DOM võtaks arvesse kõiki varusid, mis on kaupluses tellimuse täitmiseks saadaval. Selle asemel võivad nad soovida jätta osa varusid kohapealsetele klientidele. Kui seda reegli tüüpi kasutatakse, saate määrata minimaalsed varud, mida hoitakse tootekategooria, üksiku toote või tootevariandi jaoks asukohas või asukohtade grupis. Samuti saate määratleda minimaalse kaubavaru, kasutades täiendavat kategooriahierarhiat. Kui toode kuulub mitmesse kategooriasse, omistatakse lisakategooriale kõigi reeglite puhul, kus saate kategooriaid kasutada, kõrgeim tähtsus.
    - **Täitmise asukoha prioriteedi reegel** – see reegli tüüp laseb organisatsioonidel määrata asukohtade hierarhiat, et kehtestada prioriteet, mida DOM-i mootor arvesse võtab, kui üritab tuvastada konkreetsete toodete täitmise asukohti. Prioriteetide kehtiv vahemik on 1 kuni 10, kus 1 on kõrgeid prioriteet ja 10 on madalaim prioriteet. Kõrgema prioriteediga asukohti võetakse arvesse enne madalama prioriteediga asukohti. Kui reegel määratletakse karmi piirangureeglina, vahendatakse tellimused ainult nendesse asukohtadesse, mille jaoks prioriteedid on määratud. DOM eelistab lähetada tellimusi täielikult ühest asukohast. Seega, kui kogu tellimus ja selle read ei ole saadaval asukohas, mille prioriteet on 1, proovib DOM seda täita asukohas, mille prioriteet on 2.
    - **Osaliste tellimuste reegel** – Retaili versioonis 10.0.5 on parameeter **Tellimuse täitmine ainult ühest asukohast** asendatud parameetriga **Täitmise asukohtade maksimumarv**. Vana parameeter lubab kasutajatel konfigureerida, kas tellimusi saab täita ainult ühest asukohast või võimalikult paljudest asukohtadest. Uus parameeter võimaldab kasutajatel määrata, kas täitmine võib toimuda kindlas asukohtade kogumis (kuni viis) või nii paljudest asukohtadest kui võimalik. Kõikide valikute puhul, v.a täitmine ühest asukohast, tükeldab DOM rea, sest tellimuse töötlemine toimub rea haaval. See reegel töötab ainult tootmise lahendajaga.
    - **Võrguühenduseta täitmisasukoha reegel** – see reegel laseb organisatsioonidel määratleda DOM-is asukoha või asukohtade grupi võrguühenduseta või mittesaadavana, nii et tellimusi ei saa nendes asukohtades täitmiseks määrata.
    - **Maksimaalse tagasilükkamiste arvu reegel** – see reegel laseb organisatsioonidel määratleda tagasilükkamiste läve. Kui lävi saavutatakse, märgib DOM-i protsessor tellimuse või tellimuse rea erandina ja arvab selle edaspidisest töötlusest välja. Jõudluse tagamiseks ei vaata DOM kõigi tagasilükkamiste ajalugu. 

        Kui tellimuse read on asukohta määratud, saab asukoht määratud tellimuse rea tagasi lükata, kuna see ei pruugi suuta seda rida teatud põhjustel täita. Tagasilükatud read on märgitud eranditena ja need pannakse tagasi töötlemiskausta järgmisel käitusel. Järgmisel käitusel üritab DOM määrata tagasilükatud rea teise asukohta. Uus asukoht saab samuti määratud tellimuse rida tagasi lükata. See määramiste ja tagasilükkamiste tsükkel võib tekkida mitu korda. Kui tagasilükkamiste arv jõuab määratud läveni, märgib DOM tellimuse rea püsivaks erandiks ega vali seda rida uuesti määramiseks. DOM kaalub tellimuse rida ümbermääramiseks uuesti alles siis, kui kasutaja lähtestab käsitsi tellimuse rea oleku.

    - **Maksimaalse kauguse reegel** – see reegel laseb organisatsioonidel määrata maksimaalse kauguse, kus asukoht või asukohtade grupp võib tellimuse täitmiseks olla. Kui asukohale on määratud kattuvad maksimaalse kauguse reeglid, kohaldub DOM väiksemaile maksimaalsele kaugusele, mis selle asukoha jaoks on määratud.
    - **Maksimaalse tellimuste arvu reegel** – see reegel laseb organisatsioonidel määrata tellimuste maksimaalse arvu, mida asukoht või asukohtade grupp saab töödelda. Optimeerimisprotsessi ajal võtab süsteem arvesse neid tellimusi, mida pole neist asukohtadest lähetatud. Seda kontrolli tehakse kõigis profiilides. Seega, kui tellimuste maksimumarv kattub ühe asukoha kõigis profiilides, võtab süsteem arvesse kõigi profiilide jaoks määratletud tellimuste maksimumarvu. 

    Siin on mõned üldised atribuudid, mida saab määrata kõikidele eelnevatele reegli tüüpidele.

    - **Alguskuupäev** ja **Lõppkuupäev** – neid välju saate kasutada iga reegli kehtivuskuupäevade määramiseks.
    - **Keelatud** – DOM-i käituses arvestatakse ainult neid reegleid, mille väärtus selle välja jaoks on **Ei**.
    - **Range piirang** – reegli saab määrata range piiranguna või mitte range piiranguna. Iga DOM-i käitus läbi kaks iteratsiooni. Esimeses iteratsioonis koheldakse iga reeglit range piiranguna, olenemata selle välja väärtusest. See tähendab, et iga reegel kohaldatakse. Ainus erand on reegel **Asukoha prioriteet**. Teises iteratsioonis eemaldatakse reeglid, mis pole määratletud rangete piirangutena, ja asukohtadele määratakse tellimus või tellimuse read, mis ei olnud kõikide reeglite kohaldamisel asukohtadele määratud.

10. Täitmisprofiile kasutatakse reeglikogumi, juriidiliste isikute, müügitellimuste päritolude ja tarneviiside rühmitamiseks. Iga DOM-i käitus on konkreetse täitmisplaani jaoks. Nii saavad organisatsioonid määrata ja käitada reeglite kogumit juriidiliste isikute kogumite jaoks tellimustel, millel on konkreetsed müügitellimuste päritolud ja tarneviisid. Seega, kui eri müügitellimuste päritolude või tarneviiside kogumite jaoks tuleb käitada erinevat reeglite kogumit, saab täitmisprofiile määrata sellele vastavalt. Täitmisprofiilide häälestuseks läbige need etapid.  

    1. Valige suvandid **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Häälestus \> Täitmisprofiilid**.
    2. Valige suvand **Uus**.
    3. Sisestage väärtused väljadesse **Profiil** ja **Kirjeldus**.
    4. Määrake suvand **Automaatse rakendamise tulemus**. Kui määrate selle suvandi valikule **Jah**, kohaldatakse profiili DOM-i käituse tulemused automaatselt müügitellimuse ridadele. Kui määrate selle valikule **Ei**, saab tulemusi vaadata ainult täitmisplaanis. Neid ei kohaldata müügitellimuse ridadele.
    5. Kui soovite, et DOM-i profiili käitataks tellimuste puhul, millel on iga müügitellimuse päritolu olemas, sh tellimuste puhul, mille müügitellimuse päritolu pole määratletud, määrake suvandi **Töötle tellimusi, mille müügiallikas on tühi** väärtuseks **Jah**. Profiili käitamiseks vaid mõne müügitellimuse päritolu jaoks saate need määrata lehel **Müügiallikad**, nagu on kirjeldatud allpool.

        > [!NOTE]
        > Rakenduse Commerce versioonis 10.0.12 ja uuemas peab funktsioon **Võimalus määrata täitmisgruppi täitmisprofiilile** olema tööruumis **Funktsioonihaldus** lubatud. See funktsioon võimaldab teil määratleda ladude loendi, mida DOM peaks võtma arvesse, kui optimeerimine käivitatakse täitmisprofiiliga. Kui see ladude loend on määramata, võtab DOM arvesse kõiki profiilis määratud juriidiliste isikute ladusid.
        >
        > See funktsioon lisab uue konfiguratsiooni lehele **Täitmisprofiil**, mille saab seostada ühe täitmisgrupiga. 
        >
        > Kui valite täitmisgrupi, käivitatakse selle täitmisprofiili DOM-i reeglid täitmisgrupis sisalduvate „lähetavate“ ladude kohta. 
        > 
        > Selle funktsiooni tõhusaks kasutamiseks veenduge, et oleks üks täitmisgrupp, mis sisaldaks kõiki lähetavaid ladusid, ja seejärel seostage see täitmisgrupp täitmisprofiiliga.

    6. Valige kiirkaardil **Juriidilised isikud** käsk **Lisa** ja seejärel valige juriidiline isik.
    7. Valige kiirkaardil **Reeglid** käsk **Lisa** ja seejärel valige reegel profiiliga sidumiseks.
    8. Korrake eelmist kahte etappi, kuni kõik vajalikud reeglid on profiiliga seotud.
    9. Valige käsk **Salvesta**.
    10. Toimingupaanil vahekaardil **Häälestus** valige suvand **Tarneviisid**.
    11. Lehel **Tarneviisid** valige suvand **Uus**.
    12. Väljas **Ettevõte** valige juriidiline isik. Ettevõtete loend on piiratud varem lisatud juriidiliste isikutega.
    13. Valige väljas **Tarneviis** selle profiiliga seostatav tarneviis. Tarneviisi ei saa seostada mitme aktiivse profiiliga.
    14. Korrake eelmist kahte etappi, kuni kõik vajalikud tarneviisid on profiiliga seotud.
    15. Sulgege leht **Tarneviisid**.
    16. Toimingupaanil vahekaardil **Häälestus** valige suvand **Müügitellimuse päritolud**.
    17. Valige lehel **Müügiallikad** suvand **Uus**.
    18. Väljas **Ettevõte** valige juriidiline isik. Ettevõtete loend on piiratud varem lisatud juriidiliste isikutega.
    19. Väljal **Müügiallikas** valige profiiliga seostamiseks müügiallikas. Müügiallikat ei saa seostada mitme aktiivse profiiliga.
    20. Korrake eelmist kahte etappi, kuni kõik vajalikud müügiallikad on profiiliga seotud.
    21. Sulgege leht **Müügiallikad**.
    22. Määrake suvand **Luba profiil** valikule **Jah**. Kui häälestuses on vigu, kuvatakse hoiatusteade.

## <a name="dom-processing"></a>DOM-i töötlemine

DOM-i käitatakse ainult pakett-töös. DOM-i käituste jaoks pakett-töö konfigureerimiseks järgige allolevaid etappe.

1. Valige suvandid **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Pakktöötlus \> DOM-i protsessori töö häälestus**.
1. Valige kiirkaardil **Parameetrid** väljast **Täitmisprofiil** profiil, mille jaoks tuleb DOM käitada.
1. Valige kiirkaardil **Käivita taustal** väljast **Pakett-tööde grupp** konfigureeritud pakett-tööde grupp.
1. Sisestage välja **Ülesande kirjeldus** pakett-töö nimi.
1. Valige suvand **Kordumine** ja määrake pakett-töö kordumine.
1. Valige nupp **OK**.

Töötlemise ajal arvestab DOM tellimust ja tellimuse ridu, nagu on kirjeldatud siin.

- DOM-i profiili müügitellimuse pärituolude, tarneviiside ja juriidilise isiku kriteeriumidele ja järgmistele kriteeriumidele vastavad tellimuse read.

    - Need on loodud kaubanduskanalitest.
    - DOM pole neid kunagi vahendanud.
    - DOM on neid varem vahendanud, aga need on märgitud eranditeks ja katsete arv jääb allapoole maksimaalset läve.
    - Tarneviis pole järeletulemine või elektrooniline tarne.
    - Need pole tarneks märgitud.
    - Need pole käsitsi välja arvatud.

- Tellimused, mis pole ootel

Pärast reeglite, varude piirangute ja optimeerimise kohaldamist valib DOM asukoha, mis asub kliendi tarneaadressile kõige lähemal. DOM teisendab **Tarne** tüüpi aadressid laius- ja pikkuskraadi väärtusteks. Seejärel teisendab see müügitellimuse tarneaadressi laius- ja pikkuskraadi väärtusteks ning värskendab aadressi laius- ja pikkuskraadi väärtusi edaspidiseks kasutamiseks. DOM kasutab Bingi kaarte, et määrata täpsed laius- ja pikkuskraadi väärtused, mis põhinevad aadressi-, linna- ja sihtnumbriteabel.

Olenevalt seadetest kasutab DOM õhu- või teekauguste arvutamiseks Bingi kaartide API-d. Seejärel kasutab rakendus seda teavet saatmiskulu määramiseks. Optimeerimismudel prioritiseerib kogu tellimuse täitmist ühest asukohast. Isegi kui osa tellimusest on saadaval samas linnas või sihtnumbris, on mudelit optimeeritud lähetuste arvu vähendamiseks. 

DOM otsib saadaolevat varu, kuvades olemasoleva varu lao V2 üksustes. Iga pakktöötluse ajal jaotab DOM tellimused partiiks, sõltuvalt profiilis määratletud ülesannete **DOM-i protsessori** parameetri väärtusest. Selle parameetri vaikeväärtus on **2000**. Näiteks kui töötluses optimeeritakse 10 000 tellimuserida ja **DOM-i protsessori** parameetri vaikeväärtuseks on seatud **2000**, loob DOM viis partiid, mida töödeldakse samaaegselt. Seejärel saadakse optimeerjalt täitmisplaanid ja rakendatakse need reale. Kui tellimuserida tuleb kahe asukoha vahel jagada, tagab DOM, et hinnad ja maksud oleksid ridade vahel asjakohaselt jaotatud.

![Müügitellimuste kriteeriumid.](./media/ordercriteria.png "Müügitellimuste kriteeriumid")

## <a name="results-of-dom-runs"></a>DOM-i käituste tulemused

Kui täitmisprofiil on seatud valikule **Automaatne rakendamine**, rakendatakse käituse tulemused automaatselt müügitellimuse ridadele ja täitmisplaani saab eraldi vaadata. Kui aga täitmisprofiil ei ole seatud valikule **Automaatne rakendamine**, saab käituse tulemusi näha ainult täitmisplaani vaatest. 

Kõikide loodud täitmisplaanide vaatamiseks järgige alltoodud etappe.

1. Valige suvandid **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Hajutatud tellimuste haldamine**.
2. Valige tööruumist **Hajutatud tellimuste haldamine** paan **Täitmisplaanid**.
3. Täitmisplaani vaatamiseks valige vastava tellimuse täitmisplaani ID.

    Täitmisplaani tellimuse üksikasjade jaotis kuvab algsed müügitellimuse read, mis olid osa käitusest. Peale standardsete müügitellimuse rea väljade sisaldab tellimuse üksikasjade jaotis järgmist kolme DOM-iga seotud välja.

    - **Täitmistüüp** – see väli näitab, kas müügitellimuse rida on asukohta täielikult vahendatud, osaliselt vahendatud või üldse mitte vahendatud.
    - **Tükeldamine** – see väli näitab, kas üks müügitellimuse rida on tükeldatud ja vahendatud teistesse asukohtadesse.
    - **Täitmisasukohtade arv** – see väli näitab, kui mitu täitmisrida ühe müügitellimuse rea jaoks loodi (lähtudes asukohtade arvust, kuhu algne müügitellimuse rida oli vahendatud).

    Tellimuse täitmise üksikasjade jaotises on näha algse müügitellimuse ridade määramine teistesse asukohtadesse koos nende kogustega.

## <a name="order-line-actions-and-statuses"></a>Tellimuse rea tegevused ja olekud

Järgnevalt kirjeldatakse tellimuse rea sätteid. Tellimuse rea avamiseks valige suvandid **Retail ja Commerce \> Kliendid \> Kõik müügitellimused**.

- Kui määrate suvandi **Välista DOM-i töötlemisest** müügitellimuse rea vahekaardil **Üldine** valikule **Jah**, välistatakse tellimus või tellimuse rida DOM-i töötlemisest.
- Välja **DOM-i olek** müügitellimuse rea vahekaardil **Üldine** saab määrata ühele järgmistest väärtustest.

    - **Puudub** – tellimuse rida pole kunagi vahendatud.
    - **Lõpule viidud** – tellimuse rida on edukalt vahendatud ja asukohta määratud.
    - **Erand** – tellimuse rida on vahendatud, aga seda ei saa asukohta määrata. Eranditel on mitu alatüüpi, mida saab vaadata DOM-i tööruumis.

        - **Kogus pole saaval** – puuduvad saadaolevad varud, millele tellimust asukohtades määrata.
        - **Maksimaalne tagasilükkamiste arv** – tellimuse rida on saavutanud tagasilükkamiste maksimaalse läve.
        - **Andmete muutmise konflikt** – müügitellimuse rida on pärast tellimuse vahendamist muudetud. Seetõttu ei saa täitmisplaani tellimusele kohaldada.
        - **Tellimuse rea spetsiifiline erand** – tellimuse real on mitu erandit.

- Müügitellimuse sisestamise ajal saab DOM-i käivitada interaktiivses režiimis. Tellimuse rea sisestamise ajal saate pärast toote ja koguse määramist valige käsu **Uuenda rida** ja seejärel valida jaotisest **DOM** suvandi **Soovita täitmisasukohta**. Seejärel näete asukohtade loendit, mis põhineb DOM-i reeglitel, mis saavad täita tellimuse rea kogust. Seda loendit sorditakse kauguse järgi. Valige asukoht vastava koha ja lao määramiseks müügitellimuse reale. Selleks et see funktsioon toimiks, peab olemas olema aktiivne täitmisprofiil, mis vastab müügiallikale ja tarneviisile müügireal.
- Müügitellimuse rea DOM-i käituse logide vaatamiseks valige suvand **Müügitellimuse rida** ja seejärel valige jaotisest **DOM** suvand **Kuva DOM-i logid**. DOM-i logid kuvavad kõik sündmused ja logid, mille DOM-i käitus lõi. Logid aitavad teil mõista, miks konkreetne asukoht tellimuse reale määrati ning milliseid reegleid ja piiranguid määramisel arvestati. Vahekaardil **Haldamine** on DOM-i logid saadaval ja müügitellimuse päise tasemel.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>DOM-i täitmisplaanide jaoks koristustöö käivitamine

DOM-i töötluse käivitamisel luuakse täitmisplaanid. Aja jooksul säilitab süsteem hulgaliselt täitmisplaane. Süsteemi säilitatavate täitmisplaanide hulga haldamiseks saate konfigureerida pakett-töö, mis kustutab vanemat täitmisplaanid, lähtudes väärtusest **Kinnipidamise perioodi kestus päevades**.

1. Valige suvandid **Retail ja Commerce \> Hajutatud tellimuste haldamine \> Pakktöötlus \> DOM-i täitmisplaani kustutamise töö häälestus**. 
1. Valige väljast **Pakett-tööde grupp** konfigureeritud pakett-tööde grupp.
1. Valige suvand **Kordumine** ja määrake pakett-töö kordumine.
1. Valige nupp **OK**.

## <a name="more-information"></a>Lisateave

Allpool on mõned asjad, mida DOM-i funktsiooni kasutades arvesse tuleb võtta.

- Praegu vaatab DOM ainult tellimusi, mis on loodud kaubanduskanalitest. Müügitellimused tuvastatakse jaemüügitellimustena, kui suvand **Kaubanduse müük** on seatud valikule **Jah**.
- Microsoft ei ole katsetanud DOM-i laohalduse täiustatud funktsioonidega. Seega peavad kliendid ja partnerid hoolikalt määratlema, kas DOM ühildub laohalduse täiustatud võimaluste ja protsessidega, mis on nende jaoks asjakohased. Täpsem ladustamine võimaldab konfigureeritavaid dimensioone, nt laovaru olekut, mis ei anna täpset arusaama saadaolevast varust. DOM pakub laiendatavat meetodid saadaoleva laovaru määramiseks täpsemat ladustamist kasutavate rakenduste puhul. Seda saab kasutada kohandatud laovaru oleku väärtuste ja muude dimensioonidega töötamiseks.

    DOM-i laiendatavus on piiratud, kuna optimeerimine toimub valmisehitatud MIP-mudelis, mis võtab arvesse optimeerimist ja selle piiranguid. Laovaru ja järeltöötluse optimeerimise seadistamiseks on juba saadaval mitu laiendatavat punkti. DOM-i profiilid võivad müügi päritolu ja tarneviisi järgi erineda. Müügitellimuse päritolu saab määrata tellimuse sisestamise ajal ja nende väärtuste põhjal saab kasutada erinevaid optimeerimisstrateegiaid. DOM toetab ka kohandatud pakett-tööde loomist, mis võivad võtta sisendiks DOM-protsessori ülesande ja võimaldada profiili parameetrina edastamist. Tänu sellele saab erinevate äristsenaariumide toetamiseks käivitada üht optimeerimist teise järel.

- DOM on saadaval ainult kaubanduse pilveversioonis. Seda ei toetata asutusesisestes juurutustes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
