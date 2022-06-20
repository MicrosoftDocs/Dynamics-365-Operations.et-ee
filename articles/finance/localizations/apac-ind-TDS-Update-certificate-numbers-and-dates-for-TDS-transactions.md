---
title: TDS-i kannete sertifikaadinumbrite ja kuupäevade uuendamine
description: See artikkel selgitab, kuidas värskendada tagasisaadav serdi numbreid ja kuupäevi, mis salvestati allikas (TDS) mahaarvatud maksu hankija, kliendi ja pearaamatu kontodele.
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
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904437"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>TDS-i kannete sertifikaadinumbrite ja kuupäevade uuendamine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas värskendada tagasisaadav serdi numbreid ja kuupäevi, mis salvestati allikas (TDS) mahaarvatud maksu hankija, kliendi ja pearaamatu kontodele. TDS-kannete serte saate vaadata lehel **Taastatavad serdid**. Saate serte uuendada, kasutades **Sertide värskendamine** lehte.

TDS-tehingute sertifikaatide numbrite ja kuupäevade värskendamiseks toimige järgmiselt.

1. Minge **Maks \> Deklaratsioonid \> Kinnipeetav maks \> Värskenda sertifikaat**.

    [![Serdilehe värskendamine.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

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

    [![Serdi kannete leht.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
