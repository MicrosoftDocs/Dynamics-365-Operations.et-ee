---
title: Väljamineva protsessi ülevaade
description: Selles teemas antakse ülevaade väljaminevast protsessist moodulis Laohaldus.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: db1a6887e7742700dd3451c9a877b948b5ab691b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207274"
---
# <a name="outbound-process-overview"></a>Väljamineva protsessi ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade väljaminevast protsessist moodulis Laohaldus.

## <a name="output-orders"></a>Väljaminekuorderid

Müügitellimuse ridade ja üleviimistellimuse ridade seostamiseks komplekteerimislehti kasutavate väljaminevate komplekteerimisprotsessidega kasutatakse väljaminekuordereid.

Komplekteerimislehtede loomisel müügitellimustest või üleviimistellimustest luuakse automaatselt väljaminekuorderid ja saadetised. Komplekteerimislehel on saadetisega üks-ühele suhe. Saadetisest saab töödelda üleviimistellimuse saadetise või müügitellimuse saatelehe. 

Järgmisel joonisel on antud ülevaade väljaminekuorderite protsessist. 

[![Ülevaade väljaminekuorderi protsessist](./media/outbound-order.png)](./media/outbound-order.png)

Saate seadistada lähetusreeglid, et määratleda, kuidas programm peaks lähetusprotsessi käsitsema. Seejärel saab nende reeglite abil lähetusprotsessi juhtida. Konkreetsemalt võite kasutada neid reegleid juhtimiseks, millise protsessietapi jooksul saadetis tuleks välja saata. Järgmised sätted määratlevad, kuidas väljaminevaid protsesse käsitsetakse.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Müügi- ja üleviimistellimuste komplekteerimisprotsessi olek 

Avage **Ostureskontro** \> **Seadistus** \> **Ostureskontro parameetrid** ja valige siis vahekaardi **Värskendused** väljalt **Komplekteerimisprotsessi olek** väärtus.

[![Müügitellimuste komplekteerimisprotsessi oleku väli](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Kui välja **Komplekteerimisprotsessi olek** väärtuseks on määratud **Lõpule viidud**, toimub komplekteerimisprotsess komplekteerimislehtede koostamise protsessi raames automaatselt. Kui välja väärtuseks on määratud **Aktiveeritud**, tuleb komplekteerimislehe read käsitsi värskendada.

Sama puudutab üleviimistellimusi. Avage **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** ja valige siis vahekaardi **Transport** väljalt **Komplekteerimisprotsessi olek** väärtus.

[![Üleviimistellimuste komplekteerimisprotsessi oleku väli](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Väljamineku laoorderite lõpetamine

Avage **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** ja määrake siis vahekaardil **Üldine** valik **Lõpeta väljamineku laoorder**.

[![Valik Lõpeta väljamineku laoorder](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Kui laotöötaja vähendab komplekteerimislehe koguseid, eemaldatakse vastavad laoorderi kogused saadetisest. Kui komplekteerimislehte uuendatakse teatud ajahetkel, registreeritakse ülejäänud kogused uuesti tellimuse tasandil, kui suvand **Lõpeta väljamineku laoorder** on seatud väärtusele **Jah**. Kui suvand **Lõpeta väljamineku laoorder** on seatud väärtusele **Ei**, hoitakse ülejäänud koguseid avatud väljaminekuorderi kogusena ja need tuleb uuele komplekteerimislehele lisada funktsiooni **Ava väljaminekuorderid** osana. 

[![Käsk Ava väljaminekuorderid menüüs Funktsioonid](./media/open-output-order.png)](./media/open-output-order.png)

[![Lehe Ava väljaminekuorderid menüü Funktsioonid](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Vähenda kogust

Kolmas parameeter, mida saate komplekteerimislehe koostamise raames kasutada, on parameeter **Vähenda kogust**. Selle parameetri seadistus toimib koos sättega **Reserveerimine**, mis käivitab lattu väljastamise raames reserveerimisprotsessi.

[![Parameeter Vähenda kogust](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Müügitellimuse väljamineva protsessi näide

Selle näite puhul on olemas müügitellimus kahele kaubale. Komplekteerimislehe koostamise ajal tuleb valida parameeter **Vähenda kogust**. Seetõttu vabastate ja loote komplekteerimisread ainult vabale kaubavarule. Komplekteerimine tuleb registreerida komplekteerimislehtede registreerimisprotsessi kaudu (**Komplekteerimisprotsessi olek** = **Aktiveeritud**).

Veel reserveerimata kaubavaru reserveeritakse komplekteerimislehe koostamise käigus. Kaubavaru, mis pole saadaval, võib müügitellimusest eemaldada või väljastada lattu väljamineku töötlemiseks hiljem, kui varud on komplekteerimiseks saadaval.

[![Komplekteerimislehe värskendamine](./media/update-picking-list.png)](./media/update-picking-list.png)

Kohe, kui kõik komplekteerimisread on lehel **Komplekteerimislehe registreerimine** komplekteeritud, lõpetatakse seotud saadetis. Müügitellimuse saatelehtede protsessi saab siis komplekteeritud varude põhjal lähtestada.

[![Väljuvate saadetiste värskendamine](./media/outbound-shipments.png)](./media/outbound-shipments.png)
