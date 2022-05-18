---
title: TDS-i kontsessioonisertifikaadi numbrite kirjendamine
description: See teema kirjeldab, kuidas kirjendada mahaarvatud makseallika (TDS) kontsessiooniserdi numbrites, mis väljastatakse hankijatele.
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
ms.openlocfilehash: 994ddbb4666c326d237d53d529ba126f42d48595
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727141"
---
# <a name="record-tds-concession-certificate-numbers"></a>TDS-i kontsessioonisertifikaadi numbrite kirjendamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas kirjendada mahaarvatud makseallika (TDS) kontsessiooniserdi numbrites, mis väljastatakse hankijatele.

1. Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu mööndused**.
2. Valige **Maksutüübi** väljal **TDS** et kirjendada TDS-maksutüübi kontsessiooniserdid.
3. Vahekaardil **Ülevaade** valige rea loomiseks **Alt+N**.

    [![Uue rea päis.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Väljal **Kinnipeetava maksu kood** valige TDS-maksukood, mille jaoks hankija kontsessioonisertifikaadid välja antakse. Sisestage väljale **Kinnipeetava maksu nimi** kinnipeetava maksu koodi nimi.
5. Määratlege **Alates** ja **Kuni kuupäevani** kontsessiooniserdi kehtivuse periood, mis kasutab TDS-i maksukoodi hankija TDS-i kontsessiooni alusel arvutamiseks.
6. Väljale **Märkused** sisestage kõik märkused.
7. Sisestage **Jaotise** väljale juriidilise sektsiooni kood, mille alusel TDS-i kontsessiooni sert on saadaval.

    Kui sektsiooni kood on 197, kuvatakse väärtus "A" nii vormi 26Q veerus "Mahaarvamise mittevähenduse põhjus / väiksem mahaarvamine" kui ka veerus "Mahaarvamise mittevähenduse põhjus / väiksem mahaarvamine/brutokasumine (kui see on olemas)" vormis 27Q. Kui sektsiooni kood on 197A, kuvatakse mõlemas kohas väärtus "B".

8. Valige **Serddi** kiirkaart TDS-i kontsessiooniserdi numbrite kirjendamiseks hankijate jaoks.
9. Väljal **Hankija konto** valige hankija konto, mille jaoks TDS-i kontsessiooni sert välja antakse.
10. Määratlege **Alates** ja **Kuni** väljaddel kuupäevani TDS-i kontsessiooniserdi kehtivusperiood.

    TDS-i arvutamine kontsessiooni alusel põhineb perioodil, mil sert on hankija jaoks loodud.

11. Väljale **Sert** sisestage TDS-i kontsessiooniserdi number.

    [![Serdi kiirkaart.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Sulgege leht.
