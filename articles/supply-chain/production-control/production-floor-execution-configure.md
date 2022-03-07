---
title: Tootmisosakonna käivitusliidese konfigureerimine
description: Selles teemas kirjeldatakse, kuidas luua ühte või mitut konfiguratsiooni tootmisosakonna käivitusliidesele. Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d34f9c235df480658a0935d731f7267a87894067
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556310"
---
# <a name="configure-the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliidese konfigureerimine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Töökoja tegevtöötajad kasutavad tootmisosakonna käivitusliidest, et registreerida oma igapäevatööd, näiteks töö alustamise aega, töö tagasiside aruandeid, kaudsete tegevuste registreerimisi ja puudumiste aruandeid. Need registreeringud on jälgimisprotsessi ja tootmistellimuste kulude ning töötajate palga arvutamise aluseks.

Tootmisosakonna käivitusliidese avamisel laadib see automaatselt valitud konfiguratsiooni ja tööfiltri, mis vastavad brauserile ja seadmele. Konfiguratsioonis seadistate poliitikad, mis peavad vastama konkreetsele kasutusele. Järgmisena on toodud mõned kasutuse näited.

- Ettevõtte fuajees olevas seadmes registreerivad töötajad end tööle tulles sisse ja töölt lahkudes välja.
- Tootmisjaoskonnas oleval seadmel registreerivad operaatorid, kui nad alustavad ja lõpetavad tööd. Samuti registreerivad nad vaheajad ja kaudsed tegevused.

Selles teemas kirjeldatakse mitmesuguseid võimalusi töökaardi seadmete konfigureerimiseks.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Tootmisosakonna käivitusliidese ja sellega seotud valikuliste funktsioonide sisselülitamine

Tootmisosakonna käivitusliides ja mitmed selles teemas kirjeldatud valikulised sätted tuleb süsteemis enne kasutamist sisse lülitada. Kasutage [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et lülitada sisse vajaduse järgi mõned või kõik järgmistes jaotistes kirjeldatud funktsioonidest.

### <a name="the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliides

See on peamine funktsioon, mida selles teemas kirjeldatakse. Sellega lisatakse tootmisosakonna käivitusliides teie süsteemile. Selle lubamiseks lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- Tootmisosakonna käivitus

### <a name="generate-license-plates"></a>Litsentsiplaatide loomine

Need funktsioonid muudavad litsentsiplaadi funktsioonid tootmisosakonna käivitusliidese jaoks kättesaadavaks. Kui soovite neid kasutada, lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat
1. Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis

### <a name="print-labels"></a>Prindi sildid

Need funktsioonid muudavad siltide printimise funktsioonid tootmisosakonna käivitusliidese jaoks kättesaadavaks. Kui soovite neid kasutada, lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat
1. Sildi printimine töökaardi vahendilt

### <a name="allow-locking-the-touch-screen"></a>Puuteekraani lukustamise lubamine

See funktsioon lisab nupu ootmisosakonna käivitusliidesele, mis võimaldab töötajatel puuteekraani puhastada. Kui soovite seda kasutada, lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- Funktsioon töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks puhastada

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese varahoolduse funktsioon

See funktsioon lisab tootmisosakonna täideviimisliidesele varahalduse vahekaardi. Töötajad saavad kasutada seda vahekaarti, et valida vara, mis on ühendatud tööloendi valitud filtriga masinaressursiga. Valitud masina vara puhul saab töötaja vaadata vara olekut ja seisundit loenduri väärtustest kuni nelja valitud loenduri puhul. Kui soovite seda funktsiooni kasutada, lülitage [funktsioonide halduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid.

- Tootmisosakonna täideviimisliidese varahoolduse funktsioon

## <a name="work-with-production-floor-execution-configurations"></a>Tootmisosakonna käivituskonfiguratsioonidega töötamine

Seadme konfiguratsioonide loomiseks ja haldamiseks avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**. Lehel **Tootmisosakonna käivituste konfigureerimine** kuvatakse olemasolevate konfiguratsioonide loend. Sellel lehel saate teha järgmisi toiminguid.

- Saate valida kuvamiseks ja redigeerimiseks mis tahes vasakus veerus loetletud tootmisosakonna konfiguratsiooni.
- Valige toimingupaanil suvand **Uus**, et lisada loetellu uus seadme konfiguratsioon. Seejärel sisestage uue konfiguratsiooni tuvastamiseks nimi väljale **Konfiguratsioon**. Sisestatav nimi peab olema kõikide seadme konfiguratsioonide seas ainulaadne ja seda ei saa hiljem redigeerida.

Järgmisena konfigureerige valitud seadme konfiguratsiooni erinevad sätted. Saadaval on järgmised väljad.

- **Ainult sisse- ja väljaregistreerimine** – määrake selle suvandi väärtuseks *Jah*, et luua lihtsustatud liides, mis pakub ainult sisse- ja väljaregistreerimise funktsiooni. See keelab enamiku muid suvandeid sellel lehel. Enne selle suvandi lubamist peate eemaldama kõik read kiirkaardil **Vahekaardi valimine**.
- **Koguse teatamine väljaregistreerimisel** – määrake suvandi väärtuseks *Jah*, et paluda töötajatel anda käimasolevate tööde kohta väljaregistreerimisel tagasisidet. Kui suvandi väärtuseks on seatud *Ei*, siis töötajatel seda teha ei paluta.
- **Lukusta töövõtja** – kui selle suvandi väärtuseks on seatud *Ei*, siis registreeritakse töötajad välja kohe pärast registreerimist (nt uus töö). Seade naaseb seejärel sisselogimislehele. Kui suvandi väärtuseks on seatud *Jah*, siis jäävad töötajad töökaardi seadmesse sisselogituks. Töötaja saab siiski käsitsi välja logida, et teine töötaja saaks sisse logida, kui töökaardi seade jätkab sama süsteemikasutaja kontoga töötamist. Lisateavet nende kontotüüpide kohta leiate jaotisest [Määratud kasutajad](config-job-card-device.md#assigned-users).
- **Tegeliku registreerimisaja kasutamine** – seadke suvandi väärtuseks *Jah*, et iga uue registreeringu aeg oleks samaväärne täpse ajaga, mil töötaja registreeringu esitas. Kui selle suvandi väärtuseks on seatud *Ei*, kasutatakse selle asemel sisselogimisaega. Tavaliselt võiks selle väärtuseks olla *Jah*, kui olete seadnud suvandite **Lukusta töötaja** ja/või **Üksik töötaja** väärtuseks *Jah* juhul, töötajad jäävad sageli pikemaks ajaks sisselogituks.
- **Üksik töötaja** – seadke väärtuseks *Jah*, kui iga töökaardi seadet, kus see konfiguratsioon on aktiivne, kasutab ainult üks töötaja. Kui suvandi väärtuseks on seatud *Jah*, siis seatakse suvandi **Lukusta töötaja** väärtuseks automaatselt *Jah*. Lisaks eemaldab see säte töötajalt kohustuse (ja võimaluse) logida sisse pääsme ID (või sarnase ID) abil. Selle asemel logib töötaja Microsoft Dynamics 365 Supply Chain Managementi sisse süsteemi kasutajakonto kaudu, mis on seotud *ajaliselt registreeritud töötajaga* (tabelis *töötajad*), ning ta logitakse samal ajal kõnealuse töötajana töökaardi seadmesse sisse.
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