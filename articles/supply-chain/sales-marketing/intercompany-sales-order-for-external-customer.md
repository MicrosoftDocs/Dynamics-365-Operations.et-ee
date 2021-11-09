---
title: Kontsernisisese müügitellimuse loomine ja arveldamine väliskliendi puhul
description: See teema kirjeldab kuidas luua kontsernisisest müügitellimust ja arveldamist väliskliendi puhul
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548211"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Kontsernisisese müügitellimuse loomine ja arveldamine väliskliendi puhul

[!include [banner](../../includes/banner.md)]

Kontsernisisese kaubavahetuse abil saate kirjendada toote müügi ühest juriidilisest isikust teise juriidilisse isikusse, mis on samas organisatsioonis.

Algse müügitellimuse loomisega saate kontsernisisese hankija jaoks luua automaatselt kontsernisisese ostutellimuse. See loob kontsernisisese hankija juriidilises isikus automaatselt kontsernisisese müügitellimuse.

Järgmine joonis näitab kannete voogu müügitellimuse loomisel väliskliendile, kuid toode tuleb tellida teisest juriidilisest isikust teie organisatsioonis, enne kui saate toote kliendile tarnida. Sel juhul luuakse kontsernisisene ostutellimus teist juriidilist isikut esindava hankija kontole. Teises juriidilises isikus luuakse omakorda kontsernisisene müügitellimus teie juriidilist isikut esindavale kliendikontole. Otsetarne puhul sisestatakse algse müügitellimuse arve automaatselt, kui kontsernisisene ostutellimus on arveldatud.

![Kontsernisisene väline müügiprotsess](media/intercompanyexternalsalesprocess.png)

Kui kasutate otsetarnet ja valite lehe **Arve sisestamine** väljal **Kogus** suvandi **Saateleht**, põhineb kontsernisisene hankijatellimuse arve eelnevalt sisestatud kontsernisisesel toote sissetulekul.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist veenduge, et kontsernisiseste arvete automaatseks sisestamiseks ja printimiseks on täidetud järgmised eeltingimused.

1. Avage jaotis **Müük ja turundus \> Kliendid \> Kõik kliendid**.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Avage **Hanked \> Hankijad \> Kõik hankijad**.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Märkige **Kontsernisisesel** kas hankija või kliendi lehel väljagrupi **Kontsernisisene ostutellimus (otsetarne)** jaotises **Ostutellimuse poliitikad** ruut **Sisesta arve automaatselt**.
1. Märkige **Ostutellimuse poliitikad** alal väljagrupi **Algne müügitellimus (otsetarne)** ruut **Sisesta arve automaatselt**. Märkige see ruut, kui soovite kontsernisisese hankija arve sisestamisel algse müügitellimuse arve automaatselt printida.

> [!NOTE]
> Arve prindisätted määratletakse mooduli, dokumendi või kande seadistamisega **Prindihalduse seadistus** lehel.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Algse müügitellimuse loomine väliskliendile

Läbige juriidilises isikus A järgmised etapid. See protseduur vastab joonisel kastile nr 1.

1. Avage jaotis **Müügireskontro \> Müügitellimused \> Kõik müügitellimused**.
1. Lehelt, kus on loend **Kõik müügitellimused**, saate luua algse müügitellimuse. Väljade väärtused kopeeritakse kliendikontolt müügitellimusele.
1. Lehel **Müügitellimus** valige toimingupaanilt suvand **Päisevaade**.
1. Märkige **Kontsernisiseste sätete** kiirkaardil ruut **Loo kontsernisisesed tellimused automaatselt**.
1. Kui soovite, et kontsernisisene hankija tarniks kauba otse väliskliendile, märkige ruut **Otsetarne**.
1. Kui olete müügitellimuse sisestamise lõpetanud, sulgege leht **Müügitellimus**.

Kontsernisisene ostutellimus luuakse automaatselt kõigile kaupadele, millele on määratud kontsernisisene hankija, ja seejärel luuakse kontsernisisene müügitellimus. Teavitusteates kuvatakse teade, et on loodud kontsernisisene ostutellimus ja kontsernisisene müügitellimus. Sõnum sisaldab ka nende tellimuste linke. Kui kaupa ei leitud, kuvatakse punane hoiatus, mis tähendab, et tellimuse loomise protsess ei olnud lõpetatud.

> [!NOTE]
> Kui loote mitu tellimust erinevates juriidilistes isikutes ja ühes juriidilises isikus kaupu ei leitud, peatub tellimuste loomine, sea ka nende juriidiliste isikute puhul, kes saaksid oma tellimuse täita.

## <a name="invoice-an-intercompany-sales-order"></a>Kontsernisisese müügitellimuse arveldamine

Kontsernisisese müügitellimuse arveldamisel arveldatakse automaatselt vastav kontsernisisene ostutellimus. Seejärel, kui algne müügitellimus on otsetarne tellimus, arveldatakse algne müügitellimus automaatselt.

Läbige juriidilises isikus B järgmised etapid. See protseduur vastab joonisel kastile nr 2.

1. Avage jaotis **Müügireskontro \> Müügitellimused \> Kõik müügitellimused**.
1. Loendilehel **Kõik müügitellimused** valige kontsernisisene müügitellimus.
1. Toimingupaanil valige vahekaart **Arve** ja seejärel valige uuesti **Arve**.
1. Valige märkeruut **Sisestamine**.
1. Valige müügitellimus ja seejärel **OK**.

Kontsernisisese müügitellimuse kliendiarve sisestatakse juriidilises isikus B automaatselt. Kontsernisisese hankija arve luuakse seejärel automaatselt ja sisestatakse juriidilises isikus A. Kui algne müügitellimus on seadistatud otsetarnena, luuakse juriidilises isikus A algsele müügitellimusele kliendiarve.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]