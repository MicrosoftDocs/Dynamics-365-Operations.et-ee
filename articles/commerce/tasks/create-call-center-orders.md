---
title: " Kõnekeskuse tellimuste loomine"
description: See artikkel läbib näideprotseduuri, kus kõnekeskuse kasutaja otsib klienti, loob uue tellimuse, otsib toote ja kogub kliendilt makset Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228506"
---
# <a name="create-call-center-orders"></a> Kõnekeskuse tellimuste loomine

[!include [banner](../includes/banner.md)]

See artikkel läbib näideprotseduuri, kus kõnekeskuse kasutaja otsib klienti, loob uue tellimuse, otsib toote ja kogub kliendilt makset Microsoft Dynamics 365 Commerce. Protseduur kasutab USRT-demo andmeettevõtet ja on mõeldud müügitellimuse ametnikule. 

## <a name="prerequisites"></a>Eeltingimused

Protseduuri sooritanud kasutaja tuleb seadistada kõnekeskuse kasutajana. Valikuliselt saab Fabrikami poolaasta kataloogi avaldada vähemalt ühe lähtekoodiga.

### <a name="add-yourself-as-a-call-center-user"></a>Lisa ennast kõnekeskuse kasutajaks

Enda lisamiseks kõnekeskuse kasutajana järgige neid samme.

1. Minge Commerce Headquartersi jaemüügi ja ärikanalite **\> kõnekeskustesse \>\> Kõik kõnekeskused**.
1. **Valige väljal** Kasutajad suvand **Kanali kasutajad**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage **väljale Kasutaja ID** oma kasutaja ID.
1. **Sisestage väljale** Nimi oma kasutajanimi. Kasutajanimi võib olla sama mis kasutaja ID.
1. Valige toimingupaanil nupp **Salvesta**.
1. Minge tagasi jaemüügi **ja ärikanalite \> kõnekeskustesse \>\> Kõik kõnekeskused**.
1. Valige kõnekeskuse jaemüügikanali ID.
1. Veenduge, et **suvand Luba tellimuse lõpetamine** oleks seatud väärtusele **Jah**. Kui valik pole nähtav, võite selle sammu vahele jätta.

## <a name="complete-the-example-call-center-procedure"></a>Kõnekeskuse näidisprotseduuri lõpule viimine

Kõnekeskuse protseduuri näidete lõpuleviimiseks järgige neid samme.

1. Avage **Jaemüük ja kaubandus \> Kliendid \> Klienditeenindus**.
1. **Kliendi otsimise** vahekaardil sisestage otsingukriteeriumid kliendi otsimiseks. Selle näite protseduuri puhul sisestage **Karen**.
1. Valige **Otsi**. Kuvatakse **kliendi otsingu** dialoogiboks ja kuvatakse otsingutulemuste loend.
1. Valige Karen Karen Kareni kliendikirje, mille kliendikood on **2001**, ja seejärel valige **suvand Vali**.**·**
1. Tegevuspaanil valige **uus müügitellimus**.
1. Valige paremalt vahekaart **Päis**.
1. Valige tarneviisi **väljal** Tarne **kiirkaardil** **99 Standardne**.

    ![Tarneviisi valimine.](../media/Select_Mode_of_Delivery.png)

1. Paremal valige vahekaart **Read**.
1. **Sisestage uue** müügirea uue **rea** jaotises Müügitellimuse read otsimiseks kaubakood väljale Kaubakood. Selle näite protseduuri puhul sisestage **81327** ja valige seejärel ripploendist toode, et lisada see müügitellimusele.
1. **Sisestage** müügikogus väljale Kogus.
1. **Valige väljal** Lähtekood kataloogi lähtekood. Kui aktiivseid lähtekoodisid pole, võite selle sammu vahele jätta.
1. Tegevuspaanil valige kliendimakse **hõivamiseks** suvand Lõpeta. See toiming avab dialoogiboksi **Müügitellimuse kokkuvõte**, mis näitab tähtaegu kogusummat. See tegevus käivitab ka tasude arvutamise (nt lähetuse ja käsitsemise) ning näitab neid müügitellimuse **kokkuvõtte** dialoogiboksis.

    ![Nupp Lõpeta.](../media/Complete_button.png)

1. **Maksete hõivamiseks** valige kiirkaardi **Maksed dialoogiboksis** **Müügitellimuse** kokkuvõte suvand Lisa.

    ![Müügitellimuse kokkuvõtte dialoogiboks.](../media/order_summary.png)

1. **Valige makseviis väljalt** **Sisestage kliendi** makseteave väljal Makseviis. Selle näite protseduuri puhul valige **Sularaha**.
1. **Sisestage maksesumma** väljale Maksesumma. Selle näite puhul sisestage **120,00**, **mis võrdub tellimuse saldoga, mis kuvatakse müügitellimuse kokkuvõtte** dialoogiboksis. Selle summa sisestamisega saate tellimuse täielikult tasutuks täita.
1. Valige nupp **OK**.
1. Valige käsk **Esita**.

## <a name="additional-resources"></a>Lisaressursid

[Tehingumeilide kohandamine tarneviisi alusel](../customize-email-delivery-mode.md)

[Kassas tarneviisi muutmine](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
