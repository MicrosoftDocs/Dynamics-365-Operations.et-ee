---
title: Arvestus- või aruandlusvaluuta muutmine
description: Selles teemas selgitatakse, kuidas muuta arvestus- või aruandlusvaluutat või lisada aruandlusvaluuta pearaamatu seadistusse.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0435deb009173684c7faaf5340e8095c019ec71c
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085470"
---
# <a name="change-the-accounting-or-reporting-currency"></a><span data-ttu-id="4345d-103">Arvestus- või aruandlusvaluuta muutmine</span><span class="sxs-lookup"><span data-stu-id="4345d-103">Change the accounting or reporting currency</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4345d-104">Selles teemas selgitatakse, kuidas muuta arvestus- või aruandlusvaluutat või lisada aruandlusvaluuta pearaamatu seadistusse.</span><span class="sxs-lookup"><span data-stu-id="4345d-104">This topic explains how to change the accounting or reporting currency, or add a reporting currency to the setup of a ledger.</span></span>

## <a name="symptom"></a><span data-ttu-id="4345d-105">Sümptom</span><span class="sxs-lookup"><span data-stu-id="4345d-105">Symptom</span></span>

<span data-ttu-id="4345d-106">Te soovite muuta arvestus- või aruandlusvaluutat või lisada aruandlusvaluuta pearaamatu häälestusse.</span><span class="sxs-lookup"><span data-stu-id="4345d-106">You want to change the accounting or reporting currency, or add a reporting currency to the ledger setup.</span></span> <span data-ttu-id="4345d-107">See toimub tavaliselt järgmiste stsenaariumide korral.</span><span class="sxs-lookup"><span data-stu-id="4345d-107">This typically occurs in the following scenarios:</span></span>

- <span data-ttu-id="4345d-108">Juriidilise isiku seadistamisel määrati vale arvestus- või aruandlusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="4345d-108">The wrong accounting or reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="4345d-109">Te soovite nüüd seda valuutat muuta.</span><span class="sxs-lookup"><span data-stu-id="4345d-109">You now want to change that currency.</span></span>
- <span data-ttu-id="4345d-110">Juriidilise isiku seadistamisel määrati aruandlusvaluuta, kuid organisatsioon soovib nüüd aruandlusvaluuta eemaldada.</span><span class="sxs-lookup"><span data-stu-id="4345d-110">A reporting currency was specified when a legal entity was set up, but the organization now wants to remove the reporting currency.</span></span>
- <span data-ttu-id="4345d-111">Organisatsioon täiendab või migreerib rakendusele Microsoft Dynamics 365 Finance ja soovib muuta arvestus- või aruandlusvaluutat.</span><span class="sxs-lookup"><span data-stu-id="4345d-111">The organization is upgrading or migrating to Microsoft Dynamics 365 Finance, and wants to change the accounting or reporting currency.</span></span>

<span data-ttu-id="4345d-112">Organisatsioon, kes varem ei kasutanud topeltvaluuta võimalust, soovib seda kasutama hakata.</span><span class="sxs-lookup"><span data-stu-id="4345d-112">An organization that didn't previously use the Dual currency capability wants to start to use it.</span></span> <span data-ttu-id="4345d-113">See probleem ilmneb tavaliselt järgmiste stsenaariumide korral.</span><span class="sxs-lookup"><span data-stu-id="4345d-113">This issue typically occurs in the following scenarios.</span></span>

- <span data-ttu-id="4345d-114">Juriidilise isiku seadistamisel ei määratud aruandlusvaluutat.</span><span class="sxs-lookup"><span data-stu-id="4345d-114">No reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="4345d-115">(Aruandlusvaluuta on valikuline.) Te soovite nüüd lisada aruandlusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="4345d-115">(A reporting currency is optional.) You now want to add a reporting currency.</span></span>

## <a name="resolution"></a><span data-ttu-id="4345d-116">Lahendus</span><span class="sxs-lookup"><span data-stu-id="4345d-116">Resolution</span></span>

<span data-ttu-id="4345d-117">Kõige olulisem kaalutlus on see, kas pearaamatu seadistamiseks on juriidilises isikus sisestatud kandeid (tegelikke või eelarvelisi).</span><span class="sxs-lookup"><span data-stu-id="4345d-117">The most important consideration is whether any transactions (actual or budget) have been posted in the legal entity for the ledger setup.</span></span> <span data-ttu-id="4345d-118">**Kui juriidilises isikus on sisestatud kandeid (tegelikke või eelarvelisi), ei saa arvestus- või aruandlusvaluutat muuta.**</span><span class="sxs-lookup"><span data-stu-id="4345d-118">**You can't change the accounting or reporting currency, or add a reporting currency, if any transactions (actual or budget) have been posted in the legal entity.**</span></span> <span data-ttu-id="4345d-119">Sõltuvalt sellest, kas kanded on sisestatud, tehke ühes järgmistest jaotisest esitatud etapid.</span><span class="sxs-lookup"><span data-stu-id="4345d-119">Follow the steps in one of the following sections, depending on whether transactions have been posted.</span></span>

### <a name="no-transactions-have-been-posted"></a><span data-ttu-id="4345d-120">Ühtki kannet pole sisestatud</span><span class="sxs-lookup"><span data-stu-id="4345d-120">No transactions have been posted</span></span>

1. <span data-ttu-id="4345d-121">Avage juriidilises isikus, kelle jaoks valuutasid uuendate, **Pearaamat \> Pearaamatu seadistus \> Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="4345d-121">In the legal entity that you're updating currencies for, go to **General ledger \> Ledger setup \> Ledger**.</span></span>
2. <span data-ttu-id="4345d-122">Valige lehel **Pearaamat** käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="4345d-122">On the **Ledger** page, select **Edit**.</span></span>
3. <span data-ttu-id="4345d-123">Valige kiirkaardil **Valuuta** juriidilise isiku puhul kasutatav arvestusvaluuta ja aruandlusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="4345d-123">On the **Currency** FastTab, select the accounting currency and reporting currency to use for the legal entity.</span></span>
4. <span data-ttu-id="4345d-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4345d-124">Select **Save**.</span></span>

<span data-ttu-id="4345d-125">Kui lehel **Pearaamat** pole arvestusvaluuta ja aruandlusvaluuta väljad saadaval, on juriidilises isikus sisestatud vähemalt üks kanne (tegelik või eelarveline).</span><span class="sxs-lookup"><span data-stu-id="4345d-125">If the fields for the accounting currency and the reporting currency aren't available on the **Ledger** page, one or more transactions (actual or budget) have been posted in the legal entity.</span></span> <span data-ttu-id="4345d-126">Seega ei saa valuutasid muuta.</span><span class="sxs-lookup"><span data-stu-id="4345d-126">Therefore, the currencies can't be changed.</span></span> <span data-ttu-id="4345d-127">Sellisel juhul järgige järgmises jaotises esitatud etappe.</span><span class="sxs-lookup"><span data-stu-id="4345d-127">In this case, follow the steps in the next section.</span></span>

### <a name="transactions-have-been-posted"></a><span data-ttu-id="4345d-128">Kanded on sisestatud</span><span class="sxs-lookup"><span data-stu-id="4345d-128">Transactions have been posted</span></span>

<span data-ttu-id="4345d-129">**Kui juriidilises isikus on sisestatud kandeid, on ainus viis arvestus- ja aruandlusvaluutade muutmiseks või lisamiseks uue juriidilise isiku loomine, millele on õiged valuutad.**</span><span class="sxs-lookup"><span data-stu-id="4345d-129">**If transactions have been posted in the legal entity, the only way to change or add accounting and reporting currencies is to create a new legal entity that has the correct currencies.**</span></span> <span data-ttu-id="4345d-130">Selle protsessi hõlbustamiseks võimaldab süsteemi andmehaldus kopeerida seadistuskirjed ja põhikirjed praegusest juriidilisest isikust uude juriidilisse isikusse.</span><span class="sxs-lookup"><span data-stu-id="4345d-130">To help make this process easier, Data management in the system lets you copy setup records and master records from the current legal entity to a new legal entity.</span></span>

<span data-ttu-id="4345d-131">Arvestus- või aruandlusvaluuta muudatused on ulatuslikud.</span><span class="sxs-lookup"><span data-stu-id="4345d-131">Changes to the accounting and reporting currencies are pervasive.</span></span> <span data-ttu-id="4345d-132">Need ei mõjuta mitte ainult pearaamatut, vaid ka kõiki alammooduleid (müügireskontro, ostureskontro, varud, projekt jne), kõiki sõltumatu tarkvaratootja (ISV) lahendusi ja kõiki teie tehtud laiendusi, mis summasid salvestavad.</span><span class="sxs-lookup"><span data-stu-id="4345d-132">They affect not only General ledger but also every subledger (Accounts receivable, Accounts payable, Inventory, Project, and so on), every independent software vendor (ISV) solutions, and any extension that you've made that stores amounts.</span></span>

<span data-ttu-id="4345d-133">Iga summa leidmisel ja teisendamisel erinevasse valuutasse võivad tekkida vead.</span><span class="sxs-lookup"><span data-stu-id="4345d-133">The process of finding and translating each amount to a different currency is subject to error.</span></span> <span data-ttu-id="4345d-134">Seetõttu ei kinnita tehniline töörühm skripti, mis muudab või lisab arvestus- ja aruandlusvaluutasid.</span><span class="sxs-lookup"><span data-stu-id="4345d-134">Therefore, the engineering team won't approve a script that changes or adds accounting and reporting currencies.</span></span> <span data-ttu-id="4345d-135">Lisaks, kuigi varem rakenduse Microsoft Dynamics AX 2012 jaoks saadaval olnud tööriist laseb teil muuta või lisada arvestus- ja aruandlusvaluutasid, loeti see tööriist nii AX 2012 R3 kui ka Finance'i jaoks iganenuks.</span><span class="sxs-lookup"><span data-stu-id="4345d-135">Additionally, although a tool that used to be available for Microsoft Dynamics AX 2012 let you change or add accounting and reporting currencies, that tool was deprecated for both AX 2012 R3 and Finance.</span></span>

<span data-ttu-id="4345d-136">Järgige neid etappe, et kopeerida seadistus- ja koondandmed praegusest juriidilisest isikust uude juriidilisse isikusse.</span><span class="sxs-lookup"><span data-stu-id="4345d-136">Follow these steps to copy the setup and master data from the current legal entity to a new legal entity.</span></span>

1. <span data-ttu-id="4345d-137">Avage **Tööruumid \> Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="4345d-137">Go to **Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="4345d-138">Valige grupis **Import/eksport** üksus **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="4345d-138">Select **Templates** under the **Import/Export** group.</span></span>
3. <span data-ttu-id="4345d-139">Veenduge, et mallid on saadaval.</span><span class="sxs-lookup"><span data-stu-id="4345d-139">Make sure that templates are available.</span></span> <span data-ttu-id="4345d-140">Kui ühtki malli pole saadaval, valige **Vaikemallide laadimine** ja oodake, kuni mallid luuakse.</span><span class="sxs-lookup"><span data-stu-id="4345d-140">If no templates are available, select **Load default templates**, and wait for the templates to be generated.</span></span>
4. <span data-ttu-id="4345d-141">Naaske tööruumi **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="4345d-141">Return to the **Data management** workspace.</span></span>
5. <span data-ttu-id="4345d-142">Valige **Juriidilisse isikusse kopeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4345d-142">Select **Copy into legal entity**.</span></span>
6. <span data-ttu-id="4345d-143">Sisestage grupi nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="4345d-143">Enter a group name and description.</span></span>
7. <span data-ttu-id="4345d-144">Valige väljal **Algne juriidiline isik** juriidiline isik, millest andmed kopeeritakse.</span><span class="sxs-lookup"><span data-stu-id="4345d-144">In the **Source legal entity** field, select the legal entity to copy data from.</span></span>
8. <span data-ttu-id="4345d-145">Valige kiirkaardil **Juriidilised sihtisikud** üksus **Juriidiliste isikute loomine**, et luua uus juriidiline isik, millesse saate kopeerida algse juriidilise isiku andmed.</span><span class="sxs-lookup"><span data-stu-id="4345d-145">In the **Destination legal entities** FastTab, select **Create legal entities** to create a new legal entity that you can copy the source legal entity data to.</span></span> <span data-ttu-id="4345d-146">Andmete kopeerimiseks olemasolevasse juriidilisse isikusse valige **Vali olemasolev**.</span><span class="sxs-lookup"><span data-stu-id="4345d-146">Select **Select existing** to copy data to an existing legal entity.</span></span>
9. <span data-ttu-id="4345d-147">Valikuline: määrake välja **Kopeeri numbriseeriad** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="4345d-147">Optional: Set the **Copy number sequences** field to **Yes**.</span></span> <span data-ttu-id="4345d-148">(See etapp on soovitatav andmete kopeerimisel.)</span><span class="sxs-lookup"><span data-stu-id="4345d-148">(This step is recommended when you copy data.)</span></span>
10. <span data-ttu-id="4345d-149">Valige alal **Valitud üksused** käsk **Lisa mall**.</span><span class="sxs-lookup"><span data-stu-id="4345d-149">In the **Selected entities** area, select **Add template**.</span></span>
11. <span data-ttu-id="4345d-150">Valige kasutatavad mallid.</span><span class="sxs-lookup"><span data-stu-id="4345d-150">Select the templates to use.</span></span> <span data-ttu-id="4345d-151">Uue juriidilise isiku jaoks soovitatavate mallide hulgas on **025 – Pearaamat** ja **Finantsid**.</span><span class="sxs-lookup"><span data-stu-id="4345d-151">Suggested templates for a new legal entity include **025 - General Ledger** and **Financials**.</span></span> <span data-ttu-id="4345d-152">Soovitame teil üle vaadata kõik muud saadaolevad mallid, et teha kindlaks, kas mõni neist vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="4345d-152">We recommend that you review all the other available templates to determine whether any of them apply to your requirements.</span></span>
12. <span data-ttu-id="4345d-153">Valige **Juriidilisse isikusse kopeerimine** pakktöötluse alustamiseks, millega luuakse valitud üksused ja kopeeritakse need juriidilisse sihtisikusse.</span><span class="sxs-lookup"><span data-stu-id="4345d-153">Select **Copy into legal entity** to start a batch process that will create the selected entities and copy them into the destination legal entity.</span></span>
13. <span data-ttu-id="4345d-154">Pärast töötluse lõpule viimist, kuid enne mis tahes kande sisestamist, avage pearaamat ja uuendage arvestus- ja aruandlusvaluutasid käesolevas teemas eespool kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="4345d-154">After the process is completed, but before any transaction are posted, go to the ledger, and update the accounting and reporting currencies as described earlier in this topic.</span></span>

<span data-ttu-id="4345d-155">Kui lõite uue juriidilises isiku, et saaksite muuta arvestus- või aruandlusvaluutat, veenduge, et vana juriidilise isiku valuutades algsaldod teisendatakse uutesse valuutadesse.</span><span class="sxs-lookup"><span data-stu-id="4345d-155">If you created a new legal entity so that you can change the accounting or reporting currency, verify that the beginning balances are translated from the currencies of the old legal entity to the new currencies.</span></span>

<span data-ttu-id="4345d-156">Eelmisi etappe kirjeldavat videot vt [Juriidilisse isikusse kopeerimine](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span><span class="sxs-lookup"><span data-stu-id="4345d-156">For a video that shows the preceding steps, see [Copy Into Legal Entity](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span></span>