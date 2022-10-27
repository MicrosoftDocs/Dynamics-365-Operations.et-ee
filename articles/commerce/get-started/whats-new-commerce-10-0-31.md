---
title: Dynamics 365 Commercei versiooni 10.0.31 eelversioon (veebruar 2023)
description: See artikkel kirjeldab funktsioone, mis on uued või muutunud Microsoft Dynamics 365 Commerce 10.0.31-s.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 05ccd9794ffeba6a09d6fec0a57ffad2b59707ad
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709870"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Dynamics 365 Commercei versiooni 10.0.31 eelversioon (veebruar 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles artiklis loetletakse funktsioonid, mis on eelvaate versiooni Microsoft Dynamics 365 Commerce 10.0.31 uued või muutunud. Sellel versioonil on järgu number 10.0.1406 see on saadaval järgmises graafikus.

- **Väljalaske eelversioon:** oktoober 2022
- **Väljalaske üldine kättesaadavus (iseseisev värskendamine):** jaanuar 2023
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** veebruar 2023

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Tõrkekoodid | Commerce tutvustas standardiseeritud tõrkeviiteid, mis kaasatakse võrgukanali väljaregistreerimise tõrgetesse, mis esitatakse võrgupoesaatoritele.| [Väljaregistreerimise mooduli tõrkekoodid](../checkout-module-error-codes.md)  | Vaikimisi sees |
| Maksed | [Luba Maksete maksmine Dynamics 365 Payment Connectoriga Puhvrile](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-commerce’i kliendid saavad toetatud seadmete või brauserite kasutamisel kasutada Cart Payi ostukorvi ja väljaregistreerimise lehti. | Arendaja nõustumine |
| Maksed  |  Commerce lisas võimaluse piirata kasutajate suhtlemist korduvate makselubadega kogu Commerce headquartersi kasutajaliideses. Maksevormid, nagu **kõnekeskuse müügitellimuste** leht, ei kuva enam kliendi varem kasutatud korduva makse luba uues kandes kasutamiseks. Commerce Customer Paymentsi **ekraanile saab sisestada ainult määratletud "failikaardil"** sisestatud sisestatud andmed või esitatakse müügitellimuse kaudu maksmise ajal kliendiga sõlmitud kokkuleppele kõnekeskusele või Commerce Headquartersi kasutajatele. | [Piira makse loa kasutust](../dev-itpro/limit-token-usage.md)  |  Funktsioonihaldus<p>*Piira makseloa kasutust tellimuse kontekstiga*  |
| Müügikoht | [Ostutellimuste loomine müügikohast](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Täiustatud sissetulevate laovarude toiming müügikoha rakenduses, et lubada kasutajatel ostutellimuste taotlusi luua, redigeerida ja kinnitada. |  Funktsioonihaldus<p>*Võimalus luua ostutellimuse taotlus kassasüsteemis*   |



## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Commerce 10.0.31 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.31 finantside ja toimingute rakendustest (veebruar 2023).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md) 
  

### <a name="bug-fixes"></a>Veaparandused

Teavet versiooni 10.0.31 igasse versiooniga 10.0.31 Microsoft Dynamics [kaasatud värskendustes kaasatud vigaparanduste kohta logige sisse elutsükli teenustesse ja vaadake teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan](/dynamics365-release-plan/2022wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-commerce-features"></a>Eemaldatud ja taunitud commerce’i funktsioonid

Artikli [eemaldatud või taunitud funktsioonid Dynamics 365 Commerce](removed-deprecated-features-commerce.md) kirjeldavad funktsioone, mis on Commerce’i eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.


Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
