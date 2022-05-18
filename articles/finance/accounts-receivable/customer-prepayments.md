---
title: Kliendi ettemaksed
description: See teema kirjeldab, kuidas seadistada ja töödelda kliendi ettemakseid (nimetatakse ka kliendi deposiitideks).
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb0f2290a38d89d90ac0d30a59e21fb3e9a6d894
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691887"
---
# <a name="customer-prepayments"></a>Kliendi ettemaksed

[!include [banner](../includes/banner.md)]

Kliendi ettemakseid kasutatakse kliendilt makse saamiseks, kuid pole ühtegi arvet, mille suhtes makset tasakaalustada saab. Seda tüüpi makseid nimetatakse ka kliendi deposiitideks.

Kliendi ettemaksete seadistamise ja sellega töötamise protsess koosneb järgmistest põhietappidest.

1. Looge ettemaksetele kliendi sisestusreeglid.
2. Seadistage **Sisestamise profiil ettemaksu töölehekandega** parameeter.
3. Looge kliendimakse tööleht ja märkige iga rea puhul **Ettemaksu töölehe kanne** märkeruut.
4. Kliendi makse töölehe sisestamine
5. Pärast arve loomist tasakaalustage ettemaks kasutades **Seadista avatud kannete tasakaalustamine** lehte.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Looge ettemaksetele kliendi sisestamisprofiil

Tavaliselt, kui aktsepteerite klientide ettemakseid või deposiite enne kaupade või teenuste tarnimist või enne arve olemasolu süsteemis, soovite sularaha kirjendada kontoplaanil vara asemel kohustusena. Nende summade pearaamatusse kirjendamise nõuded võivad sõltuvalt teie riigist või regioonist erineda. Seetõttu konsulteerige kindlasti oma raamatupidajatega kehtivate kohalike määruste suhtes.

Üldiselt on sisestusreeglite loomise protsess, mida saab kasutada ettemaksete puhul, sama, mis teiste sisestusreeglite loomise protsessis. Peamine erinevus on põhikonto, mille valite **Summakonto** väljal. Lisateavet leiate teemast [Kliendi sisetamise profiil](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Määratlege kliendi ettemaksete parameetrid

Müügireskontros on kaks põhiparameetrit, mida peate kliendi ettemaksete süsteemi konfigureerimisel arvesse võtma. Parameetrite konfigureerimiseks tehke järgmist.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
2. Valikuline: Vahekaardil **Pearaamat ja käibemaks** kiirkaardil **Makse** määrake suvandile **Käibemaks ettemaksu töölehel** valik **Jah**.
3. Väljal **Sisestusreeglid ettemaksu töölehekandega** valige kliendi ettemaksete sisestamisel kasutamiseks kliendi sisestusreeglid.
4. Sulgege leht.

## <a name="create-customer-prepayment-vouchers"></a>Kliendi ettemakse kannete loomine

Kui loote kliendimakse töölehe iga ettemakse kohta, peate **Ettemaksu töölehe kande** valiku väärtuseks seaadistama **Jah** **Kliendi makse töölehe** lehel. Kliendi ettemakse loomiseks tehke järgmist.

1. Avage **Müügireskontro \> Maksed \> Kliendi makse tööleht**.
2. Valige **Uus**, et luua uus tööleht.
3. Valige väljal **Nimi** töölehe nimi, mida kasutatakse.

    > [!IMPORTANT]
    > Kui määrate eelmises protseduuris valiku **Ettemakse töölehekande käibemaksu** väärtuseks **Jah**, peate valima töölehe nime, kus on valitud parameeter **Summa sisaldab käibemaksu**. 

4. Valikuline: Sisestage väljale **Kirjeldus** detailne kirjeldus.
5. Valige **Read**.
6. Kui tühja rida pole olemas, valige **Uus** rea loomiseks.
7. Väljale **Kuupäev** sisestage kuupäev, millal ettemaks tuleks sisestada.
8. Väljal **Konto** valige klient järgmise makse jaoks.
9. Valikuline: Sisestage väljale **Kirjeldus** detailne kande kirjeldus.
10. Väljale **Kreedit** sisestage ettemaksu summa.
11. Väljal **Vastaskonto** valige konto millele makse tasaarvestada. Näiteks valige pank või põhikonto, mille jaoks makse sisestate.
12. Väljale **Makseviis** sisestage kliendi makse viis.
13. Seadke **Makse** vahekaardil **Ettemakse töölehekande** valiku väärtuseks **Jah**.
14. Korrake samme 7 kuni 13 iga täiendava ettemakse puhul, mida tuleb sisestada.
15. Valige **Postita** töölehtede ridade sisestamiseks.

## <a name="settle-prepayments-with-invoices"></a>Ettemaksete tasakaalustamine arvetega

Saate kasutada **Kliendimaksete** tööruumi, et lihtsalt leida ja tasakaalustada makseid, mis pole täielikult tasakaalustatud.

1. Valige **Avakuva** juhtpaneelil **Kliendimaksete** paneel.
2. Tasakaalustamiseks otsige ja valige makse jaotises vahekaardil **Kliendi kanded** **Tasakaalustamata maksed**.
3. Valige **Kannete tasakaalustamine**.
4. Valige **Märke** ruut arve jaoks ja makse jaoks, mida tasakaalustatakse.
5. Valige **Sisesta**.

Lisateavet avatud kannete tasakaalustamise kohta vt [tasakaalustamise ülevaade](/dynamics365/finance/cash-bank-management/settlement-overview).
