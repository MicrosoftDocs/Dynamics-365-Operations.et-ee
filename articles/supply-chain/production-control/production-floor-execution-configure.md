---
title: Tootmisosakonna täideviimisliidese konfigureerimine
description: See artikkel kirjeldab, kuidas luua tootmispinna täitmisliidesele üks või mitu konfiguratsiooni. Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele.
author: johanhoffmann
ms.date: 11/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 641b293617df608bc07b97c077dbcd05664f8e2a
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748682"
---
# <a name="configure-the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliidese konfigureerimine

[!include [banner](../includes/banner.md)]

Töökoja tegevtöötajad kasutavad tootmisosakonna käivitusliidest, et registreerida oma igapäevatööd, näiteks töö alustamise aega, töö tagasiside aruandeid, kaudsete tegevuste registreerimisi ja puudumiste aruandeid. Need registreeringud on jälgimisprotsessi ja tootmistellimuste kulude ning töötajate palga arvutamise aluseks.

Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele. Järgmisena on toodud mõned kasutuse näited.

- Ettevõtte fuajees olevas seadmes registreerivad töötajad end tööle tulles sisse ja töölt lahkudes välja.
- Tootmisjaoskonnas oleval seadmel registreerivad operaatorid, kui nad alustavad ja lõpetavad tööd. Samuti registreerivad nad vaheajad ja kaudsed tegevused.

See artikkel kirjeldab erinevaid valikuid tootmispinna täitmisliidese konfigureerimiseks igale seadmele, mida teie saidil kasutatakse.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Tootmisosakonna käivitusliidese ja sellega seotud valikuliste funktsioonide sisselülitamine

Tootmispinna täitmisliides ja mitmed selles artiklis kirjeldatud valikulised sätted tuleb enne nende kasutamist süsteemi jaoks sisse lülitada. Kasutage [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et lülitada sisse vajaduse järgi mõned või kõik järgmistes jaotistes kirjeldatud funktsioonidest.

### <a name="the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliides

See on selles artiklis kirjeldatud peamine funktsioon, mis on kõigi selles jaotises mainitud funktsioonide eeltingimus. Tarneahela halduse 10.0.25 puhul on see kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides Tootmispinna käivitamise funktsiooni Funktsioonihalduse tööruumis.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="generate-license-plates"></a>Litsentsiplaatide loomine

Need funktsioonid muudavad litsentsiplaadi funktsioonid tootmisosakonna käivitusliidese jaoks kättesaadavaks. Kui soovite neid kasutada, lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. *Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat*<br>(Tarneahela halduse versiooni 10.0.21 puhul lülitatakse see funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon kohustuslik.)
1. *Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis*<br>(Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon kohustuslik.)

### <a name="print-labels"></a>Prindi sildid

Need funktsioonid muudavad siltide printimise funktsioonid tootmisosakonna käivitusliidese jaoks kättesaadavaks. Kui soovite neid kasutada, lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. *Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat*<br>(Tarneahela halduse versiooni 10.0.21 puhul lülitatakse see funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon kohustuslik.)
1. *Sildi printimine töökaardi vahendilt*<br>(Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon kohustuslik.)

### <a name="allow-locking-the-touch-screen"></a>Puuteekraani lukustamise lubamine

See funktsioon võimaldab töötajatel puuteekraani lukustada, et nad saaksid seda saniteerida.

Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsiooni töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks funktsioonihalduse*[tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kasteerida.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese varahoolduse funktsioon

See funktsioon lisab tootmisosakonna täideviimisliidesele varahalduse vahekaardi. Töötajad saavad kasutada seda vahekaarti, et valida vara, mis on ühendatud tööloendi valitud filtriga masinaressursiga. Valitud masina vara puhul saab töötaja vaadata vara olekut ja seisundit loenduri väärtustest kuni nelja valitud loenduri puhul.

Tarneahela halduse versiooni 10.0.25 puhul lülitatakse see funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides tootmispinna käivitamise liidese funktsiooni jaoks Põhivarahalduse funktsioone Funktsioonihalduse tööruumis.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="job-search"></a>Tööotsing

See funktsioon võimaldab lisada tööde loendisse otsinguvälja. Töötajad saavad leida konkreetse töö, sisestades töö ID või otsides kõik konkreetse tellimuse tööd, sisestades tellimuse ID. Töötajad saavad sisestada ID võtmeklahvistikuga või vöötkoodi skannides.

Tarneahela halduse versiooni 10.0.25 puhul lülitatakse see funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides tootmispinna käivitusliidese funktsiooni Tööotsingust Funktsioonihalduse tööruumis.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="report-on-co-products-and-by-products"></a>Aruanne kaastoodete ja kaastoodete kohta

See funktsioon võimaldab töötajatel kasutada partiitellimuste edenemisest teatamiseks tootmispõranda täitmisliidest. See aruandlus hõlmab kaas- ja kõrvalsaaduste aruandlust.

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul lülitatakse funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja *lülitada, otsides kaastoodete ja by-toodete*[aruannet tootmisjuhtimise liidese funktsioonist Funktsioonihalduse tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Kuva seeria-, partii- ja litsentsiplaadinumbrid

See funktsioon pakub täiustatud kogemust seeria-, partii- ja litsentsiplaadinumbrite loendite vaatamiseks tootmispinna käivitamise liideses. Kuvamismuudatused kaardivaates, mis näitab piiratud arvu märke loendivaatesse, mis annab täisväärtuste näitamiseks piisavalt ruumi. Loend võimaldab ka otsida kindlaid numbreid.

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.25 puhul lülitatakse funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse ja välja lülitada, otsides tootmispinna käivitamise liidese funktsioonist Seeria-,*[partii](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)- ja litsentsiplaadi numbreid Funktsioonihalduse tööruumis.

Tarneahela halduse versiooni 10.0.25 puhul lülitatakse see funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse *või välja lülitada, otsides funktsioonihalduse tööruumis tootmispinna käivitamise liidese funktsioonist täielikke seeria-,*[partii- ja litsentsiplaadi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) numbreid.

### <a name="register-material-consumption"></a>Materjali tarbimise registreerimine

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

See funktsioon võimaldab töötajatel kasutada tootmispinna käivitamise liidest materjalitarbimise, partiinumbrite ja seerianumbrite registreerimiseks. Mõned tootjad, eriti need, mis on protsessitööstuses, peavad eraldi registreerima materjali hulga, mida tarbitakse iga partii või tootmistellimuse puhul. Töötajad võivad näiteks kaalu kasutada tarbimisel tarbitava materjali kaalu kaalumiseks. Täieliku materjalijälgitavuse tagamiseks peavad need organisatsioonid registreerima ka iga toote tootmiseks tarbitud partiinumbrid.

Funktsioonil on kaks versiooni. Need kaubad toetavad kaupu, mille *puhul ei ole* laohaldusprotsesse (WMS) lubatud. Teised toetavad KAUPU, mis on *WMS-i* kasutamiseks lubatud. Selle funktsiooni kasutamiseks lülitage sisse üks või mõlemad funktsioonihalduses (selles järjekorras) sõltuvalt sellest, kas teil on [WMS](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-i jaoks lubatud kaupu:

- *Materjali tarbimise registreerimine tootmisosakonna täideviimisliideses (mitte-WMS)*
- *(Eelvaade) Materjalikulu registreerimine tootmisosakonna käivitusliideses (WMS-loaga)*

> [!IMPORTANT]
> Saate kasutada ainult mitte-WMS-funktsiooni. Kuid WMS-i kasutamisel peate lubama mõlemad funktsioonid.

### <a name="report-on-catch-weight-items"></a>Tegeliku kaaluga kaupade aruanne

Töötajad saavad kasutada tootmispinna käivitamise liidest tegeliku kaalu kaupade partiitellimuste edenemise aruandeks. Partiitellimused luuakse valemitest, mille puhul saab määrata tegeliku kaalu kaubad valemiüksustena, kaastoodetena ja kaastoodetena. Valemit saab määratleda ka nii, et valemiread peaksid olema määratletud tegeliku kaalu jaoks määratletud koostisainete jaoks. Tegeliku kaalu kaubad kasutavad varude jälgimiseks kahte mõõtühiku ühikut: tegeliku kaalu kogus ja varude kogus. Näiteks võib toiduainetetööstuses määratleda karbistatud liha tegeliku kaalu kaubana, kus tegeliku kaalu kogust kasutatakse kastide arvu jälgimiseks ja varude kogust kasutatakse väljade kaalu jälgimiseks.

Selle funktsiooni kasutamiseks lülitage funktsioonihalduses sisse järgmine [funktsioon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Aruanne tegeliku kaalu üksuste kohta tootmisosakonna täideviimisliidesest*

### <a name="the-my-day-dialog"></a>Dialoog Minu päev

Dialoogiaken **Minu** päev annab töötajatele ülevaate nende igapäevastest registreerimistest ja jooksvatest saldodest tasustatud aja, tasustatud ületunnitöö, puudumiste ja tasustatud puudumiste kohta.

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul lülitatakse funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, *otsides tootmispinna käivitamise liidese funktsiooni "Minu päev"* vaadet Funktsioonihalduse [tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Meeskonnad

Kui samale tootmistööle on määratud mitu töötajat, saavad nad moodustada meeskonna. Meeskond võib määrata ühe töötaja piloodiks. Ülejäänud töötajatest saavad seejärel automaatselt selle piloodi abilised. Tulemuseks saadud meeskonna puhul peab ainult piloot registreerima töö oleku. Ajakirjed kehtivad kõigi töörühma liikmete kohta.

Selle funktsiooni kasutamiseks lülitage funktsioonihalduses sisse järgmine [funktsioon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tootmistöörühmad tootmisosakonna täideviimisliideses*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Tootmise juhtimise liidese lisakonfiguratsioon

See funktsioon lisab tootmise juhtimise lehe konfigureerimisele järgmiste **funktsioonide** sätted:

- Kui otsing on **lõpule viidud**, avaneb automaatselt dialoogiboks Alusta tööd.
- Kui otsing on **lõpetatud**, avaneb automaatselt dialoogiboks Aruande edenemine.
- Järelejäänud koguse eeltäitmine dialoogiboksi **Aruande edenemine**.
- Lubage materjalitarbimise korrigeerimised dialoogiboksis **Edenemise** aruanne. (See funktsioon nõuab ka funktsiooni *Registreerige materjalitarbimine tootmispinna käivitamise liidese (non-WMS) funktsioonis* .)
- Lubage otsingud projekti ID järgi.

Teave sätete kasutamise kohta antakse hiljem selles artiklis.

Selle funktsiooni kasutamiseks lülitage funktsioonihalduses sisse järgmine [funktsioon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tootmisosakonna täideviimisliidese täiendav konfiguratsioon*

### <a name="enable-the-my-jobs-tab"></a>Luba minu tööde vahekaart

Vahekaart **Minu** tööd lubab töötajatel hõlpsasti vaadata kõiki just neile määratud lugemata ja lõpetamata töid. See on kasulik ettevõtetele, kus tööd on mõnikord või alati määratud teatud töötajatele (inimressurssidele), mitte teist tüüpi ressurssidele (nt masinatele).

Selle funktsiooni kasutamiseks lülitage funktsioonihalduses sisse järgmine [funktsioon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tootmisosakonna täideviimisliidese vahekaart Minu tööd*

### <a name="enable-use-of-a-numpad-on-the-sign-in-page"></a>Luba numbriklahvistiku kasutamine sisselogimislehel

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

See funktsioon võimaldab administraatoritel lisada numbriklahvistiku juhtelementi tootmispinna käivitamise liidese sisselogimislehele. Töötajad saavad siis sisse logida numbriklahvistiku abil, et sisestada oma märkide ID või isiklik number.

Selle funktsiooni kasutamiseks lülitage funktsioonihalduses sisse järgmine [funktsioon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Luba sisselogimislehel numbriklahvistiku kasutamine*

## <a name="work-with-production-floor-execution-configurations"></a>Tootmisosakonna käivituskonfiguratsioonidega töötamine

Tootmispinna käivitamise konfiguratsioonide loomiseks ja säilitamiseks minge Tootmise juhtimise seadistuse **\>\>\> tootmise käivitamise konfigureerimiseks tootmispinna käivitamisele**. Lehel **Tootmisosakonna käivituste konfigureerimine** kuvatakse olemasolevate konfiguratsioonide loend. Sellel lehel saate teha järgmisi toiminguid.

- Saate valida kuvamiseks ja redigeerimiseks mis tahes vasakus veerus loetletud tootmisosakonna konfiguratsiooni.
- Tegevuspaanil valige **uus**, et lisada loendisse uus konfiguratsioon. Seejärel sisestage uue konfiguratsiooni tuvastamiseks nimi väljale **Konfiguratsioon**. Sisestatav nimi peab olema kõigi konfiguratsioonide seas kordumatu ja te ei saa seda hiljem redigeerida. **Väljale Kirjeldus** saate valikuliselt sisestada konfiguratsiooni kirjelduse.

Seejärel konfigureerige valitud konfiguratsiooni erinevad sätted, nagu kirjeldatud järgmistes alamjaotistes.

### <a name="the-general-fasttab"></a>Kiirkaart Üldine

Järgmised sätted on saadaval kiirkaardil **Üldine**:

- **Ainult sisse- ja väljaregistreerimine** – määrake selle suvandi väärtuseks *Jah*, et luua lihtsustatud liides, mis pakub ainult sisse- ja väljaregistreerimise funktsioone. See säte keelab enamiku teistest selle lehe valikutest. Enne selle suvandi lubamist peate eemaldama kõik read kiirkaardil **Vahekaardi valimine**.
- **Otsingu lubamine** : määrake see suvand valikule *Jah*, et kaasata tööde loendis otsinguväli. Töötajad saavad leida konkreetse töö, sisestades töö ID või nad saavad leida kõik konkreetse tellimuse tööd, sisestades tellimuse ID. Töötajad saavad sisestada ID võtmeklahvistikuga või vöötkoodi skannides.
- **Luba otsing projekti ID** järgi : *seadistage* see valik valikule Jah, et lubada töötajatel otsida projekti ID järgi (lisaks töö ID-le ja tellimuse ID-le) tootmisjuhtimise käivitamise liidese otsinguväljal. Saate selle suvandi seada väärtusele *Jah* ainult siis, kui suvandi **Luba** otsing väärtuseks on samuti seatud *Jah*.
- **Automaatavamiseks avanev dialoogiaken** – kui see *valik* on seatud väärtusele Jah, avatakse automaatselt dialoogiaken Alusta tööd, **kui** töötajad kasutavad töö otsimiseks otsinguriba.
- **Automaatavamiseks aruande edenemise dialoog** – kui see *valik on seatud väärtusele Jah*, avaneb automaatselt aruande edenemise dialoogiboks, **kui** töötajad kasutavad töö otsimiseks otsinguriba.
- **Materjali korrigeerimise lubamine**: seadke see valik valikule *Jah,* et lubada nuppu **Materjali korrigeerimine** dialoogiaknas **Aruande** edenemine. Töötajad saavad selle nupu valida, et korrigeerida töö materjali tarbimist.
- **Koguse teatamine väljaregistreerimisel** – määrake suvandi väärtuseks *Jah*, et paluda töötajatel anda käimasolevate tööde kohta väljaregistreerimisel tagasisidet. Kui suvandi väärtuseks on seatud *Ei*, siis töötajatel seda teha ei paluta.
- **Lukusta töövõtja** – kui selle suvandi väärtuseks on seatud *Ei*, siis registreeritakse töötajad välja kohe pärast registreerimist (nt uus töö). Liides naaseb siis sisselogimislehele. Kui see valik on seatud valikule *Jah*, siis jäävad töötajad tootmispinna käivitamise liidesesse sisse. Kuid töötaja saab käsitsi välja logida, nii et teine töötaja saab sisse logida ajal, kui tootmispinna käivitamise liides töötab sama süsteemi kasutajakonto all. Lisateavet nende kontotüüpide kohta leiate jaotisest [Määratud kasutajad](config-job-card-device.md#assigned-users).
- **Tegeliku registreerimisaja kasutamine** – seadke suvandi väärtuseks *Jah*, et iga uue registreeringu aeg oleks samaväärne täpse ajaga, mil töötaja registreeringu esitas. Kui selle suvandi väärtuseks on seatud *Ei*, kasutatakse selle asemel sisselogimisaega. Tavaliselt võiks selle väärtuseks olla *Jah*, kui olete seadnud suvandite **Lukusta töötaja** ja/või **Üksik töötaja** väärtuseks *Jah* juhul, töötajad jäävad sageli pikemaks ajaks sisselogituks.
- **Üksiktöötaja** – määrake selle suvandi väärtuseks *Jah,* kui ainult üks töötaja kasutab iga tootmispinna käivitamise liidest, kus see konfiguratsioon on aktiivne. Kui suvandi väärtuseks on seatud *Jah*, siis seatakse suvandi **Lukusta töötaja** väärtuseks automaatselt *Jah*. Lisaks eemaldab see säte töötajalt kohustuse (ja võimaluse) logida sisse pääsme ID (või sarnase ID) abil. Selle asemel logib Dynamics 365 Supply Chain Management *töötaja* Microsofti sisse, kasutades süsteemi kasutajakontot, mis on seotud registreeritud ajaga (*töötajate* tabelist) ja logib sisse tootmispinna täitmisliidesesse, kus see töötaja korraga on.
- **Luba numbriklahvistik**: *määrake* see valik valikule Jah, et lisada numbriklahvistik sisselogimiskuvale, mis võimaldab töötajatel sisestada oma märkide ID või isikliku numbri, kasutades puuteekraani numbriklahvistikku. Valikuks määrake Ei *,* et peita numbriklahvistik.
- **Puuteekraani lukustamise** võimaldamine – *seadke* see valik valikule Jah, et lubada töötajatel lukustada tootmis floori täitmisliidese puuteekraani, et nad saaks seda saniteerida. Kui see valik on seadistatud *valikule* **Jah, lisatakse sisselogimislehele** lukustusekraan nupu lähtestamiseks. Kui töötaja valib selle nupu, siis lukustub puuteekraan ajutiselt, et ennetada soovimatuid sisendeid. Kuvatakse ka taimer. Siis saab töötaja ohutult seadet ja selle ekraani puhastada. Kui taimer lõpetab, siis tehakse puuteekraan automaatselt lukust lahti.
- **Ekraaniluku kestus** – kui suvandi **Luba puuteekraani lukustamine** väärtuseks on seatud *Jah*, siis kasutage seda suvandit, et määratleda, mitu sekundit peaks puuteekraan puhastamiseks lukustatud olema. Kestus peab olema vahemikus 5–120 sekundit.
- **Loo litsentsiplaat** : määrake see valik väärtusele *Jah*, et luua uus litsentsiplaat iga kord, kui töötaja kasutab tootmise juhtimise liidest lõpetatuna näitamiseks. Identifitseerimisnumber luuakse lehel **Laohalduse parameetrid** seadistatud numbriseeria alusel. Kui suvandi väärtuseks on seatud *Ei*, siis peavad töötajad määratlema lõpetamisest teatamisel olemasoleva litsentsiplaadi.
- **Prindi silt**: määrake see valik valikule *Jah*, et printida litsentsiplaadi silt, kui töötaja kasutab tootmise juhtimise liidest lõpetatuna näitamiseks. Sildi konfiguratsioon seadistatakse dokumendi marsruudivalikul, nagu on kirjeldatud dokumendi protsessisildi [paigutustes](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Vahekaardi valiku kiirkaart

Kasutage vahekaardi valiku kiirkaardi **sätteid,** et valida, milliseid vahekaarte tootmise juhtimise liides peaks näitama, kui praegune konfiguratsioon on aktiivne. Saate kujundada nii palju vahekaarte kui vaja ning seejärel lisada ja järjestada neid vastavalt vajadusele, kasutades nuppe kiirkaardi tööriistaribal. Lisateavet vahekaartide kujundamise ja selle sätetega töö kohta vt [Tootmise juhtimise käivitamise liidese kujundamine](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Aruande edenemise kiirkaart

Järgmised sätted on saadaval kiirkaardil **Aruande edenemine**:

- **Materjali korrigeerimise lubamine**: seadke see suvand valikule *Jah,* et kaasata **nupp Materjali korrigeerimine** **dialoogiaknas** Aruande edenemine. Töötajad saavad selle nupu valida, et korrigeerida töö materjali tarbimist.
- **Järelejääv** vaikekogus: määrake see *suvand* suvandile Jah, et täita tootmistöö eeldatav järelejäänud kogus aruande **edenemise dialoogiaknas**.

## <a name="clean-up-job-configurations"></a>Töökonfiguratsioonide puhastamine

Kui tootmisjaoskonna haldur seadistab tootmiosakonna käivitusliidese, valivad nad konfiguratsiooni ja tööfiltri. Need valikud talletatakse Supply Chain Managementi viitetabelis ja brauser kasutab kohalikus küpsises talletatud ID-d, et leida selles tabelis õige rida. Tabel logib ka kuupäeva ja kellaaja, mil töötaja igasse seadmesse viimati sisse logis.

Pakett-töö puhastab regulaarselt viitetabeli kirjeid seadmetel, kus pole viimase 60 päeva jooksul ühtegi toimingut logitud. Järgmiste etappide abil saate kirjeid ka käsitsi puhastada.

1. Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**.
1. Valige toimingupaanil **Kliendi konfiguratsioonide puhastamine**.
1. Määrake dialoogiboksis **Kliendi konfiguratsioonide puhastamine** väljale **Päevade arv** passiivsete päevade arv (enne tänast), mida arvesse võtta. Saate eemaldada kõik konfiguratsioonid ja sisselogimise kirjed seadmetel, mis pole olnud selle aja jooksul aktiivsed.
1. Valige **OK**, et puhastada asjakohased konfiguratsioonid sätte **Päevade arv** põhjal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
