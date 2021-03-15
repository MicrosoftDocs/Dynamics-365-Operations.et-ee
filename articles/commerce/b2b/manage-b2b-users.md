---
title: Äripartnerist kasutajate haldamine B2B e-kaubanduse veebisaitidel
description: Selles teemas kirjeldatakse, kuidas administraatorid saavad lisada, redigeerida ja kustutada äripartnerist kasutajaid ettevõtetevahelistel (B2B) e-kaubanduse veebisaitidel.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96b76a08206b8c1bc5029acdfd385fda2870ca85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035898"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Äripartnerist kasutajate haldamine B2B e-kaubanduse veebisaitidel

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas administraatorid saavad lisada, redigeerida ja kustutada äripartnerist kasutajaid ettevõtetevahelistel (B2B) e-kaubanduse veebisaitidel.

B2B e-kaubanduse veebisaidid nõuavad, et organisatsioonide äripartneriks saamiseks registreeruksid. Kui organisatsioon on B2B e-kaubanduse veebisaidile registreerimisandmed esitanud, läbib see kvalifikatsiooniprotsessi. Kui organisatsioon on edukalt kvalifitseeritud, võetakse see äripartnerina vastu.

Kui organisatsioon on äripartneriks võetud, määratakse administraatoriks organisatsiooni see kasutaja, kes algatas äripartneriks saamise, ja talle antakse õigus liita B2B e-kaubanduse veebisaidile täiendavaid volitatud kasutajaid. Need volitatud kasutajad saavad seejärel esitada tellimusi äripartneri nimel.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>B2B e-kaubanduse võimaluse funktsiooni sisselülitamine Commerce'i peakontoris

Commerce'i peakontori B2B e-kaubanduse võimaluste funktsioon võimaldab võtta vastu äripartnereid ja määrata administraatorkasutajaid. See funktsioon võimaldab administraatoritel ka luua ja hallata äripartneri kasutajaid ja meeskondi ning määrata neile kindlaid rolle. Lõpuks võimaldab see äripartnerist kasutajatel luua tellimuse malle ja kasutada olemasolevaid tellimusi toodete uuesti tellimiseks.

B2B e-kaubanduse võimaluse funktsiooni sisselülitamiseks Commerce'i peakontoris toimige järgmiselt.

1. Avage **Tööruumid \> Funktsioonihaldus**.
1. Filtreerige vahekaardil **Kõik** väljal **Moodul** termini **Jaemüük ja kaubandus** järgi.
1. Leidke ja valige funktsioon nimega **Luba B2B e-kaubanduse võimaluste kasutamine** ja seejärel valige **Luga kohe**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Looge numbriseeria ja lisage see Commerce'i ühisparameetritele

Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid. Numbriseeriate kohta leiate lisateavet teemast [Numbriseeriate ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Numbriseeria loomiseks ja Commerce'i ühisparameetritele lisamiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Peakontori seadistus \> Numbriseeriad \> Numbriseeriad** ja looge numbriseeria.
1. Avage **Jaemüük ja kaubandus \> Peakontori seadistus \> Parameetrid \> Commerce'i ühisparameetrid** ja lisage uus numbriseerija viitele **Kliendi hierarhia ID**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Administraatorkasutajate seadistamine uue äripartneri jaoks

Potentsiaalsed äripartnerid saavad käivitada B2B e-kaubanduse veebisaidiga liitumise protsessi esitades liitumistaotluse läbi saidil oleva lingi. Pärast seda, kui potentsiaalne äripartnerist kasutaja valib lingi, saab ta esitada üksikasjad, mis on liitumise ja registreerumise jaoks nõutavad. Pärast taotluse esitamist kuvatakse esitamise kinnituse leht. Kui esildis kinnitatakse, saab taotlejast (st kasutajast, kes algatas liitumistaotluse) äripartneri administraatorkasutaja.

Äripartneri administraatorkasutaja kinnitamiseks ja häälestamiseks Commerce'i peakontoris toimige järgmiselt.

1. Avage **Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käivitage töö **P-0001**, et tõmmata kõik äripartnerite liitumistaotlused Commerce'i peakontorisse.
1. Pärast töö **P-0001** edukat käitamist avage **Jaemüügi ja kaubanduse IT \> Klient** ja käivitage töö **Sünkrooni kliendid ja äripartnerid asünkroonsest režiimist**. Kui see töö on edukalt käitatud, luuakse Commerce'i peakontoris liitumistaotlused potentsiaalsete klientide kirjetena. Nende kirjete väli **Tüübi ID** on seadistatud olekusse **Potentsiaalne B2B klient**.
1. Avage **Kliendid \> Kõik potentsiaalsed kliendid** ja avage potenstiaalsete klientide leht.
1. Valige uue äripartneri potentsiaalse kliendi kirje, et avada potentsiaalse kliendi üksikasjade leht.
1. Valige vahekaardil **Üldine** jaotis **Teisendamine \> Kinnitamine/Tagasilükkamine**, et liitumistaotlus kas kinnitada või tagasi lükata. Kui kuvatakse kinnitusteade, kinnitage, et soovite protsessiga jätkata ja taotluse kinnitada. Seejärel saadetakse taotleja meiliaadressile meil kinnitamaks, et tema organisatsioon on äripartnerina kinnitatud.

    Pärast taotluse kinnitamist määratakse potentsiaalse kliendi väli **Olek** väärtuseks **Kinnitatud**. Lisaks luuakse süsteemis kaks uut kliendikirjet: kliendikirje **Tüüp Organisatsioon** äripartneri organisatsioonile ja kliendikirje **Tüüp Isik** taotlejale. Samuti luuakse äripartnerile kliendi hierarhia kirje. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Avage **Jaemüügi ja kaubanduse IT \> Jaotusgraafik** ja käivitage töö **1010** (**Kliendid**), et suunata vastloodud kliendi ja kliendi hierarhia kirjed kanali andmebaasi.

Kui taotlus on kinnitatud ja kliendi ning kliendi hierarhia kirjed on sünkroonitud kanali andmebaasi, saab taotleja B2B e-kaubanduse veebisaidile sisse logida, kasutades taotlust esitades antud meiliaadressi. Kasutajad saavad kasutada registreerumisvoogu oma kontole parooli määratlemiseks.

## <a name="onboard-additional-business-partner-users"></a>Täiendavate äripartneri kasutajate liitmine

Äripartneri administraatorkasutaja saab vajadusel B2B e-kaubanduse veebisaidile lisada täiendavaid äripartneri kasutajaid.

B2B e-kaubanduse veebisaidile äripartnerite lisamiseks toimige järgmiselt.

1. Logige B2B e-kaubanduse veebisaidile administraatorina sisse.
1. Avage **Minu konto \> Organisatsiooni kasutajad \> Vaata üksikasju** ja valige **Lisa kasutaja**.
1. Sisestage nõutud teave ja seejärel valige **Salvesta**. Uue kasutaja olekuks seadistatakse **Ootel**.

    Pärast tööde **P-0001** ja **Sünkrooni kliendid ja äripartnerid asünkroonsest režiimist** käitamist luuakse Commerce'i peakontoris uuele kasutajale kliendikirje **Tüüp Isik**. See kliendikirje on seotud ka vastava äripartnerist kliendi hierarhia kirjega. Lisaks saadetakse e-kiri uue kasutaja meiliaadressile, et teavitada teda äripartneri organisatsiooni kasutajaks lisamisest ja sellest, et ta saab nüüd B2B e-kaubanduse veebisaidile sisse logida.

1. Käivitage töö **1010** (**Kliendid**), et sünkroonida uued äripartneri kasutajad kanali andmebaasiga.

Kui kliendikirje on sünkroonitud, määratakse kasutaja olekuks B2B e-kaubanduse veebisaidil **Aktiivne** ja uus kasutaja saab B2B e-kaubanduse veebisaidile oma meiliaadressi kasutades sisse logida. Kasutajad saavad kasutada registreerumisvoogu oma kontole parooli määratlemiseks.

## <a name="edit-business-partner-user-details"></a>Äripartneri kasutaja üksikasjade redigeerimine

Äripartneri kasutajate üksikasjade redigeerimiseks järgige neid samme.

1. Logige B2B e-kaubanduse veebisaidile administraatorina sisse.
1. Avage **Minu konto \> Organisatsiooni kasutajad \> Kuva üksikasjad** valige nupp **Redigeeri** (pliiatsi sümbol), tehke vajalikud muudatused ja seejärel valige nupp **Salvesta**. Muudatused jõustuvad alles pärast seda, kui tööd **P-0001**, **Sünkrooni kliendid ja äripartnerid asünkroonsest režiimist** ja **1010** (**Kliendid**) on käitatud.

## <a name="remove-a-business-partner-user"></a>Äripartneri kasutaja eemaldamine

Administraator saab vajadusel eemaldada äripartneri organisatsiooni olemasoleva kasutajad nende kasutajate loendist, kellel on juurdepääs B2B e-kaubanduse veebisaidile.

Äripartneri kasutaja eemaldamiseks toimige järgmiselt.

1. Logige B2B e-kaubanduse veebisaidile administraatorina sisse.
1. Avage **Minu konto \> Organisatsiooni kasutajad \> Vaata üksikasju** ja valige nupp **Eemalda** ("X" sümbol). Kui kuvatakse kinnitusteade, kinnitage, et soovite kasutaja eemaldada. Muudatused jõustuvad alles pärast seda, kui tööd **P-0001**, **Sünkrooni kliendid ja äripartnerid asünkroonsest režiimist** ja **1010** (**Kliendid**) on käitatud.

> [!NOTE]
> Kui eemaldate kasutaja B2B e-kaubanduse veebisaidile juurdepääsu omavate kasutajate hulgast, eemaldatakse vastav kasutajakirje äripartneri kliendi hierarhia kirjest. Kuid kliendikirjet ennast Commerce'i peakontorist ei kustutata.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Äripartneri ja kasutajate vastuvõtmine Commerce'i peakontoris

Administraatorid saavad äripartnereid ja kasutajaid otse Commerce'i peakontorist vastu võtta.

Äripartnerite ja kasutajate vastuvõtmiseks Commerce'i peakontorist toimige järgmiselt.

1. Looge äripartneri organisatsioonile kliendikirje **Tüüp Organisatsioon**.
1. Looge äripartneri kasutajatele kliendikirjed **Tüüp Isik**. Veenduge, et igale kliendile oleks määratud esmane meiliaadress.
1. Iga kliendikirje **Tüüp Isik** kohta, kes tuleb määrata äripartneri organisatsiooni administraatoriks, määrake kiirkaardil **Jaemüük** suvand **B2B administraator** olekusse **Jah**.
1. Looge kliendi hierarhia ID. Väljale **Nimi** sisestage nimi.
1. Sisestage väljale **Organisatsioon** äripartnerist organisatsiooni klient.
1. Valige **Lisa** ja seejärel valige klient väljalt **Nimi**.
1. Korrake seda protsessi, et lisada hierarhiasse täiendavaid kliente.

## <a name="additional-information"></a>Lisateave

- Kõiki selles teemas mainitud töid saab konfigureerida graafikus käivituma partiivormingus. Eeldatakse, et äripartnerid konfigureerivad pakett-töid vastavalt vajadusele.
- Praegu saab adiminstraatorkasutajaks määrata ainult ühe kasutaja/kliendi kirje ja seda rolli saab muuta ainult Commerce'i peakontoris. Puudub tugi iseteeninduse võimalustele, mis laseksid äripartneritel määrata mitut administraatorit või muuta B2B e-kaubanduse veebisaitidel adiminstraatoreid.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Kuigi kasutajatele saab määrata kulutamise piiranguid, ei ole kulutamise piirangute jõustamist tellimuse sisestamise protsessis veel rakendatud.
- Kogu kasutajakogemuse äriloogika ja valideerimine B2B e-kaubanduse veebisaidil põhineb kasutajale Commerce'i peakontoris vastendatud kliendikirje konfiguratsioonil.

## <a name="additional-resources"></a>Lisaressursid

[B2B e-kaubanduse saidi seadistamine](set-up-b2b-site.md)

[B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.](org-model.md)

[Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks](payment-method.md)

[Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks](quantity-limits.md)

[Numbriseeriate ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]