---
title: Ostutellimuse kinnitamise mobiilne tööruum
description: Selles teemas antakse teavet ostutellimuse kinnitamise mobiilse tööruumi kohta, mis võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida. Näiteks võite ostutellimuse kinnitada või tagasi lükata.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8a1a9e62b542bfd46607da213225338354187e29caa94ba6e67f8c4ca38e5437
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781437"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Ostutellimuse kinnitamise mobiilne tööruum

[!include [banner](../includes/banner.md)]

See teema annab teavet **ostutellimuse kinnitamise** mobiilse tööruumi kohta. See tööruum võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida. Näiteks võite ostutellimuse kinnitada või tagasi lükata.
 
## <a name="overview"></a>Ülevaade 
Kinnitamist nõudvad ostutellimused läbivad kinnitamise töövoo. See töövoog võib sisaldada mitmesuguseid samme, mis nõuavad vähemalt ühe inimese tegevusi. Näiteks võib inimesel olla vaja mõni ülesanne täita või ostutellimus kinnitada. 

**Ostutellimuse kinnitamise** mobiilne tööruum võimaldab ostutellimusi mobiilselt seadmelt hõlpsasti vaadata ja neile reageerida. See tööruum võimaldab teha ka samu töövootegevusi, mida saate teha rakenduse veebikliendist.

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Supply Chain Managementi versioonist.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Eeltingimused, kui kasutate Supply Chain Managementi 
Kui teie organisatsioonis on juurutatud Supply Chain Management, peab süsteemiadministraator avaldama mobiilse tööruumi **Ostutellimuse heakskiitmine**. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Eeltingimused, kui kasutate rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 platvormivärskendusega 3 või uuemat
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
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avaldage <strong>ostutellimuse kinnitamise</strong> mobiilne tööruum.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus
Laadige alla ja installige Finance and Operationsi mobiilirakendus.

- [Androidi telefonide puhul](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse

1. Käivitage rakendus oma mobiilses seadmes.
2. Sisestage oma Microsoft Dynamics365 URL.
3. Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
4. Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.

![Ostutellimuse kinnitamise tööruum olemasolevate tööruumide loendis.](./media/po-workspaces.png)

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]