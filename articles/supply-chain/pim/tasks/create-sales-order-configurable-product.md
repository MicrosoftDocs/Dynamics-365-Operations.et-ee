---
title: Müügitellimuse loomine konfigureeritava toote jaoks
description: See protseduur näitab, kuidas rakendada müügitellimusel tootele konfiguratsioonimalli.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f128518af01911a29ae297670883ef425f9117d65cc952cc1ffdb044c4ce085f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781898"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Müügitellimuse loomine konfigureeritava toote jaoks

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas rakendada müügitellimusel tootele konfiguratsioonimalli. Selles näites kasutatakse demoettevõtte USMF kõlarimudelit D0006. Tavaliselt kasutab seda protseduuri müügitellimuste töötleja.

## <a name="create-a-sales-order"></a>Loo müügitellimus

1. Minge **müügi ja turunduse \> tööruumides \> müügitellimuse töötlemisele ja päringule**.
1. Valige suvand **Uus**.
1. Valige **Müügitellimus**.
1. Valige *US-001* väljalt **Kliendi konto**. 
1. Valige nupp **OK**.
1. Valige väljal **Kaubakood** väärtus *D0006*.
    * Selle ülesande jaoks tuleb valida konfigureeritav toode.  
1. Klõpsake valikut  **Toode ja tarnimine**.
1. Valige **Konfigureeri joont**.
    * Pange tähele, et hind on valitud konfiguratsiooni põhjal muudetud ja välja **Lisa kaabel** väärtuseks on nüüd määratud *True*.  
    * Pange tähele kaabli jaoks valitud vaikehinda ja sätteid.  
1. Valige **Malli laadimine**.
    * Selles näites näete, kuidas rakendada malli eelmääratud konfiguratsiooni valimiseks. Kui kasutate seda protseduuri tegevuse juhisena soovite näha teisi saadaolevaid atribuudiväärtusi, peate klõpsama nuppu **Ava**.  
1. Valige nupp **OK**.
1. Valige nupp **OK**.
1. Laiendage jaotist **Rea üksikasjad**.
1. Valige vahekaart **Toode**.
    * Kauba konfiguratsioon on nüüd loetletud tootedimensioonide all.  
1. Sulgege leht.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]