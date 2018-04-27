---
title: "Lao mobiilse seadme kuvasätted"
description: "Selles artiklis kirjeldatakse, kuidas seadistada mobiilse seadme kuva välimust ja vastendada kiirklahve juhtelementidega, näiteks nuppudega."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b16f4ea27f406f3d5d5957670bd32a73d2d55529
ms.openlocfilehash: bb616f8102c67db3f8c3e872101d61657b6b64d1
ms.contentlocale: et-ee
ms.lasthandoff: 02/05/2018

---

# <a name="warehouse-mobile-device-display-settings"></a>Lao mobiilse seadme kuvasätted

[!INCLUDE [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas seadistada mobiilse seadme kuva välimust ja vastendada kiirklahve juhtelementidega, näiteks nuppudega. 

See artikkel kehtib mooduli Laohaldus täpsema ladustamise funktsioonide puhul. Mobiilset seadet saab kasutada paljude laotöötajate ülesannete puhul.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Laadise määramine ja klaviatuuri otseteede vastendamine
Mobiilse seadme konfiguratsiooni osana saate määratleda mobiilsetele seadmetele erinevad paigutused. Selleks peate teadma kaskaadlaadistike (CSS) faili ja aktiivse serveri lehe laiendi (ASPX) faili nime. Vaikefailid on installitud lao mobiilsete seadmete portaali installi osana. Kui te ei tea failinimesid, küsige neid süsteemiadministraatorilt. Saate määratleda uue laadi lehel **Mobiilse seadme kuvasätted**.

-    Sisestage CSS-faili nimi väljale **CDD-fail**. Lisage .css-faili nime laiend.
-   Määrake väljal **Mobiilse seadme kuvasätete vaade** ASPX-fail. **Ärge** lisage faili nimele laiendit .aspx.

CSS- ja ASPX-failid peavad asuma kindlas kaustas, nii et rakendus Internet Information Services (IIS) saaks need laadida. Kui käitate mobiilse seadme funktsioone erinevates brauserites või erinevatel riistvaradel, mis nõuavad erinevat paigutuse juhtelementi, võib olla kasulik määratleda erinevad CSS-failid. Lihtsaid sätteid, nagu taustavärv, font ja teksti fondisuurus, nuppude laius ja käitumine, saab hõlpsasti juhtida CSS-failide erineva kasutamisega. ASPX-faili kasutatakse mobiilisaidi kuvamiseks serveripoolsel rakendusel ASP.NET. Fail juhib, kuidas HTML-i üldine struktuur paigutatud on. Selle funktsiooni võiks kohandada ainult siis, kui teil on HTML-i ja JavaScriptiga tõsiseid struktuuriprobleeme ning peate seda koodi konkreetsete seadmete puhul muutma. Mobiilse seadme lehel olevate HTML-i juhtelementide vastendamiseks klaviatuuri otseteedega määrake lehe **Mobiilse seadme kuvasätted** väljal **Kiirklahv** klahvidele numbrilised koodid. Numbriliste koodide otsimiseks saate kasutada mobiilse seadme menüüd **Kuva klaviatuuri otseteede koodid**. Arvestage sellega, et olenevalt kasutatavast riistvarast võib vastendamine erineda. Vastenduse loomiseks peate kasutama järgmist süntaksit.

&lt;control name&gt;(&lt;key name&gt;)=&lt;key code&gt;;

Siin on süntaksi osade selgitused:

-   **&lt;control name&gt;** – juhtelemendi nimi, näiteks HTML-is renderdatud nupp.
-   **(&lt;key name&gt;)** – klaviatuuri klahvi nimi, mille jaoks loote otseteed.
-   **&lt;Key code&gt;** – numbrilise tärgi kood klahvile, mida soovite kasutada kiirklahvina.

Siin on näide.

Tühista (Esc) = 27; Täielik (F2) = 113

Kõikidel lehtedel, kus on nupp **Tühista**, on nupul järgmine tekst.

**(Esc) Tühista**

Klaviatuuril klahvi Esc vajutamine aktiveerib nupu **Tühista**. Kindlale seadmele laadi ja kiirklahvide sätete rakendamiseks peate looma väljal **Kriteerium** vastenduse. Peate kasutama regulaaravaldist .NET, et luua vastendus ja avaldis peab koosnema kolmest jaotisest, mis on eraldatud vertikaalse ribaga (|), nagu on siin näidatud.

Request.UserHostAddress=&lt;user host address&gt;|HostName=&lt;user host name&gt;|Request.UserAgent=&lt;user agent&gt;

Siin on avaldise osade selgitused:

-   **&lt;user host address&gt;** – .NET-i regulaaravaldis, mis sobitub taotleja IP-aadressiga.
-   **&lt;user host name&gt;** – .NET-i regulaaravaldis, mis sobitub taotleja võrgunimega.
-   **&lt;user agent&gt;** – .NET-i regulaaravaldis, mis sobitub taotleja kasutatava brauseri identifikaatoriga.

Järgmine näide võimaldab kasutada brauserit Internet Explorer 8:

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

Saate kasutada mobiilse seadme menüüd **Kuva kuvasätete serverikonfiguratsioon**, et otsida teavet seadistuse kohta.

## <a name="define-text-colors-for-messages"></a>Sõnumite teksti värvide määratlemine
Saate kasutada lehte **Mobiilse seadme teksti värvid**, et juhtida erinevaid värve, mida kasutatakse süsteemi loodud teadetes, näiteks tõrketeadetes. Näiteks võib teksti värv näidata teate eesmärki või olulisust. Kuvatakse järgmist tüüpi teated.

| Teate tüüp | Kirjeldus                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vaikimisi      | Vaiketeated kasutavad kõikide teadete puhul vaikevärvisätteid, nagu on määratlenud lao mobiilsete seadmete portaali CSS-fail.                                                   |
| Viga        | Tõrketeated näitavad probleemi, mille kasutaja peab lahendama, enne kui saab jätkata.                                                                                             |
| Õnnestus      | Eduteated kinnitavad, et tegevus õnnestus.                                                                                                                                |
| Hoiatus      | Hoiatusteated annavad töötajale teada, et on probleem või probleem võib tekkida, kui töötaja jätkab. Siiski ei pea töötaja jätkamiseks probleemi lahendama. |

Värvi valimiseks klõpsake lehel **Värvi valimine** paletti või tippige kuusteistkümmend-värvikood.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Mobiilsete seadmetega kasutatava kuupäevavormingu määramine
Saate laiendada iga installimise jaoks vastuvõetavate kuupäevavormingute loendit. See võimalus võib olla kasulik näiteks siis, kui soovite kasutada vormingut, mis lihtsustab töötajal mobiilsesse seadmesse kuupäevade sisestamist. Vaikevormingu määrab kasutaja vaikekeel, mis on määratud lehe **Kasutaja suvandid** väljal **Keel**. (Sama lehte kasutatakse töötaja seostamiseks kindla laotöö kasutajaga.) **Märkus.** Lao mobiilsete seadmete portaal ei kasuta lehe **Keele ja regiooni eelistused** välja **Kuupäeva, kellaaja ja numbri vorming** sätet. Kuupäevavormingu muutmiseks peate tundma Microsoft .NET Frameworki regulaaravaldisi. Lisateabe saamiseks vt jaotist [.NET Frameworki regulaaravaldised](http://go.microsoft.com/fwlink/?LinkId=391260). Kuupäevavormingute määratlemiseks redigeerige faili Dates.ini, mis asub lao mobiilsete seadmete portaali serveris asukohas Content\\Settings\\Dates.ini. Fail kasutab kuupäevavormingu määramiseks .NET-i regulaaravaldisi. Regulaaravaldis peab sisaldama allavaldisi, mis loovad nimetatud gruppe päeva, kuu ja aasta (PPKKAA) jaoks, nagu on näidatud järgmises näites.

^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$

Iga allavaldis nõuab ühte kuni kahte kohta päeva ja kuu jaoks ning ühte kuni nelja kohta aasta jaoks. Näiteks järgmine allavaldis määrab nimetatud grupi aasta kohta ja nõuab vähemalt kahte või maksimaalselt nelja numbrit.

(?&lt;year&gt;\\d{2,4})

Saate ühes failis määrata mitu avaldist. Iga avaldis peab olema eraldi real. Esimest vastendatud avaldist kasutatakse kuupäeva sõelumiseks.

<a name="see-also"></a>Vt ka
--------

[Mobiilsete seadmete konfigureerimine laotöö jaoks](configure-mobile-devices-warehouse.md)




