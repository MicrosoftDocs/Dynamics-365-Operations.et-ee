---
title: Statistilise alusprognoosi loomine
description: Selles teemas on esitatud teave nõudluse prognoosimise arvutamisel kasutatavate parameetrite ja filtrite kohta.
author: roxanadiaconu
manager: tfehr
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db0ac2d56db46f283716df6615e404a5354f8d3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426501"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Statistilise alusprognoosi loomine

[!include [banner](../includes/banner.md)]

Selles teemas on esitatud teave nõudluse prognoosimise arvutamisel kasutatavate parameetrite ja filtrite kohta. 

Alusprognoosi loomisel tuleb teil esmalt määratleda parameetrid ja filtrid, mida kasutatakse arvutamisel. Näiteks saate luua alusprognoosi, mis prognoosib tulevase kuu valitud kaupade nõudlust kindla ettevõtte viimase aasta kandeandmete alusel. 

Nõudluse prognoosi loomiseks avage **Koondplaneerimine &gt; Prognoosimine &gt; Nõudluse prognoosimine &gt; Statistilise alusprognoosi loomine**. 

Prognoosi vahemiku saate valida prognoosi loomise ajal. Saadaval on järgmised väärtused: päev, nädal ja kuu. 

Vahemike arvu, mille jaoks prognoos luuakse, saate määrata väljal **Prognoosi periood**. 

Ajaloolise perioodi lõppu eiratakse, kui prognoosi strateegiaks on määratud **Kopeeri ajalooline nõudlus ümber**. Süsteem kopeerib väljal **Prognoosi periood** määratud vahemike arvu nõudluse prognoosi, alustades alguskuupäevast, mis on seatud jaotise **Ajalooline periood** väljal **Alguskuupäev**. Kopeerides ajaloolise nõudluse teatud kuupäevast alates, saavad tootmisplaanijad järgmist kvartalit planeerida kahel viisil:

-   kopeerides eelmise aasta sama kvartali nõudluse või
-   kopeerides eelmise kvartali nõudluse.

Tootmisplaanide segaduse vältimiseks saab teatud hulga prognoosivahemike külmutada. Selle arvu saab määrata väljal **Külmuta ajapiir**. Lehel **Korrigeeritud nõudluse prognoos** on külmutatud vahemike lahtrid keelatud, et näidata visuaalselt, et neid väärtusi ei peaks muutma. 

Nõudluse alusprognoosi alguskuupäev ei pea olema tänane kuupäev ega tulevane kuupäev. Teise alguskuupäeva määramiseks kasutage välja **Alusprognoosi alguskuupäev – alates kuupäevast**. Näiteks saavad kasutajad juunis järgmise aasta prognoosi luua. Ajaloolise nõudluse lõpu ja alusprognoosi alguse prognoosivahemike puudumise tõttu ei pruugi prognoosid täpsed olla. Nõudluse prognoosimise teenuses on lünkade täitmiseks neli võimalust. Soovitud meetodi saate valida, seades parameetri MISSING\_VALUE\_SUBSTITUTION leheküljel **Nõudluse prognoosimise parameetrid**. 

> [!NOTE]
> Puuduva väärtuse asendamine toimib ainult andmelünkades ajalooliste andmete algus- ja lõppkuupäevade vahel. See ei täida andmeid enne või pärast viimast füüsilist andmepunkti, see toimib vaid üldistusena tegelike olemasolevate andmepunktide vahel. 

Väljal **Alusprognoosi alguskuupäev** - **alates kuupäevast** peab määrama prognoosi vahemiku alguse, näiteks Ameerika Ühendriikides on nädalase prognoosivahemiku puhul alguseks pühapäev. Süsteem kohandab automaatselt välja **Alusprognoosi alguskuupäev** - **alates kuupäevast**, et olla vastavuses prognoosivahemiku algusega. 

Väljale **Alusprognoosi alguskuupäev** - **alates kuupäevast** saab määrata mineviku kuupäeva. Teisisõnu on võimalik luua nõudluse prognoosi minevikus. See on kasulik, kuna laseb kasutajatel prognoosimisteenuse parameetreid kohandada selliselt, et varem loodud statistiline prognoos vastab tegelikule ajaloolisele nõudlusele. Seejärel saavad kasutajad neid parameetri sätted tulevase statistilise alusprognoosi loomisel kasutada. 

Varasemates prognoosimise iteratsioonides käsitsi tehtud korrigeerimised saab automaatselt uuele alusprognoosile rakendada, kui ruut **Kandke käsitsi tehtud korrigeerimised üle nõudluse prognoosi** on märgitud. Kui ruut on tühi, ei lisata alusprognoosis käsitsi tehtud korrigeerimisi, kuid ei kustutata ka. Prognoosis käsitsi tehtud korrigeerimisi saab kustutada ainult prognoosi importimise ajal, tühjendades ruudu **Salvestage nõudluse alusprognoosis käsitsi tehtud korrigeerimised**. Käsitsi tehtud korrigeerimised salvestatakse autoriseerimise ajal. Seega, kui kasutaja korrigeerib prognoosi käsitsi, kuid ei autoriseeri prognoosi uuesti Supply Chain Managementis, lähevad muudatused kaotsi. Käsitsi tehtud korrigeerimiste ja nende tööpõhimõtete kohta vt lisateavet teemast [Korrigeeritud prognoosi autoriseerimine](authorize-adjusted-forecast.md). 

Nõudluse prognoosil võib olla nimi ja kommetaarid, mis aitavad kasutajatel loodud prognoosi tuvastada. Need väärtused kuvatakse prognoosi loomise ajaloos leheküljel **Statistilise alusprognoosi loomise ajalugu**. 

Prognoosi loomise ajal saab rakendada mitmesuguseid filtreid, nagu kontsernisisene plaanimisgrupp, kauba eraldamisvõtmed jt. Neid saab kasutada jõudluse parandamiseks või andmete hallatavateks tükkideks jagamiseks. Pange tähele, et nõudluse prognoosi ei looda siiski mistahes kauba eraldamisvõtme liikmetele, mis ei ole seostatud kontsernisisese plaanimisgrupiga isegi siis, kui kauba eraldamisvõti on päringus valitud. 

> [!TIP]
> Mõnikord võivad kasutajad saada nõudluse prognoosi loomise ajal tõrketeateid või lõpetatakse prognoosi loomine ühegi seansilogita. See võib juhtuda päringus allesjäänud andmete tõttu, mida varem prognoosi loomisel kasutati. Probleemi lahendamiseks klõpsake nuppu **Vali**, et avada lehekülg **Päring**, seal valige suvand **Lähtesta** ja looge seejärel alusprognoos uuesti. 

Kui prognoosi ei looda korraga suure hulga kaupade jaoks, vaid näiteks ühele kaubale või ühele kauba eraldamisvõtmele, siis parema jõudluse saavutamiseks saate valida ruudu **Kasuta taotluse vastuse režiimi** vahekaardil **Koondplaneerimine – Seadistus – Nõudluse prognoosimine** - **Nõudluse prognoosimise parameetrid – Azure’i masinõpe**.

> [!NOTE]
> Potentsiaalselt lameda väljanägemisega prognoos võib olla tingitud ajaloolistest andmetest, mis peab pärinema pikemast ajaloolisest ajavahemikust (minimaalselt 3 ajaperioodi mustrite valimiseks, nt 3 aastat kuu prognoosiga). Paremate tulemuste saamiseks võite proovida muuta ajavahemiku teralisust või suurendada ajavahemikku.

<a name="additional-resources"></a>Lisaressursid
--------

- [Nõudluse prognoosi häälestus](demand-forecasting-setup.md)

- [Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)

- [Korrigeeritud prognoosi autoriseerimine](authorize-adjusted-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]