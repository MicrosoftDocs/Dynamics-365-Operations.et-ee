---
title: Töökaardi seadmes lõpetamisest teatamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida süsteemi nii, et töökaardi seadme kasutajad saavad kanda lõpetatud tooted tootmistellimusest üle varudesse.
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2fa82c721316fb21442e1cfc00ba00ff8cb2b750
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778227"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Töökaardi seadmes lõpetamisest teatamine

[!include [banner](../includes/banner.md)]

Töötajad kasutavad tootmistöö lõpetatud kogustest teatamiseks töökaardi seadme lehte **Edenemisest teatamine**. See teema kirjeldab, kuidas seadistada erinevaid valikuid, mis määravad, kuidas töötajad saavad selle lehe abil lõppu kinnitada ja mis järgmisena juhtub. Valikud on järgmised.

- Lõpetatuna teatatud toodete varudesse lisamise kindluse ja viisi kontroll.
- Kontrollige, kas ja kuidas partiinumbreid luuakse ja rakendatakse lõpetatuna kinnitamisel.
- Kontrollige, kas ja kuidas seerianumbreid luuakse ja rakendatakse lõpetatuna kinnitamisel.
- Kontrollige, kas ja kuidas lõpetatuna kinnitada litsentsiplaadile.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Lõpetatuna teatatud tooted varudesse lisamise kontroll

Selleks, et kontrollida, kas ja kuidas viimase toimingu puhul lõpetatuna teatatud kogused tuleks lisada varudesse, toimige järgmiselt.

1. Avage **Toote juhtimine \> Seadistamine \> Tootmise käivitamine \> Tootmistellimuse vaikesätted**.
1. Määrake vahekaardil **Teata lõpetamisest** välja **Uuenda lõpetatud aruannet võrgus** väärtuseks üks järgmistest väärtustest.

    - **Ei** – ühtki kogust ei lisata varudesse, kui kogused viimases toimingus esitatakse. Tootmistellimuse olek ei muutu kunagi.
    - **Olek + Kogus** – tootmistellimuse oleku väärtuseks muutub *Lõpetamine kinnitatud* ja kogus kinnitatakse lõpetatuna varudesse.
    - **Kogus** – tootmistellimuse oleku väärtus muutub lõpetatuks, kuid tootmistellimuse olek ei muutu kunagi.
    - **Olek** – muutub üksnes tootmistellimuse olek. Koguste viimases toimingus kinnitamise järel ei lisata koguseid varudesse.

> [!NOTE]
> Koguseid ei jälgita laos, kui toimingud, milles need on lõpetatuna kinnitatud, ei ole määratletud viimase toiminguna. Samas saab neid koguseid kasutada edenemise kuvamiseks. Samuti saab need kaasata reeglitesse, mis kontrollivad, kas töötajad saavad enne eelmise toimingu kinnitatud koguste kohta määratletud künnise ületamist alustada järgmist toimingut. Need reeglid saate määratleda lehe **Tootmistellimuse vaikesätted** vahekaardil **Koguste kinnitamine**.

Lehega **Tootmistellimuse vaikesätted** töötamise kohta vaadake lisateavet teemast [Juhtimise parameetrid tootmise käivitamises](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Partii kaudu juhitud kaupade lõpetatuna teatamine

Töökaardi seade toetab partiikaupade aruandluse osas kolme stsenaariumit. Need stsenaariumid kehtivad nii kaupadele, mis on lubatud täpsemate laoprotsesside jaoks, kui ka kaupadele, mis ei ole täpsemate laoprotsesside jaoks lubatud.

- **Käsitsi määratud partiinumbrid** — töötajad sisestavad kohandatud partiinumbri. Partiinumber võib tuleneda välisallikast, mis ei ole süsteemile teada.
- **Eelmääratletud partiinumbrid** — töötajad valivad partiinumbri partiinumbrite loetelust, mille süsteem on enne tootmistellimuse töökaardi seadmele väljastamist automaatselt loonud.
- **Kindlaks määratud partiinumbrid** — töötajad ei sisesta ega vali partiinumbrit. Selle asemel määrab süsteem tootmistellimusele enne väljastamist automaatselt partiinumbri.


### <a name="enable-the-feature-on-your-system"></a>Funktsiooni lubamine teie süsteemis

Selleks, et lubada töökaardi seadmel aktsepteerida lõpetatuna kinnitamise ajal partiinumbrit, peate kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada sisse järgmised funktsioonid (samas järjekorras).

1. Töökaardi vahendi aruande edenemise dialoogi täiustatud kasutuskogemus
1. Võimaldab sisestada partii- ja seerianumbreid, kui need märgitakse töökaardi vahendil lõpetatuks

### <a name="configure-products-that-require-batch-number-reporting"></a>Partiinumbri kinnitamist nõudvate toodete konfigureerimine

Kõiki saadaolevaid partiiga juhitud stsenaariumide toetamiseks toodetel toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige konfigureeritav toode.
1. Valige kiirkaardil **Varude haldus** väljal **Partiinumbri grupp** jälgimisnumbri grupp, mis on seadistatud teie stsenaariumi toetamiseks.

> [!NOTE]
> Kui partii juhitud tootele ei määrata partiinumbri gruppi, siis võimaldab töökaardi seade vaikesättena sisestada partiinumbri lõpetamisest teatamise ajal käsitsi.

Järgnevates jaotistes kirjeldatakse, kuidas seadistada jälgimisnumbri gruppe, mis toetaks igat partiikaupade aruandlusega seotud stsenaariumit.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Jälgimisnumbri grupi seadistamine, mis võimaldab töötajatel partiinumbri käsitsi määrata

Käsitsi määratud partiinumbrite lubamiseks seadistage jälgimisgrupi number, toimides järgmiselt.

1. Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.
1. Looge või valige seadistamiseks jälgimisnumbri grupp.
1. Seadke kiirkaardil **Üldine** suvandi **Käsitsi** väärtuseks **Jah**.

    ![Jälgimisnumbri grupp käsitsi sisestatud partiinumbrite korral.](media/tracking-number-group-manual.png "Jälgimisnumbri grupp käsitsi sisestatud partiinumbrite korral")

1. Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete partiinumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.

Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Partiinumber** tekstikast, kus töötajad saavad sisestada mis tahes väärtuse.

![Edenemisest teatamise leht koos käsitsi sisestatavate partiinumbrite väljaga.](media/job-card-device-batch-manual.png "Edenemisest teatamise leht koos käsitsi sisestatavate partiinumbrite väljaga")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Eelmääratletud partiinumbrite loetelu esitava jälgimisnumbri grupi seadistamine

Eelmääratletud partiinumbrite loetelu esitamiseks seadistage jälgimisgrupi number, toimides järgmiselt.

1. Avage **Varude haldus \> Seadistamine > Dimensioonid \> Jälgimisnumbri grupid**.
1. Looge või valige seadistamiseks jälgimisnumbri grupp.
1. Seadke kiirkaardil **Üldine** suvandi **Ainult laokannetele** väärtuseks **Jah**.
1. Partiinumbrite koguse kaupa eraldamiseks sisestatud väärtuse alusel kasutage välja **Koguse kohta**. Näiteks on teil kümne tüki tootmistellimus ja välja **Koguse kohta** väärtuseks on seatud *2*. Sellisel juhul määratakse tootmistellimusele loomisel viis partiinumbrit.

    ![Jälgimisnumbri grupp eeldefineeritud partiinumbrite korral.](media/tracking-number-group-predefined.png "Jälgimisnumbri grupp eeldefineeritud partiinumbrite korral")

1. Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete partiinumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.

Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Partiinumber** ripploend, kus töötajad peavad valima eelmääratletud väärtuse.

![Edenemisest teatamise leht koos eelmääratletud partiinumbrite loeteluga.](media/job-card-device-batch-predefined.png "Edenemisest teadaandmise leht koos eelmääratletud partiinumbrite loeteluga")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Automaatselt partiinumbreid määrava jälgimisnumbri grupi seadistamine

Kui partiinumbrid tuleks määrata automaatselt ja töötaja sisendita, siis toimige jälgimisnumbri grupi seadistamisel järgmiselt.

1. Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.
1. Looge või valige seadistamiseks jälgimisnumbri grupp.
1. Seadke kiirkaardil **Üldine** suvandi **Ainult laokannetele** väärtuseks **Ei**.
1. Seadistage suvandi **Käsitsi** väärtuseks **Ei**.

    ![Jälgimisnumbri grupp fikseeritud partiinumbrite korral.](media/tracking-number-group-fixed.png "Jälgimisnumbri grupp fikseeritud partiinumbrite korral")

1. Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete partiinumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.

Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Partiinumber** väärtus, kuid töötajad ei saa seda muuta.

![Edenemisest teatamise leht koos kindlaks määratud partiinumbriga.](media/job-card-device-batch-fixed.png "Edenemisest teatamise leht koos kindlaks määratud partiinumbriga")

## <a name="report-serial-controlled-items-as-finished"></a>Seeria kaudu juhitud kaupade lõpetatuna teatamine

Töökaardi seade toetab seeria kaudu juhitud kaupade aruandluse osas kolme stsenaariumit. Need stsenaariumid kehtivad nii kaupadele, mis on lubatud täpsemate laoprotsesside jaoks, kui ka kaupadele, mis ei ole täpsemate laoprotsesside jaoks lubatud.

- **Käsitsi määratud seerianumbrid** — töötajad sisestavad kohandatud seerianumbri. Seerianumber võib tuleneda välisallikast, mis ei ole süsteemile teada.
- **Eelmääratletud seerianumbrid** — töötajad valivad seerianumbri seerianumbrite loetelust, mille süsteem on enne tootmistellimuse töökaardi seadmele väljastamist automaatselt loonud.
- **Kindlaks määratud seerianumbrid** — töötajad ei sisesta ega vali seerianumbrit. Selle asemel määrab süsteem tootmistellimusele enne väljastamist automaatselt seerianumbri.

### <a name="enable-the-feature-on-your-system"></a>Funktsiooni lubamine teie süsteemis

Selleks, et lubada töökaardi seadmel aktsepteerida lõpetatuna kinnitamise ajal seerianumbrit, peate kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada sisse järgmised funktsioonid (samas järjekorras).

1. Töökaardi vahendi aruande edenemise dialoogi täiustatud kasutuskogemus
1. Võimaldab sisestada partii- ja seerianumbreid, kui need märgitakse töökaardi vahendil lõpetatuks

### <a name="configure-products-that-require-serial-number-reporting"></a>Seerianumbri kinnitamist nõudvate toodete konfigureerimine

Kõiki saadaolevaid seeriaga juhitud stsenaariumide toetamiseks toodetel toimige järgmiselt.

Iga stsenaariumi lubamiseks toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige konfigureeritav toode.
1. Valige kiirkaardil **Varude haldus** väljal **Seerianumbri grupp** jälgimisnumbri grupp, mis on seadistatud teie stsenaariumi toetamiseks.

> [!NOTE]
> Kui seeriaga juhitud tootele ei määrata seerianumbri gruppi, siis võimaldab töökaardi seade vaikesättena sisestada seerianumbri lõpetamisest teatamise ajal käsitsi.

Järgnevates jaotistes kirjeldatakse, kuidas seadistada jälgimisnumbri gruppe, mis toetaks igat seeria kaupu juhitud kaupade aruandlusega seotud stsenaariumit.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Jälgimisnumbri grupi seadistamine, mis võimaldab töötajatel seerianumbri käsitsi määrata

Käsitsi määratud seerianumbrite lubamiseks seadistage jälgimisgrupi number, toimides järgmiselt.

1. Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.
1. Looge või valige seadistamiseks jälgimisnumbri grupp.
1. Seadke kiirkaardil **Üldine** suvandi **Käsitsi** väärtuseks **Jah**.

    ![Jälgimisnumbrite gruppide leht, seerianumbrid.](media/tracking-number-group-manual-serial.png "Jälgimisnumbrite gruppide leht, seerianumbrid")

1. Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete seerianumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.

Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Seerianumber** tekstikast, kus töötajad saavad sisestada mis tahes seerianumbri väärtuse. Väärtuse sisestamisel lisatakse see seerianumbrite loendisse. Loendiga saavad töötajad teha järgmist.

- Seerianumbri praagina märkimiseks valige nupp **Praak** vastavas reas. Töötajal palutakse esitada **Tõrke põhjus**.
- Seerianumbri kustutamiseks valige nupp **Kustuta** vastavas reas.

![Edenemisest teatamise leht koos käsitsi sisestatavate seerianumbrite väljaga.](media/job-card-device-serial-manual.png "Edenemisest teatamise leht koos käsitsi sisestatavate seerianumbrite väljaga")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Eelmääratletud seerianumbrite loetelu esitava jälgimisnumbri grupi seadistamine

Eelmääratletud seerianumbrite loetelu esitamiseks seadistage jälgimisgrupi number, toimides järgmiselt.

1. Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.
1. Looge või valige seadistamiseks jälgimisnumbri grupp.
1. Seadke kiirkaardil **Üldine** suvandi **Ainult laokannetele** väärtuseks **Jah**.
1. Kasutage välja **Koguse kohta** seerianumbrite lõikamiseks ühe kogus kohta.

    ![Jälgimisnumbri grupp eeldefineeritud seerianumbrite korral.](media/tracking-number-group-predefined-sn.png "Jälgimisnumbri grupp eeldefineeritud seerianumbrite korral")

1. Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete seerianumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.

Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Seerianumber** ripploend, kus töötajad peavad valima eelmääratletud väärtuse.

![Edenemisest teatamise leht koos eelmääratletud seerianumbrite loeteluga.](media/job-card-device-serial-predefined.png "Edenemisest teatamise leht koos eelmääratletud seerianumbrite loeteluga")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Automaatselt seerianumbreid määrava jälgimisnumbri grupi seadistamine

Kui seerianumber tuleks määrata automaatselt ja töötaja sisendita, siis toimige jälgimisnumbri grupi seadistamisel järgmiselt.

1. Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.
1. Looge või valige seadistamiseks jälgimisnumbri grupp.
1. Seadke kiirkaardil **Üldine** suvandi **Ainult laokannetele** väärtuseks **Ei**.
1. Seadistage suvandi **Käsitsi** väärtuseks **Ei**.

    ![Jälgimisnumbri grupp fikseeritud seerianumbrite korral.](media/tracking-number-group-fixed-sn.png "Jälgimisnumbri grupp kindlaks määratud seerianumbrite korral")

1. Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete seerianumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.

Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Seerianumber** väärtus, kuid töötajad ei saa seda muuta. See stsenaarium on oluline ainult siis, kui tootmistellimus luuakse ühe seerianumbriga juhitud kauba koguse kohta.

![Edenemisest teatamise leht koos kindlaks määratud seerianumbriga.](media/job-card-device-serial-fixed.png "Edenemisest teatamise leht koos kindlaks määratud seerianumbritega")

## <a name="report-as-finished-to-a-license-plate"></a>Lõpetatuna kinnitamine litsentsiplaadil

Täpsemad laoprotsessid rakendavad lao asukohtades varude jälgimiseks vastaval otstarbel seadistatud litsentsiplaadi dimensiooni. Sellisel juhul nõutakse töötajalt koguste lõpetamisest teatamisel identifitseerimisnumbrit.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Litsentsiplaadi aruandluse ja sildi printimise lubamine

Antud jaotises kirjeldatud funktsioonide kasutamiseks peate kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada sisse järgmised funktsioonid (samas järjekorras).

1. Töökaardi seadmesse lisatud litsentsiplaat lõpetatuna teatamiseks (tarneahela halduse versiooniga 10.0.21 lülitatakse see funktsioon vaikimisi sisse.)
1. Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis
1. Sildi printimine töökaardi vahendilt

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Litsentsiplaadile lõpetamisest teatamise seadistamine

Selleks, et kontrollida, kas töötajad peaksid koguste lõpetamisest teatamisel kasutama olemasolevat litsentsiplaati või looma uue litsentsiplaadi, toimige järgmiselt.

1. Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Töökaardi konfigureerimine seadmetele**.
2. Määrake igale seadmele järgmised valikud.

    - **Loo litsentsiplaat** – seadke suvandi väärtuseks **Jah**, et luua iga lõpetamisest teatamise korral uus litsentsiplaat. Seadke väärtuseks **Ei**, kui iga lõpetamisest kinnitamise korral tuleks kasutada olemasolevat litsentsiplaati.
    - **Prindi silt** – seadke suvandi väärtuseks **Jah**, kui töötaja peab printima iga lõpetamisest kinnitamise jaoks litsentsiplaadi sildi. Kui silti pole vaja, siis seadke väärtuseks **Ei**. 

![Töökaardi konfigureerimine seadmete lehe jaoks.](media/config-job-card-raf.png "Töökaardi konfigureerimine seadmete lehe jaoks")

> [!NOTE]
> Sildi konfigureerimiseks avage **Laohaldus \> Seadistus \> Dokumendi marsruudivalik \> Dokumendi marsruudivalik**. Lisateavet vt teemast [Litsentsiplaadi printimise lubamine](../warehousing/tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]