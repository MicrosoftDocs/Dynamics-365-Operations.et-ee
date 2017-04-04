---
title: "Jaemüügi perifeerne simulaatori"
description: "Selles teemas on perifeerne simulator vahend, mis on kaasas Microsoft Dynamics 365 toiminguteks - jaemüük."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Jaemüügi perifeerne simulaatori

Selles teemas on perifeerne simulator vahend, mis on kaasas Microsoft Dynamics 365 toiminguteks - jaemüük.

<a name="overview"></a>Ülevaade
--------

Operatsioonide - 365 Microsoft Dynamics jaemüügi perifeerne simulator on vahend, mis aitab teil luua, katsetada ja tarvikud, mida kasutatakse jaemüügi keskkondade tõrkeotsing. Kasutage perifeerne simulator täiustamiseks, välisseadmete jaemüük katsetamine ja isoleerida küsimusi, mis on tingitud vale seadistus või rikutud seadmedraiverid. Perifeerne simulator sisaldab töölauaprogramm, mis pakub virtuaalne versioonid seadmed selle Dynamics 365 toiminguteks - jaemüügi toetab. Sektsiooni iga virtuaalse seadme tulemused näitavad seadme ja retail Müügikoht (POS) vahel. Ka kasutamist aitab sobivat erinevaid POS stsenaariume. Perifeerne simulator toetab tootjaorganisatsioonid ja virtuaalne järgmisi seadmeid:

-   **Printeri** – perifeerne simulaator saate Näita sissetulekuid, POS printer jaoks konfigureeritud.
-   **Line kuva** – saate konfigureerida virtuaalse rea ekraanile, tegevus füüsilise rea Kuva.
-   **Magnetriba lugeja (MSR)** – saate saata simuleeritud magnetriba sündmused tootjaorganisatsioonid: perifeerne simulaator.
-   **Sahtlis** – simuleerimist sularaha sahtlis.
-   **Sahtel 2** – teise rahasahtli perifeerne simulaatori luues saate simuleerida stsenaariumid, mis on seotud ühtse POS registri, millel on kaks aktiivset vahetust.
-   **Skanneri** – perifeerne simulator toetab virtuaalne vöötkoodilugejaga anda vöötkood skannimine sündmused.
-   **Skaala** – virtuaalne skaala võimaldab simuleerida kaalutud üksuste suhtlemist tootjaorganisatsioonid.
-   **Isiklik ID number (PIN) pad** – simuleerimist PIN pad toiminguid. **Märkus:** tuleb rakendada füüsilise PIN pad kaudu makse connector toetus.
-   **Allkirja kogumise** – perifeerne simulator sisaldab virtuaalne allkiri sidumise seadmega saate seadistada küsima allkirjad, mis on vajalikud mõned pakkumised, nt kliendi konto maksed.

Perifeerne simulaatori abil saate simuleerida klaviatuuri kiilu sündmused, mis pärinevad vöötkoodilugejaga ja MSR. Perifeerne virtuaalne simulaator toetab spetsiaalselt Object Linking and Embedding Retail POS (OPOS) seadmed.

## <a name="key-scenarios"></a>Stsenaariumid
### <a name="troubleshooting"></a>Tõrkeotsing

Kasutage perifeerne simulator tõrkeotsingu seadistus. Kui teil perifeerne simulator või teine seade sama liiki, see võib olla raske kindlaks teha, kui küsimusi on pärit. Aga kui teil on perifeerse simulaator, saate luua virtuaalne seadmed, ja sama koodi teed ja äriloogikat, mida kasutatakse reisijate liftid. Perifeerne simulator küljest virtuaalne seadmed ja füüsiliste seadmete peamine erinevus on objekti või seadme draiver. Füüsilise seadmete jaoks on teenuse objekt pakub seadme tootja. Seevastu perifeerne Simulator teenuse objektid on olemas osa perifeerse simulaatori. Kui perifeerne simulator töötab õigesti, kui seade ei tööta õigesti riistvaraprofiili seadme nimetus on muutunud otse seadme nimi, siis võib eeldada, on olemas tootja esitatud objekti küsimus.

### <a name="training"></a>Koolitus

Perifeerne simulaatori abil saate lisada realistlik tugipadjad Sirje koolitus kui füüsilise riistvara häälestamine ei ole saadaval. Kui perifeerne simulator sisaldab koolitust stsenaariume, kassapidaja tõhusamalt suhelda tootjaorganisatsioonid ette näha sisend nagu toote kood skaneerib ja kingitus kaardi swipes ning jälgides, millised sissetulekud on trükitud konkreetse kande.

### <a name="testing"></a>Testimine

Perifeerne simulaatori abil saate testida toote koodi, tarne formaate ja nii edasi, ilma et Juurutage füüsilise riistvara virtuaalkeskkonnas. Sest füüsilise riistvara ei ole nõutav, ja pole vaja kasutada POS kliendi riistvara station või füüsiline arvuti, saad kiiremini tagasi kontoris tehtud katse muudatused.

## <a name="set-up-the-peripheral-simulator"></a>Saate seadistada perifeerne simulaatori
### <a name="set-up-a-hardware-profile"></a>Riistvara seadistamisel

1.  Perifeerne koeraga seadmiseks avage **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara profiilid**.
2.  Uue profiili loomiseks klõpsake **uus**.
3.  Sisestage väärtused on **profiili numbrit** ja **kirjeldus** väljad.
4.  Järgnev tabel abil saate seadistada virtuaalne seadmed, mida peab katsetama. Siin on selgitus tabeli veerud:
    -   **Seadme** – selles veerus annab seadme seadistamiseks laienevaid FastTab nime.
    -   **Seadme tüüp** – selles veerus annab nimeks on seadme nime väljal väärtus.
    -   **Seadme nimi** – selles veerus annab täpne väärtus, mida saate seadme nime. **Tähtis:** seadmete nimed, mis antakse siin nõutakse, riistvara station kasutab need konkreetsed nimed seadmed tegeleda. Kui kasutate neid konkreetseid nimesid, seadet ei saa kasutada.

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

**Märkus:** pole täpne seadistus riistvaraprofiili on vaja simuleerida klaviatuuri kiilu sündmused vöötkoodilugejaga ja MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Määrata riistvaraprofiili registri

1.  Riistvara profiili on loodud, avage **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**registreerib**.
2.  Aastal ning **POS registrite** klõpsake linki selle **reg. nr** lahter, kas tuleks kasutada perifeerse simulaator.
3.  Klõpsake valikut **Redigeeri**.
4.  Aastal ning **profiilid** osa, on **riistvaraprofiili** number virtuaalne välisseadmete jaoks loodud riistvara profiili,.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Sünkroniseerida kanali andmebaasi muudatused

1.  Mine **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**.
2.  Valige selle **1090** jaotus ajakava.
3.  Klõpsake **praegu käivitada** sünkroonida muudatused tootjaorganisatsioonid.

Pärast olevad andmed on saadaval kanali andmebaasi uue riistvara profiili ja muutusi registrisse.

## <a name="install-the-peripheral-simulator"></a>Paigaldada perifeerne simulaatori
1.  Mine **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara profiilid**.
2.  Klõpsake **lae**, ja seejärel klõpsake **PeripheralSimulator**. **Märkus:** pop-up blokaatorid peate lülitama enne allalaadimist perifeerne simulaator.
3.  Pärast seda, kui allalaadimine on lõpule jõudnud, avage selle **Downloads** kaust ja topeltklõpsake **VirtualPeripherals.msi** installiprogrammi käivitamiseks.
4.  Installida perifeerne simulaatori abil.

Lisaks perifeersete simulaator, installige ühise kontrolli objektid: Monroe nõuandeteenuseid. Vastasel korral perifeersete simulator ei tööta õigesti. Ühise kontrolli objektid, minge <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Perifeerne simulaatori abil
Perifeerne simulator alustamiseks klõpsake **alustada** arvutisse, tippige **jaemüügi perifeerne simulaatori**, ja seejärel valige rakendus, kui see ilmub otsingutulemustes. Perifeerne simulator alustamisele klõpsake seadme nime nägemiseks toetatud. Need seadmed käskudena vahekaartide akna vasakus servas. Kindla seadme vaatamiseks klõpsake vahekaarti seadme jaoks.

### <a name="line-display-capabilities"></a>Line kuvafunktsioonid

Line ekraan on esimene seade, mis on loetletud perifeerne simulaatori. Kui virtuaalne rea Kuva konfiguratsioonisätted, see näitab kirjeid nad kontrollitakse POS tehinguga. Lisaks üksusi, kuvatakse kokku, mis tõttu kell tootjaorganisatsioonid pakkumise valimisel. See näitab ka tasakaalu, mis on tingitud kui pakkumine on kantud, kuid on ikka tehingu eest. Kui tootjaorganisatsioonid ei kasutata, saate sõnumi tähis, mis näitab, et kuni on suletud. Peate konfigureerima sõnum on **Line Kuva** riistvaraprofiili FastTab.

### <a name="cash-drawer-capabilities"></a>Raha sahtlis võimeid

Raha sahtlis on teine seade, mis on loetletud perifeerne simulaatori. Riistvara profiili konfigureerimisel kasutada virtuaalse Kassasahtlid tootjaorganisatsioonid avab aktiivse shift rahasahtli vastuseks sahtlis toiminguid nagu pakkumise deklaratsioonid, ning et kassast teha, muuta või sularaha standard cash-and-carry tehingute puhul. Virtuaalne Kassasahtlid on sildid **Main sahtlis** ja **teisese sahtlis**. Neid silte esindada sahtel ja sahtli 2 riistvaraprofiili, vastavalt. Kui on suletud sahtlis ja suletud rahasahtli pilt kuvatakse suletud rahasahtli nupuga on märgistatud **avatud sahtlis**. Kui klõpsate seda nuppu, pilt asendatakse pildi avatud rahasahtli näitamaks, et sahtel on nüüd avatud. Kohta avatud rahasahtli nupp kirjaga **tiheda sahtlis**. Mitmel tegevusel kell tootjaorganisatsioonid võivad põhjustada rahasahtli avamine. Enamik toiminguid ei saa alustada, kui raha sahtlis on avatud. Erandiks on mõned päeva korda. Kui POS kasutaja saab tõrketeade, mis teatab toiming takistab raha sahtlis on avatud, suletakse kasutaja, virtuaalsed või füüsilise rahasahtli jätkamiseks. Kui raha sahtlis on märgitud **jagatud** riistvara profiili, süsteem ei kinnita, et sahtel on suletud enne operatsiooni. Operatsiooni edasi nagu tavaliselt, isegi raha sahtlis on avatud. Selline käitumine toetab stsenaariumid müük sidusettevõtete vahel jagunevad Kassasahtlid ja kui üks sidusettevõte kasutab raha sahtlis, kui teise sidusettevõtte hõlmab sõltumatute toiminguid oma POS seadmes. Muudatused, mis tehakse raha sahtlis ei ole ilmne praeguse shift on suletud ja avatakse uus nihe.

### <a name="msr-capabilities"></a>MSR võimeid

Perifeerne simulator toetab tugev virtuaalne MSR toimingute toimub kas OPOS mode või klaviatuur kiilu. OPOS režiim nõuab, et liitmise seadistada riistvaraprofiili OPOS seade tööle. Klaviatuuri kiilu režiimis saadab lihtsalt klaviatuuri kiilu andmete sündmused Microsoft Windows. Lisaks erinevustele setup, erinevad OPOS ja klaviatuuri kiilu transpordiliikide järgmiselt:

-   POS client võimaldab OPOS MSR seadmed teatud olukordades, nagu stsenaariumid, mis võimaldavad lojaalsus või kingitus selles kaardi magnetriba andmed.
-   Klaviatuuri kiilu režiimis, perifeerne simulator saadetakse klaviatuuri kiilu andmed välja, mis on aktiivne, kui andmete edastamist. Selline käitumine meenutab käitumist, mis ilmneb siis, kui on sisestatud klaviatuuri kasutades. Kasutada liitmise klaviatuuri kiilu, peab kasutaja et jaemüügi kaasaegne POS (MPOS) veendumaks, et edastatakse õiged välja vahetada. Seetõttu saate konfigureerida viivitus, nii, et kasutaja on aega veendumaks, et andmed saadetakse õigele väljale.

#### <a name="testing-gift-and-payment-card-swipes"></a>Testimise kingitus ja makse kaart swipes

Virtuaalne MSR, mis perifeerne simulaator annab ka laseb teil konfigureerida MSR andmed, mida testida stsenaariumid kingitus ja makse kaardi swipes. Kaardi loomiseks klõpsake (**+**) nuppu ja valige kaardi tüüp. Seejärel määrake kaardi number või jälgida andmeid, mis tuleb saata POS lõppemise kuu ja aasta määratlete kaardi koos. Väärtus, mille valite selle **kaardi tüüp** on lihtsalt silt, mida saab vastendada kaardi. See silt on lihtsam tuvastada kui nad on swiped kaudu perifeerne simulaatori kaardid. Valige kaardid, mis on konfigureeritud perifeerne simulaatori vasaknoolt (**&lt;**) ja paremnoolt (**&gt;**) nuppe kaardi pildi kohal. Saate redigeerida ja kustutada kaarte ning **muuta** ja **kustutada** nuppu kõrval plussmärki (**+**) nuppu.

### <a name="pin-pad"></a>PIN-klahvistik

Saate konfigureerida PIN pad simulator simuleerida OPOS PIN pad. Kui elektrooniliste vahendite üleandmine (EFT) kanne tehakse tootjaorganisatsioonid ja nõuab PIN-kood, riistvara station nõuab PIN seadme PIN-koodi sisestamiseks. Töötada, nõuab PIN pad perifeerne simulaatori EFT makse connector toetust.

### <a name="printer"></a>Printer

Perifeerne virtuaalse printeri lihtsalt näitab sissetulekute, kui nad on prinditud tootjaorganisatsioonid. Kui printimise toiming mitme sissetuleku, saate kerida laekumistest.

#### <a name="configure-receipt-printing"></a>Konfigureerida kviitungi trükkimiseks

1.  Mine **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara profiilid**.
2.  Valige loodud virtuaalne välisseadmete jaoks riistvara profiili.
3.  Kohta ning **Printer** FastTab, klõpsake **muuta**.
4.  Aastal ning **kviitungi profiili ID** profiili kviitungi number,.
5.  Click **Save**.

### <a name="scale"></a>Sobita

Kui skaala toode lisatakse POS tehingu ja skaalal on konfigureeritud, toob tootjaorganisatsioonid kaalu skaala. Nii virtuaalse ja füüsilise skaala, toote või kaal tuleks sätestada enne toote lisatakse kande. Skaala toote lisada tehingule, minge perifeerne simulaatori skaala ja kasutada pluss märki (**+**) ja miinusmärgiga (**-**) skaala teatama kaalu reguleerimiseks nuppe. Saate sisestada ka otse soovitud kaalu ning **praeguse väärtuse** välja. Kohandage kaalu skaala üksuste abil plussmärki (**+**), **muuta**, ja **kustutada** nupud. Nii saab määrata üksused, kaalutakse tooteid või kui skaala kasutatakse lokaadi.

#### <a name="configure-a-scale-product"></a>Konfigureerige toote skaala

1.  Mine **jaemüügi ja****kaubanduse**&gt;**toodete ja kategooriate**&gt;**vabastatud toodete kategooria**.
2.  Avage toote kirje.
3.  Valige toode kaaluda.
4.  Kohta ning **jaemüügi** FastTab, seada selle **skaala toote** valik **nr** et **Jah**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Sünkroniseerida kanali andmebaasi muudatused

1.  Mine **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**.
2.  Valige selle **1040** jaotus ajakava.
3.  Klõpsake **praegu käivitada** sünkroonida muudatused tootjaorganisatsioonid.

Pärast seda, kui andmed sünkroonitakse skaala toote lisamisel POS tehingu, kontrollib tootjaorganisatsioonid kaalu skaala.

### <a name="signature-capture"></a>Allkirja hõivamine

Virtuaalne allkiri hõiveseade kasutajalt esitamist allkirja virtuaalne allkirja kogumise pad kasutatakse pakkumusega nõuab allkirja. Kasutaja nõustub Näita seda tootjaorganisatsioonid allkiri. Seejärel nõustub kassapidaja allkiri. Allkirja salvestatakse seejärel koos pakkumusega ja tagakontori koos muu tehingu, sünkroonitakse.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Seadistatud pakkumise allkirja

1.  Mine **hulgi- ja kaubanduse**&gt;**kanalite**&gt;**kauplustes**&gt;**kõik kauplustes**.
2.  Valige kauplusesse.
3.  Klõpsake valikut **Redigeeri**.
4.  Klõpsake **loodud**, ja siis, selle **loodud** käsul **makseviisid**.
5.  Klõpsake valikut **Redigeeri**.
6.  Valige makseviis, mis nõuab allkirja.
7.  Linnas on **üldise** jagu alla **allkirja lüüa**, seada ning **kasutada allkirja hõiveseade** võimalus **Jah**.
8.  Aastal ning **allkirja kogumise miinimumsumma** sisestage miinimumsumma, mis käivitab allkirja lüüa.

#### <a name="synchronize-changes-to-the-channel-database"></a>Sünkroniseerida kanali andmebaasi muudatused

1.  Mine **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**.
2.  Valige selle **1070** jaotus ajakava.
3.  Klõpsake **praegu käivitada** sünkroonida muudatused tootjaorganisatsioonid.

Pärast seda, kui andmed on sünkroonitud, kui pakkumise kasutatakse allkirja nõudva ja summa vastab allkirja künnis, küsib tootjaorganisatsioonid hõiveseade virtuaalne allkiri allkiri.

## <a name="additional-configuration"></a>Seadistused
Te saate perifeerne simulator konfiguratsioonifaili asjakohasemalt käsitleda stsenaariumid, mida sa testida. Leiad konfiguratsiooni faili C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfiguratsioonifaili määratleb seadmeid, mis on skaala, mis on kontrollida tüüpi kaarte ja vöötkooditüübid kontrollida. Näiteks muutes teksti väärtused konfiguratsioonifaili, saate lisada uue kaardi tüüp või mille valimist käivitamise ajal. Uued väärtused kuvatakse pärast rakenduse taaskäivitamist.

## <a name="troubleshooting"></a>Tõrkeotsing
Perifeerne Simulator tegevus on sisseloginud jooksul perifeerne simulaator. Leiad Logi C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Perifeerne simulator aru probleemid Windowsi sündmustelogis, millele pääseb kell **rakenduste ja teenuste logid**&gt;**Microsoft**&gt;**DynamicsAX**. Kui riistvaraprofiili või muudes valdkondades tehtud muudatused pole ilmne, MPOS või perifeerne simulator, pöörduge jaotus Toiminguajasti töökohti, millega sünkroonida andmebaasi kanal. Kui muudatused sünkroonitud, kuid veel ei ilmne tootjaorganisatsioonid, taaskäivitage klient POS. Konfigureeritud Kassasahtlid muudatused ei ole tõhus kuni uue shift on loodud. Seetõttu, kui muudate Kassasahtlid, veenduge, et katsetada uue raha sahtlis seadistamine olemasolevate shift alati sulgeda. Mõnikord, kui tootja draiver on installitud pärast ühise kontrolli objektid: Monroe nõuandeteenuseid, juht võib põhjustada ühise kontrolli objektid õigesti töötamise. Sel juhul peaks uuesti ühise kontrolli objektid.

<a name="see-also"></a>Vt ka
--------

[Retail peripherals overview](retail-peripherals-overview.md)


