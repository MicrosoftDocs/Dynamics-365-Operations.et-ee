---
title: Hoolduseelarvete värskendamine
description: Selles teemas selgitatakse, kuidas luua värskendada hoolduseelarvet varahalduses.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87c054cb96d56e40e35ee44142396f59d61395263ff41232423f6c7911478b0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724936"
---
# <a name="update-maintenance-budgets"></a>Hoolduseelarvete värskendamine

[!include [banner](../../includes/banner.md)]

 

Lehel **hoolduse eelarve read** kuvatakse kõik eelarveread, mis on loodud eelarve jaoks, mis on valitud lehel **Hoolduse eelarved**. (Lisateavet vt teemast [Loo hoolduse eelarved](create-maintenance-budget.md).) Hoolduse eelarve ridu saate ümber arvutada ja korrigeerida, kuni hoolduse eelarve on kinnitatud. Pärast eelarveperioodi möödumist ja vara haldusse sisestatud kulude sisestamist saate eelarve ridu ka tegelike kuludega värskendada.

## <a name="recalculate-a-maintenance-budget"></a>Hoolduse eelarve ümberarvutamine

Hoolduse eelarvet saate ümber arvutada lehel **Hoolduse eelarve read**. Hoolduse eelarve ümberarvutamisel kustutatakse olemasolevad eelarveread ja tehakse uus arvutus.

1. Lehel **Hoolduse eelarve read** valige **Arvuta ümber**.
2. Dialoogiaknas **Arvuta eelarve ümber** tehke uue arvutuse jaoks vajalikud muudatused ja seejärel valige **OK**.

Uued eelarveread luuakse vastavalt teie määratud väärtustele.

## <a name="adjust-budget-lines"></a>Kohanda eelarveridu

Kogu hoolduse eelarve ümberarvutamise asemel saate korrigeerida valitud ridu, mis on seotud eelarve kuludega.

1. Valige lehel **Hoolduse eelarve read** read, mille jaoks eelarve kulu värskendada.
2. Valige **Kohanda**.
3. Summa lisamiseks valitud ridadele valige märkekast **Lisa kulu** ja sisestage väärtus väljale **Lisa väärtus**.
4. Et korrutada eelarve kulu valitud eelarveridadele teguriga, märkige ruut **Korruta kulu** ja sisestage tegur väljale **Korruta väärtus**.

    Näiteks kui sisestate **1,2** väljale **Korruta väärtus**, suurendate eelarve kulu valitud ridadel 20 protsendi võrra. Kui sisestate **0,7**, vähendate eelarve kulu valitud ridadel 30 protsendi võrra.

5. Valige nupp **OK**.

Valitud eelarve ridu värskendatakse vastavalt väärtustele, mille seate sammus 3 või 4.

## <a name="update-actual-costs"></a>Tegelike kulude värskendamine

Pärast eelarveridade kuupäevade möödumist ja varahaldusse tegelike kulude sisestamist saate hoolduse eelarvet tegelike kuludega värskendada.

1. Lehel **Hoolduse eelarve read** valige **Värskenda kulu**.
2. Dialoogiaknas **Arvuta tegelik kulu** valige **OK**.

Eelarveridade väljad **Tegelik kulu** värskendatakse, kui eelarveridade tegelik kulu on sisestatud. Uued eelarveread võidakse luua, kui uute varade tüübid on loodud eelarve loomisest saadik ja kui neid varatüüpe on kasutatud varade puhul, mille jaoks on loodud töökäsud ja seotud kulud on sisestatud. Uued eelarveread näitavad ainult tegelikke kulusid, kuna nende jaoks ei arvutatud eelarve kulusid.

> [!NOTE]
> Et näha ülevaadet tegelikest kuludest, mis on jagatud ennetus-, parandus- ja investeerimiskuludeks, saate teha arvutuse sama perioodi kohta, mis on esitatud lehel **Vara kulude kontroll**. 

## <a name="manually-add-budget-lines"></a>Eelarveridade käsitsi lisamine

Lehel **Hoolduse eelarveread** saate uue eelarverea käsitsi lisada, valides **Uus** ja seejärel tehes tehes valikud real. Siin on mõned näited olukordadest, kus selline lähenemine võib olla kasulik:

- Te teate, et mõnede varade renoveerimine on praegu planeerimise faasis, kuid seotud tööd pole veel varahalduses loodud. Siiski soovite nende tööde eelarvete kulusid kaasata hoolduse eelarvesse.
- Pärast hoolduse eelarvet on loodud uusi varasid või varatüüpe, kuid hoolduse plaane pole nende varade või varatüüpide puhul veel seadistatud. Siiski soovite nende varatüüpide eelarvete kulusid kaasata hoolduse eelarvesse.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]