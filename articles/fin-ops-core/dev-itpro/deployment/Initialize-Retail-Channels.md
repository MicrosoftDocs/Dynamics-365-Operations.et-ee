---
title: Commerce Scale Uniti (pilv) lähtestamine
description: Selles teemas selgitatakse, kuidas Commerce Scale Uniti (pilve) lähtestada Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 84e70515accde161e7efa36755edec68d26be952
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092221"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Uniti (pilv) lähtestamine

[!include[banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas Commerce Scale Uniti (pilve) lähtestada Microsoft Dynamics 365 Commerce.

Kui kasutate Tier-2 liivakasti või tootmiskeskkonda, millel on rakenduse versioon 8.1.2.x või uuemad versioonid, peate enne jaemüügikanali funktsiooni kasutamist kas müügikoha (POS) toiminguteks või e-kaubanduse toiminguteks, mis kasutavad pilves Retail Serverit. Lähtestamine juurutab Commerce Scale Uniti (pilve).

> [!IMPORTANT]
> Olemasolevate klientide jaoks, kes kasutavad pilves jaemüügikanali funktsioone, nõuame, et värskendaksite oma jaemüügikanaleid, et kasutada Commerce Scale Uniti. Uued keskkonnad, mis on juurutatud ilma Commerce Scale Unitita, ei saa enam pilve majutatud jaemüügikanali komponentide kvaliteedi- ja teenusevärskendusi. Klientidele, kes kasutavad ainult Commerce Scale Uniti (ise hostitud) ei ole vaja toiminguid teha. Kui vajate laiendust, võtke ühendust oma Microsoft FastTracki lahendusearhitektiga.

## <a name="prerequisites"></a>Eeltingimused

1. Juurutage Tier-2 liivakast või tootmiskeskkond, mille versioon on 8.1.2.x või uuemad versioonid.
2. Saate ise juurutada kuni 2 Commerce Scale Ühikut keskkonna kohta. Kui vajate keskkonna kohta rohkem kui 2 Commerce Scale Ühikut keskkonna kohta, looge elutsükli teenustes Microsoft Dynamics (LCS) tugiteenuse taotlus ja sisestage **taotlus täiendava Commerce Scale Uniti** kohta ning märkige keskkonna ID, kaubandusskaala ühikute arv ja soovitud andmekeskuse piirkonnad. Taotlus täidetakse viie tööpäeva jooksul. Kui te ei vaja rohkem kui 2 Commerce Scale Ühikut keskkonna kohta, ei pea te tugiteenuse taotlust looma. 
3. Enne Commerce Scale Uniti lähtestamist peavad teil olema elutsükli teenuste projekti omaniku õigused.
4. Veenduge, et jaemüügi litsentsi konfiguratsioonivõtmed on teie keskkonnas lubatud. Lisateavet vt [teemast Litsentsikoodide ja konfiguratsioonivõtmete aruanne](../sysadmin/license-codes-configuration-keys-report.md). Commerce Scale Uniti kasutamiseks peavad järgmised klahvid sisse lülitama.

    - RetailBasic
    - RetaileCommerce – kui kavatsete kasutada e-kaubandust Dynamics 365 Commerce.
    - RetailGiftCard - Kui kavatsete kinkekaarte kasutada.
    - RetailInvent – kui kavatsete kasutada varusid.
    - RetailModernPos - Kui kavatsete kasutada müügikohta (kassa).
    - RetailReplenishment – kui kavatsete kasutada täiendusi.
    - RetailScheduler
    - RetailStores – kui kavatsete kassat kasutada.


## <a name="region-availability"></a>Piirkonna saadavus
Commerce Scale Unit on juurutamiseks saadaval järgmistes piirkondades.

| Globaalne asukoht | Regioon              | Kättesaadavus        |
|-----------------|---------------------|---------------------|
| AMERICAS        | Ida-USA             | Üldiselt saadaval |
| AMERICAS        | Ida-USA 2           | Üldiselt saadaval |
| AMERICAS        | Kesk-USA põhjaosa    | Üldiselt saadaval |
| AMERICAS        | Kesk-USA lõunaosa    | Üldiselt saadaval |
| AMERICAS        | Kesk-USA          | Üldiselt saadaval |
| AMERICAS        | Lääne-USA             | Üldiselt saadaval |
| AMERICAS        | Lääne-USA 2           | Üldiselt saadaval |
| AMERICAS        | Kanada kesklinn      | Piiratud võimsus    |
| AMERICAS        | Kanada idaosa         | Piiratud võimsus    |
| AMERICAS        | Usa lääneosa     | Piiratud võimsus    |
| APAC            | Ida-Austraalia      | Üldiselt saadaval |
| APAC            | Kagu-Aasia      | Üldiselt saadaval |
| APAC            | Ida-Jaapan          | Üldiselt saadaval |
| APAC            | Lääne-Jaapan          | Üldiselt saadaval |
| APAC            | Kagu-Austraalia | Piiratud võimsus    |
| APAC            | Ida-Aasia           | Piiratud võimsus    |
| APAC            | India lõunaosas         | Piiratud võimsus    |
| APAC            | India Kesk-Euroopa       | Piiratud võimsus    |
| EMEA            | Lääne-Euroopa         | Üldiselt saadaval |
| EMEA            | Põhja-Euroopa        | Üldiselt saadaval |
| EMEA            | Ühendkuningriigi lõunaosa            | Piiratud võimsus    |
| EMEA            | Ühendkuningriigi lääs             | Piiratud võimsus    |

Piiratud võimsusega piirkondades on kasutuselevõtuvõimsus äärmiselt piiratud. Kasutuselevõtu taotlusi hinnatakse iga juhtumi puhul eraldi. Kui teil on piiratud võimsusega piirkondades juurutamise jaoks kaalukas ärivajadus, võite esitada ootenimekirja lisamiseks tugiteenuse taotluse.

![Kaart, mis näitab piirkonna saadavust.](media/Commerce-Scale-Unit-Region-Availability.png "Kaart, mis näitab piirkonna saadavust")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Commerce Scale Uniti lähtestamine uue keskkonnajuurutuse osana

Palun veenduge, et peakorter on saadaval. See on vajalik skaalaüksuse registreerimiseks peakorteris lähtestamisprotsessi ajal. Kui peakorter on hoolduses, ei ole soovitatav skaalaüksust lähtestada, kuna see ei pruugi hooldusprotsessi ajal saadaval olla.

1. Veenduge, et peakontori keskkond on saadaval, mitte [hooldusrežiimis](../sysadmin/maintenance-mode.md).
2. Valige LCS-i lehel Keskkonna üksikasjad suvand **Keskkonnafunktsioonid \> Kaubandus**.
3. Valige lehel Commerce'i häälestuse juurutus käsk **Lähtesta.**
4. Valige lähtestamiseks Commerce Scale Uniti versioon.
5. Valige piirkond, kus Commerce Scale Unit lähtestada.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Kanalite konfigureerimine Commerce Scale Uniti kasutamiseks

Pärast Commerce Scale Uniti juurutamist peate tagama, et teie kanalid on konfigureeritud andmebaasi selle jaoks kasutama. 

Kanalite konfigureerimiseks Commerce Scale Uniti andmebaasi kasutamiseks tehke järgmist.

1. Avage Commerce'i peakontoris **jae- ja kaubandus \> peakontori häälestus \> Commerce Scheduler \> Channeli andmebaas**.
1. Valige vasakpoolsel paanil kanaliandmebaas.
1. **Valige kiirkaardil** Jaemüügikanal **Lisa** ja seejärel valige ripploendist oma jaemüügikanal.
1. Valige **Lisa** ja seejärel valige ripploendist oma veebikanal. 

Kui olete lõpetanud, minge jae- ja kaubandus- ja kaubandus-kaubanduse **IT-jaotuse \> ajakavasse \>** ning käivitage töö 9999.

> [!NOTE] 
> Töö 9999 sünkroonib kõik uued tooted ja kliendid Commerce Scale Unitiga. See protsess võib võtta kaua aega. Kui kanal peab olema saadaval ainult e-kaubanduse saidi koostaja konfiguratsiooni jaoks, saate töö 9999 asemel käivitada töö 1070.

### <a name="database-refresh-and-commerce-scale-units"></a>Andmebaasi värskendamine ja kaubanduse skaala ühikud

Enne alustamist veenduge, et olete tuttav juhistega [, mida pärast andmebaasi värskendamist lõpule viia keskkondade jaoks, mis kasutavad Commerce'i funktsioone](../database/database-refresh.md).

Skaalaühiku kanali andmebaasikirjeid (kanali andmebaasi vormis) ei saa andmebaasi värskendamise osana keskkondades teisaldada. Seda seetõttu, et kirjed esindavad keskkonnapõhist konfiguratsiooni.

Pärast andmebaasi värskendamist saate taastada skaalaüksuse kanaliandmebaasi kirje, andes LCS-is välja oma skaalaüksuse uuesti juurutamise. Mis tahes juurutus- või teenindustoimingud skaalaüksuses üritavad skaalaüksust peakorteris registreerida, kui registreering tuvastatakse puuduvana.

Saate välja anda skaalaüksuse uuesti juurutamise ilma komponente muutmata, valides sama versiooni juurutamise, mille skaalaüksus juba on. Seda saab LCS-is teha järgmiste toimingutega.

1. Valige LCS-i lehel Keskkonna üksikasjad suvand **Keskkonnafunktsioonid \> Jaemüük**.
2. Valige häälestuse juurutuslehel skaalaühik, mille soovite ümber paigutada.
3. Valige skaalaüksuse töömenüüs **Värskendus**.
4. Valige liuguri ripploendis **Valik versioon** suvand **Määra versioon**.
5. Tippige tekstiväljale jaotises **Versiooni** määramine skaalaühiku jaoks kuvatud versioon, mis kuvatakse lisaks praeguse versiooni **sildile**.
6. Klõpsake **nuppu Värskenda**.

Te ei pea valima **värskenduslaiendeid**, isegi kui olete varem laiendusi rakendanud, kuna skaalaüksusele rakendatud viimane laienduspakett valitakse skaalaüksuse värskendamisel automaatselt.

Kui teil on mitu skaalaühikut, peate iga skaalaühiku puhul ülaloleva toimingu tegema. Soovi korral saate neid toiminguid teha paralleelselt.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Täiendavate kaubanduse mastaabiüksuste juurutamine (valikuline)

Pärast Commerce Scale Unit'i lähtestamist saate ise juurutada teise skaalaühiku, kui teie litsents annab teile selleks õiguse. Rohkem kui kahe mastaabiühiku juurutamiseks peate looma tugitaotluse. Toetaotluses märkige vajalike kaubanduse mastaabiühikute arv, keskkonna nimi ja soovitud piirkonnad. Lisateavet litsentsimise kohta vt [Dynamics 365 litsentsimise juhend](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Iga täiendava Commerce Scale üksuse jaoks, mille juurutate, soovitame luua eraldi kanali andmebaasi rühm, järgides neid samme.

1. Commerce'i peakontoris minge aadressile **Jaemüük ja kaubandus >Retail Headquarters > Jaemüügiplaanija häälestus > Kanalite andmebaasirühm**.
2. Looge uus kanali andmebaasigrupp.
3. Mine lehele **Jaemüük ja kaubandus >Retail Headquarters > Jaemüügi ajakava seadistamine > Kanalite andmebaas** ja valige kanali andmebaas, mis vastab äsja loodud kaubanduse mastaabiühikule.
4. Valige **Muuda** ja valige uus kanali andmebaasi rühm.
5. Valige käsk **Salvesta**.
6. Valige **Käivitage täielik andmete sünkroonimine** valitud kanali andmebaasi jaoks.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Täiendavad kaalutlused pilve hostitud kaubanduskanali komponentide lähtestamisel olemasolevas keskkonnas

Kui kasutate keskkonnas juba pilvehostitud Commerce'i kanali komponente, aitab Commerce Scale Unit'i lähtestamine vähendada nende komponentide värskendamisel tekkivaid seisakuid. Enne Commerce Scale Unit lähtestamist on vaja täiendavat planeerimist.

Kui lähtestate oma esimese Commerce'i mastaabiüksuse keskkonnas, mis kasutab pilve hostitud Commerce'i kanali komponente, migreerub lähtestamisprotsess teie pilve hostitud kanalikomponentidega seotud kanalid esimesse mastaabiüksusesse. Store Scale ühikutega seotud kanaleid see ei mõjuta.

Migratsiooniprotsess on kanalitele läbipaistev. Pärast skaalaüksuse lähtestamise algust teostatakse automaatselt järgmised toimingud:

1. Luuakse uus Commerce Scale Unit ja seostatakse see keskkonnaga.
2. Commerce Scale Unit registreeritakse peakorteris saadaoleva kanaliandmebaasina.
3. Kõik kanalid on kaardistatud **Vaikimisi** peakorteri kanalite andmebaasi värskendatakse, et see vastaks uuele Commerce Scale Unitile.
4. A Commerce Data Exchange Kanaliandmete uude skaalaühikusse viimiseks tehakse andmete täielik (CDX) sünkroonimine.

**Commerce Scale Unit lähtestamise planeerimine ja testimine** Üldreeglina peate Commerce Scale Unit'i lähtestamisel planeerima viietunnise seisakuaja nii poe toimingute kui ka kõigi e-kaubanduse kanali toimingute jaoks, mis kasutavad jaemüügiserverit või pilvemüügipunkti.

1. Värskendage andmebaasi tootmiskeskkonnast liivakasti UAT-keskkonda. 
2. Initsialiseerige Commerce Scale Unit liivakasti UAT keskkonnas. 
3. Pange tähele Commerce Scale Unit'i lähtestamisaeg. See on võrreldav selle toimingu ajaga teie tootmiskeskkonnas, mille jooksul poetoimingud ja e-kaubanduse toimingud pole saadaval.

Enne Commerce Scale Unit lähtestamist peate tegema järgmised lisatoimingud.

- **Sulgege kõik POS-i vahetused** - Pärast üleviimist ei saa POS-i kasutajad sulgeda ühtegi vahetust, mis migratsiooniprotsessi ajal olid aktiivsed.
- **Kinnitage, et kõik P-tööd on edukalt sooritatud** - Soovitatav on, et ootel olevate tehingute sünkroonimiseks mõeldud P-tööd oleksid lõpetatud enne CSU initsialiseerimist.
- **Logige välja kõigist kassaseadmetest** - POS-operatsioone migratsiooni ajal ei toetata.
- **Kutsuge tagasi ja tühistage kõik POS-is peatatud tehingud** - Peatatud tehinguid ei säilitata lähtestamise osana.

> [!IMPORTANT]
> Commerce Scale Unit lähtestamise osana lähevad varasemad peatatud tehingud kaotsi ja neid ei saa tagasi kutsuda. 

Lähtestamisperioodi jooksul toimub järgmine:

- Pilve hostitud kaubanduskanalid ei tööta, välja arvatud juhul, kui lülitate sisse POS-i võrguühenduseta funktsiooni.
- POS-seadmetel, mille võrguühenduseta funktsioon on sisse lülitatud, on vähem funktsioone.
- Kõik e-kaubanduse kliendid, mis sõltuvad jaemüügiserverist, on häiritud.
- See ei mõjuta kanaleid, mida hostitakse Commerce Scale Units'is (ise hostitud).
- Peakontori funktsionaalsust see ei mõjuta.

Pärast initsialiseerimise lõppu toimub järgmine:

- Kõikide aktiveeritud POS-seadmete seadmete aktiveerimise olek säilib, mis tähendab, et seadmeid ei pea uuesti aktiveerima.
- Eraldiseisvad riistvarajaama eksemplarid jätkavad tööd.
- POS-kanalipoolsed aruanded lähtestatakse ja neid ei kuvata enne lähtestamist.
- Tööpäeviku näitamise toiming lähtestatakse ka ja see ei näita andmeid enne lähtestamist.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
