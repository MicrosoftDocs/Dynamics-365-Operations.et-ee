---
title: "Jaemüügi välisseadme simulaator"
description: "Selles teemas kirjeldatakse välisseadme simulaatori tööriista, mis Microsoft Dynamics 365 for Operationsi jaemüügi mooduliga kaasas on."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 894aaaaa844447030dae73826d326f99366aa068
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="retail-peripheral-simulator"></a>Jaemüügi välisseadme simulaator

[!include[banner](includes/banner.md)]


Selles teemas kirjeldatakse välisseadme simulaatori tööriista, mis Microsoft Dynamics 365 for Operationsi jaemüügi mooduliga kaasas on.

<a name="overview"></a>Ülevaade
--------

Microsoft Dynamics 365 for Operationsi jaemüügi välisseadme simulaator on tööriist, mis aitab seadistada ja testida jaemüügikeskkondades kasutatavaid välisseadmeid ning teha nende tõrkeotsingut. Saate kasutada välisseadme simulaatorit jaemüügi välisseadmete testimise hõlbustamiseks ja valest seadistusest või rikkis seadmedraiveritest põhjustatud probleemide isoleerimiseks. Välisseadme simulaator sisaldab töölauaprogrammi, mis pakub Dynamics 365 for Operationsi jaemüügi mooduli toetatavate seadmete virtuaalseid versioone. Iga virtuaalse seadme jaoks mõeldud sektsioon näitab seadme ja jaemüügikassa vahelist suhtlust. Saate kasutada seda ka mitmesuguste kassastsenaariumide puhul kehtiva sisendi jaoks. Välisseadme simulaator toetab kassa ja järgmiste virtuaalsete seadmete vahelist suhtlemist.

-   **Printer** – välisseadme simulaator võib kuvada kassaprinteri jaoks konfigureeritud kviitungid.
-   **Ridade kuvar** – saate konfigureerida virtuaalse ridade kuvari nii, et see näitaks tegevusi füüsilisel ridade kuvaril.
-   **Magnetribalugeja (MSR)** – võite saata simuleeritud magnetriba sündmusi välisseadme simulaatorist kassasse.
-   **Sahtel** – saate füüsilist sularahasahtlit simuleerida.
-   **Sahtel 2** – seadistades välisseadme simulaatoris teise sularahasahtli, saate simuleerida stsenaariume, mis hõlmavad ühte kahe aktiivse vahetusega kassaregistrit.
-   **Skanner** – virtuaalne vöötkoodiskanner, mida välisseadme simulaator toetab, saab väljastada vöötkoodi skannimissündmusi.
-   **Kaal** – virtuaalne kaal võimaldab simuleerida kaalutud kaupade suhtlust kassaga.
-   **PIN-koodi (PIN-i) klahvistik** – saate simuleerida PIN-klahvistiku toiminguid. **Märkus.** Peate rakendama makseliidese kaudu füüsilise PIN-klahvistiku toe.
-   **Allkirja hõivamine** – välisseadme simulaator sisaldab virtuaalset allkirja hõivamise seadet, mille saate seadistada küsima allkirju, mis on mõningate maksevahendite puhul vajalikud, nt kliendi konto maksete puhul.

Välisseadme simulaatorit saab kasutada ka vöötkoodilugejast ja MSR-ist pärinevate klaviatuurikiilu sündmuste simuleerimiseks. Virtuaalne välisseadme simulaator toetab konkreetselt süsteemi Object Linking and Embedding for Retail POS (OPOS) seadmeid.

## <a name="key-scenarios"></a>Võtmestsenaariumid
### <a name="troubleshooting"></a>Tõrkeotsing

Saate kasutada välisseadme simulaatorit seadme seadistuse tõrkeotsinguks. Kui teil ei ole välisseadme simulaatorit või teist sama klassi seadet, võib olla raske määrata, kust probleemid pärinevad. Kuid kui teil on välisseadme simulaator, saate seadistada virtuaalseid seadmeid ja käitada samu kooditeid ja äriloogikaid, mida füüsiliste seadmete puhul kasutatakse. Välisseadme simulaatori vaatepunktist on virtuaalsete ja füüsiliste seadmete peamine erinevus hooldusobjekt või seadmedraiver. Füüsiliste seadmete puhul annab hooldusobjekti seadme tootja. Seevastu välisseadme simulaatori puhul antakse hooldusobjektid välisseadme simulaatori osana. Kui välisseadme simulaator töötab õigesti, siis kui seade ei tööta õigesti pärast seda, kui seadme nimi riistvaraprofiilis on muudetud tegeliku seadme nimeks, võite järeldada, et on probleem tootja antud hooldusobjektiga.

### <a name="training"></a>Koolitus

Saate kasutada välisseadme simulaatorit realistliku kihi lisamiseks kassapidaja koolitusele, kui füüsilist riistvaraseadistust ei saa kasutada. Kui välisseadme simulaator on koolitusstsenaariumi kaasatud, saab kassapidaja tõhusamalt kassaga suhelda, sisestades näiteks toote vöötkoodi skaneeringuid ja tõmmates läbi kinkekaarte ning vaadates, milliseid kviitungeid konkreetse kande puhul prinditakse.

### <a name="testing"></a>Testimine

Välisseadme simulaatori abil saab toote vöötkoode, kviitungivorminguid jne virtuaalses keskkonnas proovida, ilma et oleks vaja füüsilist keskkonda juurutada. Kuna füüsilist riistvara pole vaja ja te ei pea juurutama kassaklienti riistvarajaamas ega füüsilises arvutis, saate kontoris tehtud muudatusi kiiremini proovida.

## <a name="set-up-the-peripheral-simulator"></a>Välisseadme simulaatori seadistamine
### <a name="set-up-a-hardware-profile"></a>Riistvaraprofiili seadistamine

1.  Välisseadme simulaatori seadistamiseks klõpsake valikuid **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiilid** &gt; **Riistvaraprofiilid**.
2.  Uue profiili loomiseks klõpsake nuppu **Uus**.
3.  Sisestage väärtused väljadele **Profiili number** ja **Kirjeldus**.
4.  Kasutage järgmist tabelit testitavate virtuaalsete seadmete seadistamiseks. Siin on tabeli veergude selgitused.
    -   **Seade** – selles veerus on antud seadme seadistamiseks laiendatava kiirkaardi nimi.
    -   **Seadme tüüp** – selles veerus on väärtus, mille seadme nimega märgistatud väljalt valite.
    -   **Seadme nimi** – selles veerus on täpne väärtus, mille seadme nimeks sisestate. **Oluline!** Siin antud seadme nimed on kohustuslikud, kuna riistvarajaam kasutab neid konkreetseid nimesid seadmete poole pöördumiseks. Kui te neid konkreetseid nimesid ei kasuta, ei saa seadet kasutada.

    | Seade            | Seadme tüüp | Seadme nimi              |
    |-------------------|-------------|--------------------------|
    | Printer           | OPOS        | MockOPOSPrinter          |
    | Rea kuva      | OPOS        | MockOPOSLineDisplay      |
    | Magnetribalugeja               | OPOS        | MockOPOSMSR              |
    | Koostaja            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Skanner           | OPOS        | MockOPOSScanner          |
    | Sobita             | OPOS        | MockOPOSScale            |
    | PIN-klahvistik           | OPOS        | MockOPOSPinPad           |
    | Allkirja hõivamine | OPOS        | MockOPOSSignatureCapture |

**Märkus.** Vöötkoodilugejast ja MSR-ist pärinevate klaviatuurikiilu sündmuste simuleerimiseks pole mingit konkreetset riistvaraprofiili seadistust vaja.

### <a name="assign-the-hardware-profile-to-a-register"></a>Riistvaraprofiili määramine kassaaparaadile

1.  Pärast riistvaraprofiili loomist avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Registrid**.
2.  Klõpsake loendis **Kassaregistrid** väljal **Registrinumber** olevat linki, mille kaudu pääseb registri juurde, mis peaks välisseadme simulaatorit kasutama.
3.  Klõpsake valikut **Redigeeri**.
4.  Jaotises **Profiilid** väljal **Riistvaraprofiil** valige riistvaraprofiil, mille virtuaalsete välisseadmete jaoks lõite.
5.  Klõpsake käsku **Salvesta**.

### <a name="synchronize-changes-to-the-channel-database"></a>Muudatuste sünkroonimine kanaliandmebaasiga

1.  Avage **Jaemüük ja kaubandus** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**.
2.  Valige jaotusgraafik **1090**.
3.  Kassa muudatuste sünkroonimiseks klõpsake valikut **Käivita kohe**.

Pärast andmete sünkroonimist on uus riistvaraprofiil ja registri muudatused kanali andmebaasis saadaval.

## <a name="install-the-peripheral-simulator"></a>Välisseadme simulaatori installimine
1.  Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiilid** &gt; **Riistvaraprofiilid**.
2.  Klõpsake valikut **Allalaadimine** ja seejärel valikut **Välisseadme simulaator**. **Märkus.** Enne välisseadme simulaatori allalaadimist tuleb hüpikublokk välja lülitada.
3.  Kui allalaadimine on lõppenud, avage kaust **Allalaadimised** ja tehke installiprogrammi käivitamiseks topeltklõps failil **VirtualPeripherals.msi**.
4.  Installige välisseadme simulaator vaikesätetega.

Lisaks välisseadme simulaatorile peate installima ettevõtte Monroe Consulting Services üldised juhtimisobjektid. Muidu ei tööta välisseadme simulaator õigesti. Üldiste juhtimisobjektide allalaadimiseks minge lehele <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Välisseadme simulaatori kasutamine
Välisseadme simulaatori käivitamiseks klõpsake arvutil nuppu **Start**, sisestage **Jaemüügi välisseadme stimulaator** ja valige siis rakendus, kui see otsingutulemustes kuvatakse. Pärast välisseadme simulaatori käivitamist klõpsake seadme nime toetatud seadmete vaatamiseks. Seadmed on loetletud vahekaartidena akna vasakul poolel. Konkreetse seadme vaatamiseks klõpsake selle seadme vahekaarti.

### <a name="line-display-capabilities"></a>Ridade kuvari võimalused

Ridade kuvar on esimene seade, mis on välisseadme simulaatori nimekirjas. Kui virtuaalne ridade kuvar on konfigureeritud, näitab see kassakandes skannitud reaüksusi. Lisaks reaüksustele näitab kuvar kogusummat, mis tasuda tuleb, kui kassas maksevahend valitakse. Samuti näitab see tasumisele kuuluvat saldot, kui sisestatakse maksevahend, kuid kande saldo on endiselt tasumata. Kui kassat ei kasutata, võib kuvada teate, mis näitab, et kassasahtel on suletud. teate saab konfigureerida riistvaraprofiili kiirkaardil **Ridade kuvar**.

### <a name="cash-drawer-capabilities"></a>Sularahasahtli võimalused

Sularahasahtel on teine seade, mis on välisseadme simulaatori nimekirjas. Kui riistvaraprofiil on konfigureeritud kasutama virtuaalseid sularahasahtleid, avab kassa toimingute (nt maksevahendi deklareerimise) korral aktiivse vahetuse sularahasahtli ja kassapidaja saab tavaliste sularahatehingute korral raha tagasi anda või sahtlisse panna. Virtuaalsetel sularahasahtlitel on sildid **Põhisahtel** ja **Sekundaarne sahtel**. Need sildid kajastavad riistvaraprofiilis vastavalt valikuid Sahtel ja Sahtel 2. Kui sahtel on suletud, siis kuvatakse suletud sularahasahtli pilt ja suletud sularahasahtli nupul on silt **Ava sahtel**. Selle nupu klõpsamisel asendatakse pilt avatud sularahasahtli pildiga, mis näitab, et sahtel on nüüd lahti. Lahtise sularahasahtli nupul on silt **Sule sahtel**. Mitu kassatoimingut võivad põhjustada sularahasahtli avanemise. Enamik toiminguid ei saa jätkuda, kui sularahasahtel on lahti. Erandiks on mõned päeva lõpu protseduurid. Kui kassa kasutaja saab tõrketeate, mis ütleb, et toimingut ei saa teha, kui sularahasahtel on lahti, peab kasutaja jätkamiseks virtuaalse või füüsilise sularahasahtli sulgema. Kui sularahasahtel on riistvaraprofiilis märgistatud kui **Ühine**, siis ei kontrolli süsteem enne toimingut, kas sahtel on kinni. Toiming jätkub tavalisel viisil, isegi kui sularahasahtel on lahti. Selline käitumisviis toetab stsenaariume, kus müüjad kasutavad samu sularahasahtleid ja kus üks müüja kasutab sularahasahtlit, sel ajal kui teine müüja teeb oma kassaseadmed muid toiminguid. Sularahasahtlile tehtud muudatusi pole näha enne jooksva vahetuse sulgemist ja uue vahetuse avamist.

### <a name="msr-capabilities"></a>MSR-i võimalused

Välisseadme simulaator pakub tõhusat virtuaalsete MSR-i toimingute tuge, töötades OPOS-i režiimis või klaviatuuri kiilu režiimis. OPOS-i režiim nõuab, et MSR oleks konfigureeritud toimima riistvaraprofiilis OPOS-i seadmena. Klaviatuurikiilu režiim saadab lihtsalt klaviatuurikiilu andmete sündmused Microsoft Windowsi. Lisaks seadistuse erinevustele erinevad OPOS-i ja klaviatuurikiilu režiimid järgmiselt.

-   Kassaklient aktiveerib OPOS-i MSR-i seadmed konkreetsete stsenaariumide puhul, näiteks stsenaariumid, mis lubavad püsikliendi- või kinkekaardi sisestamisel magnetriba andmeid.
-   Klaviatuurikiilu režiimis saadab välisseadme simulaator klaviatuurikiilu andmed väljale, mis on andmete saatmise ajal aktiivne. See sarnaneb olukorrale, kus andmed sisestatakse klaviatuuri kaudu. MSR-i kasutamiseks klaviatuurikiiluna peab kasutaja lülituma ümber Retail Modern POS-i (MPOS-i), veendumaks, et andmed õigel väljal vastu võetakse. Seega saate konfigureerida viivituse, et kasutajal oleks aega veenduda, et andmed on saadetud õigele väljale.

#### <a name="testing-gift-and-payment-card-swipes"></a>Kinke- ja maksekaarditõmmete proovimine

Virtuaalne MSR, mida välisseadme simulaator pakub, võimaldab konfigureerida ka konkreetseid MSR-i andmeid kinke- ja maksekaarditõmmete stsenaariumide proovimiseks. Kaardi loomiseks klõpsake plussmärgi (**+**) nuppu ja valige kaardi tüüp. Seejärel määrake kaardi number või jälgimisandmed, mis tuleks kassasse saata, koos määratletava kaardi aegumise kuu ja aastaga. Väljal **Kaardi tüüp** valitav väärtus on ainult silt, mille saab kaardiga vastendada. See silt muudab kaartide tuvastamise lihtsaks, kui neid läbi välisseadme simulaatori tõmmatakse. Saate valida välisseadme simulaatoris konfigureeritud kaarte vasaknoole (**&lt;**) ja paremnoole (**&gt;**) nuppudega kaardi pildi kohal. Kaarte saab redigeerida ja kustutada nuppudega **Redigeeri** ja **Kustuta** plussmärgi (**+**) nupu kõrval.

### <a name="pin-pad"></a>PIN-klahvistik

Saate OPOS-i PIN-klahvistiku simuleerimiseks PIN-klahvistiku simulaatori konfigureerida. Kui kassas tehakse elektroonilise ülekandega (EFT) kanne, mis nõuab PIN-koodi sisestamist, võtab riistvarajaam PIN-i seadmega ühendust, et küsida PIN-i sisestamist. Toimimiseks nõuab välisseadme simulaatori PIN-klahvistik EFT makseliidese tuge.

### <a name="printer"></a>Printer

Virtuaalse välisseadme printer kuvab lihtsalt kviitungid nii, nagu need kassast prinditakse. Kui printimistoimingu tulemusena tekib mitu kviitungit, saate kviitungite vahel kerida.

#### <a name="configure-receipt-printing"></a>Kviitungite printimise konfigureerimine

1.  Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiilid** &gt; **Riistvaraprofiilid**.
2.  Valige riistvaraprofiil, mille virtuaalsetele välisseadmetele lõite.
3.  Klõpsake kiirkaardil **Printer** nuppu **Redigeeri**.
4.  Valige väljalt **Kviitungi profiili ID** kviitungi profiil.
5.  Klõpsake käsku **Salvesta**.

### <a name="scale"></a>Sobita

Kui kassakandesse lisatakse kaalutoode ja kaal on konfigureeritud, toob kassa kaalumisseadmelt kaalu. Nii virtuaalse kui ka füüsilise kaalu puhul tuleb enne toote kandesse lisamist määrata toode või kaal. Enne kaalutoote lisamist kandesse minge välisseadme simulaatoris kaalu juurde ja kasutage plussmärki (**+**) ning miinusmärki (**–**) kaalu registreerimiseks, mida kaal peaks näitama. Võite sisestada soovitud kaalu ka otse väljale **Praegune väärtus**. Kaaluühikute reguleerimiseks kasutage plussmärki (**+**) ning nuppe **Redigeeri** ja **Kustuta**. Nii saab ühikuid määrata kaalutavate toodete või kaalu kasutamise lokaadi põhjal.

#### <a name="configure-a-scale-product"></a>Kaalutoote konfigureerimine

1.  Tehke valik **Jaemüük ja** **kaubandus** &gt; **Tooted ja kategooriad** &gt; **Väljastatud tooted kategooria järgi**.
2.  Avage toote kirje.
3.  Valige kaalutav toode.
4.  Määrake kiirkaardil **Jaemüük** valiku **Kaalutoode** väärtuseks **Ei** asemel **Jah**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Muudatuste sünkroonimine kanaliandmebaasiga

1.  Avage **Jaemüük ja kaubandus** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**.
2.  Valige jaotusgraafik **1040**.
3.  Kassa muudatuste sünkroonimiseks klõpsake valikut **Käivita kohe**.

Kui kassakandele lisatakse pärast andmete sünkroonimist kaalutoode, kontrollib kassa kaalult kaalu.

### <a name="signature-capture"></a>Allkirja hõivamine

Virtuaalne allkirja hõivamise seade palub kasutajal anda virtuaalsele allkirja hõivamise plaadile allkiri, kui kasutatav maksevahend nõuab allkirja. Kasutaja saab allkirja kassas kuvamiseks aktsepteerida. Seejärel saab kassapidaja allkirja aktsepteerida. Siis salvestatakse allkiri koos maksevahendiga ja see sünkroonitakse kontoriga koos muude kandeandmetega.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Maksevahendi seadistamine allkirja nõudma

1.  Avage **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Jaekauplused** &gt; **Kõik jaekauplused**.
2.  Valige jaekauplus.
3.  Klõpsake valikut **Redigeeri**.
4.  Klõpsake nuppu **Seadistus** ja seejärel klõpsake jaotises **Seadistus** valikut **Makseviisid**.
5.  Klõpsake valikut **Redigeeri**.
6.  Valige makseviis, mis nõuab allkirja.
7.  Määrake jaotises **Üldine** pealkirja **Allkirja hõivamine** all valiku **Allkirja hõivamise seadme kasutamine** väärtuseks **Jah**.
8.  Sisestage väljale **Allkirja hõivamise miinimumsumma** minimaalne summa, mis peaks allkirja hõivamise käivitama.

#### <a name="synchronize-changes-to-the-channel-database"></a>Muudatuste sünkroonimine kanaliandmebaasiga

1.  Avage **Jaemüük ja kaubandus** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**.
2.  Valige jaotusgraafik **1070**.
3.  Kassa muudatuste sünkroonimiseks klõpsake valikut **Käivita kohe**.

Kui andmed on sünkroonitud, siis kui kasutatakse allkirja nõudvat maksevahendit ja summa vastab allkirjalävele, küsib kassa virtuaalsel allkirja hõivamise seadmel allkirja.

## <a name="additional-configuration"></a>Täiendav konfiguratsioon
Saate redigeerida välisseadme simulaatori konfiguratsioonifaili, et katsetatavaid stsenaariume sobivamalt käsitleda. Leiate konfiguratsioonifaili järgmisest kohast: C:\\Programmifailid (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfiguratsioonifail määratleb üksused, mis on kaalul katsetamiseks saadaval, katsetamiseks saadaolevad kaarditüübid ja vöötkooditüübid. Näiteks konfiguratsioonifailis tekstiväärtusi muutes saate lisada uue kaarditüübi või mõõtühiku, mida saab käitusajal valida. Uued väärtused kuvatakse pärast rakendust taaskäivitamist.

## <a name="troubleshooting"></a>Tõrkeotsing
Välisseadme simulaatori tegevused logitakse välisseadme simulaatoris. Leiate logi järgmisest kohast: C:\\Programmifailid (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Välisseadme simulaator lisab probleemid ka Windowsi sündmuste logisse, millele pääsete juurde asukohas **Rakenduste ja teenuste logid** &gt; **Microsoft** &gt; **DynamicsAX**. Kui riistvaraprofiilile või muudele aladele tehtud muudatused pole näha, kui MPOS-i või välisseadme simulaatorit kasutate, siis vaadake jaotuse andmeedastaja töid, mida kasutasite andmete sünkroonimiseks kanaliandmebaasiga. Kui muudatused sünkrooniti, kuid neid pole kassas sellegipoolest näha, siis taaskäivitage kassaklient. Konfigureeritud kassasahtlite muudatused ei jõustu enne uue vahetuse loomist. Seega, kui teete sularahasahtlites muudatusi, siis veenduge, et sulgeksite uue sularahasahtli seadistuse katsetamiseks alati olemasoleva vahetuse. Mõnikord, kui pärast ettevõtte Monroe Consulting Services üldisi juhtimisobjekte installitakse tootja draiver, võib draiver takistada üldiste juhtimisobjektide õiget töötamist. Sellisel juhul tuleks üldised juhtimisobjektid uuesti installida.

<a name="see-also"></a>Vt ka
--------

[Jaemüügi välisseadmete ülevaade](retail-peripherals-overview.md)




