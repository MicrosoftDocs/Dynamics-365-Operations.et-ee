---
title: TDS-i kannete sertifikaadinumbrite ja kuupäevade uuendamine
description: See teema selgitab, kuidas kasutada tagasisaadava sertide lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023174"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>TDS-i kannete sertifikaadinumbrite ja kuupäevade uuendamine

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas kasutada tagasisaadava sertide lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks. TDS-kannete serte saate vaadata lehel **Taastatavad serdid**. Saate serte uuendada, kasutades **Sertide värskendamine** lehte.

TDS-tehingute sertifikaatide numbrite ja kuupäevade värskendamiseks toimige järgmiselt.

1. Minge **Maks \> Deklaratsioonid \> Kinnipeetav maks \> Värskenda sertifikaat**.

    [![Serdilehe värskendamine](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Valige **Serdi värskendamine** lehel **Vali** väljal **Maksu tüüp** **TDS**.
3. Väljal **Sertifikaadi number** valige kliendi või hankija TDS-i serdi number.

    > [!NOTE]
    > **Serdi numbri** väli loetleb ainult TDS-i serdinumbreid, mille puhul on ruut **Suletud** tühjendatud **Taastatavad serdid** lehel.

    Väljal **Serdi kuupäev** näidatakse serdi kuupäev. Väljal **Kontotüüp** kuvatakse kontotüüp, mille kohta TDS-serdi number vastu võetakse, ning väljal **Nimi** kuvatakse konto nimi.

5. Vahekaardil **Kuupäevast** ja **Kuupäevani** sisestage TDS kannete eelarveperioodi algus- ja lõppkuupäev.
6. Valige **Kuva andmed**, et vaadata valitud perioodi jooksul sisestatud TDS-i kandeid.

    Vahekaardi **Ülevaade** ülemisel paanil kuvatakse tabelil järgmine teave iga TDS-kande kohta, mis hankijale või kliendile valitud perioodi jooksul sisestati:

    - **Kviitung** - kuvatakse TDS tehingukande kviitungi number.
    - **Kuupäev** – TDS kannete kuupäev.
    - **Summa** - arvele sisestatud summa, mida TDS on arvutanud.
    - **Maksusumma** – TDS-i maksusumma, mis kande jaoks arvutatud.

7. Kindlate TDS-kannete teisaldamiseks ülemisest ruudustikust alumisele ruudustikule valige kanded ja seejärel käsk **Kaasa**. Teise võimalusena valige käsk **Kaasa kõik** et teisaldada kõik TDS-kanded ülemisest ruudustikust alumisele ruudustikule.

    Kindlate TDS-kannete või kõikide TDS-kannete teisaldamiseks alumisest ruudustikust ülemisse ruudustikku kasutage nuppu **Välista** või **Välista kõik**.

8. Valige **Värskenda** et värskendada **Serdi numbrit** ja **Serdi kuupäev** väljal TDS-kannete jaoks alumises ruudustikus.
10. Minge **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Taastatav sert** ja valige **Päring**, et vaadata värskendatud kanderidu, milles on uus serdi number **Serdikannete** lehel.

    [![Serdi kannete leht](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
