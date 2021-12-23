---
title: Planeerimise optimeerimise sobivuse analüüs
description: Selles teemas selgitatakse, kuidas kontrollida praegust seadistust ja andmeid planeerimise optimeerimise funktsiooni võimaluste suhtes.
author: ChristianRytt
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd0fdd677824db823f9bc42f0ad1bdd90cf3b16d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344974"
---
# <a name="planning-optimization-fit-analysis"></a>Planeerimise optimeerimise sobivuse analüüs

[!include [banner](../../includes/banner.md)]

Peaksite analüüsima planeerimise optimeerimise sobivuse analüüsi tulemust osana migreerimisprotsessist. Arvestage, et planeerimise optimeerimise ulatus ei ole praeguse sisseehitatud koondplaneerimise funktsiooniga võrdne. Soovitame teil töötada koos oma partneriga ja lugeda dokumentatsiooni, et migreerimise jaoks ette valmistuda. 

Planeerimise optimeerimise sobivuse analüüs aitab teil tuvastada, kus tulemus võib sisseehitatud koondplaneerimise mootori ja planeerimise optimeerimise vahel erineda. See analüüs tehakse teie praeguse seadistuse ja andmete alusel. 

Planeerimise optimeerimise sobivuse analüüsi tulemuse nägemiseks avage **Koondplaneerimine** \> **Seadistus** \> **Planeerimise optimeerimise sobivuse analüüs** ja valige seejärel **Käivita analüüs**. Kui analüüs tuvastab vastuolusid, loetletakse need samal lehel. (Analüüsimise käitamiseks võib kuluda mõni minut.)

> [!NOTE]
> Kui leitakse vastuolusid, saate planeerimise optimeerimist endiselt kasutada. Sobivuse analüüsi tulemused näitavad lihtsalt kohti, kus planeerimise teenus ei arvesta teie praeguse seadistusega. Teisisõnu näitavad need kohti, kus mõnda protsessi võidakse ignoreerida või ei toetata.

## <a name="analysis-results-example-1"></a>Analüüsi tulemused: näide 1

- **Funktsioon:** tootmine
- **Probleem:** kaubad, mille kooslus (BOM) on suurem kui null: 56
- **Selgitus:** sobivuse analüüsis leiti 56 kaupa, millel on tootmiseks koosluse seadistus. Kuna planeerimise optimeerimise praegune versiooni ei toetata tootmist, loob planeerimise optimeerimine plaanitud tootmistellimuste asemel plaanitud ostutellimused. Samuti kuvatakse hoiatus, mis loendab mõjutatud kaubad.

## <a name="analysis-results-example-2"></a>Analüüsi tulemused: näide 2

- **Funktsioon:** tegevused
- **Väljastus:** laovarude grupid, mille tegevuse arvutamine on lubatud: 6
- **Selgitus:** sobivuse analüüs leidis kuus laovarude gruppi, kus tegevuse arvutamine on sisse lülitatud. Kuna planeerimise optimeerimise praegune versioon ei toetata tegevusi, siis koondplaneerimise käigus tegevusi ei looda.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Sobivuse analüüsi võimalike tulemuste ülevaade

Järgmises tabelis on toodud tulemused, mida võidakse kuvada pärast sobivuse analüüsi. Numbrimärgid (_\#_) asendatakse numbriga, mis tähistab nimetatud probleemiga kirjete arvu. Toetatud või eelvaates funktsioonid on saadaval versiooniga 10.0.9 või hilisemaga (v.a juhul, kui veerus „Eeldatav saadavus” on loetletud suurem versiooninumber).

> [!NOTE]
> Mõni vastuolu ei ole planeerimise optimeerimise sobivuse analüüsiga tuvastatav. Lisateavet vt teemast [Klassikalise koondplaneerimise ja plaanimise optimeerimise vahelised erinevused](planning-optimization-differences-with-built-in.md).

| Funktsioon | Nimetatud probleem | Selgitus | Eeldatav saadavus |
| --- | --- | --- | --- |
| Tegevused | Laovarude grupp, mille tegevuste arvutamine on lubatud: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata ei looda praegu koondplaneerimise ajal tegevusi, kui planeerimise optimeerimine on lubatud. Tegevuste peamine eesmärk on pakkuda soovitusi olemasolevate tellimuste muutmiseks. Hinnake, kas teie äriprotsessi osana rakendatakse tegevusi aktiivselt või piisab tellimustega seotud viivituste teabest. | 2022. aprill |
| Põhikalendrid | Põhikalendrit kasutavad kalendrid: _\#_ | See funktsioon on ootel. Praegu eiratakse põhikalendrit, kui planeerimise optimeerimine on lubatud. Hinnake, kas teie äriprotsesside jaoks on vajalik põhikalender või piisab kalendrite otsesest seadistusest. | 2022. aprill | 
| Partii likvideerimiskoodid | Tasaarveldamatu partii likvideerimise koondandmed: _\#_ | See funktsioon on ootel. Praegu eiratakse partii likvideerimiskoode, kui planeerimise optimeerimine on lubatud. | 2022 oktoobris või uuem värskendus |
| Võimeline lubama (CTP) | Tellimuse vaikesätted, milles tarnekuupäeva kontrolliks on seatud CTP: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu CTP-d, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Staatilise plaani kopeerimine dünaamilisse plaani | Koondplaneerimise parameetrites on lubatud staatilise plaani kopeerimine dünaamilisse plaani. | Sellest sättest hoolimata ei kopeeri planeerimise optimeerimine staatilist plaani dünaamilisse plaani. Üldiselt on see kontseptsioon vähem oluline kiiruse ja täieliku taasloomise tõttu, mida planeerimise optimeerimine võimaldab. Kui kasutatakse kaht või enamat plaani, tuleb iga plaani jaoks käivitada koondplaneerimine. | 2022. oktoober |
| Kinnitamine | Laovarude grupid, millel on määratud automaatkinnitamise ajapiir: _\#_ | Versioonis 10.0.7 ja uuemates versioonides toetatakse kinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon _Automaatkinnitus planeerimise optimeerimiseks_ on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| Kinnitamine | Kauba laovarude kirjed, millel on määratud automaatkinnitamine: _\#_ | Versioonis 10.0.7 ja uuemates versioonides toetatakse automaatkinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon _Automaatkinnitus planeerimise optimeerimiseks_ on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| Kinnitamine | Koondplaanid, millel on määratud automaatkinnitamine: _\#_ | Versioonis 10.0.7 ja uuemates versioonides toetatakse automaatkinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon _Automaatkinnitus planeerimise optimeerimiseks_ on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| FitAnalysisPlanningItems | Plaanimisüksused: _\#_ | See funktsioon on ootel. Praegu käsitletakse plaanimisüksuseid nagu tavalisi kaupu, kui planeerimise optimeerimine on lubatud. | 2022 oktoobris või uuem värskendus |
| Eelarve | Laovarude grupid, millel on lubatud kontsernisiseste tellimuste kaasamine: _\#_ | Seda funktsiooni nüüd toetatakse. Lisateavet vt jaotisest [Kontsernisisene plaanimine](Intercompany-planning.md) | Toetatud |
| Eelarve | Laovarude grupid, mille sätte „Eelarve vähendamise aluseks on:” väärtus pole „Tellimused”: _\#_ | Seda funktsiooni nüüd toetatakse. Lisateavet vt [Põhiplaneerimine koos nõutud eelarvega](demand-forecast.md). | Toetatud |
| Eelarve | Alammudelitega eelarvemudelid: _\#_ |  Seda funktsiooni nüüd toetatakse. Lisateavet vt [Põhiplaneerimine koos nõutud eelarvega](demand-forecast.md). | Toetatud |
| Eelarve | Koondplaanid, millel on lubatud säte „Kaasa tarne-eelarve”: _\#_ | See funktsioon on ootel. Praegu ei toetata tarne-eelarvet, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2022 oktoobris või uuem värskendus |
| Ajapiir | Laovarude grupid, millel on määratud külmutamise ajapiir: _\#_ | Külmutamise ajapiiri ei kasutata sageli ja praegu pole plaanis seda planeerimise optimeerimisse kaasata. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | Pole rakendatav |
| Ajapiir | Kauba laovarude kirjed, millel on määratud külmutamise ajapiir: _\#_ | Külmutamise ajapiiri ei kasutata sageli ja praegu pole plaanis seda planeerimise optimeerimisse kaasata. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | Pole rakendatav |
| Ajapiir | Koondplaanid, millel on määratud külmutamise ajapiir: _\#_ | Külmutamise ajapiiri ei kasutata sageli ja praegu pole plaanis seda planeerimise optimeerimisse kaasata. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | Pole rakendatav |
| Kontsernisisene | Koondplaanid, mis hõlmavad plaanitud sissetulevat nõudlust: _\#_ | Seda funktsiooni nüüd toetatakse. Lisateavet vt jaotisest [Kontsernisisene plaanimine](Intercompany-planning.md) | Toetatud |
| Kanban | Kauba laovarude kirjed, mille plaanitud tellimusetüüp on kanban: _\#_ | See funktsioon on ootel. Praegu eiratakse kanbaniks määratud kauba laovarusid, kui planeerimise optimeerimine on lubatud. Plaanitud tellimusetüübi kanban puhul kuvatakse koondplaneerimise ajal hoiatus ja seotud nõudluse täitmiseks luuakse plaanitud ostutellimused. | 2022 oktoobris või uuem värskendus |
| Kanban | Kanban-tellimuse vaiketüübiga kaubad: _\#_ | Praegu eiratakse kanbaniks määratud vaiketellimusetüüpi, kui planeerimise optimeerimine on lubatud. Vaiketellimusetüübi kanban puhul kuvatakse koondplaneerimise ajal hoiatus ja seotud nõudluse täitmiseks luuakse plaanitud ostutellimused. | 2022 oktoobris või uuem värskendus |
| Toote töötsükli olek | Toote töötsükli olekud pole planeerimiseks aktiivsed: _\#_ | Seda funktsiooni nüüd toetatakse. Lisateavet vt [Välista tooted, millel on kindlad toote töötsükli olekud](product-lifecycle-state.md) | Toetatud |
| Tootmine | Ümardamise või mitme häälestusega koosluseread: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluseridade puhul ümardamist ja mitut häälestust, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Valemi mõõtmisega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluse- ja valemiridade puhul valemi mõõtmist, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Kauba asendamisega koosluse-/valemiread (plaanigrupid): _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluse- ja valemiridade puhul kauba asendamist (plaanigruppe), kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Negatiivse kogusega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Koosluse- ja valemiread, millel on negatiivne kogus, kaasatakse kogusega 0 (null) ja kuvatakse hoiatus, kui planeerimise optimeerimine on lubatud. Värskendage koondandmeid, et vältida hoiatusi. | 2022. oktoober |
| Tootmine | Ressursipõhise tarbimisega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Praegu eiratakse ressursipõhise tarbimisega koosluse-/valemiridasid, kui planeerimise optimeerimine on lubatud. Selle funktsiooni toetamisel kasutatakse materjalinõude korral tootmise alguskuupäeva. Kuni seda funktsiooni toetatakse, ei looda nõudeid materjalide jaoks, mis on märgitud ressursitarbimise lipuga. | 2022. oktoober |
| Tootmine | Etapipõhise tarbimisega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Praegu eiratakse koosluse-/valemiridadel etapipõhist tarbimist, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Püsiva või muutuva praagiga määratletud kooslused: _\#_ | See funktsioon on ootel. Praegu eiratakse kooslustele määratud püsivat või muutuvat praaki, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Allhankega kooslused: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluste allhankeseadistust, kui planeerimise optimeerimine on lubatud. | 2022. aprill |
| Tootmine | Kooslused ilma saidita: _\#_ | Seda funktsiooni nüüd toetatakse. Lisateavet vt jaotisest [Tootmise plaanimine](production-planning.md) | Toetatud |
| Tootmine | Kindla koosluse või marsruudinõuetega nõudlus: _\#_ | See funktsioon on ootel. Praegu eiratakse nõudlusele määratud kindlaid koosluse või marsruudinõudeid (nt müügitellimuse alamkooslust või -marsruuti), kui planeerimise optimeerimine on lubatud. Sellest sättest hoolimata kasutatakse standardset kooslust või marsruuti. | 2022. oktoober |
| Tootmine | Kaastoote/kõrvalsaadusega valemiversioonid: _\#_ | See funktsioon on ootel. Praegu eiratakse valemiversiooniga seotud kaastooteid ja kõrvalsaadusi, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Tuludega valemiversioonid: _\#_ | See funktsioon on ootel. Praegu eiratakse valemiversiooniga seotud tulu, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Järjestust sisaldavad plaanid: _\#_ | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu järjestust, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Tänasest varasema algusajaga kavandatud väljastatud tootmistellimused, mida ei ole alustatud: _\#_ | See funktsioon on ootel. Kui tootmistellimus viibib, eeldab koondplaneerimine praegu, et see viiakse lõpule täna. See on oluline väljastatud tootmistellimuste puhul, mille tarnekuupäev on minevikus, kuid see pole veel lõpetatud. | 2022. oktoober |
| Tootmine | Piiratud võimsusega kavandatud ressursid: _\#_ | See funktsioon on ootel. Praegu eiratakse piiratud võimsusega kavandatud ressursse, kui planeerimise optimeerimine on lubatud. Kavandamine toimub toote vaiketäitmisaja alusel. | 2022. oktoober |
| Tootmine | Plaanimisel kasutatavad marsruudid: _\#_ | See funktsioon on ootel. Praegu eiratakse marsruute, kui planeerimise optimeerimine on lubatud. Kasutatakse toote vaiketäitmisaega. | Eelvaade: toetatud (10.0.20), GA: oktoober 2021 |
| Tootmine | Müügirea reserveerimine koosnevusarvutuse abil: _\#_ | Koosnevusarvutust kasutavat müügirea reserveerimist ei toetata, kui planeerimise optimeerimine on lubatud. | 2022. oktoober |
| Tootmine | Tootmistellimuste koosnevusarvutusega plaanimine: _\#_ | Tootmistellimuste koosnevusarvutust kasutavat plaanimist ei toetata, kui planeerimise optimeerimine on lubatud. Tootmistellimusi saab plaanida ükshaaval. | 2022. oktoober |
| Pakkumiskutsed | Koondplaanid, mille pakkumiskutsed on lubatud: _\#_ | See funktsioon on ootel. Praegu ei peeta pakkumiskutseid (RFQ) nõudluseks, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2022. oktoober |
| Taotlused | Koondplaanid, mille taotlused on lubatud: _\#_ | Seda funktsiooni nüüd toetatakse. Lisateavet vt teemast [Ostutaotlused](purchase-requisitions.md). | Toetatud |
| Ohutuspiirid | Ohutuspiiriga laovarude grupid: _\#_ | Seda funktsiooni toetatakse nüüd osaliselt. Lisateabe saamiseks vt [Ohutuspiirid](safety-margins.md) | Sissetuleku ohutusvaru: toetatud. Lisatellimuse ohutusvaru ja väljamineku ohutusvaru: jaanuar 2022 |
| Ohutuspiirid | Ohutuspiiriga koondplaanid: _\#_ | Seda funktsiooni toetatakse nüüd osaliselt. Lisateabe saamiseks vt [Ohutuspiirid](safety-margins.md) | Sissetuleku ohutusvaru: toetatud. Lisatellimuse ohutusvaru ja väljamineku ohutusvaru: jaanuar 2022 |
| Puhvervaru täitmine | Kauba laovarude kirjed, mille säte „Täida minimaalselt” erineb sättest „Tänane kuupäev + tarneaeg”: _\#_ | Planeerimise optimeerimine kasutab sätet *Tänane kuupäev + tarneaeg*. See muudatus tehti selleks, et valmistada ette lihtsustatud planeerimise seadistamine tulevikus ja pakkuda kasutatavat tulemust. Kui tarneaega puhvervarus ei arvestata, lükatakse plaanitud tellimused, mis luuakse praeguse vähese vaba kaubavaru jaoks, täitmisaja tõttu alati edasi. Selline käitumismudel võib põhjustada palju müra ja soovimatuid plaanitud tellimusi. Parim tava on muuta sätet nii, et kasutatakse sätet *Tänane kuupäev + tarneaeg*. Värskendage koondandmeid, et vältida hoiatusi. | Pole rakendatav |
| Müügipakkumised | Koondplaanid, mille müügipakkumised on lubatud: _\#_ | See funktsioon on ootel. Praegu eiratakse pakkumisi, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2022 oktoobris või uuem värskendus |
| Kõlblikkusaeg | Koondplaanid, mille kõlblikkusaeg on lubatud: _\#_ | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu kõlblikkusaega, kui planeerimise optimeerimine on lubatud. | 2022. aprill |

## <a name="additional-resources"></a>Lisaressursid

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimise kasutamise alustamine](get-started.md)

[Klassikalise koondplaneerimise ja plaanimise optimeerimise vahelised erinevused](planning-optimization-differences-with-built-in.md)

[Parameetrid, mida planeerimise optimeerimine ei kasuta](not-used-parameters.md)

[Plaaniajaloo ja plaanimislogide kuvamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
