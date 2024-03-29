---
title: Automaatsete kannete kontod
description: See artikkel selgitab, kuidas automaatsete kannete kontosid kasutatakse Microsoft Dynamics sisestamiseks kuni 365, ja annab näiteid automaatsete kannete võtmekontode kohta.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e72840fea1f5d89c908b00e2cf572bce6befbe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880755"
---
# <a name="accounts-for-automatic-transactions"></a>Automaatsete kannete kontod

Automaatsete **kannete lehe** kontosid (**automaatsete &gt;&gt;** kannete pearaamatu sisestamise seadistuskontod) kasutatakse süsteemi iga sisestamistüübi puhul kasutatava vaike põhikonto määratlemiseks. Kuigi enamik sisestustüüpe saab konfigureerida moodulispetsiifilisel või funktsioonipõhisel lehel, saab **mõnda sisestustüüpi konfigureerida ainult automaatsete kannete** lehel Kontodel.

Näiteks saate kliendi **sisestusreeglite** **·** **lehel** määrata kliendi saldo sisestustüübi jaoks kasutatava põhikonto välja Kokkuvõte ja kasutada iga kliendi reegli puhul erinevat põhikontot. Sel viisil on teil sisestuste üle granulaarsem kontroll. Te saate veakonto määrata aga ainult lehel Automaatsete **kannete kontod**.

Kui avate **uue juriidilise isiku jaoks** lehe Kontod automaatseks kanneteks, on kontode loend tühi. Saate lisada kõige tavalisemad sisestustüübid, mida tuleb lehel konfigureerida, kui valite nupu **Loo vaiketüübid**. Seejärel saate iga rea jaoks valida põhikonto väljal **Põhikonto**. **Kui** jätate põhikonto välja sisestamistüübi jaoks tühjaks ja pole konfigureerinud põhikontot mooduliomase või funktsiooniomase lehekülje jaoks, saate veateate, kui sisestate sisestustüüpi kasutav kanne. Tavaliselt on teateks "Sisestamise tüüpi \[\] kontot ei leitud."

## <a name="default-posting-types"></a>Vaikimisi sisestustüübid

Järgmine tabel näitab näiteid vaikimisi sisestustüüpide kohta, **mis luuakse, kui valite automaatsete kannete** **lehel kontodele vaiketüübid** loomine. See näitab näidis põhikontosid ja kirjeldusi. Deebet/kreedit?" Veerg <a0/& näitab, kas kanne sisestab tavaliselt deebeti või kreediti. Mõnel juhul võib kanne sisestada kas deebeti või kreediti. Veerg Kliiringukonto näitab, kas sisestamistüüp on kliiringukonto. Kui sisestamistüüp on kliiringukonto, tühistatakse kontole sisestatud summa hilisema kande sisestamisel automaatselt.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Sendierinevus aruandlusvaluutas | 618160 | Mitmesugused kulud | Kulu | Mõlemad | Nr | Seda sisestustüüpi kasutatakse sendierinevuse puhul, kui kandesumma välisvaluutas teisendatakse aruandlusvaluutasse. |
| Arvestusvaluuta sendierinevus | 618160 | Mitmesugused kulud | Kulu | Mõlemad | Nr | Seda sisestustüüpi kasutatakse sendierinevuse puhul, kui kandesumma välisvaluutas teisendatakse arvestusvaluutasse. |
| Veakonto | 999999 | Veakonto | Kulu | Mõlemad | Nr | Seda sisestamistüüpi kasutatakse siis, kui süsteemis ilmneb tõrge. Konto tuleks kinnitada igas perioodis ja kõik tõrked tuleb lahendada. |
| Aastalõpu tulemus | 300160 | Jaotamata kasum | Omakapital | Mõlemad | Nr | Seda sisestamistüüpi **kasutatakse** aasta lõpu sulgemise protsessi käivitamisel, et teisaldada tulu ja kulu tüüpi kontode saldo aasta lõpu tulemuse jaoks valitud põhikontole. |
| Kliendi skonto | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Nr | Automaatsete kannete lehel kontodel **määratletud sisestamistüüpi** ei kasutata. Põhikonto on nõutav, kui skontod konfigureeritakse Müügireskontros.|
| Hankija skonto | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav | Nr | Automaatsete kannete lehel kontodel **määratletud sisestamistüüpi** ei kasutata. Põhikonto on nõutav, kui skontod konfigureeritakse Ostureskontros. |

## <a name="additional-posting-types"></a>Täiendavad sisestustüübid

Järgmine tabel näitab näiteid täiendavate sisestustüüpide kohta, mida tuleb konfigureerida, kui kavatsete seotud funktsioone kasutada. Nende sisestustüüpide puhul ei ole teises moodulis saadaval ühtegi sisestusreegli konfiguratsiooni. Deebet/kreedit?" Veerg <a0/& näitab, kas kanne sisestab tavaliselt deebeti või kreediti. Mõnel juhul võib kanne sisestada kas deebeti või kreediti. Veerg Kliiringukonto näitab, kas sisestamistüüp on kliiringukonto. Kui sisestamistüüp on kliiringukonto, tühistatakse kontole sisestatud summa hilisema kande sisestamisel automaatselt.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Konsolideerimiserinevuse bilansikonto | 801200 | Kasum ja kahjum – ümberhindamine | Kulu | Mõlemad | Nr | Seda sisestamistüüpi kasutatakse, kui teete konsolideerimist, mis hõlmab valuuta ümberarvutamist ja ümberhindamise ajal ilmnevad sendierinevused. |
| Konsolideerimiserinevuste tulu ja kulu konto | 801200 | Kasum ja kahjum – ümberhindamine | Kulu | Mõlemad | Nr | Seda sisestamistüüpi kasutatakse, kui teete konsolideerimist, mis hõlmab valuuta ümberarvutamist ja ümberhindamise ajal ilmnevad sendierinevused. |
| Kontsernisisene – deebet | 133500 | Saadaolev kontsernisisene | Vara | Deebet | Nr | Seda sisestamistüüpi kasutatakse siis, kui **valite** pearaamatulehel tasakaalustusdimensiooni ja dimensioon ei ole sisestatud kandes tasakaalus. |
| Üksustevaheline – kreedit | 233500 | Kontsernisisene kohustus | Kohustus | Krediit | Nr | Seda sisestamistüüpi kasutatakse siis, kui **valite** pearaamatulehel tasakaalustusdimensiooni ja dimensioon ei ole sisestatud kandes tasakaalus. |
