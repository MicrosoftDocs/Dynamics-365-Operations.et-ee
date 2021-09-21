---
title: Parameetrid, mida Planning Optimization ei kasuta
description: Selles teemas loetletakse Planning Optimization, mida planeerimise optimeerimist praegu selle toimingu ajal ei arvestata.
author: crytt
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 52cfe5be60e5a04ce2e2239574d7fedc83e7cff0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474792"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Parameetrid, mida Planning Optimization ei kasuta

[!include [banner](../../includes/banner.md)]

Selles teemas loetletakse Planning Optimization, mida planeerimise optimeerimist praegu selle toimingu ajal ei arvestata. Planeerimisteenus võib parameetri vahele jätta, kuna näiteks seotud funktsioone veel ei toetata. Võib-olla on see parameeter funktsioonimuudatuste tõttu aegunuks muutunud.

Järgmistes jaotistes loetletakse parameetrid, mida Planning Optimization planeerimine kindlatel lehtedel ei kasuta. Samuti selgitavad nad, miks iga parameetrit ei kasutata.

## <a name="master-planning-parameters-page"></a>Koondplaneerimise parameetrite leht

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Koondplaneerimise parameetrid** lehel:

- **Üldine** vahekaart:

  - **Praegune eelarveplaan** – ootel *Eelarve* tugi.
  - **Praegune staatiline koondplaan** – ootel *kopeerimise staatilise dünaamilise plaani* tugi.
  - **Praegune dünaamiline koondplaan** – ootel *kopeerimise staatilise dünaamilise plaani* tugi.
  - **Kopeerige täielik ja uuendatud staatiline koondplaan dünaamilisse koondplaani** – ootel *kopeerimise staatilise dünaamilise plaani* tugi.
  - **Arvutatud viivituste algusaeg** – ootel *arvutatud viivituste* tugi.
  - **Kasuta dünaamilisi negatiivseid päevi** – planeerimise optimeerimine kasutab alati *dünaamiliste negatiivsete päevade* lähenemist.
  - **Tänase kuupäeva kalender** - ootel *planeerimise* tugi.
  - **Vahemälu kasutamine** – Microsoft Azure kordustellimuse konfiguratsioon käsitseb jõudluspunkte.
  - **Ülesannete arv abistaja ülesannete kogumisse** – Azure'i kordustellimuse konfiguratsioon käsitseb jõudluspunkte.
  - **Eeltöötlus: otsese nõudlusega kaupade automaatne filtreerimine** – Azure'i kordustellimuse konfiguratsioon käsitseb jõudluspunkte.
  - **Eeltöötlus: otsese nõudlusega kaupade automaatne filtreerimine** – Azure'i kordustellimuse konfiguratsioon käsitseb jõudluspunkte.
  - **Ülesannete arv abistaja ülesannete kogumisse** – Azure'i kordustellimuse konfiguratsioon käsitseb jõudluspunkte.
  - **Lõimede arv** – Azure'i kordustellimuse konfiguratsioon käsitseb jõudluspunkte.
  - **Planeerimisprotsessi aeg maha minutites** – Azure'i tellimise konfiguratsioon käsitseb jõudluspunkte.
  - **Planeerimise algusaeg** – ootel *planeerimise* tugi.

- **Plaanitud tellimuste** vahekaart:

  - **Saabumisaeg** - ootel *planeerimise* tugi.
  - **Tootmine** – ootel *planeerimise* tugi.
  - Väljad jaotises **Projekt** – ootel *planeerimise* tugi.

- **Standardi uuendus** vahekaart:

  - **Uuenda märkimine** - ootel *Kinnitamis* tugi.
  - **Peata kinnitamine, kui ilmneb tõrge** – ootel *Kinnitamise* tugi.
  - **Grupeeri hankija järgi** – ootel *Kinnitamise* tugi.
  - **Grupeeri hankija järgi** – ootel *Kinnitamise* tugi.
  - **Grupeeri ostutellimuse kinnitamise järgi** – ootel *Kinnitamise* tugi.
  - **Grupeeri perioodi järgi** – ootel *Kinnitamise* tugi.
  - **Otsi ostutellimuse kinnitus** – ootel *Kinnitamise* tugi.
  - **Grupeeri planeerimise prioriteedi järgi** – ootel *Kinnitamise* tugi.
  - **Grupeeri perioodi järgi** – ootel *Kinnitamise* tugi.

## <a name="coverage-groups-page"></a>Laovarude gruppide leht

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Katvuse grupid** lehel:

- Kiirkaart **Üldine**.

  - **Positiivsed päevad** – ootel *positiivsete päevade* tugi.
  - **Tarbi vaba kaubavaru** – vaba *kaubavaru toe ootel* tarbimine.
  - **Kasutage määratud koosluse või valemi versiooni** – ootel *valemiversioonid koos kaastoote/tootega* toega.
  - **Kasuta määratud protsessi versiooni** – ootel *nõudlus kindla koosluse või protsessi nõuete määratud* toega.

- **Tegevuse** kiirkaart:

  - **Tegevusteade** – ootel *tegevuste* tugi.
  - **Tegevusaja teade** – ootel *tegevuste* tugi.
  - **Lükka edasi marginaal** - ootel *tegevuste* tugi.
  - **Täiendatud marginaal** - ootel *tegevuste* tugi.
  - **Aluskuupäev** – ootel *tegevused* tugi.
  - **Täiendatud** - ootel *tegevuste* tugi.
  - **Lükka edasi** - ootel *tegevuste* tugi.
  - **Vähenda** - ootel *tegevuste* tugi.
  - **Suurenda** - ootel *tegevuste* tugi.
  - **Tuletatud tegevused** – ootel *tegevuste* tugi.

- **Muu** kiirkaart:

  - **Ajapiir (päevades)** – *ajapiiri külmutamist* ei plaanita plaanimise Planning Optimization`is.
  - **Koosluse koosnevusarvutuse ajapiir (päevades)** – ootel *planeerimise* tugi.
  - **Võimsuse ajastamise ajapiir (päevades)** – ootel *planeerimise* tugi.
  - **Kinnitatud taotluse ajapiir (päevades)** – ootel *taotluse* tugi.
  - **Praegune eelarveplaan** – ootel *Eelarve* tugi.

- **Viivituste** kiirkaart:

  - **Arvuta viivitus** – ootel *arvutatud viivituste* tugi.
  - **Arvutatud viivituste algusaeg** – ootel *arvutatud viivituste* tugi.

## <a name="item-coverage-page"></a>Lehel Kauba laovarud

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Katvuse grupid** lehel:

- **Üldine** vahekaart:

  - **Plaanitud tellimuse tüüp** – Planning Optimization ei toeta *kanbani* valikut, ootel *kanbani* tugi.
  - **Ajapiir (päevades)** – *ajapiiri külmutamist* ei plaanita plaanimise Planning Optimization`is.
  - **Koosluse koosnevusarvutuse ajapiir (päevades)** – ootel *planeerimise* tugi.
  - **Võimsuse ajastamise ajapiir (päevades)** – ootel *planeerimise* tugi.
  - **Kinnitatud taotluse ajapiir (päevades)** – ootel *taotluse* tugi.
  - **Täida miinimum** – Planning Optimization ei toeta *tänast kuupäeva*, *esimest välja* ja *laovarude ajapiiri* suvandeid. See kasutab alati sätet *Tänane kuupäev + tarneaeg*.
  - **Miinimumperioodid** – ootel *minimaalse kaubavaru taseme* tugi.
  - **Plaanimise valem** - ootel *valemiversioonid kaastoodete* toega.
  - **Vaikimisi prioriteet** - ootel *valemiversioonid kaastoodete* toega.
  - **Praegune prioriteet** - ootel *valemiversioonid kaastoodete* toega.
  - **Muudetud kuupäev** - ootel *valemiversioonid kaastoodete* toega.
  - **Tarbi vaba kaubavaru** – vaba *kaubavaru toe ootel* tarbimine.

- **Täitmisaeg** vahekaart:

  - **Ostuaeg** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.
  - **Ostuaeg** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.
  - **Üleviimise aeg** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.
  - **Tööpäevad** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.

## <a name="master-plans-page"></a>Koondplaanide leht

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Koondplaneerimise** lehel:

- Kiirkaart **Üldine**.

  - **Kaasa käsil olev kaubavaru** – ootel *kaubavaru inventuuri* tugi.
  - **Halda kaubavaru** – ootel *kaubavaru inventuuri* tugi.
  - **Tarbi vaba kaubavaru** – vaba *kaubavaru toe ootel* tarbimine.
  - **Kaasa varu kandeid** – ootel *kaubavaru inventuuri* tugi.
  - **Kaasa müügipakkumised** – ootel *müügipakkumiste* tugi.
  - **Kaasa hinnapakkumiste taotlused** – ootel *pakkumiste taotluse* tugi.
  - **Kasutage kõlblikkusaja kuupäevi** – ootel *kõlblikkusaja* tugi.
  - **Järjepidevusplaani kaasamine** – ootel *järjepidevuse plaanimise* tugi.
  - **Planeerimise algusaeg** – ootel *planeerimise algusaja* tugi.
  - **Piiratud atribuut** – ootel *planeerimise* tugi.
  - **Võimsuse ajastamise ajapiir** – ootel *planeerimise* tugi.
  - **Piiratud võimsus** – ootel *planeerimise* tugi.
  - **Piiratud võimsuse ajapiirang** – ootel *planeerimise* tugi.
  - **Piiratud võimsus kitsaskohana asuvatele ressurssidele** – ootel *planeerimise* tugi.
  - **Piiratud võimsus kitsaskohana asuvatele ressurssidele** – ootel *planeerimise* tugi.
  - **Plaanitud tellimused** –Planning Optimization kasutab fikseeritud numbriseeriaid.
  - **Sessioon** – Planning Optimization kasutab fikseeritud numbriseeriaid.
  - **Jätkuvusplaan** –Planning Optimization kasutab fikseeritud numbriseeriaid.

- **Ajapiirid päevades** kiirkaart:

  - **Külmuta** – *ajapiiri külmutamist* tuge ei plaanita Planning Optimization`is.
  - **Plahvatus** – ootel *planeerimise* tugi.
  - **Eelarveplaan** – ootel lisa *Eelarve* tugi.
  - **Võimsus** – ootel *planeerimise* tugi.
  - **Järjepidevusplaan** – ootel *järjepidevuse plaanimise* tugi.
  - **Tegevusteade** – ootel *tegevuste* tugi.
  - **Arvuta viivitus** – ootel lisa *arvutatud viivituste* tugi.
  - **Sagedus** – ootel *Tootmise* tugi.

- **Arvutatud viivituste** kiirkaart:

  - **Veenduge, et plaanitud tellimusi ei looda enne koondplaanimise käituskuupäeva**– ootel *arvutatud viivitused* tugi.
  - **Lisage arvutatud viivitus vajaduse kuupäevale** (jaotises **Plaanitud ostutellimused** jaotis) – ootel *arvutatud viivitused* tugi.
  - **Lisage arvutatud viivitus vajaduse kuupäevale** (jaotises **Plaanitud ostutellimused** jaotis) – ootel *arvutatud viivitused* tugi.
  - **Lisage arvutatud viivitus vajaduse kuupäevale** (jaotises **Plaanitud kanne** jaotis) – ootel *arvutatud viivitused* tugi.
  - **Lisage arvutatud viivitus vajaduse kuupäevale** (jaotises **Plaanitud kanban** jaotis) – ootel *arvutatud viivitused* tugi.

- **Sageduse** kiirkaart:

  - **Seeria plaanitud tellimused pärast** koondplaneerimist – ootel *järjestuse* tugi.
  - **Vahemike tüüp** – ootel *järjestuse* tugi.
  - **Perioodi tüüp** – ootel *järjestuse* tugi.
  - **Vahemike arv kampaaniatsüklis** – ootel *järjestuse* tugi.

## <a name="released-product-details-page"></a>Leht Väljastatud toodete üksikasjad

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Välja lastud toote detailid** lehel:

- **Insener** kiirkaart:

  - **Tootmise tüüp** – Planning Optimization ei toeta *plaanimiskauba* valikut, ootel *plaanimise kaupade* tuge.

## <a name="default-order-settings-page"></a>Tellimuse vaikesätete leht

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Vaikimisi tellimuse sätted** lehel:

- **Ostutellimuse** kiirkaart:

  - **Ostutellimuse aeg** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.
  - **Tööpäevad** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.

- **Varude** kiirkaart:

  - **Tarnekuupäeva kontroll** – planeerimise optimeerimine ei toeta *CTP* valikut, ootel *CTP* tuge.
  - **Varude juhtimise aeg** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.
  - **Tööpäevad** - Planning Optimization teenuse versioonides, mis on vanemad kui väljalase 6. august 2021, kasutab Planning Optimization seda parameetrit õige tellimuse ja tarnekuupäeva arvutamiseks, kuid see ei salvesta arvutatud täitmisaega ennast plaanitud. Hilisemates versioonides kasutab teenus ka arvutatud täitmisaega, et seadistada **täitmisaja** väli ja **tööpäevade valik** nagu on plaanitud tellimuse puhul.

## <a name="working-time-calendars-page"></a>Töögraafikute leht

Planning Optimization ei kasuta lehel järgmisi parameetreid või valikuid **Töötamise kalnedri** lehel:

- **Põhikalender** – ootel *põhikalendri* tugi.

## <a name="batch-disposition-master-page"></a>Partii likvideerimise koond leht

Planning Optimization ei kasuta lehel järgmisi parameetreid **Partii likvideerimise koond** lehel:

- **Häälestuse** kiirkaart:

  - **Tasaarveldus** – ootel *partii likvideerimiskoodid* tugi.
