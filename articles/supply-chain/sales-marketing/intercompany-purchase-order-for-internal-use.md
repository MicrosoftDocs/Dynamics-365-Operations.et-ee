---
title: Kontsernisisese ostutellimuse loomine ja arveldamine sisemiseks kasutamiseks
description: See teema kirjeldab kuidas luua kontsernisisest ostutellimust ja arveldamist sisemiseks kasutamiseks
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548216"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Kontsernisisese ostutellimuse loomine ja arveldamine sisemiseks kasutamiseks

[!include [banner](../../includes/banner.md)]

Saate kontsernisisesele hankijale luua kontsernisisese ostutellimuse. See loob kontsernisisese hankija jaoks automaatselt kontsernisisese müügitellimuse.

![Kontsernisisene ostuprotsess](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Kontsernisisese müügitellimuse ja vastava kontsernisisese ostutellimuse loomine

Läbige need juriidilise isiku AAA etapid, nagu on joonisel kujutatud.

1. Valige jaotis **Ostureskontro** \> **Ostutellimused** \> **Kõik ostutellimused**.
1. Loendilehel **Kõik ostutellimused** looge ostutellimus kontsernisisesele hankijale. Väljade väärtused kopeeritakse hankija kontolt ostutellimusele.

    Kuna töötate kontsernisisese hankijaga, luuakse hankijale vastavas juriidilises isikus kontsernisisene müügitellimus. Kontsernisisese müügitellimuse number võib ühtida kontsernisisese ostutellimuse numbriga ja võib sisaldada juriidilise isiku ID-d. Kasutatav numbristruktuur sõltub valikust lehe **Kontsernisisene** väljal **Müügitellimuse number**. Kui loote näiteks juriidilises isikus AAA ostutellimuse 00029\_064, on juriidilises isikus BBB müügitellimuse number AAA00029\_64.

    Teavitusteates kuvatakse teade, et on loodud kontsernisisene ostutellimus ja kontsernisisene müügitellimus. Teade sisaldab teile teadmiseks kontsernisisese müügitellimuse numbrit.

1. Lisage ostutellimusele reakaupu. Vastavad reakaubad lisatakse automaatselt kontsernisisesele müügitellimusele. Kui teises juriidilises isikus kaupa pole, kuvatakse teade ja kaupa ei saa ostutellimusele lisada. Probleemi lahendamiseks avage teine juriidiline isik ja väljastage toode sellele juriidilisele isikule. Kaup on saadaval selles juriidilises isikus müügitellimustele lisamiseks. Seejärel naaske ostutellimuse juriidilise isiku juurde ja jätkake reakaupade lisamist.
1. Pärast ostutellimuse jaoks teabe sisestamise lõpetamist kinnitage see.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Kontsernisisese saatelehe ja kliendiarve töötlemine

Läbige need juriidilise isiku BBB etapid, nagu on joonisel kujutatud.

1. Avage jaotis **Müügireskontro \> Müügitellimused \> Kõik müügitellimused**.
1. Loendilehel **Kõik müügitellimused** valige kontsernisisene müügitellimus.
1. Tegevuspaanil valige vahekaart **Komplekteerimine ja pakkimine** ning seejärel valige **Saateleht**.
1. Valige märkeruut **Sisestamine**.
1. Valige nupp **OK**. Saateleht sisestatakse juriidilisse isikusse BBB.
1. Loendilehel **Kõik müügitellimused** valige kontsernisisene müügitellimus.
1. Toimingupaanil valige vahekaart **Arve** ja seejärel valige uuesti **Arve**.
1. Valige märkeruut **Sisestamine**.
1. Valige nupp **OK**.

    Kontsernisisese müügitellimuse kliendiarve sisestatakse juriidilisse isikusse BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Kontsernisisese toote sissetuleku ja hankija arve töötlemine

Läbige need juriidilise isiku AAA etapid, nagu on joonisel kujutatud.

1. Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.
1. Loendilehel **Kõik ostutellimused** valige kontsernisisene ostutellimus.
1. Valige tegevuspaanilt **Võta vastu** ja seejärel valige **Toote sissetulek**. Luuakse toote sissetulek. Toote sissetuleku number ühtib kontsernisisese saatelehe numbriga.
1. Valige märkeruut **Sisestamine**.
1. Valige nupp **OK**.
1. Loendilehel **Kõik ostutellimused** valige kontsernisisene ostutellimus.
1. Toimingupaanil valige **Arve** ja seejärel valige uuesti **Arve**. Luuakse tarnija arve. Hankija arve number ühtib kontsernisisese kliendiarve numbriga.
1. Lõpetage hankija arve andmete sisestamine ja seejärel sisestage see.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
