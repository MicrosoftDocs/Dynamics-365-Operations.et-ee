---
title: Planeerimise optimeerimise sobivuse analüüs
description: See artikkel selgitab, kuidas kontrollida oma praegust seadistust ja andmeid plaanimise optimeerimise funktsioonide suhtes.
author: t-benebo
ms.date: 08/11/2022
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 7e32b3ed6ed96de7193cc496e0630969137cd0c1
ms.sourcegitcommit: 15b331f39d6e3ef811b9c2bf055a4f5b4572bae2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/26/2022
ms.locfileid: "9591846"
---
# <a name="planning-optimization-fit-analysis"></a>Planeerimise optimeerimise sobivuse analüüs

[!include [banner](../../includes/banner.md)]

Peaksite analüüsima planeerimise optimeerimise sobivuse analüüsi tulemust osana migreerimisprotsessist. Arvestage, et planeerimise optimeerimise ulatus ei ole praeguse sisseehitatud koondplaneerimise funktsiooniga võrdne. Soovitame teil töötada koos oma partneriga ja lugeda dokumentatsiooni, et migreerimise jaoks ette valmistuda. 

Planeerimise optimeerimise sobivuse analüüs aitab teil tuvastada, kus tulemus võib sisseehitatud koondplaneerimise mootori ja planeerimise optimeerimise vahel erineda. See analüüs tehakse teie praeguse seadistuse ja andmete alusel. 

Planeerimise optimeerimise sobivuse analüüsi tulemuse nägemiseks avage **Koondplaneerimine** \> **Seadistus** \> **Planeerimise optimeerimise sobivuse analüüs** ja valige seejärel **Käivita analüüs**. Kui analüüs tuvastab vastuolusid, loetletakse need samal lehel. (Analüüsimise käitamiseks võib kuluda mõni minut.)

> [!NOTE]
>
> - Mõni vastuolu ei ole planeerimise optimeerimise sobivuse analüüsiga tuvastatav. Lisateavet vt teemast [Klassikalise koondplaneerimise ja plaanimise optimeerimise vahelised erinevused](planning-optimization-differences-with-built-in.md).
>
> - Kui leitakse vastuolusid, saate planeerimise optimeerimist endiselt kasutada. Sobivuse analüüsi tulemused näitavad lihtsalt kohti, kus planeerimise teenus ei arvesta teie praeguse seadistusega. Teisisõnu näitavad need kohti, kus mõnda protsessi võidakse ignoreerida või ei toetata.

## <a name="analysis-results-example-1"></a>Analüüsi tulemused: näide 1

- **Funktsioon:** tootmine
- **Probleem:** kaubad, mille kooslus (BOM) on suurem kui null: 56
- **Selgitus:** sobivuse analüüsis leiti 56 kaupa, millel on tootmiseks koosluse seadistus. Kuna planeerimise optimeerimise praegune versiooni ei toetata tootmist, loob planeerimise optimeerimine plaanitud tootmistellimuste asemel plaanitud ostutellimused. Samuti kuvatakse hoiatus, mis loendab mõjutatud kaubad.

## <a name="analysis-results-example-2"></a>Analüüsi tulemused: näide 2

- **Funktsioon:** tegevused
- **Väljastus:** laovarude grupid, mille tegevuse arvutamine on lubatud: 6
- **Selgitus:** sobivuse analüüs leidis kuus laovarude gruppi, kus tegevuse arvutamine on sisse lülitatud. Kuna planeerimise optimeerimise praegune versioon ei toetata tegevusi, siis koondplaneerimise käigus tegevusi ei looda.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Sobivuse analüüsi võimalike tulemuste ülevaade

Järgmises tabelis on toodud tulemused, mida võidakse kuvada pärast sobivuse analüüsi. Numbrimärgid (*\#*) asendatakse numbriga, mis tähistab nimetatud probleemiga kirjete arvu.

> [!IMPORTANT]
> Veel toetamata funktsioonide puhul annab järgmine tabel eeldatavat saadavusteavet, mis põhineb praegusel tegevusal. Neid hinnanguid tuleb ette teatamata muuta.

| Funktsioon | Nimetatud probleem | Selgitus | Eeldatav saadavus |
| --- | --- | --- | --- |
| Tegevused | Laovarude grupp, mille tegevuste arvutamine on lubatud: *\#* | Seda funktsiooni nüüd toetatakse. | Toetatud |
| Põhikalendrid | Põhikalendrit kasutavad kalendrid: *\#* | Seda funktsiooni nüüd toetatakse. | Toetatud | 
| Partii likvideerimiskoodid | Tasaarveldamatu partii likvideerimise koond: *\#* | See funktsioon on ootel. Praegu eiratakse partii likvideerimiskoode, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 <!-- KFM: Now available? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> |
| Võimeline lubama (CTP) | Tellimuse vaikesätted, milles tarnekuupäeva kontrolliks on seatud CTP: *\#* | Tarneahela halduses 10.0.28 *ja uuemas protsessis nimetatakse planeerimise optimeerimise CTP-iks* kinnitatud lähetus- ja vastuvõtukuupäevi, mis on saadaval pärast dünaamilise plaani käivitamist. Tarneahela halduse vanemate versioonide puhul eiratakse pärand-CTP sätet, kui planeerimise optimeerimine on lubatud. | Toetatud |
| Staatilise plaani kopeerimine dünaamilisse plaani | Koondplaneerimise parameetrites on lubatud staatilise plaani kopeerimine dünaamilisse plaani. | Sellest sättest hoolimata ei kopeeri planeerimise optimeerimine staatilist plaani dünaamilisse plaani. Üldiselt on see kontseptsioon vähem oluline kiiruse ja täieliku taasloomise tõttu, mida planeerimise optimeerimine võimaldab. Kui kasutatakse kaht või enamat plaani, tuleb iga plaani jaoks käivitada koondplaneerimine. | Pole |
| Kinnitamine | Laovarude grupid, millel on määratud automaatkinnitamise ajapiir: *\#* | Versioonis 10.0.7 ja uuemates versioonides toetatakse kinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon *Automaatkinnitus planeerimise optimeerimiseks* on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| Kinnitamine | Kauba laovarude kirjed, millel on määratud automaatkinnitamine: *\#* | Versioonis 10.0.7 ja uuemates versioonides toetatakse automaatkinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon *Automaatkinnitus planeerimise optimeerimiseks* on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| Kinnitamine | Koondplaanid, millel on määratud automaatkinnitamine: *\#* | Versioonis 10.0.7 ja uuemates versioonides toetatakse automaatkinnitamist eraldi kinnitamise pakett-tööna pärast koondplaneerimise lõpule viimist (eeldusel, et funktsioon *Automaatkinnitus planeerimise optimeerimiseks* on [funktsioonihalduses](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubatud). Arvestage sellega, et automaatkinnitus planeerimise optimeerimiseks põhineb tellimuse kuupäeval (alguskuupäeval), mitte vajaduse kuupäeval (lõppkuupäeval). Selline käitumismudel tagab, et plaanitud tellimuste kinnitamine toimub õigel ajal, ilma et peaksite kinnitamisajavahemikus täitmisajaga arvestama. | Toetatud |
| FitAnalysisPlanningItems | Plaanimisüksused: *\#* | See funktsioon on ootel. Praegu käsitletakse plaanimisüksuseid nagu tavalisi kaupu, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 või uuem |
| Eelarve | Laovarude grupid, millel on lubatud kontsernisiseste tellimuste kaasamine: *\#* | Seda funktsiooni nüüd toetatakse. Lisateavet vt jaotisest [Kontsernisisene plaanimine](Intercompany-planning.md) | Toetatud |
| Eelarve | Laovarude grupid, mille sätte „Eelarve vähendamise aluseks on:” väärtus pole „Tellimused”: *\#* | Seda funktsiooni nüüd toetatakse. Lisateavet vt [Põhiplaneerimine koos nõutud eelarvega](demand-forecast.md). | Toetatud |
| Eelarve | Alammudelitega eelarvemudelid: *\#* |  Seda funktsiooni nüüd toetatakse. Lisateavet vt [Põhiplaneerimine koos nõutud eelarvega](demand-forecast.md). | Toetatud |
| Eelarve | Koondplaanid, millel on lubatud säte „Kaasa tarne-eelarve”: *\#* | See funktsioon on ootel. Praegu ei toetata tarne-eelarvet, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2022 vabastav voo 2 või uuem |
| Ajapiir | Laovarude grupid, millel on määratud ajapiir: *\#* | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Ajapiir | Kauba laovarude kirjed, millel on määratud ajapiir: *\#* | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Ajapiir | Koondplaanid, millel on määratud ajapiir: *\#* | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu külmutamise ajapiiri seadistust, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Kontsernisisene | Koondplaanid, mis hõlmavad plaanitud sissetulevat nõudlust: *\#* | Seda funktsiooni nüüd toetatakse. Lisateavet vt jaotisest [Kontsernisisene plaanimine](Intercompany-planning.md) | Toetatud |
| Kanban | Kauba laovarude kirjed, mille plaanitud tellimusetüüp on kanban: *\#* | See funktsioon on ootel. Praegu eiratakse kanbaniks määratud kauba laovarusid, kui planeerimise optimeerimine on lubatud. Plaanitud tellimusetüübi kanban puhul kuvatakse koondplaneerimise ajal hoiatus ja seotud nõudluse täitmiseks luuakse plaanitud ostutellimused. | Tulevane laine |
| Kanban | Kanban-tellimuse vaiketüübiga kaubad: *\#* | Praegu eiratakse kanbaniks määratud vaiketellimusetüüpi, kui planeerimise optimeerimine on lubatud. Vaiketellimusetüübi kanban puhul kuvatakse koondplaneerimise ajal hoiatus ja seotud nõudluse täitmiseks luuakse plaanitud ostutellimused. | Tulevane laine |
| Toote töötsükli olek | Toote töötsükli olekud pole planeerimiseks aktiivsed: *\#* | Seda funktsiooni nüüd toetatakse. Lisateavet vt [Välista tooted, millel on kindlad toote töötsükli olekud](product-lifecycle-state.md) | Toetatud |
| Tootmine | Ümardamise või mitme häälestusega koosluseread: *\#* | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluseridade puhul ümardamist ja mitut häälestust, kui planeerimise optimeerimine on lubatud. | Tulevane laine|
| Töö | Valemi mõõtmisega koosluse-/valemiread: *\#* | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluse- ja valemiridade puhul valemi mõõtmist, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Kauba asendamisega koosluse-/valemiread (plaanigrupid): *\#* | See funktsioon on ootel. Sellest sättest hoolimata eiratakse praegu koosluse- ja valemiridade puhul kauba asendamist (plaanigruppe), kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Negatiivse kogusega koosluse-/valemiread: *\#* | See funktsioon on ootel. Koosluse- ja valemiread, millel on negatiivne kogus, kaasatakse kogusega 0 (null) ja kuvatakse hoiatus, kui planeerimise optimeerimine on lubatud. Värskendage koondandmeid, et vältida hoiatusi. | 2022 vabastav voo 2 |
| Töö | Ressursipõhise tarbimisega koosluse-/valemiread: *\#* | See funktsioon on ootel. Praegu eiratakse ressursipõhise tarbimisega koosluse-/valemiridasid, kui planeerimise optimeerimine on lubatud. Selle funktsiooni toetamisel kasutatakse materjalinõude korral tootmise alguskuupäeva. Kuni seda funktsiooni toetatakse, ei looda nõudeid materjalide jaoks, mis on märgitud ressursitarbimise lipuga. | 2022 vabastav voo 2 |
| Töö | Etapipõhise tarbimisega koosluse-/valemiread: *\#* | See funktsioon on ootel. Praegu eiratakse koosluse-/valemiridadel etapipõhist tarbimist, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Püsiva või muutuva praagiga määratletud kooslused: *\#* | See funktsioon on ootel. Praegu eiratakse kooslustele määratud püsivat või muutuvat praaki, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Allhankega kooslused: *\#* | Seda funktsiooni nüüd toetatakse. | Toetatud |
| Töö | Kooslused ilma saidita: *\#* | Seda funktsiooni nüüd toetatakse. Lisateavet vt jaotisest [Tootmise plaanimine](production-planning.md) | Toetatud |
| Tootmine | Kindla koosluse või marsruudinõuetega nõudlus: *\#* | See funktsioon on ootel. Praegu eiratakse nõudlusele määratud kindlaid koosluse või marsruudinõudeid (nt müügitellimuse alamkooslust või -marsruuti), kui planeerimise optimeerimine on lubatud. Sellest sättest hoolimata kasutatakse standardset kooslust või marsruuti. | 2022 vabastav voo 2 |
| Töö | Kaastoote/kõrvalsaadusega valemiversioonid: *\#* | See funktsioon on ootel. Praegu eiratakse valemiversiooniga seotud kaastooteid ja kõrvalsaadusi, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Tuludega valemiversioonid: *\#* | See funktsioon on ootel. Praegu eiratakse valemiversiooniga seotud tulu, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Järjestust sisaldavad plaanid: *\#* | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu järjestust, kui planeerimise optimeerimine on lubatud. | 2022 vabastav voo 2 |
| Töö | Tänasest varasema algusajaga kavandatud vabastatud tootmistellimused, mida ei ole alustatud: *\#* | See funktsioon on ootel. Kui tootmistellimus viibib, eeldab koondplaneerimine praegu, et see viiakse lõpule täna. See on oluline väljastatud tootmistellimuste puhul, mille tarnekuupäev on minevikus, kuid see pole veel lõpetatud. | Tulevane laine |
| Töö | Piiratud võimsusega kavandatud ressursid: *\#* | Seda funktsiooni nüüd toetatakse.| Toetatud |
| Töö | Plaanimisel kasutatavad marsruudid: *\#* | Seda funktsiooni toetatakse. | Toetatud |
| Töö | Müügirea reserveerimine koosnevusarvutuse abil: *\#* | Koosnevusarvutust kasutavat müügirea reserveerimist ei toetata, kui planeerimise optimeerimine on lubatud. | Tulevane laine |
| Töö | Tootmistellimuste koosnevusarvutusega plaanimine: *\#* | Tootmistellimuste koosnevusarvutust kasutavat plaanimist ei toetata, kui planeerimise optimeerimine on lubatud. Tootmistellimusi saab plaanida ükshaaval. | Tulevane laine |
| Pakkumiskutsed | Koondplaanid, mille pakkumiskutsed on lubatud: *\#* | See funktsioon on ootel. Praegu ei peeta pakkumiskutseid (RFQ) nõudluseks, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2022 vabastav voo 2 |
| Taotlused | Koondplaanid, mille taotlused on lubatud: *\#* | Seda funktsiooni nüüd toetatakse. Lisateavet vt teemast [Ostutaotlused](purchase-requisitions.md). | Toetatud |
| Ohutuspiirid | Ohutuspiiriga laovarude grupid: *\#* | Seda funktsiooni nüüd toetatakse. Lisateabe saamiseks vt [Ohutuspiirid](safety-margins.md) | Toetatud |
| Ohutuspiirid | Ohutuspiiriga koondplaanid: *\#* | Seda funktsiooni nüüd toetatakse. Lisateabe saamiseks vt [Ohutuspiirid](safety-margins.md) |  Toetatud |
| Puhvervaru täitmine | Kauba laovarude kirjed, mille säte „Täida minimaalselt” erineb sättest „Tänane kuupäev + tarneaeg”: *\#* | Planeerimise optimeerimine kasutab sätet *Tänane kuupäev + tarneaeg*. See muudatus tehti selleks, et valmistada ette lihtsustatud planeerimise seadistamine tulevikus ja pakkuda kasutatavat tulemust. Kui tarneaega puhvervarus ei arvestata, lükatakse plaanitud tellimused, mis luuakse praeguse vähese vaba kaubavaru jaoks, täitmisaja tõttu alati edasi. Selline käitumismudel võib põhjustada palju müra ja soovimatuid plaanitud tellimusi. Parim tava on muuta sätet nii, et kasutatakse sätet *Tänane kuupäev + tarneaeg*. Värskendage koondandmeid, et vältida hoiatusi. | Pole rakendatav |
| Müügipakkumised | Koondplaanid, mille müügipakkumised on lubatud: *\#* | See funktsioon on ootel. Praegu eiratakse pakkumisi, kui planeerimise optimeerimine on lubatud. Neid eiratakse, hoolimata sellest sättest. | 2022 vabastav voo 2 või uuem |
| Kõlblikkusaeg | Koondplaanid, mille kõlblikkusaeg on lubatud: *\#* | See funktsioon on ootel. Hoolimata sellest sättest eiratakse praegu kõlblikkusaega, kui planeerimise optimeerimine on lubatud. | Toetatud |

## <a name="additional-resources"></a>Lisaressursid

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimise kasutamise alustamine](get-started.md)

[Klassikalise koondplaneerimise ja plaanimise optimeerimise vahelised erinevused](planning-optimization-differences-with-built-in.md)

[Parameetrid, mida planeerimise optimeerimine ei kasuta](not-used-parameters.md)

[Plaaniajaloo ja plaanimislogide kuvamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
