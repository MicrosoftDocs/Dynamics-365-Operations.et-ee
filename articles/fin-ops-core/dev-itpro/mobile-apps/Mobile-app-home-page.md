---
title: Mobiilirakenduse avaleht
description: See artikkel kirjeldab finantside ja toimingute (Dynamics 365) mobiilirakendust ning sisaldab linke ressurssidele, mis aitavad teil seda organisatsioonis juurutada.
author: sericks007
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.custom: intro-internal
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.openlocfilehash: a0979df7c0cd685f810c0ab743fbede740e7aacb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284064"
---
# <a name="mobile-app-home-page"></a>Mobiilirakenduse avaleht

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

See artikkel kirjeldab **Finantside ja toimingute (Dynamics 365)** mobiilirakendust ja sisaldab linke ressurssidele, mis aitavad teil seda organisatsioonis juurutada.

## <a name="overview"></a>Ülevaade

Mobiilirakendus võimaldab teie organisatsioonil teha äriprotsessid kättesaadavaks mobiilsetes seadmetes. Kui teie IT-administraator on organisatsiooni jaoks mobiilsete tööruumid lubanud, saavad kasutajad rakendusse sisse logida ja hakata äriprotsesse oma mobiilsetest seadmetest kohe käitama. Mobiilirakendus sisaldab järgmisi funktsioone, mis võivad aidata tootlikkust tõsta.

- Kasutajad saavad äriandmeid vaadata, redigeerida ja nendega tegeleda, isegi kui võrguühendus on katkendlik või mobiilne seade on täiesti võrguühenduseta. Seadme võrguühenduse taastumisel sünkroonitakse võrguühenduseta andmed automaatselt.
- IT-administraatorid või arendajad saavad luua ja avaldada mobiilseid tööruume, mis on kohandatud nende organisatsioonile. Rakendus kasutab teie olemasolevaid koodilõike. Seega ei pea te oma valideerimisprotseduure, äriloogikat ega turbekonfiguratsiooni uuesti juurutama.
- IT-administraatorid või arendajad saavad mobiilseid tööruume hõlpsasti kujundada, kasutades veebikliendis sisalduvat klõpsatavat tööruumikujundajat.
- IT-administraatorid või arendajad saavad soovi korral optimeerida ka tööruumide võrguühenduseta võimalusi, kasutades äriloogika laiendatavuse raamistikku. Kuna andmete töötlemine jätkub, kui seade on võrguühenduseta, püsivad teie mobiilsed stsenaariumid rikkalikud ja sujuvad, isegi kui seadmetel pole pidevat võrguühendust.

## <a name="elements-of-the-mobile-app"></a>Mobiilirakenduse elemendid
Mobiilirakenduse navigeerimispaan koosneb neljast peamisest osast: armatuurlaud, tööruumid, lehed ja tegevused. 

[![Navigeerimispaani põhimõtted mobiilirakenduses.](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Rakenduse käivitamisel avaneb **armatuurlaud**.
2. Armatuurlaual näete avaldatud **tööruumide** loendit.
3. Igas tööruumis näete loendit **lehtedest**, mis on selle tööruumi jaoks saadaval.
4. Lehel olles saate teha mitut toimingut. Järgmisena on toodud mõned näited.

    - Üksikasjalike andmete kuvamine.
    - Lehelt teistele lehtedele navigeerimine seotud andmete nägemiseks, nagu üksuse üksikasjad või read.
    - Selle lehe puhul kasutatavate **toimingute** loendi kuvamine. Tegevused võimaldavad teil andmeid luua või olemasolevaid andmeid muuta.

## <a name="implementation-process"></a>Juurutusprotsess
Järgmisel joonisel on näidatud nii Microsofti pakutavate kui ka kohandatud mobiilsete tööruumide juurutusprotsess. 

[![Mobiilirakenduste juurutamise protsess.](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

Järgmises tabelis on lingid ressursside juurde, mis aitavad juurutada nii Microsofti pakutavaid kui ka kohandatud mobiilseid tööruume. Esimeses veerus toodud numbrid vastavad eelmisel joonisel kujutatud nummerdatud etappidele.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Etapp</th>
<th>Roll</th>
<th>Tegevus</th>
<th>Ressursid, mis aitavad teil tegevusi lõpule viia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Süsteemiadministraator</td>
<td>Juurutage finantsid ja toimingud teie organisatsioonis.</td>
<td><ul><li>Kui te e&#39;i ole veel ühtegi Microsoft Dynamics 365 versiooni juurutanud, vt jaotist <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.</li><li>Kasutatavate mobiilsete tööruumide loendi leiate jaotisest <a href="mobile-workspaces-released.md">Hiljuti välja antud mobiilsed tööruumid</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Süsteemiadministraator</td>
<td><strong>Kui kasutat&#39;e Microsoft Dynamics 365 for Operationsi versiooni 1611:</strong> laadige alla ja installige KB-d, mis lubavad Microsofti pakutavad mobiilsed tööruumid.</td>
<td>Lisateavet vt järgmistest teemadest.
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Kulujuhtimise mobiilsed tööruumid</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiilse tööruumi varude laoseis</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Müügitellimuste mobiilsed tööruumid</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Hankija koostöö mobiilne tööruum</a></li>
<li><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Mobiilse tööruumi projekti ajakirje</a></li>
<li><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Kuluhalduse mobiilne tööruum</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Süsteemiadministraator</td>
<td>Avaldage Microsofti pakutavad mobiilsed tööruumid.</td>
<td><a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Arendaja või sõltumatu tarkvaratarnija (ISV)</td>
<td>Kasutage mobiilset platvormi kohandatud mobiilsete tööruumide loomiseks.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobiilne platvorm</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Looge kohandatud mobiilseid tööruume sisaldav juurutatav pakett ja laadige see üles teenusesse Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Juurutatava paketi loomine</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Süsteemiadministraator</td>
<td>Rakendage sõltumatu tarkvaratarnija (ISV) pakutavaid kohandatud tööruume sisaldav juurutatav pakett.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Süsteemiadministraator</td>
<td>Avaldage ISV pakutavad kohandatud mobiilsed tööruumid.</td>
<td><a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Kasutaja</td>
<td>Laadige alla ja installige mobiilirakendus.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finantside ja toimingute rakendus<a0/& jaoks Android</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finantside ja toimingute rakendus iOS-i jaoks</a><BR/>
(Windows Phone’i ei toetata)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Kasutaja</td>
<td>Logige mobiilirakendusse sisse ja kasutage seda. Rakendus sisaldab süsteemiadministraatori avaldatud mobiilseid tööruume.</td>
<td>Microsofti pakutavate mobiilsete tööruumide loendi leiate jaotisest <a href="mobile-workspaces-released.md">Hiljuti välja antud mobiilsed tööruumid</a>.
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a>Tõrkeotsing
[Mobiiliplatvormi ressursid](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

