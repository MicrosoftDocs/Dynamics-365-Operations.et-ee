---
title: "Kulude halduse mobiilne tööruum"
description: "See teema annab teavet mobiilse tööruumi Kulude haldamine kohta. See tööruum võimaldab kasutajatel kviitungeid salvestada ja üles laadida, et neid hiljem kuluaruandele lisada. Kasutajad saavad ka kiiresti luua kuluridu, kasutades lisatud kviitungit, ning luua ja hallata oma kuluaruandeid."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6f6add07a2426b1846cbeb9dee149a63f66f779e
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="expense-management-mobile-workspace"></a>Kuluhalduse mobiilne tööruum

[!include[banner](../includes/banner.md)]

See teema annab teavet mobiilse tööruumi **Kulude haldamine** kohta. See tööruum võimaldab kasutajatel kviitungeid salvestada ja üles laadida, et neid hiljem kuluaruandele lisada. Kasutajad saavad ka kiiresti luua kuluridu, kasutades lisatud kviitungit, ning luua ja hallata oma kuluaruandeid. Samuti saavad kinnitajad kasutada mobiilset tööruumi **Kulude haldamine** endale määratud kuluaruannete vaatamiseks ning nende kuluaruannete kinnitamiseks või tagasilükkamiseks.


See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.


## <a name="overview"></a>Ülevaade

Paljud ettevõtted nõuavad, et reisiga seotud või äriga seotud kuluaruandele, mille töövõtja korvamiseks esitab, lisatakse kviitungi koopia. Mobiilne tööruum **Kulude haldus** võimaldab kasutajatel kiiresti luua oma valitud mobiilses seadmes uusi kuluridu, kasutades lisatud fotot kviitungist. Teise võimalusena saavad kasutajad jäädvustada kviitungist foto ja lisada selle kuluaruandele hiljem. Töötajad saavad ka luua ja hallata oma kuluaruandeid ning edastada need kinnitamiseks ja korvamiseks, kasutades oma mobiilset seadet.


Täpsemalt võimaldab mobiilne tööruum **Kulude haldamine** teha kasutajatel järgmist.

- Kviitungist foto tegemine ja selle üleslaadimine Microsoft Dynamicsi 365 for Finance and Operationsisse. Seejärel saab lisada selle foto hiljem kuluaruandele.
- Faili üleslaadimine salvestatud kviitungina. Seejärel saab lisada selle faili hiljem kuluaruandele.
- Uue kulurea loomine, kasutades lisatud kviitungit. Seejärel saab lisada selle reaüksuse hiljem kuluaruandele ning esitada selle heakskiitmiseks ja korvamiseks.

Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, saate kasutada ka järgmisi funktsioone.

- Uue kuluaruande loomine.
- Kuluaruandele krediitkaardikannete ja muude varem loodud kulude lisamine.
- Kuluaruande jaoks uute kulude loomine.
- Kuluaruande jaoks mis tahes kulule kviitungi lisamine, tehes kviitungist foto või laadides jäädvustatud kviitungi failina üles.
- Olenevalt ettevõtte kulude poliitikast saab lisada kulule külaliste nimekirja.
- Olenevalt ettevõtte kulude poliitikast saab kulud täpsustada.
- Kuluaruande esitamine kinnitamiseks ja korvamiseks.
- Nende kuluaruannete kinnitamine või tagasilükkamine, mille kinnitajaks teid on määratud.

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Eeltingimused Microsoft Dynamics 365 for Finance and Operationsi kasutamisel 
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, peab süsteemiadministraator avaldama mobiilse tööruumi **Kulude haldamine**. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<td>Rakendage KB 4019015.</td>
<td>Süsteemiadministraator</td>
<td>KB 4019015 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Kulude haldamine</strong>. KB 4019015 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ExpenseMobile</strong>, ning seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avaldama mobiilse tööruumi <strong>Kulude haldamine</strong>.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operationsi mobiilirakenduse alla laadimine ja installimine
Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.

- [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse
1. Käivitage rakendus oma mobiilses seadmes.
2. Sisestage Dynamics 365 URL.
4. Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
5. Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.


[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kviitungi salvestamine, kasutades kulude haldamise mobiilset tööruumi

1. Avage oma mobiilses seadmes tööruum **Kulude haldamine**.
2. Valige suvand **Salvesta kviitung**.
3. Valige suvand **Tee foto** või **Vali pilt**.
4. Järgige üht neist sammudest.

    - Kui valisite suvandi **Tee foto**, toimige järgmiselt.

        1. Avaneb teie mobiilse seadme kaamera, et saaksite kviitungist foto jäädvustada. Kui foto on tehtud, valige selle aktsepteerimiseks nupp **OK**.
        2. Valikuline: saate sisestada fotole pealkirja ja märkused.

    - Kui valisite suvandi **Vali pilt**, toimige järgmiselt.

        1. Valige loendist pilt.
        2. Valikuline: saate sisestada pildile pealkirja ja märkused.

5. Valige suvand **Valmis**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Kulude kiire sisestamine, kasutades mobiilset tööruumi Kulude haldamine
1. Avage oma mobiilses seadmes tööruum **Kulude haldamine**.
2. Valige suvand **Kiire kulusisestus**.
3. Valige kulu kategooria. Näete loendit kulukategooriatest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie kategooriat pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Saate otsida kulukategooria järgi või lülituda kulutüübi järgi otsingule.
4. Sisestage kulu kande kuupäev.
5. Valikuline: saate sisestada kaupmehe kulu.
6. Sisestage kulu summa.
7. Saate valida kulu valuuta. Näete loendit valuutakoodidest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 400 valuutat, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie valuutat pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Saate otsida valuuta järgi või lülituda nime järgi otsingule.
8. Valige suvand **Tee foto** või **Vali pilt**.
9. Järgige üht neist sammudest.

    - Kui valisite suvandi **Tee foto**, avaneb teie mobiilse seadme kaamera, et saaksite kviitungist foto jäädvustada. Kui foto on tehtud, valige selle aktsepteerimiseks nupp **OK**.
    - Kui valisite suvandi **Vali pilt**, valige loendist pilt.

10. Valige suvand **Valmis**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Kuluaruande kinnitamine, kasutades mobiilset tööruumi Kulude haldamine (kui kasutate 2017. aasta juulivärskendust)
1. Avage oma mobiilses seadmes tööruum **Kulude haldamine**.
2. **Kulu kinnitamised** kuvab teile kinnitamiseks määratud kuluaruannete arvu. Arvu värskendatakse umbes iga 30 minuti järel. Valige suvand **Kulu kinnitamised**.

    Kuvatakse teile kinnitamiseks määratud kuluaruannete loend.
    
3. Valige kuluaruanne, mille kulude üksikasju soovite vaadata.
4. Valige kulu, mille üksikasju soovite vaadata. Kulu puhul kuvatav teave hõlmab kõiki kviitungite, külaliste ja täpsustuste andmeid.
5. Naaske lehele **Kuluaruanne** ja valige, kas kuluaruanne kinnitada või tagasi lükata.
6. Soovi korral sisestage kinnitustegevuse kohta kommentaarid.
7. Valige suvand **Valmis**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Uue kuluaruande loomine ja kinnitamiseks esitamine, kasutades mobiilset tööruumi Kulude haldamine (kui kasutate 2017. aasta juulivärskendust)
1. Avage oma mobiilses seadmes tööruum **Kulude haldamine**.
2. Valige suvand **Kulukanne**.
3. Valige **Uusaruanne** või valige loendist olemasolev kuluaruanne.
4. Sisestage uue kuluaruande eesmärk ja muu saadaolev lisateave. See teave erineb olenevalt sellest, kuidas on kulude haldamine teie ettevõtte puhul konfigureeritud.
5. Valige suvand **Valmis**.
6. Olemasolevate kulude, nagu krediitkaardikanded, lisamiseks kuluaruandesse valige käsk **Manusta**.
7. Valige loendist üks või mitu kulu.
8. Valige suvand **Valmis**.
9. Kuluaruandesse uue kulu lisamiseks valige suvand **Uus kulu**.
10. Valige kulu kategooria. Näete loendit kulukategooriatest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie kategooriat pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Saate otsida kulukategooria järgi või lülituda kulutüübi järgi otsingule.
11. Valikuline: saate sisestada kaupmehe kulu.
12. Sisestage kulu kande kuupäev.
13. Sisestage kulu summa.
14. Saate valida kulu valuuta. Näete loendit valuutakoodidest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 400 valuutat, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie valuutat pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Saate otsida valuuta järgi või lülituda nime järgi otsingule.
15. Valige suvand **Valmis**.
16. Kulu üksikasjade lisamiseks valige **Üksikasjade lisamine**. Saadaolevad väljad sõltuvad teie ettevõtte kuluhalduse konfiguratsioonist.
17. Kui ettevõtte poliitika nõuab kulu puhul kviitungit, valige suvand **Kviitungid** ja seejärel toimige järgmiselt.

    1. Valige suvand **Salvesta kviitung** või **Manusta kviitung**.
    2. Järgige üht neist sammudest.

        - Kui valisite suvandi **Salvesta kviitung**, toimige järgmiselt.

            1. Valige suvand **Tee foto** või **Vali pilt**.
            2. Järgige üht neist sammudest.

                - Kui valisite suvandi **Tee foto**, toimige järgmiselt.

                    1. Avaneb teie mobiilse seadme kaamera, et saaksite kviitungist foto jäädvustada. Kui foto on tehtud, valige selle aktsepteerimiseks nupp **OK**.
                    2. Valikuline: saate sisestada fotole pealkirja ja märkused.

                - Kui valisite suvandi **Vali pilt**, toimige järgmiselt.

                    1. Valige loendist pilt.
                    2. Valikuline: saate sisestada pildile pealkirja ja märkused.

            3.  Valige suvand **Valmis**.

        - Kui valisite suvandi **Manusta kviitung**, toimige järgmiselt.

            1.  Valige loendist üks või mitu pilti.
            2.  Valige suvand **Valmis**.

    3. Valige kulu üksikasjade juurde naasmiseks nupp **Tagasi**.

18. Kui ettevõtte poliitika nõuab kulu puhul külaliste märkimist, valige suvand **Külalised** ja seejärel toimige järgmiselt.

    1. Valige suvand **Külaline**, **Eelmised külalised** või **Kaastöötajad**.
    2. Järgige üht neist sammudest.

        - Kui valisite suvandi **Külaline**, toimige järgmiselt.

            1. Sisestage külalise nimi.
            2. Valikuline: sisestage külalise organisatsioon ja/või riik.
            3. Valikuline: sisestage külalise ametinimetus.
            4. Valige suvand **Valmis**.

        - Kui valisite suvandi **Eelmised külalised**, toimige järgmiselt.

            1. Valige loendist üks või mitu eelmist külalist. Kuvatakse loend eelmistest külalistest, kelle olete lisanud eelmistesse kuluaruannetesse, mis on laaditud teie rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie eelmist külalist pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Saate otsida nime järgi või lülituda otsingule organisatsiooni, riigi või ametinimetuse järgi.
            2. Valige suvand **Valmis**.

        - Kui valisite suvandi **Kaastöötajad**, toimige järgmiselt.

            1. Valige loendist üks või mitu kaastöötajat. Näete loendit kaastöötajatest, kes on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie kaastöötajat pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Saate otsida nime järgi või lülituda otsingule ettevõtte või ametinimetuse järgi.
            2. Valige suvand **Valmis**.

    3. Valige kulu üksikasjade juurde naasmiseks nupp **Tagasi**.

19. Kui ettevõtte poliitika nõuab kulu täpsustamist, valige suvand **Täpsusta** ja seejärel toimige järgmiselt.

    1. Valige täpsustamiseks alguskuupäev.
    2. Valige suvand **Lisa täpsustus**.
    3. Valige kulu täpsustuse alamkategooria. Näete loendit kulu alamkategooriatest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Kui teie alamkategooriat pole loendis, valige veebiotsingu tegemiseks käsk **Otsi**. Tehke otsing kulu alamkategooria nime järgi.
    4. Sisestage täpsustuseks kande summa.
    5. Vajaduse korral redigeerige kande kuupäeva.
    6. Valige suvand **Valmis**.
    7. Korrake eelnevaid etappe seni, kuni olete valitud kuupäeva kohta kõik täpsustused lisanud.
    8. Järgmiste päevade puhul saate valida käsu **Kopeeri järgmisele päevale**, et kopeerida täpsustused järgmisele päevale. Teise võimalusena saate valida täpsustamiseks kuupäeva ja seejärel lisada täpsustused samamoodi, nagu esimese kuupäeva puhul.
    9. Kui olete kulu täpsustamise lõpetanud, valige kulu üksikasjade juurde naasmiseks nupp **Tagasi**.

20. Valige lehele **Kuluaruanne** naasmiseks nupp **Tagasi**.
21. Korrake eelnevaid etappe, kuni olete kõik kulud lisanud.
22. Valige käsk **Esita**.
23. Soovi korral sisestage kinnitajale kommentaarid.
24. Valige suvand **Valmis**.

