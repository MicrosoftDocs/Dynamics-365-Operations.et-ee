---
title: Lao konfiguratsiooni ülevaade
description: Selles artiklis selgitatakse, kuidas konfigureerida ladu. See sisaldab teavet selle kohta, kuidas lubada lao paigutust ja laoprotsesse.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8cd436f1b8324335cc39ce54344db834dddebc9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426120"
---
# <a name="warehouse-configuration-overview"></a>Lao konfiguratsiooni ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas konfigureerida ladu. See sisaldab teavet selle kohta, kuidas lubada lao paigutust ja laoprotsesse.

> [!NOTE]
> See artikkel kehtib mooduli **Laohaldus** funktsioonidele (täpsem ladustamine). See ei kehti ladustamisfunktsioonidele moodulis **Laohaldus**.

## <a name="warehouse-layout"></a>Lao paigutus
Laohalduse süsteem rakenduses Supply Chain Management pakub paindlikke võimalusi lao paigutuse määratlemiseks, et rahuldada muutuvaid vajadusi, nii et saavutaksite optimaalse lao tõhususe.

-   Saate luua ja kõrge prioriteediga ja madal prioriteediga hoiustamisalasid kaupade optimaalseks paigutamiseks.
-   Saate jagada oma lao tsoonideks, et rahuldada mitmesuguseid ladustamisvajadusi, näiteks temperatuurinõudeid või mitmesuguseid kaubakäibe kiirusi.
-   Saate määrata lao asukohad igal tasandil (näiteks laoala, ladu, riiulirida, sektsioon, riiul ja alusekoht).
-   Saate rühmitada asukohti, kasutades füüsilise mahu piirangu sätteid.
-   Saate kaupade ladustamise ja komplekteerimise viisi juhtida, tuginedes päringuga määratud reeglitele.

Rakenduses Supply Chain Management laohalduse kasutamiseks peate looma lao ja lubama selle täpsema või spetsiaalse laohalduse tegevuste jaoks. Tehke lehel **Laod** valik **Kasuta laohaldusprotsesse**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Tsoonigrupid, tsoonid, asukohatüübid ja asukohad

Laopaigutuse lubamise protsessi raames tuleb määratleda laotsoonide grupid ja tsoonid, asukohaprofiilid, asukohatüübid ja asukohad.

-   **Tsoonigrupid** – tsoonide füüsiline või loogiline grupeering laos.
-   **Tsoonid** – asukohtade füüsiline või loogiline grupeering laos.
-   **Asukohaprofiilid** – samade lao asukoha protsessi poliitikatega asukohtade loogiline või füüsiline grupeering (näiteks saab seal ladustada erinevate kaubakoodide segu ja kehtivad samad füüsilise mahu piirangud).
-   **Asukohatüübid** – laoasukohtade füüsiline või loogiline grupeering. Näiteks saate luua asukohatüüp ajastamise kõigi asukohtade jaoks. Lehe **Laohalduse parameetrid** kohustuslikud sätted juhivad vaheasukoha tüüpide ja lõppsihtkoha määratlemise protsessi.
-   **Asukohad** – asukohateabe madalaim tase. Asukohti kasutatakse jälgimiseks, kus vaba kaubavaru laos ladustatakse ja komplekteeritakse.

Laopaigutuse määratlemiseks loodavaid üksusi kasutatakse töömallidel seadistatavates päringutes lao töötellimuste juhtimiseks. Seetõttu arvestage tsoonide, asukohatüüpide jne määratlemisel, kuidas lao erinevaid alasid erinevate protsesside jaoks kasutatakse. Lisaks arvestage selliseid tegureid nagu konkreetse ala füüsilised omadused. Näiteks võib olla alasid, kus saate kasutada ainult teatud tüüpi kahveltõstukit. Või kui teie ettevõttel on samas rajatises nii tootmis- kui ka lõpetatud tooted, võite soovi korral luua rakenduses Supply Chain Management ühe lao, kuid seejärel eraldada need kaks toimingut, luues kaks tsoonigruppi. Andke oma üksustele kirjeldavad nimed, et neid oleks lihtne tuvastada, kui kasutate neid mallpäringutes.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Asukoha ladustamispiirangud, asukohaprofiilid ja fikseeritud komplekteerimiskohad

Peate arvestama lao füüsilist paigutust nii ladustamismahu (asukoha ladustamispiirangute ja asukohaprofiilide) määratlemiseks kui ka optimaalsete laoprotsesside saavutamiseks. 

Asukoha ladustamispiirangud aitavad tagada, et tööd ei looda taotlemaks varude asetamist asukohta, millel pole varude vedamiseks sobivat füüsilist jõudlust. Kui mõned asukohad laos saavad hoida ainult üht kaubaalust asukoha kohta, saab asukoha ladustamispiirangud lubada. Väärtuseks **Kogus** võib määrata **1** ja **Ühiku** väärtuseks saab konkreetses asukohaprofiili grupeeringus määrata **PL** . 

Kui asukoha mahupiirangute juhtimiseks on vaja keerukamaid arvutusi, võib kasutada asukohaprofiili sätteid. Sel juhul arvestatakse mahu arvutustes kaalu ja mahtu. 

Optimaalsete lähetustoimingute saavutamiseks tuleks hinnata, kas kasutada fikseeritud komplekteerimiskohti ja/või pakkimiskohti. Sageli kasutatakse täiendusprotsessides hulgialalt fikseeritud komplekteerimiskohta minimaalset/maksimaalset täiendamist ja samas laos ning tootevariantide puhul saab lubada mitu fikseeritud komplekteerimiskohta. Mõelge paindlikkusele, mille võite saavutada, kui lubate spetsiaalse nõudluse täiendamise ületäitumise asukohad, mida kasutatakse ainult voo/koorma täiendamise töötlemisel.

### <a name="location-setup-wizard"></a>Asukoha häälestuse viisard

Laos kiireks asukohtade loomiseks võite kasutada viisardit **Asukoha seadistus**. Selle protsessi käigus saate hõlpsasti asukohanimede vormingut hallata.

## <a name="warehouse-processes"></a>Laoprotsessid
Lao konfiguratsiooni osana on oluline lubada laoprotsessid vastavalt ettevõtte vajadustele. Kõige olulisemad komponendid, mis tuleb seadistada, on voomallid, töömallid, töökaustad ja asukohakorraldused.

### <a name="wave-templates"></a>Voomallid

Voomallid aitavad lubada väljaminevat lattu väljastamise protsessi. Kui tellimuse read on väljastatud (kas otse lähtedokumentidest, pakett-töö protsesside või juba loodud koormate kaudu), kasutatakse voomalli funktsiooni. 

Saate luua kolme tüüpi voomalle. 
-   **Lähetamine**
-   **Tootmistellimus**
-   **Kanban** 

Parameetreid kasutatakse määratlemiseks, kui kaugele peaks süsteem automaatselt väljamineva töö töötlemisel minema. Voomall valitakse voomallide seeria ja mallis määratud kriteeriumide alusel. Kui mall on seeria ülaosas, kontrollitakse kõigepealt selle malli kriteeriume. Kui kriteeriumid saab täita, töödeldakse voomall. Vastasel korral kontrollitakse järgmise malli kriteeriume jne. Seetõttu on soovitatav panna kõige konkreetsemate kriteeriumidega mall voomallide seeria loendi etteotsa, et seda töödeldaks esimesena. Näiteks soovite töödelda täna kogu konkreetse vedaja tööd ja viivitada ajutiselt teiste vedajate töötlemisega. Sel juhul tuleks sellele vedajale tööd valiv voomall paigutada seerias teistest mallidest kõrgemale. Vastasel korral võidakse muude vedajate töö töödelda enne, kui selle vedaja tööga lõpule jõutakse. 

Peate määrama voo töötlemise meetodid igas voomallis. Saadaolevad meetodid on erinevad, olenevalt voomalli tüübist.

### <a name="work-templates"></a>Töömallid

Töömalli definitsioonidel on laohalduse tööprotsesside määratlemisel oluline roll. Need määratlevad, millist tööd ja kuidas tehakse. Mallid võivad sisaldada ka korralduse koodi, mis on seotud asukohakorraldusega töö tegemise koha määratlemiseks. Töömallid sisaldavad päringut, mis määrab töö kriteeriumid. Iga mall peab sisaldama vähemalt ühte valimistoimingut ja ühte paigutamistoimingut, et juhtida põhilist tööoperatsiooni, kus vaba kaubavaru viiakse ühest kohast teise. 

Kui mõne laotoimingu puhul peab saama tööd töödelda mitu töötajat, võib olla vaja kasutada varude puhul mõistet *ajastamine* ja eraldada töö läbiviimine erinevatesse tööklassidesse.

### <a name="work-pools"></a>Töökaustad

Töö korraldamiseks gruppidesse kasutatakse töökaustu. Näiteks saate luua töökausta teatud laoasukohas toimuva töö klassifitseerimiseks. Kõigi töö tüüpide puhul, v.a inventuur, saate määrata töömallile töökausta. Tsükliliseks inventuuriks saate määrata töökausta järgmistel lehtedel.

-   Tsüklilise inventuuri plaanid
-   Tsüklilise inventuuri läved
-   Tsükli loenduse töö asukoha alusel
-   Tsükli loenduse töö kauba alusel

Töö loomisel töömallide kasutamisel määratakse tööle automaatselt töökaust. 

Töökausta ID-sid saab kasutada ka konkreetsele laotöötajale suunatud töö tüübi piiramiseks, eeldusel, et see funktsioon on vastava mobiilse seadme menüüelemendis konfigureeritud.

### <a name="location-directives"></a>Asukoha korraldus

Nagu nimigi viitab, kasutatakse asukohakorraldusi töökannete suunamiseks sobivatesse asukohtadesse laos. Teisisõnu: need määratlevad, kust valida ja kuhu paigutada. 

Iga asukohakorralduse reaga seotud toimingute hõlpsamaks ja kiriemaks määratlemiseks võib kasutada ühte eelnevalt määratud strateegiat. Näiteks võite kasutada strateegiat **Tühi asukoht sissetuleva tööta** vabade kohtade otsimiseks laost või strateegiat **FEFO partii reserveerimine** väljamineva müügi komplekteerimiseks.

<a name="additional-resources"></a>Lisaressursid
--------

[Asukohtade konfigureerimine WMS-loaga laos](tasks/configure-locations-wms-enabled-warehouse.md)



