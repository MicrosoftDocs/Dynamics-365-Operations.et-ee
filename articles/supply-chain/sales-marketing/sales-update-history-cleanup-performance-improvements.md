---
title: Müügiajaloo andmete puhastamise plaanimine
description: See artikkel kirjeldab, kuidas saate aidata parandada süsteemi jõudlust, planeerides müügi uuendamisajaloo perioodilise puhastuse ülesande regulaarseks käitamiseks korrapärase intervalliga.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335499"
---
# <a name="schedule-sales-history-data-cleanup"></a>Müügiajaloo andmete puhastamise plaanimine

[!include [banner](../includes/banner.md)]

Standardse toimingu osana loob ja talletab Dynamics 365 Supply Chain Management Microsoft müügiajaloo uuendamisandmed jooksvalt. Aja jooksul võib süsteemi akumuleerida suur hulk aegunud müügiajaloo andmeid. Need akumuleeritud andmed võivad müügitellimustega seotud dokumentide sisestamisel põhjustada jõudlust ja funktsionaalsed väljaminek. (Need dokumendid hõlmavad müügitellimuse kinnitusi, müügi saatelehti, müügi komplekteerimislehti ja arveid). Seetõttu tuleb teil seadistada ja planeerida müügi *uuenduste ajaloo puhastamine*, et käitada perioodiline ülesanne regulaarse intervalliga. See ülesanne eemaldab kõik müügiajaloo uuendusandmed, mida enam ei vajata.

Kui kasutate müügi uuendamisajaloo *perioodilist* puhastusülesannet, *soovitame* teil lubada müügiajaloo jõudluse parendusfunktsiooni, mis muudab ülesande töö tõhusamaks. (Sellest hoolimata saate ülesande käivitada ka seda funktsiooni lubamata.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Lülita müügiajaloo puhastamisfunktsioonid sisse

*Et* seadistada ja kasutada müügi värskendusajaloo perioodilist puhastusülesannet koos kõigi selles artiklis kirjeldatud funktsioonidega, *·* *peate lubama müügiajaloo puhastamisjõudluse parendused ja puhastama müügi värskendamise ajaloo, mis põhineb* funktsioonihalduse vanuse funktsioonidel, nagu kirjeldatud järgmistes alamjaotistes.

### <a name="sales-history-cleanup-performance-improvements"></a>Müügiajaloo puhastamise jõudluse täiustused

**Müügi värskenduste ajaloo puhastamise** perioodiline töö võib võtta kaua aega, kui seda käitatakse harva suure müügiuuendustega keskkondades. Sellises olukorras võib funktsioon *Müügiajaloo puhastamisjõudluse parendamine* vähendada käituskestust ja parandada usaldusväärsust.

See funktsioon parandab olemasolevat puhastustööd järgmistel viisidel:

- See tükeldab puhastuse partiideks (partii suurust saate kohandamiste kaudu muuta).
- See töötab maksimaalselt 2 tundi (kohandamiste kaudu saate kestust muuta).
- Võimaluse korral võimendatakse andmebaasi võimalusi lukustamise minimeerimiseks ja kannete tabelite ühendamise vältimiseks puhastamise ajal.

Pärast funktsiooni lubamist käitatakse partiitöö **Müügi värskendamise ajaloo puhastamine** (**Müük ja turundus \> Perioodi ülesanded \> Puhastamine \> Müügi värskendamiste ajaloo puhastamine**) nii, nagu seda enne, kuid parema jõudluse ja maksimaalselt 2 tunni jooksul. See tähendab, et teatud andmete säilitamiseks teatud ajavahemiku jooksul võib vaja minna mitut käivitamist.

Enne selle funktsiooni kasutamist tuleb see teie süsteemi jaoks sisse lülitada. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Müük ja turundus*
- **Funktsiooni nimi:** *Müügiajaloo puhastamise jõudluse täiustused*

### <a name="clean-up-sales-update-history-based-on-age"></a>Müügi värskendamise ajaloo puhastamine vanuse põhjal

Vanuse *funktsioonil põhinev müügi värskendamise* ajaloo puhastamine võimaldab *teil* määrata kirjete maksimaalse vanuse, kui käitatakse müügi värskendamise ajaloo puhastamist. Vanemad kirjed kustutatakse. See funktsioon on vajalik siis, kui seadistate ülesande perioodiliselt käivituma, kuna vanus arvutatakse alati vastavalt ülesande käituskuupäevale. Kui te seda funktsiooni ei kasuta, saate vanimatele säilitamiskirjetele seada ainult kindla kuupäeva.

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumi ajastusel põhinevat müügivärskenduste ajaloo puhastamist.

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Müügiajaloo perioodilise puhastuse ülesande häälestamine ja plaanimine

Müügiajaloo perioodilise puhastusülesande *seadistamiseks ja* plaanimiseks järgige neid samme.

1. Analüüsige oma ettevõtet, et määrata, mitu päeva algse müügitellimuse sisestusandmetest peate kinni pidama. Tavaliselt on soovitatav käivitada puhastusülesanne iga kolme kuu järel ja kuni iga kuue kuu järel.
1. Minge müügi **ja turundusperioodi \> ülesannetele \> müügi uuendamisajaloo \> puhastuse puhastamine**.
1. **Seadke dialoogiboksi Müügi värskendamise ajaloo** puhastamine kiirkaardil **Parameetrid** järgmised väljad:

    - **Puhasta** – valige puhastatav kirjetüübi määramiseks üks järgmistest väärtustest:

        - **Käivitatud**: kustutage ainult täielikult töödeldud kirjed. Kuna teil pole nende kirjete puhul edaspidist kasutamist, on see valik kõige turvalisem.
        - **Teostatud ja vigased** – kustutage nii täielikult töödeldud kirjed kui ka kirjed, kus ilmnes tõrge. See suvand on kõige sagedamini kasutatav. Te soovite ehk kontrollida ja isegi parandada vigaseid kirjeid, selle asemel et neid automaatselt puhastada. Paljud ettevõtted valivad siiski nende kirjete puhastamise ka pärast kuut, sest need pole enam selleks ajaks asjakohased.
        - **Kõik** – kustutage teostatud, vigased ja ootel kirjed. Ootel kirjed on kehtivad, kuid need ei ole veel täielikult töödeldud. Enamasti ei soovi te tõenäoliselt neid automaatselt kustutada. Mõnel juhul võite siiski valida nende automaatse kustutamise pärast teatud aja möödumist.

    - **Säilita vanusel põhinevad** kirjed – määrake, kas soovite puhastada kirjed nende vanuse alusel ülesande käivitamisel või enne fikseeritud kuupäeva loodud kirjete kustutamist. Kui planeerite puhastust korduva ülesandena, *peaksite selle suvandi seadistama väärtusele Jah*, kuna ajaline vanus arvutatakse alati ülesande käitamise kuupäeva suhtes.

        - Määrake väärtuseks Jah *,* et lubada välja **Maksimaalne vanus**. Kasutage seda välja, et määrata kirjete maksimaalne vanus iga kord, kui ülesannet käitatakse. Välja **Loodud kuni** ignoreeritakse.
        - Seadke see valik valikule *Ei,* et lubada **välja Loodud kuni**. Kasutage seda välja, et määrata kirjete vanim loomiskuupäev, mida ülesande käivitamisel säilitada. Maksimaalse **vanuse välja** ignoreeritakse.

    - **Loodud kuni** – see säte rakendub ainult siis, kui suvandi **Säilita vanusel** põhinevad kirjed väärtuseks on seatud *Ei*. Saate määrata ülesande käivitamisel säilitamiskirjete vanima loomiskuupäeva. Kirjed, mis loodi enne seda kuupäeva, kustutatakse.
    - **Maksimaalne** vanus – see säte rakendub ainult siis, kui **suvandi Säilita** vanusel põhinevad kirjed väärtuseks on seatud *Jah*. Saate määrata kirjete maksimaalse vanuse (päevades), mis tuleb iga kord ülesande käivitamisel säilitada. Vanemad kirjed kustutatakse.

1. **Määrake kiirkaardil Käivita taustal**, kuidas, millal ja kui sageli ülesannet käitatakse. Kasutage neid sätteid, et rakendada graafikut, mille määratlesid sammus 1. Väljad töötavad samuti nagu tarneahela halduses teist [tüüpi](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) pakett-tööde puhul.
1. Valige **OK**, et rakendada oma sätted ja sulgeda dialoogiboks.
