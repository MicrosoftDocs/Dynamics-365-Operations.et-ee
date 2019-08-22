---
title: Kulupoliitikate määratlemine
description: Saate määratleda kulupoliitikad, mida teie töötajad peavad järgima, kui nad rakenduses Microsoft Dynamics 365 for Finance and Operations kuluaruandeid ja reisiplaane sisestavad ning edastavad.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840885"
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

## <a name="policy-tips"></a>Poliitika näpunäited
Siin on mõned soovitused, millest on kasu uue kuluhalduse poliitika loomisel. 
* Poliitikatel on jõustumiskuupäevad ja need ei jõustu, kui poliitika luuakse pärast kulu tekkimise kuupäeva. Näiteks kui loote täna uue poliitika, et kehtestada maksimaalseks eine kuluks 50 dollarit, siis kõiki eile sisestatud kulusid ei kontrollita selle poliitika suhtes.
* Kui loote kulukategooria jaoks poliitika, mida saab üksikasjalikult kasutada, kaaluge kulurea tüübi tingimuse lisamist. Mõned poliitikad, nagu kviitungi nõudmine, ei pruugi olla konkreetsete üksikasjalike ridade jaoks sobilikud ja neid tuleks rakendada ainult päise või üksikasjalikustamata reale. 

## <a name="when-to-evaluate-policies"></a>Millal hinnata poliitikaid

Kuluhalduse parameetrites on võimalus hinnata kuluhalduse poliitikaid, kui rida on salvestatud, või kui kuluaruanne on esitatud. Kui otsustate hinnata salvestatud rida, siis tagab see, et kasutajatel on varem võimalik näha, mida nad peavad tegema, et lõpetada kõik kuluaruanded korraga. Võite ka poliitika hindamise edasi lükata ja aega säästa, kui kontrollimine toimub lõpus, töövoogu esitamise ajal.
