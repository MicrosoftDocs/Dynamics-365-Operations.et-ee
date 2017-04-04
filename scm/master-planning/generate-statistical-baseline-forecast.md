---
title: Luua statistilise baseline Ilmaennustus
description: "Selles artiklis on esitatud teave nõudluse prognoosimise arvutamisel kasutatavate parameetrite ja filtrite kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Luua statistilise baseline Ilmaennustus

Selles artiklis on esitatud teave nõudluse prognoosimise arvutamisel kasutatavate parameetrite ja filtrite kohta. 

Alusprognoosi loomisel tuleb teil esmalt määratleda parameetrid ja filtrid, mida kasutatakse arvutamisel. Näiteks saate luua alusprognoosi, mis prognoosib tulevase kuu valitud kaupade nõudlust kindla ettevõtte viimase aasta kandeandmete alusel. 

Kaasa tuua nõudluse, Ilmaennustus, minge **kapten planeerimine &gt;Eelarvestus &gt;nõudluse prognoosimise &gt;Loo statistilise uuringu Ilmaennustus**. 

Prognoosi vahemiku saate valida prognoosi loomise ajal. Saadaval on järgmised väärtused: päev, nädal ja kuu. 

Vahemike arvu, mille jaoks prognoos luuakse, saate määrata väljal** Prognoosi periood**. 

Ajaloolise perioodi lõppu eiratakse, kui prognoosi strateegiaks on määratud **Kopeeri ajalooline nõudlus ümber**. Kopeerib ämbrid nimetatud arv on **ilm horizon** välja nõudluse prognoos, sätestatud kuupäevast alates on **alates** alusel välja **ajaloolise horizon**. Kopeerides ajaloolise nõudluse teatud kuupäevast alates, saavad tootmisplaanijad järgmist kvartalit planeerida kahel viisil:

-   kopeerides eelmise aasta sama kvartali nõudluse või
-   kopeerides eelmise kvartali nõudluse.

Tootmisplaanide segaduse vältimiseks saab teatud hulga prognoosivahemike külmutada. Selle arvu saab määrata väljal **Külmuta ajapiir**. Lehel **Korrigeeritud nõudluse prognoos **on külmutatud vahemike lahtrid keelatud, et näidata visuaalselt, et neid väärtusi ei peaks muutma. 

Nõudluse alusprognoosi alguskuupäev ei pea olema tänane kuupäev ega tulevane kuupäev. Teise alguskuupäeva määramiseks kasutage välja **Alusprognoosi alguskuupäev – alates kuupäevast**. Näiteks saavad kasutajad juunis järgmise aasta prognoosi luua. Ajaloolise nõudluse lõpu ja alusprognoosi alguse prognoosivahemike puudumise tõttu ei pruugi prognoosid täpsed olla. Kui kasutate Microsoft Dynamics 365 toimingute nõudluse prognoosimise teenus, selleks on neli võimalust, kus saate täita puuduvad lüngad. Meetodit, mida on kadunud seadmisega saate\_VÄÄRTUST\_asendamise parameeter on **nõudluse prognoosimise parameetrid** lehel. 

Selle **ravi prognoos alguskuupäev** - **alates** väli peab olema prognoositav kopp, nt alguses Ameerika Ühendriikides, kui prognoosimise kopp on nädala pühapäeval. Süsteem reguleerib automaatselt ning **ravi prognoos alguskuupäev** - **alates** sobitada prognoositav kopp alguses välja. 

Selle **ravi prognoos alguskuupäev** - **alates** väärtuseks saab kätte varem. Teisisõnu on võimalik luua nõudluse prognoosi minevikus. See on kasulik, kuna võimaldab kasutajatel prognoosimisteenuse parameetreid kohandada selliselt, et varem loodud statistiline prognoos vastab tegelikule ajaloolisele nõudlusele. Seejärel saavad kasutajad neid parameetri sätted tulevase statistilise alusprognoosi loomisel kasutada. 

Varasemates prognoosimise iteratsioonides käsitsi tehtud korrigeerimised saab automaatselt uuele alusprognoosile rakendada, kui ruut **Kandke käsitsi tehtud korrigeerimised üle nõudluse prognoosi** on märgitud. Kui ruut on tühi, ei lisata alusprognoosis käsitsi tehtud korrigeerimisi, kuid ei kustutata ka. Prognoosis käsitsi tehtud korrigeerimisi saab kustutada ainult prognoosi importimise ajal, tühjendades ruudu **Salvestage nõudluse alusprognoosis käsitsi tehtud korrigeerimised **. Käsitsi tehtud korrigeerimised salvestatakse autoriseerimise ajal. Seega, kui kasutaja teeb eelarvesse käsitsi muudatusi, kuid ei luba tagasi, et Dynamics 365 operatsioonide ilm, lähevad muudatused kaotsi. Käsitsi muudatusi ja kuidas need töötavad kohta lisateabe saamiseks vaadake [korrigeeritud prognoos lubab](authorize-adjusted-forecast.md). 

Nõudluse prognoosil võib olla nimi ja kommetaarid, mis aitavad kasutajatel loodud prognoosi tuvastada. Need väärtused kuvatakse prognoosi loomise ajaloos leheküljel **Statistilise alusprognoosi loomise ajalugu**. 

Prognoosi loomise ajal saab rakendada mitmesuguseid filtreid, nagu kontsernisisene plaanimisgrupp, kauba eraldamisvõtmed jt. Neid saab kasutada jõudluse parandamiseks või andmete hallatavateks tükkideks jagamiseks. Pange tähele, et nõudluse prognoosi ei looda siiski mistahes kauba eraldamisvõtme liikmetele, mis ei ole seostatud kontsernisisese plaanimisgrupiga isegi siis, kui kauba eraldamisvõti on päringus valitud. 

**Näpunäide**: mõnikord võivad kasutajad saada nõudluse prognoosi loomise ajal tõrketeateid või lõpetatakse prognoosi loomine ühegi seansilogita. See võib juhtuda päringus allesjäänud andmete tõttu, mida varem prognoosi loomisel kasutati. Probleemi lahendamiseks klõpsake nuppu **Vali**, et avada lehekülg **Päring**, seal klõpsake nuppu **Lähtesta** ning looge seejärel alusprognoos uuesti. 

Kui prognoos on loodud suur hulk kaupu, vaid, nt ühe üksuse või ühe kauba korraga, siis parema tulemuse saamiseks valige selle **režiimi kasutamine taotluse vastus** ruut selle **kapten planeerimise - Setup - nõudluse prognoosimise** - **nõudluse prognoosimise parameetrid - Azure'i masinõppe** vahekaart.

<a name="see-also"></a>Vt ka
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


