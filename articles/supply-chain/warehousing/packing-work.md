---
title: Väljaminevate konteinerite ja saadetiste töötlemise pakketöö
description: See artikkel kirjeldab töötellimuse tüüpi "Pakkimine", mis haldab konteinerite pakkimist ning toetab koormatega seotud pakitud konteinerite osalisi saadetisi, kus lao kaubad jäävad lahti pakimata.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220737"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Väljaminevate konteinerite ja saadetiste töötlemise pakketöö

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab *töötellimuse* tüüpi, mis haldab konteinerite pakendamise tööd ja toetab koormatega seotud pakitud konteinerite osalisi saadetisi, kus lao kaubad jäävad lahti pakkimata. Pakketöö võimaldab kasutada [konteineritega](confirm-and-transfer.md) seotud väljaminevate saadetiste kinnitamiseks kinnitamise ja ülekandmise funktsioone.

Pakkimistöö luuakse automaatselt, kui lähtedokumendi tööga seotud ladu pannakse pakkimisasukoha *tüüpi asukohta*. Töö koosneb kahest reast, üks noppimiseks *ja* teine *panemiseks* ning seda hallatakse automaatselt konteineri sulgemise/taasavamise protsessi osana.

Lisateavet konteinerite pakkimisprotsessi häälestamise ja kasutamise kohta vt saadetise [pakkekonteineritest](packing-containers.md).

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Kui teie süsteem ei kaasa juba selles artiklis kirjeldatud funktsioone, [minge](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Funktsioonihaldusse ja lülitage järgmised funktsioonid sisse järgmises järjekorras. Mõlemad funktsioonid on laohalduse **mooduli osa**.

1. *Kinnitamine ja üleviimine*
1. *Pakkimistöö pakkimisjaamade jaoks*

## <a name="set-up-a-location-for-packing-work"></a>Pakkimistöö asukoha seadistamine

Kasutage pakkimisasukohtade häälestamiseks järgmist protseduuri. Iga asukoha jaoks saate valida, kas süsteem loob pakketöö automaatselt.

1. Minge laohalduse **häälestamise pakkimisjaama \>\>\> häälestusse.**
1. Tegevuspaanil valige uus **,** et lisada pakkimisjaama häälestuse kirje.
1. Seadke uuel kirjel järgmised väljad:

    - **Ladu**: valige või sisestage ladu, kus pakkimise asukoht asub.
    - **Asukoht** : valige või sisestage pakkimisasukoht. See asukoht peab olema määratud asukohaprofiilile, mis kasutab pakkimisasukoha tüübina konfigureeritud **asukoha tüüpi laohalduse parameetrite lehel teie ettevõtte** jaoks. Lisateavet vt saadetise [pakkekonteineritest](packing-containers.md).
    - **Loo pakkimistöö** – märkige see ruut, et luua pakketöö iga kord, kui kaubad tarnitakse pakkimiskohta. Töö sisaldab linke seotud koormaridadele, nii et osalisi koormaid saab pakkida ja saata.

## <a name="example-scenario"></a>Näidisstsenaarium

See näitestsenaarium näitab, kuidas töödelda väljamineva müügitellimuse voogu konteineri pakkimisel ja osalise koormuse saatmisel.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Seda stsenaariumi saate kasutada ka tootmissüsteemis funktsiooni kasutamise juhistena. Sel juhul tuleb teil siiski sisestada oma väärtused iga siin kirjeldatud sätte jaoks.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Pakkimistöö konfigureerimine lao pakkimise asukoha jaoks

Alustamiseks peate konfigureerima pakkimistöö *protsessi* konkreetse lao ja asukoha jaoks.

1. Minge laohalduse **häälestamise pakkimisjaama \>\>\> häälestusse.**
1. Tegevuspaanil valige häälestuskirje **lisamiseks** uus.
1. Seadke uuel kirjel järgmised väärtused:

    - **Ladu:** *62*
    - **Asukoht:** *Pakkimine*
    - **Pakketöö loomine:** *jah*

1. Sulgege pakkimisjaama **häälestuse** leht.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Loo koormamall, mis lubab osalist saatmist

Koorma tarnimist mitme saadetise kohta peate seostama koormamalliga, mis lubab osalist saatmist. Nõutava malli loomiseks järgige neid samme.

1. Avage jaotis **Laohaldus \> Seadistus \> Koormus \> Koormusmallid**.
1. Tegevuspaanil valige häälestuskirje **lisamiseks** uus.
1. Seadke uuel kirjel järgmised väärtused:

    - **Koormuse malli ID:** *osaline*
    - **Luba koorma tükeldamine saadetise kinnitamisel:** *Jah*

1. Sulgege leht **Laadi mallid**.

Lisateavet vt Kinnitusest ja [ülekandmisest](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Müügitellimuse <a0/& protsess

Järgige neid samme müügitellimuse töötlemiseks ja osaliselt lähetamiseks.

1. Viige lõpule [lähetamiseks](packing-containers.md#scenario) pakkekonteinerites esitatud [näidisstsenaarium](packing-containers.md). Selle stsenaariumi korral loote müügitellimuse ühe kauba kahe tüki kohta. Seejärel pakite ainult ühe tüki konteinerisse ja sulete konteineri. Peate looma selle saadetise ID märkuse, nagu stsenaariumis juhendatakse.
1. Avage jaotis **Laohaldus \> Töö \> Kõik tööd**.
1. Märkige filtrialal ruut **Kuva suletud** töö. Seejärel sisestage saadetise ID väljale **Filter ja** valige filtreerimiseks saadetise **ID väärtuse** alusel. Peaksite nüüd nägema kolme tööpäist. Üks on müügitellimuse komplekteerimistöö jaoks ja selle olek on *Suletud*. Pakkimisprotsessi jaoks on kaks kaupa: *üks* on seotud suletud konteineriga ja selle olek on Suletud ning *teine on seotud pakimata järelejäänud kaubaga ja selle olek on Avatud*.
1. Valige koorma **üksikasjade lehe avamiseks mis tahes tööpäise** **koorma ID** väärtus.
1. Lülituge vaatele **Päis**.
1. **Valige kiirkaardil** Üldine nupp **Redigeeri** koormuse **malli ID välja** jaoks. Seejärel valige osaline saadetise koormamall, mille lõite selle stsenaariumi jaoks (*Osaline*).
1. Valige tegevuspaani vahekaardil Läheta **ja** võta vastu kinnitusgrupis **Väljaminev** **saadetis**.
1. Dialoogiaknas **Saada** kinnitus valige suvand Tükelda **kogus uude koormusse**.
1. Valige nupp **OK**.

Olete nüüd lähetanud ühe algse koormaga seotud konteineri ja süsteem on loonud uue koorma ülejäänud kaupadele, mis tuleb veel konteineritesse pakkida.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
