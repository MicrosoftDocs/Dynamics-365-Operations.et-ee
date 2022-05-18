---
title: Perioodilise TDS-i tasakaalustusprotsessi käitamine
description: See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.
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
ms.openlocfilehash: 6c0aca4d0a916b21ca5ac6ee14e6ab658e0bae26
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726430"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Perioodilise TDS-i tasakaalustusprotsessi käitamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.

1. Minge **Maksu \> Deklaratsioonidesse \> Kinnipeetav maks \> Kinnipeetava maksu makse**.

    [![Kinnipeetava maksu makse dialoogiboks.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Dialoogiaknas **Kinnipeetava maksu makse** väljal **Maksu tüüp** valige **TDS**.
3. Väljal **Maksukonto number (TAN)** valige maksukonto number (TAN), mille tasakaalustusprotsessi käitada.
4. Väljal **Kinnipeetava maksu komponendigrupp** valige TDS-i komponendigrupp, mille tasakaalustusprotsess käivitada.
5. Väljal **Tasakaalustusperiood** valige TDS-i tasakaalustusperiood, mille tasakaalustusprotsessi käivitada.

    > [!NOTE]
    > TDS-i tasakaalustusprotsessi käitatakse kõigi perioodide kohta, mis on seadistatud TDS-i tasakaalustusperioodiks lehekülje **Perioodid** vahekaardil **Kinnipeetava maksu tasakaalustusperioodid** lehel (**Maksud \> Kaudsed maksud \> Kinnipeetav maks \> kinnipeetav maksu tasakaalustusperioodid**).

6. Väljal **Kuupäevast** valige TDS-i tasakaalustusprotsessi käivitamiseks alguskuupäev.

    Tasakaalustusperioodi kindla perioodi alguskuupäevaks võetakse "alates" kuupäev. Näiteks TDS-i tasakaalustusperioodil on kaks perioodi: 1. aprill kuni 30. aprill 2009 ja 1. mai kuni 31. mai 2009. Kui valite **04.06.2009** (6. aprill 2009) **alguskuupäevaks** käivitatakse tasakaalustusprotsess siiski alates 1. aprillist 2009.

    Kui sisestate hilisema perioodi väljale **Kuupäevast** kuid tasakaalustamata tasakaalustusperioodi eelmist perioodi, siis tasakaalustust ei toimu eelmiste perioodide puhul. Näiteks TDS-i tasakaalustusperioodil on kolm perioodi: 1. aprill kuni 30. aprill 2009, 1. mai kuni 31. mai 2009 ja 1. juuni kuni 30. juuni 2009. Kui valite **05.01.2009** (1. mai 2009) alguskuupäevaks väljal **Alates kuupäevast**, käivitatakse tasakaalustusprotsess ainult 1. maist kuni 31. maini 2009. Tasakaalustus ei toimu 01. aprillist kuni 30. aprillini 2009.

7. Väljal **Tasakaalustusprotsessi kuupäev** valige TDS-i tasakaalustusprotsessi käivitamiseks alguskuupäev.
8. Dialoogiaknas **Kinnipeetava maksu makse** väljal valige TDS tasakaaluversioon:

     - **Originaal** – Kasutage seda valikut TDS-i tasakaalustusprotsessi esmakordselt käivitamiseks. Algset makseversiooni kasutatakse vaid üks kord TDS-i tasakaalustusprotsessi käivitamiseks kinnipeetava maksu komponendigrupi ja kinnipeetava maksu tasakaalustusperioodi kombinatsiooni puhul.
    - **Viimased versioonid** – Kasutage seda valikut, kui TDS-i tasakaalustusprotsess on juba määratud perioodiks käitatud. Kaasab järelkuupäevaga kanded, mis sisestati pärast selle perioodi tasakaalustusprotsessi eelnevalt käivitamist. Selle valiku abil saate tasakaalustusprotsessi käivitada mis tahes arv kordi.

9. Valige **Uuenda** märkeruut TDS-i tasakaalustusprotsessi käivitamiseks ja summade pearaamatukontodele sisestamiseks. Kui see ruut on tühi, siis tasakaalustusprotsessi ei käivitata ja finantskandeid ei looda.
10. Valige **OK** TDS-i tasakaalustusprotsessi käivitamiseks ja kinnipeetava maksu maksearuande loomiseks. Tasakaalustusprotsessi kaasatud TDS-kannete olek kuvatakse **Tasakaalustusena** **Tasakaalustus** lehel (minge **Ostureskontro \> Maksete \> Hankija makse tööleht**, **Read**, valige **Funktsioonid** ja siis valige **Tasakaalustamine**).

### <a name="important-points"></a>Olulised punktid

- Kui kinnipeetava maksu komponendigruppi tasakaalustusprotsessi käigus ei valita, toimub tasakaalustus kõigi kinnipeetava maksu komponendigruppide puhul valitud TAN maksu ja tasakaalustusperioodi jooksul. Iga kinnipeetava maksu komponendi rühma jaoks luuakse eraldi rida **Ava tehingu redigeerimine** lehel.
- Tasakaalustusprotsess põhineb tasakaalustusperioodi hinnakategooria olemusel. Kanded, mille hindamiskategooria olemus on **Ettevõte** tasakaalustatakse ja kuvatakse ühe reana **Avatud kannete redigeerimise** lehel. Kanded, mille hindamiskategooria olemus on **Ettevõte** tasakaalustatakse ja kuvatakse ühe reana **Avatud kannete redigeerimise** lehel.
- TDS-i tasakaalustatud TDS-kande ridade tähtaeg **Avatud kande redigeerimise** lehel on määratud TDS-i maksetingimustel, mis on TDS hankija jaoks määratud **Hankijad** lehel. Kui TDS-i asutuse hankija jaoks ei ole maksetingimusi määratletud, kuvatakse tasakaalustusperioodi viimane päev tähtajana.
