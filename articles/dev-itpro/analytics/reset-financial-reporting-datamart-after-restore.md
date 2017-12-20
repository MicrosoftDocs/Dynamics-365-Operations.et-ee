---
title: "Finantsaruandluse andmevaka lähtestamine"
description: "Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: et-ee
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Finantsaruandluse andmevaka lähtestamine

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka järgmistes versioonides.

- Rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaanne 7.2.6.0 ja uuem
- Rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaanne 7.0.10000.4 ja uuem
- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (kohapealne)

Rakenduse Finance and Operations finantsaruandluse väljaande 7.2.6.0 hankimiseks saate laadida alla teabebaasi artikli nr 4052514 aadressilt <https://support.microsoft.com/en-us/help/4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Rakenduse Finance and Operations finantsaruandluse väljaande 7.2.6.0 ja uuema finantsaruandluse andmevaka lähtestamine

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Aruande koostaja finantsaruandluse andmevaka lähtestamine

> [!NOTE]
> Selle protsessi etappe toetatakse rakenduse Finance and Operations finantsaruandluse väljaandes 7.2.6.0 ja uuemas. Kui teil on varasem väljaanne, pöörduge abi saamiseks tugimeeskonna poole.

Teatud juhtudel võib olla vajalik finantsaruandluse andmevaka lähtestamine. Saate selle ülesande täita aruande koostaja kliendis. Allpool on esitatud mõned stsenaariumid, mille korral võib olla vajalik andmevaka lähtestamine.

- Rakenduse Finance and Operations andmebaas taastati, kuid andmevaka andmebaasi ei taastatud.
- Perioodi kohta kuvatakse valed andmed.
- Tugimeeskond juhendab teid, kuidas lähtestada andmevakka tõrkeotsingu sammu osana.

Andmevakka tuleks lähtestada ainult aegadel, mil töötlemise hulk andmebaasis on väike. Finantsaruandluse pole lähtestamise ajal saadaval.

#### <a name="reset-the-data-mart"></a>Andmevaka lähtestamine

Andmevaka lähtestamiseks avage Aruande koostaja ja valige menüüs **Tööriistad** suvand **Lähtesta andmevakk**. Kuvatud dialoogiboksis on kaks jaotist: **Statistika** ja **Lähtestamine**.

[![Dialoogiboks Lähtesta andmevakk](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>Integratsioonikatsed

Ruudustik **Integratsioonikatsed** näitab, mitu korda süsteem on proovinud kandeid integreerida. Kui esimesed paar katset ebaõnnestuvad, üritab süsteem valitud päevade jooksul andmeid uuesti integreerida. Andmevakk tuleb lähtestada, kui katsete arv on 8 või enam ja dimensioonide kombinatsioone või kandekirjeid on palju. Sellisel juhul ei esitata andmete kohta aruandeid.

##### <a name="data-status"></a>Andmete olek

Ruudustik **Andmete olek** annab hetkeülevaate andmevakas olevatest kannetest, vahetuskurssidest ja dimensiooniväärtustest. Kui aegunud kirjeid on väga palju, näitab see, et eelmisi kirjeid on korduvalt värskendatud. Selle tulemusena võib aruannete loomine minna aeglasemalt.

##### <a name="misaligned-main-account-categories"></a>Valesti joondatud põhikonto kategooriad

Kui kasutate varasemat väljaannet kui rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaanne 7.2.1, võib juhtuda, et peate andmevaka lähtestama, kui nimetate kontosid ümber ja teisaldate kontosid kontokategooriate vahel. Nende tegevuste tagajärjeks võib olla põhikonto kategooriate valesti joondamine. Seda, kas teil on see probleem, näitab väli **Valesti joondatud põhikonto kategooriad**.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Andmevaka lähtestamine rakenduse Finance and Operations finantsaruandluse väljaandes 7.2.6.0

Andmevaka lähtestamiseks rakenduse Finance and Operations finantsaruandluse väljaandes 7.2.6.0 ja varasemas valige dialoogiboksis **Lähtesta andmevakk** märkeruut **Lähtesta andmevakk** ja seejärel klõpsake **OK**. Soovitame andmevakka lähtestada ainult plaanitud seisakuajal.

[![Märkeruut Lähtesta andmevakk](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Andmevaka lähtestamine ja põhjuse valimine rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaandes 7.3.0

Kui otsustate, et andmevaka lähtestamine on vajalik, valige märkeruut **Lähtesta andmevakk** ja valige väljal **Põhjus** lähtestamise põhjus. Valikud on järgmised:

- **Puuduvad või valed andmed** – tegite statistika põhjal kindlaks, et andmeid võib olla puudu. Enne jätkamist soovitame teha koostööd tugimeeskonnaga, et selgitada välja juurpõhjus.
- **Andmebaasi taastamine** – rakenduse Finance and Operations andmebaas taastati, kuid finantsaruandluse andmevaka andmebaasi ei taastatud.
- **Muu** – lähtestate andmevakka mõnel muul põhjusel. Kui usute, et ilmnenud on probleem, võtke selle tuvastamiseks ühendust toega.

> [!NOTE]
> Enne etappide lõpule viimist veenduge, et kõik olemasolevad ülesanded oleksid integreerimise lõpule viinud. Integreerimise oleku nägemiseks valige **Tööriistad** &gt; **Integreerimisolek**.

#### <a name="clear-users-and-companies"></a>Eemalda kasutajad ja ettevõtted

Valige märkeruut **Eemalda kasutajad ja ettevõtted**, kui taastasite oma andmebaasi, kuid muutsite seejärel kasutajaid või ettevõtteid. Seda märkeruutu ei lähe tavaliselt vaja.

Kui olete valmis lähtestamist alustama, valige **OK**. Teil palutakse kinnitada, et olete valmis protsessi käivitama. Pange tähele, et lähtestamise ning hiljem toimuva andmete esialgse integreerimise ajal pole finantsaruandlus saadaval.

Kui soovite saada integreerimise olekust ülevaate, valige **Tööriistad** &gt; **Integreerimisolek**, et näha, millal viimati integreerimine käivitati ja mis oli selle olek.

[![Integreerimise oleku vaatamine](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Rakenduse Finance and Operations finantsaruandluse väljaande 7.0.10000.4 ja uuema finantsaruandluse andmevaka lähtestamine

Kui taastate oma rakenduse Finance and Operations andmebaasi varukoopia põhjal või kopeerite mõnest muust keskkonnast pärit andmebaasi, peate järgima selles jaotises toodud juhiseid tagamaks, et finantsaruandluse andmevakk kasutab taastatud Finance and Operationsi andmebaasi õigesti.

> [!NOTE]
> Selle protsessi etappe toetatakse Microsoft Dynamics AX-i rakenduse versioonis 7.0.1 (mai 2016) (rakenduse järgus 7.0.1265.23014 ja finantsaruandluse järgus 7.0.10000.4) ja uuemates. Kui teil on rakenduse Finance and Operations varasem versioon, pöörduge abi saamiseks tugimeeskonna poole.

### <a name="export-report-definitions"></a>Aruande definitsioonide eksportimine

Esmalt järgige neid etappe, et eksportida aruande koostajast aruande kujundused.

1. Valige aruande koostajas suvandid **Ettevõte** &gt; **Koosteüksuste grupid**.
2. Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**.

    > [!NOTE]
    > Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.

3. Valige eksportimiseks aruande definitsioonid.

    - Kõigi aruandedefinitsioonide ja seotud koosteüksuste eksportimiseks valige **Vali kõik**.
    - Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks valige vastav vahekaart ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl. Eksporditavate aruannete valimisel valitakse nendega seotud read, veerud, puud ja dimensioonikogumid.

4. Valige **Ekspordi**.
5. Sisestage faili nimi ja valige turvaline asukoht, kuhu soovite eksporditud aruande definitsioonid salvestada.
6. Valige **Salvesta**.

Saate faili kopeerida või laadida üles turvalisse asukohta. Sel viisil saab faili hiljem teise keskkonda importida. Lisateavet Microsoft Azure’i salvestuskonto kasutamise kohta vt teemast [Andmeedastus käsurea utiliidiga AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft ei paku Finance and Operationsi lepingu raames salvestuskontot. Peate ostma salvestuskonto või kasutama eraldi Azure’i tellimuse salvestuskontot.

> [!WARNING]
> Olge kursis Azure’i virtuaalarvutite D-ketta käitumisega. Ärge talletage oma eksporditud koosteüksuste gruppe jäädavalt D-kettale. Lisateavet ajutiste ketaste kohta vt teemast [Ajutine ketas Windows Azure’i virtuaalarvutites](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Teenuste peatamine

Järgmistel Microsofti Windowsi teenustel on avatud ühendus Finance and Operationsi andmebaasiga. Seetõttu peate kasutama Microsofti kaugtöölauda ühenduse loomiseks kõigi arvutitega keskkonnas ja seejärel kasutama faili services.msc järgmiste teenuste peatamiseks.

- Ülemaailmse veebi avaldamisteenus (kõigil rakendusobjekti serverite [AOS] arvutitel)
- Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)
- Management Reporter 2012 protsessiteenus (ainult äriteabe [BI] arvutitel)

### <a name="reset"></a>Lähtestamine

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Uusima paketi MinorVersionDataUpgrade.zip allalaadimine

Laadige alla uusim pakett MinorVersionDataUpgrade.zip. Juhiste saamiseks selle kohta, kuidas leida üles ja laadida alla andmete täienduspaketi õige versioon, vt teemat [Uusima andmeuuenduse juurutuspaketi allalaadimine](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Paketi MinorVersionDataUpgrade.zip alla laadimiseks ei ole vaja uuendust. Seega peate lihtsalt järgima selle teema jaotises „Uusima andmeuuenduse juurutuspaketi allalaadimine” olevaid etappe. Võite kõik teised teemas olevad etapid vahele jätta.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Skriptide käivitamine Finance and Operationsi andmebaasi suhtes

Käivitage järgmised skriptid Finance and Operationsi andmebaasi suhtes (mitte finantsaruandluse andmebaasi suhtes).

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Need skriptid aitavad tagada õiged kasutajad, rollid ja muudatuste jälgimise sätted.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Windows PowerShelli käsu käivitamine andmebaasi lähtestamiseks

Käivitage AOS-i arvutis Microsoft Windows PowerShell administraatorina ja käivitage järgmised käsud, et lähtestada Finance and Operationsi ja finantsaruandluse integratsioon.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Siin on käsus **Reset-DatamartIntegration** olevate parameetrite selgitus.

- Parameetri **-Reason** sobivad väärtused on **SERVICING**, **BADDATA** ja **OTHER**.
- Parameeter **-ReasonDetail** on vaba tekst.
- Põhjus ja põhjuse üksikasjad salvestatakse jaotisse telemeetria / keskkonna jälgimine.

> [!NOTE]
> Pärast käskude käivitamist palutakse teil sisestada **Y**, et kinnitada, et soovite andmebaasi lähtestada.

#### <a name="restart-services"></a>Teenuste taaskäivitamine

Taaskäivitage faili services.msc abil eelnevalt peatatud teenused.

- ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)
- Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)
- Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)

#### <a name="import-report-definitions"></a>Aruande definitsioonide importimine

Importige aruande kujundused aruande koostajast, kasutades eksportimise ajal loodud faili.

1. Valige aruande koostajas suvandid **Ettevõte** &gt; **Koosteüksuste grupid**.
2. Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**.

    > [!NOTE]
    > Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.

3. Valige koosteüksus **Vaikeväärtus** ja seejärel valige **Impordi**.
4. Valige eksporditud aruande definitsioone sisaldav fail ja seejärel valige **Ava**.
5. Valige dialoogiboksis **Importimine** imporditav aruandedefinitsioon.

    - Kõigi aruandedefinitsioonide ja seotud koosteüksuste importimiseks valige **Vali kõik**.
    - Valige konkreetsete aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks aruanded, read, veerud, puud või dimensioonikogumid.

6. Valige **Impordi**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Rakenduse Finance and Operations (kohapealne) finantsaruandluse andmevaka lähtestamine

1. Paluge kõigil kasutajatel aruande koostajast ja rakenduse Finance and Operations finantsaruandluse alalt väljuda.
2. Käivitage finantsaruandluse andmebaasi (MRDB) suhtes uuesti järgmine skript.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Lühendage või kustutage rakenduse Finance and Operations andmebaasis (AXDB) kõik kirjed tabelist FINANCIALREPORTS.
4. Lühendage või kustutage kõik kirjed tabelist FINANCIALREPORTVERSION, kui see tabel on rakenduse Finance and Operations andmebaasis olemas. Kui rakenduse Finance and Operations andmebaasis pole seda tabelit, jätke see etapp vahele.
5. Käivitage finantsaruandluse andmebaasi suhtes uuesti skript **ResetDatamart.sql**. See skript keelab andmevaka integreerimise, kustutab kõik andmevaka andmed ja seejärel lubab andmevaka integreerimise uuesti.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Pärast lähtestamist saate uuesti laaditud andmeid käsitsi kontrollida, käivitades finantsaruandluse andmebaasi suhtes järgmise päringu.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Kontrollige, et kõigi ridade väärtus oleks **LastRunTime** ja et suvand **StateType** oleks seatud väärtusele **5**. Suvandi **StateType** väärtus **5** näitab, et andmete uuesti laadimine õnnestus. Väärtus **7** näitab nurjunud olekut. Mõnikord on organisatsiooni hierarhia kaardil selle esimesel käivitamisel see olek. Kuid nurjunud oleku lahendamine peaks olema automaatne.

