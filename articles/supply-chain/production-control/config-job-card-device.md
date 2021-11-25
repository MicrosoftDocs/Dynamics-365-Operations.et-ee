---
title: Töökaardi konfigureerimine seadmetele
description: Selles teemas kirjeldatakse mitmesuguseid võimalusi töökaardi seadme konfigureerimiseks.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 0382e34664f20389c43e8dec4437f0078fa1f60a
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777736"
---
# <a name="configure-job-card-for-devices"></a>Töökaardi konfigureerimine seadmetele

[!include [banner](../includes/banner.md)]

Töökaardi seadet kasutavad tegevtöötajad, et registreerida oma igapäevatööd, nagu näiteks see, millal tööd alustati, töö tagasiside aruandlus, kaudsete tegevuste registreerimine ja puudumiste aruandlus. Need registreeringud on jälgimisprotsessi ja tootmistellimuste kulude ning töötajate palga arvutamise aluseks. Selles teemas kirjeldatakse mitmesuguseid võimalusi töökaardi seadmete konfigureerimiseks.

## <a name="enable-new-features-in-feature-management"></a>Uute funktsioonide lubamine funktsioonihalduses

Mõned selles teemas kirjeldatud sätted peavad teie süsteemis olema lubatud, enne kui need teile kättesaadavad on. Kasutage [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et lubada vajaduse järgi mõned või kõik järgmistest funktsioonidest.

### <a name="generate-license-plate"></a>Loo litsentsiplaat

Selle funktsiooni kättesaadavaks muutmiseks lubage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmised funktsioonid (järjekorras).

1. Töökaardi seadmesse lisatud litsentsiplaat lõpetatuna teatamiseks (tarneahela halduse versiooniga 10.0.21 lülitatakse see funktsioon vaikimisi sisse.)
1. Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis

### <a name="print-label"></a>Prindi silt

Selle funktsiooni kättesaadavaks muutmiseks lubage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmised funktsioonid (järjekorras).

1. Töökaardi seadmesse lisatud litsentsiplaat lõpetatuna teatamiseks (tarneahela halduse versiooniga 10.0.21 lülitatakse see funktsioon vaikimisi sisse.)
1. Sildi printimine töökaardi vahendilt

### <a name="allow-locking-of-touch-screen"></a>Puuteekraani lukustamise lubamine

Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. Kui soovite seda kasutada, veenduge, et funktsioonihalduses on järgmine funktsioon sisse [...](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lülitatud:

- Funktsioon töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks puhastada

## <a name="manage-your-device-configurations"></a>Seadme konfiguratsioonide haldamine

Seadme konfigureerimiseks avage **Tootmise juhtimine > Seadistamine > Tootmise käivitamine > Töökaardi konfigureerimine seadmete jaoks**. Avaneb leht **Töökaardi konfigureerimine seadmete jaoks**, kus on toodud olemasolevate konfiguratsioonide loetelu. Siin saate teha järgmist. 

- Valige kuvamiseks ja redigeerimiseks mis tahes vasakus veerus loetletud seadme konfiguratsioon.
- Valige toimingupaanil suvand **Uus**, et lisada loetellu uus seadme konfiguratsioon. Seejärel sisestage uue konfiguratsiooni tuvastamiseks nimi väljale **Konfiguratsioon**. Siia sisestatav väärtus peab olema kõikide seadme konfiguratsioonide seas ainulaadne ja seda ei saa hiljem redigeerida.

Teavet töökaardi seadmete konfigureerimise iga sätte üksikasjade kohta leiate järgmistest jaotistest.

## <a name="general-settings"></a>Üldsätted

Kiirkaart **Üldine** võimaldab konfigureerida valitud seadmekonfiguratsiooni kõiki saadaolevaid suvandeid. Saadaval on järgmised sätted.

- **Koguse teatamine väljaregistreerimisel** – määrake suvandi väärtuseks **Jah**, et paluda töötajatel anda käimasolevate tööde kohta väljaregistreerimisel tagasisidet. Kui väärtuseks on seatud **Ei**, siis töötajatel seda teha ei paluta.
- **Lukusta töötaja** – kui väärtuseks on seatud **Ei**, siis logitakse iga töötaja välja kohe pärast registreeringu tegemist (nt uus töö) ja seejärel naaseb seade sisselogimise lehele. Kui suvandi väärtuseks on seatud **Jah**, siis jääb iga töötaja töökaardi seadmesse sisselogituks. Samas saab töötaja siiski käsitsi välja logida, et võimaldada mõnel teisel töötajal sisse logida, kui töökaardi seade jätkab töötamist sama süsteemi kasutajakonto all. Lisateavet nende kontotüüpide kohta leiate jaotisest [Määratud kasutajad](#assigned-users).
- **Vöötkoodilugeja** – seadke väärtuseks **Jah**, et pakkuda töökaardi seadmes võimalust, mis lubab töötajatel registreerida uue töö algus vöötkoodi skannimisega.
- **Tegeliku registreerimisaja kasutamine** – seadke väärtuseks **Jah**, et iga uue registreeringu aeg oleks samaväärne täpse ajaga, mil töötaja registreeringu esitas. Seadke väärtuseks **Ei**, et kasutada selle asemel sisselogimise aega. Tavaliselt võiks selle väärtuseks olla **Jah**, kui olete lubanud suvandid **Lukusta töötaja** ja/või **Üksik töötaja**, mille puhul jäävad töötajad sageli pikemaks ajaks sisselogituks.
- **Üksik töötaja** – seadke väärtuseks **Jah**, kui iga töökaardi seadet, kus see konfiguratsioon on aktiivne, kasutab ainult üks töötaja. Kui see valik on valitud, siis seatakse suvandi **Lukusta töötaja** väärtuseks automaatselt **Jah**. Lisaks eemaldab see suvand töötajalt kohustuse (ja võimaluse) logida sisse pääsme ID (või sarnase tunnuse) abil. Selle asemel logib töötaja teenusesse Supply Chain Management sisse süsteemi kasutajakonto kaudu, mis on seotud *ajaliselt registreeritud töötajaga* (tabelis *töötajad*), ning ta logitakse samal ajal kõnealuse töötajana töökaardi seadmesse sisse.  Lisateavet nende kontotüüpide kohta leiate jaotisest [Määratud kasutajad](#assigned-users).
- **Luba töötajatel seadistada isiklikke filtreid** – seadke väärtuseks **Jah**, et võimaldada töötajatel filtreerida neile seadmes kuvatavaid töid. Töötaja saab muuta kõigi järgmiste filtrikriteeriumide väärtust: **Tootmisüksus**, **Ressursigrupp** ja **Ressurss**. Seadmes kuvatakse vaid tööd, mis on ajastatud ressursside jaoks, mis ühtivad valitud filtrikriteeriumidega. Samuti saate määrata igale kriteeriumile vaikeväärtuseid, mis kehtivad ka juhul, kui seda suvandit ei valita.
- **Luba puuteekraani lukustamine** – seadke väärtuseks **Jah**, et võimaldada töötajatel lukustada töökaardi seadme puuteekraan, et nad saaksid seda puhastada. Kui see on lubatud, siis lisatakse seadme sisselogimise lehele nupp **Ekraani lukustamine puhastamiseks**. Kui töötaja valib selle nupu, siis lukustub puuteekraan ajutiselt, et ennetada soovimatuid sisendeid, ning kuvatakse aega mahaarvestav taimer. Nüüd saab töötaja ohutult seadet ja selle ekraani puhastada. Kui taimer lõpetab, siis tehakse puuteekraan automaatselt lukust lahti.
- **Ekraaniluku kestus** – kui suvand **Luba puuteekraani lukustamine** on lubatud, siis kasutage seda suvandit, et määratleda, mitu sekundit peaks puuteekraan puhastamiseks lukustatud olema. Kestus peab olema vahemikus 5–120 sekundit.
- **Tootmisüksus** – valige tootmisüksus, mida rakendatakse vaikefiltrikriteeriumina igale töötajale kuvatava tööde loetelu puhul. Seadmes kuvatakse esialgu vaid tööd, mis plaanitakse ressurssidele, mis on grupeeritud valitud tootmisüksuse alla. Kui suvand **Luba töötajatel seadistada isiklikke filtreid** on lubatud, siis saavad töötajad seda väärtust redigeerida. Vastasel juhul rakendatakse filtrit alati, kui seadme konfiguratsioon on aktiivne.
- **Ressursigrupp** – valige ressursigrupp, mida rakendatakse vaikefiltrikriteeriumina igale töötajatele kuvatava tööde loetelu puhul. Seadmes kuvatakse esialgu vaid tööd, mis plaanitakse ressurssidele, mis on grupeeritud valitud ressursigrupi alla. Kui suvand **Luba töötajatel seadistada isiklikke filtreid** on lubatud, siis saavad töötajad seda väärtust redigeerida. Vastasel juhul rakendatakse filtrit alati, kui seadme konfiguratsioon on aktiivne.
- **Ressurss** – valige ressurss, mida rakendatakse vaikefiltrikriteeriumina igale töötajatele kuvatava tööde loetelu puhul. Seadmes kuvatakse esialgu vaid tööd, mis plaanitakse ressurssidele, mis on grupeeritud valitud ressursi alla. Kui suvand **Luba töötajatel seadistada isiklikke filtreid** on lubatud, siis saavad töötajad seda väärtust redigeerida. Vastasel juhul rakendatakse filtrit alati, kui seadme konfiguratsioon on aktiivne.
- **Loo litsentsiplaat** – seadke suvandi väärtuseks **Jah**, et luua uus litsentsiplaat iga kord, kui töötaja kasutab töökaardi seadet töö lõpetamisest teatamiseks. Identifitseerimisnumber luuakse lehel **Laohalduse parameetrid** seadistatud numbriseeria alusel. Kui väärtuseks on seatud **Ei**, siis peavad töötajad määratlema lõpetamisest teatamisel olemasoleva litsentsiplaadi.
- **Prindi silt** – seadke suvandi väärtuseks **Jah**, et printida litsentsiplaadi silt, kui töötaja kasutab töökaardi seadet lõpetamisest teatamiseks. Sildi konfiguratsioon on seadistatud dokumendi marsruudivalikus, nagu on kirjeldatud teemas [Identifitseerimisnumbri siltide dokumendi marsruudivaliku paigutus](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Määratud kasutajad

Kasutage kiirkaarti **Määratud kasutajad** ühe või enama süsteemikasutaja seostamiseks praeguse seadme konfiguratsiooniga. Igat süsteemikasutajat saab määrata vaid ühele tööseadme konfiguratsioonile.

Seadme seadistamisel logib IT-töötaja teenusesse Supply Chain Management sisse tavaliselt süsteemi kasutajakonto abil. Seejärel rakendatakse selle süsteemikasutajaga seotud tööseadme konfiguratsiooni seni, kuni süsteemikasutaja on sisse logitud. Need süsteemi kasutajakontod on tavaliselt piiratud, võimaldades juurdepääsu vaid töökaardi seadme lehele, kuid mitte ühelegi muu Supply Chain Managementi teenuse osale.

Kui süsteemikasutaja on sisse logitud ja tööseadme konfiguratsioon on laaditud, saavad töötajad töökaardi seadmesse sisse logida, kasutades oma *ajaliselt registreeritud töötaja* kontot (nt skannides oma pääsmel toodud vöötkoodi), et nad saaksid alustada uusi töid ja teha muid registreeringuid. Päeva jooksul võivad sisse ja välja logida erinevad kasutajad ning selles masinas püsib jõus üks ja sama seadme konfiguratsioon, kuna süsteemikasutaja jääb teenusesse Supply Chain Management kogu päevaks sisselogituks.

Kuid nagu varem mainitud, siis logivad töötajad suvandi **Üksik töötaja** kasutamisel teenusesse Supply Chain Management tavaliselt ise sisse, kasutades oma *ajaliselt registreeritud töötaja* kontot, nii et nad laadivad samal ajal seadme konfiguratsiooni ja logivad töötajana töökaardi seadmesse sisse.

## <a name="additional-resources"></a>Lisaressursid

[Töökaardi seadmes lõpetamisest teatamine](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]