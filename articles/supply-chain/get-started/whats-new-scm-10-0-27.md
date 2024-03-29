---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.27 (juuli 2022)
description: See artikkel kirjeldab funktsioone, mis on Microsoft Dynamics 365 Supply Chain Management 10.0.27 uued või muutunud.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 3ce3b2f3524dbeb043717ed9ef5429ea0eea4b8a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427796"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10027-july-2022"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.27 (juuli 2022)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.27 uued või muutunud. Sellel versioonil on järgu number 10.0.1227 see on saadaval järgmises graafikus.

- **Eelvaateversiooni välja andmine:** aprill 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuni 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuli 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud ja logistika | [Varude eraldamine varude nähtavuse lisandmooduli jaoks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Inventory Visibility varude eraldamine](../inventory/inventory-visibility-allocation.md) | Vaikimisi lubatud |
| Tootmine | Tootmisosakonna täideviimisliidese vaade Minu päev | [Kuidas töötajad kasutavad tootmispinna käivitamise liidest](../production-control/production-floor-execution-use.md) ja kuvavad [puhkusesaldosid tootmispinna käivitamise liideses](../production-control/production-floor-execution-payroll-stats.md) | Funktsioonihaldus:<br>*Tootmisosakonna täideviimisliidese vaade Minu päev* |
| Planeerimine | [Plaanimise optimeerimise tugi allhankeks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Allhanketöö haldamine tootmises](../production-control/manage-subcontract-work-production.md) | Vaikimisi lubatud |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Koondplaneerimine | Arvestage plaanitud üleviimistellimuse loomisel lao täitmisajaga | Kui luuakse plaanitud üleviimistellimus, arvestab süsteem kauba vaiketellimuse sätetes määratud lao täitmisaega plaanitud üleviimistellimuse sissetuleku kuupäeva arvutamisel tarnekuupäeva kontrolli seadistuse jaoks täitmisajana *tüübiga* Pole või *Müük*. Kui ülekande täitmisaeg on määratud, kasutatakse selle väärtust sissetulekukuupäeva arvutamiseks ja transpordipäevade ignoreeritakse. |
| Hanked | Maaklerilepingu vaikemaksuteave hankijaarve ridadel | See funktsioon tutvustab loogikat, et seadistada **maaklerilepingu** **hankija** arve ridade käibemaksu ja kauba käibemaksu väljadele vaikeväärtused. Seda loogikat rakendatakse ainult siis, kui maaklerilepingu real on pearaamat/pearaamat. Kauba käibemaksugrupp võtab vaikeväärtuse kas maakleritasu hankekategooriast (kui see on häälestatud) või tasu tüübist. Käibemaksugrupp võtab vaikeväärtuse hankija kontolt. |
| Hanked | Ostutellimuse ridade arvu piiramine partiiülesande kohta | See funktsioon aitab teil optimeerida süsteemi jõudlust kinnituste ja toote sissetulekute sisestamisel. See lisab **hankeparameetrite** **·** **lehe vahekaardile Tarne uue sätte nimega Read ülesande** kohta. See uus säte võimaldab teil piirata ostutellimuse ridade arvu, mida iga partii ülesande protsesse. Seega võib see takistada suurte pakktöötluste süsteemi aeglasemaks tegemist. |
| Tooteteabe haldus | Toote atribuudiväärtuste asustamine | See funktsioon lisab perioodilise ülesande nimega Asusta *tooteatribuudi väärtused*. See uus perioodiline ülesanne loob puuduva tooteatribuudi väärtuskirjed atribuutide jaoks, mis seostatakse toodetega tootekategooria kaudu. |
| Tootmise juhtimine | Tootmisosakonna täideviimisliidese täiendav konfiguratsioon | <p>See funktsioon lisab tootmispinna käivitamise lehe **konfigureerimisele järgmised** valikud:</p><ul><li>**Ava otsingu lõpuleviimisel automaatselt avanev dialoogiaken** – kui see suvand on lubatud, avatakse automaatselt dialoogiaken Alusta tööd, **kui** töötajad kasutavad töö otsimiseks otsinguriba.</li><li>**Aruande edenemise automaatne dialoog otsingu lõpuleviimisel** – kui see suvand on lubatud, avatakse töö edenemise dialoogiboks automaatselt, **kui** töötajad kasutavad töö otsimiseks otsinguriba.</li><li>**Järelejäänud vaikekogus aruande edenemise** dialoogis – kui see suvand on lubatud, **kuvatakse** dialoogiaknas Edenemise aruanne järelejäänud kogus, et tootmistööst aru saada.</li></ul><p>Lisateavet vt tootmise juhtimise [liidese konfigureerimine](../production-control/production-floor-execution-configure.md).</p> |
| Tootmise juhtimine | Tootmistöörühmad tootmisosakonna täideviimisliideses | <p>Kui samale tootmistööle on määratud mitu töötajat, saavad nad nüüd piloodiks määrata ühe töötaja. Ülejäänud töötajatest saavad automaatselt selle piloodi abid. Tulemuseks saadud töörühma puhul peab töö olekut registreerima ainult piloot, ajakirjed aga kõigile töörühma liikmetele. See funktsioon toetab ka stsenaariumi nimega *abiressurss*. Selles stsenaariumis saab töötaja registreerida end teise töötaja assistendiks, kes saab seejärel vastloodud grupi piloodiks.</p><p>Lisateavet vt teemast Kuidas töötajad [kasutavad tootmispinna täitmisliidest](../production-control/production-floor-execution-use.md).</p> |
| Tootmise juhtimine | Plaanimisüksuste aruanne tootmisosakonna täideviimisliideses | See funktsioon lihtsustab partiitellimuste aruandluse protsessi kaupade planeerimiseks tootmisplaani käivitamise liideses. Kui partiitellimus on loodud *tootele*, mille tootmistüüp on Plaanimine, saab lõpetatuna kinnitatud teha ainult selle partiitellimuse kaastoodete ja kaastoodete puhul. Kaupade planeerimiseks kasutatavaid partiitellimusi kasutatakse tavaliselt selleks, et toetada ladumisprotsessi, kus toormaterjal jagatakse mitmeks eristatavaks tooteks. Kui töötaja esitab lõpetatuna planeerimiseks partiitellimuse, **kuvatakse** edenemise dialoogiaknas nüüd ainult kaastooted ja kaastooted. Varem ilmnes ka plaanimisüksus ja selline käitumine võib töötajaid segadusse ajada. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt värskendanud järgmised spikriartiklid. Need artiklid ei pea tingimata olema seotud uute funktsioonidega, mis selle väljalaske jaoks lisati, nagu on loetletud eelmistes jaotistes. Kuid need võivad aidata teil rohkem olemasolevatest funktsioonidest välja saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Kuluhaldus | [Kaalutud keskmise kuupäev koos kaasa füüsilise väärtuse ja märkimisega](../cost-management/weighted-average-date.md) |
| Hajutatud hübriidtopoloogia | [Skaalaühikute proovimine hajutatud hübriidtopoloogias](../cloud-edge/cloud-edge-try-out.md) |
| Topeltkirjutus | [Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Laohaldus | [Lattu väljastamine](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Microsoft Dynamics 365 Supply Chain Management 10.0.27 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.27 finantside ja toimingute rakendustest (juuli 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md)

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.27 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

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

