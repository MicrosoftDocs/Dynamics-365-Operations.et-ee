---
title: "Ostutellimuse kinnitamise mobiilne tööruum"
description: "Selles teemas antakse teavet ostutellimuse kinnitamise mobiilse tööruumi kohta, mis võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida. Näiteks võite ostutellimuse kinnitada või tagasi lükata."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 60744c2b90e64ac77155ba28cdc4fcf65fee1bb6
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a>Ostutellimuse kinnitamise mobiilne tööruum

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

See teema annab teavet **ostutellimuse kinnitamise** mobiilse tööruumi kohta. See tööruum võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida. Näiteks võite ostutellimuse kinnitada või tagasi lükata.
 
## <a name="overview"></a>Ülevaade 
Kinnitamist nõudvad ostutellimused läbivad kinnitamise töövoo. See töövoog võib sisaldada mitmesuguseid samme, mis nõuavad vähemalt ühe inimese tegevusi. Näiteks võib inimesel olla vaja mõni ülesanne täita või ostutellimus kinnitada. 

**Ostutellimuse kinnitamise** mobiilne tööruum võimaldab ostutellimusi mobiilselt seadmelt hõlpsasti vaadata ja neile reageerida. See tööruum võimaldab teha ka samu töövootegevusi, mida saate teha Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni veebikliendist.

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Finance and Operationsi versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Eeltingimused Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni (juuli 2017) kasutamisel 
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juuli 2017), peab süsteemiadministraator avaldama **ostutellimuse kinnitamise** mobiilse tööruumi. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Eeltingimused Microsoft Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused. 

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
<td>Rakendage KB 4017918.</td>
<td>Süsteemiadministraator</td>
<td>KB 4017918 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Ostutellimuse kinnitamine</strong>. KB 4017918 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avaldage <strong>ostutellimuse kinnitamise</strong> mobiilne tööruum.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus
Laadige alla ja installige Microsoft Dynamics 365 for Unified Operationsi mobiilirakendus.

- [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse

1. Käivitage rakendus oma mobiilses seadmes.
2. Sisestage Microsoft Dynamics 365 URL.
3. Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
4. Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.

![Ostutellimuse kinnitamise tööruum olemasolevate tööruumide loendis](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Vaadake teile määratud tellimusi
1. Valige oma mobiilses seadmes tööruum **Ostutellimuse kinnitamine**.
2. Valige **Mulle määratud tellimused** kõigi ostutellimuste vaatamiseks, mille puhul teil on palutud ostutellimuse kinnitamise töövoos midagi teha.
3. Valige tellimus. Lehel **Tellimuse üksikasjad** näete tellimuse päise andmeid ja ridu. Leiate juhiseid ka töövooülesandest.
4. Valige **Arvestuse jaotused** lehe **Arvestuse jaotuse päis** avamiseks.
5. Naaske lehele **Tellimuse üksikasjad** ja valige rida. Tellimuse rea üksikasjadest saate uurida ka reapõhiseid arvestuse jaotusi.

## <a name="complete-an-action-on-the-purchase-order"></a>Ostutellimusega tegevuse läbiviimine
Kui olete endale määratud ostutellimust vaadanud ja töövoo juhiseid lugenud, peaksite olema tegutsemiseks valmis.

1. Valige oma mobiilses seadmes tööruum **Ostutellimuse kinnitamine**.
2. Valige **Mulle määratud tellimused** kõigi ostutellimuste vaatamiseks, mille puhul teil on palutud ostutellimuse kinnitamise töövoos midagi teha.
3. Valige tellimus ja vaadake üksikasjade lehte.
4. Valige **Tegevused** olemasolevate tegevuste kuvamiseks. Saadaolevad toimingud olenevad teile määratud ülesandest.

    | Ülesande tegevus    | Kinnitamise tegevus  |
    |----------------|------------------|
    | Vii lõpule       | Kinnita          |
    | Tagasta         | Lükka tagasi           |
    | Taotle muudatust | Taotle muudatust   |
    | Delegaat       | Delegaat         |

5. Valige sobiv tegevus.
6. Sisestage lehele **Ülesande täitmine** kommentaar. Pange tähele, et kui valite tegevuse **Delegeeri**, siis peate valima kasutaja, kellele ülesanne delegeerida.
7. Valige suvand **Valmis**. Kui olete tööruumi uuendanud, ei ole ostutellimust enam teie loendis. 

