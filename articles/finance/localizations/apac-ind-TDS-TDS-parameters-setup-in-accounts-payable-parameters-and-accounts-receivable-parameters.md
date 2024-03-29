---
title: TDS-i parameetrite määramine ostureskontros ja müügireskontros
description: See artikkel selgitab, kuidas määrata parameetrid Ostureskontros ja Müügireskontros, et toetada allika (TDS) mahaarvamistes mahaarvatud maksu.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e547b92f9f7e0ccc5b92df4cd991ce402369b568
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883146"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>TDS-i parameetrite määramine ostureskontros ja müügireskontros

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas määrata parameetrid Ostureskontros ja Müügireskontros, et toetada allika (TDS) mahaarvamistes mahaarvatud maksu.

1. Minge **Maks \> Seadistus \> Parameetrid \> Müügireskontro parameetrid**.
2. Vahekaardil **Uuendused** valige dialoogiboksi **Tellimuse ridade värskendamine** avamiseks suvand **Tellimuse ridade värskendamine** dialoogiboks.
3. Jaotise **TDS grupp** väljal **TDS-i grupi värskendamine** määrake meetod, mida kasutataks TDS-grupi värskendamiseks rea tasemel. Seda sätet kasutatakse TDS-i grupi tellimuse päises uuendamisel. Valikud on järgmised:

    - **Mitte kunagi** – TDS-gruppi ei uuendata tellimuse ridadel, kui seda värskendatakse tellimuse päises.
    - **Alati** – TDS-gruppi ei uuendata tellimuse ridadel, kui seda värskendatakse tellimuse päises.
    - **Viip** – Kasutajad saavad sõnumi, mis palub neil uuendada TDS-i gruppi tellimuse ridadel.
4. Valige nupp **OK**.

    [![Tellimuseridade uuendamise dialoogiboks.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Minge **Maks \> Seadistus \> Parameetrid \> Müügireskontro parameetrid**.
6. Seadke **Üldine** vahekaardil **Tükelda tarneaadressi põhjal** **Toote sissetulek** väärtusele **Jah** et sisestada ja tükeldada toote sissetulek, kus on erinevad tarneaadressid ja maksukonto numbrid (TAN-id). Kui see valik on seatud valikule **Ei** ei saa te sisestada ostu saatelehte, kus on erinevad tarneaadressid ja TAN-id.
7. TAN-idega ostuarve sisestamiseks ja tükeldamiseks määrake valiku **Arve** valiku väärtuseks **Jah**.

    [![Tükelda tarneteabe kiirkaardi põhjal.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Sulgege leht.
