---
title: Hajutatud tellimuste haldamine (DOM)
description: Selles teemas kirjeldatakse hajutatud tellimuste haldamise (DOM) funktsiooni rakenduses Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0ebac1c3f9f79ee49ae11a121a4a0dd3bd456c8f
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578480"
---
# <a name="distributed-order-management-dom"></a>Hajutatud tellimuste haldamine (DOM)

[!include [banner](includes/banner.md)]

Jaemüügitoimingute uues paradigmas üritavad jaemüüjad pakkuda isikupärastatud klientide kaasamist, ühiskanali kogemusi ja sujuvat suhtlust. Kuna saadaval on nii palju valikuid, ostlevad tarbijad seal, kus nad saavad kõige positiivsema kogemuse. Paljudel juhtudel ei ole hinnad ja tooted enam tarbijate jaoks peamised otsustajad.

Tarbijakogemuse parandamiseks peab jaemüüjatel olema reaalajas ülevaade oma varudest kõikides kanalites. Üks terviklik ülevaade kõikidest varudest võib aidata optimeerida tellimuste täitmist, eraldamist ja jaotust. Seetõttu muutub hajutatud tellimuste haldamise (DOM) süsteemi omaksvõtmine ja juurutamine jaemüüjatele üha hädavajalikumaks.

DOM optimeerib tellimuste täitmist süsteemide ja protsesside keerukas võrgustikus. See tugineb ühele globaalsele ülevaatele varudest kogu organisatsioonis, et nutikalt hallata tellimusi, et neid täidetaks täpselt ja tulusalt. Jaemüüja tarneahela tõhusust parandades aitab DOM jaemüüjal paremini klientide ootusi täita.

Järgmisel joonisel on näha müügitellimuse elutsükkel DOM-i süsteemis.

![Müügitellimuse elutsükkel DOM-i kontekstis](./media/flow.png "Müügitellimuse elutsükkel DOM-i kontekstis")

## <a name="set-up-dom"></a>DOM-i seadistamine

1. Valige suvandid **Süsteemihaldus \> Seadistamine \> Litsentsi konfiguratsioon**.
2. Vahekaardil **Konfiguratsioonivõtmed** laiendage sõlme **Jaemüük** ja seejärel valige märkeruut **Hajutatud tellimuste haldamine**.
3. Valige suvandid **Jaemüük \> Hajutatud tellimuste haldamine \> Seadistamine \> DOM-i parameetrid**.
4. Vahekaardil **Üldine** määrake järgmised väärtused.

    - **Luba hajutatud tellimuste haldamine** – määrake see suvand väärtusele **Jah**.
    - **Kinnita Bingi kaartide kasutamine DOM-i jaoks** – määrake see suvand väärtusele **Jah**.

        > [!NOTE]
        > Saate selle suvandi määrata väärtusele **Jah** ainult siis, kui suvand **Luba Bingi kaardid** vahekaardil **Bingi kaardid** lehel **Jaemüügi ühisparameetrid** (**Jaemüük \> Peakontori seadistamine \> Parameetrid \> Jaemüügi ühisparameetrid**) on samuti seatud valikule **Jah** ja välja **Bingi kaartide võti** on sisestatud kehtiv võti.

    - **Kinnipidamise perioodi kestus päevades** – määrake, kui kaua hoitakse süsteemis täitmisplaane, mida DOM-i käitused loovad. Pakett-töö **DOM-i täitmisandmete kustutamise töö seadistamine** kustutab kõik täitmisplaanid, mis on vanemad, kui siin määratud päevade arv.
    - **Tagasilükkamise periood (päevades)** – määrake, kui palju aega peab mööduma, enne tagasi lükatud tellimuse rida saab määrata samasse asukohta.

5. Vahekaardil **Lahendaja** määrake järgmised väärtused.

    - **Automaatse täitmise katsete maksimaalne arv** – määrake, kui mitu korda üritab DOM-i mootor tellimuse rida asukohta vahendada. Kui DOM-i mootor ei suuda tellimuse rida määratud arvu katsetega asukohta vahendada, märgistab see tellimuse rea erandina. Seejärel jätab mootor tulevastes käitustes selle rea vahele, kuni olek käsitsi lähtestatakse.
    - **Kohaliku poe piirkonna raadius** – sisestage väärtus. See väli aitab määrata, kuidas asukohti rühmitatakse ja kauguse osas võrdseteks peetakse. Näiteks kui sisestate väärtuse **100**, peetakse iga poodi või jaotuskeskust 100 miili raadiuses täitmisaadressist kauguse osas võrdseteks.
    - **Lahendaja tüüp** – valige väärtus. Retailiga väljastatakse kaks lahendaja tüüpi: **Tootmise lahendaja** ja **Lihtsustatud lahendaja**. Kõikide masinate kohta, mis käitavad DOM-i (ehk kõikide serverite kohta, mis on osa grupist DOMBatch), tuleb valida suvand **Tootmise lahendaja**. Tootmise lahendaja jaoks on vaja spetsiaalset litsentsivõtit, mis vaikimisi litsentsitakse ja juurutatakse tootmiskeskkondades. Mittetootmiskeskkondade jaoks tuleb see litsentsivõti tuleb käsitsi juurutada. Litsentsivõtme käsitsi juurutamiseks järgige allolevaid etappe.

        1. Avage Microsoft Dynamicsi teenuses Lifecycle Services ühiste vahendite teek, valige vahendi tüübiks **Mudel** ja laadige alla fail **DOM-i litsents**.
        2. Käivitage Microsofti teenuste Internet Information Services (IIS) haldur, paremklõpsake valikut **AOSService’i veebisait** ja seejärel valige suvand **Uuri**. Windows Exploreri aken avaneb veebijuures **\<AOS-i teenuse juur\>\\**. Märkige \<AOS-i teenuse juure\> tee üles, kuna kasutate seda järgmises etapis.
        3. Kopeerige konfiguratsioonifail kausta **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        4. Avage programm Retail Headquarters ja seejärel avage leht **DOM-i parameetrid**. Vahekaardil **Lahendaja** väljal **Lahendaja tüüp** valige suvand **Tootmise lahendaja** ja veenduge, et tõrketeateid ei kuvataks.

        > [!NOTE]
        > Lihtsustatud lahendaja on selleks, et jaemüüjad saaksid katsetada DOM-i funktsiooni spetsiaalset litsentsi juurutamata. Organisatsioonid ei tohi lihtsustatud lahendajat kasutada tootmiskeskkondades.
        >
        > Kuigi lihtsustatud lahendaja pakub samasuguseid võimalusi kui tootmise lahendaja, on selles jõudluse (käituses käsitletavate tellimuste ja tellimuse ridade arv) ja tulemuste ühitamise (tellimuste partiid ei pruugi anda mõnes stsenaariumis parimat tulemust) osas piirangud.
     
6. Minge tagasi suvanditesse **Jaemüük \> Hajutatud tellimuste haldamine \> Seadistamine \> DOM-i parameetrid**.
7. Vahekaardil **Numbriseeriad** määrake mitmesugustele DOM-i üksustele vajalikud numbriseeriad.

    > [!NOTE]
    > Enne kui numbriseeriaid saab üksustele määrata, peavad need olema määratud lehel **Numbriseeriad** (**Organisatsiooni haldus \> Numbriseeriad \> Numbriseeriad**).

8. DOM-i funktsioon toetab eri tüüpi DOM-i reeglite defineerimist ja organisatsioonid saavad konfigureerida mitut reeglit, olenevalt oma ärivajadustest. DOM-i reegleid saab defineerida asukohtade grupile või üksikutele asukohtadele ja konkreetsele tootekategooriale, tootele või tootevariandile. DOM-i reeglite jaoks kasutatava asukohtate grupeeringu loomiseks järgige alltoodud etappe.

    1. Valige suvandid **Jaemüük \> Kanali seadistus \> Täitmisgrupid**.
    2. Valige suvand **Uus** ning sisestage uue grupi nimi ja kirjeldus.
    3. Valige käsk **Salvesta**.
    4. Valige suvand **Lisa rida**, et lisada gruppi üks asukoht. Võite ka valida suvandi **Lisa read**, et lisada mitu asukohta.

9. Reeglite defineerimiseks valige suvandid **Jaemüük \> Hajutatud tellimuste haldamine \> Seadistamine \> Reeglite haldamine**. Praegu toetatakse järgmisi DOM-i reegleid.

    - **Minimaalsete varude reegel** – see reegli tüüp laseb organisatsioonidel ümbritseda konkreetseid tootekoguseid muul eesmärgil kui tellimuse täitmiseks. Näiteks ei pruugi organisatsioonid tahta, et DOM võtaks arvesse kõiki varusid, mis on kaupluses tellimuse täitmiseks saadaval. Selle asemel võivad nad soovida jätta osa varusid kohapealsetele klientidele. Kui seda reegli tüüpi kasutatakse, saate määrata minimaalsed varud, mida hoitakse tootekategooria, üksiku toote või tootevariandi jaoks asukohas või asukohtade grupis.
    - **Täitmise asukoha prioriteedi reegel** – see reegli tüüp laseb organisatsioonidel määrata asukohtade hierarhiat, et kehtestada prioriteet, mida DOM-i mootor arvesse võtab, kui üritab tuvastada konkreetsete toodete täitmise asukohti. Prioriteetide kehtiv vahemik on 1 kuni 10, kus 1 on kõrgeid prioriteet ja 10 on madalaim prioriteet. Kõrgema prioriteediga asukohti võetakse arvesse enne madalama prioriteediga asukohti. Kui reegel määratletakse karmi piirangureeglina, vahendatakse tellimused ainult nendesse asukohtadesse, mille jaoks prioriteedid on määratud.
    - **Osaliste tellimuste reegel** – see reegel laseb organisatsioonidel määrata, kas tellimust või tellimuse rida saab täitsa osaliselt. Saadaval on järgmised parameetrid.

        - **Kas täita osalised tellimused?** – kui see valik on seatud väärtusele **Jah**, saab DOM täita ainult osa tellimuse rea kogusest. See osaline täitmine saavutatakse tellimuse rea tükeldamisega.
        - **Kas täita osalised read?** – kui see valik on seatud väärtusele **Jah**, saab DOM täita ainult tellimuse ridade osalise koguse. See osaline täitmine saavutatakse tellimuse rea tükeldamisega.
        - **Kas täita tellimus ainult ühest asukohast?** – kui see valik on seatud väärtusele **Jah**, tagab DOM selle, et kõik tellimuse read täidetakse ühest asukohast.


        Järgmises tabelis kirjeldatakse käitumist, kui nende parameetrite kombinatsioon on määratud.

        |      | Osaliste tellimuste täitmine | Osaliste ridade täitmine | Tellimuse täitmine ainult ühest asukohast | Kirjeldus |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Jah                    | Jah                   | Jah                                  | Täita saab paari tellimuse rida ja üksikuid ridu saab täita osaliselt, aga kõik read peavad DOM-i käituses pärinema eksemplari samast asukohast. (Seda kombinatsiooni praegu ei toetata.) |
        | 2    | Jah                    | Ei                    | Jah                                  | Täita saab paari tellimuse rida, aga üksikuid ridu ei saa täita osaliselt ja kõik täidetud read peavad DOM-i käituses pärinema eksemplari samast asukohast. (Seda kombinatsiooni praegu ei toetata.) |
        | 3    | Jah                    | Jah                   | Ei                                   | Täita saab paari tellimuse rida, üksikuid ridu saab täita osaliselt ja iga rida saab täita DOM-i käituses eksemplaris rohkem kui ühest asukohast. |
        | 4\*  | Ei                     | Pole kohaldatav        | Ei                                   | Kõik tellimuse read peavad olema täidetud, üksikud read ei saa olla osaliselt täidetud ja iga tellimuse rida saab täita eri asukohast. |
        | 5\*  | Ei                     | Pole kohaldatav        | Jah                                  | Kõik tellimuse read peavad olema täidetud, üksikud read ei saa olla osaliselt täidetud ja kõiki tellimuse ridu saab edastada ainult ühest asukohast. |
        | 6\*  | Ei                     | Pole kohaldatav        | Ei                                   | See kombinatsioon toimib nagu kombinatsioon 4, kuna valikut **Osaliste ridade täitmine** ei saa seada väärtusele **Jah**, kui valik **Osaliste tellimuste täitmine** on seatud väärtusele **Ei**. |
        | 7\*  | Ei                     | Pole kohaldatav        | Jah                                  | See kombinatsioon toimib nagu kombinatsioon 5, kuna valikut **Osaliste ridade täitmine** ei saa olla väärtusel **Jah**, kui valik **Osaliste tellimuste täitmine** on seatud väärtusele **Ei**. |
        | 8    | Jah                    | Ei                    | Ei                                   | Täita saab paari tellimuse rida, aga üksikuid ridu ei saa täita osaliselt ja erinevaid tellimuse ridu saab täita DOM-i käituses eksemplaris rohkem kui ühest asukohast. |
        | 9\*  | Ei                     | Pole kohaldatav        | Jah                                  | Kõik tellimuse read peavad olema täidetud ja kõik tellimuse read peavad olema täidetud ainult ühest asukohast. |

        \* Kui valik **Osaliste tellimuste täitmine** on seatud väärtusele **Ei**, arvestatakse alati, et valik **Osaliste ridade täitmine** on seatud väärtusele **Ei**, olenemata sellest, kuidas see tegelikult seatud on.

> [!NOTE]
> Retaili versioonis 10.0.5 on parameeter **Tellimuse täitmine ainult ühest asukohast** asendatud parameetriga **Täitmise asukohtade maksimumarv**. Selle asemel et võimaldada kasutajal konfigureerida, kas tellimused tuleb täita ainult ühest asukohast või nii paljudest asukohtadest, kui võimalik, saavad kasutajad nüüd määrata, kas täitmine toimub määratud hulgast asukohtadest (kuni 5) või nii paljudest asukohtadest, kui võimalik. See annab suurema paindlikkuse selle kohta, mitmest asukohast tellimusi saab täita.

   - **Ühenduseta täitmise asukoha reegel** – see reegel laseb organisatsioonidel määratleda DOM-is asukoha või asukohtade grupi ühenduseta või mittesaadaval asukoha või grupina, nii et tellimusi ei saa nendele asukohtadele täitmiseks määrata.
    - **Maksimaalse tagasilükkamiste arvu reegel** – see reegel laseb organisatsioonidel määratleda tagasilükkamiste läve. Kui lävi saavutatakse, märgib DOM-i protsessor tellimuse või tellimuse rea erandina ja arvab selle edaspidisest töötlusest välja.

        Kui tellimuse read on asukohta määratud, saab asukoht määratud tellimuse rea tagasi lükata, kuna see ei pruugi suuta seda rida teatud põhjustel täita. Tagasilükatud read on märgitud eranditena ja need pannakse tagasi töötlemiskausta järgmisel käitusel. Järgmisel käitusel üritab DOM määrata tagasilükatud rea teise asukohta. Uus asukoht saab samuti määratud tellimuse rida tagasi lükata. See määramiste ja tagasilükkamiste tsükkel võib tekkida mitu korda. Kui tagasilükkamiste arv jõuab määratud läveni, märgib DOM tellimuse rea püsivaks erandiks ega vali seda rida uuesti määramiseks. DOM kaalub tellimuse rida ümbermääramiseks uuesti alles siis, kui kasutaja lähtestab käsitsi tellimuse rea oleku.

   - **Maksimaalse kauguse reegel** – see reegel laseb organisatsioonidel määrata maksimaalse kauguse, kus asukoht või asukohtade grupp võib tellimuse täitmiseks olla. Kui asukohale on määratud kattuvad maksimaalse kauguse reeglid, kohaldub DOM väiksemaile maksimaalsele kaugusele, mis selle asukoha jaoks on määratud.
    - **Maksimaalse tellimuste arvu reegel** – see reegel laseb organisatsioonidel määrata tellimuste maksimaalse arvu, mida asukoht või asukohtade grupp saab kalendripäeva jooksul töödelda. Kui tellimuste maksimaalne arv ühe päeva jooksul on asukohale määratud, ei määra DOM sellele asukohale selle kalendripäeva jooksul rohkem tellimusi.

   Siin on mõned üldised atribuudid, mida saab määrata kõikidele eelnevatele reegli tüüpidele.

   - **Alguskuupäev** ja **Lõppkuupäev** – igale reeglile saab määrata kehtivuskuupäevad, kasutades neid välju.
   - **Keelatud** – DOM-i käituses arvestatakse ainult neid reegleid, mille väärtus selle välja jaoks on **Ei**.
   - **Range piirang** – reegli saab määrata range piiranguna või mitte range piiranguna. Iga DOM-i käitus läbi kaks iteratsiooni. Esimeses iteratsioonis koheldakse iga reeglit range piiranguna, olenemata selle välja väärtusest. See tähendab, et iga reegel kohaldatakse. Ainus erand on reegel **Asukoha prioriteet**. Teises iteratsioonis eemaldatakse reeglid, mis pole määratletud rangete piirangutena, ja asukohtadele määratakse tellimus või tellimuse read, mis ei olnud kõikide reeglite kohaldamisel asukohtadele määratud.

10. Täitmisprofiile kasutatakse reeglikogumi, juriidiliste isikute, müügitellimuste päritolude ja tarneviiside rühmitamiseks. Iga DOM-i käitus on konkreetse täitmisplaani jaoks. Nii saavad organisatsioonid määrata ja käitada reeglite kogumit juriidiliste isikute kogumite jaoks tellimustel, millel on konkreetsed müügitellimuste päritolud ja tarneviisid. Seega, kui eri müügitellimuste päritolude või tarneviiside kogumite jaoks tuleb käitada erinevat reeglite kogumit, saab täitmisprofiile määrata sellele vastavalt. Täitmisprofiilide seadistamiseks läbige need etapid.  

    1. Valige suvandid **Jaemüük \> Hajutatud tellimuste haldamine \> Seadistamine \> Täitmisprofiilid**.
    2. Valige suvand **Uus**.
    3. Sisestage väärtused väljadesse **Profiil** ja **Kirjeldus**.
    4. Määrake suvand **Automaatse rakendamise tulemus**. Kui määrate selle suvandi valikule **Jah**, kohaldatakse profiili DOM-i käituse tulemused automaatselt müügitellimuse ridadele. Kui määrate selle valikule **Ei**, saab tulemusi vaadata ainult täitmisplaanis. Neid ei kohaldata müügitellimuse ridadele.
    5. Kui soovite, et DOM-i profiili käitatakse tellimustele, millel on iga müügitellimuse päritolu olemas, isegi tellimustele, mille müügitellimuse päritolu pole määratletud, määrake suvand **Töötle tellimusi, mille müügiallikas on tühi** valikule **Jah**. Profiili käitamiseks vaid paari müügitellimuse päritolu jaoks saate määrata need lehel **Müügiallikad**, nagu on kirjeldatud allpool.
    6. Valige kiirkaardil **Juriidilised isikud** käsk **Lisa** ja seejärel valige juriidiline isik.
    7. Valige kiirkaardil **Reeglid** käsk **Lisa** ja seejärel valige reegel profiiliga sidumiseks.
    8. Korrake eelmist kahte etappi, kuni kõik vajalikud reeglid on profiiliga seotud.
    9. Valige käsk **Salvesta**.
    10. Toimingupaanil vahekaardil **Seadistamine** valige suvand **Tarneviisid**.
    11. Lehel **Tarneviisid** valige suvand **Uus**.
    12. Väljas **Ettevõte** valige juriidiline isik. Ettevõtete loend on piiratud varem lisatud juriidiliste isikutega.
    13. Valige väljas **Tarneviis** selle profiiliga seostatav tarneviis. Tarneviisi ei saa seostada mitme aktiivse profiiliga.
    14. Korrake eelmist kahte etappi, kuni kõik vajalikud tarneviisid on profiiliga seotud.
    15. Sulgege leht **Tarneviisid**.
    16. Toimingupaanil vahekaardil **Seadistamine** valige suvand **Müügitellimuse päritolud**.
    17. Valige lehel **Müügiallikad** suvand **Uus**.
    18. Väljas **Ettevõte** valige juriidiline isik. Ettevõtete loend on piiratud varem lisatud juriidiliste isikutega.
    19. Väljal **Müügiallikas** valige profiiliga seostamiseks müügiallikas. Müügiallikat ei saa seostada mitme aktiivse profiiliga.
    20. Korrake eelmist kahte etappi, kuni kõik vajalikud müügiallikad on profiiliga seotud.
    21. Sulgege leht **Müügiallikad**.
    22. Määrake suvand **Luba profiil** valikule **Jah**. Kui seadistuses on vigu, kuvatakse hoiatusteade.

## <a name="dom-processing"></a>DOM-i töötlemine

DOM-i käitatakse ainult pakett-töös. DOM-i käituste jaoks pakett-töö konfigureerimiseks järgige allolevaid etappe.

1. Valige suvandid **Jaemüük \> Hajutatud tellimuste haldamine \> Pakktöötlus \> DOM-i protsessori töö seadistamine**.
1. Valige kiirkaardil **Parameetrid** väljast **Täitmisprofiil** profiil, mille jaoks tuleb DOM käitada.
1. Valige kiirkaardil **Käivita taustal** väljast **Pakett-tööde grupp** konfigureeritud pakett-tööde grupp.
1. Sisestage välja **Ülesande kirjeldus** pakett-töö nimi.
1. Valige suvand **Kordumine** ja määrake pakett-töö kordumine.
1. Valige nupp **OK**.

Töötlemise ajal arvestab DOM tellimust ja tellimuse ridu, nagu on kirjeldatud siin.

- DOM-i profiili müügitellimuse pärituolude, tarneviiside ja juriidilise isiku kriteeriumidele ja järgmistele kriteeriumidele vastavad tellimuse read.

    - Need on loodud jaemüügikanalitest.
    - DOM pole neid kunagi vahendanud.
    - DOM on neid varem vahendanud, aga need on märgitud eranditeks ja katsete arv jääb allapoole maksimaalset läve.
    - Tarneviis pole järeletulemine või elektrooniline tarne.
    - Need pole tarneks märgitud.
    - Need pole käsitsi välja arvatud.

- Tellimused, mis pole ootel

Pärast reeglite, varude piirangute ja optimeerimise kohaldamist valib DOM asukoha, mis asub kliendi tarneaadressile kõige lähemal.

![Müügitellimuse kriteeriumid](./media/ordercriteria.png "Müügitellimuse kriteeriumid")

## <a name="results-of-dom-runs"></a>DOM-i käituste tulemused

Kui täitmisprofiil on seatud valikule **Automaatne rakendamine**, rakendatakse käituse tulemused automaatselt müügitellimuse ridadele ja täitmisplaani saab eraldi vaadata. Kui aga täitmisprofiil ei ole seatud valikule **Automaatne rakendamine**, saab käituse tulemusi näha ainult täitmisplaani vaatest. 

Kõikide loodud täitmisplaanide vaatamiseks järgige alltoodud etappe.

1. Valige suvandid **Jaemüük \> Hajutatud tellimuste haldamine \> Hajutatud tellimuste haldamine**.
2. Valige tööruumist **Hajutatud tellimuste haldamine** paan **Täitmisplaanid**.
3. Täitmisplaani vaatamiseks valige vastava tellimuse täitmisplaani ID.

    Täitmisplaani tellimuse üksikasjade jaotis kuvab algsed müügitellimuse read, mis olid osa käitusest. Peale standardsete müügitellimuse rea väljade sisaldab tellimuse üksikasjade jaotis järgmist kolme DOM-iga seotud välja.

    - **Täitmistüüp** – see väli näitab, kas müügitellimuse rida on asukohta täielikult vahendatud, osaliselt vahendatud või üldse mitte vahendatud.
    - **Tükeldamine** – see väli näitab, kas üks müügitellimuse rida on tükeldatud ja vahendatud teistesse asukohtadesse.
    - **Täitmisasukohtade arv** – see väli näitab, kui mitu täitmisrida ühe müügitellimuse rea jaoks loodi (lähtudes asukohtade arvust, kuhu algne müügitellimuse rida oli vahendatud).

    Tellimuse täitmise üksikasjade jaotises on näha algse müügitellimuse ridade määramine teistesse asukohtadesse koos nende kogustega.

## <a name="order-line-actions-and-statuses"></a>Tellimuse rea tegevused ja olekud

Järgnevalt kirjeldatakse tellimuse rea sätteid. Tellimuse rea avamiseks valige suvandid **Jaemüük \> Kliendid \> Kõik müügitellimused**.
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

1. Valige suvandid **Jaemüük \> Hajutatud tellimuste haldamine \> Pakktöötlus \> DOM-i täitmisplaani kustutamise töö seadistamine**. 
1. Valige väljast **Pakett-tööde grupp** konfigureeritud pakett-tööde grupp.
1. Valige suvand **Kordumine** ja määrake pakett-töö kordumine.
1. Valige nupp **OK**.

## <a name="more-information"></a>Lisateave

Allpool on mõned asjad, mida DOM-i funktsiooni kasutades arvesse tuleb võtta.

- Praegu vaatab DOM ainult tellimusi, mis on loodud jaemüügikanalitest. Müügitellimused tuvastatakse jaemüügitellimustena, kui suvand **Jaemüük** on seatud valikule **Jah**.
- Microsoft ei ole katsetanud DOM-i laohalduse täiustatud funktsioonidega. Kliendid ja partnerid peavad hoolikalt määratlema, kas DOM ühildub laohalduse täiustatud võimaluste ja protsessidega, mis on nende jaoks asjakohased.
- DOM on saadaval ainult Retaili pilveversioonis. Seda ei toetata asutusesisestes juurutustes.
