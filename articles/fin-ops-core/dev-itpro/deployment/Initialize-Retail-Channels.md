---
title: Commerce Scale Uniti (pilv) lähtestamine
description: See artikkel selgitab, kuidas käivitada Commerce Scale Uniti (pilve) sisse Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: f9d21de3e498b293394835d5cf564899338b9c18
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473985"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Uniti (pilv) lähtestamine

[!include[banner](../includes/banner.md)]

See artikkel selgitab, kuidas käivitada Commerce Scale Uniti (pilve) sisse Microsoft Dynamics 365 Commerce.

Kui kasutate kiht-2 ruutu või tootmiskeskkonda, mille rakenduse versioon on 8.1.2.x või uuem, peate lähtestama commerce Scale Uniti (pilve), enne kui saate kasutada jaemüügikanali funktsioone kas müügikoha (POS) toimingutes või e-kaubanduse toimingutes, mis kasutavad Jaemüügiserverit pilves. Lähtestamine juurutab Commerce Scale Uniti (pilve).

> [!IMPORTANT]
> Olemasolevate klientide jaoks, kes kasutavad pilves jaemüügikanali funktsioone, on äri jätkuva ja katkestamata toe tagamiseks vaja värskendada jaemüügikanaleid Commerce Scale Uniti kasutamiseks. Ilma Commerce Scale Unitita juurutatud uued keskkonnad ei saa enam pilve majutatud jaemüügikanali komponentide kvaliteedi ja teenuse värskendusi. Tegevust ei nõuta klientide puhul, kes kasutavad ainult Commerce Scale Uniti (ise majutatud). Kui vajate laiendust, pöörduge oma Microsoft FastTracki lahenduse arhitekti poole.

## <a name="prerequisites"></a>Eeltingimused

1. Juurutage kiht-2info või tootmiskeskkond, mille versioon on 8.1.2.x või uuem.
2. Saate ise juurutada kuni 2 Commerce Scale Unitsi keskkonna kohta. Kui vajate elutsükli teenustes (LCS Microsoft Dynamics) rohkem kui 2 Commerce Scale Unitsi keskkonna kohta, **looge tugitaotlus ja sisestage commerce Scale Uniti** lisataotlus ning näidake keskkonna ID-d, Commerce Scale Unitsi arvu ja soovitud andmekeskuste piirkondi. Taotlus täidetakse viie tööpäeva jooksul. Kui te ei nõua rohkem kui 2 Commerce Scale Unitsi keskkonna kohta, ei pea te tugitaotlust looma. 
3. Enne Commerce Scale Uniti lähtestamist peavad teil olema projekti omaniku õigused elutsükli teenustes.
4. Veenduge, et jaemüügi litsentsi konfiguratsioonivõtmed on teie keskkonnas lubatud. Lisateavet vt litsentsikoodide [ja konfiguratsioonivõtmete aruandest](../sysadmin/license-codes-configuration-keys-report.md). Commerce Scale Uniti kasutamiseks peavad teil järgmised võtmed olema sisse lülitatud.

    - RetailBasic
    - RetaileCommerce – kui plaanite kasutada E-commerce’i rakenduse <a0/&a; jaoks,Dynamics 365 Commerce
    - RetailGiftCard – kui plaanite kinkekaarte kasutada.
    - RetailInvent – kui plaanite varusid kasutada.
    - RetailModernPos – kui plaanite kasutada kassat;
    - RetailReplenishment – kui plaanite varusid kasutada.
    - RetailScheduler
    - RetailStores – kui plaanite kassat kasutada.


## <a name="region-availability"></a>Piirkonna saadavus
Commerce Scale Unit on saadaval juurutamiseks järgmistes regioonides.

| Globaalne asukoht | Regioon              | Kättesaadavus        | Kommentaarid                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERICAS        | Ida-USA             | Üldiselt saadaval |  Kommentaarid puuduvad.                         |
| AMERICAS        | Ida-USA 2           | Üldiselt saadaval |  Kommentaarid puuduvad.                          |
| AMERICAS        | Kesk-USA põhjaosa    | Piiratud võimsus    |  Kommentaarid puuduvad.                            |
| AMERICAS        | Kesk-USA lõunaosa    | Piiratud võimsus    |  Kommentaarid puuduvad.                            |
| AMERICAS        | Kesk-USA          | Üldiselt saadaval |  Kommentaarid puuduvad.                            |
| AMERICAS        | Lääne-USA             | Üldiselt saadaval |  Kommentaarid puuduvad.                            |
| AMERICAS        | Lääne-USA 2           | Üldiselt saadaval |  Kommentaarid puuduvad.                            |
| AMERICAS        | Kanada keskpank      | Piiratud võimsus    |  Kommentaarid puuduvad.                            |
| AMERICAS        | Kanada, Ida         | Piiratud võimsus    |   Kommentaarid puuduvad.                           |
| AMERICAS        | Lääne-Kesk-USA     | Piiratud võimsus    |   Kommentaarid puuduvad.                           |
| APAC            | Ida-Austraalia      | Üldiselt saadaval |   Kommentaarid puuduvad.                           |
| APAC            | Kagu-Aasia      | Piiratud võimsus | Juurutused pole lubatud.    |
| APAC            | Ida-Jaapan          | Üldiselt saadaval |  Kommentaarid puuduvad.                            |
| APAC            | Lääne-Jaapan          | Üldiselt saadaval |   Kommentaarid puuduvad.                           |
| APAC            | Kagu-Austraalia | Üldiselt saadaval |   Kommentaarid puuduvad.                           |
| APAC            | Ida-Aasia           | Piiratud võimsus    |   Kommentaarid puuduvad.                           |
| APAC            | India ( Lõuna-India)         | Piiratud võimsus | Juurutused pole lubatud.    |
| APAC            | India Central       | Piiratud võimsus    | Vajab kinnitusprotsessi. |
| EMEA            | Lääne-Euroopa         | Üldiselt saadaval    |  Kommentaarid puuduvad. |
| EMEA            | Põhja-Euroopa        | Üldiselt saadaval    |  Kommentaarid puuduvad. |
| EMEA            | UK Lõuna            | Üldiselt saadaval |    Kommentaarid puuduvad.                          |
| EMEA            | UK, Lääs             | Üldiselt saadaval |    Kommentaarid puuduvad.                          |
| Aüe             | Põhja-AÜE           | Piiratud võimsus    | Vajab kinnitusprotsessi. |

Piiratud võimsusega regioonides on juurutamisvõimsus väga piiratud. Juurutamistaotlusi hinnatakse juhtumi kaupa. Kui teil on piiratud võimsusega regioonides ärisuhteid vaja juurutada, saate ooteloendisse lisata tugitaotluse. Võimsuse piiratud alad ei võimalda praegu Commerce Scale Uniti juurutamist. 

![Saate vastendada regiooni kättesaadavusega.](media/Commerce-Scale-Unit-Region-Availability.png "Kuva regiooni saadavust kuvav vastendamine")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Commerce Scale Uniti lähtestamine uue keskkonna juurutamise osana

Veenduge, et peakontor on saadaval. See on vajalik, et registreerida kaaluühik lähtestamisprotsessi ajal peakontoris. Kaaluühikut ei soovitata käivitada, kui peakontor on hooldamis all, kuna see ei pruugi töö käigus muutuda kättesaadavaks.

1. Veenduge, et peakontori keskkond on saadaval ja mitte [hooldusrežiimis](../sysadmin/maintenance-mode.md).
2. LCS-i keskkonna üksikasjade lehel valige keskkonnafunktsioonid **\> Commerce**.
3. Valige commerce’i häälestamise juurutamise lehel suvand **Lähtesta**.
4. Valige lähtestamiseks Commerce Scale Uniti versioon.
5. Valige piirkond, kus Commerce Scale Unit lähtestada.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Kanalite konfigureerimine Commerce Scale Uniti kasutamiseks

Pärast Commerce Scale Uniti juurutamist peate tagama, et teie kanalid on konfigureeritud selle jaoks andmebaasi kasutama. 

Oma kanalite konfigureerimiseks Commerce Scale Uniti andmebaasi kasutamiseks järgige neid samme.

1. Minge Commerce Headquartersi Rakenduse Retail ja **Commerce Headquarters häälestamise \> rakenduse \> Commerce Scheduler \> Channel andmebaasi**.
1. Valige vasakul paanil kanali andmebaas.
1. **Jaemüügikanali kiirkaardil** valige **käsk** Lisa ja seejärel valige ripploendist jaemüügikanal.
1. **Valige** lisa ja seejärel valige ripploendist oma võrgukanal. 

Kui olete lõpetanud, minge jaemüügi **ja rakenduse Commerce Retail ja äri it-jaotuse \>\> graafikusse** ja käivitage töö 9999.

> [!NOTE] 
> Töö 9999 sünkroonib kõik uued tooted ja kliendid Commerce Scale Uniti. See protsess võib võtta palju aega. Kui kanal peab olema saadaval ainult e-äri saidi koostaja konfiguratsiooni jaoks, saate töö 9999 asemel käivitada töö 1070.

### <a name="database-refresh-and-commerce-scale-units"></a>Andmebaasi värskendamine ja äriskaala ühikud

Enne alustamist veenduge, et olete tuttav [läbitud sammudega pärast andmebaasi värskendamist Commerce’i funktsiooni kasutava keskkonna puhul](../database/database-refresh.md).

Kaaluühiku kanali andmebaasi kirjeid (kanali andmebaasi vormis) ei saa andmebaasi värskenduse osana läbi kogu keskkonda teisaldada. Seda seetõttu, et kirjed tähistavad keskkonnaspetsiifilist konfiguratsiooni.

Pärast andmebaasi värskendamist saate luua uuesti kaaluühiku kanali andmebaasi kirje, väljasdes taasjuurutades oma kaaluühiku LCS-s. Iga juurutamine või hooldamine kaaluühikus üritab registreerida kaaluühikut peakontoris, kui registreerimine tuvastatakse puuduvana.

Saate väljasta kaaluühiku taasjuurumise ilma komponente muutmata, valides sama versiooni, mille juures teie kaaluühik juba on. Seda saab teha LCS-s järgmiste sammude abil:

1. Valige LCS-i keskkonna üksikasjade lehel keskkonnafunktsioonid **Jaekaubandus \>**.
2. Valige häälestuse juurutamise lehel kaaluühik, mida soovite uuesti juurutada.
3. Valige kaaluühiku operatsioonimenüü suvand **Uuenda**.
4. Valige versiooni valimine slaidi **ripploendist** **suvand Määra versioon**.
5. Tippige tekstiväljale "Määra **versioon"** oma kaaluühiku jaoks näidatav versioon, mis kuvatakse praeguse versiooni **sildi** peale.
6. Klõpsake nuppu **Uuenda**.

Te ei pea valima **värskendamislaiendeid** isegi juhul, kui olete laiendusi juba rakendanud, kuna kaaluühikule rakendatud viimane laienduspakett komplekttakse kaaluühiku uuendamisel automaatselt.

Kui teil on mitu skaalaühikut, peate sooritama operatsiooni igale kaaluühikule. Soovi korral võite teha neid toiminguid paralleelselt.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Commerce Scale Unitsi täiendavate juurutamine (valikuline)

Pärast Commerce Scale Uniti lähtestamist saate teise kaaluühiku kasutusele võtta, kui teie litsents seda lubab. Rohkem kui kahe kaaluühiku juurutamiseks peate looma tugitaotluse. Tugitaotluses peate lisama Commerce Scale Unitsi ühikute arvu, keskkonna nime ja soovitud regioonid. Lisateavet litsentsimise kohta vt [Dynamics 365 litsentsijuhendist](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Iga täiendava juurutatud Commerce Scale Uniti puhul on soovitatav luua eraldi kanali andmebaasi grupp, järgides neid samme.

1. Minge Äri peakontoris jaemüügi **ja äri > > Retail Headquarters kaupluse andmeedastaja > kanali andmebaasi grupis**.
2. Looge uus kanali andmebaasigrupp.
3. Minge jaemüügi ja **Retail Headquarters äri > > Kaupluse andmeedastaja häälestus > Kanali** andmebaasi ja valige kanali andmebaas, mis vastab vastloodud Äriskaala ühikule.
4. Valige **Redigeeri** ja valige uus kanali andmebaasi grupp.
5. Valige käsk **Salvesta**.
6. Valige **valitud kanali andmebaasi jaoks** suvand Käivita andmete täielik sünkroonimine.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Täiendavad kaalutlused pilve majutatud Ärikanali komponentide lähtestamisel olemasolevas keskkonnas

Kui kasutate juba pilves majutatud Commerce Kanali komponente keskkonnas, aitab Commerce Scale Uniti lähtestamine nende komponentide värskendamisel etteaega vähendada. Enne Commerce Scale Uniti lähtestamist on vajalik täiendav planeerimine.

Kui lähtestate oma esimese Commerce Scale Uniti keskkonnas, mis kasutab pilves majutatud Ärikanali komponente, siirdab lähtestamisprotsess teie pilves majutatud kanali komponentidega seotud kanalid esimese skaala ühikusse. Kaupluse kaalu ühikutega seostatud kanalid pole mõjutatud.

Siirdeprotsess on kanalite jaoks selge. Pärast kaaluühiku lähtestamist sooritatakse automaatselt järgmised operatsioonid:

1. Luuakse uus Commerce Scale Unit ja seostatakse keskkonnaga.
2. Commerce Scale Unit registreeritakse peakontoris saadaoleva kanali andmebaasina.
3. Kõik peakontori vaikekanali andmebaasiga **vastendatud** kanalid värskendatakse uue Commerce Scale Unitiga vastendamiseks.
4. (Commerce Data Exchange CDX) tehakse andmete täielik sünkroonimine, et viia kanali andmed uude skaala ühikusse.

**Commerce Scale Uniti** lähtestamise planeerimine ja testimine üldreeglina Commerce Scale Uniti lähtestamisel peate plaanima kaupluse toimingute jaoks viietunnise töötunnise akna, aga ka mis tahes e-äri kanali toimingute jaoks, mis kasutavad jaemüügiserverit või pilve müügipunkti.

1. Saate teha andmebaasivärskenduse tootmiskeskkonnastboxi UAT-i keskkonda. 
2. Commerce Scale Uniti lähtestamineboxi UAT-keskkonnas. 
3. Pange tähele Commerce Scale Uniti puhul lõpetamiseks etteantud lähtestamise aega. See on võrreldav ajaga, mis kulub teie tootmiskeskkonnas ning mille jooksul ei ole kauplusetoimingud ja e-kaubanduse toimingud saadaval.

Enne Commerce Scale Uniti lähtestamist peate sooritama järgmised lisa sammud.

- **Sulgege kõik müügikoha vahetused** – pärast migreerimist ei saa kassa kasutajad sulgeda vahetusi, mis migreerimisprotsessi ajal aktiivsed olid.
- **Kontrollige, kas kõik P-tööd on** edukalt lõpetatud – enne CSU lähtestamist on P-tööde sünkroonimine ootel kannetega soovitatav.
- **Kassaseadmest välja logimine –** kassatoiminguid ei toetata migreerimise ajal.
- **Kutsu tagasi ja tühista kõik peatatud kanded kassas** - peatatud kandeid ei säilitata lähtestamise osana.

> [!IMPORTANT]
> Äriskaala ühiku lähtestamise osana kaotatakse varasemad peatatud kanded ja neid ei saa tagasi kutsuda. 

Siin on, mis toimub lähtestamisperioodil:

- Pilves majutatud Ärikanalid ei tööta, välja arvatud juhul, kui lülitate kassa võrguühenduseta võimaluse sisse.
- Võrguühenduseta tööga müügikoha seadmetel on vähendatud funktsioone.
- Kõik jaemüügiserverist sõltuvad e-commerce’i kliendid katkevad.
- Commerce Scale Unitsis majutatud kanaleid (ise majutatud) ei mõjutata.
- Peakontori funktsioone see ei mõjuta.

Siin on, mis toimub pärast lähtestamist:

- Kõikide aktiveeritud müügikoha seadmete seadme aktiveerimise olek säilitatakse, mis tähendab, et seadmeid ei pea uuesti aktiveerima.
- Autonoomse riistvarajaama eksemplarid jätkavad tööd.
- Müügikoha kanali poole aruanded lähtestatakse ja need ei näita andmeid enne lähtestamist.
- Näita töölehe toimingut lähtestatakse samuti ja see ei näita andmeid enne lähtestamist.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
