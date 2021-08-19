---
title: Dimensioonipõhise tooteetaloni jaoks koosluse loomine
description: Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 696cb96c6e934eaa44bfe6f51347df4541e5648f75f1ce07139787a1b235d69d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715767"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Dimensioonipõhise tooteetaloni jaoks koosluse loomine

[!include [banner](../../includes/banner.md)]

Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras. Esimesed 4 salvestust seadistavad andmed, mida on selle protseduuri lõpuleviimiseks vaja. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Seda ülesannet täidab tavaliselt toote koostaja.

## <a name="select-the-product"></a>Toote valimine

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Märkige loendis valitud rida.
    * Otsige üles väljastatud tooteetalon koos dimensioonipõhise konfiguratsiooni tehnoloogiaga, mille lõite esimese ülesande juhendis selles järjekorras.  
1. Valige tegevuste paanil käsk **Insener**.
1. Valige suvand **Koosluse versioonid**.

## <a name="create-new-bom-and-bom-version"></a>Uue koosluse ja koosluse versiooni loomine

1. Valige suvand **Uus**.
1. Valige **kooslus ja koosluse versioon**.
1. Sisestage väärtus väljale **Nimi**.
    * Tegevuskoha seadistamine  
    * Selles protseduuris ei määrata kooslusele konkreetset tegevuskohta.  
1. Valige nupp **OK**.
1. Valige suvand **Uus**.
    * Selles protseduuris lisame kooslusele neli rida. Kaks rida tähistavad kaabli suvandeid ja kaks rida tähistavad kartoteegi suvandeid.  
1. Märkige loendis valitud rida.
1. Sisestage või valige väärtus väljale **Kauba kood**.
    * Valige kauba number A0001, HDMI 6' kaablid.  
1. Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.
    * Valige kaabli konfiguratsioonigrupp, mis loodi juhendis 4 selles järjekorras.  
1. Valige suvand **Uus**.
    * Valige kauba number A0002, HDMI 12' kaablid.  
1. Märkige loendis valitud rida.
1. Sisestage või valige väärtus väljale **Kauba kood**.
1. Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.
    * Valige uuesti kaabli konfiguratsioonigrupp.  
1. Valige suvand **Uus**.
1. Märkige loendis valitud rida.
1. Sisestage või valige väärtus väljale **Kauba kood**.
    * Valige kauba number D0002 kartoteek.  
1. Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.
    * Valige kartoteegi konfiguratsioonigrupp sellele koosluse reale.  
1. Valige suvand **Uus**.
1. Märkige loendis valitud rida.
1. Sisestage või valige väärtus väljale **Kauba kood**.
    * Valige kauba number M0007 StandardCabinet viimase koosluse reana.  
1. Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.
    * Valige kartoteegi konfiguratsioonigrupp viimasele koosluse reale.  

## <a name="approve-and-activate"></a>Kinnita ja aktiveeri

1. Sulgege leht.
1. Valige **Kinnita**.
1. Valige või sisestage väärtus väljal **Kinnitaja**.
1. Valige *Jah* väljal **Kas soovite ka koosluse kinnitada?**.
1. Valige nupp **OK**.
1. Valige **Aktiveeri**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]