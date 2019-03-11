---
title: Kulupoliitikate määratlemine
description: Saate määratleda kulupoliitikad, mida teie töötajad peavad järgima, kui nad rakenduses Microsoft Dynamics 365 for Finance and Operations kuluaruandeid ja reisiplaane sisestavad ning edastavad.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "342427"
---
# <a name="expense-policies"></a>Kulude poliitikad

[!include [banner](../includes/banner.md)]

Saate määratleda põhimõtted, mida teie töötajad peavad järgima, kui nad kuluaruandeid ja reisiplaane sisestavad ning edastavad.         
Kulupõhimõtete rakendamine võib aidata teil kulusid tõhusamalt hallata.         

Näiteks võite kehtestada New Yorgi hotellikulude kohta põhimõtte, et ühe öö maksumus hotellis ei tohi ületada 250 USA dollarit.       
Kui töötaja esitab kuluaruande või reisiplaani, milles toa maksumus ületab selle summa, teatab süsteem        
töötajale, et kulupoliitikas ettenähtud summat on ületatud. Poliitika määratlemisel saate konfigureerida teadet,        
mille töötaja saab.      
        
Määratleda saab kolme tüüpi poliitikaid.         
        
- Hoiatus – lubab töötajal kuluaruande või reisiplaani esitada, kuid kulu märgitakse kõigile kinnitajatele ja        
  hilisemaks aruandluseks.        

- Tõrge – nõuab töötajalt, et ta enne kuluaruande või reisiplaani esitamist kulu üle vaataks, nii et see vastaks poliitikale.       
 
  - Põhjendus – nõuab, et töötaja või juht sisestaks enne kuluaruande või reisiplaani esitamist põhjenduse poliitika summa ületamise kohta.        
 
  Seadistada saab ka kuupäevavahemiku, mille puhul kulupoliitikad kehtivad. Näiteks võivad lennukipiletite hinnad Taani      
  ja New York City vahel reisihooajal kõrged olla. Saate määratleda lennupiletite kulureegli, mis seab      
  New York City lendude hinnapiiriks 5000 taani krooni, ja võite täpsustada, et see reegel kehtib ajavahemikul 15. märtsist kuni      
  15. septembrini.
