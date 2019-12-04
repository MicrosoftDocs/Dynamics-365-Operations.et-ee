---
title: Loodud dokumentidele kohandatud talletuskoha määramine
description: Selles teemas selgitatakse, kuidas laiendada talletuskohtade loendit dokumentidele, mille loovad elektroonilise aruandluse (ER) vormingud.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2c7ee610c6e3c446a4bcc9d6d46ca72dd71cb23c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771394"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="df781-103">Loodud dokumentidele kohandatud talletuskoha määramine</span><span class="sxs-lookup"><span data-stu-id="df781-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="df781-104">Elektroonilise aruandluse (ER) rakenduse programmeerimisliidese (API) raamistik võimaldab teil laiendada talletuskohtade loendit ER vormingute loodavatele dokumentidele.</span><span class="sxs-lookup"><span data-stu-id="df781-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="df781-105">See teema sisaldab ülevaadet põhiülesannetest, mille peate kohandatud talletuskoha lisamiseks lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="df781-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df781-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="df781-106">Prerequisites</span></span>

<span data-ttu-id="df781-107">Peate juurutama topoloogia, mis toetab pidevat järku.</span><span class="sxs-lookup"><span data-stu-id="df781-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="df781-108">(Lisateavet vt jaotisest [Pideva järgu ja testimise automaatikat toetavate topoloogiate juurutamine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Teil peab sellele topoloogiale olema juurdepääs ühe järgmise rolli jaoks:</span><span class="sxs-lookup"><span data-stu-id="df781-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="df781-109">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="df781-109">Electronic reporting developer</span></span>
- <span data-ttu-id="df781-110">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="df781-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="df781-111">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="df781-111">System administrator</span></span>

<span data-ttu-id="df781-112">Samuti peab teil selle topoloogia puhul olema juurdepääs arenduskeskkonnale.</span><span class="sxs-lookup"><span data-stu-id="df781-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="df781-113">Elektroonilise aruandluse vormingu konfiguratsiooni loomine või importimine</span><span class="sxs-lookup"><span data-stu-id="df781-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="df781-114">Dokumentide loomiseks, mille jaoks plaanite lisada kohandatud talletuskoha, looge praeguses topoloogias [uus elektroonilise aruandluse vorming](tasks/er-format-configuration-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="df781-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="df781-115">Teise võimalusena [importige olemasolev elektroonilise aruandluse vorming sellesse topoloogiasse](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="df781-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Vormingu koostaja leht](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="df781-117">Loodav või imporditav elektroonilise aruandluse vorming peab sisaldama vähemalt ühte järgmist vorminguelementi.</span><span class="sxs-lookup"><span data-stu-id="df781-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="df781-118">Fail</span><span class="sxs-lookup"><span data-stu-id="df781-118">File</span></span>
> - <span data-ttu-id="df781-119">Kaust</span><span class="sxs-lookup"><span data-stu-id="df781-119">Folder</span></span>
> - <span data-ttu-id="df781-120">Ühinemine</span><span class="sxs-lookup"><span data-stu-id="df781-120">Merger</span></span>
> - <span data-ttu-id="df781-121">Manus</span><span class="sxs-lookup"><span data-stu-id="df781-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="df781-122">Uue dokumenditüübi loomine</span><span class="sxs-lookup"><span data-stu-id="df781-122">Create a new document type</span></span>

<span data-ttu-id="df781-123">Määramaks, kuidas ER-vormingu loodavaid dokumente suunatakse, peate konfigureerima [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="df781-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="df781-124">Peate igas ER-i sihtkohas, mis on konfigureeritud talletama loodud dokumente failidena, määrama dokumendihalduse raamistiku dokumenditüübi.</span><span class="sxs-lookup"><span data-stu-id="df781-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="df781-125">Erinevate ER-i vormingute loodavate dokumentide suunamiseks saab kasutada erinevaid dokumenditüüpe.</span><span class="sxs-lookup"><span data-stu-id="df781-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="df781-126">Lisage varem loodud või imporditud ER-i vormingule uus [dokumenditüüp](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management).</span><span class="sxs-lookup"><span data-stu-id="df781-126">Add a new [document type](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="df781-127">Järgneval joonisel on dokumenditüübiks **FileX**.</span><span class="sxs-lookup"><span data-stu-id="df781-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="df781-128">Selle dokumenditüübi teistest dokumenditüüpidest eristamiseks lisage selle nimesse konkreetne märksõna.</span><span class="sxs-lookup"><span data-stu-id="df781-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="df781-129">Järgneval joonisel on nimeks näiteks **(KOHALIK) kaust**.</span><span class="sxs-lookup"><span data-stu-id="df781-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="df781-130">Määrake väljal **Klass** suvand **Lisa fail**.</span><span class="sxs-lookup"><span data-stu-id="df781-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="df781-131">Määrake väljal **Grupp** suvand **Fail**.</span><span class="sxs-lookup"><span data-stu-id="df781-131">In the **Group** field, specify **File**.</span></span>

![Dokumenditüüpide leht](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="df781-133">Dokumenditüübid on ettevõttekohased.</span><span class="sxs-lookup"><span data-stu-id="df781-133">Document types are company-specific.</span></span> <span data-ttu-id="df781-134">ER-i vormingu kasutamiseks mitmes ettevõttes konfigureeritud sihtkohaga peate igas ettevõttes konfigureerima eraldi dokumendi tüübi.</span><span class="sxs-lookup"><span data-stu-id="df781-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="df781-135">Lähtekoodi ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="df781-135">Review source code</span></span>

<span data-ttu-id="df781-136">Vaadake üle klassi **ERDocuManagement** meetodi **insertFile()** kood.</span><span class="sxs-lookup"><span data-stu-id="df781-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="df781-137">Pange tähele, et sündmus **AttachingFile()** tõstatatakse, kui loodud fail manustatakse kirjele.</span><span class="sxs-lookup"><span data-stu-id="df781-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="df781-138">Sündmus **AttachingFile()** tõstatatakse järgmiste ER-i sihtkohtade töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="df781-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="df781-139">**Arhiiv** – selle sihtkoha kasutamisel luuakse tabelis ERFormatMappingRunJobTable käitatava ER-i vormingu jaoks uus kirje.</span><span class="sxs-lookup"><span data-stu-id="df781-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="df781-140">Selle kirje väli **Arhiivitud** on määratud väärtusele **Väär**.</span><span class="sxs-lookup"><span data-stu-id="df781-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="df781-141">Kui ER-i vormingu käitamine õnnestub, manustatakse loodud dokument sellele kirjele ja tõstatatakse sündmus **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="df781-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="df781-142">Selles ER-i sihtkohas valitud dokumenditüüp määrab manuses oleva faili (Microsoft Azure’i mälu või Microsoft SharePointi kaust) talletuskoha.</span><span class="sxs-lookup"><span data-stu-id="df781-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="df781-143">**Töö arhiiv** – selle sihtkoha kasutamisel luuakse tabelis ERFormatMappingRunJobTable käitatava ER-i vormi jaoks uus kirje.</span><span class="sxs-lookup"><span data-stu-id="df781-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="df781-144">Selle kirje väli **Arhiivitud** on määratud väärtusele **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="df781-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="df781-145">Kui ER-i vormingu käitamine õnnestub, manustatakse loodud dokument sellele kirjele ja tõstatatakse sündmus **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="df781-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="df781-146">ER-i parameetrites konfigureeritud dokumenditüüp määrab manuses oleva faili (Azure’i mälu või  SharePointi kaust) talletuskoha.</span><span class="sxs-lookup"><span data-stu-id="df781-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Elektroonilise aruandluse parameetrite leht](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="df781-148">Elektroonilise aruandluse sihtkoha konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="df781-148">Configure an ER destination</span></span>

1. <span data-ttu-id="df781-149">Arhiivitud sihtkoha konfigureerimine ühele teie loodud või imporditud ER-i vormingu eelnevalt mainitud elemendile (fail, kaust, ühinemine või manus).</span><span class="sxs-lookup"><span data-stu-id="df781-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="df781-150">Juhendit vt teemast [ER-i sihtkohtade konfigureerimine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="df781-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="df781-151">Kasutage dokumendi tüüpi, mille konfigureeritud sihtkoha jaoks varem lisasite.</span><span class="sxs-lookup"><span data-stu-id="df781-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="df781-152">(Selles teemas on dokumenditüübiks näiteks **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="df781-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialoogiboks Sihtkoha sätted](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="df781-154">Lähtekoodi muutmine</span><span class="sxs-lookup"><span data-stu-id="df781-154">Modify source code</span></span>

1. <span data-ttu-id="df781-155">Lisage oma Microsoft Visual Studio projektile uus klass ja kirjutage kood, et tellida eelnevalt mainitud sündmus **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="df781-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="df781-156">(Lisateavet kasutatava laiendatavusmustri kohta vt jaotisest [Vastamine üksuse EventHandlerResult abil](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Kirjutage nt uues klassis kood, mis teeb järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="df781-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="df781-157">Talletage loodud failid selle serveri kohaliku failisüsteemi kaustas, kus töötab teenus rakendusobjekti server (AOS).</span><span class="sxs-lookup"><span data-stu-id="df781-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="df781-158">Talletage need loodud failid ainult juhul, kui faili manustamisel ER-i käitamise töölogi kirjele kasutatakse uut dokumendi tüüpi (nt tüüp **FileX** mille nimes on märksõna „(KOHALIK)”)).</span><span class="sxs-lookup"><span data-stu-id="df781-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="df781-159">Looge oma projekt uuesti.</span><span class="sxs-lookup"><span data-stu-id="df781-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="df781-160">Käivitage ER-i vorming, mille lõite või importisite</span><span class="sxs-lookup"><span data-stu-id="df781-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="df781-161">Täitke ER-i vorming, mille lõite või importisite.</span><span class="sxs-lookup"><span data-stu-id="df781-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="df781-162">Avage **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Elektroonilise aruandluse tööd**.</span><span class="sxs-lookup"><span data-stu-id="df781-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="df781-163">Leidke kirje, mis loodi selle käivitamistöö jaoks ja millele on manustatud loodud fail.</span><span class="sxs-lookup"><span data-stu-id="df781-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="df781-164">Uurige kohalikku **C:\\0** kausta, et leida sama loodud fail.</span><span class="sxs-lookup"><span data-stu-id="df781-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df781-165">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="df781-165">Additional resources</span></span>

- [<span data-ttu-id="df781-166">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="df781-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="df781-167">Laiendatavuse avaleht</span><span class="sxs-lookup"><span data-stu-id="df781-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
