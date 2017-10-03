---
title: "Analüütika lisamine tööruumidele teenuse Power BI Embedded abil"
description: "See teema kirjeldab, kuidas kaasata Power BI aruanne tööruumi vahekaardile Analüütika."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Platform, UnifiedOperations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e819aafbdf55fbc2a6dc996d275244de1e11d89b
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Analüütika lisamine tööruumidele teenuse Power BI Embedded abil

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Seda funktsiooni toetatakse rakenduses Dynamics 365 for Finance and Operations (versioon 7.2 ja uuemad).

# <a name="introduction"></a>Sissejuhatus
See teema kirjeldab, kuidas kaasata Microsoft Power BI aruanne tööruumi vahekaardile **Analüütika**. Siin toodud näite puhul laiendame sõidukipargi halduse rakenduse tööruumi **Reserveerimise haldus**, et kaasata analüütiline tööruum vahekaardile **Analüütika**.

# <a name="prerequisites"></a>Eeltingimused
+ Juurdepääs arendaja keskkonnale, mis käitab platvormivärskendust 8 või uuemat.
+ Microsoft Power BI töölaua abil loodud analüütiline aruanne (pbix-fail), millel on üksuse kaupluse andmebaasist hangitud andmemudel.

# <a name="overview"></a>Ülevaade
Olenemata sellest, kas laiendate olemasolevat rakenduse tööruumi või võtate kasutusele omaenda uue tööruumi, saate kaasatud analüütiliste vaadete abil kuvada oma äriandmetest selgeid ja interaktiivseid vaateid. Analüütilise tööruumi vahekaardi lisamise protsess koosneb neljast etapist.

1. Dynamicsi 365 ressursina pbix-faili lisamine.
2. Analüütilise tööruumi vahekaardi määratlemine.
3. Pbix-ressursi kaasamine tööruumi vahekaardile.
4. Valikuline: laienduste lisamine vaate kohandamiseks.

> [!NOTE]
> Lisateavet analüütiliste aruannete loomise kohta vaadake jaotisest [Power BI töölauaga alustamine](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). See leht on suurepärane allikas ülevaadete jaoks, mis aitavad teil luua mõjusaid analüütilise aruandluse lahendusi.

# <a name="add-a-pbix-file-as-a-resource"></a>Ressursina pbix-faili lisamine
Enne alustamist peate looma või hankima Power BI aruande, mille soovite tööruumi kaasata. Lisateavet analüütiliste aruannete loomise kohta vaadake jaotisest [Power BI töölauaga alustamine](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).
 
Pbix-faili lisamiseks Visual Studio projekti artefaktina toimige järgmiselt.

1. Looge asjakohases mudelis uus projekt.
2. Valige Solution Exploreris projekt, paremklõpsake ja siis valige suvandid **Lisa** > **Uus üksus**.
3. Valige dialoogiboksi **Uue üksuse lisamine** jaotises **Toimingute artefaktid** mall **Ressurss**.
4. Sisestage nimi, mida kasutatakse aruande viitamiseks X++ metaandmetes, ja klõpsake nuppu **Lisa**.

    ![Dialoogiboks Uue üksuse lisamine](media/analytical-workspace-add.png)

5. Leidke pbix-fail, mis sisaldab analüütilise aruande määratlust, seejärel klõpsake käsku **Ava**.

    ![Dialoogiboks Ressursifaili valimine](media/analytical-workspace-select-resource.png)
  
Nüüd kui olete lisanud pbix-faili Dynamics 365 ressursina, saate kaasata aruanded tööruumidesse ja lisada ka otselingid, kasutades menüü-üksusi.

# <a name="add-a-tab-control-to-an-application-workspace"></a>Vahekaardi juhtelemendi lisamine rakenduse tööruumi
Selles näites laiendame mudeli Sõidukipargi haldus tööruumi **Reserveerimise haldus**, lisades vahekaardi **Analüütika** vormi **FMClerkWorkspace** määratlusele.
 
Järgmisel joonisel on näha, milline näeb vorm **FMClerkWorkspace** välja Microsoft Visual Studio kujundajas.

![Vorm FMClerkWorkspace enne muudatusi](media/analytical-workspace-definition-before.png)

Vormi määratluse laiendamiseks tööruumi **Reserveerimise haldus** puhul toimige järgmisel.

1. Avage kujunduse määratluse laiendamiseks vormikujundaja.
2. Valige kujunduse määratluses ülemine element sildiga **Kujundus | Muster: tegevuses tööruum**.
3. Paremklõpsake ja valige suvandid **Uus** > **Vahekaart**, et lisada uus juhtelement nimega **FormTabControl1**.
4. Valige vormikujundajas suvand **FormTabControl1**.
5. Paremklõpsake ja valige uue vahekaardilehe lisamiseks suvand **Uus vahekaardileht**.
6. Andke vahekaardilehele tähenduslik nimi, näiteks **Tööruum**.
7. Valige vormikujundajas suvand **FormTabControl1**.
8. Paremklõpsake ja valige suvand **Uus vahekaardileht**.
9. Andke vahekaardilehele tähenduslik nimi, näiteks **Analüütika**.
10. Valige vormikujundajas suvand **Analüütika (vahekaardileht)**.
11. Seadke atribuudi **Pealdis** sätteks **Analüütika**.
12. Paremklõpsake juhtelementi ja valige suvandid **Uus** > **Rühm**, et lisada uus vormirühma juhtelement.
13. Andke vormirühmale tähenduslik nimi, näiteks **powerBIReportGroup**.
14. Valige vormikujundajas suvand **PanoramaBody (vahekaart)** ja seejärel lohistage juhtelement vahekaardile **Tööruum**.
15. Valige kujunduse määratluses ülemine element sildiga **Kujundus | Muster: tegevuses tööruum**.
16. Paremklõpsake ja valige suvand **Eemalda muster**.
17. Paremklõpsake uuesti ja valige suvandid **Lisa muster** > **Vahekaartidega tööruum**.
18. Koostage järk muudatuste kinnitamiseks.
 
Järgmisel joonisel on näha, milline näeb kujundus välja pärast nende muudatuste rakendamist.

![FMClerkWorkspace pärast muudatusi](media/analytical-workspace-definition-after.png)

Nüüd, kui olete tööruumi aruande kaasamiseks kasutatavad vormi juhtelemendid lisanud, peate määratlema ülemjuhtelemendi suuruse, nii et see mahuks paigutusse. Vaikimisi jäävad aruandes nähtavaks nii leht **Filtripaan** kui ka leht **Vahekaart**. Saate nende juhtelementide nähtavust siiski aruande sihttarbija vajaduste järgi muuta.
 
> [!NOTE]
> Kaasatud tööruumide puhul soovitame kasutada ühtluse nimel laiendusi nii lehe **Filtripaan** kui ka **Vahekaart** peitmiseks.
 
Nüüd olete rakenduse vormimääratluse laiendamise ülesande täitnud. Lisateavet kohandamiste tegemiseks laienduste kasutamise kohta vaadake jaotisest [Kohandamine: ülekate ja laiendused](../extensibility/customization-overlayering-extensions.md).

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a>X++ äriloogika lisamine vaaturi juhtelemendi kaasamiseks
Tööruumi **Reserveerimise haldus** kaasatud aruandevaaturi juhtelementi lähtestava äriloogika lisamiseks toimige järgmiselt.

1. Avage kujunduse määratluse laiendamiseks vormikujundaja **FMClerkWorkspace**.
2. Vajutage klahvi F7, et pääseda juurde koodimääratluse taga olevale koodile.
3. Lisage järgmine X++ kood.

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Koostage järk muudatuste kinnitamiseks.

Nüüd olete kaasatud aruandevaaturi juhtelementi lähtestava äriloogika lisamise ülesande täitnudl. Järgmisel joonisel on näha, milline näeb tööruum välja pärast nende muudatuste rakendamist.

![Tööruumi kaasatud aruanne](media/analytical-workspace-final.png)

> [!NOTE]
> Pääsete juurde olemasolevale toiminguvaatele, kasutades lehe pealkirja all olevaid tööruumi vahekaarte.

# <a name="reference"></a>Viide

## <a name="pbireporthelperinitializereportcontrol-method"></a>Meetod PBIReportHelper.initializeReportControl
See jaotis annab teavet abilise klassi kohta, mida kasutatakse Power BI aruande kaasamiseks (pbix-ressurss) vormirühma juhtelementi.

### <a name="syntax"></a>Süntaks
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a>Parameetrid

| Nimi | Kirjeldus |
|---|---|
| resourceName | Pbix-ressursi nimi |
| formGroupControl | Vormirühma juhtelement, millele Power BI aruande juhtelement rakendada. |
| defaultPageName | Vaikelehe nimi. |
| showFilterPane | Kahendmuutuja väärtus, mis näitab, kas filtripaan tuleb kuvada (**tõene**) või peita (**väär**). |
| showNavPane | Kahendmuutuja väärtus, mis näitab, kas navigeerimispaan tuleb kuvada (**tõene**) või peita (**väär**). |
| defaultFilters | Power BI aruande vaikefiltrid. |

