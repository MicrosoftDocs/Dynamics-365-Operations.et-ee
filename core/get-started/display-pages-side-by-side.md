---
title: "Lehtede kuvamine kõrvuti, kasutades ikooni Ava uues aknas"
description: "Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 for Operationsis lehti kõrvuti kuvada."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 940d086f9c99af54bfcc7911ee7272f9eccba464
ms.lasthandoff: 03/31/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Lehtede kuvamine kõrvuti, kasutades ikooni Ava uues aknas

Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 for Operationsis lehti kõrvuti kuvada.

Microsoft Dynamics 365 for Operations aitab tõhusalt ülesandeid täita. Mõnikord võib ülesannete kiireks lahendamiseks olla vaja mitut lehte kõrvuti vaadata. Näiteks võite soovida kontrollida või sisestada ridu mitmele töölehele. Tavaliselt on selleks vaja liikuda edasi-tagasi töölehtede loendis kuvatud lehe ja antud töölehe ridu kuvava lehe vahel. Kuid funktsioon **Ava uues aknas** võimaldab kuvada need lehed kõrvuti, et saaksite oma toiminguid kiiresti teha. Jätkates ülal nimetatud näitega, võite ridu vaadates klõpsata ikooni **Ava uues aknas**. [![avatud-on-uus-aken-ikoon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) käsku ning **Ava uues aknas** ikooni avab ridade lehe brauseris uus, hüpikakende ja seejärel viib originaal brauseri ajaloos tagasi lehele, mida kuvatakse töölehtede loendi. Seejärel saate kuvada mõlemad lehed kõrvuti. Kui olete töölehe vaatamise lõpetanud, saate muuta valitud töölehte töölehtede loendilehel ja ridade lehel hüpikaknas kuvatakse automaatselt uue valitud töölehe read. [![lehed-Näita-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) Dünaamiline linkimine ja värskendav juhtub tõttu andmeid, mis on toetus külastamine vahelisi suhteid. Kui süsteem pole andmete vahelisest seosest teadlik, ei värskendata hüpikakent automaatselt, kui muuta akent, millest see pärines. Mõnel lehel on mitu vaadet: näiteks ruudustiku vaade, päise vaade ja üksikasjade vaade. Ikoon **Ava uues aknas** põhjustab kogu lehe avamise uues brauseris. Seetõttu ei saa funktsiooniga **Ava uues aknas** sama lehe kahte vaadet kõrvuti hoida. Kuid peaaegu kõigil sellistel lehtedel on navigeerimisloend, mida võite kirjete vahetamiseks kasutada ja saada samasuguse kogemuse. Enne funktsiooni **Ava uues aknas** kasutamist tuleb konfigureerida brauseri hüpikakende blokeerija nii, et see lubaks hüpikaknaid Dynamics 365 for Operationsi saidi URL-ilt. Näiteks võib lubada hüpikud saidilt "\*. dynamics.com". Funktsioon **Ava uues aknas** on saadaval ainult siis, kui aknas on avatud mitu lehte. Samuti suletakse hüpikaken automaatselt, kui rohkem lehti pole avatud (st akna viimase lehe sulgemisel). Dynamics 365 for Operations suleb avatud lehed ka siis, kui lähete rakenduses teisele alale. Seetõttu, kui teil on hüpikaknad avatud ja lähete rakenduses teisele alale, suletakse hüpikaknad automaatselt, kuna süsteem sulges nendes akendes olevad lehed. Hüpikakende ülaribal on kuvatud teave ettevõtte kohta, mille all leht avati, ja see on kirjutuskaitstud. Hüpikaknad sõltuvad ka Dynamics 365 for Operationsi peamisest brauseriaknast. Kui peamine aken suletakse või seda värskendatakse, muutuvad kõik hüpikaknad kirjutuskaitstuks. See tähendab, et saate neis akendes siiski teavet vaadata, kuid ei saa sellega midagi teha.


