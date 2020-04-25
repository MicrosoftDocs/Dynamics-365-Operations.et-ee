---
title: Kvaliteedijuhtimise protsessid
description: Selles artiklis antakse teavet mittevastavate toodete kvaliteedijuhtimise protsessi kohta. Kirjeldatakse, kuidas saate kasutada kvaliteedikontrolli funktsiooni, kuidas määratleda ja hallata mittevastavusi ning kuidas käsitleda parandusi.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ab3b886b9d5237e96e193d7369c6060f19516e5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214063"
---
# <a name="quality-management-processes"></a>Kvaliteedijuhtimise protsessid

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet mittevastavate toodete kvaliteedijuhtimise protsessi kohta. Kirjeldatakse, kuidas saate kasutada kvaliteedikontrolli funktsiooni, kuidas määratleda ja hallata mittevastavusi ning kuidas käsitleda parandusi.

Kvaliteedijuhtimine hõlmab toote testimist ja mittevastava materjali haldamist. Kvaliteedijuhtimise protsessid aitavad tagada toote kõrge kvaliteedi teie tarneahelas. Need protsessid aitavad optimeerida ka tarneahela protsesse ja suurendada klientide rahulolu. Kvaliteedijuhtimise abil saate hallata ümberpööramise aegu, kui käsitsete mittevastavaid tooteid, olenemata nende toodete päritolukohast. Saate siduda diagnostilisi tulemusi parandustoimingutega. Süsteem saab probleemide lahendamiseks ülesandeid plaanida ja seega aidata vältida tulevikus nende probleemide kordumist. Kvaliteedijuhtimine võimaldab teil ka probleeme (sealhulgas ettevõttesiseseid probleeme) probleemi tüübi järgi jälgida ja leida lühiajalisi või pikaajalisi lahendusi. Tulemuslikkuse võtmenäitajate (KPI) statistika annab ülevaate varasematest mittevastavuse probleemidest ja nende kõrvaldamiseks kasutatud lahendustest. Saate kasutada varasemaid andmeid varasemate kvaliteedimeetmete tulemuslikkuse ülevaatamiseks ja sobivate tulevikus kasutatavate meetmete määramiseks.

## <a name="controlling-the-quality-management-process"></a>Kvaliteedijuhtimise protsessi kontrollimine
Siin on mõned kvaliteedijuhtimise protsessi kontrollimise viisid.

-   Saate koostada kvaliteettellimusi, mis põhinevad käivitamispunktidel (nt „toote sissetulekul” sissetulevate toimingute või „toote pealevõtmisel” väljaminevate toimingute puhul).
-   Saate katsetulemusi dokumenteerida ja määratleda, kas tulemused vastavad kehtestatud katsekriteeriumidele ja vastuvõetavatele kvaliteeditasemetele.
-   Saate kontrollimisprotsessi käigus kasutada aruandluse osana dokumendihaldust toote üksikasjalike andmete ja kasutajapõhiste märkmete jaoks.
-   Saate hallata mittevastavaid tooteid ja seostada neid tooteid täiendava mittevastavuse teabega, et selgitada välja probleemi algpõhjus.
-   Saate dokumenteerida mittevastavuse haldamise kulu. See kulu võib sisaldada kaupu (nt varuosi), lisakulusid ja ajatabeli tunde, mis on mittevastavuse kõrvaldamiseks vajalikud.
-   Saate plaanida veaparandusprotsesse, kasutades paranduste käsitsemist, mis on kvaliteettellimustega seotud.

[![Kvaliteedijuhtimise protsess](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Tootetestimine ja kvaliteettellimused
Tootetestimist nimetatakse tavaliselt kvaliteedikontrolliks ning selle korral kasutatakse kvaliteettellimusi. Kvaliteedikontrolli funktsiooni kasutamisel saate teha järgmist.

-   Määratleda katsed, mis tuleb materjaliga teha. Need testid hõlmavad kvaliteedispetsifikatsioone, rakendatavat testimisvahendit, testi kirjeldavaid dokumente, valimi plaani ja vastuvõetavaid kvaliteeditasemeid (AQL).
-   Saate luua kvaliteettellimuse, mis määratleb konkreetses tellimuse (nt ostu- või tootmistellimuse) või konkreetse laokoguse puhul läbi viidavad testid. Saate koostada kvaliteettellimuse käsitsi või automaatselt, tuginedes kvaliteedijuhistele.
-   Saate määrata kvaliteedijuhised igas äriprotsessis ostu, vahelao, tootmistellimuste või müügitellimustega seotud kvaliteettellimuse automaatseks loomiseks, määratledes sissetuleva või väljamineva materjali testimisnõuded.
-   Saate talletada testitulemused kvaliteettellimuses, kontrollida testitulemusi vastuvõetavate kvaliteeditasemete suhtes ning printida testitulemusi kajastava analüüsitunnistuse.

## <a name="nonconformance"></a>Mittevastavus
Mittevastavus kirjeldab kaupa, millel on kvaliteediprobleem. Mittevastavuse protsess võimaldab luua mittevastavuse tellimuse, milles on toodud mittevastava materjali kogus, probleemne allikas, probleem tüüp ja selgitavad märkused. Saate määratleda probleemi tüüpide klassifikatsiooni, et mittevastavat materjali oleks hõlpsam analüüsida. Saate printida ka mittevastavuse sildi ja mittevastavuse aruande, et juhtida mittevastava materjali likvideerimist. Näiteks võib sildil ja aruandel olla näidatud olek **Kasutuskõlbmatu** või **Piiratud kasutus**.

Järgmises tabelis loetletakse kuus mittevastavuse vaiketüüpi ja kirjeldatakse teavet, mis tuleb iga tüübi puhul salvestada.

| Mittevastavuse tüüp   | Allika teave                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klient              | Kliendikood, müügitellimuse number või müügitellimuse kande saatepartii number. Näiteks võib mittevastavus olla seotud kindla müügitellimuse saadetisega või kliendi tagasisidega toote kvaliteedi kohta.       |
| Teenuse päring       | Kliendikood, müügitellimuse number või müügitellimuse kande saatepartii number. Näiteks võib mittevastavus olla seotud kindla müügitellimuse saadetisega või kliendi kaebusega kauba kvaliteedi kohta.     |
| Hankija                | Hankija konto number, ostutellimuse number või ostutellimuse kande saatepartii number. Näiteks võib mittevastavus olla seotud ostutellimuse sissetulekuga või tarnija murega osa pärast, mida ta pakub. |
| Tootmine            | Tootmistellimuse number või tootmistellimuse kande saatepartii number. Näiteks võib mittevastavus olla seotud kindla partiiga, mis toodeti.                                                                      |
| Sisemine              | Kvaliteettellimuse number või kvaliteettellimuse kande saatepartii number. Näiteks võib mittevastavus olla seotud testidega, mida kvaliteettellimuse osana tehakse, või töötaja murega toote kvaliteedi pärast.     |
| Kaastoote tootmine | Kõrvalsaaduse tootmistellimuse mittevastavus, mis on seotud tootmistellimuste partiiga.                                                                                                                                                    |

Mittevastavused seostatakse probleemi tüübiga. Probleemi tüübid on määratletud lehel **Probleemi tüübid**, kus saate määrata, milliseid probleemi tüüpe saab iga mittevastavuse tüübiga seostada. Näiteks probleemi tüübid mittevastavuse tüübi **Hooldustaotlus** puhul võivad kajastada kliendikaebuste klassifikatsiooni, samas kui mittevastavuse tüübi **Sisemine** puhul võivad probleemi tüübid kajastada defektikoodide klassifikatsiooni.

Kui loote uue mittevastavuse, tuleb valida mittevastavuse tüüp ja probleemi tüüp. Esialgne kinnitamise olek on **Uus**, mis näitab, et see nõuab tegevust. Järgmine samm on määrata kinnitamise olekuks **Kinnitatud** või **Keeldutud**, mis näitab, kas reageerite mittevastavusele või mitte. Saate mittevastavuse ka sulgeda (märkides eraldi ruudu), mis näitab, et olete tegevuse sellega lõpetanud, või saate mittevastavuse uuesti avada, mis näitab, et on vajalikud täiendavad kaalutlused.

Saate sisestada mittevastavuse kohta kommentaare, lisades dokumendi. On mõistlik määrata mittevastavustele kordumatu dokumenditüüp, kasutades lehte **Dokumenditüüp**. Seejärel saate määratleda lehel **Aruande seadistus**, kas printida mittevastavuse aruande ja mittevastavuse sildi kommentaarid selle dokumenditüübi puhul. Mittevastavuse aruanne ja mittevastavuse silt võivad olla abiks materjali likvideerimisel. Saate valikuliselt luua aruandeid ja silte, mis põhinevad mittevastavusega seotud valikukriteeriumidel. Nende kriteeriumide hulka kuuluvad mittevastavuse number, kaup, klient, hankija ja olek.

Mittevastavuse aruanne kuvab mittevastavuse numbri, kauba ja probleemitüübi. Olenevalt teie aruande seadistuspoliitikast võib aruanne kuvada ka seotud märkusi mittevastavuse kohta. Mittevastavuse silt kuvab sarnast teavet ja sisaldab ka vahelao tsooni ja tüüpi (nt **Piiratud kasutus** või **Kasutuskõlbmatu**), mille määrasite mittevastavusele, et aidata juhtida praakmaterjalide likvideerimist.

## <a name="approved-nonconformance"></a>Kinnitatud mittevastavus
Võite kinnitatud mittevastavusele valikuliselt määrata ühe või mitu seotud operatsiooni. Seotud toiming kirjeldab tööd, mis tuleks teha, ja sisaldab loendit teie määratletud kvaliteeditoimingutest ja töö põhjust kirjeldavat teksti. Pärast operatsiooni määratlemist saate valikuliselt määrata lisakulud, kaubad ja töötundide ajatabeli, mida on töö tegemiseks vaja. Näidatakse seotud operatsiooni arvutatud kulusid ja mittevastavuse kõiki arvutatud kulusid. Arvutatud kulud ja aluseksolevad üksikasjad (kauba, töötundide ja lisakulude kohta) kajastavad viiteteavet ja neid kasutatakse ainult kvaliteedihalduse funktsioonis.

Võite valikuliselt luua mittevastavusest kvaliteettellimuse, tehes kõigepealt päringu kvaliteettellimuste kohta ja luues seejärel uue kvaliteettellimuse. Näiteks võiv kvaliteettellimus tuvastada vajaduse testida (või uuesti testida) praakmaterjali. Äsja loodud kvaliteettellimus näitab seost algse mittevastavusega.

Võite soovi korral siduda ühe mittevastavuse teisega ja luua olemasolevast mittevastavusest uue. Seos võib peegeldada näiteks vastastikust seost kvaliteediprobleemide vahel.

## <a name="correction-handling"></a>Paranduste käsitlemine
Lehel **Parandused** saate luua loendi mittevastavustest, mis tuleb parandada. Iga parandatav kaup seostatakse diagnostika tüübiga, mis tuvastatava probleemi põhjustas. Leht **Parandused** sisaldab teavet ka selle kohta, kes parandustoimingu peab tegema ja millal. Saate kirjeldada probleemi üksikasju ja vajalikku parandustoimingut, lisades parandusele dokumendi. Pärast mittevastavusega tegelemist või selle kõrvaldamist saate parandusüksuse „sulgeda”, tehes valiku **Lõpetatud**. Saate ka näidata, et lahendus oli lühiajaline lahendus.

On mõistlik määrata parandustele kordumatu dokumenditüüp, kasutades lehte **Dokumenditüüp**. Seejärel saate määratleda lehel **Aruande seadistus**, kas printida selle dokumenditüübi puhul kommentaarid paranduste aruandele. Prinditud paranduste aruandel on teave mittevastavuse kohta ja mittevastavusega seotud märkused. Aruanne sisaldab ka paranduse teavet nagu diagnostika tüüp ja seotud paranduse märkused.

<a name="additional-resources"></a>Lisaressursid
--------

[Kvaliteedijuhtimise ülevaade](enable-quality-management.md)

[Mittevastavuse haldus](enable-nonconformance-management.md)

[Varude blokeerimine](inventory-blocking.md)

[Vahelaoorderid](quarantine-orders.md)

[Kvaliteettellimuste seadistamine](tasks/set-up-quality-orders.md)

[Kaupade kvaliteedi kontrollimine](tasks/inspect-quality-goods.md)
