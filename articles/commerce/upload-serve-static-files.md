---
title: Staatiliste failide üleslaadimine ja kasutamine
description: See artikkel kirjeldab, kuidas Microsoft Dynamics 365 Commerce staatilist faili saidikonstruktorisse üles laadida ja kuidas luua kohandatud URL-i ja faili nime, mida saab faili taotleda.
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8b30150d4187bbb0195bcb23960afe7389d56a5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281935"
---
# <a name="upload-and-serve-static-files"></a>Staatiliste failide üleslaadimine ja kasutamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas Microsoft Dynamics 365 Commerce staatilist faili saidikonstruktorisse üles laadida ja kuidas luua kohandatud URL-i ja faili nime, mida saab faili taotleda.

Mõned kolmanda osapoole konnektorid nõuavad, et fail majutatakse ja serveeritakse e-kaubanduse saidilt. Need konnektorid eeldavad, et fail tagastatakse taotlustega kindlale tagasihelistamise URL-i teele ja failinimele. Seetõttu selgitab see artikkel, kuidas laadida üles ja teenindada staatilist faili, mille kasutaja määratletav URL ja faili nimi on Dynamics 365 Commerce e-äri saidil.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Looge saidi URL, mis tagastab staatilise faili.

Saidi URL-i loomiseks, mis tagastaks staatilise faili e-kaubanduse saidiloojas, toimige järgmiselt.

1. Minge oma saidi meediateeki ja laadige üles fail, mis tuleks kätte toimetada teie määratud URL-i taotlustega. Kui olete faili juba üles laadinud, võite selle sammu vahele jätta.
1. Avage oma saidi **URL-id**.
1. Valige **uus \> Uus URL**.
1. **Uus URL** dialoogiaknas valige **Meediateegi vara**.
1. Sisestage **URL-i tee** väljale URL-i tee. Kaasake teele faili nimi.
1. Valige **Edasi**. Avatakse meediateek ja kuvatakse kõik üleslaetud **dokumendi** tüübi meediumid.
1. Valige fail, mis peaks olema saadaval sammus 5 määratletud URL-i taotluste jaoks.
1. Valige käsk **Salvesta**.

Sel hetkel on teie poolt loodud URL mustandi olekus. Faili, millele URL osutab, ei tagastata enne, kui olete URL-i avaldanud. Enne URL-i avaldamist saate tõendada, et see tagastab õiged andmed.

## <a name="validate-and-publish-a-url"></a>Tõendage ja avaldage URL

URL-i valideerimiseks enne selle avaldamist tehke järgmist.

1. Avage oma saidi **URL-id** ja valige eelvaateks URL.
2. Parempoolsel atribuutide paanil valige **Redigeeri** nupu all olev õige URL-i link. Avatakse uus brauseri aken ja te peaksite saama 404 tõrke.
3. Lisage see **?preview=inprogress** päringu string URL-iks (nt `https://yoursite.com/callback.html?preview=inprogress`) ja laadige leht uuesti. Mediateeki üleslaetud fail tuleks vastuseks tagastada.

Pärast URL-i kontrollimist saate selle avaldada.

1. Avage oma saidi **URL-id** ja valige URL.
2. Valige käsuribal **Avalda**.

## <a name="update-the-file-that-a-url-points-to"></a>Värskendage faili, millele URL osutab

Pärast URL-i avaldamist saate seda värskendada nii, et see osutab mõnele muule failile. Teise võimalusena saate URL-i värskendada nii, et see osutab erinevale ressursitüübile, nagu on kirjeldatud järgmises jaotises. Näiteks saate suunata URL-i sisemisele lehele või ümber suunata.

URL-i osutatud faili värskendamiseks toimige järgmiselt.

1. Avage oma saidi **URL-id** ja valige uuendamiseks URL.
1. Parempoolsel atribuutide paanil valige suvand **Redigeeri**.
1. Jaotises **URL-i määramine** valige **Samm 2** aken ja seejärel valige uus meediateegist dokument.
1. Valige **Rakendamine**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Värskendage varatüüpi, millele URL osutab

Samuti saate värskendada URL-i nii, et see osutab erinevat tüüpi varale (ressurss), nagu sisemine leht või ümbersuunamine.

URL-i osutatud ressursitüübi värskendamiseks toimige järgmiselt.

1. Avage oma saidi **URL-id** ja valige uuendamiseks URL.
1. Parempoolsel atribuutide paanil valige suvand **Redigeeri**.
1. Valige **URL-i määramine** jaotises **Samm 1** ja valige muu ressursitüüp.
1. Valige **Samm 2** aken ja seejärel valige uus ressurss.
1. Valige **Rakendamine**.

## <a name="change-the-url-path"></a>Muuda URL-i teed

Pärast URL-i loomist ei saa selle teed muuta. Kui peate muutma faili või mõnda muud tüüpi ressurssi sisaldavat URL-i teed, peate looma uue URL-i, vastendama selle olemasoleva faili või muu ressursiga ning seejärel tühistama ja kustutama vana URL-i.

URL-i tee muutmiseks tehke järgmist.

1. Uue URL-i loomiseks ja selle vastendamiseks olemasoleva faili või muu ressursiga järgige juhiseid saidi URL-i [loomiseks,](#create-a-site-url-that-returns-a-static-file) mis tagastab selle artikli varasema staatilise faili sektsiooni.
1. Valige uus URL ja valige käsk **Avalda**. Uus URL on avaldatud.
1. Vana URL-i avaldamise tühistamiseks valige see ja seejärel valige käsuribal käsk **Tühista avaldamine**. Soovi korral võite nüüd vana URL-i kustutada.

## <a name="additional-resources"></a>Lisaressursid

[Digitaalse varahalduse ülevaade](dam-overview.md)

[Piltide üleslaadimine](dam-upload-images.md)

[Videote üleslaadimine](dam-upload-video.md)

[Failide üleslaadimine, v. a pildid ja videod](dam-upload-files.md)

[Piltide kärpimine](dam-crop-images.md)

[Pildi keskpunktide kohandamine](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
