---
title: Microsoft Power Apps portaalide kasutamine osapoole andmemudeliga
description: See teema kirjeldab muudatusi Microsoft Power Apps portaalide veebirollides osapoole andmemudeli topeltkirjutuse tõttu.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 872b477ae73a374cd62b9e86048bfc27c84064c1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781364"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Microsoft Power Apps portaalide kasutamine osapoole andmemudeliga

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Topeltkirjutusega rakenduse orkestratsioonilahenduse versioon 2.0.999.0 ja uuem sisaldab andmemudeli muudatusi osapoole ja globaalse aadressiraamatu konto- ja kontaktitabelite kohta. Muudatused võimaldavad mitu-mitmele-seoseid, mis toetavad laiendatud äristsenaariume. Neid muudatusi ei toeta portaali veebirollid, sealhulgas kliendiportaal, mis on tarnitud valmislahendustena või mis oli teie keskkonnas olemas enne topeltkirjutuse installimist. Selleks, et veebirollid töötaks nii nagu oodatud, peate looma uued veebirollid, kasutades uut andmemudelit. 

Kokkuvõttes on tabelite omavaheline suhtlus muutunud, kuid tabeliõigused kliendiportaalis pole muutunud. See teema kirjeldab, kuidas luua uusi veebirolle, mis töötavad uue täiustatud andmemudeliga.

Diagramm näitab tabeliseost **ilma** osapooleta ja globaalse aadressiraamatu andmemudelita.

   ![osapoolemudelita.](media/without-party-model.PNG)

Diagramm näitab tabeliseost **koos** osapoole ja globaalse aadressiraamatu andmemudeliga.

   ![osapoolemudeliga.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Loo uue tabeli luba

Nende uute tabeli lubade loomiseks järgige neid samme.

1. Logige sisse [Power Apps](https://make.powerapps.com) ja minge oma rakendustesse.
2. Valige oma portaalihalduse rakendus.
3. Valige külgribal **Turvalisuse > Tabeliõigused**.

    Peate looma kolm uut luba.

    + **Kontakt** ja **Osapoole** tabelite ühendus
    + **Osapoole** ja **Konto** tabelite ühendus
    + **Konto** ja **Tellimus** tabelite ühendus

4. Looge ja salvestage luba Kontakti ja Osapoole vahel ühenduse loomiseks, häälestades need parameetrid.

    + **Nimi**: **Osapool** ja **Konto** tabeli ühendus (või teie valik)
    + **Tabeli nimi**: msdyn_contactforparty
    + **Veebisait**: kliendiportaal
    + **Ulatus**: Kontakt
    + **Privileegid**: vali kõik
    + **Veebirollid**: autenditud kasutajad, kliendi esindaja (või teie valik)

5. Looge ja salvestage luba Osapoole ja Konto vahel ühenduse loomiseks, häälestades need parameetrid.

    + **Nimi**: ühenduse loomine Osapoole ja Konto vahel (või teie valik)
    + **Tabeli nimi**: konto
    + **Veebisait**: kliendiportaal
    + **Ulatus**: vanem
    + **Privileegid**: vali kõik
    + **Ematabeli luba**: ühendus Konto ja Osapoole vahel

6. Looge ja salvestage luba Konto ja Tellimuse vahel ühenduse loomiseks, häälestades need parameetrid.

    + **Nimi**: ühenduse loomine Konto ja Tellimuse vahel (või teie valik)
    + **Tabeli nimi**: müügitellimus
    + **Veebisait**: kliendiportaal
    + **Ulatus**: vanem
    + **Privileegid**: vali kõik
    + **Ematabeli luba**: ühendus Osapoole ja Konto vahel

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
