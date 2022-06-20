---
title: TDS-i maksukoodide TDS-i maksugruppidele manustamine ja TDS-i arvutamise valemi määratlemine
description: See artikkel selgitab, kuidas seadistada allika (TDS) maksugruppides mahaarvatud maksu ja lisada TDS-i maksukoodid TDS-maksugruppidele. TDS-i maksugrupi TDS-i arvutamiseks peate määrama sellele lisatud TDS-i maksukoodide valemi.
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
ms.openlocfilehash: 3607e44bdcf7a32b156e6b4639ef907aa923cadc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853310"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>TDS-i maksukoodide TDS-i maksugruppidele manustamine ja TDS-i arvutamise valemi määratlemine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada allika (TDS) maksugruppides mahaarvatud maksu ja lisada TDS-i maksukoodid TDS-maksugruppidele. TDS-i maksugrupi TDS-i arvutamiseks peate määrama sellele lisatud TDS-i maksukoodide valemi.

Järgige neid samme TDS-i maksugrupi häälestamiseks, lisage TDS-i maksukoodid ja määratlege TDS-i arvutamiseks valem.

1. Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu grupid**.

    [![Kinnipeetava maksugrupi leht.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.
3. Tehke väljal **Maksu tüüp** valik **TDS**.
4. Tehke uue rea loomiseks kiirkaardil **Seaded** valik **Lisa**.
5. Valige väljal **Kinnipeetava maksu kood** kinnipeetava maksu grupi jaoks kinnipeetava maksu kood. Väljal **Kinnipeetava maksu nimi** kuvatakse TDS-maksukoodi nimi ja väljal **Väärtus** kuvatakse väärtus.
6. TDS-kannetes TDS-i maksukoodiga seotud TDS-i maksukomponendile määratud läve limiidi ja erandi läve limiidi ignoreerimiseks märkige ära **Unusta lävi** ruut.
7. Valige märkeruut **Vabastatud**, et vältida arvutatud summa redigeerimist programmi mallis.
8. Tegevuspaanil valige **Kujundaja** et avada valemikoosturit, nii et saate TDS-i maksugrupi jaoks määratleda TDS-i arvutamise valemi. Lehel **Kujundaja** kuvatakse vahekaardil **Maksud** TDS-i maksugrupi jaoks valitud TDS-i maksukoodid.

    [![Kujundaja leht.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Rea **Kalkulatsioon** loomiseks valige vahekaardil **Alt+N**. Väli **ID** näitab automaatselt loodud prioriteedi ID-d TDS-i arvutamiseks.
10. Valige väljal **Kinnipeetava maksu kood** kinnipeetava maksu grupi jaoks kinnipeetava maksu kood. Kõik TDS-i maksukoodid, mis on TDS-i maksugrupi jaoks valitud, on sellel väljal saadaval.
11. Väljal **Maksustatava alus** valige TDS-i arvutamise alus:

    - **Brutosumma** – Arvutage TDS kande brutosumma (st arve summa) alusel, kasutades maksukoodi jaoks määratletud arvutusavaldist.
    - **Välja arvatud brutosumma** – Arvutage TDS maksukoodile määratud arvutusavaldise alusel.

    > [!NOTE]
    > Välja **Maksustatav alus** ei saa seada väärtusele **Välja arvatud brutosumma** TDS-maksukoodi jaoks, mille prioriteedi ID on **1**.

12. TDS-i arvutus põhineb valemil, mis on määratud arvutusavaldise väljal **Arvutusavaldis** TDS-maksugrupiga seotud maksukoodi jaoks. Valige plussmärk (+), miinusmärk (-), korrutusmärk (\*), või jagamismärk (/) TDS-maksukoodi arvutusavaldise sisestamiseks **Arvutusavaldis** väljal.

    > [!NOTE]
    > Arvutusavaldist ei saa määrata TDS-i maksukoodile, mille prioriteedi ID on **1**.

13. TDS-i maksukoodi arvutusavaldise määratlemiseks **Arvutusavaldise** väljal, lisage saadaolevad TDS-maksukoodid **Maksud** vahekaardile. TDS-i maksukoodide lisamiseks **Arvutusavaldise** väljale saate kasutada mõnda järgmistest meetoditest:

    - Lohistage nõutav maksukood **Maksud** vahekaardilt **Arvutusavaldise** väljale.
    - Topeltpuudutage (või topeltklõpsake) vahekaardil **Maksud** nõutavat maksukoodi.
    - Valige ja hoidke all (või paremklõpsake) nõutavat maksukoodi vahekaardil **Maksud** ja valige **Lisage maksukood**.

    > [!NOTE]
    > Saate lisada arvutusavaldise iga TDS-i maksukoodi ette. Arvutusavaldisse lisatud TDS-maksukoodid kuvatakse sulgudes (\[...\]).

14. Käibemaksukoodi jaoks määratletud arvutusavaldise tühjendamiseks väljal **Arvutusavaldis** valige **C** nupp.
15. Kirje kustutamiseks vahekaardil **Kalkulatsioon** valige **Kustuta**.
16. Sulgege leht.
