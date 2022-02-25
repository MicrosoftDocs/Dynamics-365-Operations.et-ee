---
title: Tootmisosakonna käivitusliidese konfigureerimine
description: Selles teemas kirjeldatakse, kuidas luua ühte või mitut konfiguratsiooni tootmisosakonna käivitusliidesele. Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele.
author: johanhoffmann
ms.date: 10/05/2020
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
ms.openlocfilehash: 30f36ccf967c47d6a034c00544d45cdfdc3d1907
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103384"
---
# <a name="configure-the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliidese konfigureerimine

[!include [banner](../includes/banner.md)]

Töökoja tegevtöötajad kasutavad tootmisosakonna käivitusliidest, et registreerida oma igapäevatööd, näiteks töö alustamise aega, töö tagasiside aruandeid, kaudsete tegevuste registreerimisi ja puudumiste aruandeid. Need registreeringud on jälgimisprotsessi ja tootmistellimuste kulude ning töötajate palga arvutamise aluseks.

Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele. Järgmisena on toodud mõned kasutuse näited.

- Ettevõtte fuajees olevas seadmes registreerivad töötajad end tööle tulles sisse ja töölt lahkudes välja.
- Tootmisjaoskonnas oleval seadmel registreerivad operaatorid, kui nad alustavad ja lõpetavad tööd. Samuti registreerivad nad vaheajad ja kaudsed tegevused.

See teema kirjeldab erinevaid valikuid tootmispinna täitmisliidese konfigureerimiseks iga teie juures kasutusel seadme jaoks.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Tootmisosakonna käivitusliidese ja sellega seotud valikuliste funktsioonide sisselülitamine

Tootmisosakonna käivitusliides ja mitmed selles teemas kirjeldatud valikulised sätted tuleb süsteemis enne kasutamist sisse lülitada. Kasutage [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et lülitada sisse vajaduse järgi mõned või kõik järgmistes jaotistes kirjeldatud funktsioonidest.

### <a name="the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliides

See on selles teemas kirjeldatud peamine funktsioon, mis on kõigi selles jaotises mainitud funktsioonide eeltingimus. Tarneahela halduse 10.0.25 puhul on see kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides Tootmispinna käivitamise funktsiooni Funktsioonihalduse tööruumis.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

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

See funktsioon lisab tootmisosakonna täideviimisliidesele varahalduse vahekaardi. Töötajad saavad kasutada seda vahekaarti, et valida vara, mis on ühendatud tööloendi valitud filtriga masinaressursiga. Valitud masina vara puhul saab töötaja vaadata vara olekut ja seisundit loenduri väärtustest kuni nelja valitud loenduri puhul. Kui soovite seda funktsiooni kasutada, lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- *Tootmisosakonna täideviimisliidese varahoolduse funktsioon*<br>(Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon vaikimisi sisse lülitatud.)

### <a name="enable-job-search"></a>Luba tööotsing

See funktsioon võimaldab lisada tööde loendisse otsinguvälja. Töötajad saavad leida konkreetse töö, sisestades töö ID või otsides kõik konkreetse tellimuse tööd, sisestades tellimuse ID. Töötajad saavad sisestada ID võtmeklahvistikuga või vöötkoodi skannides. Kui soovite seda kasutada, lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- *Tootmisosakonna täideviimisliidese töö otsing*<br>(Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon vaikimisi sisse lülitatud.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Lubage kaas- ja kõrvalsaaduste aruandlus

See funktsioon võimaldab töötajatel kasutada partiitellimuste edenemisest teatamiseks tootmispõranda täitmisliidest. See aruandlus hõlmab kaas- ja kõrvalsaaduste aruandlust. Selle funktsiooni kasutamiseks lubage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmine funktsioon.

- *Tootmisosakonna täideviimisliidese kaas- ja kõrvalsaaduste aruanne*

## <a name="work-with-production-floor-execution-configurations"></a>Tootmisosakonna käivituskonfiguratsioonidega töötamine

Tootmispinna käivitamise konfiguratsioonide loomiseks ja säilitamiseks minge Tootmise juhtimise seadistuse **\>\>\> tootmise käivitamise konfigureerimiseks tootmispinna käivitamisele**. Lehel **Tootmisosakonna käivituste konfigureerimine** kuvatakse olemasolevate konfiguratsioonide loend. Sellel lehel saate teha järgmisi toiminguid.

- Saate valida kuvamiseks ja redigeerimiseks mis tahes vasakus veerus loetletud tootmisosakonna konfiguratsiooni.
- **Uue** konfiguratsiooni lisamiseks loendisse valige tegevuspaanil uus. Seejärel sisestage uue konfiguratsiooni tuvastamiseks nimi väljale **Konfiguratsioon**. Sisestatav nimi peab olema kõigi konfiguratsioonide seas kordumatu ja te ei saa seda hiljem redigeerida.

Seejärel konfigureerige valitud konfiguratsiooni erinevad sätted. Saadaval on järgmised väljad.

- **Ainult sisse- ja väljaregistreerimine** – määrake selle suvandi väärtuseks *Jah*, et luua lihtsustatud liides, mis pakub ainult sisse- ja väljaregistreerimise funktsiooni. See keelab enamiku muid suvandeid sellel lehel. Enne selle suvandi lubamist peate eemaldama kõik read kiirkaardil **Vahekaardi valimine**.
- **Luba otsing** - Seadke see suvand valikule *Jah* et kaasata tööde loendis otsinguväli. Töötajad saavad leida konkreetse töö, sisestades töö ID või otsides kõik konkreetse tellimuse tööd, sisestades tellimuse ID. Töötajad saavad sisestada ID võtmeklahvistikuga või vöötkoodi skannides.
- **Koguse teatamine väljaregistreerimisel** – määrake suvandi väärtuseks *Jah*, et paluda töötajatel anda käimasolevate tööde kohta väljaregistreerimisel tagasisidet. Kui suvandi väärtuseks on seatud *Ei*, siis töötajatel seda teha ei paluta.
- **Lukusta töövõtja** – kui selle suvandi väärtuseks on seatud *Ei*, siis registreeritakse töötajad välja kohe pärast registreerimist (nt uus töö). Liides naaseb siis sisselogimislehele. Kui see valik on seatud valikule *Jah*, siis jäävad töötajad tootmispinna käivitamise liidesesse sisse. Kuid töötaja saab käsitsi välja logida, nii et teine töötaja saab sisse logida ajal, kui tootmispinna käivitamise liides töötab sama süsteemi kasutajakonto all. Lisateavet nende kontotüüpide kohta leiate jaotisest [Määratud kasutajad](config-job-card-device.md#assigned-users).
- **Tegeliku registreerimisaja kasutamine** – seadke suvandi väärtuseks *Jah*, et iga uue registreeringu aeg oleks samaväärne täpse ajaga, mil töötaja registreeringu esitas. Kui selle suvandi väärtuseks on seatud *Ei*, kasutatakse selle asemel sisselogimisaega. Tavaliselt võiks selle väärtuseks olla *Jah*, kui olete seadnud suvandite **Lukusta töötaja** ja/või **Üksik töötaja** väärtuseks *Jah* juhul, töötajad jäävad sageli pikemaks ajaks sisselogituks.
- **Üksiktöötaja** – määrake selle suvandi väärtuseks *Jah,* kui ainult üks töötaja kasutab iga tootmispinna käivitamise liidest, kus see konfiguratsioon on aktiivne. Kui suvandi väärtuseks on seatud *Jah*, siis seatakse suvandi **Lukusta töötaja** väärtuseks automaatselt *Jah*. Lisaks eemaldab see säte töötajalt kohustuse (ja võimaluse) logida sisse pääsme ID (või sarnase ID) abil. Selle asemel logib Dynamics 365 Supply Chain Management *töötaja* Microsofti sisse, kasutades süsteemi kasutajakontot, mis on seotud registreeritud ajaga (*töötajate* tabelist) ja logib sisse tootmispinna täitmisliidesesse, kus see töötaja korraga on.
- **Puuteekraani lukustamise** võimaldamine – *seadke* see valik valikule Jah, et lubada töötajatel lukustada tootmis floori täitmisliidese puuteekraani, et nad saaks seda saniteerida. Kui see valik on seadistatud *valikule* **Jah, lisatakse sisselogimislehele** lukustusekraan nupu lähtestamiseks. Kui töötaja valib selle nupu, siis lukustub puuteekraan ajutiselt, et ennetada soovimatuid sisendeid. Kuvatakse ka taimer. Siis saab töötaja ohutult seadet ja selle ekraani puhastada. Kui taimer lõpetab, siis tehakse puuteekraan automaatselt lukust lahti.
- **Ekraaniluku kestus** – kui suvandi **Luba puuteekraani lukustamine** väärtuseks on seatud *Jah*, siis kasutage seda suvandit, et määratleda, mitu sekundit peaks puuteekraan puhastamiseks lukustatud olema. Kestus peab olema vahemikus 5–120 sekundit.
- **Loo litsentsiplaat** : määrake see valik väärtusele *Jah*, et luua uus litsentsiplaat iga kord, kui töötaja kasutab tootmise juhtimise liidest lõpetatuna näitamiseks. Identifitseerimisnumber luuakse lehel **Laohalduse parameetrid** seadistatud numbriseeria alusel. Kui suvandi väärtuseks on seatud *Ei*, siis peavad töötajad määratlema lõpetamisest teatamisel olemasoleva litsentsiplaadi.
- **Prindi silt**: määrake see valik valikule *Jah*, et printida litsentsiplaadi silt, kui töötaja kasutab tootmise juhtimise liidest lõpetatuna näitamiseks. Sildi konfiguratsioon on seadistatud dokumendi marsruudivalikus, nagu on kirjeldatud teemas [Identifitseerimisnumbri siltide dokumendi marsruudivaliku paigutus](../warehousing/document-routing-layout-for-license-plates.md).
- **Vahekaartide valimine**  – Kasutage selles jaotises olevaid sätteid, et valida, millised vahekaardid tootmisosakonna käivitusliides kuvab, kui see konfiguratsioon on aktiivne. Saate kujundada nii palju vahekaarte kui vaja ja seejärel lisada ja korraldada neid siin vastavalt vajadusele. Üksikasjalikumat teavet selle kohta, kuidas kujundada vahekaarte ja siinseid sätteid kasutada, leiate teemast [Tootmisosakonna käivitusliidese kujundamine](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Töökonfiguratsioonide puhastamine

Kui tootmisjaoskonna haldur seadistab tootmiosakonna käivitusliidese, valivad nad konfiguratsiooni ja tööfiltri. Need valikud talletatakse Supply Chain Managementi viitetabelis ja brauser kasutab kohalikus küpsises talletatud ID-d, et leida selles tabelis õige rida. Tabel logib ka kuupäeva ja kellaaja, mil töötaja igasse seadmesse viimati sisse logis.

Pakett-töö puhastab regulaarselt viitetabeli kirjeid seadmetel, kus pole viimase 60 päeva jooksul ühtegi toimingut logitud. Järgmiste etappide abil saate kirjeid ka käsitsi puhastada.

1. Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**.
1. Valige toimingupaanil **Kliendi konfiguratsioonide puhastamine**.
1. Määrake dialoogiboksis **Kliendi konfiguratsioonide puhastamine** väljale **Päevade arv** passiivsete päevade arv (enne tänast), mida arvesse võtta. Saate eemaldada kõik konfiguratsioonid ja sisselogimise kirjed seadmetel, mis pole olnud selle aja jooksul aktiivsed.
1. Valige **OK**, et puhastada asjakohased konfiguratsioonid sätte **Päevade arv** põhjal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
