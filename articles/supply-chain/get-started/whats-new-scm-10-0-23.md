---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.23. (jaanuar 2022)
description: See artikkel kirjeldab funktsioone, mis on Microsoft Dynamics 365 Supply Chain Management 10.0.23 uued või muutunud.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 1b45cc2ba26f60ab444edca6c513c581e8332a2a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219120"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10023-january-2022"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.23. (jaanuar 2022)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.23 uued või muutunud. Selle versiooni number on 10.0.1037 ja see on saadaval järgmiselt:

- **Väljalaske eelversioon:** oktoober 2021
- **Väljalaske üldine kättesaadavus (enesevärskendus):** detsember 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** jaanuar 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Veerg *Funktsioon* pakub linke [väljalaskeplaani](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) kus saate vaadata iga funktsiooni ametlikke väljalaskekuupäevi. Veerg *Lisateave* pakub üksikasju/linke seotud dokumentatsioonile. Funktsiooni sisselülitamise määratlemiseks vaadake veergu *Lubatud*. Lisateavet funktsioonihalduse kasutamise kohta vt [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Võime seda artiklit värskendada, et kaasata funktsioonid, mis muutsid selle koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Globaalne aadressiraamat | Määrake aadressi seadistuses iga riigi/piirkonna jaoks vaikeosariik/provints | Nüüd saate globaalse aadressiraamatu aadressi seadistuses määratleda iga riigi/piirkonna jaoks vaikeosariigi/provintsi. Kui vaikeosariik/provints on määratud, on see osariigi/provintsi väljadele sisestatud vaikeväärtus, kui loote selle riigi/piirkonna jaoks uue maakonna või linna kirje. Vaata ka [Aadressi häälestamine](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Vaikimisi lubatud. |
| Varud&nbsp;ja&nbsp;logistika | [Warehouse Management mobiilirakenduse ülesannete peatamine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Mobiilse seadme menüükäskude sammude ümbersuunamise konfigureerimine](../warehousing/warehouse-app-detours.md) | Funktsioonide haldamine (*Warehouse management rakenduse ümbersuunamised*) |
| Varud&nbsp;ja&nbsp;logistika | [Laorakenduse ülendatud väljad](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Mobiilseadmes sammude jaoks esiletoodud väljade konfigureerimine](../warehousing/warehouse-app-promoted-fields.md)| Funktsioonide haldamine (*Laohalduse rakenduse esiletoodud väljad*) |
| Tootmine | [Tootmise käivitamissüsteemide integreerimine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Kolmanda osapoole tootmise käivitussüsteemidega integreerimine](../production-control/mes-integration.md) | Funktsioonihaldus (Tootmise *käivitamissüsteemi integreerimine*) |
| Tootmine | [Tootmisosakonna täideviimisliidese kaas- ja kõrvalsaaduste aruanne](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Kuidas töötajad kasutavad tootmisosakonna käivitusliidest](../production-control/production-floor-execution-use.md) | Funktsioonide haldamine (*Kaas- ja kõrvalsaaduste aruanne tootmispõranda täitmisliidesest*) |
| Planeerimine | [Optimeerimise toetuse plaanimine prioriteedipõhiseks planeerimiseks](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Prioriteedipõhine planeerimine](../master-planning/planning-optimization/priority-based-planning.md) | Funktsioonihaldus (prioriteedipõhine *MRP tugi optimeerimise planeerimisel*) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske uued funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõnda neist funktsioonidest sisse või välja lülitada, peate seda tegema [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kus need on loetletud, kasutades järgmise tabeli veerus *Funktsiooni nimi funktsioonide halduses* näidatud nimesid.

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Varahaldus | Töökäsu töölehtedel olevad kulude vastaskontod | See funktsioon võimaldab teil määrata tasaarvestuskonto iga töökäsu töökirjas loetletud kulu jaoks. Tavaliselt võite iga kuluga siduda hankija konto, kuid toetatud on ka muud kontotüübid. See lisab lehel **Töökäsupäevik** vahekaardile **Kulud** kaks uut veergu (**Tasaarvestuskonto tüüp** ja **Tasaarvestuskonto**).|
| Kuluhaldus | Standardomahinna ümardamise ümberhindamise jaoks seotud vautšerite loomine | <p>Kui tehakse kannete finantsarvestus (nt müügitellimuse arve või laokanne), loob süsteem iga seotud standardkulu ümardamise ümberhindluse jaoks eraldi kande ja seob selle finantsi sisestuskandega seotud kandena.</p><p>Ilma selle funktsioonita salvestab süsteem standardkulu ümardamise ümberhindlused samale kande sisestamisele. Selline käitumine võib mõnikord põhjustada vastuolulisi kuupäeva andmeid, kuna ümberhindamised kasutavad seansi või süsteemi kuupäeva, samas kui finantssisestused kasutavad sisestuskuupäeva.</p> |
| Varude ja laohaldus | \[Venemaa\] Postitage storno finantsinventari tehingud müügitellimuste finantsvautšeril oleva paranduslipu järgi | See funktsioon mõjutab Venemaa kreeditarvete korrigeerimise funktsioone. See võimaldab müügiarvete laotehingud konteerida vastavalt pearaamatu parandusvõimalusele. Kui see funktsioon on lubatud, ei esine enam lahknevusi laotehingu finantskviitungil oleva lipu **Parandus** ja laotehingutel oleva lipu **Storno** vahel. |
| Varude ja laohaldus | (Venemaa) Varde saldo käibearuande arvutamise käitamine partiidena | Supply Chain Management haldamise venekeelsete tõlgete puhul annab see funktsioon võimaluse käitada *Varude saldo käibe* aruannet partiidena, seda salvestada ja vaadata varem koostatud aruandeid. |
| Varude ja laohaldus | (Venemaa) Laohalduses riigile või regioonile omastes peamistes vormides kohaliku keele tõlke kasutamine | Supply Chaing Managementi venekeelsete tõlgete puhul võimaldab see funktsioon kasutada toodete/kaubanimede ja mõõtühikute venekeelseid tõlkeid järgmistel venekeelsetel varude väljatrükkidel: loendusloend (INV-3), loendusloend (INV-5), ja loendusloend (INV-6). |
| Koondplaneerimine | Teenus Azure Machine Learning nõudluse prognoosi jaoks | See funktsioon võimaldab Azure’i masinaõppimisteenusel luua ajaloolistel andmetel põhinevaid nõudluse prognoose. Lisateavet vt nõudluse prognoosimise [häälestusest](../master-planning/demand-forecasting-setup.md). |
| Hanked | Ostutellimuse värskendamise ajaloo puhastamine | See funktsioon võimaldab teil puhastada ostutellimuse värskendustega seotud ajutisi ajaloolisi kirjeid. See lisab lehel **Kõik ostutellimused** toimingupaanile uue nupu nimega **Ostuvärskenduste ajaloo puhastamine**. Funktsioon on vaikimisi lubatud. |
| Tootmise juhtimine | Laos lubatud materjalide automaatne valimine automaatselt sisestatud komplekteerimislehtede jaoks | See funktsioon võimaldab teil automaatselt valida ja lahendada varude dimensioone automaatselt postitatud, tuletatud ja tagasilõigatud komplekteerimisloendi töölehtede jaoks. |
| Tootmise juhtimine | Kinnitage tooraine aegumiskuupäev kavandatud tarbimiskuupäeva suhtes | See funktsioon muudab partii aegumiskuupäevade valideerimist, kui reserveeritakse toormaterjali partii tootmiseks kasutamiseks. Kui see funktsioon on lubatud, kontrollitakse partii aegumiskuupäeva kavandatud tarbimiskuupäeva (tooraine kuupäeva) suhtes, mis on kehtestatud tootmismaterjalide rea või partiitellimuse valemi real. Kui see funktsioon on keelatud, kontrollitakse partii aegumiskuupäeva tootmis- või partiitellimuse kavandatud tarnekuupäeva suhtes (nagu varem). |
| Müük ja turundus | Müügi värskendamise ajaloo puhastamine vanuse põhjal | See funktsioon võimaldab teil seada kirjete maksimaalse vanuse, kui käitatakse müügi uuendamisajaloo **perioodilist puhastusülesannet**. Vanemad kirjed kustutatakse. See on kasulik, kui seadistate ülesande perioodiliseks käivitumiseks, kuna iga arvutatakse alati vastavalt ülesande käituskuupäevale. Ilma selle funktsioonita saate määrata ainult konkreetse kuupäeva vanimatele säilitamiskirjetele. Lisateavet vt müügiajaloo [andmete puhastamise plaanimine](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Müük ja turundus | Parandage klientide aruande „100 esimest” jõudlust | See funktsioon parandab **Top 100** klientide aruande toimivust, käitades aruannet alati kõigi klientide kohta (see on selle kavandatud kasutus), mitte lubades kohandatud päringuid. Kui see funktsioon on lubatud, on kõik **Kaasatavad kirjed** sätted **Top 100** aruandedialoogis keelatud. |
| Laohaldus | Skaalaüksuse tugi väljaminevate tellimuste laole vabastamiseks | Kui see funktsioon on lubatud, saab väljaminevad tellimused jaoturist vabastada otse skaalaüksusesse, kus tellimused täidetakse. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmised spikriartiklid. Need artiklid ei pea tingimata olema seotud uute funktsioonidega, mis selle väljalaske jaoks lisati, nagu on loetletud eelmises jaotises. Kuid need võivad aidata teil rohkem funktsionaalsust olemasolevatest funktsioonidest kätte saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Tehnilise muudatuse haldamine | [Tehnilised atribuudid ja tehnilise atribuudi otsing](../engineering-change-management/engineering-attributes-and-search.md) nüüd kirjeldab, kuidas tehnilise atribuudi pärimine töötab. |
| Koondplaneerimine | [Üldplaneering nõudluse prognooside](../master-planning/planning-optimization/demand-forecast.md) ja [Prognoosi vähendamise võtmetega](../master-planning/reduction-keys.md) pakuvad nüüd rohkem teavet vähendamise võtmetega töötamise kohta. |
| Koondplaneerimine | [Kaubavarude ohutu täitmine](../master-planning/safety-stock-replenishment.md) annab nüüd rohkem teavet miinimum-/maksimumivõtmete kasutamise kohta. |
| Koondplaneerimine | [Varude prognoosid](../master-planning/inventory-forecast.md) pakuvad nüüd rohkem teavet prognooside jaotamise kohta. |
| Koondplaneerimine | [Tarnegraafik](../master-planning/supply-schedule.md) |
| Laohaldus | [Mobiilsete seadmete globaalsed parameetrid](../warehousing/mobile-device-parameters.md) |
| Laohaldus | [Ankurdamine](../warehousing/anchoring.md) |
| Müük ja turundus | Kontsernisisest kaubandust on nüüd üksikasjalikult kirjeldatud, alustades [kontsernisisese](../sales-marketing/intercompany-trade-set-up.md) kaubanduse ja sellega seotud artiklitega. |
| Müük ja turundus | [Müügiajaloo puhastamise jõudluse täiustused](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Varud | Lao nähtavuse dokumentatsiooni on laiendatud ja uuendatud, alustades varude [nähtavuse lisandmooduli ülevaatega](../inventory/inventory-visibility.md) ja selle seotud artiklitega. |
| Laohaldus | [Mobiilse seadme kasutaja kontod](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Microsoft Dynamics 365 Supply Chain Management 10.0.23 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.23 finantside ja toimingute rakendustest (november 2021).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md)

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.23 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 ja majandusharu pilved: 2021 väljalaskevoo 2 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2021 väljalaskevoo 2 plaan](/dynamics365-release-plan/2021wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Artikli [eemaldatud või taunitud Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funktsioonid kirjeldavad funktsioone, mis on tarneahela halduses eemaldatud või plaaniliselt eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

