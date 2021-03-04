---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Talent (9. juuli 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: feb39966d98fa7bde9a6bfad26b07fbd224da59b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528027"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Talent (9. juuli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Peagi tulekul rakenduses Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>Töökinnitused kuvatakse avalehel

Kinnitused kuvatakse armatuurlaua jaotises **Kinnitused**. Kinnitajad saavad kinnitusi üle vaadata jaotises **Teile määratud**, kus kuvatakse töö ID, töö pealkiri, teised kinnitajad ja töö määramise kuupäev. Kasutajad, kes töö kinnitamiseks esitavad, saavad oma töid üle vaadata jaotises **Teie taotletud**, mis kuvab kinnitajaid, kes peavad edastatud tööd veel kinnitama.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Teenuse Finance and Operations platvormivärskendus 28

Finance and Operations platvormivärskenduse 28 kohta lisainfo saamiseks vt [Dynamics 365 Finance and Operations platvormivärskenduse 28 (juuli 2019) funktsioonide eelvaade](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Üksuse tugi ühise andmeteenuse Common Data Service kohandatud väljadele 

Järgmised üksused toetavad kohandatud välju: 

- **Tasu fikseeritud plaan**
- **Palga koos lisatasudega võrdluspunkti seadistus**
- **Palga koos lisatasudega võrdluspunkti seadistuse rida**
- **Palga tulukood**
- **Makseperiood**
- **Põhipalga sündmus**
- **Hüvitise ruudustik**

Kõigi värskendatud üksuste kuvamine Talentis:

1. Valige **Süsteemi Administreerimine**, valige **Lingid** ja seejärel valige **Common data service konfiguratsioon**.
2. Valige rippmenüüst **CDS-üksuse** nimi. Kõik loetletud üksused on viimases versioonis. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Töötaja üksusele lisatav täisnimi teenuses Common Data Service

Üksusse **Töötaja** on lisatud väli **Täisnimi**.

### <a name="full-time-equivalent-higher-than-10"></a>Täistööajaga ekvivalent on suurem kui 1,0

Hoiatus kuvatakse nüüd, kui ametikoha täistööajaga töötajale on sisestatud väärtus, mis on suurem kui 1,0. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Hoiatust ei kuvata enam töötaja lehel, kui puudub tulevane töö.

Te ei saa enam teadet, mis näitab, et tulevane töösuhe on olemas, kui navigeerite **Töötaja** lehele **Olemasolevad töötajad** nimekirjast **Personalijuhtimise** tööruumis. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Äriprotsessi ei saa Talentis kustutada

Äriprotsesse saab kustutada tööruumis **Äriprotsess**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Puhkusejääki ei kuvata enam selliste plaanide puhul, mille tekkeperioodi seisuga saldo kasutamisel pole viitvõlad enam nullis

Viitvõlgadega seadistatud plaanid saavad nüüd saldot kuvada.

## <a name="in-preview"></a>Eelvaates

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Eelvaate funktsioonid on lubatud ainult liivakasti eksemplarides

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata **Tootmine** või **Liivakast**. **Liivakasti** tüübi eksemplarid võimaldavad uute funktsioonide varajast katsetamist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks **Tootmine**. Kui soovite mõne olemasoleva eksemplari **Liivakasti** tüübile värskendada, võtke muudatuse taotlemiseks ühendust [Toega](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support).

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Puhkuse tüüpide piiramine puhkusetaotluste korral

Organisatsioonid võivad töötajatele pakkuda mitut erinevat tüüpi puhkust. Siiski ei pruugi töötajatel olla asjakohane teatud puhkuse tüüpide puhkusetaotluste esitamine. Neid puhkuse tüüpe võib hallata hoopis HR. Selle väljalaskega saate konfigureerida, milliste puhkusetüüpide puhkusetaotluseid töötajad saavad esitada. 

## <a name="coming-soon-in-core-hr"></a>Tulemas Core HR-i

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Halduri iseteeninduses jõudluse lisateabe kuvamine

Uus suvand võimaldab juhtidel vaadata nii oma otseste kui ka kaudsete alluvate jõudlust. Praegu saavad rea haldurid määrata ja uuendada jõudluse eesmärke ja väljastada uusi arvustusi, mida nende töötajad samuti haldavad. Lisaks saavad otsesed juhid ja nende töötajad hallata ja värskendada jõudluse töölehti, mis aitavad tagada sujuva jõudluse ülevaate protsessi. Selle muudatuse rakendamisel saavad juhid vaadata ja hallata lisaks otseste alluvate jõudlusega seotud teabele ka oma kaudsete alluvate jõudlusega seotud teavet. 

### <a name="entities-supporting-custom-fields"></a>Kohandatud välju toetavad üksused

Ühisandmete teenuse Common Data Service kohandatud väljade jaoks lubatakse järgmised üksused 

- **Puhkuse tüüp**
- **Töötaja pangakonto**
- **Tööaja kalender**


[!INCLUDE[footer-include](../includes/footer-banner.md)]