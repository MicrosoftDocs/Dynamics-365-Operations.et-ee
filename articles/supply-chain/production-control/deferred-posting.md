---
title: Lõpetatud kaupade enne töölehele sisestamist füüsiliselt kättesaadavaks tegemine
description: Kui toodetud kaup on lõpetatuna kinnitatud, registreeritakse see kui see on edasiseks füüsiliseks töötlemiseks saadaval ja sisestatakse üks või mitu töölehte. See artikkel kirjeldab, kuidas viittöölehe sisestusi, lubades neid töödelda pakett-tööna teatejärjekorras.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689336"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Lõpetatud kaupade enne töölehele sisestamist füüsiliselt kättesaadavaks tegemine

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Kui töötaja esitab aruande toodetud kauba lõpetatuna, registreerib süsteem selle edasiseks füüsiliseks töötlemiseks (nt saadetis või panemine) kättesaadavaks. Selle protsessi ajal sisestatakse ka üks või mitu töölehte (nt lõpetatuna kinnitatud tööleht, komplekteerimislehe tööleht ja protsessikaardi tööleht). Kui soovite kaubad enne kõigi sisestuste töötlemist füüsiliselt kättesaadavaks teha, saate seadistada süsteemi töölehe sisestuste edasilükkamise jaoks. Edasilükatud sisestusi haldab seejärel pakett-töö, mis töötleb sisestusi süsteemiressursside lubatudna.

Järgmine näide näitab, kuidas sisestustöölehtede protsesse käivitatakse nii sisestamisel kui ka ilma edasi lükatud sisestamiseta.

![Lõpetatuna kinnitatud protsess koos töölehe sisestamisega ja ilma edasilükatud töölehe sisestamisega.](media/deferred-posting-flowchart.png "Lõpetatuna kinnitatud protsess koos töölehe sisestamisega ja ilma edasilükatud töölehe sisestamisega")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Edasilükatud töölehe sisestamise sisse lülitamine süsteemi jaoks

Enne kui saate edasilükatud töölehe sisestamist kasutada, tuleb see süsteemi sisse lülitada. Administraatorid saavad funktsioonihalduse [tööruumi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kasutada, et kontrollida funktsiooni olekut ja lülitada see sisse. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *tootmise juhtimine*
- **Funktsiooni nimi:** *(eelvaade) Lõpetatud kaupade füüsiliselt kättesaadavaks teha enne töölehtedele sisestamist*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Töölehe sisestamissuvandite seadistamine lõpetatuna teatamiseks

Töötajad saavad kaupade lõpetatuna teatada, kasutades järgmisi kliente:

- Veebiklient
- Laohalduse mobiilirakendus
- Tootmispinna käivitamise liides

Veebiklient kasutab laohalduse mobiilirakendusega sama sisestusmeetodi konfiguratsiooni. Kuid sisestamismeetodit, mida tootmispinna käivitamise liides kasutab, tuleb konfigureerida eraldi.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Veebikliendi ja laohalduse mobiilirakenduse jaoks töölehe sisestamise suvandite määramine

Mobiilses rakenduses vad **töötajad** *·* *kaupade lõpetatuna, avades mobiilse seadme menüükäsu, kus töö loomise protsessi väärtus on Aruanne lõpetatuna või Teata lõpetatuna ja seadke ära.* Veebikliendis teatada kaubad lõpetatuna lehelt **Kõik tootmistellimused või** Tootmistellimuse **(üksikasjad) leheküljelt**. Saate konfigureerida kogu ettevõtet hõlmava vaikemeetodi ja samuti seadistada laopõhised alistused vastavalt vajadusele.

Kasutage järgmist protseduuri kogu ettevõtet hõlmava vaike-sisestusmeetodi konfigureerimiseks kaupade lõpetatuna teatamiseks veebikliendist või laohalduse mobiilirakendusest.

1. Minge tootmise **juhtimise seadistuse \>\> tootmisjuhtimise parameetritele**.
1. **Seadke vahekaardi Töölehed** jaotises Lõpetatuna **kinnitamine** **sisestusmeetodi** väljale üks järgmistest väärtustest:

    - *Vahetu* – kui kaup on lõpetatuna kinnitatud, töötleb süsteem täielikult kõik seotud töölehe sisestused, enne kui märgib lõpetatud kauba füüsiliselt kättesaadavaks.
    - *Edasi* lükatud – kui kaup on lõpetatuna kinnitatud, märgib süsteem lõpetatud kauba füüsiliselt saadaolevaks ja lisab töölehe sisestused teatejärjekorda. Süsteem ei oota enne, kui sisestused on täielikult töödeldud, enne kui märgib lõpetatud kauba füüsiliselt kättesaadavaks.

Kasutage järgmist protseduuri, et konfigureerida laopõhised alistamised vaikimisi sisestusmeetodi puhul, mis on **konfigureeritud tootmise juhtimise parameetrite** lehel.

1. Minge laohalduse **häälestuse \> varude \> jaotuse laod \>.**
1. Valige ladu, mida soovite seadistada.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Seadke jaotises **Tootmistellimused** lao **kiirkaardil** sisestusmeetodi **väljale** üks järgmistest väärtustest:

    - *Pärilus* – valitud ladu pärib sätte lehelt **Tootmise juhtimise parameetrid**.
    - *Vahetu* – kui kaup on lõpetatuna kinnitatud, töötleb süsteem täielikult kõik seotud töölehe sisestused, enne kui märgib lõpetatud kauba füüsiliselt kättesaadavaks.
    - *Edasi* lükatud – kui kaup on lõpetatuna kinnitatud, märgib süsteem lõpetatud kauba füüsiliselt saadaolevaks ja lisab töölehe sisestused teatejärjekorda. Süsteem ei oota enne, kui sisestused on täielikult töödeldud, enne kui märgib lõpetatud kauba füüsiliselt kättesaadavaks.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Töölehe sisestusvalikute määramine tootmispinna käivitamise liidesele

Kasutage järgmist protseduuri, et konfigureerida sisestusmeetod, mida kasutatakse siis, kui kaubad on tootmispinna käivitamise liidesest lõpetatuks kinnitatud.

1. Minge tootmisjuhtimise **seadistuse tootmise \>\> käivitamise \> tootmistellimuse vaikeväärtustele**.
1. **Seadke vahekaardi Lõpetatuna** kinnitatud töölehe **jaotises Lõpetatuna kinnitamine** **välja** Sisestusmeetod väärtuseks üks järgmistest väärtustest:

    - *Vahetu* – kui kaup on lõpetatuna kinnitatud, töötleb süsteem täielikult kõik seotud töölehe sisestused, enne kui märgib lõpetatud kauba füüsiliselt kättesaadavaks.
    - *Edasi* lükatud – kui kaup on lõpetatuna kinnitatud, märgib süsteem lõpetatud kauba füüsiliselt saadaolevaks ja lisab töölehe sisestused teatejärjekorda. Süsteem ei oota enne, kui sisestused on täielikult töödeldud, enne kui märgib lõpetatud kauba füüsiliselt kättesaadavaks.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Teateprotsessori pakett-töö plaanimine edasilükatud sisestuste töötlemiseks

Teateprotsessori pakett-töö vastutab töölehe sisestuste töötlemise eest pärast nende järjekordamist. Töölehe sisestuste töötlemise tagamiseks peate selle töö konfigureerima nii, et see töötaks regulaarse intervalliga. Kasutage järgmist protseduuri, et seadistada nõutav pakett-töö.

1. Minge süsteemihalduse **teateprotsessori \> teateprotsessorisse \>**.
1. Seadke kiirkaardi **Parameetrid** välja Teatejärjekord **väärtuseks** *Tootmine*.
1. Seadke kiirkaardiL **Käivita taustal** suvandi Pakktöötlus **väärtuseks** *Jah*. Seejärel seadistage korduv graafik ja konfigureerige muud vajalikud sätted. Sätted töötavad nii, nagu nad töötavad Microsofti muud [tüüpi taustatöödel](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Edasilükatud sisestuste edenemise jälgimine

Edasilükatud töölehe sisestused järjekorras olevad teateprotsessori *teadetena*, mis ootavad, kuni teateprotsessor neid *töötleb*. Teateprotsessor tuleb seadistada käivituma plaanitud pakett-tööna. Teadete töötleja poolt töödeldud või töödeldud edasilükatud sisestusteadete vaatamiseks minge **\>\> tootmisjuhtimise tootmistellimuste edasilükatud tootmistellimuse sisestamisele.**

### <a name="message-grid-columns-and-filters"></a>Teatepaneeli veerud ja filtrid

Saate kasutada välju edasilükatud **tootmistellimuse** sisestuslehe ülaosas, et aidata leida mis tahes kindlaid teateid, mida te otsite.

Saadaval on järgmised filtrid.

- **Teate tüüp** : määrake ruudustikus kuvatavate teadete tüüp.
- **Teate** olek: määrake ruudustikus kuvatavate teadete olek. On olemas järgmised tingimused:

    - *Järjekorras* – sõnum on teateprotsessori töötlemiseks valmis.
    - *Töödeldud* – sõnum on teateprotsessori poolt edukalt töödeldud.
    - *Tühistatud* – teadet ei õnnestunud lõpliku katse ajal töödelda ja kasutaja tühistas selle.
    - *Nurjus* – teadet ei õnnestunud viimase katse ajal töödelda. Süsteem kordab nurjunud teateid kolm korda. Siis loobub ja jätab sõnumi olekusse *Nurjunud*. Pange tähele, et te ei saa käsitsi sõnumit tühistada ega redigeerida enne viimast neist kolmest katsest.

- **Sõnumi sisu** – selle filtriga tehakse sõnumisisu täistekstotsing. (Teate sisu ei kuvata ruudustikus.) Filter käsitleb enamikku erisümboleid (nt sidekriipse) tühikumärkidena ning käsitleb kõiki ruumimärke Kahendmuutujate või tehtemärkidena. Näiteks kui otsite kindlat väärtust, `journalid`*mis on võrdne USMF-123456-ga*, otsib süsteem kõik teated, mis sisaldavad "USMF" või "123456." Sellisel juhul on tulemuste loend tõenäoliselt pikk. Seetõttu on parem sisestada *123456*, sest te saate konkreetsema tulemuse.

Saate loendit ka sortida ja filtreerida, valides mis tahes veeru pealkirjadest ja sisestades kriteeriumid ripploendisse.

### <a name="view-the-message-log-message-content-and-details"></a>Saate kuvada teatelogi, sõnumi sisu ja üksikasju

Teate kohta üksikasjaliku **teabe** **leiate**, valides selle ruudustikust ja valides teateruudustikust vahekaardi Logi või Toorsisu, kus kuvatakse iga töötlemissündmus.

Vahekaardi **Logi** tööriistaribal on järgmised nupud:

- **Logi** – valige see nupp, et kuvada töötlustulemused. See nupp on eriti kasulik, kui teadete **töötlemistulemuse** *väärtus on Nurjunud* ja te soovite teada töötluse tõrke põhjusi.
- **Kogum** – mitu teatetöötlustoimingut saab käitada ühe ja sama pakktöötluse osana. Selle nupu abil saate vaadata üksikasjalikke andmeid. Näiteks saate vaadata, kas on olemas sõltuvusi, mis nõuavad teatud teadete puhul konkreetset töötlemistellimust.

### <a name="manually-process-or-cancel-a-message"></a>Sõnumi käsitsi saatmine või tühistamine

Sõltuvalt selle praegusest olekust saate teadet vajaduse korral käsitsi töödelda või tühistada. Valige ruudustikus teade ja seejärel valige tegevuspaanil **suvand** **Töötle** või Tühista.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Saate häälestada ärisündmusi teatiste esitamiseks nurjunud töötlemise tulemuste kohta

Saate seadistada [ärisündmusi](../../fin-ops-core/dev-itpro/business-events/home-page.md), mis teavitavad teid ebaõnnestunud töötlustulemustest. Minge süsteemihalduse seadistuse **ärisündmuste \>\> ärisündmuste \> kataloogi ja aktiveerige ärisündmus, mille nimi** on Teateprotsessori teade *.*

Aktiveerimisprotsessi osana palutakse teil määrata, kas sündmus on omane ühele juriidilisele isikule või rakendub kõigile juriidilistele isikutele. Teil palutakse sisestada ka lõpp-punkti **nime** väärtus. See väärtus peab olema esimesena määratletud.

> [!NOTE]
> Kui väli **Ärisündmuse toimumisel** *Microsoft Power Automate* on seatud (*näiteks HTTPS-i* asemel), **luuakse** lõpp-punkti nime väärtus seadistuse põhjal automaatselt tarneahela halduses *Microsoft Power Automate*.
