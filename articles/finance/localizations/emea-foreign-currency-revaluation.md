---
title: Välisvaluuta ümberarvutamine pangakontode jaoks
description: See artikkel annab teavet pangakontode välisvaluuta ümberarvutamise kohta.
author: panolte
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea40312a848e6c757400ff5fb5448fb19781012f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894790"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a>Välisvaluuta ümberarvutamine pangakontode jaoks

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a>Välisvaluuta summade ümberarvutamine pangakonto kannete jaoks

> [!IMPORTANT]
> See jaotis kehtib ainult nende juriidiliste isikute puhul, kelle esmane aadress on Poolas.

Välisvaluuta summasid saate pangakonto kannete jaoks ümber arvutada. Seejärel saate luua aruande, et vaadata pangakandeid, mille puhul on tehtud välisvaluuta ümberarvutamise korrigeerimisi.

1. Valige **Sularaha- ja pangahaldus** &gt; **Perioodilised ülesanded** &gt; **Pank – vahetuskursi korrigeerimine (FIFO/LIFO)**.
2. Sisestage väljale **Kuupäeval** ümberarvutamise lõppkuupäev. Arvutamisse kaasatakse ainult kanded, mille kuupäev on varasem määratud kuupäevast.
3. Pangakonto lisamiseks valige **Kaasatavad kirjed** &gt; **Filtreeri** &gt; **Lisa**. Kui te ei määra pangakontot, hinnatakse kõikide pangakontode summad ümber.
4. Päringulehe sulgemiseks valige **OK**.
5. Kõigi avatud perioodide välisvaluuta summade ümberarvutamiseks valige lehel **Välisvaluuta ümberarvutamine** märkeruut **Ümberarvutus**.

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a>Aruande loomine, et vaadata pangakandeid, mille puhul on tehtud välisvaluuta ümberarvutamise korrigeerimisi

> [!IMPORTANT]
> See jaotis kehtib ainult nende juriidiliste isikute puhul, kelle esmane aadress on Poolas.

1. Valige **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Pank – valuutakursi korrigeerimisaruanne**.
2. Ühe või mitme pangakonto teabe vaatamiseks valige **Kaasatavad kirjed** &gt; **Filtreeri**.
3. Valikuline: valige pangakonto väljal **Pangakonto**. Kui jätate selle välja tühjaks, kaasatakse aruandesse kõigi pangakontode pangakannete üksikasjad.
4. Aruande loomiseks valige **OK**. 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a>Vahetuskursi korrigeerimiste arvutamine pangakonto kannete jaoks

> [!IMPORTANT]
> See jaotis kehtib ainult nende juriidiliste isikute puhul, kelle esmane aadress on Tšehhi Vabariigis, Eestis, Leedus või Lätis.

Teil tuleb ümber hinnata ja reguleerida pangakontosid, kui arvestusvaluuta ja aruandlusvaluuta vahetuskurss erinevad. See ülesanne aitab teil arvutada õige saldo pangakontode arvestusvaluuta ja aruandlusvaluuta jaoks.

1. Valige **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**.
2. Valige vahekaardi **Numbriseeriad** väljal **Viide** numbriseeria viitele **Pank - vahetuskursi korrigeerimine**.
3. Sulgege leht.
4. Valige **Pearaamat** &gt; **Seadistus** &gt; **Valuuta** &gt; **Valuuta vahetuskursi määrad**. Lehel **Valuuta vahetuskursi määrad** saate määrata kahe valuuta või valuutapaari vahetuskursi.
5. Kui olete lõpetanud, sulgege leht.
6. Valige **Pearaamat** &gt; **Seadistus** &gt; **Pearaamat**. Valige väljadel **Realiseerimata kasum** ja **Realiseerimata kahjum** peamine konto, mille jaoks vahetuskursse sisestate.
7. Sulgege leht.
8. Valige **Sularaha- ja pangahaldus** &gt; **Perioodilised ülesanded** &gt; **Välisvaluuta ümberarvutamine**.
9. Väljal **Kuupäeval** valige ümberarvutamise või korrigeerimise kuupäev.
10. Valige praegune valuutakood väljal **Valuutast**. Valige valuuta, millesse korrigeerimine tuleks teha, väljal **Valuutaks**.
11. Valige pangakonto leidmiseks **Kaasatavad kirjed** &gt; **Filtreeri** ja seejärel **OK**.
12. Tehke lehel **Välisvaluuta ümberarvutamine** valik **OK**. Arvutatakse valitud kuupäeva pangakonto kannete korrigeerimine.

> [!NOTE]
> Pearaamatus saate vaadata kahte eraldiseisvat kannet: üks on arvestusvaluuta ja teine aruandlusvaluuta jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]