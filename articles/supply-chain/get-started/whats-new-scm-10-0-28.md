---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.28. (august 2022)?
description: See artikkel kirjeldab funktsioone, mis on Microsoft Dynamics 365 Supply Chain Management 10.0.28 uued või muutunud.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 184da494b9998e3e1cf6bd1639b452192d7e7857
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427816"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.28. (august 2022)?

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.28 uued või muutunud. Sellel versioonil on järgu number 10.0.1264 see on saadaval järgmises graafikus.

- **Väljalaske eelversioon:** mai 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuli 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuli 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud ja logistika | [Väljaminekuga kulude integreerimise üksused kolmandate osapoolte veostele](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Väljalaadimiskulu üksuste ülevaade](../landed-cost/landed-cost-entities-overview.md) | Vaikimisi lubatud |
| Planeerimine | [Nõudlusepõhiste materjalinõuete planeerimine (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Nõudlusepõhiste materjalinõuete planeerimise ülevaade](../master-planning/planning-optimization/ddmrp-overview.md) | Funktsioonihaldus:<br>*(Eelversioon) Planeerimise optimeerimise DDMRP* |
| Planeerimine | [Plaanimise optimeerimise tugi võimelisele/lubadustele (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [Müügitellimuse tarnekuupäevade arvutamine CTP-d kasutades](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | Funktsioonihaldus:<br>*(Eelversioon) Planeerimise optimeerimise CTP* |
| Planeerimine | [Kõlblikkusaja plaanimise optimeerimise tugi](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [Piiratud kõlblikkusajaga toodete koondplaneerimine](../master-planning/planning-optimization/shelf-life.md) | Vaikimisi lubatud |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Varude ja laohaldus | Luba kontsernisiseses laoseisus kuvada ainult nullist erinev laoseisu kogus | See funktsioon võimaldab teil valida, kas null vaba kaubavaruga kaubad tuleks kaasata kontsernisisesesse vaba kaubavaru loendisse. Seda valikut **saate** juhtida, kasutades valikut Ära kuva null vaba kaubavaruga kaupu kontsernisisese vaba kaubavaru loendi sättes **, mille see funktsioon lisab varude ja laohalduse parameetrite lehele**. |
| Varude ja laohaldus | (India) Üleviimise hinnareeglite puhul ignoreerige asukohta, kui "Lao koodist" on seatud väärtusele "Kõik" | <p>See funktsioon kehtib ainult India lokaliseerimise puhul. See muudab laoülekannete ülekandehindade seadistamise intuitiivsemaks.</p><p>Te seadistate ülekande hinnad, konfigureerides iga kaupa ülekande hinnakujunduse reeglitega. Üks võimalus seda konfiguratsiooni teha on kaasata reegli rida, kus **välja Laost kood** väärtuseks on määratud *Kõik*. See säte näitab, et rea määratletud ülekande hind peaks rakenduma sõltumata laost, millelt kaup komplekteeritud on. Kui see funktsioon on lubatud, eiravad ülekande **hinnareeglid**, kus väli Laost koodi väli on *seadistatud* sättele Kõik, asukoha **sätet**. Seetõttu rakendub reegel sõltumata üleviimistellimusel määratud asukohast. Selline käitumine on eeldatav, sest asukoht on laoala dimensiooni hierarhias laost allpool.</p><p>Ilma selle funktsioonita kohaldab süsteem seda tüüpi reegleid ainult siis, kui üleviimistellimuse asukoht ühtib täpselt reegli jaoks seadistatud asukohaga. (Kui reegli jaoks on tühi asukoht määratud, rakendab süsteem reeglit ainult üleviimistellimustele, mille asukoha väärtus on samuti tühi.)</p> |
| Varude ja laohaldus | Laoseisu aruande andmete puhastamine | See funktsioon võimaldab puhastada andmeid, mida kasutatakse laoseisu *aruande ladustamisaruannete loomiseks*. |
| Tootmise juhtimine | Määrake projektitegevused teenuseleppe ja teenusetellimuse ridadele | See funktsioon lisab välja nimega Projekti **tegevus** teenuselepingule ja teenusetellimuse ridadele, nii et saate nende jaoks seada projekti tegevuse. See funktsioon aitab vältida blokeerimisvigu, kui sisestate teenusehalduse projektitöölehti, mis nõuavad projekti tegevuse seadistamist.  |
| Laohaldus | Käsitsi ülekanderea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele | See funktsioon võimaldab administraatoril käsitsi komplekteeritud laokandeid, mis on seotud üleviimisridadega. Need read sisaldavad juba lattu väljastatud ridu. Administraatorid peaksid seda komplekteerimist tegema ainult erandlikel juhtudel, näiteks siis, kui süsteem on rikutud olekus. Lisateavet vt müügi ja [rea komplekteerimise erandite käsitsi käsitsemisest](../warehousing/manual-order-line-picking-exception-handling.md). |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt värskendanud järgmised spikriartiklid. Need artiklid ei pea tingimata olema seotud uute funktsioonidega, mis selle väljalaske jaoks lisati, nagu on loetletud eelmistes jaotistes. Kuid need võivad aidata teil rohkem olemasolevatest funktsioonidest välja saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Kuluhaldus | [Fikseeritud jaehind](../cost-management/fixed-receipt-price.md) |
| Kuluhaldus | [Korduma kippuvad küsimused varude kuluarvutuse kohta](../cost-management/inventory-costing-faq.md) |
| Kuluhaldus | [Kulude kontole sisestamise raamatupidamispõhimõte](../cost-management/post-to-charge-account-accounting-principle.md) |
| Varud | [Laokande üksikasjad](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Microsoft Dynamics 365 Supply Chain Management 10.0.28 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.28 finantside ja toimingute rakendustest (august 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md)

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.28 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan](/dynamics365-release-plan/2022wave1/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Artikli [eemaldatud või taunitud Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funktsioonid kirjeldavad funktsioone, mis on tarneahela halduses eemaldatud või plaaniliselt eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

