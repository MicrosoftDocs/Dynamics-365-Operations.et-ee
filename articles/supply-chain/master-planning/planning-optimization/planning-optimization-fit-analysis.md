---
title: Planeerimise optimeerimise sobivuse analüüs
description: Selles teemas selgitatakse, kuidas kontrollida praegust seadistust ja andmeid planeerimise optimeerimise funktsiooni võimaluste suhtes.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 04605370cbcc7b8c13552ae7f999212a1efabfab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967057"
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

| Funktsioon | Nimetatud probleem | Selgitus | Eeldatav saadavus |
| --- | --- | --- | --- |
| Tegevused | Laovarude grupp, mille tegevuste arvutamine on lubatud: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata ei looda praegu koondplaneerimise ajal tegevusi, kui planeerimise optimeerimine on lubatud. Tegevuste peamine eesmärk on pakkuda soovitusi olemasolevate tellimuste muutmiseks. Hinnake, kas teie äriprotsessi osana rakendatakse tegevusi aktiivselt või piisab tellimustega seotud viivituste teabest. | 2021. oktoober |
| Põhikalendrid | Põhikalendrit kasutavad kalendrid: _\#_ | See funktsioon on ootel. Praegu eiratakse põhikalendrit, kui planeerimise optimeerimine on lubatud. Hinnake, kas teie äriprotsesside jaoks on vajalik põhikalender või piisab kalendrite otsesest seadistusest. | 2021. aprill | 
| Partii likvideerimiskoodid | Tasaarveldamatu partii likvideerimise koondandmed: _\#_ | See funktsioon on ootel. Praegu eiratakse partii likvideerimise koode, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Võimeline lubama (CTP) | Tellimuse vaikesätted, milles tarnekuupäeva kontrolliks on seatud CTP: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu CTP-d, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Staatilise plaani kopeerimine dünaamilisse plaani | Koondplaneerimise parameetrites on lubatud staatilise plaani kopeerimine dünaamilisse plaani. | Sellest sättest hoolimata ei kopeeri planeerimise optimeerimine staatilist plaani dünaamilisse plaani. Üldiselt on see kontseptsioon vähem oluline kiiruse ja täieliku taasloomise tõttu, mida planeerimise optimeerimine võimaldab. Kui kasutatakse kaht või enamat plaani, tuleb iga plaani jaoks käivitada koondplaneerimine. | 2021. oktoober |
| Kinnitamine | Laovarude grupid, millel on määratud automaatkinnitamise ajapiir: _\#_ | Versioonis 10.0.7 ja uuemates versioonides toetatakse kinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon _Automaatkinnitus planeerimise optimeerimiseks_ on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| Kinnitamine | Kauba laovarude kirjed, millel on määratud automaatkinnitamine: _\#_ | Versioonis 10.0.7 ja uuemates versioonides toetatakse automaatkinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon _Automaatkinnitus planeerimise optimeerimiseks_ on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| Kinnitamine | Koondplaanid, millel on määratud automaatkinnitamine: _\#_ | Versioonis 10.0.7 ja uuemates versioonides toetatakse automaatkinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon _Automaatkinnitus planeerimise optimeerimiseks_ on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| FitAnalysisPlanningItems | Plaanimisüksused: _\#_ | See funktsioon on ootel. Praegu käsitletakse plaanimisüksuseid nagu tavalisi kaupu, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Eelarve | Laovarude grupid, millel on lubatud kontsernisiseste tellimuste kaasamine: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata ei hõlma koondplaneerimine praegu sissetulevat planeeritud nõudlust, kui planeerimise optimeerimine on lubatud. Pange tähele, et väljastatud/kinnitatud tellimused töötavad endiselt tavaliste kontsernisiseste funktsioonidega ja hõlmavad enamikku stsenaariume. | Eelvaates |
| Eelarve | Laovarude grupid, mille sätte „Prognoosi vähendamisalus:” väärtus pole „Tellimused”: _\#_ | Sellest sättest hoolimata kasutab planeerimise optimeerimine tellimuste puhul vaikimisi sätet „Prognoosi vähendamisalus:”. | Toetatud |
| Eelarve | Alammudelitega prognoosimudelid: _\#_ | See funktsioon on ootel. Praegu ei toetata allmudeleid kasutavaid prognoose, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2021. aprill |
| Eelarve | Koondplaanid, millel on lubatud säte „Kaasa tarneprognoos”: _\#_ | See funktsioon on ootel. Praegu ei toetata tarneprognoose, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2021. oktoober |
| Ajapiir | Laovarude grupid, millel on määratud külmutamise ajapiir: _\#_ | Külmutamise ajapiiri ei kasutata sageli ja praegu pole plaanis seda planeerimise optimeerimisse kaasata. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | Pole rakendatav |
| Ajapiir | Kauba laovarude kirjed, millel on määratud külmutamise ajapiir: _\#_ | Külmutamise ajapiiri ei kasutata sageli ja praegu pole plaanis seda planeerimise optimeerimisse kaasata. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | Pole rakendatav |
| Ajapiir | Koondplaanid, millel on määratud külmutamise ajapiir: _\#_ | Külmutamise ajapiiri ei kasutata sageli ja praegu pole plaanis seda planeerimise optimeerimisse kaasata. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | Pole rakendatav |
| Kontsernisisene | Koondplaanid, mis hõlmavad plaanitud sissetulevat nõudlust: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata ei hõlma koondplaneerimine praegu sissetulevat planeeritud nõudlust, kui planeerimise optimeerimine on lubatud. Pange tähele, et väljastatud/kinnitatud tellimused töötavad endiselt tüüpiliste kontsernisiseste funktsioonidega ja hõlmavad enamikku stsenaariume. | Eelvaates |
| Kanban | Kauba laovarude kirjed, mille plaanitud tellimusetüüp on kanban: _\#_ | See funktsioon on ootel. Praegu eiratakse kanbaniks määratud kauba laovarusid, kui planeerimise optimeerimine on lubatud. Plaanitud tellimusetüübi kanban puhul kuvatakse koondplaneerimise ajal hoiatus ja seotud nõudluse täitmiseks luuakse plaanitud ostutellimused. | 2021. oktoober |
| Kanban | Kanban-tellimuse vaiketüübiga kaubad: _\#_ | Praegu eiratakse kanbaniks määratud vaiketellimusetüüpi, kui planeerimise optimeerimine on lubatud. Vaiketellimusetüübi kanban puhul kuvatakse koondplaneerimise ajal hoiatus ja seotud nõudluse täitmiseks luuakse plaanitud ostutellimused. | 2021. oktoober |
| Toote töötsükli olek   | Toote töötsükli olekud pole planeerimiseks aktiivsed: _\#_ | See on ootel funktsioon. Hetkel toote töötsükli olekut ignoreeritakse, kui planeerimise optimeerimine on lubatud. Saate korrigeerida plaani taseme tootefiltrit, et vältida toodete kaasamist, kui planeerimisel on toote töötsükli olek keelatud. | Toetatud |
| Tootmine | Ümardamise või mitme häälestusega koosluseread: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluseridade puhul ümardamist ja mitut häälestust, kui planeerimise optimeerimine on lubatud. | 2021. aprill |
| Tootmine | Valemi mõõtmisega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluse- ja valemiridade puhul valemi mõõtmist, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Kauba asendamisega koosluse-/valemiread (plaanigrupid): _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluse- ja valemiridade puhul kauba asendamist (plaanigruppe), kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Negatiivse kogusega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Koosluse- ja valemiread, millel on negatiivne kogus, kaasatakse kogusega 0 (null) ja kuvatakse hoiatus, kui planeerimise optimeerimine on lubatud. Värskendage koondandmeid, et vältida hoiatusi. | 2021. oktoober |
| Tootmine | Ressursipõhise tarbimisega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Praegu eiratakse ressursipõhise tarbimisega koosluse-/valemiridasid, kui planeerimise optimeerimine on lubatud. Selle funktsiooni toetamisel kasutatakse materjalinõude korral tootmise alguskuupäeva. Kuni seda funktsiooni toetatakse, ei looda nõudeid materjalide jaoks, mis on märgitud ressursitarbimise lipuga. | 2021. aprill |
| Tootmine | Etapipõhise tarbimisega koosluse-/valemiread: _\#_ | See funktsioon on ootel. Praegu eiratakse koosluse-/valemiridadel etapipõhist tarbimist, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Püsiva või muutuva praagiga määratletud kooslused: _\#_ | See funktsioon on ootel. Praegu eiratakse kooslustele määratud püsivat või muutuvat praaki, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Allhankega kooslused: _\#_ | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluste allhankeseadistust, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Kooslused ilma saidita: _\#_ | See funktsioon on ootel. Praegu eiratakse saidita kooslusi, kui planeerimise optimeerimine on lubatud. | Toetatud |
| Tootmine | Kindla koosluse või marsruudinõuetega nõudlus: _\#_ | See funktsioon on ootel. Praegu eiratakse nõudlusele määratud kindlaid koosluse või marsruudinõudeid (nt müügitellimuse alamkooslust või -marsruuti), kui planeerimise optimeerimine on lubatud. Sellest sättest hoolimata kasutatakse standardset kooslust või marsruuti. | 2021. oktoober |
| Tootmine | Kaastoote/kõrvalsaadusega valemiversioonid: _\#_ | See funktsioon on ootel. Praegu eiratakse valemiversiooniga seotud kaastooteid ja kõrvalsaadusi, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Tuludega valemiversioonid: _\#_ | See funktsioon on ootel. Praegu eiratakse valemiversiooniga seotud tulu, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Järjestust sisaldavad plaanid: _\#_ | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu järjestust, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Tänasest varasema algusajaga kavandatud väljastatud tootmistellimused, mida ei ole alustatud: _\#_ | See funktsioon on ootel. Kui tootmistellimus viibib, eeldab koondplaneerimine praegu, et see viiakse lõpule täna. See on oluline väljastatud tootmistellimuste puhul, mille tarnekuupäev on minevikus, kuid see pole veel lõpetatud. | 2021. oktoober |
| Tootmine | Piiratud võimsusega kavandatud ressursid: _\#_ | See funktsioon on ootel. Praegu eiratakse piiratud võimsusega kavandatud ressursse, kui planeerimise optimeerimine on lubatud. Kavandamine toimub toote vaiketäitmisaja alusel. | 2021. aprill |
| Tootmine | Plaanimisel kasutatavad marsruudid: _\#_ | See funktsioon on ootel. Praegu eiratakse marsruute, kui planeerimise optimeerimine on lubatud. Kasutatakse toote vaiketäitmisaega. | 2021. aprill |
| Tootmine | Müügirea reserveerimine koosnevusarvutuse abil: _\#_ | Koosnevusarvutust kasutavat müügirea reserveerimist ei toetata, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |
| Tootmine | Tootmistellimuste koosnevusarvutusega plaanimine: _\#_ | Tootmistellimuste koosnevusarvutust kasutavat plaanimist ei toetata, kui planeerimise optimeerimine on lubatud. Tootmistellimusi saab plaanida ükshaaval. | 2021. oktoober |
| Pakkumiskutsed | Koondplaanid, mille pakkumiskutsed on lubatud: _\#_ | See funktsioon on ootel. Praegu ei peeta pakkumiskutseid (RFQ) nõudluseks, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2021. oktoober |
| Taotlused | Koondplaanid, mille taotlused on lubatud: _\#_ | See funktsioon on ootel. Praegu eiratakse taotlusi, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2021. oktoober |
| Ohutuspiirid | Ohutusvaruga laovarude grupid: _\#_ | See funktsioon on ootel. Praegu eiratakse ohutusvaru, kui planeerimise optimeerimine on lubatud. Selle käitumismudeli kompenseerimiseks saate pikendada täitmisaega nii, et see sisaldaks ohutusvaru. | Sissetuleku ohutusvaru: toetatud. Lisatellimuse ohutusvaru ja väljamineku ohutusvaru: aprill 2021 |
| Ohutuspiirid | Ohutusvaruga koondplaanid: _\#_ | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu ohutusvaru, kui planeerimise optimeerimine on lubatud. Selle käitumismudeli kompenseerimiseks saate pikendada täitmisaega nii, et see sisaldaks ohutusvaru. | Sissetuleku ohutusvaru: toetatud. Lisatellimuse ohutusvaru ja väljamineku ohutusvaru: aprill 2021 |
| Puhvervaru täitmine | Kauba laovarude kirjed, mille säte „Täida minimaalselt” erineb sättest „Tänane kuupäev + tarneaeg”: _\#_ | Planeerimise optimeerimine kasutab sätet *Tänane kuupäev + tarneaeg*. See muudatus tehti selleks, et valmistada ette lihtsustatud planeerimise seadistamine tulevikus ja pakkuda kasutatavat tulemust. Kui tarneaega puhvervarus ei arvestata, lükatakse plaanitud tellimused, mis luuakse praeguse vähese vaba kaubavaru jaoks, täitmisaja tõttu alati edasi. Selline käitumismudel võib põhjustada palju müra ja soovimatuid plaanitud tellimusi. Parim tava on muuta sätet nii, et kasutatakse sätet *Tänane kuupäev + tarneaeg*. Värskendage koondandmeid, et vältida hoiatusi. | Pole rakendatav |
| Müügipakkumised | Koondplaanid, mille müügipakkumised on lubatud: _\#_ | See funktsioon on ootel. Praegu eiratakse pakkumisi, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2021. oktoober |
| Kõlblikkusaeg | Koondplaanid, mille kõlblikkusaeg on lubatud: _\#_ | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu kõlblikkusaega, kui planeerimise optimeerimine on lubatud. | 2021. oktoober |

## <a name="additional-resources"></a>Lisaressursid

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimisega alustamine](get-started.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]