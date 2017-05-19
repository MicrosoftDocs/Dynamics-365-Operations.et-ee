---
title: Dynamics 365 for Operationsi mobiilirakenduse koduleht
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Operationsi mobiilirakendust ja antakse linke ressurssidele, mis aitavad teil seda oma organisatsioonis juurutada.
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Dynamics 365 for Operationsi mobiilirakenduse koduleht

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse Microsoft Dynamics 365 for Operationsi mobiilirakendust ja antakse linke ressurssidele, mis aitavad teil seda oma organisatsioonis juurutada.

<a name="overview"></a>Ülevaade
--------

Microsoft Dynamics 365 for Operationsi mobiilirakendus võimaldab teie organisatsioonil teha äriprotsessid kättesaadavaks mobiilsetes seadmetes. Kui teie IT-administraator on organisatsiooni jaoks mobiilsete tööruumide funktsiooni luabnud, saavad kasutajad rakendusse sisse logida ja hakata äriprotsesse oma mobiilsetest seadmetest kohe käitama. Dynamics 365 for Operationsi mobiilirakendus sisaldab järgmisi funktsioone, mis võivad aidata tootlikkust tõsta.

-   Kasutajad saavad äriandmeid vaadata, redigeerida ja nendega tegeleda, isegi kui võrguühendus on katkendlik või mobiilne seade on täiesti võrguühenduseta. Seadme võrguühenduse taastumisel sünkroonitakse võrguühenduseta andmed automaatselt Dynamics 365 for Operationsiga.
-   IT-administraatorid või arendajad saavad luua ja avaldada mobiilseid tööruume, mis on kohandatud nende organisatsioonile. Rakendus kasutab teie olemasolevaid koodilõike. Seega ei pea te oma valideerimisprotseduure, äriloogikat ega turbekonfiguratsiooni uuesti juurutama.
-   IT-administraatorid või arendajad saavad mobiilseid tööruume hõlpsasti kujundada, kasutades Dynamics 365 for Operationsi veebikliendis sisalduvat klõpsatavat tööruumikujundajat.
-   IT-administraatorid või arendajad saavad soovi korral optimeerida ka tööruumide võrguühenduseta võimalusi, kasutades äriloogika laiendatavuse raamistikku. Kuna andmete töötlemine jätkub, kui seade on võrguühenduseta, püsivad teie mobiilsed stsenaariumid rikkalikud ja sujuvad, isegi kui seadmetel pole pidevat võrguühendust.

## <a name="elements-of-the-mobile-app"></a>Mobiilirakenduse elemendid
Mobiilirakenduse navigeerimispaan koosneb neljast lihtsast osast: armatuurlaud, tööruumid, lehed ja tegevused. 

[![Navigeerimispaani põhimõtted mobiilirakenduses](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Rakenduse käivitamisel avaneb **armatuurlaud**.
-   Armatuurlaual näete loendit **tööruumidest**, mis on avaldatud teie Dynamics 365 for Operationsi keskkonnas.
-   Igas tööruumis näete loendit **lehtedest**, mis on selle tööruumi jaoks saadaval.
-   Lehel saate vaadata andmeid, mis on kogutud Dynamics 365 for Operationsi ühelt või mitmelt lehelt.
-   Saate lehelt navigeerida teistele lehtedele seotud andmete nägemiseks, nagu üksuse üksikasjad või read.
-   Lehel kuvatakse ka loend **tegevustest**, mis on selle lehe puhul saadaval.
-   Tegevused võimaldavad teil andmeid luua või olemasolevaid andmeid muuta.

## <a name="implementation-process"></a>Juurutusprotsess
Järgmisel joonisel jyvatajse Dynamics 365 for Operationsi mobiilirakenduse juurutamise protsess teie organisatsioonis. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

Järgmises tabelis on toodud lingid ressurssidele, mis aitavad teil Dynamics 365 for Operationsi mobiilirakendust oma organisatsioonis juurutada. Esimeses veerus toodud numbrid vastavad eelmisel joonisel kujutatud nummerdatud etappidele.

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
<td>Juurutage Dynamics 365 for Operations organisatsioonile.</td>
<td>Kui teie organisatsioonis pole Dynamics 365 for Operations veel juurutatud, vt teemat <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operationsi demokeskkonna juurutamine</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Süsteemiadministraator</td>
<td>Laadige alla ja installige KB-d, mis lubavad Microsofti pakutavad mobiilsed tööruumid.</td>
<td>Vaadake teema jaotisest &quot;Eeltingimused&quot; teavet mobiilse tööruumi kohta, mida teie organisatsioon soovib kasutada.
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Kulujuhtimise mobiilsed tööruumid</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobiilse tööruumi varude laoseis</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Müügitellimuste mobiilsed tööruumid</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Hankija koostöö mobiilne tööruum</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobiilse tööruumi projekti ajakirje</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Süsteemiadministraator</td>
<td>Avaldage Microsofti pakutavad mobiilsed tööruumid.</td>
<td>Vaadake teema jaotisest &quot;Eeltingimused&quot; teavet mobiilse tööruumi kohta, mida teie organisatsioon soovib kasutada.
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Kulujuhtimise mobiilsed tööruumid</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobiilse tööruumi varude laoseis</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Müügitellimuste mobiilsed tööruumid</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Hankija koostöö mobiilne tööruum</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobiilse tööruumi projekti ajakirje</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>Arendaja või sõltumatu tarkvaratarnija (ISV)</td>
<td>Kasutage Dynamics 365 for Operationsi mobiilset raamistikku kohandatud mobiilsete tööruumide loomiseks.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operationsi mobiilne raamistik</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Dynamics 365 for Operationsi tööruumi X++ API-d</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Looge kohandatud mobiilseid tööruume sisaldav juurutatav pakett ja laadige see üles Microsoft Dynamicsi elutsükliteenustesse (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Juurutatava paketi loomine</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Süsteemiadministraator</td>
<td>Rakendage ISV pakutavaid kohandatud tööruume sisaldav juurutatav pakett.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Microsoft Dynamicsi 365 for Operationsi juurutatava paketi rakendamine</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Süsteemiadministraator</td>
<td>Avaldage ISV pakutavad kohandatud mobiilsed tööruumid.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Kasutaja</td>
<td>Laadige alla ja installige Dynamics 365 for Operationsi mobiilirakendus.</td>
<td><ul>
<li>Androidile: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations Google Play Store’is</a></li>
<li>iPhone’ile: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations iTunes apps store’is</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Kasutaja</td>
<td>Logige sisse ja kasutage Dynamics 365 for Operationsi mobiilirakendust. Rakendus sisaldab avaldatud mobiilseid tööruume.</td>
<td>Microsoft pakub järgmisi mobiilseid tööruume.
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Kulujuhtimise mobiilsed tööruumid</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobiilse tööruumi varude laoseis</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Müügitellimuste mobiilsed tööruumid</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Hankija koostöö mobiilne tööruum</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobiilse tööruumi projekti ajakirje</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Vt ka
--------

[Dynamics 365 for Operationsi mobiilirakenduse jaoks hiljuti välja antud mobiilsed tööruumid](mobile-workspaces-released.md)





