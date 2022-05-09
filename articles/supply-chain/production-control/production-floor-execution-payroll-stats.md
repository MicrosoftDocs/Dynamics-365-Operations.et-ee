---
title: Näita puhkusesaldosid tootmispinna käivitamise liideses
description: See teema annab näide stsenaariumi, mis Dynamics 365 Supply Chain Management näitab, kuidas Microsoft seadistada nii, et see kasutab palgastatistikat, et anda töötajatele ülevaade oma praeguse aasta puhkusesaldost.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: a97858c72b0be50609cee552bd0635e2d68ea478
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648163"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Näita puhkusesaldosid tootmispinna käivitamise liideses

[!include [banner](../includes/banner.md)]

See teema annab näide stsenaariumi, Dynamics 365 Supply Chain Management mis näitab, kuidas Microsoft seadistada nii, et see kasutab palgastatistikat, et anda igale töötajale ülevaade oma praeguse aasta puhkusesaldost. Töötajad saavad oma puhkusesaldot näha tootmispinna **käivitamise** liidese dialoogiboksis Minu päev.

See stsenaarium kasutab Taani pühaseadust, kus puhkuseaasta on 1. september – 31. august. Selles stsenaariumis on teie ettevõte palganud uue töötaja ja annab sellele töötajale ülejäänud puhkuseaastaks 10 puhkusepäevasaldo.

## <a name="turn-on-the-required-features"></a>Nõutavate funktsioonide sisselülitamine

Selle stsenaariumi käivitamiseks peate lubama funktsioonihalduse *tootmispinna täitmisliidese* vaate "Minu [päev"](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Lisateavet selle ja teiste tootmispinna käivitamise liidese funktsioonide lubamise kohta vt Tootmise [juhtimise käivitamise liidese konfigureerimine](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

## <a name="create-a-new-pay-type"></a>Uue tasutüübi loomine

Alustage uue tasutüübi *loomisega,* mis jälgib töötajate teenitud puhkusepäevi (nimetatakse ka töötajate *puhkusesaldoks*). Tavaliselt kasutatakse töötajate tasu arvutamiseks tasutüüpe. Siin loomisel kasutatavat tasutüüpi kasutatakse siiski saldo arvutamiseks.

1. Minge jaotisesse **Kellaaeg ja kohalviibimise \> palgaarvestuse \> tasutüübid \>**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Seadke uuel real järgmised väärtused:

    - **Tasu tüüp:** *5151-1*
    - **Kirjeldus:** *töötaja puhkusepäevade loendur*
    - **Kaasa eksporti:** *Ei*

## <a name="update-the-pay-agreement"></a>Tasulelepingu värskendamine

Selles jaotises redigeerite *olemasolevat* tasulelepingut, lisades uue tasutüübi ja seadistades reeglid, mis määravad, kuidas iga töötaja puhkusesaldot puhkusepäevade registreerides korrigeeritakse.

1. Avage kellaaeg ja **kohalviibimise palgaarvestuse \>\> tasuleppe \> seadistus**.
1. Valige tasuleleping, kus soovite puhkusepoliitika seadistada. (Kui töötate standardsete USMF-i näidisandmetega, on ainult üks tasuleleping, *Man*.)
1. Kontrollige, kas valitud tasuleleping kehtib praeguse kuupäeva kohta. Kui töötate standardsete USMF-i näidisandmetega, **·** *võib* tootja tasulelepingu välja Kuupäevani väärtuseks olla määratud möödunud kuupäev. Muutke väärtust nii, et see oleks aasta või kaks tulevikus, nagu nõutud.
1. Tegevuspaanil valige Lepingu **read**.
1. **Seadke tasulelepingu** ridade lehe kiirkaardi **Ülevaade** tööriistaribal järgmised väärtused:

    - Valige esimeses ripploendis **esmaspäev**.
    - Valige teises ripploendis **Puudumine**.

1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Seadke uuel real tasutüübi **väljale** selle stsenaariumi jaoks loodud tasutüüp (*5151-1*). Jätke kõik teised väljad vaikeväärtustele.
1. Kui uus rida on veel valitud, seadke **kiirkaardil** Üldine järgmised väärtused:

    - **Puudumise kood:** *puhkus*
    - **Kasuta fikseeritud kogust:** *Jah*
    - **Konstant:** *-1*

1. Tegevuspaanil valige suvand **Kopeeri päev**.
1. **Seadke dialoogiboksis Päeva** kopeerimine järgmised väärtused:

    - **Teisipäev**, **kolmapäev**, **neljapäev** ja reede **:** *Jah*
    - **Kirjuta üle:** *Jah*
    - **Puudumine:** *Jah*

1. Valige nupp **OK**.

## <a name="create-a-payroll-statistic-group"></a>Palgastatistikagrupi loomine

*Palgastatistikagruppe* kasutatakse töötaja registreerimiste statistika häälestamiseks perioodi jooksul. Selles stsenaariumis kasutate palgastatistika gruppi, et arvutada puhkusepäevade arvu, mida töötajad puhkuseperioodil teenivad. Taanis kestab puhkuseperiood 1. septembrist kuni 31. augustini.

1. Minge leheküljele **Kellaaeg ja kohalviibimise \>\> häälestus Palgastatistika \> grupid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Seadke uuel real järgmised väärtused:

    - **Palgastatistikagrupp:** *FS*
    - **Kirjeldus: puhkusesaldo** *·*
    - **Ülekanne:** *ei*

1. Kui uus rida on endiselt valitud, valige tegevuspaanil **seadistus**.
1. **Ruudustiku rea** lisamiseks valige häälestuse **paanil** suvand Uus.
1. Seadke uuel real tasutüübi välja **väärtuseks** *5151-1*.
1. Valige ja hoidke all (või paremklõpsake) välja **Perioodi** kood ning valige suvand **Kuva üksikasjad**. Nüüd saate seadistada perioodikoodi, mille hiljem sellele väljale määrate.
1. Valige tegevuspaanil **periooditüüpide** lehel väärtus **Uus**, et lisada rida ruudustikule.
1. Seadke uuel real järgmised väärtused:

    - **Perioodi tüübid:** *YearYear*
    - **Kirjeldus:** *puhkuseaasta*
    - **Sagedus:** *aastad*

1. Kui uus rida on endiselt valitud, valige **tegevuspaanil** suvand Loo perioodid.
1. **Seadke dialoogiboksis** Perioodide loomine järgmised väärtused:

    - **Määrake perioodi alguskuupäev: 1.** *september 2021.*
    - **Perioodi pikkus:** *5*

1. Valige nupp **OK**.
1. Sulgege leht **Perioodi tüübid**, et naasta palgastatistika **gruppide lehele**.
1. Seadke välja **Perioodi kood** väärtuseks äsja loodud periooditüübile (*YearYear*).

## <a name="create-a-statistical-balance-setup"></a>Statistilise saldo häälestuse loomine

Selles jaotises saate luua statistilise saldo *seadistuse*, mis on seotud eelmises jaotises loodud palgastatistika grupiga. Hiljem seote selle statistilise saldo seadistuse tootmispinna **käivitamise** liidese vaatega Minu päev. Sel **juhul** saab vaade Minu päev näidata seotud palgastatistika grupile määratud tasutüübi puhkusesaldosid.

1. Minge leheküljele **Kellaaeg ja kohalviibimise häälestus \>\> Palga statistiline \> saldo häälestus**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Seadke uuel real järgmised väärtused:

    - **Palgastatistikagrupp:** *FS*
    - **Välisnimi: puhkusesaldo** *·*
    - **Paind:** *ei*

## <a name="create-a-manual-premium"></a>Käsipreemia loomine

*Käsipreemiaid* kasutatakse tavaliselt töötajate lisatöö eest lisatasu andmiseks. Selle stsenaariumi korral loote käsitsi preemia, mida saate kasutada iga töötaja algse puhkusesaldo häälestamiseks.

1. Minge leheküljele **Kellaaeg ja kohalviibimise \> seadistus \> Palgaarvestus käsipreemiad \>**.
1. Tegevuspaanil valige kirje **lisamiseks** suvand Uus.
1. Seadke uuel kirjel järgmised väärtused:

    - **Preemiad:** *FS*
    - **Kirjeldus:** *töötajate puhkusesaldo korrigeerimised*
    - **Tasu tüüp:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Töötaja algse puhkusesaldo seadmine ja selle korrigeerimine ühe päevaga

Palgaarvestuse administraatorid kasutavad lehte **Kinnita**, et vaadata üle ja kinnitada töötajate igapäevaseid registreerimisi. Selles stsenaariumis võtate administraatori rollile nii, et saate töötajale seada algse puhkusesaldo ja registreerida töötaja puhkusepäevad.

1. Minge kellaaja ja **kohalviibimise ülevaatuse \> ja kinnitage kinnitamist \>**.
1. **Seadke dialoogiboksis** Kinnitamine järgmised väljad:

    - **Kinnitusegrupp** – valige kinnitusegrupp, kuhu te kuulute. (Kui töötate standardsete USMF-i näidisandmetega, on ainult üks kinnitusgrupp, *AdmMan*.)
    - **Vaadake tervet gruppi, 1** päev – valige suvand ja seejärel seadistage väli praegusele kuupäevale.

1. Valige nupp **OK**.
1. Kinnitamisleht **kuvab** teie kriteeriumile vastavad kirjed. Valige töötaja, kelle soovite kinnitada. Kui töötate standardsete USMF-i näidisandmetega, valige töötaja *000496* (*Portra*).
1. Anna valitud töötajale 10 puhkusepäeva.

    1. Kui töötaja on endiselt valitud, valige tegevuspaanil **preemiaread**.
    1. Rea lisamiseks **ruudustikule** **valige** preemiaridade lehekülje tegevuspaanil väärtus Uus.
    1. Seadke uuel real järgmised väärtused:

        - **Preemiad:** *FS*
        - **Kogus:** *10*

    1. Sulgege preemiaridade **leht**.

1. Registreerige **lehel** Kinnitamine fakt, et töötaja kasutas jooksval kuupäeval üht oma puhkusepäevast:

    1. Kui töötaja on endiselt valitud, **valige** lehe alumises osas vahekaardil Ülevaade tööriistaribal suvand Uus, **et** lisada rida ruudustikule.
    1. Seadke uuel real järgmised väärtused:

        - **Töölehe registreerimise tüüp:** *puudumine*
        - **Viide:** *puhkus*

    1. Lehe ülaosas valige tööriistaribal Ülekanne **, et** rakendada puhkusesaldot ja arvutada mahaarvamine.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfigureerige tootmispinna käivitamise liides nii, et see sisaldab dialoogiboksi Minu päev.

Selles jaotises saate tootmispinna käivitamise **liidesele** lisada nupu Minu päev. Töötajad saavad seda nuppu kasutada dialoogiboksi **Minu päev** avamiseks.

1. Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**.
1. Valige konfiguratsioon, nt *Vaikimisi*.
1. Tegevuspaanil valige **vahekaart Kujundus**.
1. Valige vahekaardi **Kujundus** loendipaanil suvand Kõik *tööd*, et vaadata selle vahekaardi sätteid. Väli **Peavaade** peaks nüüd kuvama kõigi *tööde väärtuse*.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige teisese **tööriistariba** kiirkaardi veerus Saadaolevad **tegevused** suvand Minu **päev**. Seejärel valige paremnoolenupp, et teisaldada see valitud **tegevuste veergu**.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Kontrollige oma saldot tootmispinna käivitamise liideses

Selles jaotises saate sisse logida tootmispinna täitmisliidesesse kui töötaja, kelle puhkuseaja seadistasite varem. Siis avate dialoogiboksi Minu **päev** oma puhkusesaldo vaatamiseks.

1. Minge tootmisjuhtimise **seadistuse tootmise \>\> käivitamise tootmispinna \> käivitamisele**.
1. Kui teil palutakse valida konfiguratsioon, valige konfiguratsioon, mille selles stsenaariumis varem seadistasite (*vaikimisi*).
1. Logi sisse kasutajana, mille selles stsenaariumis seadistasite. Kui töötate standardsete USMF-i näidisandmetega, peaksite olema võimeline sisse logima, *sisestades 123* **väljale Badge ID**. See badge ID vastab bad Portrale.
1. Valige **vasakul tööriistaribal** suvand Minu päev.
1. Kontrollige **dialoogiboksi saldode** osa. Sellest jaotisest tuleb nüüd näidata, et teil on üheksa puhkusepäeva saldo.
