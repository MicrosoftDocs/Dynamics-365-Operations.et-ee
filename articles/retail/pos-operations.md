---
title: "Ühendusega ja ühenduseta kassatoimingud"
description: "See teema kirjeldab üksikasjalikult Microsoft Dynamics 365 for Retaili kassaoperatsioone. See kirjeldab, millises rakenduse osas saab operatsioone käivitada ning kas need on saadaval ka ühenduseta režiimis."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 58653d6e991f1896673a07e3057bd516c74edd76
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="online-and-offline-point-of-sale-pos-operations"></a>Ühendusega ja ühenduseta kassatoimingud

[!include [banner](includes/banner.md)]

Enamikku toiminguid, mida kasutaja kassas teeb, loetakse toiminguteks. Operatsioone konfigureeritakse ja hallatakse teenuse Microsoft Dynamics 365 for Retail kontoris. Paljud operatsioonid saab lisada kassa nupupaneeli nuppudele. Kasutajad saavad seejärel nuppude abil operatsioone käivitada ja nende funktsioone kasutada. Muud operatsioonid on osa kassa põhirakendusest ning need käivitatakse ekraanil kuvatavate nuppude abil või muude töövoogude või protsesside raames.

Järgmisest tabelist leiate üksikasjalikku teavet operatsioonide kohta, mis on saadaval Dynamics 365 for Retailile mõeldud Retail Modern POS-is ja Cloud POS-is. Samuti on tabelis märgitud, millises rakenduse osas saab operatsioone käivitada ning kas need on saadaval ka siis, kui kassa on ühenduseta režiimis.

Mõningad operatsioonid ei ole praegu Dynamics 365 for Retailile mõeldud Retail Modern POS-is või Cloud POS-i saadaval. Mõned neist operatsioonidest on lokaadipõhised ning nõuavad täiendavaid laiendeid ja konfigureerimist. Ülejäänud on Microsoft Dynamics AX 2012 funktsioonid, mida praegu ei toetata.

Järgmised veerud näitavad, kus operatsioone käivitatakse.

- **Nupupaneel**: operatsiooni saab määrata kassa nupupaneeli nuppudele, mis on osa kassa ekraanipaigutusest.
- **Kandeekraan**: operatsiooni saab käivitada kassa kandeekraanil konfigureeritud nupupaneeli nuppudega.
- **Tervitusekraan**: operatsiooni saab käivitada kassa tervitusekraanil konfigureeritud nupupaneeli nuppudega.

Märkus. Allpool loetletud toimingud kehtivad rakenduse Dynamics 365 for Retail uusimale versioonile. Mõned toimingud võivad olla muutunud või ei pruugi varasemates versioonides saadaval olla.

| ID | Toiming | Kirjeldus | Nupupaneel | Kandeekraan | Tervitusekraan | Ühenduseta saadaval | Lokaadipõhine |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Seadme aktiveerimine | Aktiveerige praegune seade, lubades autenditud kasutajal sisestada ühenduse teabe ning määrata seadme ja kassaaparaadi ID. | Ei | Ei | Ei | Ei | Ei |
| 134 | Lisa alluvus | Eelvalitud alluvuse lisamine kandele. Valige alluvus lehel **Nupu atribuudid**. | Jah | Jah | Ei | Jah | Ei |
| 135 | Lisa alluvus loendist | Lisage kandele alluvus, valides selle loendist. | Jah | Jah | Jah | Jah | Ei |
| 643 | Lisa kupongikood | Lisage kupong, sisestades kassasse selle koodi. | Jah | Jah | Ei | Jah | Ei |
| 117 | Kliendikaardi lisamine | Paluge kasutajal sisestada kliendikaardi number, mis lisatakse praegusesse kandesse. | Jah | Jah | Ei | Jah | Ei |
| 136 | Seerianumbri lisamine | See operatsioon võimaldab kasutajal määrata praegu valitud toote seerianumbri. | Jah | Jah | Ei | Jah | Ei |
| 1214 | Lisa tarneaadress | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 519 | Lisa kinkekaardile | Raha lisamine määratud kinkekaardile. | Jah | Jah | Ei | Ei | Ei |
| 6000 | Luba fiskaalüksuse registreerimise vahelejätmine | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 1212 | Raha hoiustamine panka | Panka saadetava rahasumma ja muu teabe, näiteks pangakoti numbri kirjendamine. | Jah | Jah | Jah | Jah | Ei |
| 923 | Pangasumma tõendamine | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 915 | Tühi toiming | See operatsioon kujutab endast kohandatavat nuppu, millele tarkvaraarendaja võib programmeerida äritegevuses vajaliku eritoimingu. | Jah | Jah | Jah | Jah | Ei |
| 1053 | Pimedalt suletud vahetus | Määrake praegune vahetus pimesi suletuks ja logige kasutaja välja. Pimesi suletud vahetus on täiendavate kannete jaoks suletud, ent avatud sahtliga seotud operatsioonide jaoks, nagu maksevahendite eemaldamine ja deklareerimine. | Jah | Jah | Jah | Ei | Ei |
| 310 | Kogusumma arvutamine | Kui allahindluse arvutamine hilineb, käivitab see operatsioon praeguse kande arvutuse. | Jah | Jah | Ei | Jah | Ei |
| 642 | Tarni kõik tooted | Määrake kõigi ridade tarneviisiks **Järeletulemine**. | Jah | Jah | Ei | Jah\* | Ei |
| 641 | Tarni valitud tooted | Määrake valitud ridade tarneviisiks **Järeletulemine**. | Jah | Jah | Ei | Jah\* | Ei |
| 1215 | Muuda parooli | Operatsioon võimaldab kassa kasutajal oma parooli muuta. | Jah | Jah | Jah | Ei | Ei |
| 123 | Muuda mõõtühikut | Muutke valitud rea kauba mõõtühikut. | Jah | Jah | Ei | Jah | Ei |
| 639 | Tühjenda kandest vaikemüügiesindaja | Eemaldage komisjonitasu müügigrupp (müügiesindaja) kandest. | Jah | Jah | Ei | Jah | Ei |
| 106 | Tühjenda kogus | Lähtestage valitud rea kogus väärtusele **1**. | Jah | Jah | Ei | Jah | Ei |
| 640 | Tühjenda realt müügiesindaja | Eemaldage komisjonitasu müügigrupp (müügiesindaja) praegu valitud realt. | Jah | Jah | Ei | Jah | Ei |
| 121 | Tühjenda väli Müüja | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 1055 | Sule vahetus | Sulgege praegune vahetus, printige Z-aruanne ja logige kasutaja süsteemist välja. | Jah | Jah | Jah | Ei | Ei |
| 925 | Pangatšeki kopeerimine | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 620 | Kliendi tellimuse loomine | Teisendage kassa kanne kliendi tellimuseks. | Jah | Jah | Ei | Jah\* | Ei |
| 621 | Loo pakkumine | Teisendage kassa kanne müügipakkumiseks. | Jah | Jah | Ei | Jah\* | Ei |
| 636 | Loo jaemüügikanne | See operatsioon võimaldab kasutajal luua standardse müügikande, kui kassa vaikekäitumine on klienditellimuste loomine. | Jah | Jah | Ei | Jah | Ei |
| 600 | Klient | Lisage kandesse konkreetne klient. | Ei | Ei | Ei | Jah | Ei |
| 1100 | Kliendikonto deposiit | Makse tegemine kliendi kontole. | Jah | Jah | Jah | Jah | Jah |
| 612 | Lisa klient | Operatsioon võimaldab kasutajal luua uue kliendikirje. | Jah | Jah | Jah | Jah† | Ei |
| 603 | Tühjenda väli Klient | Eemaldage klient praegusest tehingust. | Jah | Jah | Ei | Jah | Ei |
| 602 | Kliendi otsing | See operatsioon võimaldab kasutajal otsida kliendikirjet, navigeerides kassas kliendiotsingu lehele. | Jah | Jah | Jah | Jah | Ei |
| 609 | Kliendi kanded | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 917 | Andmebaasiühenduse olek | Operatsioon võimaldab kasutajal vaadata praeguse ühenduse sätteid ning vahetada ühendusega ja ühenduseta režiimide vahel. | Jah | Jah | Jah | Jah | Ei |
| 1200 | Deklareeri algsumma | Päeva või vahetuse alguses sahtlis oleva summa deklareerimine. | Jah | Jah | Jah | Jah | Ei |
| 132 | Deposiidi alistamine | Klienditellimuste vaikedeposiidi alistamine. | Jah | Jah | Ei | Jah\* | Ei |
| 913 | Keela kujundusrežiim | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 912 | Kujundusrežiimi lubamine | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 1217 | Komplektide osadeks jaotamine | Komplekti jaotamine komponenttoodeteks. | Jah | Jah | Jah | Jah | Ei |
| 624 | Kuva tagasimakse summad | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 513 | Kuva kogusumma | Kuvab kande kuvamine kliendikuval. | Jah | Jah | Jah | Jah | Ei |
| 623 | Muuda klienti | Muutke praeguse kliendi üksikasju. | Jah | Jah | Ei | Ei | Ei |
| 614 | Kliendi tellimuse redigeerimine | Kutsuge valitud tellimus tagasi, et seda saaks kassas muuta. | Ei | Ei | Ei | Ei | Ei |
| 615 | Redigeeri pakkumist | Kutsuge valitud pakkumine tagasi, et seda saaks kassas muuta. | Ei | Ei | Ei | Ei | Ei |
| 518 | Kulukontod | Sularahasahtlist juhuslike kulutuste jaoks eemaldatud raha kirjendamine. | Jah | Jah | Jah | Jah | Ei |
| 919 | Laiendatud sisselogimine | Määrake või eemaldage vöötkoodi skannimise või kaarditõmbega sisselogimise õigus. | Jah | Jah | Jah | Ei | Ei |
| 1201 | Sularaha sissemakse | See operatsioon võimaldab kasutajal praegusesse sahtlisse või vahetusse raha lisada. | Jah | Jah | Jah | Jah | Ei |
| 1218 | Ava perifeerseade sunniviisiliselt | Operatsiooni kasutatakse süsteemisiseselt kassa välisseadmete avamiseks. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 520 | Kinkekaardi saldo | Näitab kinkekaardi saldot. | Jah | Jah | Ei | Ei | Ei |
| 708 | Seadme inaktiveerimine | Inaktiveerige praegune seade, et seda ei saaks kasutada kassaaparaadina. | Ei | Ei | Ei | Ei | Ei |
| 517 | Tulukontod | Sularahasahtlisse muudel põhjustel (mitte müük) pandud raha kirjendamine. | Jah | Jah | Jah | Jah | Ei |
| 801 | Otsing varudest | Vaadake saadaolevat, tellimusse lisatud ja lubamiseks saadaval (ATP) olevaid koguseid praeguses kaupluses ja muudes saadaolevates asukohtades. | Jah | Jah | Jah | Ei | Ei |
| 122 | Arve kommentaar | See operatsioon võimaldab kasutajal sisestada praeguse kande kohta kommentaari. | Jah | Jah | Ei | Jah | Ei |
| 511 | Väljasta krediiditeatis | Väljastage krediiditeatis, et pakkuda tagasimakse asemel vautšerit. | Jah | Jah | Ei | Ei | Ei |
| 512 | Väljasta kinkekaart | Väljastage uus kinkekaart määratud summas. | Jah | Jah | Ei | Ei | Ei |
| 625 | Kliendikaardi väljastamine | Väljastage kliendikaart kliendile, et ta saaks osaleda kaupluse püsikliendiprogrammis. | Jah | Jah | Jah | Ei | Ei |
| 300 | Rea allahindluse summa | Kande rea kauba allahindluse summa sisestamine. Seda operatsiooni kasutatakse ainult allahinnatavate kaupade puhul ja ainult määratud allahindluse piires. | Jah | Jah | Ei | Jah | Ei |
| 301 | Rea allahindluse protsent | Kande rea kauba allahindluse protsendi sisestamine. Seda operatsiooni kasutatakse ainult allahinnatavate kaupade puhul ja ainult määratud allahindluse piires. | Jah | Jah | Ei | Jah | Ei |
| 703 | Lukusta register | Lukustage praegune kassaaparaat, et seda ei saaks kasutada, ent praegune kasutaja jääb sisselogituks. | Ei | Ei | Ei | Jah | Ei |
| 701 | Logi välja | Logige praegune kasutaja kassaaparaadist välja. | Jah | Jah | Jah | Jah | Ei |
| 521 | Kliendikaardi punktisaldo | Kuvab määratud kliendikaardi punktisaldo. | Jah | Jah | Ei | Ei | Ei |
| 918 | Vahetuste haldamine | Saate kuvada aktiivsete, peatatud ja pimedalt suletud vahetused. | Jah | Jah | Jah | Ei | Ei |
| 914 | Minimeeri kassa aken | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 1000 | Ava sahtel | Tehke ilma müügita toiming ja avage praegu valitud sularahasahtel. | Jah | Jah | Jah | Jah | Ei |
| 928 | Tellimuse täitmine | See toiming võimaldab kasutajatel tellimusi komplekteerida, pakkida, lähetada või tagasi kutsuda kauplusest kättesaamiseks. | Jah | Jah | Jah | Ei | Ei |
| 129 | Tühista rea toote maks | Tühistage valitud rea kauba maks ja valige muu määratud maks. | Jah | Jah | Ei | Jah | Ei |
| 130 | Tühista rea kauba maks loendist | Tühistage valitud rea kauba maks ja kasutage maksu, mille kasutaja loendist valib. | Jah | Jah | Ei | Jah | Ei |
| 127 | Kande maksu tühistamine | Tühistage kandel olev maks ja kasutage muud määratud maksu. | Jah | Jah | Ei | Jah | Ei |
| 128 | Kande maksu tühistamine loendist | Tühistage kandel olev maks ja kasutage maksu, mille kasutaja loendist valib. | Jah | Jah | Ei | Jah | Ei |
| 131 | Saateleht | Looge valitud tellimuse saateleht. | Ei | Ei | Ei | Ei | Ei |
| 710 | Ühenda riistvarajaam | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 201 | Tasumine kaardiga | Aktsepteerige maksmisel kaarte, nagu krediit- või deebetkaardid. | Jah | Jah | Ei | Jah | Ei |
| 200 | Tasumine sularahas | Maksmine sularahas. | Jah | Jah | Ei | Jah | Ei |
| 206 | Kiirtasumine sularahas | Viige kanne ühe puudutusega lõpule ja võtke tasutav summa sularahas vastu (täpne vahetusraha). | Jah | Jah | Ei | Jah | Ei |
| 204 | Tasumine tšekiga | Tšekiga maksmine. | Jah | Jah | Ei | Jah | Ei |
| 213 | Tasumise krediiditeatis | Võtke vastu kaupluse väljastatud krediiditeatis (vautšer). | Jah | Jah | Ei | Ei | Ei |
| 203 | Tasumise valuuta | Maksmine erinevates valuutades. | Jah | Jah | Ei | Jah | Ei |
| 202 | Tasumine kliendikontoga | Võtke kliendi kontolt kande eest tasu. Makseviis ei ole sobilik klienditellimuse deposiitide puhul. | Jah | Jah | Ei | Ei | Ei |
| 214 | Tasumine kinkekaardiga | Võtke vastu kaupluse väljastatud kinkekaart. | Jah | Jah | Ei | Ei | Ei |
| 207 | Maksa kliendikaardiga | Võtke vastu kliendikaardimakse ja lunastage punkte sobivate toodete soetamiseks. | Jah | Jah | Ei | Ei | Ei |
| 634 | Maksete ajalugu | Vaadake praeguse klienditellimuse kliendi makseajalugu. | Jah | Jah | Ei | Ei | Ei |
| 803 | Komplekteerimine ja vastuvõtmine | Avage leht **Komplekteerimine ja vastuvõtmine**, kus saate valida kaupluses komplekteeritavad või vastuvõetavad tellimused. | Jah | Jah | Jah | Ei | Ei |
| 632 | Järeletulemine kõigile toodetele | Määrake kõigi ridade täitmismeetodiks **Poodi järeletulemine**. | Jah | Jah | Ei | Jah\* | Ei |
| 631 | Järeletulemine valitud toodetele | Määrake valitud ridade täitmismeetodiks **Poodi järeletulemine**. | Jah | Jah | Ei | Jah\* | Ei |
| 400 | Hüpikmenüü | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 101 | Hinnakontroll | See operatsioon võimaldab kasutajal otsida konkreetse toote hinda. | Jah | Jah | Jah | Jah | Ei |
| 104 | Hinnaerand | Tühistage toote hind, kui toode on seadistatud nii, et hinna tühistamine on lubatud. | Jah | Jah | Ei | Jah | Ei |
| 1058 | Prindi X-finantsaruanne | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 1059 | Prindi Z-finantsaruanne | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 927 | Prindi kaubasilt | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 926 | Riiulisildi printimine | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 1056 | Prindi X | Printige praeguse vahetuse X-aruanne. | Jah | Jah | Jah | Ei | Ei |
| 103 | Tootekommentaar | Kande valitud rea kaubale kommentaari lisamine. | Jah | Jah | Ei | Jah | Ei |
| 100 | Tootemüük | Lisage konkreetne toode kandesse. | Jah | Jah | Jah | Jah | Ei |
| 108 | Toote otsing | See operatsioon võimaldab kasutajal otsida toodet, navigeerides kassas tooteotsingu lehele. | Jah | Jah | Jah | Jah | Ei |
| 633 | Pakkumise aegumiskuupäev | See operatsioon võimaldab kasutajal vaadata või muuta müügipakkumise aegumiskuupäeva. | Jah | Jah | Ei | Jah\* | Ei |
| 627 | Uuestiarvutamine | Arvutage kõik klienditellimuse read ja maksud ümber praeguse konfiguratsiooni alusel. | Jah | Jah | Ei | Jah\* | Ei |
| 515 | Tellimuse tagasikutsumine | See operatsioon võimaldab kasutajal klienditellimusi ja müügipakkumisi otsida ja tagasi kutsuda. | Jah | Jah | Jah | Ei | Ei |
| 504 | Kutsu kanne tagasi | See operatsioon võimaldab kasutajal praeguses kaupluses tagasi kutsuda varem peatatud kande. | Jah | Jah | Ei | Jah‡ | Ei |
| 305 | Püsikliendi punktide lunastamine | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |
| 635 | Saatekulude tagasimakse | See operatsioon võimaldab kasutajal teha tagasimakse tühistatud tellimuse saatekulude eest. | Ei | Ei | Ei | Ei | Ei |
| 644 | Kupongikoodi eemaldamine | Paluge kasutajal eemaldada kupongid, valides need kupongide loendist, mis on praegu kandega seotud. | Jah | Jah | Ei | Jah | Ei |
| 1057 | Kordustrüki Z | Printige eelmise või valitud vahetuse Z-aruanne uuesti. | Jah | Jah | Jah | Ei | Ei |
| 1216 | Sisestage uus parool | Operatsioon võimaldab parooli lähtestamise õigusega kasutajal lähtestada muu töötaja parooli, kasutades ajutist parooli. | Jah | Jah | Jah | Ei | Ei |
| 109 | Toote tagastamine | Üksikute toodete tagastamine. Järgmine skannitud toode kuvatakse tagastatud tootena, millel on negatiivne kogus ja hind. | Jah | Jah | Ei | Jah | Ei |
| 114 | Tagastuskanne | Kutsuge varasem kanne kviitungi numbri alusel tagasi, et tagastada osad või kõik tooted. | Jah | Jah | Jah | Jah§ | Ei |
| 1211 | Seifi viidav raha | Raha viimine kassaaparaadist seifi. | Jah | Jah | Jah | Jah | Ei |
| 516 | Müügiarve | See operatsioon võimaldab kliendil teha makseid valitud müügiarve alusel. | Jah | Jah | Ei | Ei | Ei |
| 502 | Müüja | See operatsioon võimaldab kasutajal määrata kassas klienditellimuste müügitellimuses väärtuse **Müügi ülevõtja**. | Jah | Jah | Ei | Jah\* | Ei |
| 2000 | Graafiku haldus | See operatsioon võimaldab kasutajatel luua, muuta või vaadata töövõtjate ajakavasid. | Jah | Jah | Jah | Ei | Ei |
| 2001 | Graafiku taotlused | See operatsioon võimaldab kasutajal taotleda vaba aega, töövahetusi vahetada või pakkuda vahetusi teistele töötajatele. | Jah | Jah | Jah | Ei | Ei |
| 622 | Otsige | See operatsioon võimaldab kasutajatel eelkonfigureerida kassa nuppe, et otsida kauba, kliendi või kategooria alusel. | Jah | Jah | Jah | Jah | Ei |
| 1213 | Otsi tarneaadress | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 709 | Riistvarajaama valimine | See operatsioon võimaldab kasutajal valida riistvarajaama saadaolevate riistvarajaamade loendist. | Jah | Jah | Jah | Jah | Ei |
| 637 | Määra kande vaikemüügiesindaja | See operatsioon võimaldab kasutajal valida ühe sobilikest komisjonitasu müügigruppidest (müügiesindajad) hiljem lisatavate ridade vaikemüügiesindajaks. | Jah | Jah | Ei | Jah | Ei |
| 105 | Määra kogus | Kande rea kauba koguse muutmine. | Jah | Jah | Ei | Jah | Ei |
| 638 | Määra reale müügiesindaja | See operatsioon võimaldab kasutajal valida ühe sobilikest komisjonitasu müügigruppidest (müügiesindajad) praegu valitud rea jaoks. | Jah | Jah | Ei | Jah | Ei |
| 630 | Läheta kõik tooted | Määrake kõigi rea kaupade täitmisrežiimi olekuks **Lähetamine**. | Jah | Jah | Ei | Jah\* | Ei |
| 629 | Läheta valitud tooted | Määrake valitud ridade täitmisrežiimi olekuks **Lähetamine**. | Jah | Jah | Ei | Jah\* | Ei |
| 115 | Töölehe kuvamine | Vaadake kaupluse töölehte. Saate vaadata kandeid, kviitungeid ja ostukviitungeid uuesti printida ning tagastamiseks tagasi kutsuda. | Jah | Jah | Jah | Jah\*\* | Ei |
| 802 | Laoinventuur | See operatsioon võimaldab kasutajal luua või muuta laoinventuuri töölehti füüsilise laoseisu või tsüklilise inventuuri jaoks. | Jah | Jah | Jah | Ei | Ei |
| 401 | Alammenüü | See operatsioon suunab kasutaja muule lingitud nupupaneelile. | Jah | Jah | Jah | Jah | Ei |
| 1054 | Peata vahetus | Peatage praegune vahetus, et kassaaparaadis saaks aktiveerida uue või muu vahetuse. | Jah | Jah | Jah | Ei | Ei |
| 503 | Peata kanne | Peatage praegune müügikanne, et selle saaks hiljem kaupluses tagasi kutsuda. | Jah | Jah | Ei | Jah‡ | Ei |
| 1004 | Ülesande salvestaja | Avage tegevuse salvestaja kassas protseduuri juhiste kirjendamiseks. | Ei | Ei | Ei | Jah | Ei |
| 1052 | Päevakassa | See toiming võimaldab kasutajal määrata sahtlis oleva raha koguse iga loetud makseviisi kohta. | Jah | Jah | Jah | Jah | Ei |
| 1210 | Väljamakse | See operatsioon võimaldab kasutajal eemaldada praegusest sahtlist või vahetusest raha. | Jah | Jah | Jah | Jah | Ei |
| 920 | Kell | See operatsioon võimaldab kasutajatel töövahetusi ja pause sisse ja välja registreerida. | Jah | Jah | Jah | Ei | Ei |
| 302 | Lõppallahindluse summa | Sisestage kandele allahindluse summa. Seda operatsiooni kasutatakse ainult allahinnatavate kaupade puhul ja ainult määratud allahindluse piires. | Jah | Jah | Ei | Jah | Ei |
| 303 | Lõppallahindluse protsent | Sisestage kande allahindluse protsent. Seda operatsiooni kasutatakse ainult allahinnatavate kaupade puhul ja ainult määratud allahindluse piires. | Jah | Jah | Ei | Jah | Ei |
| 501 | Kande kommentaar | Lisage praegusele kandele kommentaar. | Jah | Jah | Ei | Jah | Ei |
| 922 | Kuva toote üksikasjad | Avage praegu valitud rea kauba toote üksikasjade leht. | Jah | Jah | Ei | Jah | Ei |
| 1003 | Aruannete kuvamine | Vaadake praeguse kasutaja jaoks konfigureeritud aruandeid. | Jah | Jah | Jah | Ei | Ei |
| 921 | Kellaaja kirjete vaatamine | Vaadake kõigi kaupluse töötajate kella kirjeid. | Jah | Jah | Jah | Ei | Ei |
| 211 | Tühista makse | Tühistage praegu valitud makserida kandest. | Jah | Jah | Ei | Jah | Ei |
| 102 | Tühista toode | Tühistage praegu valitud rea kaup kandest. | Jah | Jah | Ei | Jah | Ei |
| 500 | Kande tühistamine | Tühistage praegune kanne. | Jah | Jah | Ei | Jah | Ei |
| 916 | Windowsi töövoo alus | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Ei |
| 924 | X aruanne pangakaartide kohta | Seda operatsiooni ei toetata. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Jah |

\* Klienditellimuse või müügipakkumise loomisel on operatsioon saadaval ainult ühenduseta režiimis ja seda ainult juhul, kui kassa funktsiooniprofiilil on konfigureeritud ühenduseta režiimis klienditellimuste ja müügipakkumiste loomine. Operatsiooni ei saa teha reaalajas teenusega tellimuste loomise või tellimuste tagasikutsumise ja muutmise ajal.

† Operatsiooni saab teha ühenduseta režiimis ainult juhul, kui kassa funktsiooniprofiilil on lubatud klientide ühenduseta loomine.

‡ Kui kassa on ühenduseta, saab peatatud kandeid tagasi kutsuda ainult praeguse kassaaparaadi ühenduseta andmebaasist. Kasutajad ei saa muudes kassaaparaatides kandeid peatada ega tagasi kutsuda.

§ Kui kassa on ühenduseta, saab tagastamiseks kutsuda ainult praeguses ühenduseta andmebaasis olevaid kandeid.

\*\* Kui kassa on ühenduseta, kuvatakse töölehel ainult praeguse võrguühenduseta kanali andmebaasi kanded.

