---
title: Koondplaneerimise kasutamise alustamine
description: See artikkel selgitab, kuidas alustada koondplaneerimise funktsioonide kasutamist rakenduses Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780304"
---
# <a name="get-started-with-master-planning"></a>Koondplaneerimise kasutamise alustamine

[!include [banner](../../includes/banner.md)]

Tarneahela halduse koondplaneerimist pakub väline teenus nimega Planeerimise optimeerimise lisandmoodul Dynamics 365 Supply Chain Management. See teema kirjeldab, kuidas teenust hankida ja seadistada.

## <a name="availability"></a>Kättesaadavus

Plaanimise optimeerimine on praegu saadaval järgmistes Azure’i geograafilistes asukohtades: USA, Kanada, Brasiilia, Euroopa, Prantsusmaa, Ühendkuningriik, Norra, Šveits, Austraalia, Aasia Vaikse ookeani diagramm, Jaapan ja India. Kui proovite lisandmoodulit installida muus geograafilises piirkonnas, siis kuvab LCS teate, et seda geograafilist piirkonda ei toetata. Lisateavet Azure'i piirkondade ja seotud piirkondade kohta vt [Azure'i piirkonnad](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Pange tähele, et planeerimise optimeerimine ei toeta Dynamics 365 Supply Chain Management-i kohapealseid juurutusi.

## <a name="licensing"></a>Litsentsimine

Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.

## <a name="install-and-enable-planning-optimization"></a>Planning Optimizationi installimine ja lubamine

Rakenduse Planning Optimization asutamiseks peate veenduma, et teie süsteemil oleksid kõik eeltingimused olemas, ja seejärel lubama selle litsentsivõtme ja installima rakenduse Planning Optimization lisandmooduli rakendusele Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Eeltingimused

Enne rakenduse Planning Optimization lisandmooduli installimist peavad olema täidetud järgmised eeltingimused.

- Supply Chain Management peab teil töötama LCS-i loaga suure kättesaadavusega keskkonnas, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos rakenduse Dynamics 365 Supply Chain Management versiooniga 10.0.7 või hilisem. Kui proovite paigaldada moodulit OneBoxi keskkonnas, siis ei viida paigaldust lõpule ja te peate paigalduse tühistama.

- Teie süsteem peab olema seadistatud Power Platformi integreerimiseks. Lisateabe saamiseks vt integratsiooni finantside [Microsoft Power Platform ja toimingute rakendustega](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Planning Optimizationi litsentside lubamine

Planning Optimizationi kasutamiseks peate lubama selle konfiguratsioonivõtme. Selleks tehke järgmist.

1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Valige vahekaardil **Konfiguratsioonivõtmed** märkeruut **Planning Optimization**.
1. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>Planning Optimizationi lisandmooduli installimine

Peate installima lisandmooduli oma LCS projektist ja lülitama seejärel Planning Optimizationi funktsiooni Supply Chain Managementi kasutajaliidesest sisse.

Planning Optimizationi lisandmooduli installimiseks tehke järgmist.

1. Logige LCS-i sisse ja avage soovitud keskkond.
1. Avage **Kõik üksikasjad**.
1. Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.
1. Valige **Installi uus lisandmoodul**.
1. Valige **Planeerimise optimeerimine**.
1. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.
1. Valige **Installi**.
1. Kiirkaardil **Keskkonna lisandmoodulid** peaksite nägema, et Planning Optimization on installitud.
1. Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud** (võimalik, et peate lehte värskendama). Kui installimine on lõpetatud, olete valmis aktiveerima optimeerimise plaanimise rakenduses Dynamics 365 Supply Chain Management.

Planning Optimizationi lisandmooduli installimise peamine eesmärk on ühendada teenus ja keskkond. Seetõttu peate installima lisandmooduli eraldi igasse keskkonda, kus te kasutate planeerimise optimeerimist, olenemata mis tahes koodist, mis on teisaldatud keskkondade vahel.

## <a name="integrate-planning-optimization-with-your-system"></a>Planning Optimizationi integreerimine süsteemiga

Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Optimeerimise parameetrite plaanimine**.

### <a name="connection-status"></a>Ühenduse olek

Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut. Järgmine tabel näitab võimalikke väärtuseid.

| Ühenduse olek | Kirjeldus | Kas planeerimise optimeerimist saab kasutada? |
|---|---|---|
| Ühendus on loodud | Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus. | Jah |
| Ühenduse loomine | Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd. | Ei |
| Ühendus on katkestatud | Planeerimise optimeerimise teenusega puudub ühendus. LCS-i kaudu saab ühenduse sisse lülitada, nagu kirjeldatud selles artiklis. | Nr |
| Ühenduse katkestamine | Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd. | Ei |
| Oleku hankimine | Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet. | Ei |

### <a name="the-use-planning-optimization-option"></a>Planeerimise optimeerimise kasutamise suvand

Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.

- **Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.
- **Ei** – taunitud koondplaneerimise mootorit kasutatakse koondplaneerimiseks.

See säte kehtib kõigi juriidiliste isikute (ettevõtete) kohta. Mõnedes juriidilistes isikutes ei saa kasutada plaanimise optimeerimist ja teiste juriidiliste isikute mittetaunitud koondplaneerimise mootorit.

> [!NOTE]
> Kui plaanimise pakett-tööd **·**, mis loodi taunitud koondplaneerimise mootori jaoks, käivitatakse ajal, kui valiku Kasuta optimeerimist väärtuseks on **määratud** Jah, siis need tööd nurjuvad.

### <a name="integration-with-the-setup"></a>Integreerimine seadistamisega

Kui planeerimise optimeerimine on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades. Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
