---
title: Hankekataloogid
description: See artikkel kirjeldab kõrgel tasemel, kuidas ostuspetsialistid saavad hankekatalooge seadistada ja hallata. Hankekataloogid määratlevad kaubad ja teenused, mida ettevõtte töötajad saavad ettevõttesiseseks kasutamiseks tellida.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f49c25e8d653219c9a2e5bead0c25f09898e27b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "358412"
---
# <a name="procurement-catalogs"></a>Hankekataloogid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab kõrgel tasemel, kuidas ostuspetsialistid saavad hankekatalooge seadistada ja hallata. Hankekataloogid määratlevad kaubad ja teenused, mida ettevõtte töötajad saavad ettevõttesiseseks kasutamiseks tellida.

Ostuspetsialistid saavad luua ja hallata katalooge kaupade ja teenuste kohta, mida saab osta organisatsioonisiseseks kasutamiseks. Kui kataloogid on seadistatud, saavad ettevõtte töötajad luua ostutaotlusi nende tellimiseks. Kataloogide abil saab jõustada ostupoliitikaid, nii et töötajad saavad tellida ainult neid kaupu ja teenuseid, mis on nende ostva juriidilise isiku jaoks lubatud. Hankekataloogi loomisel peate täitma järgmised ülesanded.

-   Konfigureerige enne kataloogi loomist hankekategooria hierarhia.
-   Töötajatele tellimiseks saadaolevate toodete määratlemine. Saate kataloogisõlmes kuvada või peita konkreetsed tooted või kõik tooted.
-   Hankekataloogide vajaliku arvu määratlemine. Juurdepääsu hankekataloogile määratleb kataloogi poliitikareegel, mille peate konfigureerima juriidilisele isikule ja tootmisüksusele, kuhu töötaja on määratud.

Tooteid, mida töötajad saavad tellida, ja hankekatalooge, mida nad saavad ostutaotluste loomisel kasutada, määratakse mitme teguriga.

-   Kategooria juurdepääsupoliitika reegel ostupoliitikas määrab, millised hankekategooriad on ostutaotluses saadaval. Kui ühtki reeglit pole määratletud, on saadaval kõik hankekategooriad.
-   Töötajad saavad toodet tellida ainult siis, kui see on teie organisatsiooni aktiivses hankekataloogis, asub lubatud sõlmes ja pole peidetud. Tood peab olema ka kategoorias, millele konkreetsel töötajal on kategooria juurdepääsupoliitika reegli alusel juurdepääs.
-   Kataloogi poliitika reegel määrab kasutatava kataloogi. Kui kataloogi poliitika reegel on määratlemata, määrab ainult kategooria juurdepääsureegel need tooted, mida töötaja saab taotluses tellida.

## <a name="prerequisites"></a>Eeltingimused 
Järgmises tabelis kirjeldatakse ülesandeid, mis tuleb täita, enne kui ostuspetsialist saab hankekataloogi luua.

| Ülesanne                                                | Roll               | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hankekategooria hierarhia seadistamine.            | Ostujuht | Hankekategooria hierarhia liigitab tooteid või kandeid aruandluse ja analüüsi jaoks. Hankekategooria hierarhia abil saavad ettevõtted kategooriad, tooteid, hankijaid ja muid hanketegureid kesksest asukohast strateegiliselt hallata. Kogu organisatsioonile määratletakse üks aktiivne hankekategooria hierarhia. Kataloogi aluseks on hankekategooria hierarhia: hierarhia kategooriad muutuvad kataloogi sõlmedeks. Hankijad ja tooted kaasatakse teie kataloogi. |
| Hankijate ja toodete lisamine hankekategooriatesse. | Ostujuht | Kui teie organisatsiooni jaoks on hankekategooria hierarhia loodud, saab iga hankekategooria seostada kindlate hankijate, toodetega jne. Need seosed kopeeritakse automaatselt kataloogi.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Kataloogi seadistamine
Katalooge saate seadistada, kui eeltingimused on täidetud. Saate luua ühe kataloogi, mida kasutab kogu ettevõte, või mitu kataloogi, mida kasutavad organisatsiooni erinevad osakonnad. Kui loote ühe kataloogi kogu organisatsiooni jaoks, juhivad juurdepääsu kataloogile ostupoliitika reeglid.  

Kataloog määratleb, millised tooted on ostutaotluste loomisel saadaval, kuid saate kategooria juurdepääsupoliitika reeglitega rakendada täiendavaid piiranguid. Kuna kataloogi sõlmed on hankekategooriad, saab juurdepääsu neile keelata kategooria juurdepääsupoliitika reegli abil. Sellisel juhul pole selles kategoorias olevad tooted töötajatele taotlustel kasutamiseks saadaval. Kategooria juurdepääsupoliitika reeglid saate määratleda lehel **Ostupoliitikad**. Järgmises tabelis kirjeldatakse ülesandeid, mis tuleb kataloogi seadistamiseks täita.

| Ülesanne                                                   | Roll             | Kirjeldus                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uue kataloogi loomine.                                  | Ostuagent | Kataloogi loomisel peate määrama selle nime ja kirjelduse. Saate ka määratleda, kas kataloogi värskendatakse käsitsi või automaatselt, ja määrata kataloogi omaniku.                                                                                                                                      |
| Saate määrata, kas tooted on kataloogis saadaval. | Ostuagent | Kuna tooted päritakse hankekategooriatest, kuvatakse need kõik asjakohastes kataloogisõlmedes. Saate määrata, kas kõik sõlmes olevad tooted on peidetud või kuvatud, kui kataloogi kasutatakse ostutaotlusel. Samuti saate määrata, kas üksikud tooted sõlmes on peidetud või kuvatud. |
| Kataloogi avaldamine.                                   | Ostuagent | Enne kui kataloog on töötajatele taotluses kasutamiseks saadaval, peate määratlema kataloogi poliitikareegli, määrama kataloogi olekuks **Aktiivne** ja kataloogi avaldama. Saate inaktiveerida kataloogid, mida ei soovi oma kasutajatele enam kättesaadavaks teha.                                              |

Värskendusi saab avaldada kas automaatselt või käsitsi olenevalt sellest, millise suvandi valite lehe **Kataloogid** väljal **Värskenduse vaiketüüp**. Kataloogide jaoks on saadaval on järgmised värskenduse vaiketüübid.

-   **Dünaamiline** – kataloogi värskendatakse automaatselt iga kord, kui seda muudetakse.
-   **Staatiline** – katalooge tuleb käsitsi värskendada.
-   **Mõlemad** – kui kataloog sisaldab tootekategooriat, mille värskenduse vaiketüüp on **Staatiline**, tuleb seda kataloogide värskendamisel käsitsi värskendada. Kui kataloog sisaldab tootekategooriaid, mille värskenduse vaiketüüp on **Dünaamiline**, toimub värskendamine automaatselt iga kord, kui seda muudetakse.


<a name="additional-resources"></a>Lisaressursid
--------

[Hankekategooria hierarhia seadistamine (tegevuse juhis)](tasks/set-up-procurement-category-hierarchy.md)



