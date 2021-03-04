---
title: Finantsaruandluse KKK
description: Sellesse teemasse on kogutud teiste kasutajate esitatud finantsaruandlusega seotud küsimused.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070213"
---
# <a name="financial-reporting-faq"></a>Finantsaruandluse KKK 

Sellesse teemasse on kogutud teiste kasutajate esitatud finantsaruandlusega seotud küsimused. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Kuidas piirata turvapuu abil juurdepääsu aruandele?

Stsenaarium: USMF-i demoettevõte ei soovi, et tema bilansi aruanne oleks D365-s nähtav kõigile finantsaruandluse kasutajatele. Lahendus: turvapuu abil saate piirata juurdepääsu ühele aruandele nii, et sellele oleks juurdepääs ainult teatud kasutajatel. 

1.  Logige sisse finantsaruandluse aruandekoosturisse.

2.  Looge uus puu definitsioon (Fail | Uus | Puu definitsioon) a.    Topeltklõpsake veerus **Üksuse turve** rida **Kokkuvõte**.
  i.    Klõpsake suvandit Kasutajad ja rühmad.  
          1. Valige kasutaja(d) või rühm, kellele soovite lubada juurdepääsu sellele aruandele. 
          
[![kasutaja ekraan](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![turbeekraan](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Klõpsake nuppu **Salvesta**.
  
[![salvestamisnupp](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Lisage aruandedefinitsioonis uus puu definitsioon.

[![puu definitsiooni vorm](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Asudes puu definitsioonis klõpsake nuppu Säeadistamine ja märkige jaotises „Aruandlusüksuse valik“ ruut „Kaasa kõik üksused“.

[![aruandlusüksuse valiku vorm](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Enne:** [![enne-kuvatõmmis](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Pärast:** [![pärast-kuvatõmmis](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Märkus. Ülaltoodud teate põhjuseks on, et pärast Üksuse turbe rakendamist pole minu kasutajal sellele aruandele juurdepääsu



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Kuidas määratleda, milline konto või millised kontod pole vastavuses minu saldodega D365-s?

Kui teil on aruanne, mis ei vasta D365-s eeldatud olukorrale, võivad järgmised tegevused aidata teil selliseid kontosid ja hälbeid tuvastada. 

### <a name="in-financial-reporter-report-designer"></a>Finantsaruandluse aruandekoosturis

1.  Looge uus readefinitsioon a.    Klõpsake Redigeeri | Lisa read dimensioonidest i.  Valige MainAccount [![Valige Peaekraan_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Klõpsake nuppu Ok b.    Salvestage readefinitsioon

2.  Looge uus veerudefinitsioon     [![Looge uus veerudefinitsioon](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Looge uus aruandedefinitsioon a.    Klõpsake Sätted ja tühjendage märkeruut [![Sätetevorm](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Looge aruanne. 

5.  Eksportige aruanne Excelisse.

### <a name="in-d365"></a>D365-s: 
1.  Klõpsake Pearaamat | Päringud ja aruanded | Proovibilanss a.    Parameetrid i.  Alguskuupäev: rahandusaasta algus ii. Kuupäevani: kuupäev, millal lõite iii. aruande    Finantsdimensioonikogum „Põhikonto kogum“ [![Põhikonto vorm](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Klõpsake valikut Arvuta

2.  Eksportige aruanne Excelisse

Nüüd saate kopeerida andmeid FR Exceli aruandest D365 proovibilansi aruandesse ja võrrelda veerge „Sulgemissaldo“.
