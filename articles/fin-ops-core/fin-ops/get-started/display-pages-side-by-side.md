---
title: Lehtede kõrvuti kuvamine, kasutades uue akna funktsioonis nuppu „Ava“
description: Selles artiklis selgitatakse, kuidas kuvada lehti kõrvuti.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf77e488b60cc4c526398db494104c31b0f210b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570941"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Lehtede kõrvuti kuvamine, kasutades uue akna funktsioonis nuppu „Ava“

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas kuvada lehti kõrvuti.

Mõnikord võib ülesannete kiireks lahendamiseks olla vaja mitut lehte kõrvuti vaadata. Näiteks võite soovida kontrollida või sisestada ridu mitmele töölehele. Tavaliselt on rohkem kui ühel töölehel ridade kinnitamiseks või sisestamiseks vaja liikuda edasi-tagasi töölehtede loendis kuvatud lehe ja antud töölehe ridu kuvava lehe vahel. Kuid funktsioon **Ava uues aknas** võimaldab kuvada need lehed kõrvuti, et saaksite oma toiminguid kiiresti teha.

Jätkates ülal nimetatud näitega, võite ridu vaadates klõpsata ikooni **Ava uues aknas**.

[![Klõpsake ikooni Ava uues aknas.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Kui klõpsate ikooni **Ava uues aknas**, avaneb ridade leht uues hüpikbrauseris ja seejärel naaseb algne brauser lehele, millel oli kuvatud töölehtede loend. Seejärel saate kuvada mõlemad lehed kõrvuti. Pärast töölehe vaatamist saate muuta valitud töölehte töölehtede loendilehel ja ridade lehel hüpikaknas kuvatakse automaatselt uue valitud töölehe read.

[![Saate kuvada lehed kõrvuti.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dünaamiline sidumine ja värskendamine toimub neid lehti toetavate andmete vahelise seose abil. Kui süsteem pole andmete vahelisest seosest teadlik, ei värskendata hüpikakent automaatselt, kui muuta akent, millest see pärines.

Mõnel lehel on mitu vaadet: näiteks ruudustiku vaade, päise vaade ja üksikasjade vaade. Ikoon **Ava uues aknas** põhjustab kogu lehe avamise uues brauseriaknas. Seetõttu ei saa funktsiooniga **Ava uues aknas** sama lehe kahte vaadet kõrvuti hoida. Peaaegu kõigil sellistel lehtedel on navigeerimisloend, mida võite kirjete vahetamiseks kasutada ja saada samasuguse kogemuse.

Enne funktsiooni **Ava uues aknas** kasutamist tuleb konfigureerida brauseri hüpikakende blokeerija nii, et see lubaks hüpikaknaid saidi URL-ilt. Näiteks võib lubada hüpikaknad saidilt \*.dynamics.com.

Funktsioon **Ava uues aknas** on saadaval ainult siis, kui aknas on avatud mitu lehte. Samuti suletakse hüpikaken automaatselt, kui rohkem lehti pole avatud (st selle akna viimase lehe sulgemisel). Süsteem suleb avatud lehed ka siis, kui lähete rakenduses teisele alale. Seetõttu, kui teil on hüpikaknad avatud ja lähete rakenduses teisele alale, sulguvad hüpikaknad automaatselt, kuna süsteem sulges nendes akendes olevad lehed.

Hüpikakende ülaribal on kuvatud teave ettevõtte kohta, mille all leht avati, ja see on kirjutuskaitstud. Hüpikaknad sõltuvad ka peamisest brauseriaknast. Kui peamine aken suletakse või seda värskendatakse, muutuvad kõik hüpikaknad kirjutuskaitstuks. Selle olukorra ilmnemisel saate neis akendes siiski teavet vaadata, kuid ei saa sellega midagi teha.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]