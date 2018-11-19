---
title: "Jaemüügikanali fiskaalüksuse integreerimine"
description: "Selles teemas antakse ülevaade Retail POS-i fiskaalüksuse integreerimisest."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: et-ee
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="aa65b-103">Jaemüügikanali fiskaalüksuse integreerimine</span><span class="sxs-lookup"><span data-stu-id="aa65b-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa65b-104">Selles teemas antakse ülevaade programmis Microsoft Dynamics 365 for Retail saadaolevast fiskaalse integreerimise funktsioonist.</span><span class="sxs-lookup"><span data-stu-id="aa65b-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="aa65b-105">See fiskaalüksuse integreerimise funktsioon on raamistik, mis on loodud jaekaubanduse pettusi ennetavate kohalike maksuseaduste toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="aa65b-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="aa65b-106">Tavalised stsenaariumid, mis kuuluvad fiskaalüksuse integreerimise alla, on järgmised.</span><span class="sxs-lookup"><span data-stu-id="aa65b-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="aa65b-107">Fiskaalkviitungi printimine ja selle kliendile andmine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="aa65b-108">Kassas teostatud müügi ja tagastustega seotud teabe edastamine maksuhalduri pakutavale välisele teenusele.</span><span class="sxs-lookup"><span data-stu-id="aa65b-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="aa65b-109">Andmekaitse kasutamine maksuhalduri volitatud digitaalallkirjaga.</span><span class="sxs-lookup"><span data-stu-id="aa65b-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="aa65b-110">Selles teemas antakse juhised fiskaalüksuse integreerimise seadistamiseks, et kasutajad saaksid teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="aa65b-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="aa65b-111">Fiskaalkonnektorite konfigureerimine, milleks on fiskaalsed seadmed või teenused, mida kasutatakse fiskaalüksuse registreerimise jaoks nagu salvestamine, digiallkirjastamine või finantsandmete turvaline esitamine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="aa65b-112">Dokumendipakkuja konfigureerimine, mis määratleb fiskaaldokumendi loomise väljundmeetodi ja algoritmi.</span><span class="sxs-lookup"><span data-stu-id="aa65b-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="aa65b-113">Fiskaalüksuse registreerimisprotsessi konfigureerimine, mis määratleb etappide jada ja igal etapil kasutatava konnektorite grupi.</span><span class="sxs-lookup"><span data-stu-id="aa65b-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="aa65b-114">Fiskaalüksuse registreerimisprotsessi määratlemine kassa funktsiooniprofiilidele.</span><span class="sxs-lookup"><span data-stu-id="aa65b-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="aa65b-115">Konnektori tehniliste profiilide, kas riistvaraprofiilide (kohalike fiskaalkonntektorite) või kassa funktsiooniprofiilide (teiste fiskaalkonnektorite tüüpide jaoks) määratlemine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="aa65b-116">Fiskaalüksuse integreerimise elluviimise voog</span><span class="sxs-lookup"><span data-stu-id="aa65b-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="aa65b-117">Järgmine stsenaarium näitab harilikku fiskaalüksuse integreerimise elluviimise voogu.</span><span class="sxs-lookup"><span data-stu-id="aa65b-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="aa65b-118">Fiskaalüksuse registreerimisprotsessi lähtestamine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="aa65b-119">Pärast mõne sellise toimingi tegemist, kus fiskaalüksuse registreerimine on nõutav (nt pärast jaemüügikande sõlmimist), seostatakse fiskaalüksuse registreerimisprotsess praeguse kassa funktsiooniprofiiliga.</span><span class="sxs-lookup"><span data-stu-id="aa65b-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="aa65b-120">Fiskaalkonnektori otsimine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="aa65b-121">Igale fiskaalüksuse registreerimisprotsessi etapile vastab süsteemis fiskaalkonnektorite loend.</span><span class="sxs-lookup"><span data-stu-id="aa65b-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="aa65b-122">Nende konnektorite määratletud konnektori grupid hõlmavad funktsiooniprofiile ning mitme konnektori tehnilised profiilid on seotud praeguse riistvaraprofiiliga (ainult konnektoritüübi puhul, mis on **Kohalik**) või praeguse kassa funktsiooniprofiiliga (teiste konnektori tüüpide puhul).</span><span class="sxs-lookup"><span data-stu-id="aa65b-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="aa65b-123">Fiskaalüksuse integreerimise teostamine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="aa65b-124">Süsteem käivitab kõik vajalikud tegevused, mille määratleb leitud konnektoriga ühendatud kogum.</span><span class="sxs-lookup"><span data-stu-id="aa65b-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="aa65b-125">See toimub vastavalt konnektori eelmise etapi funktsiooniprofiili ja tehnilise profiili seadetele.</span><span class="sxs-lookup"><span data-stu-id="aa65b-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="aa65b-126">Vajalikud seadistused enne fiskaalüksuse integreerimise kasutamist</span><span class="sxs-lookup"><span data-stu-id="aa65b-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="aa65b-127">Enne fiskaalüksuse integreerimise funktsiooni kasutamist tuleb määratleda järgmised seaded.</span><span class="sxs-lookup"><span data-stu-id="aa65b-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="aa65b-128">Määratlege fiskaalüksuse funktsiooniprofiili numbri jaoks numbriseeria **Jaemüügi parameetrite** lehel.</span><span class="sxs-lookup"><span data-stu-id="aa65b-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="aa65b-129">Määratlege numbriseeriad **Jaemüügi ühisparameetrite** lehel järgmistele viidetele:</span><span class="sxs-lookup"><span data-stu-id="aa65b-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="aa65b-130">Fiskaalüksuse tehnilise profiili number</span><span class="sxs-lookup"><span data-stu-id="aa65b-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="aa65b-131">Fiskaalkonnektori grupi number</span><span class="sxs-lookup"><span data-stu-id="aa65b-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="aa65b-132">Registreerimisprotsessi number</span><span class="sxs-lookup"><span data-stu-id="aa65b-132">Registration process number</span></span>

- <span data-ttu-id="aa65b-133">Looge igale seadmele või teenusele, mida plaanite fiskaalüksuse integratsiooni eesmärgil kasutada **Fiskaalkonnektor**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaalkonnektorid**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="aa65b-134">Looge kõigile fiskaalkonnektoritele **Fiskaaldokumendi pakkuja**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaaldokumendi pakkujad**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="aa65b-135">Andmetüüpide vastendamist peetakse fiskaaldokumendi pakkuja osaks.</span><span class="sxs-lookup"><span data-stu-id="aa65b-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="aa65b-136">Samale konnektorile erinavte vastenduste loomiseks (nt riigipõhised määrused), tuleb luua erinevad fiskaaldokumendi pakkujad.</span><span class="sxs-lookup"><span data-stu-id="aa65b-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="aa65b-137">Looge igale fiskaaldokumendi pakkujale **Konnektori funktsiooniprofiil**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Konnektori funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="aa65b-138">Valige konnektori nimi.</span><span class="sxs-lookup"><span data-stu-id="aa65b-138">Select a connector name.</span></span>
  - <span data-ttu-id="aa65b-139">Valige dokumendipakkuja.</span><span class="sxs-lookup"><span data-stu-id="aa65b-139">Select a document provider.</span></span>
  - <span data-ttu-id="aa65b-140">Määratlege KM-määra sätted vahekaardil **Teenuse seadistus**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="aa65b-141">Määratlege KM-koodide vastendamine ja maksevahendi tüübi vastendamine **Andmete vastendamise** vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="aa65b-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="aa65b-142">Näited</span><span class="sxs-lookup"><span data-stu-id="aa65b-142">Examples</span></span> 

  |  | <span data-ttu-id="aa65b-143">Vorming</span><span class="sxs-lookup"><span data-stu-id="aa65b-143">Format</span></span> | <span data-ttu-id="aa65b-144">Näide</span><span class="sxs-lookup"><span data-stu-id="aa65b-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="aa65b-145">KM-määrade seadistamine</span><span class="sxs-lookup"><span data-stu-id="aa65b-145">VAT rates settings</span></span> | <span data-ttu-id="aa65b-146">väärtus: KM-määr</span><span class="sxs-lookup"><span data-stu-id="aa65b-146">value : VATrate</span></span> | <span data-ttu-id="aa65b-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="aa65b-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="aa65b-148">KM-koodide vastendamine</span><span class="sxs-lookup"><span data-stu-id="aa65b-148">VAT codes mapping</span></span> | <span data-ttu-id="aa65b-149">KM-kood: väärtus</span><span class="sxs-lookup"><span data-stu-id="aa65b-149">VATcode : value</span></span> | <span data-ttu-id="aa65b-150">KM20 : 1, KM18 : 2</span><span class="sxs-lookup"><span data-stu-id="aa65b-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="aa65b-151">Maksevahendi tüüpide vastendamine</span><span class="sxs-lookup"><span data-stu-id="aa65b-151">Tender types mapping</span></span> | <span data-ttu-id="aa65b-152">Maksevahendi tüüp: väärtus</span><span class="sxs-lookup"><span data-stu-id="aa65b-152">TenderTyp : value</span></span> | <span data-ttu-id="aa65b-153">Sularaha: 1 kaart: 2</span><span class="sxs-lookup"><span data-stu-id="aa65b-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="aa65b-154">Looge **Fiskaalkonnektorite grupid**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaalkonnektori grupp**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="aa65b-155">Konnektori grupp on selliste funktsiooniprofiilide alamkogu, mis on seotud fiskaalkonnektoritega, mis teostvad samu funktsioone ja mida kasutatakse fiskaalüksuse registreerimise protsessi samal etapil.</span><span class="sxs-lookup"><span data-stu-id="aa65b-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="aa65b-156">Konnektori grupile funktsiooniprofiilide lisamine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="aa65b-157">Klõpsake **Lisa** lehel **Funktsiooniprofiilid** ja valige profiili number.</span><span class="sxs-lookup"><span data-stu-id="aa65b-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="aa65b-158">Kui soovite peatada funktsiooniprofiili kasutamise, määratlege **Keela** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="aa65b-159">See muudatus mõjutab ainult praegust konnektori gruppi.</span><span class="sxs-lookup"><span data-stu-id="aa65b-159">This change affects the current connector group only.</span></span> <span data-ttu-id="aa65b-160">Saate jätkata sama funktsiooniprofiili kasutamist teistes konnektori gruppides.</span><span class="sxs-lookup"><span data-stu-id="aa65b-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="aa65b-161">Konnektori grupis saab igal fiskaalkonnektoril olla ainult üks funktsiooniprofiil.</span><span class="sxs-lookup"><span data-stu-id="aa65b-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="aa65b-162">Looge igale fiskaalkonnektorile **Konnektori tehniline profiil**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Konnektori tehnilised profiilid**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="aa65b-163">Valige konnektori nimi.</span><span class="sxs-lookup"><span data-stu-id="aa65b-163">Select a connector name.</span></span>
  - <span data-ttu-id="aa65b-164">Valige konnektori tüüp.</span><span class="sxs-lookup"><span data-stu-id="aa65b-164">Select a connector type:</span></span> 
      - <span data-ttu-id="aa65b-165">**Kohalik** – määratlege see tüüp füüsilistele seadmetele või kohalikku arvutisse installitud rakendustele.</span><span class="sxs-lookup"><span data-stu-id="aa65b-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="aa65b-166">**Sisemine** – määratlege see tüüp fiskaalsetele seadmetele ja teenustele, mis on ühendatud jaemüügiserveriga.</span><span class="sxs-lookup"><span data-stu-id="aa65b-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="aa65b-167">**Väline** – väliste finantsteenuste jaoks nagu maksuhalduri pakutav veebiportaal.</span><span class="sxs-lookup"><span data-stu-id="aa65b-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="aa65b-168">Määratlege sätted **Ühenduse** vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="aa65b-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="aa65b-169">Nii tehnilistele kui funktsiooniprofiilidele laaditakse varem laaditud värskendatud konfiguratsiooni versioon.</span><span class="sxs-lookup"><span data-stu-id="aa65b-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="aa65b-170">Teid teavitatakse, kui sobiv konnektor või dokumendipakkuja on juba kasutuses.</span><span class="sxs-lookup"><span data-stu-id="aa65b-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="aa65b-171">Vaikimisi talletatakse kõik tehnilistes ja funktsiooniprofiilides käsitsi tehtud muudatused.</span><span class="sxs-lookup"><span data-stu-id="aa65b-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="aa65b-172">Nende profiilide asendamiseks konfiguratsiooni vaikeparameetritega klõpsake **Konnektori funktsiooniprofiilide** lehel ja **Konnektori tehniliste profiilide** lehel nuppu **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="aa65b-173">Looge igale fiskaalüksuse integreerimise kordumatule protsessile **Fiskaalüksuse registreerimisprotsess**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaalüksuse integreerimisprotsess**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="aa65b-174">Registreerimisprotsess määratletakse registreerimisetappide järjestuse ja igal etapil kasutatava konnektori grupi järgi.</span><span class="sxs-lookup"><span data-stu-id="aa65b-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="aa65b-175">Registreerimisetappide protsessi lisamine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="aa65b-176">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-176">Click **Add**.</span></span>
      - <span data-ttu-id="aa65b-177">Valige konnektori tüüp.</span><span class="sxs-lookup"><span data-stu-id="aa65b-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="aa65b-178">See väli määratleb, kust süsteem konnektorile tehnilist profiili otsib, kas riistvaraprofiilidest **Kohaliku** konnektori tüübi jaoks või kassa funktsiooniprofiilidest teiste fiskaalkonnektori tüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="aa65b-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="aa65b-179">Konnektori grupi valimine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="aa65b-180">Klõpsake **Kontrolli**, et kontrollida registreerimisprotsessi struktuuri tervislikkust.</span><span class="sxs-lookup"><span data-stu-id="aa65b-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="aa65b-181">Kontrollimine on soovitatav järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="aa65b-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="aa65b-182">Uue registreerimisprotsessi suhtes pärast seda, kui kõik seadistamised (sh kassa funktsiooniprofiilide ja riistvaraprofiilide sidumine) on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="aa65b-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="aa65b-183">Pärast olemasoleva registreerimisprotsessi värskendamist.</span><span class="sxs-lookup"><span data-stu-id="aa65b-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="aa65b-184">Fsikaalüksuse registreerimisprotsessi sidumiseks kassa funktsiooniprofiilidega minge **Jaemüük > Kanali seadistus > Kassa seadistus > Kassa profiilid > Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="aa65b-185">Klõpsake **Redigeeri** ja valige **Protsessi number** vahekaardil **Fiskaalüksuse registreerimisprotsess**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="aa65b-186">Konnektori tehniliste profiilide sidumiseks riistvaraprofiilidega minge **Jaemüük > Kanali seadistus > Kassa seadistus > Kassa profiilid > Riistvaraprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="aa65b-187">Klõpsake **Redigeeri**, seejärel klõpsake **Fiskaalüksuse tehnilise profiili** vahekaardil **Uus**.</span><span class="sxs-lookup"><span data-stu-id="aa65b-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="aa65b-188">Valige **Profiili numbri** väljal konnektori tehniline profiil.</span><span class="sxs-lookup"><span data-stu-id="aa65b-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="aa65b-189">Riistvaraprofiilile saab lisada mitu tehnilist profiili.</span><span class="sxs-lookup"><span data-stu-id="aa65b-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="aa65b-190">Kuid seda ei toetata, kui riistvaraprofiilil on mis tahes konnektori grupiga rohkem kui üks lõikumine.</span><span class="sxs-lookup"><span data-stu-id="aa65b-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="aa65b-191">Valede seadistuste vältimiseks on soovitatav pärast kõigi riistvaraprofiilide värskendamist registreerimisprotsessi kontrollida.</span><span class="sxs-lookup"><span data-stu-id="aa65b-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

