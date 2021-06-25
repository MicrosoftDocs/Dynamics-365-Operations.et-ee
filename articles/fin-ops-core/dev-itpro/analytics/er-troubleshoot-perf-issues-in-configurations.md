---
title: Jõudlusprobleemide tõrkeotsing ER-i konfiguratsioonides
description: See teema selgitab, kuidas leida ja lahendada jõudluse probleeme elektroonilise aruandluse (ER) konfiguratsioonides.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216861"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="20dd7-103">Jõudlusprobleemide tõrkeotsing ER-i konfiguratsioonides</span><span class="sxs-lookup"><span data-stu-id="20dd7-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="20dd7-104">See teema selgitab, kuidas leida ja lahendada jõudluse probleeme [elektroonilise aruandluse](general-electronic-reporting.md) (ER) [konfiguratsioonides](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="20dd7-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="20dd7-105">Tavaliselt koosneb toimivuse uurimine mitmest etapist.</span><span class="sxs-lookup"><span data-stu-id="20dd7-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="20dd7-106">[Kogu](#collecting-data) andmeid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="20dd7-107">Analüüsige kogutud andmeid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="20dd7-108">Analüüsi tulemuste põhjal kasutage ER-konfiguratsioone [muudatuste tegemiseks](#making-changes) või otsustage koguda rohkem andmeid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="20dd7-109">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="20dd7-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="20dd7-110">Täitmisaja analüüsimine</span><span class="sxs-lookup"><span data-stu-id="20dd7-110">Analyze execution time</span></span>

<span data-ttu-id="20dd7-111">Täitmisaeg võib sõltuda ettearvamatutest teguritest, näiteks muudest samas keskkonnas töötavatest toimingutest ja vahemällu salvestamisest, mis kasutab andmeid, kui neid esimest korda kutsutakse.</span><span class="sxs-lookup"><span data-stu-id="20dd7-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="20dd7-112">Seetõttu peaksite täitmist ja mõõtmist mitu korda kordama.</span><span class="sxs-lookup"><span data-stu-id="20dd7-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="20dd7-113">Mõnikord ei põhjusta jõudlusprobleeme aruandluseks kasutatav ER-vormingu konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="20dd7-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="20dd7-114">Selle asemel on need põhjustatud X++ koodist, mida kasutatakse selle ER-vormingu konfiguratsiooni avamiseks.</span><span class="sxs-lookup"><span data-stu-id="20dd7-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="20dd7-115">Vaadake [tegevuskeskuses](#infolog-time) või [sündmuselogis](#event-log-time) aruande täitmise aega.</span><span class="sxs-lookup"><span data-stu-id="20dd7-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="20dd7-116">Saate võrrelda aruande täitmisaega stsenaariumi kogu täitmisajaga.</span><span class="sxs-lookup"><span data-stu-id="20dd7-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="20dd7-117">Kui aruande täitmisaeg on palju lühem kui kogu täitmisaeg, kaaluge aruande töödeldavate andmete hulka.</span><span class="sxs-lookup"><span data-stu-id="20dd7-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="20dd7-118">Kui aruanne töötleb väikest hulka andmeid, võib probleemiks olla konfiguratsiooni laadimisaeg.</span><span class="sxs-lookup"><span data-stu-id="20dd7-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="20dd7-119">Kui aruanne töötleb suurt hulka andmeid, võib probleem hõlmata eeltöötlust X++.</span><span class="sxs-lookup"><span data-stu-id="20dd7-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="20dd7-120">Selle juhtumi analüüsimiseks kasutage [trace parserit](#analyze-trace-parser-trace).</span><span class="sxs-lookup"><span data-stu-id="20dd7-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="20dd7-121">Muudel juhtudel vaadake järgmisi jaotisi.</span><span class="sxs-lookup"><span data-stu-id="20dd7-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="20dd7-122">Saate käivitada mitu testi, mis hõlmavad erinevat andmehulka, et määratleda, kuidas täitmisaeg sõltub andmehulgast.</span><span class="sxs-lookup"><span data-stu-id="20dd7-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="20dd7-123">Jälitamised Trace Parseri abil</span><span class="sxs-lookup"><span data-stu-id="20dd7-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="20dd7-124">Valmistage ette väike näide või koguge aruande loomise jaoks juhuslikke osi.</span><span class="sxs-lookup"><span data-stu-id="20dd7-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="20dd7-125">Seejärel [trace-parser\`is](#trace-parser) tehke standardne alt-üles-analüüs ja vastake järgmistele küsimustele:</span><span class="sxs-lookup"><span data-stu-id="20dd7-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="20dd7-126">Millised on ajatarbimise peamised meetodid?</span><span class="sxs-lookup"><span data-stu-id="20dd7-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="20dd7-127">Millist osa koguajast need meetodid kasutavad?</span><span class="sxs-lookup"><span data-stu-id="20dd7-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="20dd7-128">Vastake päringute puhul samadele küsimustele.</span><span class="sxs-lookup"><span data-stu-id="20dd7-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="20dd7-129">Kui näete, et meetodite eesliide on "ER", liikuge edasi järgmisse jaotisse.</span><span class="sxs-lookup"><span data-stu-id="20dd7-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="20dd7-130">Kui näete, et meetodid või päringud pärinevad rakendusekomplektist, kaaluge üldisi optimeerimisi (nt registrite loomine).</span><span class="sxs-lookup"><span data-stu-id="20dd7-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="20dd7-131">Saate analüüsida kõnede arvu.</span><span class="sxs-lookup"><span data-stu-id="20dd7-131">Analyze the number of calls.</span></span> <span data-ttu-id="20dd7-132">Kui arv on oodatust oluliselt suurem, kaaluge konfiguratsiooni vastavate sõlmede vahemällu salvestamist.</span><span class="sxs-lookup"><span data-stu-id="20dd7-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="20dd7-133">Andmebaasikõnede analüüsimine</span><span class="sxs-lookup"><span data-stu-id="20dd7-133">Analyze database calls</span></span>

<span data-ttu-id="20dd7-134">Valmistage ette näide, millel on väike andmehulk, et saaksite koguda [ER-jälge](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="20dd7-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="20dd7-135">Seejärel avage ER-mudeli vastendamise kujundajas jälitus ja vaadake lehe allserva.</span><span class="sxs-lookup"><span data-stu-id="20dd7-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="20dd7-136">Vastake järgmistele küsimustele:</span><span class="sxs-lookup"><span data-stu-id="20dd7-136">Answer the following questions:</span></span>

- <span data-ttu-id="20dd7-137">Kas päringu dubleerimine on olemas?</span><span class="sxs-lookup"><span data-stu-id="20dd7-137">Is there any query duplication?</span></span> <span data-ttu-id="20dd7-138">Kui on, kaaluge ühte järgmistest parandustest:</span><span class="sxs-lookup"><span data-stu-id="20dd7-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="20dd7-139">[Kasutage vahemällu salvestamist](#use-caching) kui arvate, et ühe emakirje sees on mitu kõnet.</span><span class="sxs-lookup"><span data-stu-id="20dd7-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="20dd7-140">[Kasutage vahemällu talletatud, parameetri põhjal arvutatud välja](#cached-parameterized) juhul kui arvate, et erinevates kirjetes on kõnesid samale kirjele.</span><span class="sxs-lookup"><span data-stu-id="20dd7-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="20dd7-141">[Kasutage **ÜHENDA** andmeallikat](#use-join-datasource) kui peate lugema andmebaasist mõnda muud kirjet.</span><span class="sxs-lookup"><span data-stu-id="20dd7-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="20dd7-142">Kas päringute ja toodud kirjete arv vastab andmete koguhulgale?</span><span class="sxs-lookup"><span data-stu-id="20dd7-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="20dd7-143">Näiteks kui dokumendil on 10 rida, kas statistika näitab, et aruanne ekstraktib 10 rida või 1000 rida?</span><span class="sxs-lookup"><span data-stu-id="20dd7-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="20dd7-144">Kui teil on suur hulk tõmmatud kirjeid, kaaluge ühte järgmistest parandustest:</span><span class="sxs-lookup"><span data-stu-id="20dd7-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="20dd7-145">[Kasutage **FILTREERI** funktsiooni **KUS** funktsiooni](#filter) asemel SQL serveri poolel andmete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="20dd7-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="20dd7-146">Samade andmete toomise vältimiseks kasutage vahemällu salvestamist.</span><span class="sxs-lookup"><span data-stu-id="20dd7-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="20dd7-147">[Kogutud andmefunktsioonide abil saate](#collected-data) vältida samade andmete toomist summeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="20dd7-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="20dd7-148">PerfView jälgede analüüsimine</span><span class="sxs-lookup"><span data-stu-id="20dd7-148">Analyze PerfView traces</span></span>

<span data-ttu-id="20dd7-149">[PerfView](#perfview) on tööriist kogenud arendajatele.</span><span class="sxs-lookup"><span data-stu-id="20dd7-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="20dd7-150">Üksikasjalikumat teavet järgmiste sammude kohta leiate teemast [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="20dd7-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="20dd7-151">Saate lõimeaja abil jälituse koguda.</span><span class="sxs-lookup"><span data-stu-id="20dd7-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="20dd7-152">Kaasa ainult virnad, mis kasutavad **käitaSidumata**, et filtreerida ainult lõime, millel on konfiguratsiooni käivitamine.</span><span class="sxs-lookup"><span data-stu-id="20dd7-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="20dd7-153">(Lisage **käitaSidumata** sisendvälja **IncPats** ruutu.)</span><span class="sxs-lookup"><span data-stu-id="20dd7-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="20dd7-154">Voltige kogu protsessor, võrk ja blokeeritud aeg.</span><span class="sxs-lookup"><span data-stu-id="20dd7-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="20dd7-155">[Laadige PerfView jaoks ER-i valmissätted](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="20dd7-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="20dd7-156">Valige **ER** \> **Muu valmissäte**.</span><span class="sxs-lookup"><span data-stu-id="20dd7-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="20dd7-157">Vaata nimesid:</span><span class="sxs-lookup"><span data-stu-id="20dd7-157">Look at the names:</span></span>

    - <span data-ttu-id="20dd7-158">Tõenäoliselt näete platvormi koodi, mis tarbib kõige rohkem aega.</span><span class="sxs-lookup"><span data-stu-id="20dd7-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="20dd7-159">Võite topeltkoputada (või topeltklõpsata) ja minna üles **helistaja kaudu**.</span><span class="sxs-lookup"><span data-stu-id="20dd7-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="20dd7-160">Kui leiate klassid, millel on eesliide "ERExpression" ja kui need on valemitega seotud funktsioonid, võite funktsiooni nime klassi nime põhjal ära arvata ja atribuutide vaatamiseks vaadata ER-i repo-d.</span><span class="sxs-lookup"><span data-stu-id="20dd7-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="20dd7-161">Parandused</span><span class="sxs-lookup"><span data-stu-id="20dd7-161">Fixes</span></span>

- <span data-ttu-id="20dd7-162">Kui näete, et päringud tarbivad suurema osa protsessori ajast, proovige päringute arvu vähendada:</span><span class="sxs-lookup"><span data-stu-id="20dd7-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="20dd7-163">[Vaadake ER-i jälitusi](#analyze-database-calls) dubleeritud päringutele.</span><span class="sxs-lookup"><span data-stu-id="20dd7-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="20dd7-164">Vaadake, kui palju kirjeid on toodud, ja hinnake, kui palju andmeid tuleks teoreetiliselt tuua.</span><span class="sxs-lookup"><span data-stu-id="20dd7-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="20dd7-165">Kui näete, et suurema osa protsessori ajast tarbivad kasutatavad funktsioonid, proovige leida koht konfiguratsioonis, mis tarbib kõige rohkem ressursse.</span><span class="sxs-lookup"><span data-stu-id="20dd7-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="20dd7-166">Kui näete, et suurema osa protsessori ajast tarbivad andmekogumisfunktsioonid, kaaluge nende asendamist *SQL-grupiga* mudeli vastendamise poolel.</span><span class="sxs-lookup"><span data-stu-id="20dd7-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="20dd7-167">Andmete kogumine</span><span class="sxs-lookup"><span data-stu-id="20dd7-167">Collecting data</span></span>

<span data-ttu-id="20dd7-168">Sõltuvalt teie keskkonnast on saadaolevate andmete kogumiseks mitu võimalust:</span><span class="sxs-lookup"><span data-stu-id="20dd7-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="20dd7-169">Hankige kogu käitusaeg:</span><span class="sxs-lookup"><span data-stu-id="20dd7-169">Get the total running time:</span></span>

    - <span data-ttu-id="20dd7-170">Tegevuskeskusest</span><span class="sxs-lookup"><span data-stu-id="20dd7-170">From the Action center</span></span>
    - <span data-ttu-id="20dd7-171">Sündmuselogist</span><span class="sxs-lookup"><span data-stu-id="20dd7-171">From the event log</span></span>

- <span data-ttu-id="20dd7-172">Profiili täitmine:</span><span class="sxs-lookup"><span data-stu-id="20dd7-172">Profile the execution:</span></span>

    - <span data-ttu-id="20dd7-173">ER-tööriistade abil</span><span class="sxs-lookup"><span data-stu-id="20dd7-173">By using ER tools</span></span>
    - <span data-ttu-id="20dd7-174">Trace parseri abil</span><span class="sxs-lookup"><span data-stu-id="20dd7-174">By using Trace parser</span></span>
    - <span data-ttu-id="20dd7-175">PerfView abil</span><span class="sxs-lookup"><span data-stu-id="20dd7-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="20dd7-176">Tootmiskeskkonna andmete kogumine</span><span class="sxs-lookup"><span data-stu-id="20dd7-176">Collecting data in a production environment</span></span>

<span data-ttu-id="20dd7-177">Mõnikord saab probleeme paljundada ainult tootmiskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="20dd7-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="20dd7-178">Saate andmeid koguda järgmistel viisidel:</span><span class="sxs-lookup"><span data-stu-id="20dd7-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="20dd7-179">Kasutades [Trace Parser](../perf-test/trace-trace-tutorial.md) jälitamisi</span><span class="sxs-lookup"><span data-stu-id="20dd7-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="20dd7-180">Kasutades [ER-i täitmise](trace-execution-er-troubleshoot-perf.md) jälgi</span><span class="sxs-lookup"><span data-stu-id="20dd7-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="20dd7-181">Kogu täitmisaja abil</span><span class="sxs-lookup"><span data-stu-id="20dd7-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="20dd7-182">Arenduskeskkonna andmete kogumine</span><span class="sxs-lookup"><span data-stu-id="20dd7-182">Collecting data in a development environment</span></span>

<span data-ttu-id="20dd7-183">Lisaks tööriistadele, mida saab kasutada tootmiskeskkonnas, on mitmeid tööriistu, mida saate arenduskeskkonnas kasutada:</span><span class="sxs-lookup"><span data-stu-id="20dd7-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="20dd7-184">Sündmuselogi (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="20dd7-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="20dd7-185">See logi võib anda teile kogu täitmisaja.</span><span class="sxs-lookup"><span data-stu-id="20dd7-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="20dd7-186">Levinumad .NET-i tööriistad nagu näiteks PerfView.</span><span class="sxs-lookup"><span data-stu-id="20dd7-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="20dd7-187">Lisaks annab arenduskeskkond teile rohkem paindlikkust eksperimenteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="20dd7-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="20dd7-188">Näiteks saate aruannete osad välja lülitada, et näha, kuidas täitmisaeg mõjutab.</span><span class="sxs-lookup"><span data-stu-id="20dd7-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="20dd7-189">Tööriistad</span><span class="sxs-lookup"><span data-stu-id="20dd7-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="20dd7-190">Täitmisaeg tegevuskeskuses</span><span class="sxs-lookup"><span data-stu-id="20dd7-190">Execution time in the Action center</span></span>

<span data-ttu-id="20dd7-191">ER saab kuvada konfiguratsiooni täitmisaja tegevuskeskuses.</span><span class="sxs-lookup"><span data-stu-id="20dd7-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="20dd7-192">See suvand töötab ainult kindla kasutaja ja kindla ettevõtte puhul ning ainult interaktiivsete seansside puhul.</span><span class="sxs-lookup"><span data-stu-id="20dd7-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="20dd7-193">Selle funktsiooni kättesaadavaks tegemiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="20dd7-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="20dd7-194">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="20dd7-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20dd7-195">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="20dd7-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="20dd7-196">Dialoogiboksis **Kasutaja parameetrid** määrake suvand **Käivita silumisrežiimis** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="20dd7-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="20dd7-197">Täitmisaeg sündmuselogis</span><span class="sxs-lookup"><span data-stu-id="20dd7-197">Execution time in the event log</span></span>

1. <span data-ttu-id="20dd7-198">Windows Event Viewer avamine.</span><span class="sxs-lookup"><span data-stu-id="20dd7-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="20dd7-199">Jaotises **Rakenduste ja teenuste logid** avage **Microsoft-Dynamics-ElektroonilineAruandlus/Operatsioon**.</span><span class="sxs-lookup"><span data-stu-id="20dd7-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="20dd7-200">Otsige **FormatMapingRun** sündmusi, kus **SündmusID=2**, kuna need sündmused sisaldavad teavet möödunud aja kohta.</span><span class="sxs-lookup"><span data-stu-id="20dd7-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="20dd7-201">Jälitamised Trace Parseri abil</span><span class="sxs-lookup"><span data-stu-id="20dd7-201">Trace parser traces</span></span> 

<span data-ttu-id="20dd7-202">Kuna ER rakendatakse X++-s, saate jõudluse analüüsimiseks kasutada tavalisi X++ tööriistu.</span><span class="sxs-lookup"><span data-stu-id="20dd7-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="20dd7-203">Lisateavet leiate teemast [Trace parseri abil jälgede võtmine](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="20dd7-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="20dd7-204">Sellel lähenemisviisil on mõned piirangud.</span><span class="sxs-lookup"><span data-stu-id="20dd7-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="20dd7-205">Kuna osa ER-ist rakendatakse C#-s, pole kõik üksikasjad saadaval.</span><span class="sxs-lookup"><span data-stu-id="20dd7-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="20dd7-206">Siiski saate vaadata andmekasutuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="20dd7-206">However, you can view the data usage details.</span></span> <span data-ttu-id="20dd7-207">Lisaks võivad pikad aruandeajamid ületada jälgimissalvestuse piiranguid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="20dd7-208">ER jäljed</span><span class="sxs-lookup"><span data-stu-id="20dd7-208">ER traces</span></span>

<span data-ttu-id="20dd7-209">ER võib koguda oma jälgi ning tal on nende jälgede visualiseerimis- ja analüüsivahendid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="20dd7-210">Lisateavet leiate teemast [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="20dd7-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="20dd7-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="20dd7-211">PerfView</span></span>

<span data-ttu-id="20dd7-212">Kuna nii X++ kui ka ER on rakendatud .NET-platvormi peale, saate kasutada levinud .NET-i tööriistu.</span><span class="sxs-lookup"><span data-stu-id="20dd7-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="20dd7-213">Näiteks saate kasutada tasuta [PerfView](https://github.com/Microsoft/perfview) tööriista.</span><span class="sxs-lookup"><span data-stu-id="20dd7-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="20dd7-214">Andmeid saate koguda ka käsurealt.</span><span class="sxs-lookup"><span data-stu-id="20dd7-214">You can also collect data from the command line.</span></span> <span data-ttu-id="20dd7-215">Näiteks järgmine Windows PowerShell skript kogub täitmisaega, kuni mis tahes vormingu täitmine on arvutis peatatud.</span><span class="sxs-lookup"><span data-stu-id="20dd7-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="20dd7-216">Sellel lähenemisviisil on mõned piirangud.</span><span class="sxs-lookup"><span data-stu-id="20dd7-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="20dd7-217">Teil peab olema administratiivne juurdepääs masinale.</span><span class="sxs-lookup"><span data-stu-id="20dd7-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="20dd7-218">Lisaks peate olema kogenud arendaja, sest seal on järsk õppimiskõver.</span><span class="sxs-lookup"><span data-stu-id="20dd7-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="20dd7-219">Muudatuste tegemine</span><span class="sxs-lookup"><span data-stu-id="20dd7-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="20dd7-220">Vahemällu salvestamise kasutamine</span><span class="sxs-lookup"><span data-stu-id="20dd7-220">Use caching</span></span>

<span data-ttu-id="20dd7-221">Kuigi vahemällu salvestamine vähendab aega, mis kulub andmete uuesti toomiseks, maksab see mälu.</span><span class="sxs-lookup"><span data-stu-id="20dd7-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="20dd7-222">Kasutage vahemällu salvestamist juhtudel, kui toodud andmete hulk pole väga suur.</span><span class="sxs-lookup"><span data-stu-id="20dd7-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="20dd7-223">Lisateavet ja näiteid vahemällu salvestamise kasutamise kohta leiate teemast [Mudelivastenduse täiustamine täitmisjälitusjälitusteabe põhjal](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="20dd7-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="20dd7-224">Vahemällu talletatud, parameeter arvutatud välja kasutamine</span><span class="sxs-lookup"><span data-stu-id="20dd7-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="20dd7-225">Mõnikord tuleb väärtusi korduvalt uurida.</span><span class="sxs-lookup"><span data-stu-id="20dd7-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="20dd7-226">Näited hõlmavad kontonimesid ja kontonumbreid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="20dd7-227">Aja säästmiseks saate luua arvutatud välja, millel on ülemise taseme parameetrid, ja seejärel lisada välja vahemällu.</span><span class="sxs-lookup"><span data-stu-id="20dd7-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="20dd7-228">Soovitame seda lähenemist kasutada ainult siis, kui vahemällu talletatud andmete maht on väike.</span><span class="sxs-lookup"><span data-stu-id="20dd7-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="20dd7-229">Lisateavet vt teemast [ER lahenduste täiustamine arvutatud välja parametriseeritud andmeallika lisamisega](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="20dd7-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="20dd7-230">Kasutage ÜHILDA andmeallikat</span><span class="sxs-lookup"><span data-stu-id="20dd7-230">Use a JOIN data source</span></span>

<span data-ttu-id="20dd7-231">**ÜHILDA** andmeallikas võimaldab ühe päringu abil tuua mitu ühendatud kirjet.</span><span class="sxs-lookup"><span data-stu-id="20dd7-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="20dd7-232">Iga ühendatud kirje toomiseks ei pea kasutama eraldi päringut.</span><span class="sxs-lookup"><span data-stu-id="20dd7-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="20dd7-233">Näiteks kui teil on 1000 rida ja toote kaubaandmed iga rea kohta seoste kaupa, on teil 1001 päringut (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="20dd7-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="20dd7-234">Kui kasutate **ÜHILDA** andmeallikat, saate samade andmete toomiseks kasutada ainult ühte päringut.</span><span class="sxs-lookup"><span data-stu-id="20dd7-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="20dd7-235">Vaata lisateavet [Andmeallikate ÜHILDA kasutamine andmete saamiseks mitmest rakendusetabelist elektroonilise aruandluse (ER) mudeli vastendustes](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="20dd7-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="20dd7-236">Kasutage funktsiooni KUS asemel funktsiooni FILTER</span><span class="sxs-lookup"><span data-stu-id="20dd7-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="20dd7-237">**[FILTER](er-functions-list-filter.md)** funktsioon käitab SQL Serveris tingimusi, samas kui **KUS** funktsioon toob kõik andmed loendist, ühe kirje korraga ja rakendab tingimuse iga kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="20dd7-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="20dd7-238">Näiteks soovite valida ühe kirje 1000 kirjest.</span><span class="sxs-lookup"><span data-stu-id="20dd7-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="20dd7-239">Kui kasutate **KUS**, tuuakse kõik 1000 kirjet.</span><span class="sxs-lookup"><span data-stu-id="20dd7-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="20dd7-240">Kui aga kasutate **FILTRIT**, tuuakse täpselt üks kirje.</span><span class="sxs-lookup"><span data-stu-id="20dd7-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="20dd7-241">**FILTRIT** saab kasutada ka indekseid andmebaasi poolel.</span><span class="sxs-lookup"><span data-stu-id="20dd7-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="20dd7-242">Kogutud andmefunktsioonide või akumuleeritud andmeallika kasutamine</span><span class="sxs-lookup"><span data-stu-id="20dd7-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="20dd7-243">Kui teie konfiguratsioonil on *grupeerige* komponentide rühm, mis võtab kokku varem aruande alusel toodud andmed, toob komponent kõik andmed uuesti.</span><span class="sxs-lookup"><span data-stu-id="20dd7-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="20dd7-244">Kogutud andmefunktsioonide abil saate lubada ER-l koguda andmeid esimese toomise ajal.</span><span class="sxs-lookup"><span data-stu-id="20dd7-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="20dd7-245">Lisateavet vt jaotisest [ER vormingu konfigureerimine inventuuri tegemiseks ja summeerimiseks](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="20dd7-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="20dd7-246">Konfiguratsiooni osade ümberkirjutamine X++</span><span class="sxs-lookup"><span data-stu-id="20dd7-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="20dd7-247">ER toetab tabelite ja klasside helistamismeetodeid, sealhulgas laiendusi.</span><span class="sxs-lookup"><span data-stu-id="20dd7-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="20dd7-248">Jõudluse parandamiseks kaaluge x++ mudelivastenduse osade ümberkirjutamist.</span><span class="sxs-lookup"><span data-stu-id="20dd7-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="20dd7-249">ER võib tarbida andmeid järgmistest allikatest:</span><span class="sxs-lookup"><span data-stu-id="20dd7-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="20dd7-250">Klassid (**objekti** ja **klass** andmeallikad)</span><span class="sxs-lookup"><span data-stu-id="20dd7-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="20dd7-251">Tabelid (**tabel** ja **tabeli kirjed** andmeallikad)</span><span class="sxs-lookup"><span data-stu-id="20dd7-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="20dd7-252">[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) pakub ka võimalust saata kõnekoodist eelarvutatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="20dd7-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="20dd7-253">Rakenduskomplekt sisaldab arvukalt näiteid selle lähenemisviisi kohta.</span><span class="sxs-lookup"><span data-stu-id="20dd7-253">The application suite contains numerous examples of this approach.</span></span>
