---
title: Optimeerimisnõustaja reeglite loomine
description: Selles teemas kirjeldatakse, kuidas optimeerimisnõustajale uusi reegleid lisada.
author: roxanadiaconu
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d2a0d6d2e70bfb797de919b536fa1ca62fd181a8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745997"
---
# <a name="create-rules-for-optimization-advisor"></a>Optimeerimisnõustaja reeglite loomine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas **optimeerimisnõustaja** jaoks uusi reegleid luua. Näiteks saate luua uue reegli selle tuvastamiseks, millistel pakkumiskutse juhtumitel on tühi pealkiri. Juhtumite jaoks pealkirjade kasutamine muudab need kergesti tuvastatavaks ja otsitavaks. See lihtne näide selgitab, mida saab optimeerimisreeglitega saavutada. 

*Reegel* on avalduse andmete kontrollimine. Kui reegli hinnatav tingimus on täidetud, luuakse võimalused protsesside optimeerimiseks või andmete täiendamiseks. Võimalusi saab toiminguks kasutada ja toimingute mõju on võimalik mõõta. 

**Optimeerimisnõustaja** jaoks uue reegli loomiseks lisage uus klass, mis laiendab abstraktset klassi **SelfHealingRule** abstraktse klassi, rakendab liidest **IDiagnosticsRule** ja mida kujundab atribuut **DiagnosticRule**. Klassil peab olema ka atribuudiga **DiagnosticsRuleSubscription** kujundatud meetod. Tava kohaselt tehakse seda meetodiga **opportunityTitle**, mida selgitatakse hiljem. Selle uue klassi saab lisada kohandatud mudelile sõltuvusega mudelist **SelfHealingRules**. Järgmises näites rakendatakse reeglit **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Abstraktsel klassil **SelfHealingRule** on abstraktsed meetodid, mis tuleb juurutada pärinevates klassides. Tuumaks on meetod **hinnang** meetod, mis annab vastuseks reegli tuvastatud võimaluste loendi. Võimalused saavad olla juriidilise isiku kohta või kehtida tervele süsteemile.

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

Ülal näidatud meetod loob tsükli ettevõtete üle ja valib tühjade pealkirjadega pakkumiskutsete juhtumid meetodis **findRFQCasesWithEmptyTitle**. Kui leitakse vähemalt üks selline juhtum, luuakse meetodi **getOpportunityForCompany** abil ettevõttepõhine võimalus. Pange tähele, et tabeli **SelfHealingOpportunity** välja **Andmed** tüüp on **Konteiner**, mistõttu võib see väli sisaldada igasuguseid selle reegli loogikaga seotud andmeid. Üksuse **OpportunityDate** väärtuseks ajakohase ajatempli määramine registreerib võimaluse viimase hinnangu aja.  

Võmalused saavad olla ka ettevõtteülesed. Sel juhul ei ole ettevõtete ülest tsüklit vaja ja võimalus tuleb luua meetodiga **getOpportunityAcrossCompanies**. 

Järgmine kood näitab meetodit **findRFQCasesWithEmptyTitle**, mis annab vastuseks tühjade pealkirjadega pakkumiskutsete juhtumite ID-d.

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

Kaks meetodit, mida tuleb veel juurutada, on **opportunityTitle** ja **opportunityDetails**. Esimene annab vastuseks võimaluse lühipealkirja, teine annab vastuseks võimaluse üksikasjaliku kirjelduse, mis võib sisaldada ka andmeid.

Üksuse **opportunityTitle** poolt vastuseks antud pealkiri kuvatakse veeru **Optimeerimisvõimalus** all tööruumis **Optimeerimisnõustaja**. Samuti kuvatakse see võimaluse kohta rohkem teavet näitava külgpaani päisena. Tava kohaselt on see meetod kujundatud atribuudiga **DiagnosticRuleSubscription** atribuut, mis võtab järgmisi argumente. 

* **Diagnostika ala** – tüübi **DiagnosticArea** loetelu, mis kirjeldab seda, millisele avalduse alale reegel kuulub, näiteks **DiagnosticArea::SCM**. 

* **Reegli nimi** – string reegli nimega. See ilmub veerus **Reegli nimi** vormil **Diagnostikareeglite kinnitamise reegel** (**DiagnosticsValidationRuleMaintain**). 

* **Käitussagedus** – tüübi **DiagnosticRunFrequency** loetelu, mis kirjeldab seda, kui sagedasti tuleb reeglit käitada, nt **DiagnosticRunFrequency::Daily**. 

* **Reegli kirjeldus** – string reegli üksikasjalikuma kirjeldusega. See ilmub veerus **Reegli kirjeldus** vormil **Diagnostikareeglite kinnitamise reegel** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Atribuut **DiagnosticRuleSubscription** on reegli toimimiseks kohustuslik. Tavaliselt kasutatakse seda üksuse **opportunityTitle** kohta, aga see võib kujundada klassi igat meetodit.

Järgnev näide on juurutamise kohta. Lihtsuse nimel kasutatakse toorstringe, kuigi õigeks juurutamiseks on vaja silte. 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

Üksuse **opportunityDetails** poolt vastuseks antud kirjeldus kuvatakse võimaluse kohta rohkem teavet näitaval külgpaanil. See võtab argumendi **SelfHealingOpportunity**, mis on väli **Andmed**, mida saab kasutada võimaluse kohta üksikasjalikuma teabe pakkumiseks. Näites annab meetod vastuseks tühja pealkirjaga pakkumiskutse juhtumite ID-d. 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

Kaks ülejäänud juurutatavat abstraktset meetodit on **provideHealingAction** ja **securityMenuItem**. 

**provideHealingAction** annab vastuseks väärtuse tõene, kui parandustoiming on olemas, vastasel korral annab vastuseks väärtuse vale. Kui vastuseks on antud väärtus tõene, tuleb juurutada meetodit **performAction**, vastasel juhul ilmneb tõrge. Meetod **performAction** võtab argumendi **SelfHealingOpportunity**, kus saab andmeid kasutada tegevuseks. Näites avab tegevus üksuse **PurchRFQCaseTableListPage** käsitsi parandamiseks. 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

Reegli üksikasjadest sõltuvalt võib võimaluse andmeid kasutades olla võimalik teha automaatne toiming. Selles näites saab süsteem pakkumiskutse juhtumite pealkirjad luua automaatselt. 

**securityMenuItem** annab vastuseks toimingumenüü üksuse nime nii, et reegel on nähtav ainult kasutajatele, kes pääsevad toimingumenüü üksusele ligi. Turvalisuse nimel võib olla vajalik, et teatud reeglid ja võimalused oleksid ligipääsetavad ainult autoriseeritud kasutajatele. Näites saavad võimalust vaadata ainult kasutajad, kellel on ligipääs üksusele **PurchRFQCaseTitleAction**. Pange tähele, et see toimingumenüü üksus loodi selle näite jaoks ning see lisati tubeprivileegi **PurchRFQCaseTableMaintain** sisenemispunktiks. 

> [!NOTE]
> Menüükäsk peab olema tegevuse menüükäsk, et turve õigesti töötaks. Muud tüüpi menüükäsud, näiteks **Kuvamenüü käsud** ei tööta õigesti.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Pärast seda, kui reegel on kompileerimise lõpetanud, käivitage järgmine töö, et see kuvataks kasutajaliidesel.

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

Reegel kuvatakse vormil **Diagnostikareeglite kinnitamise reegel**, mis on saadaval asukohas **Süsteemihaldus** > **Perioodilised ülesanded** > **Diagnostika kinnitamise reegli haldamine**. Selle hindamiseks minge asukohta **Süsteemihaldus** > **Perioodilised ülesanded** > **Diagnostika kinnitamise reegli ajastamine** ning valige reegli sagedus, nt **Kord päevas**. Klõpsake nupul **OK**. Uue võimaluse vaatamiseks minge asukohta **Süsteemihaldus** > **Optimeerimisnõustaja**. 

Järgmine näide on koodilõik reegli raamistikuga, mis sisaldab kõiki vajalikke meetodeid ja atribuute. See aitab teid uute reeglite loomisega alustamisel. Näites sisalduvaid silte ja tegevuse menüükäskusid on kasutatud ainult demoeesmärgil.

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

Lisateabe saamiseks vaadake YouTube’i lühivideot: [Optimeerimise nõustaja rakenduses Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]