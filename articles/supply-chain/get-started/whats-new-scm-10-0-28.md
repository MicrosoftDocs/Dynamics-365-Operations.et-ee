---
title: Dynamics 365 Supply Chain Management 10.0.28 eelvaade (august 2022)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.28 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813158"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Dynamics 365 Supply Chain Management 10.0.28 eelvaade (august 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas loetletakse funktsioonid, mis on Microsofti eelvaate versioonis Dynamics 365 Supply Chain Management 10.0.28 uued või muutunud. Sellel versioonil on järgu number 10.0.1264 see on saadaval järgmises graafikus.

- **Väljalaske eelversioon:** mai 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuli 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuli 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda teemat uuendada, et kaasata funktsioonid, mis lisati järgule pärast selle teema algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud ja logistika | [Väljaminekuga kulude integreerimise üksused kolmandate osapoolte veostele](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Väljaminev kuluüksuste ülevaade](../landed-cost/landed-cost-entities-overview.md) | Vaikimisi lubatud |
| Planeerimine | [Kõlblikkusaja plaanimise optimeerimise tugi](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Peagi tulekul <!-- KFM: Vendor is preparing this. Expected May 20. --> | Vaikimisi lubatud |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Varude ja laohaldus | Luba kontsernisisesel vabal kaubavarul kuvada ainult nullist erinev laoseis | See funktsioon võimaldab teil valida, kas null vaba kaubavaruga kaubad tuleks kaasata kontsernisisesesse vaba kaubavaru loendisse. Seda valikut **saate** juhtida, kasutades valikut Ära kuva null vaba kaubavaruga kaupu kontsernisisese vaba kaubavaru loendi sättes **, mille see funktsioon lisab varude ja laohalduse parameetrite lehele**. |
| Varude ja laohaldus | (India) Üleviimise hinnareeglite puhul ignoreerige asukohta, kui "Lao koodist" on seatud väärtusele "Kõik" | <p>See funktsioon kehtib ainult India lokaliseerimise puhul. See muudab laoülekannete ülekandehindade seadistamise intuitiivsemaks.</p><p>Te seadistate ülekande hinnad, konfigureerides iga kaupa ülekande hinnakujunduse reeglitega. Üks võimalus seda konfiguratsiooni teha on kaasata reegli rida, kus **välja Laost kood** väärtuseks on määratud *Kõik*. See säte näitab, et rea määratletud ülekande hind peaks rakenduma sõltumata laost, millelt kaup komplekteeritud on. Kui see funktsioon on lubatud, eiravad ülekande **hinnareeglid**, kus väli Laost koodi väli on *seadistatud* sättele Kõik, asukoha **sätet**. Seetõttu rakendub reegel sõltumata üleviimistellimusel määratud asukohast. Selline käitumine on eeldatav, sest asukoht on laoala dimensiooni hierarhias laost allpool.</p><p>Ilma selle funktsioonita kohaldab süsteem seda tüüpi reegleid ainult siis, kui üleviimistellimuse asukoht ühtib täpselt reegli jaoks seadistatud asukohaga. (Kui reegli jaoks on tühi asukoht määratud, rakendab süsteem reeglit ainult üleviimistellimustele, mille asukoha väärtus on samuti tühi.)</p> |
| Varude ja laohaldus | Laoseisu aruande andmete puhastamine | See funktsioon võimaldab puhastada andmeid, mida kasutatakse laoseisu *aruande ladustamisaruannete loomiseks*. |
| Tootmise juhtimine | Määrake projektitegevused teenuseleppe ja teenusetellimuse ridadele | See funktsioon lisab välja nimega Projekti **tegevus** teenuselepingule ja teenusetellimuse ridadele, nii et saate nende jaoks seada projekti tegevuse. See funktsioon aitab vältida blokeerimisvigu, kui sisestate teenusehalduse projektitöölehti, mis nõuavad projekti tegevuse seadistamist.  |
| Laohaldus | Käsitsi ülekanderea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele | See funktsioon võimaldab administraatoril käsitsi komplekteeritud laokandeid, mis on seotud üleviimisridadega. Need read sisaldavad juba lattu väljastatud ridu. Administraatorid peaksid seda komplekteerimist tegema ainult erandlikel juhtudel, näiteks siis, kui süsteem on rikutud olekus. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt värskendanud järgmised Spikriteemad. Need teemad ei ole tingimata seotud uute funktsioonidega, mis sellele väljalaskele lisati, nagu on loetletud eelmistes jaotistes. Kuid need võivad aidata teil rohkem olemasolevatest funktsioonidest välja saada.

| Funktsiooniala | Uued või värskendatud teemad |
|---|---|
| Kuluhaldus | [Fikseeritud jaehind](../cost-management/fixed-receipt-price.md) |
| Kuluhaldus | [Laokulu korduma kippuvad küsimused](../cost-management/inventory-costing-faq.md) |
| Kuluhaldus | [Sisesta kulukonto raamatupidamispõhimõttesse](../cost-management/post-to-charge-account-accounting-principle.md) |
| Varud | [Laokande üksikasjad](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.28 sisaldab platvormivärskendusi. Lisateavet leiate finantside ja [toimingute rakenduste versiooni 10.0.28 platvormi värskendustest (juuni 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md)<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.28 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan](/dynamics365-release-plan/2022wave1/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
