---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.26 (mai 2022)
description: See artikkel kirjeldab funktsioone, mis on Microsoft Dynamics 365 Supply Chain Management 10.0.26 uued või muutunud.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 8be79f259505c084a8680c453ec15a4cef1a890f
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124490"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.26 (mai 2022)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.26 uued või muutunud. Selle versiooni number on 10.0.1192 ja see on saadaval järgmiselt:

- **Väljalaske eelversioon:** märts 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** aprill 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** mai 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis muutsid selle koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud ja logistika | [Laovarude nähtavuse vaba kaubavaru päring täpsema laohalduse kaupade toetamiseks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Inventory Visibility WMS-i kaupade tugi](../inventory/inventory-visibility-whs-support.md) | Funktsioonihaldus:<br>*Laokauba lubamine varude nähtavuses* |
| Varud ja logistika | [Saadaval-lubadus varude nähtavuse lisandmooduli jaoks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Varude nähtavuse laoseisu muudatuste graafikud ja lubaduse andmiseks saadaval](../inventory/inventory-visibility-available-to-promise.md) | Lubatud teenuse konfiguratsiooni järgi |
| Tootmine | [Tootmispinna täitmisliidese tegeliku kaalu kaubad](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Kuidas töötajad kasutavad tootmisosakonna käivitusliidest](../production-control/production-floor-execution-use.md) | Funktsioonihaldus:<br>*(Eelversioon) Aruanne tegeliku kaalu üksuste kohta tootmisosakonna täideviimisliidesest* |
| Tootmine | Tootmisosakonna täideviimisliidese vahekaart Minu tööd <!-- KFM: Add link to release plan when available --> | [Kuidas töötajad kasutavad tootmisosakonna käivitusliidest](../production-control/production-floor-execution-use.md) | Funktsioonihaldus:<br>*Tootmisosakonna täideviimisliidese vahekaart Minu tööd* |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Hanked | Laos olevate toodete registreeritud koguste ja laos olevate toodete jääkide sisestamine kviitungite ja hankija arvete jaoks | See funktsioon muudab, kuidas hankija arvete ja sissetulevate saadetiste töötlemisel ostutellimuste suhtes sisestatakse ladustamata toodete (nt teenuste) kogused. Funktsioon *muudab* *registreeritud* koguse ja teenuste koguse valiku käitumist sissetulekute ja hankija arvete sisestamiseks, muutes selle nii, et see vastaks registreeritud koguse ja ladustamata toodete suvandi käitumisele, mis on müügi saatelehtedele koguste sisestamisel juba antud.<br><br>Kui kasutate toote *sissetuleku* või hankija arve sisestamisel registreeritud koguse ja teenuste koguse valikut, sisestab süsteem ladustatavate toodete registreeritud koguse ja sisestab mitte ladustatavate toodete jääkkoguse (sh teenused ja teenused, mida pole). Ilma selle funktsioonita sisestab süsteem siiski ladustatavate toodete registreeritud koguse (sh ladustatavate kaupadena konfigureeritud teenused), kuid sisestab alati kogu tellimata teenuse toodete koguse (ja *ignoreerib mitte ladustamata tooteid, mille tüüp ei ole Teenus*). |
| Hanked | Sünkroonige jälgimisdimensioonid ettevõtetevahelistel müügi- ja ostutellimuste ridadel | Selle funktsiooniga saate kontrollida, kas seeria- ja partiinumbri jälgimisdimensioonid sünkroonitakse kontsernisiseste müügi- ja ostutellimuste ridade vahel. See lisab uued sätted nii ostutellimuste **poliitikatele** **·** **kui ka klientide ja hankijate kontsernisisese** seadistuse lehe müügitellimuse poliitika vahekaartidele. Samuti uuendatakse seal mõne seotud ja selle lähedalasuva sätetega seotud sätete nimesid.<br><br>Kui kasutate laohaldusprotsesse (WMS), võtke arvesse, et see funktsioon sünkroonib partii- ja seerianumbrid ainult siis, kui need dimensioonid on sihtkoha reserveerimishierarhias asukohast kõrgemal. |
| Tooteteabe haldus | Puhastage toote atribuudiväärtused | See funktsioon lisab perioodilise ülesande nimega **Toote** atribuudi väärtuste puhastamine, mis puhastab toote atribuudi väärtuse kirjed, mis ei ole enam tootekategooria kaudu ühegi tootega seostatud. |
| Varude ja laohaldus | (Venemaa) Vältige lahknevusi WMS-i toega tooteid sisaldavate ostutellimuste GTD-de väljastamisel | See funktsioon on üksnes Vene lokaliseerimise jaoks. See takistab lahknevusi, mis ilmnevad Venemaa tollideklaratsiooni numbrite (GTD-de) väljastamisel impordi ostutellimustele, mis sisaldavad laohaldusprotsessidele lubatud kaupu (WMS). GTD väljaandmisprotsess muudab mõned varude dimensiooni väärtused seotud laokannetel arvete puhul, mis on kaasatud kohandatud töölehele, mis viib lahknevustele ostutellimuse töökirjete ja ostu laokannete vahel. Kui see funktsioon on lubatud, loob GTD-väljaandmisprotsess korrigeerimistöid, mis selliseid lahknevusi ei kustuta. |
| Laohaldus | Täiustatud parser GS1 vöötkoodide jaoks | See funktsioon lisab täiustatud parseri GS1 sümboliandmete jaoks. Uus parser juurutab GS1 üldise spetsifikatsiooni algoritmi GS1 sümbolite sõelumiseks ja pakub kinnitamist vajavad andmed. Lisateavet vt GS1 [vöötkoodi skannimine](../warehousing/gs1-barcodes.md). |
| Laohaldus | Uued koorma planeerimise töölaua leheküljed | Lisab kaks uut koorma planeerimise töölaualehte: **sissetuleva koorma planeerimise töölaud** **ja väljamineva koorma plaanimise töölaud**. |
| Laohaldus | Laohalduse rakendus – tühi GTD | See funktsioon on üksnes Vene lokaliseerimise jaoks. See võimaldab laohalduse mobiilirakendust kasutavatel töötajatel vajadusel Jätta Venemaa tollideklaratsiooni numbrid (GTD-d) tühjaks. Kui GTD jälgimisdimensioon on seadistatud lubama tühje väärtusi, aktsepteerib süsteem vaba kaubavaru operatsioonide GTD jaoks tühje väärtusi. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmised spikriartiklid. Need artiklid ei pea tingimata olema seotud uute funktsioonidega, mis selle väljalaske jaoks lisati, nagu on loetletud eelmistes jaotistes. Kuid need võivad aidata teil rohkem funktsionaalsust olemasolevatest funktsioonidest kätte saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Kuluhaldus | Igale järgmisele artiklile lisati värskendatud näited ja diagrammid:<ul><li>[FIFO füüsilise väärtuse ja märkimisega](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO füüsilise väärtuse ja märkimisega](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO kuupäev füüsilise väärtuse ja märgistusega](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Keskmine jooksev omahind](../cost-management/running-average-cost-price.md)</li><li>[Kaalutud keskmine füüsilise väärtuse ja märgistusega](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Microsoft Dynamics 365 Supply Chain Management 10.0.26 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.26 finantside ja toimingute rakendustest (mai 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md)

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.26 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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

