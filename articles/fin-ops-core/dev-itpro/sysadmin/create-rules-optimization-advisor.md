---
title: Optimeerimisnõustaja reeglite loomine
description: Selles teemas kirjeldatakse, kuidas optimeerimisnõustajale uusi reegleid lisada.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180986"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="adffd-103">Optimeerimisnõustaja reeglite loomine</span><span class="sxs-lookup"><span data-stu-id="adffd-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adffd-104">Selles teemas selgitatakse, kuidas **optimeerimisnõustaja** jaoks uusi reegleid luua.</span><span class="sxs-lookup"><span data-stu-id="adffd-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="adffd-105">Näiteks saate luua uue reegli selle tuvastamiseks, millistel pakkumiskutse juhtumitel on tühi pealkiri.</span><span class="sxs-lookup"><span data-stu-id="adffd-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="adffd-106">Juhtumite jaoks pealkirjade kasutamine muudab need kergesti tuvastatavaks ja otsitavaks.</span><span class="sxs-lookup"><span data-stu-id="adffd-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="adffd-107">See lihtne näide selgitab, mida saab optimeerimisreeglitega saavutada.</span><span class="sxs-lookup"><span data-stu-id="adffd-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="adffd-108">*Reegel* on avalduse andmete kontrollimine.</span><span class="sxs-lookup"><span data-stu-id="adffd-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="adffd-109">Kui reegli hinnatav tingimus on täidetud, luuakse võimalused protsesside optimeerimiseks või andmete täiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="adffd-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="adffd-110">Võimalusi saab toiminguks kasutada ja toimingute mõju on võimalik mõõta.</span><span class="sxs-lookup"><span data-stu-id="adffd-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="adffd-111">**Optimeerimisnõustaja** jaoks uue reegli loomiseks lisage uus klass, mis laiendab abstraktset klassi **SelfHealingRule** abstraktse klassi, rakendab liidest **IDiagnosticsRule** ja mida kujundab atribuut **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="adffd-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="adffd-112">Klassil peab olema ka atribuudiga **DiagnosticsRuleSubscription** kujundatud meetod.</span><span class="sxs-lookup"><span data-stu-id="adffd-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="adffd-113">Tava kohaselt tehakse seda meetodiga **opportunityTitle**, mida selgitatakse hiljem.</span><span class="sxs-lookup"><span data-stu-id="adffd-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="adffd-114">Selle uue klassi saab lisada kohandatud mudelile sõltuvusega mudelist **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="adffd-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="adffd-115">Järgmises näites rakendatakse reeglit **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="adffd-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="adffd-116">Abstraktsel klassil **SelfHealingRule** on abstraktsed meetodid, mis tuleb juurutada pärinevates klassides.</span><span class="sxs-lookup"><span data-stu-id="adffd-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="adffd-117">Tuumaks on meetod **hinnang** meetod, mis annab vastuseks reegli tuvastatud võimaluste loendi.</span><span class="sxs-lookup"><span data-stu-id="adffd-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="adffd-118">Võimalused saavad olla juriidilise isiku kohta või kehtida tervele süsteemile.</span><span class="sxs-lookup"><span data-stu-id="adffd-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
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

<span data-ttu-id="adffd-119">Ülal näidatud meetod loob tsükli ettevõtete üle ja valib tühjade pealkirjadega pakkumiskutsete juhtumid meetodis **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="adffd-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="adffd-120">Kui leitakse vähemalt üks selline juhtum, luuakse meetodi **getOpportunityForCompany** abil ettevõttepõhine võimalus.</span><span class="sxs-lookup"><span data-stu-id="adffd-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="adffd-121">Pange tähele, et tabeli **SelfHealingOpportunity** välja **Andmed** tüüp on **Konteiner**, mistõttu võib see väli sisaldada igasuguseid selle reegli loogikaga seotud andmeid.</span><span class="sxs-lookup"><span data-stu-id="adffd-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="adffd-122">Üksuse **OpportunityDate** väärtuseks ajakohase ajatempli määramine registreerib võimaluse viimase hinnangu aja.</span><span class="sxs-lookup"><span data-stu-id="adffd-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="adffd-123">Võmalused saavad olla ka ettevõtteülesed.</span><span class="sxs-lookup"><span data-stu-id="adffd-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="adffd-124">Sel juhul ei ole ettevõtete ülest tsüklit vaja ja võimalus tuleb luua meetodiga **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="adffd-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="adffd-125">Järgmine kood näitab meetodit **findRFQCasesWithEmptyTitle**, mis annab vastuseks tühjade pealkirjadega pakkumiskutsete juhtumite ID-d.</span><span class="sxs-lookup"><span data-stu-id="adffd-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
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

<span data-ttu-id="adffd-126">Kaks meetodit, mida tuleb veel juurutada, on **opportunityTitle** ja **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="adffd-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="adffd-127">Esimene annab vastuseks võimaluse lühipealkirja, teine annab vastuseks võimaluse üksikasjaliku kirjelduse, mis võib sisaldada ka andmeid.</span><span class="sxs-lookup"><span data-stu-id="adffd-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="adffd-128">Üksuse **opportunityTitle** poolt vastuseks antud pealkiri kuvatakse veeru **Optimeerimisvõimalus** all tööruumis **Optimeerimisnõustaja**.</span><span class="sxs-lookup"><span data-stu-id="adffd-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="adffd-129">Samuti kuvatakse see võimaluse kohta rohkem teavet näitava külgpaani päisena.</span><span class="sxs-lookup"><span data-stu-id="adffd-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="adffd-130">Tava kohaselt on see meetod kujundatud atribuudiga **DiagnosticRuleSubscription** atribuut, mis võtab järgmisi argumente.</span><span class="sxs-lookup"><span data-stu-id="adffd-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="adffd-131">**Diagnostika ala** – tüübi **DiagnosticArea** loetelu, mis kirjeldab seda, millisele avalduse alale reegel kuulub, näiteks **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="adffd-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="adffd-132">**Reegli nimi** – string reegli nimega.</span><span class="sxs-lookup"><span data-stu-id="adffd-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="adffd-133">See ilmub veerus **Reegli nimi** vormil **Diagnostikareeglite kinnitamise reegel** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="adffd-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="adffd-134">**Käitussagedus** – tüübi **DiagnosticRunFrequency** loetelu, mis kirjeldab seda, kui sagedasti tuleb reeglit käitada, nt **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="adffd-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="adffd-135">**Reegli kirjeldus** – string reegli üksikasjalikuma kirjeldusega.</span><span class="sxs-lookup"><span data-stu-id="adffd-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="adffd-136">See ilmub veerus **Reegli kirjeldus** vormil **Diagnostikareeglite kinnitamise reegel** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="adffd-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="adffd-137">Atribuut **DiagnosticRuleSubscription** on reegli toimimiseks kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="adffd-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="adffd-138">Tavaliselt kasutatakse seda üksuse **opportunityTitle** kohta, aga see võib kujundada klassi igat meetodit.</span><span class="sxs-lookup"><span data-stu-id="adffd-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="adffd-139">Järgnev näide on juurutamise kohta.</span><span class="sxs-lookup"><span data-stu-id="adffd-139">The following is an example implementation.</span></span> <span data-ttu-id="adffd-140">Lihtsuse nimel kasutatakse toorstringe, kuigi õigeks juurutamiseks on vaja silte.</span><span class="sxs-lookup"><span data-stu-id="adffd-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="adffd-141">Üksuse **opportunityDetails** poolt vastuseks antud kirjeldus kuvatakse võimaluse kohta rohkem teavet näitaval külgpaanil.</span><span class="sxs-lookup"><span data-stu-id="adffd-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="adffd-142">See võtab argumendi **SelfHealingOpportunity**, mis on väli **Andmed**, mida saab kasutada võimaluse kohta üksikasjalikuma teabe pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="adffd-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="adffd-143">Näites annab meetod vastuseks tühja pealkirjaga pakkumiskutse juhtumite ID-d.</span><span class="sxs-lookup"><span data-stu-id="adffd-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
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

<span data-ttu-id="adffd-144">Kaks ülejäänud juurutatavat abstraktset meetodit on **provideHealingAction** ja **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="adffd-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="adffd-145">**provideHealingAction** annab vastuseks väärtuse tõene, kui parandustoiming on olemas, vastasel korral annab vastuseks väärtuse vale.</span><span class="sxs-lookup"><span data-stu-id="adffd-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="adffd-146">Kui vastuseks on antud väärtus tõene, tuleb juurutada meetodit **performAction**, vastasel juhul ilmneb tõrge.</span><span class="sxs-lookup"><span data-stu-id="adffd-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="adffd-147">Meetod **performAction** võtab argumendi **SelfHealingOpportunity**, kus saab andmeid kasutada tegevuseks.</span><span class="sxs-lookup"><span data-stu-id="adffd-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="adffd-148">Näites avab tegevus üksuse **PurchRFQCaseTableListPage** käsitsi parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="adffd-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="adffd-149">Reegli üksikasjadest sõltuvalt võib võimaluse andmeid kasutades olla võimalik teha automaatne toiming.</span><span class="sxs-lookup"><span data-stu-id="adffd-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="adffd-150">Selles näites saab süsteem pakkumiskutse juhtumite pealkirjad luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="adffd-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="adffd-151">**securityMenuItem** annab vastuseks toimingumenüü üksuse nime nii, et reegel on nähtav ainult kasutajatele, kes pääsevad toimingumenüü üksusele ligi.</span><span class="sxs-lookup"><span data-stu-id="adffd-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="adffd-152">Turvalisuse nimel võib olla vajalik, et teatud reeglid ja võimalused oleksid ligipääsetavad ainult autoriseeritud kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="adffd-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="adffd-153">Näites saavad võimalust vaadata ainult kasutajad, kellel on ligipääs üksusele **PurchRFQCaseTitleAction**.</span><span class="sxs-lookup"><span data-stu-id="adffd-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="adffd-154">Pange tähele, et see toimingumenüü üksus loodi selle näite jaoks ning see lisati tubeprivileegi **PurchRFQCaseTableMaintain** sisenemispunktiks.</span><span class="sxs-lookup"><span data-stu-id="adffd-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="adffd-155">Menüükäsk peab olema tegevuse menüükäsk, et turve õigesti töötaks.</span><span class="sxs-lookup"><span data-stu-id="adffd-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="adffd-156">Muud tüüpi menüükäsud, näiteks **Kuvamenüü käsud** ei tööta õigesti.</span><span class="sxs-lookup"><span data-stu-id="adffd-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="adffd-157">Pärast seda, kui reegel on kompileerimise lõpetanud, käivitage järgmine töö, et see kuvataks kasutajaliidesel.</span><span class="sxs-lookup"><span data-stu-id="adffd-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
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

<span data-ttu-id="adffd-158">Reegel kuvatakse vormil **Diagnostikareeglite kinnitamise reegel**, mis on saadaval asukohas **Süsteemihaldus** > **Perioodilised ülesanded** > **Diagnostika kinnitamise reegli haldamine**.</span><span class="sxs-lookup"><span data-stu-id="adffd-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="adffd-159">Selle hindamiseks minge asukohta **Süsteemihaldus** > **Perioodilised ülesanded** > **Diagnostika kinnitamise reegli ajastamine** ning valige reegli sagedus, nt **Kord päevas**.</span><span class="sxs-lookup"><span data-stu-id="adffd-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="adffd-160">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="adffd-160">Click **OK**.</span></span> <span data-ttu-id="adffd-161">Uue võimaluse vaatamiseks minge asukohta **Süsteemihaldus** > **Optimeerimisnõustaja**.</span><span class="sxs-lookup"><span data-stu-id="adffd-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="adffd-162">Järgmine näide on koodilõik reegli raamistikuga, mis sisaldab kõiki vajalikke meetodeid ja atribuute.</span><span class="sxs-lookup"><span data-stu-id="adffd-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="adffd-163">See aitab teid uute reeglite loomisega alustamisel.</span><span class="sxs-lookup"><span data-stu-id="adffd-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="adffd-164"> Näites sisalduvaid silte ja tegevuse menüükäskusid on kasutatud ainult demoeesmärgil.</span><span class="sxs-lookup"><span data-stu-id="adffd-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
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

<span data-ttu-id="adffd-165">Lisateabe saamiseks vaadake YouTube’i lühivideot: [Optimeerimise nõustaja rakenduses Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="adffd-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>