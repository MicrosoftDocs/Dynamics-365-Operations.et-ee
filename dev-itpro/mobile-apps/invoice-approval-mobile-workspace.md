---
title: "Arvete kinnitamise mobiilne tööruum"
description: "See teema annab teavet arvete kinnitamise mobiilse tööruumi kohta. See tööruum annab loendi arvetest, mis on määratud teile hankija arve päise töövooprotsessi kaudu."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 70f3e0fe53fc0b1daa471a7022f5659d09caa867
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="invoice-approvals-mobile-workspace"></a>Arvete kinnitamise mobiilne tööruum

[!include[banner](../includes/banner.md)]

See teema annab teavet **arvete kinnitamise** mobiilse tööruumi kohta. See tööruum annab loendi arvetest, mis on määratud teile hankija arve päise töövooprotsessi kaudu. 

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Ülevaade

**Arvete kinnitamise** mobiilne tööruum võimaldab ostureskontro ametnikel ja juhtidel vaadata arveid, mis on neile hankija arve päise töövooprotsessi käigus määratud. Saate vaadata arve andmeid ja isegi rea ja jaotuse üksikasju, mis aitab teil teha teadlikke kinnitamisotsuseid. Tööruumist saab teha toiminguid arve suunamiseks läbi töövooprotsessi. 

## <a name="prerequisites"></a>Eeltingimused

Enne selle mobiilse tööruumi kasutamist peavad olema täidetud järgmised eeltingimused.

<table>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Roll</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Teie organisatsioonis peab olema juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni 2017. aasta juuli värskendus.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.
</td>
</tr>
<tr class="even">
<td><strong>Arvete kinnitamise</strong> mobiilne tööruum tuleb avaldada.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus

Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.

-   [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse

1.  Käivitage rakendus oma mobiilses seadmes.
2.  Sisestage Microsoft Dynamics 365 URL.
3.  Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
4.  Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.

    [![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Arvete kinnitamine, kasutades arvete kinnitamise mobiilset tööruumi
1.  Valige oma mobiilses seadmes tööruum **Arvete kinnitamine**.
2.  Valige arve, mis on teile hankija arve päise töövooprotsessiga määratud.
3.  Vaadake lehel **Arve üksikasjad** üle arve päise teave, nt hankija ja kuupäeva andmed.
4.  Valige arvel rida, et vaadata selle kohta üksikasjalikumat teavet vaates **Arve rea üksikasjad**.
5.  Tehke vaates **Arve rea üksikasjad** valik **Jaotused** rea jaotuste kuvamiseks. Siin saate vaadata arve rea arvestust. Kuvatav teave hõlmab finantsdimensioone ja põhikontot.
6.  Tehke lehel **Arve rea üksikasjad** valik **Jaotused** kõigi jaotuste kuvamiseks. Siin saate vaadata kogu arve arvestust. Kuvatav teave hõlmab finantsdimensioone ja põhikontosid. 
7.  Valige **Manused** kõigi arvele manustatud märkmete või failide kuvamiseks.
8.  Valige lehelt **Arve üksikasjad** sobiv töövoog ülevaatuse protsessi lõpuleviimiseks.
9.  Valige suvand **Valmis**.
