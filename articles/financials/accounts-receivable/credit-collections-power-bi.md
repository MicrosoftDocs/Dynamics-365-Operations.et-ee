---
title: "Krediidi ja võlanõuete halduse Power BI sisu"
description: "See teema kirjeldab, mida hõlmab krediidi ja võlanõuete halduse Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 694a8bfd4601b48a80872662fa7a16bf15d6e65c
ms.contentlocale: et-ee
ms.lasthandoff: 12/18/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Krediidi ja võlanõuete halduse Power BI sisu

See teema kirjeldab, mida hõlmab **krediidi ja võlanõuete halduse** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Krediidi ja võlanõuete halduse** Power BI sisu on mõeldud krediidi ja võlanõuete juhtidele ning võlanõuetega tegelevatele ametnikele. Selles antakse peamised krediidi ja võlanõuete mõõdikud, nt laekumata müügi päevad, laekumata saldo, krediidi maht ja kliendid, kes on krediidilimiidi ületanud. See kasutab kandeandmeid ja annab koondvaated krediidist ja võlanõuetest kõigi ettevõtete lõikes. Samuti pakub see andmete jaotust ettevõtete, kliendigruppide ja klientide lõikes.

See Power BI sisu koosneb 10 aruandelehest.

- Kaks ülevaatelehte (üks leht krediidiülevaate ja üks leht sissenõuete ülevaate jaoks).
- Kaheksa andmelehte, millel on üksikasjad krediidi ja võlanõuete mõõdikute kohta, mis on mitmesuguste dimensioonide lõikes osadeks jagatud.

Kõik summad on näidatud süsteemivaluutas. Süsteemi valuuta saab seadistada lehel **Süsteemi parameetrid**.

Vaikimisi kuvatakse praeguse ettevõtte krediidi ja võlanõuete andmed. Andmete vaatamiseks kõigi ettevõtete lõikes määrake rollile kohustus **CustCollectionsBICrossCompany**.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Power BI sisu **Krediidi ja võlanõuete haldus** kuvatakse tööruumis **Klientide krediidihaldus ja võlanõuded**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded

**CustCollectionsBICrossCompany** Power BI sisu sisaldab aruannet, mis koosneb mõõdikute kogumist. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate Power BI sisu **CustCollectionsBICrossCompany** visualiseerimistest.

| Aruandeleht                 | Visualiseering |
|-----------------------------|---------------|
| Võlanõuete ülevaade        | <ul><li>Tähtaja ületanud kliendid</li><li>Krediidilimiiti ületavad kliendid</li><li>DSO 30 päeva</li><li>Avatud juhtumid</li><li>Keskmine päevade arv teenindusjuhtumi sulgemiseni</li><li>Avatud tegevused</li><li>Keskmine päevade arv tegevuste sulgemiseni</li><li>Avatud viivisearved</li><li>Avatud märgukirjad</li><li>Ootel klient</li><li>Ootel müük</li><li>Aegunud saldod</li><li>Võlanõuete oleku summad</li><li>Võlanõuete koodi summad</li><li>Mahakandmine põhjusega</li><li>Tähtajaline saldo regiooniti</li><li>Eeldatavad maksed</li></ul> |
| Krediidi ülevaade             | <ul><li>Tähtaja ületanud kliendid</li><li>Krediidilimiit võrreldes deebetsaldoga</li><li>Krediidilimiiti ületavate klientide tabel</li><li>Krediidilimiiti ületavad kliendid ettevõtte kohta</li><li>Kasutatud krediit võrreldes kogu krediidilimiidiga</li><li>Krediidilimiit võrreldes regiooniti kasutatud krediidiga</li><li>Kliendid krediidireitingu kohta</li></ul> |
| Krediidilimiit                | <ul><li>Krediidilimiit</li><li>Krediidilimiidi üksikasjad</li><li>Krediidilimiit kliendi kohta</li><li>Krediidilimiit kliendigrupi kohta</li><li>Krediidilimiit ettevõtte krediidireitingu kohta</li><li>Krediidilimiit vs. regiooniti kasutatud krediit</li></ul> |
| Krediidilimiiti ületavad kliendid | <ul><li>Krediidilimiiti ületavad kliendid</li><li>Krediidilimiiti ületavate klientide üksikasjad</li><li>Krediidilimiiti ületavad kliendid ettevõtte kohta</li><li>Krediidilimiiti ületavad kliendid kliendigrupi kohta</li><li>Krediidilimiiti ületavad kliendid regiooniti</li></ul> |
| Tähtaja ületanud kliendid          | <ul><li>Tähtaja ületanud kliendid</li><li>Tähtaja ületanud kliendi üksikasjad</li><li>Tähtaja ületanud kliendid ettevõtte kohta</li><li>Tähtaja ületanud kliendid kliendigrupi kohta</li><li>Tähtaja ületanud kliendid regiooniti</li></ul> |
| Aegunud saldod               | <ul><li>Aegunud saldod</li><li>Aegunud saldode üksikasjad</li><li>Aegunud saldod ettevõtte kohta</li><li>Aegunud saldod kliendigrupi kohta</li></ul> |
| Eeldatavad maksed           | <ul><li>Eeldatavad maksed</li><li>Eeldatavate maksete üksikasjad</li><li>Eeldatavad maksed ettevõtte kohta</li><li>Eeldatavad maksed kliendigrupi kohta</li><li>Eeldatavad maksed regiooniti</li></ul> |
| Mahakandmised                  | <ul><li>Mahakandmised regiooniti</li><li>Mahakandmiste üksikasjad</li><li>Mahakandmised põhikonto järgi</li><li>Mahakandmised ettevõtte järgi</li><li>Mahakandmised kliendigrupi kohta</li><li>Mahakandmised regiooniti</li></ul> |
| Sissenõuete olek          | <ul><li>Vaidlustatud</li><li>Makselubadust on murtud</li><li>Makselubadus</li><li>Võlanõuete oleku üksikasjad</li><li>Võlanõuete oleku summad</li><li>Avatud juhtumid</li><li>Avatud tegevused</li></ul> |
| Märgukirjad         | <ul><li>Sissenõude koodi summad</li><li>Võlanõude koodi summa üksikasjad</li><li>Märgukirja summa ettevõtte kohta</li><li>Märgukirja summa kliendigrupi kohta</li><li>Märgukirja summa regiooniti</li></ul> |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Power BI-s filtreerimise ja kinnitamise kohta lisateabe saamiseks vaadake teemat [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Visualisatsioonis summeeritud alusandmete eksportimiseks saab kasutada ka alusandmete eksportimise funktsiooni.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

Aruandelehtede täitmiseks **krediidi ja võlanõuete halduse** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| Üksus                                      | Peamised koondmõõtmised           | Andmeallikas                                 | Väli                                                      | Kirjeldus |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Suletud tegevuste arv ja keskmine aeg nende tegevuste sulgemiseks. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Avatud tegevuste arv. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Aegunud saldode summa. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Tähtaja ületanud summad. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Suletud teenindusjuhtumite arv ja keskmine aeg nende teenindusjuhtumite sulgemiseks. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Avatud teenindusjuhtumite arv. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Avatud märgukirjade arv. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Sisestatud märgukirjade saldo. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Võlanõude olekuga kannete saldo. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Krediidi mahu summa ja summad, mille võrra kliendid on oma krediidilimiiti ületanud. |
| CustCollectionsBICustOnHold                 | Blokeeritud                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Ootel olevate klientide arv. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Laekumata müügi päevad 30 päeva kohta. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Eeldatavate maksete summa järgmise aasta jooksul. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Loodud viivisearvete arv. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Ootel olevate müügitellimuste arv. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Maha kantud kannete summa. |

