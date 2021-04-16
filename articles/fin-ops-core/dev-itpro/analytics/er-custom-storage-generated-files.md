---
title: Loodud dokumentidele kohandatud salvestuskohtade määramine
description: Selles teemas selgitatakse, kuidas laiendada talletuskohtade loendit dokumentidele, mille on loodud elektroonilise aruandluse (ER) vormingud.
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 25719de3d86785442e00f7375de525b95bdb094d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753692"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="30a8f-103">Loodud dokumentidele kohandatud salvestuskohtade määramine</span><span class="sxs-lookup"><span data-stu-id="30a8f-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="30a8f-104">Elektroonilise aruandluse (ER) rakenduse programmeerimisliidese (API) raamistik võimaldab teil laiendada talletuskohtade loendit ER vormingute loodavatele dokumentidele.</span><span class="sxs-lookup"><span data-stu-id="30a8f-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="30a8f-105">See teema selgitab, kuidas lisada loodud dokumentidele kohandatud talletuskoht, delegeerides ülesande luua ER-i sihtkohad vaikimisi sihtkoha tehases ja rakendada seejärel kohandatud klassi, millel on oma sihtkoha loogika.</span><span class="sxs-lookup"><span data-stu-id="30a8f-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30a8f-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="30a8f-106">Prerequisites</span></span>

<span data-ttu-id="30a8f-107">Juurutage topoloogia, mis toetab pidevat järku.</span><span class="sxs-lookup"><span data-stu-id="30a8f-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="30a8f-108">Lisainfo saamiseks vt [Pideva järgu ja testimise automaatikat toetavate topoloogiate juurutamine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="30a8f-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="30a8f-109">Samuti peab teil olema sellele topoloogiale juurdepääs ühe järgmise rolliga.</span><span class="sxs-lookup"><span data-stu-id="30a8f-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="30a8f-110">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="30a8f-110">Electronic reporting developer</span></span>
- <span data-ttu-id="30a8f-111">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="30a8f-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="30a8f-112">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="30a8f-112">System administrator</span></span>

<span data-ttu-id="30a8f-113">Samuti peab teil selle topoloogia puhul olema juurdepääs arenduskeskkonnale.</span><span class="sxs-lookup"><span data-stu-id="30a8f-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="30a8f-114">Kõik selle teema ülesanded saab täita ettevõttes **USMF**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="30a8f-115">Impordib põhivara edasiarendus ER-i vormingus</span><span class="sxs-lookup"><span data-stu-id="30a8f-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="30a8f-116">Dokumentide loomiseks, mida kavatsete kohandatud talletuskoht lisada, [importige](er-download-configurations-global-repo.md) **põhivara edasiarvestuse** ER-i vormingu konfiguratsioon praegusesse topoloogiasse.</span><span class="sxs-lookup"><span data-stu-id="30a8f-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Konfiguratsioonihoidla leht](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="30a8f-118">Käitage põhivara edasiarvestuse aruanne</span><span class="sxs-lookup"><span data-stu-id="30a8f-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="30a8f-119">Avage jaotis **Põhivarad** \> **Päringud ja aruanded** \> **Kande aruanded** \> **Põhivara edasiarvestus**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="30a8f-120">Sisestage väljale **Alates kuupäevast** väärtus **1/1/2017** (1. jaanuar 2017).</span><span class="sxs-lookup"><span data-stu-id="30a8f-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="30a8f-121">Sisestage väljale **Lõpukuupäev** väärtus **1/31/2017** (31. jaanuar 2017).</span><span class="sxs-lookup"><span data-stu-id="30a8f-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="30a8f-122">Valige väljal **Valuuta** sobiv **Raamatupidamise valuuta**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="30a8f-123">Valige väljal **Vormingu vastendamine** väärtus **Põhivara edasiarvestus**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="30a8f-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-124">Select **OK**.</span></span>

![Põhivara edasiarenduse aruande käitusaja dialoogiboks](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="30a8f-126">Vaadake Microsoft Excelis üle väljamineva dokumendi, mis on loodud ja allalaadimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="30a8f-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="30a8f-127">Selline käitumine on [vaikimisi käitumine](electronic-reporting-destinations.md#default-behavior) ER-i vormingu jaoks, mille jaoks ei ole konfigureeritud ühtegi [sihtkohta](electronic-reporting-destinations.md) ja mis töötab interaktiivses režiimis.</span><span class="sxs-lookup"><span data-stu-id="30a8f-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="30a8f-128">Lähtekoodi läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="30a8f-128">Review the source code</span></span>

<span data-ttu-id="30a8f-129">Vaadake läbi klassi `AssetRollForwardService` meetodi `generateReportByGER()` kood.</span><span class="sxs-lookup"><span data-stu-id="30a8f-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="30a8f-130">Pange tähele, et meetodit `Run()` kasutatakse ER-i raamistiku kutsumiseks ja **põhivara edasiarenduse** aruande loomiseks.</span><span class="sxs-lookup"><span data-stu-id="30a8f-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="30a8f-131">Lähtekoodi muutmine</span><span class="sxs-lookup"><span data-stu-id="30a8f-131">Modify the source code</span></span>

1. <span data-ttu-id="30a8f-132">Lisage oma Visual Studio projektis uus klass (selles näites `AssetRollForwardDestination`) ja kirjutage kood, et rakendada oma kohandatud sihtkoht loodava **põhivara edasiarenduse** aruande joaks.</span><span class="sxs-lookup"><span data-stu-id="30a8f-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="30a8f-133">Meetodi `new()` eesmärk on hankida algne ER-i sihtkoha objekt ja rakenduse loogika juhitud parameeter, mis määrab kohandatud asukoha, kus loodud aruanded tuleks talletada.</span><span class="sxs-lookup"><span data-stu-id="30a8f-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="30a8f-134">Selles näites on kohandatud asukoht serveri kohaliku failisüsteemi kausta nimi, kus käitatakse rakendusobjekti serveri (AOS) teenust.</span><span class="sxs-lookup"><span data-stu-id="30a8f-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="30a8f-135">Meetodi `saveFile()` eesmärk on salvestada loodud dokument AOS-i teenust käitava serveri kohaliku failisüsteemi kausta.</span><span class="sxs-lookup"><span data-stu-id="30a8f-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="30a8f-136">Lisage oma Visual Studio projektis uus klass (selles näites `AssetRollForwardDestinationFactory`) ja kirjutage kood, et seadistada kohandatud sihtkoha tehas, mis delegeerib sihtkoha loomise sihtkoha tehasele, ja mähkida faili sihtkohta koos oma sihtkohaga.</span><span class="sxs-lookup"><span data-stu-id="30a8f-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="30a8f-137">Muutke olemasolevat klassi `AssetRollForwardService` ja kirjutage kood, et seadistada kohandatud sihtkoha tehases aruande käitaja.</span><span class="sxs-lookup"><span data-stu-id="30a8f-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="30a8f-138">Pange tähele, et kui kohandatud sihtkoha vabrik on loodud, edastatakse rakenduse juhitud parameeter, mis määrab sihtkausta.</span><span class="sxs-lookup"><span data-stu-id="30a8f-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="30a8f-139">Sel viisil kasutatakse sihtkausta loodud failide talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="30a8f-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="30a8f-140">Veenduge, et määratud kaust (selles näites **c:\\0**) on AOS-i teenust käitava serveri kohalikus failisüsteemis olemas.</span><span class="sxs-lookup"><span data-stu-id="30a8f-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="30a8f-141">Vastasel juhul kuvatakse käitusajal erand [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="30a8f-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="30a8f-142">Looge oma projekt uuesti.</span><span class="sxs-lookup"><span data-stu-id="30a8f-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="30a8f-143">Käitage uuesti põhivara edasiarvestuse aruanne</span><span class="sxs-lookup"><span data-stu-id="30a8f-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="30a8f-144">Avage jaotis **Põhivarad** \> **Päringud ja aruanded** \> **Kande aruanded** \> **Põhivara edasiarvestus**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="30a8f-145">Sisestage väljale **Alates kuupäevast** väärtus **1/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="30a8f-146">Sisestage väljale **Kuni kuupäevani** väärtus **1/31/2017**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="30a8f-147">Valige väljal **Valuuta** sobiv **Raamatupidamise valuuta**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="30a8f-148">Valige väljal **Vormingu vastendamine** väärtus **Põhivara edasiarvestus**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="30a8f-149">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="30a8f-149">Select **OK**.</span></span>
7. <span data-ttu-id="30a8f-150">Sirvige kohalikku **C:\\0** kausta, et leida loodud fail.</span><span class="sxs-lookup"><span data-stu-id="30a8f-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="30a8f-151">Kuna objekti `originDestination` ei kasutata selles näites objekti `AssetRollForwardDestination` jaoks, ER-i vormingute konfiguratsioone [sihtkohad](electronic-reporting-destinations.md) käitusajal ignoreeritakse.</span><span class="sxs-lookup"><span data-stu-id="30a8f-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30a8f-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="30a8f-152">Additional resources</span></span>

- [<span data-ttu-id="30a8f-153">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="30a8f-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="30a8f-154">Laiendatavuse avaleht</span><span class="sxs-lookup"><span data-stu-id="30a8f-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]