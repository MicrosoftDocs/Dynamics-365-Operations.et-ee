---
title: Väljamineva töökoormuse visualiseerimine
description: See artikkel annab teavet väljamineva töökoormuse visualiseerimise kohta. See funktsioon võimaldab laojuhatajatel ja -ülemustel luua kohandatud töökoormusgraafikuid, mida saab kasutada praeguse töö ja selle allesjäänud osa edenemise jälgimiseks. Laojuhatajad saavad luua mitu vaadet ja häälestada vajaduse korral automaatse värskendamise.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78d0d81095bb52a314936dd7590a5690d94ecb15
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334411"
---
# <a name="outbound-workload-visualization"></a>Väljamineva töökoormuse visualiseerimine

[!include [banner](../includes/banner.md)]

Täpsemad häälestusvõimalused, mis on juurdepääsetavad lehel **Väljamineva töökoormuse visualiseerimine**, võimaldavad laojuhtidel ja -ülemustel luua kohandatud töökoormusgraafikuid, mida saab kasutada praeguse töö ja selle allesjäänud osa edenemise jälgimiseks. Laojuhatajad saavad luua mitu vaadet ja häälestada vajaduse korral automaatse värskendamise. Väljamineva töökoormuse visualiseeringud sobivad kuvamiseks laojõudluse lehtedel.

Neid funktsioone saab kasutada komplekteerimistöö edenemise jälgimiseks. Funktsioon on integreeritud tööhaldusega ja kui tööhaldus on häälestatud, võib väljamineva töökoormuse visualiseerimine näidata kuvatava (filtreeritud) komplekteerimistöö allesjäänud töötunde.

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>Väljamineva töökoormuse visualiseeringu funktsiooni sisse- või väljalülitamine

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.25 puhul lülitatakse funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumist väljamineva töökoormuse visualiseerimise*[funktsiooni](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-outbound-workload-visualizations"></a>Väljamineva töökoormuse visualiseeringute häälestamine

Visualiseeringute häälestamiseks saate luua filtrid (vaated) ja iga filtri kujundada, et see näitaks erinevat tüüpi analüüsi. Filtrite kujundamiseks kasutage lehte **Filtrite konfigureerimine**.

Väljamineva töökoormuse visualiseerimise häälestamiseks toimige järgmiselt.

1. Valige **Laohaldus \> Lao jälgimise aruanded \> Väljamineva töökoormuse visualiseerimine**.

    Kuvatakse leht **Väljamineva töökoormuse visualiseerimine**. Pärast filtrite loomist kuvatakse sellel lehel teie visualiseering. Saate luua soovitud arvu filtreid. Kõik teie loodud filtrid salvestatakse teie kasutajakontole, et saaksite neid hiljem kasutada. Teisisõnu on igal kasutajal oma loodud filtrid. Neid filtreid ei jagata teiste kasutajatega.

1. Valige lehel **Väljamineva töökoormuse visualiseerimine** vahekaardi **Filtrid** toimingupaanil **Konfigureeri filtrid**.
1. Filtri lisamiseks valige lehel **Filtrite konfigureerimine** toimingupaanil nupp **Uus** ja seejärel määrake selle jaoks järgmised väljad.

    - **X-telje grupi tabel** – valige tabel, mis sisaldab x-telje väärtuste grupeerimiseks kasutatavat välja.
    - **X-telje grupi väli** – valige väljal **X-telje grupi tabel** valitud tabeli väljade seast väli, mida X-telje väärtuste grupeerimiseks kasutatakse.
    - **X-telje väärtuse tabel** – valige tabel, sisaldab rühmade põhjalikumaks analüüsimiseks kasutatavat välja.
    - **X-telje väärtuse väli** – valige väljal **X-telje väärtuse tabel** valitud tabeli väljade seast väli, mis annab iga grupi kohta analüüsitavad väärtused.
    - **Automaatne värskendamine** – valige, kas visualiseeringut tuleks automaatselt värskendada.
    - **Värskendusintervall (minutid)** – sisestage minutite arv automaatse värskendamise vahel.
    - **Kuvamistase** – valige, kas diagramm peaks näitama avatud ridu või avatud päiste arvu.
    - **Komplekteerimistüüp** – kui määrate välja **Kuvamistase** jaoks väärtuse _Avatud read_, valige, kas diagrammi avatud tööga ridadel peaks olema algne komplekteerimine, ettevalmistav komplekteerimine või nii algne komplekteerimine kui ka ettevalmistav komplekteerimine.
    - **Sait** – valige sait, mille jaoks diagramm laadida.
    - **Ladu** – valige ladu, mille jaoks diagramm laadida.
    - **Kaasatavate päevade arv** – sisestage päevade arv minevikus, mille jaoks diagramm tuleb luua.
    - **Töökäsu tüüp** – valige väljaminevate töökäskude tüübid, mida filtreerida.

    ![Filtrite konfigureerimise leht.](media/work-viz-filters-1.png "Filtrite konfigureerimise leht")

1. Sulgege leht **Filtrite konfigureerimine**, et naasta lehele **Väljamineva töökoormuse visualiseeringud**.

    Lehel **Väljamineva töökoormuse visualiseeringud** kuvatakse nüüd uutel filtrisätetel põhinevad andmed. Uus filter on nüüd saadaval ja on valitud väljal **Filter**. Diagrammi ülaosas on saadaval järgmised väljad.

    - **Filter** – see väli sisaldab kõiki seni loodud filtreid. Valige filter, et vaadata selle andmeid diagrammis.
    - **Viimati värskendatud** – sellel väljal kuvatakse kuupäev ja kellaaeg, kui teavet diagrammis viimati värskendati.
    - **Hinnanguline/tegelik aeg** – kui teie süsteemis häälestati tööstandardid, määrake selle suvandi väärtuseks *Jah*, et kuvada diagrammi iga veeru ülaosas akumuleeritud hinnangulised komplekteerimisajad. Kui te tööstandardit ei kasuta, ei ole see suvand saadaval.

    ![Näide visualiseerimisest.](media/work-viz-chart.png "Näide visualiseerimisest")

1. Valige diagrammil mis tahes riba, et vaadata seotud töörea üksikasju.

    ![Töörea üksikasjad.](media/work-viz-work-details.png "Töörea üksikasjad")

## <a name="example-outbound-workload-visualization-for-zones"></a>Näide: väljamineva töökoormuse visualiseerimine tsoonide jaoks

Selle näite puhul häälestatakse visualiseering, mis näitab iga tsooni tööridu ja iga töörea olekut (_Avatud_, _Suletud_ või _Tühistatud_). Sellisel juhul saate häälestada filtri, millel on järgmised sätted.

- **Filtri nimi** – sisestage filtri nimi (nt _Tsoon versus töö olek_).
- **Kirjeldus** – sisestage filtri lühikirjeldus (nt _Tsoon versus töö olek_).
- **X-telje grupi tabel** – valige _asukohad._
- **X-telje grupp** – valige _tsooni ID_.
- **X-telje väärtuste tabel** – valige väärtus _Töö_, sest soovite kuvada töö tsooni kohta.
- **X-telje väärtuste väli** – valige väärtus _Töö olek_, sest soovite kuvada töö oleku.
- **Automaatne värskendamine** – valige, kas visualiseeringut tuleks automaatselt värskendada.
- **Komplekteerimistüüp** – valige väärtus _Algne komplekteerimine ja ettevalmistav komplekteerimine_, sest soovite kuvada nii algsed komplekteerimised kui ka komplekteerimised ettevalmistusaladel. Teisisõnu on vaja kaasata kõik komplekteerimistöö read, mis teil on.
- **Kuvamistase** – valige väärtus _Avatud read_, sest soovite teavet rea kohta, mitte töö päise kohta.

Järgnev illustratsioon näitab tulemuseks oleva diagrammi näidet.

![Tsooni versus töö oleku visualiseerimine.](media/work-viz-chart.png "Tsooni versus töö oleku visualiseerimine")

Sellel diagrammil kuvatakse kaks tsooni, mille nimeks on **PÕRAND** ja **HULGI**, ning tsoon, mille nimi on **Tühi**. **Tühi** tsoon tähistab kõiki tööridu, mis ei kuulu tsooni. Diagrammis kuvatakse alati kõik sõltumatud filtreeritud andmed **tühjana**, et pakkuda võimalikult palju nähtavust. Tsooni **PÕRAND** kohta kuvab diagramm kolm suletud rida ja neli avatud rida. Tsooni **HULGI** kohta kuvab diagramm neli suletud rida, ühe avatud rea ja 24 tühistatud rida. Lõpuks näitab diagramm kaheksat suletud rida, mis pole üheski tsoonis ja on seetõttu loetletud **tühjana**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]