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
ms.openlocfilehash: f852779d43beb3a43c6921a25d393ee00dff96d1
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777957"
---
# <a name="configure-the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliidese konfigureerimine

[!include [banner](../includes/banner.md)]

Töökoja tegevtöötajad kasutavad tootmisosakonna käivitusliidest, et registreerida oma igapäevatööd, näiteks töö alustamise aega, töö tagasiside aruandeid, kaudsete tegevuste registreerimisi ja puudumiste aruandeid. Need registreeringud on jälgimisprotsessi ja tootmistellimuste kulude ning töötajate palga arvutamise aluseks.

Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele. Järgmisena on toodud mõned kasutuse näited.

- Ettevõtte fuajees olevas seadmes registreerivad töötajad end tööle tulles sisse ja töölt lahkudes välja.
- Tootmisjaoskonnas oleval seadmel registreerivad operaatorid, kui nad alustavad ja lõpetavad tööd. Samuti registreerivad nad vaheajad ja kaudsed tegevused.

Selles teemas kirjeldatakse mitmesuguseid võimalusi töökaardi seadmete konfigureerimiseks.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Tootmisosakonna käivitusliidese ja sellega seotud valikuliste funktsioonide sisselülitamine

Tootmisosakonna käivitusliides ja mitmed selles teemas kirjeldatud valikulised sätted tuleb süsteemis enne kasutamist sisse lülitada. Kasutage [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et lülitada sisse vajaduse järgi mõned või kõik järgmistes jaotistes kirjeldatud funktsioonidest.

### <a name="the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliides

See on peamine funktsioon, mida selles teemas kirjeldatakse. Tarneahela halduse versiooni 10.0.21 puhul lülitatakse see vaikimisi sisse. Sellega lisatakse tootmisosakonna käivitusliides teie süsteemile. Selle lubamiseks lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- Tootmisosakonna käivitus

### <a name="generate-license-plates"></a>Litsentsiplaatide loomine

Need funktsioonid muudavad litsentsiplaadi funktsioonid tootmisosakonna käivitusliidese jaoks kättesaadavaks. Kui soovite neid kasutada, lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. Töökaardi seadmesse lisatud litsentsiplaat lõpetatuna teatamiseks (tarneahela halduse versiooniga 10.0.21 lülitatakse see funktsioon vaikimisi sisse.)
1. Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis

### <a name="print-labels"></a>Prindi sildid

Need funktsioonid muudavad siltide printimise funktsioonid tootmisosakonna käivitusliidese jaoks kättesaadavaks. Kui soovite neid kasutada, lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. Töökaardi seadmesse lisatud litsentsiplaat lõpetatuna teatamiseks (tarneahela halduse versiooniga 10.0.21 lülitatakse see funktsioon vaikimisi sisse.)
1. Sildi printimine töökaardi vahendilt

### <a name="allow-locking-the-touch-screen"></a>Puuteekraani lukustamise lubamine

Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. See lisab nupu tootmispinna käivitamise liidesele, mis võimaldab töötajatel puuteekraani lähtestada. Kui soovite seda kasutada, veenduge, et funktsioonihalduses on järgmine funktsioon sisse [...](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lülitatud:

- Funktsioon töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks puhastada

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese varahoolduse funktsioon

See funktsioon lisab tootmisosakonna täideviimisliidesele varahalduse vahekaardi. Töötajad saavad kasutada seda vahekaarti, et valida vara, mis on ühendatud tööloendi valitud filtriga masinaressursiga. Valitud masina vara puhul saab töötaja vaadata vara olekut ja seisundit loenduri väärtustest kuni nelja valitud loenduri puhul. Kui soovite seda funktsiooni kasutada, lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- Tootmisosakonna täideviimisliidese varahoolduse funktsioon

### <a name="enable-job-search"></a>Luba tööotsing

See funktsioon võimaldab lisada tööde loendisse otsinguvälja. Töötajad saavad leida konkreetse töö, sisestades töö ID või otsides kõik konkreetse tellimuse tööd, sisestades tellimuse ID. Töötajad saavad sisestada ID võtmeklahvistikuga või vöötkoodi skannides. Kui soovite seda kasutada, lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- Tootmisosakonna täideviimisliidese töö otsing

### <a name="enable-reporting-on-co-products-and-by-products"></a>Lubage kaas- ja kõrvalsaaduste aruandlus

See funktsioon võimaldab töötajatel kasutada partiitellimuste edenemisest teatamiseks tootmispõranda täitmisliidest. See aruandlus hõlmab kaas- ja kõrvalsaaduste aruandlust. Selle funktsiooni kasutamiseks lubage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmine funktsioon.

- Tootmisosakonna täideviimisliidese kaas- ja kõrvalsaaduste aruanne

## <a name="work-with-production-floor-execution-configurations"></a>Tootmisosakonna käivituskonfiguratsioonidega töötamine

Seadme konfiguratsioonide loomiseks ja haldamiseks avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**. Lehel **Tootmisosakonna käivituste konfigureerimine** kuvatakse olemasolevate konfiguratsioonide loend. Sellel lehel saate teha järgmisi toiminguid.

- Saate valida kuvamiseks ja redigeerimiseks mis tahes vasakus veerus loetletud tootmisosakonna konfiguratsiooni.
- Valige toimingupaanil suvand **Uus**, et lisada loetellu uus seadme konfiguratsioon. Seejärel sisestage uue konfiguratsiooni tuvastamiseks nimi väljale **Konfiguratsioon**. Sisestatav nimi peab olema kõikide seadme konfiguratsioonide seas ainulaadne ja seda ei saa hiljem redigeerida.

Järgmisena konfigureerige valitud seadme konfiguratsiooni erinevad sätted. Saadaval on järgmised väljad.

- **Ainult sisse- ja väljaregistreerimine** – määrake selle suvandi väärtuseks *Jah*, et luua lihtsustatud liides, mis pakub ainult sisse- ja väljaregistreerimise funktsiooni. See keelab enamiku muid suvandeid sellel lehel. Enne selle suvandi lubamist peate eemaldama kõik read kiirkaardil **Vahekaardi valimine**.
- **Luba otsing** - Seadke see suvand valikule *Jah* et kaasata tööde loendis otsinguväli. Töötajad saavad leida konkreetse töö, sisestades töö ID või otsides kõik konkreetse tellimuse tööd, sisestades tellimuse ID. Töötajad saavad sisestada ID võtmeklahvistikuga või vöötkoodi skannides.
- **Koguse teatamine väljaregistreerimisel** – määrake suvandi väärtuseks *Jah*, et paluda töötajatel anda käimasolevate tööde kohta väljaregistreerimisel tagasisidet. Kui suvandi väärtuseks on seatud *Ei*, siis töötajatel seda teha ei paluta.
- **Lukusta töövõtja** – kui selle suvandi väärtuseks on seatud *Ei*, siis registreeritakse töötajad välja kohe pärast registreerimist (nt uus töö). Seade naaseb seejärel sisselogimislehele. Kui suvandi väärtuseks on seatud *Jah*, siis jäävad töötajad töökaardi seadmesse sisselogituks. Töötaja saab siiski käsitsi välja logida, et teine töötaja saaks sisse logida, kui töökaardi seade jätkab sama süsteemikasutaja kontoga töötamist. Lisateavet nende kontotüüpide kohta leiate jaotisest [Määratud kasutajad](config-job-card-device.md#assigned-users).
- **Tegeliku registreerimisaja kasutamine** – seadke suvandi väärtuseks *Jah*, et iga uue registreeringu aeg oleks samaväärne täpse ajaga, mil töötaja registreeringu esitas. Kui selle suvandi väärtuseks on seatud *Ei*, kasutatakse selle asemel sisselogimisaega. Tavaliselt võiks selle väärtuseks olla *Jah*, kui olete seadnud suvandite **Lukusta töötaja** ja/või **Üksik töötaja** väärtuseks *Jah* juhul, töötajad jäävad sageli pikemaks ajaks sisselogituks.
- **Üksik töötaja** – seadke väärtuseks *Jah*, kui iga töökaardi seadet, kus see konfiguratsioon on aktiivne, kasutab ainult üks töötaja. Kui suvandi väärtuseks on seatud *Jah*, siis seatakse suvandi **Lukusta töötaja** väärtuseks automaatselt *Jah*. Lisaks eemaldab see säte töötajalt kohustuse (ja võimaluse) logida sisse pääsme ID (või sarnase ID) abil. Selle asemel logib töötaja Microsoft Dynamics 365 Supply Chain Management i sisse süsteemi kasutajakonto kaudu, mis on seotud *ajaliselt registreeritud töötajaga* (tabelis *töötajad*), ning ta logitakse samal ajal kõnealuse töötajana töökaardi seadmesse sisse.
- **Luba puuteekraani lukustamine** – seadke väärtuseks *Jah*, et võimaldada töötajatel lukustada töökaardi seadme puuteekraan, et nad saaksid seda puhastada. Kui suvandi väärtuseks on seatud *Jah*, lisatakse seadme sisselogimislehele nupp **Ekraani lukustamine puhastamiseks**. Kui töötaja valib selle nupu, siis lukustub puuteekraan ajutiselt, et ennetada soovimatuid sisendeid. Kuvatakse ka taimer. Siis saab töötaja ohutult seadet ja selle ekraani puhastada. Kui taimer lõpetab, siis tehakse puuteekraan automaatselt lukust lahti.
- **Ekraaniluku kestus** – kui suvandi **Luba puuteekraani lukustamine** väärtuseks on seatud *Jah*, siis kasutage seda suvandit, et määratleda, mitu sekundit peaks puuteekraan puhastamiseks lukustatud olema. Kestus peab olema vahemikus 5–120 sekundit.
- **Loo litsentsiplaat** – seadke suvandi väärtuseks *Jah*, et luua uus litsentsiplaat iga kord, kui töötaja kasutab töökaardi seadet töö lõpetamisest teatamiseks. Identifitseerimisnumber luuakse lehel **Laohalduse parameetrid** seadistatud numbriseeria alusel. Kui suvandi väärtuseks on seatud *Ei*, siis peavad töötajad määratlema lõpetamisest teatamisel olemasoleva litsentsiplaadi.
- **Prindi silt** – seadke suvandi väärtuseks *Jah*, et printida litsentsiplaadi silt, kui töötaja kasutab töökaardi seadet lõpetamisest teatamiseks. Sildi konfiguratsioon on seadistatud dokumendi marsruudivalikus, nagu on kirjeldatud teemas [Identifitseerimisnumbri siltide dokumendi marsruudivaliku paigutus](../warehousing/document-routing-layout-for-license-plates.md).
- **Vahekaartide valimine**  – Kasutage selles jaotises olevaid sätteid, et valida, millised vahekaardid tootmisosakonna käivitusliides kuvab, kui see konfiguratsioon on aktiivne. Saate kujundada nii palju vahekaarte kui vaja ja seejärel lisada ja korraldada neid siin vastavalt vajadusele. Üksikasjalikumat teavet selle kohta, kuidas kujundada vahekaarte ja siinseid sätteid kasutada, leiate teemast [Tootmisosakonna käivitusliidese kujundamine](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Töökonfiguratsioonide puhastamine

Kui tootmisjaoskonna haldur seadistab tootmiosakonna käivitusliidese, valivad nad konfiguratsiooni ja tööfiltri. Need valikud talletatakse Supply Chain Managementi viitetabelis ja brauser kasutab kohalikus küpsises talletatud ID-d, et leida selles tabelis õige rida. Tabel logib ka kuupäeva ja kellaaja, mil töötaja igasse seadmesse viimati sisse logis.

Pakett-töö puhastab regulaarselt viitetabeli kirjeid seadmetel, kus pole viimase 60 päeva jooksul ühtegi toimingut logitud. Järgmiste etappide abil saate kirjeid ka käsitsi puhastada.

1. Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**.
1. Valige toimingupaanil **Kliendi konfiguratsioonide puhastamine**.
1. Määrake dialoogiboksis **Kliendi konfiguratsioonide puhastamine** väljale **Päevade arv** passiivsete päevade arv (enne tänast), mida arvesse võtta. Saate eemaldada kõik konfiguratsioonid ja sisselogimise kirjed seadmetel, mis pole olnud selle aja jooksul aktiivsed.
1. Valige **OK**, et puhastada asjakohased konfiguratsioonid sätte **Päevade arv** põhjal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
