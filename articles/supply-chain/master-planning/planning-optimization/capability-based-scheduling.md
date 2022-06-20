---
title: Plaanimine võimaluse põhjal ressursivalikuga
description: See artikkel kirjeldab ressursside valikut piiramatu võimsuse planeerimise ajal, kui määrate operatsioonile võimalusi ressursi nõuetena.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 26b2b65a2d565052b188f4d70f0cc0a773cd7b43
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847958"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Plaanimine võimaluse põhjal ressursivalikuga

[!include [banner](../../includes/banner.md)]

Määrates tootmisprotsessi toimingu ressursinõuded, määratlete, mis on vajalik selle operatsiooni sooritamiseks. Näiteks võib toiming vajada konkreetset ressurssi või ressursigruppi või oskuste või võimaluste kombinatsiooni. See artikkel kirjeldab ressursside valikut piiramatu võimsuse planeerimise ajal, kui määrate operatsioonile võimalusi ressursi nõuetena.

## <a name="turn-on-the-capability-based-scheduling-feature"></a>Lülitage sisse võimetepõhine planeerimise funktsioon

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Koondplaneerimine*
- **Funktsiooni nimi:** *Planeerimise optimeerimise lõpmatu võimsuse ajastamine*

Lisateabe saamiseks selle funktsiooni kohta vaata [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Võimetepõhine planeerimine

Võimsus on operatsiooniressursi võime teatud tegevust sooritada. Ühele toiminguressursile saab määrata mitu võimet ja ühele võimalusele saab määrata rohkem kui ühte ressursi. Võimeid saab määrata igat tüüpi ressurssidele, nagu tööriistad, müüjad, masinad, asukohad, rajatised ja inimressursid.

Kui määrate võimsusi ressursi nõuetena, saate tellimuste plaanimiseni ressursi eraldamist edasi viia. Kindlate ressursside või ressursigruppide protsessi operatsioonile määramise asemel saate määratleda võimalused, mis on vajalikud iga protsessi operatsiooni jaoks. Seejärel sobitab süsteem planeerimise ajal nõutavad võimalused ressurssidele määratud võimalustega. Süsteem valib ainult nõuetele vastavaid ressursse.

Operatsiooniressursile võimaluste määramiseks kasutage **Võimed** kiirkaarti **Ressursid** lehel. Võimele ressursside määramiseks kasutage lehe **Ressursside võimalused** kiirkaarti **Ressursid**. Mõlemad lehed on saadaval navigeerimispaanil jaotises **Tootmise juhtimine \> Seadistamine \> Ressursid**. Mõlemad kiirkaardid sisaldavad ruudustikku, mis loetleb valitud ressursi või võimalusega seostatud ressursse. Mõlemad kiirkaardid sisaldavad ka tööriistariba, mida saate kasutada ruudustiku ridade lisamiseks, eemaldamiseks ja redigeerimiseks. Ruudustik sisaldab järgmisi veerge.

- **Ressurss** või **Võimsus** – Valige rea poolt määratud ressurss või võimsus.
- Sisestage väljale **Kirjeldus** ressursi või võimsuse lühikirjeldus.
- **Efektiivne** - määrake esimene kuupäev, mil rakendatakse ressursi või võimsuse määrangut. Planeerimise ajal ei kasuta süsteem ressurssi või võimsust, mille võimsus on aegunud, isegi kui see ressurss vastab muul juhul nõuetele.
- **Aegumine** - määrake viimane kuupäev, mil rakendatakse ressursi või võimsuse määrangut. Planeerimise ajal ei kasuta süsteem ressurssi või võimsust, mille võimsus on aegunud, isegi kui see ressurss vastab muul juhul nõuetele.
- **Tase** – määrake puudulikkuse tase, mis ressursil peab võimaluse jaoks olema. Seejärel, kui määrate **Minimaalse vajaliku taseme** väärtuse ressursile või võimsusnõudele, võtab planeerimismootor ressursivaliku ajal puudulikkuse taseme. Süsteem valib siis ainult need ressursid, millel on nõutav võimsus tasemel, mis on ressursi nõuetes määratud minimaalse tasemega võrdne või ületab selle.
- **Prioriteet** – planeerimise optimeerimine ei toeta veel seda välja. Kuid kui kasutate integreeritud planeerimismootorit, saate ressursi või võimsuse määramises kasutada välja **Prioriteet**, et määrata ressursi prioriteet. Seejärel, kui lehel **Primaarne ressursi valik** väljal **Ajastamisparameetrid** on valitud *Prioriteet*, valib süsteem kõigepealt ressursi, millel on kõrgeim prioriteet (st väikseim arvväärtus väljal **Prioriteet**) ajastamise ajal.

## <a name="example"></a>Näide

See näide näitab, kuidas planeerimismootor valib võimsusel põhinevad ressursid.

Tootmisprotsessil on viis operatsiooni: *10*, *20*, *30*, *40*, and *50*. Iga protsessitoiming nõuab eri võimalustega ressurssi. Näiteks protsessi operatsioon *10* nõuab ressurssi, mis suudab kõlarit kokku panna (*0050 Spkr Assembly*) ja suudab teha puidutöötlust (*1010 Wood capabilities*). Protsessi operatsioon *50* nõuab ressurssi, mis on võimeline tooteid pakkima (*0070 Packing capability*).

![Planeerimiseks kasutatud võimed.](media/capability-based-scheduling.png "Planeerimiseks kasutatud võimed.")

Planeerimise ajal otsib mootor ressursse, mis vastavad operatsiooni nõuetele. Näiteks plaanimismootor valib toimingu *10* sooritamiseks ressursi *00101*, sest see ressurss on esimene ressurss, mille puhul leitakse mõlemad nõutud võimalused. Plaanimismootor valib toimingu *50* sooritamiseks ressursi *00301*, sest see ressurss on ainuke ressurss, millel on pakkimisvõime.

Järgmisena kaaluge, kuidas seda näidet puudulikkuse tasemete kasutamisel mõjutatakse.

- Toiming *10* nõuab *0059 Assembly* võimeks oskustasemeks minimaalset *7*.
- Ressursil *00101* on puudulikkuse tase *5* *0059 Assembly* võime jaoks.
- Ressursil *00102* on puudulikkuse tase *10* *0059 Assembly* võime jaoks.

Sellisel juhul valib planeerimismootor piiramatu võimsuse planeerimise ajal operatsiooni *10* sooritamiseks ressursi *00102*, sest erinevalt ressursist *00101* on sellel ressursil võimsuse jaoks nõutav oskustase.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
