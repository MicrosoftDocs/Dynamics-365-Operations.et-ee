---
title: Standardkulu hälbe sisestamine
description: Sellest teemast leiate teavet standardkuluarvestuse sisestusreeglite seadistamise kohta.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804637"
---
# <a name="standard-cost-variance-posting"></a>Standardkulu hälbe sisestamine

Kui kasutate oma organisatsioonis ühe või mitme toote standardset kuluarvestust, peate konfigureerima [standardse kuluarvestuse eeltingimused](/supply-chain/cost-management/prerequisites-standard-costs.md). See teema selgitab sisestuskontosid, mida on vaja eeltingimuste sammu 3 jaoks, "Määrake pearaamatukontod kauba sisestustele, mis on seotud standardsete kuluhälvetega."

Ostu- ja tootmistellimuste puhul võib esineda eri tüüpi hälbeid. Tootmiskulude hälvete näiteid vt teemast [Tootmishälvete tavalised allikad](/supply-chain/cost-management/common-sources-of-production-variances.md). Ostutellimuse hinna hälbeid kasutatakse siis, kui kasutate ostetud kauba standardset kulu ning ostutellimusel on erinevus toote standardkulu ja arveldatud summa vahel.

## <a name="sample-posting-profile-configuration"></a>Sisestusprofiili näidiskonfiguratsioon

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid. See sisaldab näidis põhikontosid ja kirjeldusi.

- Deebet/kreedit?" Veerg <a0/& näitab, kas kanne on tavaliselt deebet või kreedit. Mõnel juhul saab kanne sisestada deebeteid või kreediteid.
- Veerg Kliiringukonto näitab, et sisestamistüüp on kliiringukonto. See tähendab, et hilisema kande sisestamisel tühistatakse kontole sisestatud summa automaatselt.
- Veerus "P/F" kuvatakse sisestamistüüp. "P" tähistab füüsilist sisestamist ja "F" esindab finantsilist sisestamist.
- Veerg Järgi näitab, kas sisestamistüübi põhikonto on tavaliselt sama, mis mõne muu sisestustüübi põhikonto. See näitab tavaliselt kasutatavat sisestustüüpi.

> [!NOTE]
> Tabelis on soovitused põhikontode ja põhikonto nimede kohta. Soovitame teil teha koostööd raamatupidajaga, et määratleda ärivajaduste jaoks parim konfiguratsioon.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Ostuhinna erinevus | 510310 | Ostuhinna erinevus | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse siis, kui ostuhinna ja ostutellimuse standardkulu vahel on hälve. |
| Varude kulu ümberhindlus | 510330 | Varude kulu ümberhindlus | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse siis, kui standardkuluüksuse puhul aktiveeritakse uus kuluversioon vaba kaubavaru ümberhinnamiseks. |
| Kulumuutuse hälve | 510320 | Kulumuutuse hälve | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse, kui laoaladel on standardkuludes erinevus või kui kaup tagastatakse ning algse standardkulu ja toote praeguse standardkulu vahel on muutus. |
| Tootmise saatepartii suuruse hälve | 510370 | Tootmise saatepartii suuruse hälve | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse siis, kui koosluse kalkulatsiooni aluse ja tootmistellimuse kulukalkulatsiooni tegeliku koguse vahel on erinevusi. |
| Tootmishinna hälve | 510340 | Tootmishinna hälve | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse hinnaerinevuste puhul tootmistellimuse eeldatava omahinna ja tegeliku kulu vahel. |
| Tootmise koguse hälve | 510350 | Tootmise koguse hälve | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse siis, kui tootmistellimuse eeldatava omahinna ja tegeliku kulu vahel on koguseerinevusi. |
| Tootmise asendamise hälve | 510360 | Tootmise asendamise hälve | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse, kui tootmistellimusel toimub ootamatu tarbimine. |
| Ümardamise hälve | 618160 | Ümardamise erinevus | Kulu | Kas | Nr | R | Pole kohaldatav | Seda kontot kasutatakse ümarduserinevuse puhul, kui tootmiskulud arvutatakse standardkuludest. |
