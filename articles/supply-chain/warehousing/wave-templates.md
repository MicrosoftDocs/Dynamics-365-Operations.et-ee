---
title: Voomallid
description: See artikkel kirjeldab, kuidas seadistada kriteeriume, mis määratlevad, kas laineid töödeldakse käsitsi või automaatselt, ning voo töötlemisel lao jaoks loodud tööd.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e4a74b61ea32df432da118ac8af550a4ca4b0089
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851194"
---
# <a name="wave-templates"></a>Voomallid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada kriteeriume, mis määratlevad, kas laineid töödeldakse käsitsi või automaatselt, ning voo töötlemisel lao jaoks loodud tööd. Kriteeriumite määramiseks seadistage voomallid ja päringud, mis vastavad müügitellimuste, tootmistellimuste ja kanbanide väljastatud ridadega voole.

## <a name="settings-for-wave-templates"></a>Voomallide sätted

Voomalli seadistamisel määrake järgmised elemendid.

- **Tegevuskoht** ja **ladu**, mille kohta mall loob töö.
- Mallide hindamise järjekord. Mallide vastendamise järjekord müügitellimuste, tootmistellimuste ja kanbanide väljastatud ridadega. Kui rida vabastatakse, rakendab süsteem esimest voomalli, mille puhul rida vastab kriteeriumidele. Mida laiemad kriteeriumid on, seda tõenäolisem on, et rida vastab kriteeriumidele, seega peaksite kõige konkreetsemate kriteeriumidega mallid loendi ülaossa panema. Toimingupaanil loendi mallide sättimiseks kasutage nuppe **Nihuta üles** ja **Nihuta alla**.
- Iga malli toimingud. Voog **Meetodid**, mis teeb malli loodud toiminguid, nagu iga voomalli tüübi jaoks töö loomine või jaotamine.
- Voo atribuudid (filtrid), mida tuleb rakendada kasutatava voomalli puhul.

> [!NOTE]
> Vajaduse korral saab arendaja luua lisameetodeid. Lehel **Voo protsessimeetod** saate vaadata täielikku meetodite loendit.

Mõned sätted tähistavad järgmisi strateegilisi otsuseid voo töötluse kohta.

- Malli kasutamine müügi- ja ülekandetellimuste jaoks kaupade saatmiseks või tootmistellimuste või kanbanide jaoks kaupade üleviimiseks tootmisesse.
- Voo töötlemine järgmisel viisil käsitsi või automaatselt.

  - **Käsitsi töötlemine** – rida lisatakse voole ja varud reserveeritakse, kuid peate siiski tellimuse jaoks komplekteerimistöö loomiseks klõpsama valikut **Töötle** loendilehel **Kõik vood**.
  - **Automaatne töötlemine** – saate voo töötlust täielikult või osaliselt automatiseerida. Voo töötluse täieliku automatiseerimise korral luuakse voog, mis sisaldab müügitellimuse, tootmistellimuse või kanbani rida, kui luuakse müügitellimus, tootmistellimus või kanban. Kaubad arvatakse vabast kaubavarust maha ja luuakse komplekteerimistöö. Voo töötluse osalise automatiseerimise korral saate määrata väärtused, mis käivitavad voo töötluse. Saate näiteks määrata saadetiste maksimaalse kaalu, mis käivitab voo töötluse, kui voo ridade kogukaal jõuab selle väärtuseni.

- Saadetiste määramine avatud voole. Kui te näiteks lubate klientidele, et kella 12:00 tehtud tellimus saadetakse välja 24 tunni jooksul, saate seadistada voomalli tellimuseridade automaatseks määramiseks avatud voole kuni kella 12:00. Sel ajal töödeldakse voogu automaatselt.

Pärast voo töötlemist võetakse loodud komplekteerimistöö aluseks töömall ja asukoha korraldus, mis on lao jaoks määratud. Töömall määrab komplekteerimistöö loomise viisi ja asukoha korraldus määrab komplekteerimise ning ladustamise asukohad.

## <a name="create-a-wave-template"></a>Voomalli loomine

Voomalli seadistamiseks tehke järgmist.

1. Avage jaotis **Laohaldus** \> **Seadistus** \> **Vood** \> **Voomallid**.
1. Valige uue voomalli loomiseks **Uus**.
1. Väljal **Voomalli tüüp** valige üks järgmistest valikuteks.

    - *Saatmine* - kasutage voomalli müügi- ja ülekandetellimuste jaoks kaupade saatmiseks.
    - *Tootmistellimused* - kasutage voomalli tootmistellimuste jaoks kaupade teisaldamiseks.
    - *Kanban* - kasutage voomalli kanbantellimuste jaoks kaupade teisaldamiseks.

1. Sisestage väljadele **Voomalli nimi** ja **voomalli kirjeldus** voomalli nimi ja kirjeldus.

    > [!NOTE]
    > Kui lao jaoks luuakse mitu malli, tähistab väljal **Voomalli jada** olev number malli asukohta mallide rakendamise järjekorras malli kriteeriumite täitmisel. Saate mallide järjestuse muutmiseks valida **Nihuta üles** või **Nihuta alla**.

1. Väljadel **Piirkond** ja **Ladu** valige asukoht ja ladu, mille jaoks voomall loob vood ja komplekteerimistööd.
1. Kui soovite voo töötlemist automatiseerida, seadistage vastavalt vajadusele järgmised sätted.

    - **Automaatne voo loomine** - selle väärtuse määramisel *Jah* luuakse voog automaatselt, kui ostutellimus, tootmistellimus või kanban väljastatakse lattu.
    - **Määra avatud voogudele** - seadke see väärtusele *Jah*, et määrata read ridade vabastamist automaatselt avatud voole. Read määratakse voogudele voomalli päringufiltri põhjal.
    - **Töötle lainet lattu väljaandmisel** - määrake selle väärtuseks *Jah*, et voogu automaatselt töödelda ja luua töö, kui rida on lattu välja antud.
    - **Voo automaatne töötlemine lävendil** - selle suvandi väärtuseks *Jah* seadmisel töödeldakse voogu automaatselt, kui selle väärtused jõuavad väljagrupil **Vooläved** määratud kaalu, saadetise ja ridade läveni. See säte on aktiivne vaid siis, kui väljal *Voo mall* on valitud **Lähetamine**.
    - **Voo väljaandmise automatiseerimine** - voo automaatseks väljaandmiseks määrake selle väärtuseks *Jah*. Luuakse komplekteerimistöö ja muudetakse see mobiilsetel seadmetel kättesaadavaks.
    - **Täiendustöö väljaandmise automatiseerimine** - valige selle suvandi väärtuseks *Jah* nõudlusel põhineva täiendustöö loomiseks ja selle automaatseks väljastamiseks. Selleks peab voomallile lisama täiendusvoo meetodi ja looma täiendamismalli tüübiga *Voo nõue*. Häälestage lehel **Täiendamise mall** täiendamise mall. Selleks on vaja voomallile lisada täiendamise meetod.
    - **Voo töötlemise jätkamine, kui töö loomine ebaõnnestub** - kui selle väärtuseks on *Jah*, kasutab süsteem tühja asukohta juhul, kui see ei saa reserveerida varusid asukohakorralduse pakutavas asukohas (nt kuna varusid pole enam saadaval). Kui selle väärtuseks on *Ei*, siis voog nurjub, kui süsteem ei saa varusid reserveerida.

1. Seadistage väljagrupp **Vooläved** vastavalt vajadusele.
    - **Voo kaalu lävi** – sisestage maksimaalne kaal, mida voog võib sisaldada.
    - **Saadetise lävi** – sisestage saadetiste maksimumarv, mida saab voosse kaasata.
    - **Rea lävi** – sisestage ridade maksimumarv, mida saab voosse kaasata.

1. Väljagrupis **Vaikimisi väärtused** valige voomalli lisakriteeriumitena kasutatavad voo atribuudid. Voo atribuudid sobivad voomallile lisakriteeriumite määramiseks, nagu kindla kliendi nimi. Need atribuuditüübid saate luua lehel **Voo atribuudid**. 

1. Seadistage **voo teavituspoliitika** poliitikale, mida soovite kasutada seda malli kasutavate voogudega seotud teatiste loomiseks. Voo teavituspoliitika näiteid vt [Voo käivitamisteatised](wave-execution-notifications.md).

1. Kiirkaardil **Meetodid** on paanil **Valitud meetodid** esitatud valitud voomalli tüübi meetodid. Voo meetodid, mis teevad malli loodud toiminguid, nagu iga voomalli tüübi jaoks töö loomine või jaotamine. Neid toiminguid nimetatakse ka vooetappideks. Voomeetodid on eelmääratletud iga voomalli tüübi jaoks. Eelmääratletud voomeetodeid ei saa eemaldada, kuid saate muuta meetodite järjekorda ja lisada täiendavaid meetodeid. Kui loote näiteks saadetise jaoks voomalli, saate lisada täiendamise ja konteinerite koostamise meetodeid. Voona konteinerite koostamist saab lisada voomeetodite seeriale, et määrata voomallis töödeldud ridadel konteinerite koostamist. Uue meetodi lisamiseks tehke järgmist.

    - Valige paanilt **Järelejäänud meetodid** meetod ja valige siis noolenupp **Vasak** selle lisamiseks paanile **Valitud meetodid**.
    - Järjekorra muutmiseks valige meetod ja valige seejärel **ülemist** või **alumist** noolenuppu.

    > [!NOTE]
    > Meetodi lisamisel viiakse see automaatselt etappide järjekorras õigesse asukohta.

1. Päringu häälestamiseks, mis vastendab vabastatud read sobiva vooga, valige tegevuspaanil suvand **Redigeeri päringut**.
1. Voomalli sätete kehtivuse kontrollimiseks valige **Valideeri mall**.
