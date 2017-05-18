---
title: "Kulude halduse mobiilne tööruum"
description: "See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva kulude haldamise mobiilse tööruumi kohta. See tööruum võimaldab kasutajatel kviitungeid salvestada ja üles laadida, et neid hiljem kuluaruandele lisada. Mobiilne tööruum võimaldab kasutajatel ka kiiresti luua kuluridu, kasutades lisatud kviitungit."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Kulude halduse mobiilne tööruum

[!include[banner](../includes/banner.md)]

„[!include[banner](../includes/banner.md)]”


See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva kulude haldamise mobiilse tööruumi kohta. See tööruum võimaldab kasutajatel kviitungeid salvestada ja üles laadida, et neid hiljem kuluaruandele lisada. Mobiilne tööruum võimaldab kasutajatel ka kiiresti luua kuluridu, kasutades lisatud kviitungit.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Kulude halduse mobiilse tööruumi ülevaade
---------------------------------------------------

Paljud ettevõtted nõuavad, et reisiga seotud või äriga seotud kuluaruandele, mille töövõtja korvamiseks esitab, lisatakse kviitungi koopia. Mobiilne tööruum **Kulude haldus** võimaldab kasutajatel kiiresti luua oma valitud mobiilses seadmes uusi kuluridu, kasutades lisatud fotot kviitungist. Teise võimalusena saavad kasutajad jäädvustada kviitungist foto ja lisada selle kuluaruandele hiljem. Täpsemalt võimaldab mobiilne tööruum **Kulude haldamine** teha kasutajal järgmist.

-   Kviitungist foto tegemine ja selle üleslaadimine Microsoft Dynamicsi 365 for Operationsisse. Seejärel saab kasutaja lisada selle foto hiljem kuluaruandele.
-   Faili üleslaadimine salvestatud kviitungina. Seejärel saab kasutaja lisada selle faili hiljem kuluaruandele.
-   Uue kulurea loomine, kasutades lisatud kviitungit. Seejärel saab kasutaja lisada selle reaüksuse hiljem kuluaruandele ning esitada selle heakskiitmiseks ja korvamiseks.

Selle teema ülejäänud jaotistes selgitatakse, kuidas mobiilset tööruumi **Kulude haldamine** seadistada ja kasutada.

## <a name="prerequisites"></a>Eeltingimused
Enne mobiilse tööruumi **Kulude haldamine** juurutamist veenduge, et teie süsteemiadministraator oleks täitnud järgmised eeltingimused.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Roll</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Juurutatud peab olema Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuemaga.</td>
<td>Süsteemiadministraator</td>
<td>Kui teie organisatsioonis pole Dynamics 365 for Operations veel juurutatud, peaks süsteemiadministraator vaatama teemat <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operationsi demokeskkonna juurutamine</a>.</td>
</tr>
<tr class="even">
<td>Juurutatud peab olema KB 4019015.</td>
<td>Süsteemiadministraator</td>
<td>KB 4019015 (X ++ värskendus või metaandmete kiirparandus) sisaldab tarneahela haldamiseks nelja mobiilset tööruumi. KB 4019015 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li>Laadima KB 4019015 alla Microsoft Dynamicsi elutsükliteenustest (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Looma juurutatava paketi</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ExpenseMobile</strong>, ning seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Rakendama juurutatavat paketti</a> teie Microsoft Dynamics 365 for Operationsi süsteemile.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobiilne tööruum <strong>Kulude haldamine</strong> tuleb avaldada Dynamics 365 for Operationsi mobiilirakenduses.</td>
<td>Süsteemiadministraator</td>
<td><ol>
<li>Käivitage oma brauseris rakendus Dynamics 365 for Operations.</li>
<li>Valige lehel <strong>Süsteemiparameetrid</strong> suvand <strong>Mobiilsete tööruumide haldamine</strong>.</li>
<li>Valige tööruum <strong>Kulude haldamine</strong>.</li>
<li>Klõpsake nuppu <strong>Mobiilse tööruumi avaldamine</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operationsi mobiilirakenduse alla laadimine ja installimine
Laadige mobiilirakenduste poest alla mobiilirakendus Microsoft Dynamics 365 for Operations ja installige see.

-   Androidile: [Dynamics 365 for Operations Google Play Store’is](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone’ile: [Dynamics 365 for Operations iTunes apps store’is](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   Windows phone’ile (universaalne Windowsi platvorm \[UWP\]): tuleb peagi!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Logige sisse, et kasutada Dynamics 365 for Operationsi mobiilirakendust
1.  Käivitage rakendus oma mobiilses seadmes.
2.  Sisestage oma Dynamics 365 for Operationsi URL.
3.  Sisestage ettevõte, millesse soovite sisse logida. Näiteks sisestage **USMF**.
4.  Esmakordsel sisselogimisel palutakse teil sisestada oma Dynamics 365 for Operationsi konto kasutajanimi ja parool. Sisestage oma identimisteave.
5.  Pärast sisselogimist näete oma ettevõtte jaoks saadaolevaid tööruume. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem. Võite mobiilsete tööruumide loendi värskendamiseks tõmmata. [![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kviitungi salvestamine, kasutades kulude haldamise mobiilset tööruumi
1.  Valige oma mobiilses seadmes tööruum **Kulude haldamine**.
2.  Valige suvand **Salvesta kviitung**.
3.  Valige suvand **Tee foto** või **Vali pilt**.
4.  Kui valisite suvandi **Tee foto**, toimige järgmiselt.
    1.  Avaneb teie mobiilse seadme kaamera, et saaksite kviitungist foto jäädvustada. Kui foto on tehtud, klõpsake selle aktsepteerimiseks nuppu **OK**.
    2.  Valikuline: saate sisestada fotole pealkirja ja märkused.

     Kui aga valisite suvandi **Vali pilt**, toimige järgmiselt.
    1.  Valige loendist pilt.
    2.  Valikuline: saate sisestada pildile pealkirja ja märkused.

5.  Valige suvand **Valmis**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Kiire kulusisestus, kasutades kulude haldamise mobiilset tööruumi
1.  Valige oma mobiilses seadmes tööruum **Kulude haldamine**.
2.  Valige suvand **Kiire kulusisestus**.
3.  Valige kulu kategooria. Näete loendit kulukategooriatest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse kuni 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Dynamics 365 for Operationsi mobiiliplatvorm](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Kui soovitud kategooriat pole loendis, valige suvand **Otsi**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Saate otsida kulukategooria järgi või lülituda kulutüübi järgi otsingule.
4.  Sisestage kulu kande kuupäev.
5.  Valikuline: saate sisestada kaupmehe kulu.
6.  Sisestage kulu summa.
7.  Saate valida kulu valuuta. Näete loendit valuutakoodidest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse kuni 400 valuutat, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Dynamics 365 for Operationsi mobiiliplatvorm](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Kui soovitud valuutat pole loendis, valige suvand **Otsi**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Saate otsida valuuta järgi või lülituda nime järgi otsingule.
8.  Valige suvand **Tee foto** või **Vali pilt**.
9.  Kui valisite suvandi **Tee foto**, avaneb teie mobiilse seadme kaamera, et saaksite kviitungist foto jäädvustada. Kui foto on tehtud, klõpsake selle aktsepteerimiseks nuppu **OK**.  Kui aga valisite suvandi **Vali pilt**, valige loendist pilt.
10. Valige suvand **Valmis**.






