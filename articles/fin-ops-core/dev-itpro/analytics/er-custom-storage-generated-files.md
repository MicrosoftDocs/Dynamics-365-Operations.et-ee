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
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Loodud dokumentidele kohandatud salvestuskohtade määramine

[!include[banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) rakenduse programmeerimisliidese (API) raamistik võimaldab teil laiendada talletuskohtade loendit ER vormingute loodavatele dokumentidele. See teema selgitab, kuidas lisada loodud dokumentidele kohandatud talletuskoht, delegeerides ülesande luua ER-i sihtkohad vaikimisi sihtkoha tehases ja rakendada seejärel kohandatud klassi, millel on oma sihtkoha loogika.

## <a name="prerequisites"></a>Eeltingimused

Juurutage topoloogia, mis toetab pidevat järku. Lisainfo saamiseks vt [Pideva järgu ja testimise automaatikat toetavate topoloogiate juurutamine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Samuti peab teil olema sellele topoloogiale juurdepääs ühe järgmise rolliga.

- Elektroonilise aruandluse arendaja
- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Samuti peab teil selle topoloogia puhul olema juurdepääs arenduskeskkonnale.

Kõik selle teema ülesanded saab täita ettevõttes **USMF**.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Impordib põhivara edasiarendus ER-i vormingus

Dokumentide loomiseks, mida kavatsete kohandatud talletuskoht lisada, [importige](er-download-configurations-global-repo.md) **põhivara edasiarvestuse** ER-i vormingu konfiguratsioon praegusesse topoloogiasse.

![Konfiguratsioonihoidla leht](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Käitage põhivara edasiarvestuse aruanne

1. Avage jaotis **Põhivarad** \> **Päringud ja aruanded** \> **Kande aruanded** \> **Põhivara edasiarvestus**.
2. Sisestage väljale **Alates kuupäevast** väärtus **1/1/2017** (1. jaanuar 2017).
3. Sisestage väljale **Lõpukuupäev** väärtus **1/31/2017** (31. jaanuar 2017).
4. Valige väljal **Valuuta** sobiv **Raamatupidamise valuuta**.
5. Valige väljal **Vormingu vastendamine** väärtus **Põhivara edasiarvestus**.
6. Valige nupp **OK**.

![Põhivara edasiarenduse aruande käitusaja dialoogiboks](./media/er-custom-storage-generated-files-runtime-dialog.png)

Vaadake Microsoft Excelis üle väljamineva dokumendi, mis on loodud ja allalaadimiseks saadaval. Selline käitumine on [vaikimisi käitumine](electronic-reporting-destinations.md#default-behavior) ER-i vormingu jaoks, mille jaoks ei ole konfigureeritud ühtegi [sihtkohta](electronic-reporting-destinations.md) ja mis töötab interaktiivses režiimis.

## <a name="review-the-source-code"></a>Lähtekoodi läbivaatamine

Vaadake läbi klassi `AssetRollForwardService` meetodi `generateReportByGER()` kood. Pange tähele, et meetodit `Run()` kasutatakse ER-i raamistiku kutsumiseks ja **põhivara edasiarenduse** aruande loomiseks.

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

## <a name="modify-the-source-code"></a>Lähtekoodi muutmine

1. Lisage oma Visual Studio projektis uus klass (selles näites `AssetRollForwardDestination`) ja kirjutage kood, et rakendada oma kohandatud sihtkoht loodava **põhivara edasiarenduse** aruande joaks.

    - Meetodi `new()` eesmärk on hankida algne ER-i sihtkoha objekt ja rakenduse loogika juhitud parameeter, mis määrab kohandatud asukoha, kus loodud aruanded tuleks talletada. Selles näites on kohandatud asukoht serveri kohaliku failisüsteemi kausta nimi, kus käitatakse rakendusobjekti serveri (AOS) teenust.
    - Meetodi `saveFile()` eesmärk on salvestada loodud dokument AOS-i teenust käitava serveri kohaliku failisüsteemi kausta.

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

2. Lisage oma Visual Studio projektis uus klass (selles näites `AssetRollForwardDestinationFactory`) ja kirjutage kood, et seadistada kohandatud sihtkoha tehas, mis delegeerib sihtkoha loomise sihtkoha tehasele, ja mähkida faili sihtkohta koos oma sihtkohaga.

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

3. Muutke olemasolevat klassi `AssetRollForwardService` ja kirjutage kood, et seadistada kohandatud sihtkoha tehases aruande käitaja. Pange tähele, et kui kohandatud sihtkoha vabrik on loodud, edastatakse rakenduse juhitud parameeter, mis määrab sihtkausta. Sel viisil kasutatakse sihtkausta loodud failide talletamiseks.

    > [!NOTE] 
    > Veenduge, et määratud kaust (selles näites **c:\\0**) on AOS-i teenust käitava serveri kohalikus failisüsteemis olemas. Vastasel juhul kuvatakse käitusajal erand [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).

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

4. Looge oma projekt uuesti.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Käitage uuesti põhivara edasiarvestuse aruanne

1. Avage jaotis **Põhivarad** \> **Päringud ja aruanded** \> **Kande aruanded** \> **Põhivara edasiarvestus**.
2. Sisestage väljale **Alates kuupäevast** väärtus **1/1/2017**.
3. Sisestage väljale **Kuni kuupäevani** väärtus **1/31/2017**.
4. Valige väljal **Valuuta** sobiv **Raamatupidamise valuuta**.
5. Valige väljal **Vormingu vastendamine** väärtus **Põhivara edasiarvestus**.
6. Valige nupp **OK**.
7. Sirvige kohalikku **C:\\0** kausta, et leida loodud fail.

> [!NOTE]
> Kuna objekti `originDestination` ei kasutata selles näites objekti `AssetRollForwardDestination` jaoks, ER-i vormingute konfiguratsioone [sihtkohad](electronic-reporting-destinations.md) käitusajal ignoreeritakse.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Laiendatavuse avaleht](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]