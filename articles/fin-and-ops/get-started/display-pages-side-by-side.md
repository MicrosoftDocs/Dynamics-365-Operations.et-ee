---
title: Lehtede kuvamine kõrvuti, kasutades funktsiooni Ava uues aknas
description: Selles artiklis selgitatakse, kuidas kuvada rakenduses Microsoft Dynamics 365 for Finance and Operations lehti kõrvuti.
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9b091735a4971446c5b5d0e054076260040683
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558948"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>Lehtede kuvamine kõrvuti, kasutades ikooni Ava uue akna funktsioonis

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas kuvada rakenduses Microsoft Dynamics 365 for Finance and Operations lehti kõrvuti.

Microsoft Dynamics 365 for Finance and Operations aitab teil ülesandeid tõhusamalt täita. Mõnikord võib ülesannete kiireks lahendamiseks olla vaja mitut lehte kõrvuti vaadata. Näiteks võite soovida kontrollida või sisestada ridu mitmele töölehele. Tavaliselt on selleks vaja liikuda edasi-tagasi töölehtede loendis kuvatud lehe ja antud töölehe ridu kuvava lehe vahel. Kuid funktsioon **Ava uues aknas** võimaldab kuvada need lehed kõrvuti, et saaksite oma toiminguid kiiresti teha.

Jätkates ülal nimetatud näitega, võite ridu vaadates klõpsata ikooni **Ava uues aknas**.

[![ikoon-ava-uues-aknas](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Kui klõpsate ikooni **Ava uues aknas**, avaneb ridade leht uues hüpikbrauseris ja seejärel naaseb algne brauser lehele, millel oli kuvatud töölehtede loend. Seejärel saate kuvada mõlemad lehed kõrvuti. Kui olete töölehe vaatamise lõpetanud, saate muuta valitud töölehte töölehtede loendilehel ja ridade lehel hüpikaknas kuvatakse automaatselt uue valitud töölehe read.

[![lehtede-kuvamine-kõrvuti](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dünaamiline sidumine ja värskendamine toimub neid lehti toetavate andmete vahelise seose abil. Kui süsteem pole andmete vahelisest seosest teadlik, ei värskendata hüpikakent automaatselt, kui muuta akent, millest see pärines.

Mõnel lehel on mitu vaadet: näiteks ruudustiku vaade, päise vaade ja üksikasjade vaade. Ikoon **Ava uues aknas** põhjustab kogu lehe avamise uues brauseris. Seetõttu ei saa funktsiooniga **Ava uues aknas** sama lehe kahte vaadet kõrvuti hoida. Kuid peaaegu kõigil sellistel lehtedel on navigeerimisloend, mida võite kirjete vahetamiseks kasutada ja saada samasuguse kogemuse.

Enne funktsiooni **Ava uues aknas** kasutamist tuleb konfigureerida brauseri hüpikakende blokeerija nii, et see lubaks hüpikaknaid Finance and Operationsi saidi URL-ilt. Näiteks võib lubada hüpikaknad saidilt \*.dynamics.com.

Funktsioon **Ava uues aknas** on saadaval ainult siis, kui aknas on avatud mitu lehte. Samuti suletakse hüpikaken automaatselt, kui rohkem lehti pole avatud (st akna viimase lehe sulgemisel). Finance and Operations suleb avatud lehed ka siis, kui lähete rakenduses teisele alale. Seetõttu, kui teil on hüpikaknad avatud ja lähete rakenduses teisele alale, suletakse hüpikaknad automaatselt, kuna süsteem sulges nendes akendes olevad lehed.

Hüpikakende ülaribal on kuvatud teave ettevõtte kohta, mille all leht avati, ja see on kirjutuskaitstud. Hüpikaknad sõltuvad ka Finance and Operationsi peamisest brauseriaknast. Kui peamine aken suletakse või seda värskendatakse, muutuvad kõik hüpikaknad kirjutuskaitstuks. See tähendab, et saate neis akendes siiski teavet vaadata, kuid ei saa sellega midagi teha.
