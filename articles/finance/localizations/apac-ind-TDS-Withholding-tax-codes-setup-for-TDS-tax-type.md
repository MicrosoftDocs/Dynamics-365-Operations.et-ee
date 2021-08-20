---
title: Kinnipeetava maksu koodide häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.
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
ms.openlocfilehash: add91eaef2ad091df7fd45e3de2dfe3993e6d62fdcbbcfcf95a7fc4953189239
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754875"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Kinnipeetava maksu koodide häälestamine TDS-i maksutüübi jaoks

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.

1. Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu koodid**.

    [![Kinnipeetava maksu koodide leht.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.
3. Väljal **Üldine** kiirkaardil **Maksu tüüp** valige **TDS** maksukood, et maksukoodi liigitada.
4. Väljal **Tasakaalustusperiood** valige TDS-i tasakaalustusperiood, mille tasakaalustusprotsessi käivitada.
5. Väljal **Põhikonto** valige pearaamatukonto, mille kohta tuleb TDS-summa sisestada.
6. Väljal **Müügireskontro** valige müügireskontro konto, mille kohta tuleb sisestadamüügikannetes mahaarvatud TDS-summa.

    Välja **Päritolu** väärtuseks seatakse automaatselt **Protsent brutosummast** ja seda väärtust ei saa muuta.

    > [!NOTE]
    > Te ei saa määrata päritolu väärtusele **Protsent netosummast** maksukoodide puhul, mille maksutüüp on TDS.

7. Väljal **Kinnipeetava maksu komponent** valige TDS maksu komponent TDS-i maksukoodiks.
8. Tegevuspaanil valige **Väärtused** et avada **Vahekaartide kujundamine** leht.
9. Valige arvutuse jaoks alguskuupäev väljal **Kuupäevast**. Väljale **Kuupäevani** sisestage lõpukuupäev.

    > [!NOTE]
    > Väljad **Alampiir**, **Ülempiir**, ja **Välista %** on TDS-maksutüübiga maksukoodide puhul saadaval.

10. Sisestage **Väärtus** väljale TDS protsent TDS maksu koodiks.
11. Sulgege **Kinnipeetava maksu väärtus** leht, et naasta **Kinnipeetava maksu koodid** lehele.

    > [!NOTE]
    > **Limiidid** nupp **Kinnipeetava maksu koodid** lehel ei ole saadaval maksukoodide puhul, mille tüüp on TDS.

12. Sulgege leht.
