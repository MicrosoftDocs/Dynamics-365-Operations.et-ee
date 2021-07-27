---
title: Tagasimaksehalduse mooduli ülevaade
description: Selles teemas antakse ülevaade Microsoft Dynamics 365 Supply Chain Management tagasimakse haldusmoodulist.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 577d48e207c8ce5911d104e657101a8557100064
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339990"
---
# <a name="rebate-management-module-overview"></a>Tagasimaksehalduse mooduli ülevaade

[!include [banner](../includes/banner.md)]

Saate kasutada **tagasimakse halduse** moodulit, et luua oma ettevõtte ja selle klientide või müüjate vahelisi lepinguid, tehinguid või kokkuleppeid, nii et saate arvutada tagasimakseid, mahaarvamisi ja autoritasusid. Tagasimaksehaldus jälgib ja haldab tagasimakse- ja mahaarvamiskandeid keskses asukohas, kus kasutajad saavad neid efektiivselt luua, läbi vaadata ja töödelda.

Tagasimaksehaldus toetab *tagasimaksete* loomist, hooldust ja töötlemist. Tagasimakse on ostuhinna osa tagastamine müüjale või ostjale. Tagasimaksed põhinevad tavaliselt kindla koguse või väärtuse ostmisel kindlal perioodil. Erinevalt allahindlustest tehakse tagasimaksed pärast ostusumma täielikku arveldamist.

Tagasimaksehaldus toetab ka *mahaarvamisi*. Mahaarvamine on hüvitis, arvestus või tasu, mida makstakse intellektuaalomandi, näiteks kaubamärgi, autoriõiguse või patendi kasutamise litsentsi või privileegi eest või privileegi eest kasutada loodusvarasid nagu näiteks kalapüük, jahindus või kaevandamine. Mahaarvamised arvutatakse tavaliselt protsendina realiseeritud kasutamisest saadud tulust või kasumist. Mida rohkem intellektuaalset vara või loodusvara kasutatakse, seda suurem on realiseeritud mahaarvamine.

Lisaks toetab tagasimaksehaldus kliendi *litsentsitasusid*. Autoritasud on maksed, mida üks osapool maksab litsentsisaajale või frantsiisivõtjale vara kasutamise õiguse eest.

Tagasimaksehaldus võimaldab teil määratleda sätete, tagasimaksete ja mahakandmisreeglite sisestusprofiile. Sisestusi saab määratleda ka kindla kliendi või müüja kohta. Sel viisil saab sisestuste kaudu jälgida tehinguid, mis ei kehti kõigile kliendi või müüja stsenaariumidele.

Tagasimakse kanded luuakse automaatselt arvutusmeetodi alusel, mis valitakse ja planeeritakse partiitöödes. Lisaks saate seadistada töövood lepingute haldamiseks, läbivaatamiseks ja kinnitamiseks.

## <a name="basis-calculation"></a>Arvutuse alus

Kliendi tagasimaksed, kliendi autoritasud ja müüja tagasimaksed võivad kõik sõltuvalt teie ärinõuetest kasutada erinevat alust:

- Kliendi tagasimaksed võivad põhineda müügitellimustel, tarneteatel või arvetel.
- Kliendi autoritasud võivad põhineda müügitellimustel, tarneteatel või makstud arvetel.
- Müüja tagasimaksed võivad põhineda kas ostu- või müügitellimustel. Need saab arvutada tagasimakse hankijalt ostetud ja müügiarvete kaudu klientidele müüdud toodete põhjal.

## <a name="flexible-calculations"></a>Paindlikud kalkulatsioonid

Tagasimakse arvutamise perioodid on saadaval nii kliendi- kui hankijakannete puhul. Arvestusperiood määrab tehingu pikkuse, arvutussageduse ja -perioodi. Tagasimakseid saab koguneda vastavalt müügitellimuste kogustele või kvalifitseeritud toodete summadele tagasimakseperioodi jooksul.

Iga lepingu arvutamiseks saab seadistada mis tahes järgmisi perioode.

- Arve
- Päev
- Nädal
- Kuu
- Kvartal
- Aasta
- Kohandatud periood
- Mis tahes varem loetletud perioodide mis tahes kordsed

Arvutust saab rakendada üksikutele klientidele ja toodetele, klientide ja toodete rühmadele või kõigile klientidele ja toodetele. Mitme üksikasja reaga tagasimaksetel võivad olla erinevad kvalifitseerumiskuupäeva vahemikud. Sätted ja nõude perioodid võivad erineda. Näiteks saab eraldisi töödelda iga päev, samas kui nõudeid töödeldakse üks kord kuus.

Tagasimakseid saab konfigureerida paljude erinevate parameetrite alusel. Näiteks saab neid konfigureerida protsendina, määrana või fikseeritud summana. On olemas neli peamist arvutusmeetodit:

- Astmeline
- Kumulatiivne
- Jooksev
- Koguväärtus

Tagasimakse kalkulatsiooni tulemusi saab vähendada ka teiste tagasimaksete võrra, sõltuvalt sellest, kas tagasimakse on seadistatud arvutama netosumma põhjal või mitte.

Müüja poolel saavad müügitellimustel põhinevad allahindlused hinna arvutamisel lähtuda FIFO-reeglist, viimase ostuhinnast, keskmisest ostuhinnast või müügihinnast.

## <a name="rebate-target-transactions"></a>Tagasimakse sihtkanded

Tagasimakse lepingu või kokkuleppe loodud väljundid võivad olla rahalised vahendid või kirjed.

Finantsväljundid määratakse maksetüübi järgi, mis määratakse lepingule sisestusprofiilist. Need väljundid võivad hõlmata kliendi mahaarvamise töölehti, vabas vormis arveid ja müüja arveid. Auditeerimise eesmärgil sisaldavad rahaliste tagasimaksete sihttehingud viidet algsele tagasimakselepingule.

Kauba väljundid loovad vaba kauba müügitellimuse kliendi tagasimaksetele ja ostutellimuse müüja tagasimaksetele. Kauba tagasimakse sihtkanded sisaldavad valikuid, et määrata, milline tagasimakse viide tuleks sisestada tasuta kauba müügitellimusele või ostutellimusele.

## <a name="accurate-rebate-calculations"></a>Täpsed tagasimakse arvutused

Seotud tehingute, arvutuste sageduse, arvutusaluse ja valitud arvutusmeetodi kombinatsioon määrab allahindluste arvutuste täpsuse. Tagasimakse sätteid saab kasutada postitatud ja taotletud väärtuste kogumiseks.

Sätteid saab hallata iga päev, iga nädal, iga kuu või vastavalt kohandatud perioodile. Kuid funktsiooniga saab allahindlust eraldada või maksta või selle eest maksta mis tahes määratud sagedusega, mis on sama või pikem kui eraldamissagedus. Mahakandmine kasutab allahindlusega sama sagedust. Kasutajad saavad väljamakse ajal plaani või makseid hõlpsalt kohandada.

Kasutajad ei pea enam kahe sammuga tehinguid või sätteid käsitlema. Kanded ja mahakandmised sisestatakse otse pearaamatusse. Kreeditarveid saab luua ka automaatselt. Seetõttu toimub täielik integreerimine ostureskontro ja müügireskontroga. Töötlemise käigus arvestatakse arvutustes arveldussoodustusi, tasutud arveid, kauplemissoodustusi ja olemasolevaid kreeditarveid, et tagada summade ja väärtuste täpne arvutamine.

Tagasimaksete arvutamisel loob protsess kanded, mille saab enne sisestamist üle vaadata. Eraldi protsess sisestab allahindluse halduse kanteid. Seejärel saab soovitatud kannetele sisestamise ajal luua töölehe, kreeditarve või deebetkande. Aruandluse aruandeid ja kandeloendiid on võimalik saada, et tagada vastavus, efektiivsus ja tõhusus.


## <a name="guaranteed-royalty-payments"></a>Garantiiga autoritasud

Tagasimaksehalduses võimaldab automaatne makse loomine autoritasusid käsitseda kiiresti ja hõlpsasti, isegi siis, kui rakenduvad garantii miinimumid. 

## <a name="maximizing-spend-versus-rebates"></a>Kulu ja tagasimaksete maksimeerimine

Müüjaid ja tooteid saab rühmitada territooriumi järgi ning pakkuda erinevaid pakkumisi olenevalt tehingu riigist või piirkonnast. Kui kasutajad valivad tooteid, saavad nad määrata kaasatud kaubad ja tagasimakse otsuses kasutatavate kaupade arvu.
