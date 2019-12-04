---
title: Riistvara suuruse muutmise nõuded kohapealsetes keskkondades
description: Riistvara suuruse muutmise nõuded kohapealsetes keskkondades
author: kfend
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 65f21d71c22d295902b968e6c18134e1577e01f2
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812553"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="793d6-103">Riistvara suuruse muutmise nõuded kohapealsetes keskkondades</span><span class="sxs-lookup"><span data-stu-id="793d6-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="793d6-104">Enne kui alustate kohapealses keskkonnas riistvara ja taristu suuruse muutmise protsessi, tutvuge [pilvjuurutuste süsteeminõuete](system-requirements.md) ning [seadistus- ja juurutusjuhistega](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), et aluseks olev taristu endale hästi selgeks teha.</span><span class="sxs-lookup"><span data-stu-id="793d6-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements for cloud deployments](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="793d6-105">Optimaalse jõudluse saavutamiseks pöörake tähelepanu süsteemi seadistamise parimatele tavadele.</span><span class="sxs-lookup"><span data-stu-id="793d6-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="793d6-106">Kui olete dokumentatsiooni läbi vaadanud, võite alustada oma tehingute ja samaaegsete kasutajate mahu hindamise ning keskkonna suuruse muutmise protsessi tuuma keskmise läbilaskevõime põhjal.</span><span class="sxs-lookup"><span data-stu-id="793d6-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="793d6-107">Suuruse muutmist mõjutavad tegurid</span><span class="sxs-lookup"><span data-stu-id="793d6-107">Factors that affect sizing</span></span>

<span data-ttu-id="793d6-108">Suuruse muutmist mõjutavad kõik järgmisel joonisel näidatud tegurid.</span><span class="sxs-lookup"><span data-stu-id="793d6-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="793d6-109">Mida põhjalikum on kogutud teave, seda täpsemalt saate suuruse muutmise kindlaks määrata.</span><span class="sxs-lookup"><span data-stu-id="793d6-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="793d6-110">Riistvaraline suuruse muutmine ilma toetavate andmeteta on tõenäoliselt ebatäpne.</span><span class="sxs-lookup"><span data-stu-id="793d6-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="793d6-111">Vajalike andmete absoluutne miinimumnõue on maksimaalne kanderea koormus tunni kohta.</span><span class="sxs-lookup"><span data-stu-id="793d6-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="793d6-112">[![Riistvara suuruse muutmine kohapealsetes keskkondades](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="793d6-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="793d6-113">Vaadates vasakult paremale, on esimene ja kõige olulisem suuruse muutmise täpseks prognoosimiseks vajalik tegur kannete profiil ehk kannete iseloomustus.</span><span class="sxs-lookup"><span data-stu-id="793d6-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="793d6-114">Tähtis on leida alati maksimaalne kannete maht tunnis.</span><span class="sxs-lookup"><span data-stu-id="793d6-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="793d6-115">Kui tipp-perioode on mitu, tuleb need perioodid täpselt määratleda.</span><span class="sxs-lookup"><span data-stu-id="793d6-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="793d6-116">Kui mõistate koormust, mis teie taristut mõjutab, peate põhjalikumalt aru saama ka järgmistest teguritest.</span><span class="sxs-lookup"><span data-stu-id="793d6-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="793d6-117">**Kanded** – tavaliselt on kandemahtudel päeva/nädala jooksul teatud tipud.</span><span class="sxs-lookup"><span data-stu-id="793d6-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="793d6-118">See sõltub enamasti kandetüübist.</span><span class="sxs-lookup"><span data-stu-id="793d6-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="793d6-119">Aja- ja kulukannetel on harilikult maksimumid kord nädalas, samas müügitellimuse kanded tulevad sageli päeva jooksul integratsiooni või edastuste kaudu hulgi.</span><span class="sxs-lookup"><span data-stu-id="793d6-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="793d6-120">**Samaaegsete kasutajate arv** – samaaegsete kasutajate arv on teine olulisim suuruse muutmise tegur.</span><span class="sxs-lookup"><span data-stu-id="793d6-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="793d6-121">Samaaegsete kasutajate arvu põhjal ei saa suuruse muutmist usaldusväärselt prognoosida, seega kui need on ainsad saadaolevad andmed, võtke hindamise aluseks ligikaudne arv ja seejärel tulge selle juurde tagasi, kui teil on rohkem andmeid.</span><span class="sxs-lookup"><span data-stu-id="793d6-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="793d6-122">Samaaegsete kasutajate täpne määratlus tähendab järgmist.</span><span class="sxs-lookup"><span data-stu-id="793d6-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="793d6-123">Nimega kasutajad ei ole samaaegsed kasutajad.</span><span class="sxs-lookup"><span data-stu-id="793d6-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="793d6-124">Samaaegsetel kasutajatel on alati alamkogum nimega kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="793d6-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="793d6-125">Maksimaalne töökoormus määratleb suuruse muutmiseks vajaliku maksimaalse samaaegsuse.</span><span class="sxs-lookup"><span data-stu-id="793d6-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="793d6-126">Samaaegsete kasutajate kriteeriumid tähendavad, et kasutaja vastab kõigile järgmistele kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="793d6-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="793d6-127">On sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="793d6-127">Logged on.</span></span>
    - <span data-ttu-id="793d6-128">töötab loendamise ajal kannete/päringutega.</span><span class="sxs-lookup"><span data-stu-id="793d6-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="793d6-129">Ei ole jõudeolekus.</span><span class="sxs-lookup"><span data-stu-id="793d6-129">Not an idle session.</span></span>

- <span data-ttu-id="793d6-130">**Andmete koosseis** – see tähendab enamasti seda, kuidas teie süsteem seadistatakse ja konfigureeritakse.</span><span class="sxs-lookup"><span data-stu-id="793d6-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="793d6-131">Näiteks kui palju on teil juriidilisi isikuid, kui palju üksusi, kui palju koosluse tasemeid ja kui keeruline on teie turbeseadistus.</span><span class="sxs-lookup"><span data-stu-id="793d6-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="793d6-132">Kõik need tegurid võivad jõudlust veidi mõjutada, seega saab need taristu loomisel nutikate valikute abil kõrvale nihutada.</span><span class="sxs-lookup"><span data-stu-id="793d6-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="793d6-133">**Laiendused** – kohandused võivad olla lihtsad või keerulised.</span><span class="sxs-lookup"><span data-stu-id="793d6-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="793d6-134">Kohanduste arvul ning keerukusel ja kasutusel on taristu vajalikule suurusele muutuv mõju.</span><span class="sxs-lookup"><span data-stu-id="793d6-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="793d6-135">Keeruliste kohanduste puhul on soovitatav teha jõudluse hindamisi tagamaks, et neid ei testitaks üksnes tõhususe suhtes, vaid ka selleks, et mõista taristu vajadusi.</span><span class="sxs-lookup"><span data-stu-id="793d6-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="793d6-136">See on isegi veel kriitilisem, kui laiendused pole jõudluse ja skaleeritavuse jaoks parimate tavade järgi kodeeritud.</span><span class="sxs-lookup"><span data-stu-id="793d6-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="793d6-137">**Aruandlus ja analüüs** – need tegurid sisaldavad tavaliselt töötavaid väga sagedasi päringuid erinevatest andmebaasidest süsteemides.</span><span class="sxs-lookup"><span data-stu-id="793d6-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the system.</span></span> <span data-ttu-id="793d6-138">Sageduse mõistmine ja vähendamine kuluaruannete käitamisel aitab teil mõista nende mõju.</span><span class="sxs-lookup"><span data-stu-id="793d6-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="793d6-139">**Kolmanda osapoole lahendused** – neil lahendustel, nagu ISV-d, on sama mõju ja soovitused kui laienduste puhul.</span><span class="sxs-lookup"><span data-stu-id="793d6-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-environment"></a><span data-ttu-id="793d6-140">Keskkonna suuruse muutmine</span><span class="sxs-lookup"><span data-stu-id="793d6-140">Sizing your environment</span></span>

<span data-ttu-id="793d6-141">Suuruse muutmise nõuete mõistmiseks peate teadma kannete maksimaalset mahtu, mida peate töötlema.</span><span class="sxs-lookup"><span data-stu-id="793d6-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="793d6-142">Enamik abistavaid süsteeme, nagu halduse aruandja või SSRS, on vähem missioonikriitilised.</span><span class="sxs-lookup"><span data-stu-id="793d6-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="793d6-143">Seetõttu keskendub see dokument peamiselt AOS-ile ja SQL Serverile.</span><span class="sxs-lookup"><span data-stu-id="793d6-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="793d6-144">Üldiselt selgitatakse välja arvutusjärgud ja seda tuleks teha meetodil N + 1, mis tähendab, et kui hindate kolme AOS-i, lisage neljas AOS.</span><span class="sxs-lookup"><span data-stu-id="793d6-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="793d6-145">Andmebaasijärk tuleks seadistada hästi kättesaadava seadistuse meetodil „alati sees”.</span><span class="sxs-lookup"><span data-stu-id="793d6-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="793d6-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="793d6-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="793d6-147">Suuruse muutmine</span><span class="sxs-lookup"><span data-stu-id="793d6-147">Sizing</span></span>

- <span data-ttu-id="793d6-148">3000 kuni 15 000 kanderida tunnis iga andmebaasiserveri tuuma kohta.</span><span class="sxs-lookup"><span data-stu-id="793d6-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="793d6-149">AOS-i ja SQL-i tuumade suhe primaarse SQL Serveri puhul on tüüpiliselt 3 : 1.</span><span class="sxs-lookup"><span data-stu-id="793d6-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="793d6-150">Lisatuumad on vajalikud olenevalt valitud suure kättesaadavuse konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="793d6-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="793d6-151">Andmebaasile raskete toimingute töötlemine võib selle vähendada suhtele 2 : 1.</span><span class="sxs-lookup"><span data-stu-id="793d6-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="793d6-152">Erinevust mõjutavad järgmised tegurid.</span><span class="sxs-lookup"><span data-stu-id="793d6-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="793d6-153">Kasutatavad parameetrisätted.</span><span class="sxs-lookup"><span data-stu-id="793d6-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="793d6-154">Laienduste tasemed.</span><span class="sxs-lookup"><span data-stu-id="793d6-154">Levels of extensions.</span></span>
    - <span data-ttu-id="793d6-155">Lisafunktsioonide, nagu andmebaasilogid ja hoiatused, kasutamine.</span><span class="sxs-lookup"><span data-stu-id="793d6-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="793d6-156">Äärmuslik andmebaasilogimine vähendab läbilaskevõimet tunnis tuuma kohta veelgi vähem kui 3000 reale.</span><span class="sxs-lookup"><span data-stu-id="793d6-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="793d6-157">Andmete koosseisu keerukus – lihtsa kontoplaani mõju läbilaskevõimele on teistsugune kui näiteks põhjaliku ja detailse kontoplaani puhul.</span><span class="sxs-lookup"><span data-stu-id="793d6-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="793d6-158">Kannete iseloomustus.</span><span class="sxs-lookup"><span data-stu-id="793d6-158">Transaction characterization.</span></span>
    - <span data-ttu-id="793d6-159">2 GB kuni 16 GB mälu iga tuuma kohta.</span><span class="sxs-lookup"><span data-stu-id="793d6-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="793d6-160">Abistavad andmebaasid andmebaasiserveris, nagu halduse aruandja ja SSRS-i andmebaasid.</span><span class="sxs-lookup"><span data-stu-id="793d6-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="793d6-161">Ajutine andmebaas = 15% andmebaasimahust, võrdse failide ja füüsiliste protsessorite arvuga.</span><span class="sxs-lookup"><span data-stu-id="793d6-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="793d6-162">SAN-i suurus ja läbilaskevõime põhinevad samaaegsete kannete kogumahul/-kasutusel.</span><span class="sxs-lookup"><span data-stu-id="793d6-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="793d6-163">Suur kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="793d6-163">High availability</span></span>

<span data-ttu-id="793d6-164">Soovitame kogumi või peegelduse seadistamisel kasutada alati SQL Serverit.</span><span class="sxs-lookup"><span data-stu-id="793d6-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="793d6-165">SQL-i teisel sõlmel peab olema sama arv tuumi mis primaarsel sõlmel.</span><span class="sxs-lookup"><span data-stu-id="793d6-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="793d6-166">Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="793d6-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="793d6-167">AD FS-i suuruse muutmiseks vaadake [AD FS-i serveri jõudluse dokumentatsiooni](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="793d6-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="793d6-168">Teie juurutuses eksemplaride arvu kavandamiseks on saadaval [suuruse muutmise tabel](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx).</span><span class="sxs-lookup"><span data-stu-id="793d6-168">A [sizing spreadsheet](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="793d6-169">AOS (veebipõhine ja pakktöötlus)</span><span class="sxs-lookup"><span data-stu-id="793d6-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="793d6-170">Suuruse muutmine</span><span class="sxs-lookup"><span data-stu-id="793d6-170">Sizing</span></span>

- <span data-ttu-id="793d6-171">Suuruse muutmine kannete mahu/kasutuse järgi</span><span class="sxs-lookup"><span data-stu-id="793d6-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="793d6-172">2000–6000 rida tuuma kohta</span><span class="sxs-lookup"><span data-stu-id="793d6-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="793d6-173">16 GB eksemplari kohta</span><span class="sxs-lookup"><span data-stu-id="793d6-173">16 GB per instance</span></span>
    - <span data-ttu-id="793d6-174">Standardne kast – 4–24 tuuma</span><span class="sxs-lookup"><span data-stu-id="793d6-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="793d6-175">10–15 ettevõtte kasutajat tuuma kohta</span><span class="sxs-lookup"><span data-stu-id="793d6-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="793d6-176">15–25 tegevuste kasutajat tuuma kohta</span><span class="sxs-lookup"><span data-stu-id="793d6-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="793d6-177">25–50 töörühma liiget tuuma kohta</span><span class="sxs-lookup"><span data-stu-id="793d6-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="793d6-178">Partii</span><span class="sxs-lookup"><span data-stu-id="793d6-178">Batch</span></span>

    - <span data-ttu-id="793d6-179">1–4 pakktöötluslõime tuuma kohta</span><span class="sxs-lookup"><span data-stu-id="793d6-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="793d6-180">Pakktöötlusakna iseloomustusel põhinev suurus</span><span class="sxs-lookup"><span data-stu-id="793d6-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="793d6-181">Pange tähele, et AOS-il. andmehaldusel ja pakktöötlusel on Service Fabricus sama roll.</span><span class="sxs-lookup"><span data-stu-id="793d6-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="793d6-182">Peate valima suuruse nende kolme töökoormuse kohta kokku ega tohi neid eraldada nagu rakenduses Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="793d6-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="793d6-183">Siin kehtivad samad varieeruvustegurid mis SQL Serveri puhul.</span><span class="sxs-lookup"><span data-stu-id="793d6-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="793d6-184">Suur kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="793d6-184">High availability</span></span>

- <span data-ttu-id="793d6-185">Veenduge, et teil oleks saadaval vähemalt 1–2 AOS-i rohkem kui prognoosite.</span><span class="sxs-lookup"><span data-stu-id="793d6-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="793d6-186">Veenduge, et teil oleks saadaval vähemalt 3–4 virtuaalset hosti.</span><span class="sxs-lookup"><span data-stu-id="793d6-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="793d6-187">Halduse aruandja</span><span class="sxs-lookup"><span data-stu-id="793d6-187">Management reporter</span></span>

<span data-ttu-id="793d6-188">Enamasti peaks soovitatud miinimumnõuded, kasutades kaht sõlme, hästi toimima, kui neid ulatuslikult ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="793d6-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="793d6-189">Ainult juhtudel, kui kasutuskoormus on suur, vajate rohkem kui kaht sõlme.</span><span class="sxs-lookup"><span data-stu-id="793d6-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="793d6-190">Skaleerige vajadust mööda.</span><span class="sxs-lookup"><span data-stu-id="793d6-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="793d6-191">SQL Serveri aruandlusteenused</span><span class="sxs-lookup"><span data-stu-id="793d6-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="793d6-192">Üldiselt kättesaadava versiooni puhul saab juurutada ainult ühe SSRS-i sõlme.</span><span class="sxs-lookup"><span data-stu-id="793d6-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="793d6-193">Jälgige oma SSRS-i sõlme testimise ajal ja suurendage SSRS-i jaoks saadaolevate tuumade arvu vajadust mööda.</span><span class="sxs-lookup"><span data-stu-id="793d6-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="793d6-194">Veenduge, et teil oleks virtuaalhostis saadaval eelkonfigureeritud teisene sõlm, mis ei ole SSRS-i virtuaalarvuti.</span><span class="sxs-lookup"><span data-stu-id="793d6-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="793d6-195">See on oluline, kui SSRS-i või virtuaalhosti majutava virtuaalarvutiga tekib mõni probleem.</span><span class="sxs-lookup"><span data-stu-id="793d6-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="793d6-196">Sellisel juhul tuleb see arvutada.</span><span class="sxs-lookup"><span data-stu-id="793d6-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="793d6-197">Keskkonna korraldaja</span><span class="sxs-lookup"><span data-stu-id="793d6-197">Environment Orchestrator</span></span>

<span data-ttu-id="793d6-198">Korraldusteenus on teenus, mis haldab teie juurutust ja seotud sidet LCS-iga.</span><span class="sxs-lookup"><span data-stu-id="793d6-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="793d6-199">See teenus juurutatakse primaarse Service Fabricu teenusena ja nõuab vähemalt kolme virtuaalarvutit.</span><span class="sxs-lookup"><span data-stu-id="793d6-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="793d6-200">Teenus asub samas kohas mis Service Fabricu korraldusteenused.</span><span class="sxs-lookup"><span data-stu-id="793d6-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="793d6-201">Selle suurus tuleks määrata kogumi tippkoormuse järgi.</span><span class="sxs-lookup"><span data-stu-id="793d6-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="793d6-202">Lisateavet vaadake jaotisest [Service Fabricu kogumi jõudlusplaani kaalutlused](/azure/service-fabric/service-fabric-cluster-capacity).</span><span class="sxs-lookup"><span data-stu-id="793d6-202">For more information, see [Service Fabric cluster capacity planning considerations](/azure/service-fabric/service-fabric-cluster-capacity).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="793d6-203">Virtualiseerimine ja ületellimine</span><span class="sxs-lookup"><span data-stu-id="793d6-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="793d6-204">Missioonikriitilisi teenuseid, nagu AOS, tuleks majutada virtuaalhostides, millel on spetsiaalsed ressursid – tuumad, mälu ja ketas.</span><span class="sxs-lookup"><span data-stu-id="793d6-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>