---
title: Eelarve juhtimise ülevaade
description: See artikkel tutvustab eelarve juhtimise funktsiooni ja annab teavet, mis aitab teil konfigureerida eelarve juhtimist, et optimeerida teie organisatsiooni finantsressursside haldamist.
author: panolte
ms.date: 03/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27eb31919937e7f43a785616b547e3d6952eaaf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898294"
---
# <a name="budget-control-overview"></a>Eelarve juhtimise ülevaade

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel tutvustab eelarve juhtimise funktsiooni ja annab teavet, mis aitab teil konfigureerida eelarve juhtimist, et optimeerida teie organisatsiooni finantsressursside haldamist.

Eelarve juhtimine toetab organisatsiooni finantsressursside haldamist kontoplaani, töövoogude, kasutajagruppide, lähtedokumentide ja töölehtede, saadaoleva raha konfigureeritava arvutamise, eelarvetsüklite ja lävede kaudu. Rakendatud juhtimisega saab organisatsioon plaanida, mõõta, hallata ja prognoosida oma rahalisi vahendeid kogu rahandusaasta jooksul. 

Pärast eelarve heakskiitmist süsteemis saate kasutada eelarveplaane, et luua eelarve registrikandeid organisatsiooni kulude eelarve salvestamiseks. Teise võimalusena saate luua või importida eelarve registrikandeid kolmanda osapoole programmist, selle asemel, et kasutada eelarve planeerimise funktsiooni. 

Kulusid saab salvestada põhikontode ja finantsdimensioonide abil. Saate konfigureerida kogukulude juhtimist vastavalt organisatsiooni poliitikatele ja nõuetele, grupeerides finantsdimensioonide ja põhikontode kombinatsioone. 

Järgmisel skeemil näidatakse eelarve juhtimist tüüpilise eelarvetsükli etappides.

[![Tüüpiline eelarvetsükkel.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Saate konfigureerida eelarve juhtimist erinevate tegurite alusel.

- **Finantsdimensioonid** – milliseid finantsdimensioone tuleb kasutada eelarve ja tegelike summade aruandluseks ning milliseid finantsdimensioone on vaja eelarvete juhtimiseks? Kas konkreetsed dimensioonikombinatsioonid või põhikontod vajavad erilist tähelepanu? Näiteks kas eelarve jälgimine tegelike summadega on kulukeskuse ja programmiga nõutav? Kas reisikulud vajavad erilist tähelepanu?
- **Aeg** – millist ajavahemikku (rahandusperiood, rahandusperiood kuupäevani jne) kasutatakse saadaolevate eelarvefondide hindamiseks?
- **Lähtedokumendid** – milliseid lähtedokumente tuleb hinnata eelarve juhtimise puhul? Kas dokumente tuleks hinnata rea või dokumendi kohta?
- **Saadaolevate vahendite arvutus** – kas dokumentidega, nagu ostutaotlused (eelpandiõigused) ja ostutellimused (pandiõigused), tuleb saadaolevate vahendite arvutamisel arvestada? Kas mustandi olekus dokumente tuleb arvutamisel arvestada?
- **Tühistamise luba** – kellel on õigus saadaolevat eelarvet ületada?

Eelarve juhtimine on täielikult integreeritud rakendusega. Seetõttu saate hinnata saadaolevat eelarvet nii plaanitud kui ka tegelike ostude puhul. Saadaval on eelarve päringud ja aruanded. Seega saavad kasutajad eelarvet hinnata ja teha kõiki nõutavaid korrigeerimisi kogu eelarvetsükli jooksul eelarverevisjonide või ülekannete kujul. Eelarvehaldur saab eelarve ja tegelikud kulud ka Microsoft Excelisse eksportida, et vajaduse korral paremini analüüsida ning prognoosida.

## <a name="configuring-budget-control"></a>Eelarve juhtimise konfigureerimine

### <a name="budget-cycle-time-span"></a>Eelarvetsükli periood

Pärast põhilise eelarvestamise konfigureerimist saate määratleda eelarvestamise ja eelarve juhtimise aja või algus- ja lõpp-perioodid lehel **Eelarvetsükli periood**. Eelarvetsüklid vastavad sageli rahanduskalendritele, kuid võivad ulatuda rahandusaastateni.

Järgmised konfigureerimise etapid viiakse lõpule lehe avatud **Eelarve juhtimise konfiguratsioon** vahekaartidel.

### <a name="define-parameters"></a>Parameetrite määratlemine

Eelarve puhul lubatud finantsdimensioonide põhjal saate eelarve juhtimiseks kasutada kõiki või alamkogumi finantsdimensioone. 

Lisaks saate määrata vaikeajaintervalli (nt **Rahandusaasta**, **Rahandusaasta kuupäevani**, **Rahandusperiood** või **Kord kvartalis**), mille järel eelarve kontrolli teostatakse seotud eelarve ajavahemiku jooksul. Samuti saate määrata vaikimisi eelarvehalduri ja lävi, mida kasutatakse kasutajate teavitamiseks, kui lävi on saavutatud. Nende väljade väärtusi kasutatakse vaikeväärtusetan uue eelarve juhtimise reegli või eelarvegrupi loomisel. Siiski saab vaikeväärtusi üksikute gruppide või reeglite puhul muuta. 

Eelarvete loomise ja eelarveregistrisse kirjendamise viis on abiks saadaolevate eelarvevahendite hindamisel valitavate ajavahemike määramisel. Dimensiooniväärtuse kombinatsiooni aastapõhise summa välja töötamisel ja kasutamisel võib olla mõistlik kasutada rahandusaasta või rahandusaasta kuupäevani lähenemist. Kui organisatsioon loob eelarveid rahandusperioodi järgi või eraldab need rahandusperioodideks ja soovib üksikasjalikumat juhtimist, võidakse kaaluda ajavahemikke rahandusperiood kuupäevani või kord kvartalis. 

Lisaks aitab eelarvestamise ja eelarve juhtimisega seotud ettevõtte kultuur konfiguratsiooni määratleda.

### <a name="over-budget-permissions"></a>Eelarve ületamise load

Vahekaardil **Eelarve ületamise load** saate määrata kasutajagrupid. Samuti saate määrata, kas grupi liikeks olevatel kasutajatel on luba eelarvet ületada. Saate takistada lehel **Eelarve parameetrid** kasutajatele määratud eelarveläve ületamist või saate takistada eelarve ületamist mis tahes summa võrra, olenemata lävest. Olenevalt sellest, kui aktiivselt organisatsioon oma kulusid haldab, aitavad need load rahalisi vahendeid hallata. 

### <a name="budget-funds-available"></a>Saadaolevad eelarvefondid

Vahekaardil **Saadaolevad eelarvefondid** saate määratleda saadaolevate eelarvefondide arvutamiseks kasutatava valemi. Olenevalt sellest, kui konservatiivselt organisatsioon oma rahalisi vahendeid haldab või olenevalt eeskirjadest või valdkonna nõuetest võidakse arvutamisse kaasata mustand või sisestamata dokumendid. 

> [!NOTE]
> Kui kalkulatsiooni on eelarvetsükli jooksul muudetud, ei mõjuta muudatused ühtegi dokumenti, mis on eelnevalt läbinud eelarvekontrolli kontrollid ja need sisestati või lõpetati. Funktsioon, mille nimi on Ainult **jälgige** summasid saadaolevas eelarvefondide arvutuses, võimaldab teil muuta, milliseid andmeid BudgetSourceTracking tabelites jälgitakse. Kui see funktsioon on sisse lülitatud, talletatakse summad ainult siis, kui need on valitud kasutamiseks saadaoleva eelarvefondide arvutamisel. Lisateavet vt saadaolevad [eelarvefondid](budget-funds-available.md).

### <a name="documents-and-journals"></a>Dokumendid ja töölehed

**Vahekaardil Dokumendid ja töölehed** saate valida, millised lähtedokumendid ja töölehed kuuluvad eelarve juhtimise kontrolli alla, ning kas tšekid toimuvad rea kirje või kogu dokumendi tasemel. Lisaks sisaldab uus eelarve juhtimise dokumendi filtreerimise täiustusfunktsioon, **·** Microsoft Dynamics mis on saadaval alates 365 Finantsversioonist 10.0.27, iga eelarve juhtimisse kaasatud dokumendi päringupõhise filtri valiku. Seetõttu saate määrata eelarve juhtimise dokumentide eelarvekontrolli. Sel viisil võimaldab see funktsioon eelarvet kontrollida vaid dokumenditüübi alamkogumit. Näiteks saate kontrollida ainult ostutellimusi, mille välja **Pool väärtuseks** on seatud **01**. Vahekaardile Dokumendid ja töölehed lisatud **uus veerg näitab**, kas valitud dokumenditüübi jaoks on päring määratletud. Lisaks sellele saate lisada kaks uut nuppe, mis on lisatud tööriistaribale dokumendi ruudustiku kohal, lisada, redigeerida või kustutada filtreerimist. 

Peate valitud lähtedokumendid viima vastavusse saadaolevate eelarvevahendite arvutusse kaasatud saldode märkeruutudega. Näiteks kui valisite **Pandiõiguste eelarve reserveerimised**, peaksite valima suvandi **Ostutellimused**. Kui eelarvekontroll tehakse osturea summade ja kontode kohta, on reserveeringule määratud eelarve juhtimise kategooriaks **Pandiõigus**. Kui eelarvekontroll tehakse ostutaotluse summade ja kontode kohta, on reserveeringule määratud eelarve juhtimise kategooriaks **Eelpandiõigus**. 

Kui saadaolevate eelarvefondide arvutusse on kaasatud **Pandiõiguse eelarve reserveerimised** ja/või **Eelpandiõiguse eelarve reserveerimised** ning neid tuleb kajastada pearaamatu sisestuste kaudu, peab **kohustuste raamatupidamisarvestuse** grupi valikud olema lehel **Pearaamatu parameetrid** lubatud.

### <a name="assign-budget-models"></a>Eelarvemudelite määramine

Vahekaardil **Eelarvemudelite määramine** saate määrata eelarvemudelid eelarve juhtimisse kaasatavatele eelarvetsükli perioodidele.

### <a name="define-budget-control-rules"></a>Eelarve juhtimise reeglite määratlemine

Vahekaardil **Eelarve juhtimise reeglite määratlemine** peate looma konkreetsed reeglid eelarve juhtimisel lubatud finantsdimensioonide alusel. Näiteks kui fookus on osakonna kulul või kulude vahemikul, saab neid kulusid määratleda ja hinnata sellel vahekaardil olevate sätetega. Iga eelarve juhtimise reegli puhul saab määratleda eri lävesid. 

> [!Important]
> Eelarve juhtimine lubatakse põhukonto tüüpide **Kasum ja kahjum**, **Kulu**, **Tulu, Bilanss, Kohustused, Omakapital** või **Vara** puhul. Kui **Määra eelarve kontrollireeglid** vahekaart sisaldab reeglit, millel on tühi kriteerium, lubatakse eelarve juhtimine **kõikide** finantsdimensioonide puhul, mis hülmavad seda tüüpi põhikontosid. Seetõttu looge kindlasti eelarve juhtimise reeglid, mis määratlevad ainult finantsdimensiooni kombinatsioonide vahemikud, kus eelarve juhtimise sisselülitamine on oluline.

### <a name="select-main-accounts"></a>Põhikontode valimine

Kui **Põhikonto** ei ole lehel **Parameetrite määratlemine** valitud eelarvekontrolli dimensiooniks, kuid hallatakse kindlaid kulusid, saate need kulud valida vahekaardil **Põhikontode valimine**. Kui **Põhikonto** valitakse eelarvekontrolli dimensioonina, siis kirjeid ei nõuta.

### <a name="define-budget-groups"></a>Eelarvegruppide määratlemine

Vahekaardil **Eelarvegruppide määratlemine** saate valikuliselt määratleda kordumatud finantsdimensioonide kombinatsioonid, kuhu eelarvevahendid teiseseks eelarve kontrollimiseks koondatakse. Saate luua ühe kirje, mis sisaldab kogu organisatsiooni või mitu gruppi üksikute osakondade või kulukeskuste tähistamiseks.

### <a name="define-message-levels"></a>Määratle teatetasemed

Kui eelarvejuhtimise hoiatusteateid tuleb mõne kasutajagrupi puhul tõkestada, saate määrata need grupid lehel **Teatetasemete määratlemine**. Kasutajagruppide liikmed saavad jätkuvalt tõrketeateid, kui nad ületavad saadaolevaid eelarvefonde nende eelarve ületamise lubade põhjal.

### <a name="activate-budget-control"></a>Eelarve juhtimise aktiveerimine

Pärast seda, kui eelarve juhtimine on konfigureeritud, saate selle sisse lülitada ja aktiveerida vahekaardil **Eelarve juhtimise aktiveerimine**. Seejärel jõustub mustandversioon.

> [!Important]
> Kui eelarve juhtimine on sisse lülitatud ja aktiivne ning kanded on sisestatud, ei tohi seda aasta keskel välja lülitada. Kui eelarve juhtimine on välja lülitatud, siis tegevusi eelave juhtimise eesmärkidel ei salvestata ja eelarvet enam ei kontrollita. Seetõttu ei pruugi juba sisestatud dokumendid õigesti kajastada eelave juhtimisega seotud päringutes ja aruanntes olevaid vabastatavaid summasid või saldosid. See hõlmab eelarve juhtimise statistikat allavoolu kohta või dokumentide ja töölehtede korrigeerimist. 

Pange tähele ka seda, et enne eelarve juhtimise sisselülitamist sisestatud kandeid, sh eelarveregistri kandeid, eelarve juhtimises ei arvestata. Seetõttu tasub eelarve juhtimine sisse lülitada ainult uue eelarvetsükli alguses. Veenduge, et eelarve juhtimise puhul eelarve algsaldosid sisaldavate eelarve registrikannete eelarvesaldosid värskendataks ainult siis, kui eelarve juhtimine on sisse lülitatud. Mis tahes avatud dokumenti (nt ostutellimust) kontrollitakse saadaolevate eelarvevahendite osas ja see saab eelarve juhtimise puhul eelarve reservatsiooni, kui kasutaja käivitab dokumendis käsitsi eelarve juhtimise kontrolli.

## <a name="using-budget-control"></a>Eelarve juhtimise kasutamine
Kui eelarve juhtimine on sisse lülitatud, saate eelarve juhtimise osas konfigureeritud dokumentides ja töölehtedes hoiatus- ja tõrketeateid. Pidage meeles, et saate konfigureerida eelarve juhtimist nii, et kasutajaid hoiatatakse, kui nad ületavad eelarvefonde, kuid saavad siiski kandeid kinnitada või sisestada. Saate vaadata nurjunud eelarve kontrollide üksikasju lehel **Eelarve juhtimise tõrked ja hoiatused**.

Sellelt lehelt saavad kasutajad minna süvitsi lehele **Eelarve juhtimise statistika perioodide kaupa**, et vaadata eelarve saadavaloleku üksikasju ja valitud eelarve juhtimise dimensiooni kombinatsiooni reserveerimisi. Kasutajad saavad süveneda ka lehele **Eelarve juhtimise statistika**, et vaadata kõikide eelarve juhtimisel kasutatavate finantsdimensioonide kombinatsioonide eelarve saadavalolekut. 

Kui eelarve juhtimine on ostutellimuste puhul sisse lülitatud, saab eelarvehaldur kasutada tööruumi **Pearaamatu eelarved ja prognoosid**, et vaadata üle kõikide kinnitamata ostutellimuste järjestus, millel on eelarve kontrollimise hoiatused ja tõrked. Kui eelarve halduril on eelarve ületamise load konfigureeritud, saab ostutellimused kinnitada otse tööruumis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
