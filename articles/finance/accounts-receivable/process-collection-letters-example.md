---
title: Protsesside kogumiskirjade näide
description: Käesolev teema peab läbima näite, mis näitab märgukirjade loomise, printimise ja sisestamise protsessi.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fb2651644efd2cadfccb91e48c34dfddc8383e1f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021412"
---
# <a name="process-collection-letters-example"></a>Protsesside kogumiskirjade näide

[!include [banner](../../includes/banner.md)]

Käesolev teema peab läbima näite, mis näitab märgukirjade loomise, printimise ja sisestamise protsessi. Näide põhineb **Krediit ja Sissenõuete märgukirjakoodi arvutamisel eira makseid** valikute krediiditeatisi. See kasutab andmeid USMF-i demoettevõttes ja uut klienti US-045.

Et alustada, minge **Müügireskontro \> Kliendid \> Kõik kliendid**, valige **Uus** ja seejärel sisestage nõutav teave kliendi loomiseks US-045.

Kui olete lõpetanud, järgige järgmisi etappe.

1. Minge moodulisse **Kreedit ja sissenõuded \> Märgukiri \> Märgukirjaseeria seadistus** ning seadistage märgukirjaseeria, nagu näidatud järgmises tabelis, mis on määratud kliendi sisestusreeglitele.

|     Märgukirja kood      |     Kirjeldus                           |     Currency      |     Põhikonto        |     Tasu valuutas     |     Minimaalne üle        |     Blokeeri päevad      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     1. märgukiri         |     Teine teatis tasuga        |     USA dollar           |                           |     0,00                  |     0,00                  |     2                 |
|     2. märgukiri         |     Teine teatis tasuga        |     USC           |     403150                |     20.00                 |     10.00                 |     3                 |
|     Kogum                    |     Lõplik teatis tasuga         |     USA dollar           |     403150                |     50.00                 |     100.00                |     15                |

Järgmine näide näitab teavet, mis on tabelis nii, nagu seda kuvataks **märgukirjade** lehel. 

[![Märgukirjaseeria seadistamine](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Nüüd peate seadistama kaks selle näite puhul nõutavat parameetrit.

2. Avage **Krediit ja sissenõudmine \> Seadistus \> Müügireskontro parameetrid**, ja järgige järgmisi samme:

    1. Kaardil **Sissenõudmine** märkige **Krediit ja sissenõuete märgukirjakoodi arvutamisel eira makseid valikute krediiditeatisi** valiku väärtuseks **Jah**.
    2. Veenduge, et välja **Loo märgukiri** oleks seatud väärtusele **Klient**.

    [![Sissenõuete müügireskontro parameetrite seadistamine](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Minge **müügireskontro \> Arved \> Kõik vabas vormis arved**, valige **Uus** ja seejärel järgige järgmisi samme:

    1. Valige **US-045** väljalt **Kliendi konto**.
    2. Sisestage **Arve kuupäev** väljale **1/15/2021**.
    3. Sisestage **Alates kuupäevast** väljale väärtus **1/16/2021**.
    4. Sisestage **Arve read** kiirkaardi väljale **Põhikonto** väärtus **401100**.
    5. Sisestage väljale **Ühiku hind** väärtus **500.00**.
    6. Valige **Sisesta**.

    Peate nüüd sisestama kliendile kaks kreeditarvet.

4. Valige käsk **Uus** ja tehke järgmist:

    1. Valige **US-045** väljalt **Kliendi konto**.
    2. Sisestage **Arve kuupäev** väljale **1/15/2021**.
    3. Sisestage **Alates kuupäevast** väljale väärtus **1/16/2021**.
    4. Sisestage **Arve read** kiirkaardi väljale **Põhikonto** väärtus **401100**.
    5. Sisestage **Ühiku hind** väljale **-100.00**.
    6. Valige **Sisesta**.

5. Korrake sammu 4, kuid sisestage **-200.00** väljal **Ühiku hind**.
6. Minge **müügireskontro \> Kliendid \> Kõik kliendid** ja valige klient **US-045**. Seejärel valige tegevuspaanil **Kanded \> Kanded** et vaadata kliendikandeid, mille sisestasite varem.

    [![Sisestatud kliendikannete ülevaatamine](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Teil on vaja nüüd kliendile US-045 märgukirjad koostada.

7. Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ja järgige järgmisi etappe:

    1. Seadke valiku **Arve** ja **Kreeditarve** väärtuseks **Jah**.

        Vaikimisi peaks välja **Märgukiri** väärtuseks olema määratud **Sissenõude märgukiri kliendi kohta**.

    2. Sisestage **Arve kuupäev** väljale **1/19/2021**.
    3. **Kaasamiseks** kiirkaardil valige **Filter** ja siis lisage **Kliendikonto** väljale **US-045**.
    4. Valige nupp **OK**.
    5. Sissenõudekirja printimiseks klõpsake **OK**.

8. Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ning järgige järgmisi etappe:

    1. Pange tähele, et märgukirja kood nii päisel kui kanderidadel on **1. märgukiri**, sest see märgukiri on seeria esimene märgukiri. (Kanderidade vaatamiseks peate võib-olla valima **Kannete** kiirkaardi.)

   [![Kontrollimine, et sama märgukirja kood ilmub päisele ja ridadele](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Tehke toimingupaanil valik **Väljastamine**.
    3. Sisestage **Arve kuupäev** väljale **1/19/2021**.

    Teil on vaja nüüd kliendile US-045 märgukirjad koostada.

9. Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ja järgige järgmisi etappe:

    1. Seadke valiku **Arve** ja **Kreeditarve** väärtuseks **Jah**.

        Vaikimisi peaks välja **Märgukiri** väärtuseks olema määratud **Sissenõude märgukiri kliendi kohta**.

    2. Sisestage **Märgukirja kuupäev** väljale **1/23/2021**.
    3. **Kaasamiseks** kiirkaardil valige **Filter** ja siis lisage **Kliendikonto** väljale **US-045**.
    4. Valige nupp **OK**.
    5. Sissenõudekirja printimiseks klõpsake **OK**.

10. Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ning järgige järgmisi etappe:

    1. Pange tähele, et päises oleva märgukirja kood on **1. märgukiri**. Kanderidade kood on siiski **2. märgukiri**.

   [![Kontrollimine, et sama märgukirja kood ilmub päisele ja ridadele](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Koodid erinevad, kuna **Sissemaksete koodi arvutamisel eira makseid ja krediiditeatisi** valiku väärtuseks on **Jah**.

  2. Ärge postitage seda märgukirja.

11. Minge **Krediit ja sissenõueded \> Seadistamine \> Müügireskontro parameetritesse** ja siis **Sissenõuded** vahekaardil **Eira makseid ja krediiditeatisi märgukirjakoodi arvutamisel** suvandile **Ei**.

    [![Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramiseks seadke väärtuseks Ei](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Teil on vaja nüüd kliendile US-045 märgukirjad koostada.

12. Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ja järgige järgmisi etappe:

    1. Seadke valiku **Arve** ja **Kreeditarve** väärtuseks **Jah**.

        Vaikimisi peaks välja **Märgukiri** väärtuseks olema määratud **Sissenõude märgukiri kliendi kohta**.

    2. Sisestage **Märgukirja kuupäev** väljale **1/23/2021**.
    3. **Kaasamiseks** kiirkaardil valige **Filter** ja siis lisage **Kliendikonto** väljale **US-045**.
    4. Valige nupp **OK**.
    5. Sissenõudekirja printimiseks klõpsake **OK**.

13. Minge **Krediit ja sissenõuded \> Märgukiri \> Vaadake üle ja koostage märgukiri** ja pange tähele, et märgukirja kood päisel ja kanderidadel on **2. märgukiri**.

    [![Kontrollimine, et sama märgukirja kood ilmub päisele ja ridadele](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Koodid erinevad, kuna **Sissemaksete koodi arvutamisel eira makseid ja krediiditeatisi** valiku väärtuseks on **Jah**.
