---
title: Maksukomponentide häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas seadistada kinnipeetava maksu komponente allika (TDS) maksutüübis mahaarvatud maksu jaoks. See selgitab ka, kuidas määrata läve limiiti, mida kasutatakse iga TDS-i komponendi TDS-i arvutamiseks.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 11b1336289f1fad0366882a18867ff527900d8bfb14051c909a0b0ff72779073
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726006"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Maksukomponentide häälestamine TDS-i maksutüübi jaoks

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada kinnipeetava maksu komponente allika (TDS) maksutüübis mahaarvatud maksu jaoks. TDS-i komponendid on TDS, lisatasu, PE-Cess ja SHE Cess. See selgitab ka, kuidas määrata läve limiiti, mida kasutatakse iga TDS-i komponendi TDS-i arvutamiseks. Lisaks saate määratleda erandi läve, mida kasutatakse iga TDS-i komponendi TDS-i arvutamiseks.

TDS komponentidde häälestamiseks tehke järgmist.

1. Minge **Maks \> Seadistus \> Kinnipeetav maks \> Kinnipeetava maksu komponendid**.

    [![Kinnipeetava maksu komponentide leht.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. **Maksu tüübi** väljal valige **TDS** kinnipeetava maksu komponentide häälestamiseks.
3. Rea loomiseks valige toimingupaanilt suvand **Uus**.
4. Sisestage **Kinnipeetava maksu** väljale TDS-i komponendi nimi.
5. Väljal **Kinnipeetava maksu komponendigrupp** valige TDS-i kinnipeetava maksu komponendi grupp, et lisada TDS-i komponent.
6. Sisestage TDS komponendi kirjeldus kiirkaardi **Üldine** väljale **Kirjeldus**.
7. Tegevuspaanil valige **Avamisläve** lehel **Lävi** leht, nii et saate määratleda läve, mida kasutatakse TDS-i komponendi jaoks TDS-i arvutamiseks.
8. Kasutage välju **Alates** ja **Kuni** et määrata periood, mille suhtes lävi kehtib.
9. **Üldisele** kiirkaardile **Läve** väljal sisestage lävendsumma, mida kasutatakse TDS-i komponendi jaoks TDS-i arvutamiseks. Maks arvatakse maha allika juures ainult siis, kui kumulatiivne arvesumma ületab läve.

    Näiteks kui lävisumma on 10 000, siis arvutatakse TDS pärast seda, kui kumulatiivne arvesumma on suurem kui 10 000 (teisisõnu, kui see on 10 001 või enam).

10. Kaardile **Erani lävi** väljal sisestage lävendsumma, mida kasutatakse TDS-i komponendi jaoks TDS-i arvutamiseks. Maks arvatakse maha allika juures ainult siis, kui kumulatiivne arvesumma ületab läve.

    Näiteks kui erandi lävisumma on 5000, siis arvutatakse TDS konkreetsel arvereal, kui arve rea summa ületab 5000 (teisisõnu on see 5001 või rohkem).

    [![Läve leht.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Erandi lävisumma peab olema lävisummast väiksem või sellega võrdne.
    >
    > Kande maks arvatakse maha, kui kande summa ületab erandi läve, isegi kui kumulatiivne arvesumma ei ületa **Läve** määratud välja.

11. Sulgege leht **Lävi**, et naasta **kinnipeetava maksu komponentide** lehele.
12. Tegevuspaanil valige suvand Kopeeri, et avada dialoogiboks Kinnipeetava maksu komponentide kopeerimine, nii et saate kopeerida ühe TDS-i komponendigrupi jaoks seadistatud TDS-i komponendid teise **Kopeeri** et avada dialoogiboks **Kinnipeetava maksu komponentide kopeerimine** nii et saate kopeerida ühe TDS-i komponendigrupi jaoks seadistatud TDS-i komponendid teise TDSi komponendigruppi.
13. Valige väljal **Alates** komponendigrupp TDS, millelt TDS-i komponente kopeerida. Valige väljal **Alates** komponendigrupp TDS, millelt TDS-i komponente kopeerida.

    > [!NOTE]
    > TDS-i mõlema komponendigrupiga seotud ühiseid TDS-i komponente ei kopeerita.

14. Valige **OK** et kopeerida ja luua TDS-i komponente muule TDS-i komponendigrupile **kinnipeetava maksu komponentide** lehel.

    [![Kinnipeetava maksu komponentide dialoogiboksi kopeerimine.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Sulgege leht.
