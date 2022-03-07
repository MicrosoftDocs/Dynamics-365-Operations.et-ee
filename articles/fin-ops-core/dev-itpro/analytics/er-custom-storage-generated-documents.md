---
title: Loodud dokumentidele kohandatud talletuskoha määramine
description: Selles teemas selgitatakse, kuidas laiendada talletuskohtade loendit dokumentidele, mille loovad elektroonilise aruandluse (ER) vormingud.
author: NickSelin
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 61a1e46497d650e2c063a5fe7537d17cf7aa1828a5a4504bb781e84aeb88f04a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718497"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Loodud dokumentidele kohandatud talletuskoha määramine

[!include[banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) rakenduse programmeerimisliidese (API) raamistik võimaldab teil laiendada talletuskohtade loendit ER vormingute loodavatele dokumentidele. See teema sisaldab ülevaadet põhiülesannetest, mille peate kohandatud talletuskoha lisamiseks lõpule viima.

## <a name="prerequisites"></a>Eeltingimused

Peate juurutama topoloogia, mis toetab pidevat järku. (Lisateavet vt jaotisest [Pideva järgu ja testimise automaatikat toetavate topoloogiate juurutamine](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Teil peab sellele topoloogiale olema juurdepääs ühe järgmise rolli jaoks:

- Elektroonilise aruandluse arendaja
- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Samuti peab teil selle topoloogia puhul olema juurdepääs arenduskeskkonnale.

## <a name="create-or-import-an-er-format-configuration"></a>Elektroonilise aruandluse vormingu konfiguratsiooni loomine või importimine

Dokumentide loomiseks, mille jaoks plaanite lisada kohandatud talletuskoha, looge praeguses topoloogias [uus elektroonilise aruandluse vorming](tasks/er-format-configuration-2016-11.md). Teise võimalusena [importige olemasolev elektroonilise aruandluse vorming sellesse topoloogiasse](general-electronic-reporting-manage-configuration-lifecycle.md).

![Vormingukujundaja leht.](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Loodav või imporditav elektroonilise aruandluse vorming peab sisaldama vähemalt ühte järgmist vorminguelementi.
>
> - Fail
> - Kaust
> - Ühinemine
> - Manus

## <a name="create-a-new-document-type"></a>Uue dokumenditüübi loomine

Määramaks, kuidas ER-vormingu loodavaid dokumente suunatakse, peate konfigureerima [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md). Peate igas ER-i sihtkohas, mis on konfigureeritud talletama loodud dokumente failidena, määrama dokumendihalduse raamistiku dokumenditüübi. Erinevate ER-i vormingute loodavate dokumentide suunamiseks saab kasutada erinevaid dokumenditüüpe.

1. Lisage varem loodud või imporditud ER-i vormingule uus [dokumenditüüp](../../fin-ops/organization-administration/configure-document-management.md). Järgneval joonisel on dokumenditüübiks **FileX**.
2. Selle dokumenditüübi teistest dokumenditüüpidest eristamiseks lisage selle nimesse konkreetne märksõna. Järgneval joonisel on nimeks näiteks **(KOHALIK) kaust**.
3. Määrake väljal **Klass** suvand **Lisa fail**.
4. Määrake väljal **Grupp** suvand **Fail**.

![Dokumenditüüpide lehed.](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Dokumenditüübid on ettevõttekohased. ER-i vormingu kasutamiseks mitmes ettevõttes konfigureeritud sihtkohaga peate igas ettevõttes konfigureerima eraldi dokumendi tüübi.

## <a name="review-source-code"></a>Lähtekoodi ülevaatamine

Vaadake üle klassi **ERDocuManagement** meetodi **insertFile()** kood. Pange tähele, et sündmus **AttachingFile()** tõstatatakse, kui loodud fail manustatakse kirjele.


```xpp
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

Sündmus **AttachingFile()** tõstatatakse järgmiste ER-i sihtkohtade töötlemisel.

- **Arhiiv** – selle sihtkoha kasutamisel luuakse tabelis ERFormatMappingRunJobTable käitatava ER-i vormingu jaoks uus kirje. Selle kirje väli **Arhiivitud** on määratud väärtusele **Väär**. Kui ER-i vormingu käitamine õnnestub, manustatakse loodud dokument sellele kirjele ja tõstatatakse sündmus **AttachingFile()**. Selles ER-i sihtkohas valitud dokumenditüüp määrab manuses oleva faili (Microsoft Azure’i mälu või Microsoft SharePointi kaust) talletuskoha.
- **Töö arhiiv** – selle sihtkoha kasutamisel luuakse tabelis ERFormatMappingRunJobTable käitatava ER-i vormi jaoks uus kirje. Selle kirje väli **Arhiivitud** on määratud väärtusele **Tõene**. Kui ER-i vormingu käitamine õnnestub, manustatakse loodud dokument sellele kirjele ja tõstatatakse sündmus **AttachingFile()**. ER-i parameetrites konfigureeritud dokumenditüüp määrab manuses oleva faili (Azure’i mälu või SharePointi kaust) talletuskoha.

![Elektroonilise aruandluse parameetrite leht.](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Elektroonilise aruandluse sihtkoha konfigureerimine

1. Arhiivitud sihtkoha konfigureerimine ühele teie loodud või imporditud ER-i vormingu eelnevalt mainitud elemendile (fail, kaust, ühinemine või manus). Juhendit vt teemast [ER-i sihtkohtade konfigureerimine](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Kasutage dokumendi tüüpi, mille konfigureeritud sihtkoha jaoks varem lisasite. (Selles teemas on dokumenditüübiks näiteks **FileX**.)

![Sihtkoha sätete dialoogiboks.](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Lähtekoodi muutmine

1. Lisage oma Microsoft Visual Studio projektile uus klass ja kirjutage kood, et tellida eelnevalt mainitud sündmus **AttachingFile()**. (Lisateavet kasutatava laiendatavusmustri kohta vt jaotisest [Vastamine üksuse EventHandlerResult abil](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Kirjutage nt uues klassis kood, mis teeb järgmisi toiminguid.

    1. Talletage loodud failid selle serveri kohaliku failisüsteemi kaustas, kus töötab teenus rakendusobjekti server (AOS).
    2. Talletage need loodud failid ainult juhul, kui faili manustamisel ER-i käitamise töölogi kirjele kasutatakse uut dokumendi tüüpi (nt tüüp **FileX** mille nimes on märksõna „(KOHALIK)”).

    ```xpp
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

2. Looge oma projekt uuesti.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Käivitage ER-i vorming, mille lõite või importisite

1. Täitke ER-i vorming, mille lõite või importisite.
2. Avage **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Elektroonilise aruandluse tööd**. Leidke kirje, mis loodi selle käivitamistöö jaoks ja millele on manustatud loodud fail.
3. Uurige kohalikku **C:\\0** kausta, et leida sama loodud fail.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Laiendatavuse avaleht](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]