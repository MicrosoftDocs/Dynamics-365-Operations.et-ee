---
title: Käibemaksu arvutamine ja ümardamine
description: See artikkel annab ülevaate käibemaksu arvutamisest ja ümardamisest ning selgitab käibemaksu arvutamise ja ümardamise seadistuse parameetreid.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939229"
---
# <a name="sales-tax-calculation-and-rounding"></a>Käibemaksu arvutamine ja ümardamine

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate käibemaksu arvutamisest ja ümardamisest Microsoft Dynamics 365 Finantsid. Samuti selgitab see parameetreid, mida kasutatakse käibemaksu arvutamise ja ümardamise seadistamisel, ning seda, kuidas need parameetrid koos töötavad.

## <a name="parameters"></a>Parameetrid

Käibemaksu arvutamise ja ümardamise parameetreid on mitu:

- **Arvutamismeetod** – see parameeter seadistatakse **pearaamatu** parameetrite lehel ja määratleb, kas maksu baassumma arvutatakse dokumendi või rea kohta. Kui käibemaksukoodi **marginaali** **põhiparameetri** väärtuseks on seatud Arve saldo netosumma, arvutatakse maksu baassumma alati dokumendi kohta, sõltumata selle parameetri sättest.
- **Ümardamis** by – see parameeter seadistatakse käibemaksugrupile ja määratleb, kas maksusumma ümardatakse käibemaksukoodi või käibemaksukoodi kombinatsiooni kohta.
- **Päritolukoht** – see parameeter on seadistatud käibemaksukoodile ja määratleb käibemaksusumma arvutamise. Lisateavet vt käibemaksu [arvutamise meetoditest väljal Päritolu](sales-tax-calculation-methods-origin-field.md).
- **Marginaali** alus – see parameeter on **seadistatud käibemaksukoodile ja määrab, millist summat kasutatakse leheküljel Käibemaksukoodi väärtused asjakohaste maksumäärade** valimiseks. Lisateabe saamiseks vaadake teemat [Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal](marginal-base-field.md).
- **Käibemaksu ümardamisreegel** – see parameeter on seadistatud käibemaksukoodile ja määratleb, kuidas määratletud käibemaksusumma ümardatakse, kaasa arvatud ümardamise täpsus ja ümardamismeetod.

Ülejäänud osa sellest artiklist sisaldab mõningaid tüüpilisi käibemaksu arvutamise ja ümardamise näiteid, mis kasutavad eelnevate parameetrite kombinatsiooni.

## <a name="scenario-for-the-examples"></a>Näidete stsenaarium

- Maksustatavas dokumendis on kaks rida ja iga rea maksu baassumma on 42,42.
- Igale reale on määratletud kaks käibemaksukoodi: käibemaksukood 1 ja käibemaksukood 2.
- Maksukoodi 1 ja maksukoodi 2 maksumäär on 10 protsenti.
- Hind ei sisalda maksu.
- Ümardamise täpsus on 0,01.
- Ümardamismeetod on **ümardamine**.

## <a name="example-1"></a>Näide 1

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus    | Lähtekoht                   | Marginaali alus       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Rida               | Käibemaksukood | Protsent netosummast | Netosumma rea kohta |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ------------| ---------------| --------------| -----------------|
| 1           | Kood 1         | 42.42         | 4.25             |
| 1           | Kood 2         | 42.42         | 4.25             |
| 2           | Kood 1         | 42.42         | 4.25             |
| 2           | Kood 2         | 42.42         | 4.25             |

Maksu baassumma arvutatakse rea kohta:

- **1. rida:** 42.42
- **2. rida:** 42.42

Maksusumma arvutatakse käibemaksukoodi alusel:

- **Rida 1:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 protsenti = 4,242
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 protsenti = 4,242

- **Rida 2:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 protsenti = 4,242
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 protsenti = 4,242

Maksusumma ümardatakse käibemaksukoodi kohta:

- **Rida 1:**

    - Ümardatud maksusumma käibemaksukoodile 1 = 4,25.
    - Ümardatud maksusumma käibemaksukoodile 2 = 4,25.

- **Rida 2:**

    - Ümardatud maksusumma käibemaksukoodile 1 = 4,25.
    - Ümardatud maksusumma käibemaksukoodile 2 = 4,25.

## <a name="example-2"></a>Näide 2

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus    | Lähtekoht                   | Marginaali alus                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Rida/summa         | Käibemaksukood | Protsent netosummast | Arve saldo netosumma |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.25             |
| 1           | Kood 2         | 42.42         | 4.25             |
| 2           | Kood 1         | 42.42         | 4.24             |
| 2           | Kood 2         | 42.42         | 4.24             |

Maksu baassumma arvutatakse dokumendi kohta:

- Maksu baassumma = 42,42 + 42,42 = 84,84

Maksusumma arvutatakse käibemaksukoodi alusel:

- Käibemaksusumma käibemaksukoodile 1 = 84,84 &times; 10 protsenti = 8,484
- Käibemaksukoodi 2 maksusumma = 84,84 &times; 10 protsenti = 8,484

Maksusumma ümardatakse käibemaksukoodi kohta:

- Ümardatud maksusumma käibemaksukoodile 1 = 8,49.
- Ümardatud maksusumma käibemaksukoodile 2 = 8,49.

Ümardatud maksusumma eraldatakse igale käibemaksukoodi reale:

- Eraldage käibemaksukoodi 1 (8.49) ümardatud maksusumma reale 1 (4.25) ja reale 2 (4.24).
- Eraldage ümardatud maksusumma käibemaksukoodile 2 (8.49) reale 1 (4.25) ja real 2 (4.24).

## <a name="example-3"></a>Näide 3

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus    | Lähtekoht                              | Marginaali alus       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Rida               | Käibemaksukood | Arvutatud protsent netosummast | Netosumma rea kohta |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.72             |
| 1           | Kood 2         | 42.42         | 4.72             |
| 2           | Kood 1         | 42.42         | 4.72             |
| 2           | Kood 2         | 42.42         | 4.72             |

Maksu baassumma arvutatakse rea kohta:

- **1. rida:** 42.42
- **2. rida:** 42.42

Maksusumma arvutatakse käibemaksukoodi alusel:

- **Rida 1:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133

- **Rida 2:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133

Maksusumma ümardatakse käibemaksukoodi kohta:

- **Rida 1:**

    - Ümardatud maksusumma käibemaksukoodile 1 = 4,72.
    - Ümardatud maksusumma käibemaksukoodi 2 = 4,72 kohta

- **Rida 2:**

    - Ümardatud maksusumma käibemaksukoodile 1 = 4,72.
    - Ümardatud maksusumma käibemaksukoodi 2 = 4,72 kohta

## <a name="example-4"></a>Näide 4

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus    | Lähtekoht                              | Marginaali alus                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Rida/summa         | Käibemaksukood | Arvutatud protsent netosummast | Arve saldo netosumma |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.72             |
| 1           | Kood 2         | 42.42         | 4.72             |
| 2           | Kood 1         | 42.42         | 4.71             |
| 2           | Kood 2         | 42.42         | 4.71             |

Maksu baassumma arvutatakse dokumendi kohta:

- Maksu baassumma = 42,42 + 42,42 = 84,84

Maksusumma arvutatakse käibemaksukoodi alusel:

- Käibemaksusumma käibemaksukoodile 1 = 84,84 &times; 10 &divide; protsenti (1 - 10 protsenti) = 9,4267
- Käibemaksusumma käibemaksukoodile 2 = 84,84 &times; 10 &divide; protsenti (1 - 10 protsenti) = 9,4267

Maksusumma ümardatakse käibemaksukoodi kohta:

- Ümardatud maksusumma käibemaksukoodile 1 = 9,43.
- Ümardatud maksusumma käibemaksukoodi 2 = 9,43 kohta

Ümardatud maksusumma eraldatakse igale käibemaksukoodi reale:

- Eraldage käibemaksukoodi 1 (9.43) käibemaksusumma reale 1 (4.72) ja reale 2 (4.71).
- Eraldage käibemaksukoodi 2 (9.43) maksusumma reale 1 (4.72) ja reale 2 (4.71).

## <a name="example-5"></a>Näide 5

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus                | Lähtekoht                   | Marginaali alus       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Rida               | Käibemaksukoodi kombinatsioon | Protsent netosummast | Netosumma rea kohta |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.25             |
| 1           | Kood 2         | 42.42         | 4.24             |
| 2           | Kood 1         | 42.42         | 4.24             |
| 2           | Kood 2         | 42.42         | 4.24             |

Maksu baassumma arvutatakse rea kohta:

- **1. rida:** 42.42
- **2. rida:** 42.42

Maksusumma arvutatakse käibemaksukoodi alusel:

- **Rida 1:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 protsenti = 4,242
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 protsenti = 4,242

- **Rida 2:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 protsenti = 4,242
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 protsenti = 4,242

Maksusumma ümardatakse käibemaksukoodi kombinatsiooni kohta:

- Käibemaksu kogusumma = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, mis ümardatakse 16,97-ni

Ümardatud maksusumma eraldatakse igale käibemaksukoodi reale:

- Eraldage käibemaksusumma (16,97) reale 1 ja reale 2:

    - **Rida 1:**

        - Käibemaksusumma käibemaksukoodile 1 = 4.25
        - Käibemaksukoodi 2 = 4.24 maksusumma

    - **Rida 2:**

        - Käibemaksusumma käibemaksukoodile 1 = 4.24
        - Käibemaksukoodi 2 = 4.24 maksusumma

## <a name="example-6"></a>Näide 6

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus                | Lähtekoht                   | Marginaali alus                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Rida/summa         | Käibemaksukoodi kombinatsioon | Protsent netosummast | Arve saldo netosumma |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.25             |
| 1           | Kood 2         | 42.42         | 4.24             |
| 2           | Kood 1         | 42.42         | 4.24             |
| 2           | Kood 2         | 42.42         | 4.24             |

Maksu baassumma arvutatakse dokumendi kohta:

- Maksu baassumma = 42,42 + 42,42 = 84,84

Maksusumma arvutatakse käibemaksukoodi alusel:

- Käibemaksusumma käibemaksukoodile 1 = 84,84 &times; 10 protsenti = 8,484
- Käibemaksukoodi 2 maksusumma = 84,84 &times; 10 protsenti = 8,484

Maksusumma ümardatakse käibemaksukoodi kombinatsiooni kohta:

- Käibemaksu kogusumma = 8,484 + 8,484 = 16,968, mis ümardatakse üles 16,97-ni.

Ümardatud maksusumma eraldatakse igale käibemaksukoodi reale:

- Eraldage käibemaksusumma (16,97) reale 1 ja reale 2:

    - **Rida 1:**

        - Käibemaksusumma käibemaksukoodile 1 = 4.25
        - Käibemaksukoodi 2 = 4.24 maksusumma

    - **Rida 2:**

        - Käibemaksusumma käibemaksukoodile 1 = 4.24
        - Käibemaksukoodi 2 = 4.24 maksusumma

## <a name="example-7"></a>Näide 7

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus                | Lähtekoht                              | Marginaali alus       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Rida               | Käibemaksukoodi kombinatsioon | Arvutatud protsent netosummast | Netosumma rea kohta |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.72             |
| 1           | Kood 2         | 42.42         | 4.71             |
| 2           | Kood 1         | 42.42         | 4.71             |
| 2           | Kood 2         | 42.42         | 4.72             |

Maksu baassumma arvutatakse rea kohta:

- **1. rida:** 42.42
- **2. rida:** 42.42

Maksusumma arvutatakse käibemaksukoodi alusel:

- **Rida 1:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133

- **Rida 2:**

    - Käibemaksusumma käibemaksukoodile 1 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133
    - Käibemaksusumma käibemaksukoodile 2 = 42,42 &times; 10 &divide; protsenti (1 - 10 protsenti) = 4,7133

Maksusumma ümardatakse käibemaksukoodi kombinatsiooni kohta:

- Käibemaksu kogusumma = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, mis ümardatakse üles 18,86

Ümardatud maksusumma eraldatakse igale käibemaksukoodi reale:

- Eraldage käibemaksusumma (18,86) reale 1 ja reale 2:

    - **Rida 1:**

        - Käibemaksusumma käibemaksukoodile 1 = 4,72
        - Käibemaksukoodi 2 = 4.71 maksusumma

    - **Rida 2:**

        - Käibemaksusumma käibemaksukoodile 1 = 4,71
        - Käibemaksusumma käibemaksukoodile 2 = 4,72

## <a name="example-8"></a>Näide 8

### <a name="parameter-values"></a>Parameetriväärtused

| Arvutamismeetod | Ümardusalus                | Lähtekoht                              | Marginaali alus                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Rida/summa         | Käibemaksukoodi kombinatsioon | Arvutatud protsent netosummast | Arve saldo netosumma |

### <a name="calculation-and-rounding-behavior"></a>Arvutuse ja ümardamise käitumine

| Rea number | Käibemaksukood | Summa alus | Käibemaksu summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kood 1         | 42.42         | 4.72             |
| 1           | Kood 2         | 42.42         | 4.71             |
| 2           | Kood 1         | 42.42         | 4.71             |
| 2           | Kood 2         | 42.42         | 4.72             |

Maksu baassumma arvutatakse dokumendi kohta:

- Maksu baassumma = 42,42 + 42,42 = 84,84

Maksusumma arvutatakse käibemaksukoodi alusel:

- Käibemaksusumma käibemaksukoodile 1 = 84,84 &times; 10 &divide; protsenti (1 - 10 protsenti) = 9,4267
- Käibemaksusumma käibemaksukoodile 2 = 84,84 &times; 10 &divide; protsenti (1 - 10 protsenti) = 9,4267

Maksusumma ümardatakse käibemaksukoodi kombinatsiooni kohta:

- Käibemaksu kogusumma = 9,4267 + 9,4267 = 18,8534, mis ümardatakse üles 18,86-ni

Ümardatud maksusumma eraldatakse igale käibemaksukoodi reale:

- Eraldage käibemaksusumma (18,86) reale 1 ja reale 2:

    - **Rida 1:**

        - Käibemaksusumma käibemaksukoodile 1 = 4,72
        - Käibemaksukoodi 2 = 4.71 maksusumma

    - **Rida 2:**

        - Käibemaksusumma käibemaksukoodile 1 = 4,71
        - Käibemaksusumma käibemaksukoodile 2 = 4,72

## <a name="additional-resources"></a>Lisaressursid

- [Käibemaksuarvutusmeetodid väljal Päritolu](sales-tax-calculation-methods-origin-field.md)
- [Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal](marginal-base-field.md)
- [Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul](whole-amount-interval-options-sales-tax-codes.md)
