---
title: Hooldusprognoosid
description: Selles teemas tutvustatakse hooldusprognoose varahalduses.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7976a7d555c04cb2ea01a2dbe571f6b8b440b69a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347064"
---
# <a name="maintenance-forecasts"></a>Hooldusprognoosid

[!include [banner](../../includes/banner.md)]



Kui loote töökäsu, loote töökäsu tööd, millel on seotud varad ja hooldustööde tüübid. Kui valite hooldusprognoosi sisaldava hooldustöö tüübi, kopeeritakse prognoosid automaatselt töökäsku.

Võimalik, et saate töökäsule lisada prognoosiread või need töökäsust kustutada. Töökäsu töötsükli oleku seadistus, seotud projektitüüp ja seotud projektitüübi oleku reeglid määravad ära, kas saate prognoosi ridu lisada või redigeerida. Lisateavet töökäsu elutsükli olekute ja seotud projekti etappide kohta vt teemast [Prognoosid, töökäsud ja projektid](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige loendist töökäsk ja seejärel tehke tegumiriba vahekaardi > **Töökäsk** jaotises **Projekt** valik **Prognoos**. Lehel **Töökäsu hooldusprognoos** kuvatakse töökäsu tööl valitud hooldustöö tüüpi prognoosi ridu.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Tundide prognoosi lisamine töökäsule

1. Valige lehel **Töökäsu hooldusprognoos** töökäsu töö. millel prognoos lisada.

2. Tehke uue rea loomiseks kiirkaardil **Tunnid** valik **Lisa**.

3. Valige kategooria väljal **Kategooria**.

4. Sisestage väljale **Tunnid** prognoositud tundide arv.

5. Valige real kasutatav kulu tüüp väljal **Rea atribuut**.


## <a name="add-an-items-forecast-to-a-work-order"></a>Üksuste prognoosi lisamine töökäsule

Üksuste lisamiseks töötellimuse hooldusprognoosine on kolm võimalust. Võite luua read üksustele (varuosadele), mis ei sisaldu varuosade loendis või vara koosluses (BOM), võite valida varuosi kinnitatud varuosade loendist ja võite valida üksuseid vara kooslusest.

- Valige lehel **Töökäsu hooldusprognoos** töökäsu töö. millel prognoos lisada.

- Lisage kiirkaardil **Üksused** üksused hooldusprognoosi sobiva meetodi abil.

Varuosade loendis või vara koosluses mittesisalduva varuosa jaoks uue rea loomiseks järgige järgmisi juhendeid.

1. Valige **Lisa**.
2. Valige kaup väljalt **Kaubakood**.
3. Sisestage kogus väljale **Müügikogus**.
4. Valige väljal **Ühik** koguse mõõtühik.
5. Sisestage sobivad väärtused väljadele **Omahind** ja **Valuuta**
6. Valige rea atribuut väljal **Rea atribuut**.
7. Üksuse ridadel kuvatavate mõõtude loendi muutmiseks valige **Varud** > **Kuva mõõdud**, valige mõõdud ja seejärel määrake valiku **Salvesta seadistus** väärtuseks **Jah**.

Varuosa lisamiseks heakskiidetud varuosade loendist tehke järgmist.

1. Valige **Lisa varuosad**.
2. Valige varuosa ja redigeerige vajadusel seotud teavet.
3. Valige nupp **OK**.

Üksuse lisamiseks põhivara kooslusest toimige järgmiselt.

1. Valige **Lisa koosluse üksused**.
2. Valige üksus ja redigeerige vajadusel seotud teavet.
3. Valige nupp **OK**.

Et saada ülevaadet sellest, kus varahalduses valitud real olevat kaupa kasutatakse, valige varade, hooldustöö tüübi vaikesätete, varuosade ja töökäskude puhul väärtus **Üksus, kus kasutatud**. Lisateavet selle ülevaate kohta vt teemast [Üksus, kus kasutatud](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Kuluprognoosi lisamine töökäsule

1. Valige lehel **Töökäsu hooldusprognoos** töökäsu töö. millel prognoos lisada.

2. Tehke uue rea loomiseks kiirkaardil **Kulud** valik **Lisa**.

3. Valige kategooria väljal **Kategooria**.

4. Sisestage kogus väljale **Kogus**.

5. Sisestage sobivad väärtused väljadele **Omahind**, **Müügivaluuta** ja **Müügihind**.

6. Valige real kasutatav kulu tüüp väljal **Rea atribuut**.

>[!NOTE]
>Kiirkaardil **Hooldusprognoosi kogusummad** kuvatakse ülevaade igale kiirkaardile loodud ridade arvust valitud töökäsu töö ja töökäsu jaoks. Samuti kuvatakse töökäsu töö ja töökäsu prognoositud töötundide summat.

Alloleval joonisel kuvatakse lehe **Töökäsu hooldusprognoos** näide.

![Joonis 1.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Töökäsu prognooside automaatne värskendamine

Kui tunnikulud, üksuse kulud ja kulud värskendatakse Microsoft Dynamics 365 for Finance and Operationsi muudes moodulites, võidakse varahalduse töökäskude prognoosid automaatselt värskendada nende muudatuste peegeldamiseks. See funktsioon aitab tagada, et töökäsu prognoosides kasutatakse alati uusimaid omahindu. Sarnaseid värskendusi saate teha ka [hooldustöö tüübi prognoosidele](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Valige **Varahaldus** > **Perioodiline** > **Prognoos** > **Värskenda töökäsu prognoosi**.

2. Dialoogi **Töökäsu prognoosi värskendamine** kiirkaardil **Kaasatavad kirjed** saate vajadusel lisada kindlate töökäskude ja töökäsu tööde valikud. Asjakohaste valikute tegemiseks valige **Filtreeri**.

3. Vahekaardil **Taustal käitamine** saate vastavalt vajadusele seadistada automaatse värskenduse pakett-tööna.

4. Valige **OK**, et alustada prognoosi värskendamist.


Alloleval joonisel kuvatakse dialoogi **Töökäsu prognooside värskendamine** näide.

![Joonis 2.](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]