---
title: Kaubanduse pisikulude kassa haldus Ida-Euroopa puhul
description: See teema kirjeldab, kuidas seadistada ja kasutada kaubanduse kassahalduse funktsiooni Ida-Euroopas.
author: epopov
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9305e7143bc0a978569d51544a1ae65ee57b3243
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798816"
---
# <a name="petty-cash-management-for-commerce-for-eastern-europe"></a>Kaubanduse pisikulude kassa haldus Ida-Euroopa puhul

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse Ida-Euroopa kaubandusega seotud lokaliseerimist.

Ida-Euroopa raamatupidamise nõuete järgi saate seadistada sularahakontode operatsioonid, et automatiseerida sissetulekute, kassdokumentide ja sularahaaruannetega seotud protsesse. Lisateabe saamiseks avage [(EEUR) Kassahalduse parameetrite seadistamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).

Jaemüüjad võivad võtta müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega. Kuigi levinuim maksemeetod on sularaha, võivad jaemüüjad võtta tasu ka tšekkide, kaartide või kannetega. Kassas käideldakse sularaha, krediitkaardimakseid ja muid maksemeetodeid rahakäitlusüksuse kaudu.

Kassahaldusega saate kaubanduses teha järgmist:

- luua iga kaupluse jaoks valitud maksemeetodile sularahakonto,
- kasutada jaemüügikassas tehtud sularahatehingute ja kliendimaksete sisestamiseks kassatöölehti,
- koondada väljavõtte sisestamisel kanded väljavõtte reale. Saate koondada seifi viidava raha, panka viidava raha, kandetehingud, eemaldada maksevahendi kandeid, sularaha kirje kandeid, tulu kandeid, kulu kandeid, kliendimakseid, müügitehinguid ja tagastuskandeid.

Kõik kassas tehtavad kanded sisestatakse pearaamatu töölehte kasutades. Kannete loomiseks ja sisestamiseks saate kasutada sularahamaksete töölehti, kliendimaksete töölehti ja üldtöölehti. Lisateabe saamiseks avage [Kaupluse aruannete loomine, arvutamine ja sisestamine](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).

Tegumirea **Sisestatud väljavõtete** lehel saate teha järgmist.

- Väljavõttega seotud sularahamaksete töölehtede avamiseks valige **Päringu \> Sularahamaksete tööleht**.
- Väljavõttega seotud pearaamatu töölehtede (v.a kliendimaksed ja sularahamaksed) avamiseks valige **Päringud \> Päevaraamat**.

## <a name="set-up-for-cash-management-for-pos"></a>Kassahalduse seadistamine

Enne sularahahalduse kasutamist peate lõpule viima järgmise seadistusprotseduuri.

- Seadistage **Makseviiside** lehel igale jaemüüja aktsepteeritavale maksetüübile makseviis. Saate kassa kannete sisestamiseks kasutada erinevaid makseviise. Makseviiside kohta lisateabe saamiseks vt [Makseviise](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).
- Parameetrite seadistamine kassatoimingute jaoks.
- Kaupluse sularahamaksete maksemeetodi seadistamine.

### <a name="set-up-parameters-for-cash-operations"></a>Parameetrite seadistamine kassatoimingute jaoks

Saate seadistada parameetreid kaubanduse funktsiooniga sularahakannete loomiseks ja sisestamiseks. Kassas saate müügikannete ja maksekannete sisestamiseks kasutada rakenduse sularahamaksete töölehti, kliendimaksete töölehti ja üldtöölehti. Väljavõtte sisestamisel saate ühendada samade atribuutidega kanded.

1. Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Klõpsake vasakul paanil nuppu **Sisestamine**.
2. Määrake **Sisestamise** alal **Kogumi** kiirkaardil **Väljamakse-/vahetusraha** olekuks **Jah**, et koondada väljavõtte sisestamisel kokku väljavõtte reaga seotud väljamakse kanded ja vahetusraha kanded.  Maksevahendi eemaldamise kanne luuakse, kui võtate sularaha kassast välja. Vahetusraha kirje kanne luuakse, kui panete kassasse sularaha.
3. Aktiveerige alltoodud parameetrid, et koondada väljavõtte sisestamisel väljavõttereaga seotud kanded.

    - **Raha hoiustamine panka** – pangakannete koondamine.
    - **Seifi viidav raha** – seifikannete koondamine.
    - **Tulu/kulu kanded** – tulu- või kulukannete koondamine.
    - **Kupongi kanded** – kupongi kannete koondamine.
    - **Kliendi maksed** – kliendimaksete koondamine.
    - **Müügid ja tagastusted** – müükide ja tagastuste kanded.

4. Määrake **Maksete** kiirkaardil töölehe vaikenimi järgmistele valikutele.

    - **Kliendimaksete tööleht** – seda töölehte kasutatakse kliendimaksete sisestamiseks.
    - **Sularahamaksete tööleht** – seda töölehte kasutatakse sularahamaksete sisestamiseks.
    - **Päevaraamat** – seda töölehte kasutatakse kannete (v.a kliendimaksete ja sularahamaksete) sisestamiseks.

### <a name="set-up-a-payment-method-for-cash-payments-in-a-store"></a>Kaupluse sularahamaksete maksemeetodi seadistamine

Kaupluses sularahamaksete kasutamiseks maksemeetodi häälestamiseks tehke järgmist.

1. Minge jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kauplused \> Kõik kauplused**.
2. Valige **Kõigi kaupluste** loendi lehel kauplus, mille jaoks maksemeetodit seadistate.
3. Klõpsake tegumiriba vahekaardil **Seadista** grupis **Seadistus** valikut **Maksemeetodid**.
4. Looge või määrake **Maksemeetodi** lehel maksemeetod.
5. Valige **Sisestamise** kiirkaardil **Konto** väljagrupis **Kontotüübi** väljal **Sularahakonto**.

    > [!NOTE]
    > Saate **Konto tüübi** väljal **Sularahakonto** valida ainult siis, kui valite **Funktsiooni** väljal valiku **Tavaline** või **Väljamakse-/vahetusraha**.

6. Valige **Kontonumbri** väljal maksemeetodi sularahakonto number.
7. Valige **Väljamakse-/vahetusraha** väljagrupis **Vastaskonto** väljal vastaskonto, millele sisestada maksemeetodi väljamakse või vahetusraha kanded.

> [!NOTE]
> Kauplusele tuleb seadistada vastaskontod nii sularaha maksemeetodi jaoks kui ka väljamakse või vahetusraha maksemeetodi jaoks. See loob tasakaalus pearaamatu sissekanded maksemeetodi väljamakse või vahetusraha kannetele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]