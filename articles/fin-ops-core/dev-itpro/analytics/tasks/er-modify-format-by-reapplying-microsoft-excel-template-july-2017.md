---
title: Vormingute muutmine Exceli mallide uuesti rakendamisega
description: Nende etappide lõpuleviimiseks peate esmalt läbima protseduuri „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML”.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 255e45ec724eb4e6a4a87c65f62867eb50c7df93
ms.sourcegitcommit: cb94f16d69455cbf6fd059f9f394e7623810c924
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2020
ms.locfileid: "4011605"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Vormingute muutmine Exceli mallide uuesti rakendamisega

[!include [banner](../../includes/banner.md)]

Nende etappide lõpuleviimiseks peate esmalt läbima protseduuri „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML”.

See protseduur selgitab, kuidas muuta elektroonilise aruandluse (ER) vormingu konfiguratsiooni muudetud Microsoft Exceli malli uuesti rakendades. Selles protseduuris selgitatakse, kuidas importida näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioonidesse muudetud Exceli mall ja seejärel luua elektrooniline dokument. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia GBSI-i andmekomplekti abil. Enne alustamist laadige alla ja salvestage fail SampleVendPaymWsReport2.xlsx, mis on toodud spikriteemas „Elektroonilise aruandluse vormingu muutmine Exceli malli uuesti kasutades“ (modify-electronic-reporting-format-reapply-excel-template/).

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.  

## <a name="select-the-er-format"></a>Elektroonilise aruandluse vormingu valimine
1. Klõpsake valikut Aruandluse konfiguratsioonid.
2. Laiendage puus sõlme „Payment model”.
3. Tehke puul valik Maksemudel \ töölehe aruande näide.
4. Klõpsake suvandit Manused.
    * Pange tähele, et Exceli fail SampleVendPaymWsReport.xlsx on praegu mallina kasutatav makse töölehe töötlemiseks.   
5. Klõpsake valikut Ava.
    * Klõpsake käsku Ava Exceli malli paigutuse uurimiseks.  
    * Vaadake mall üle. Pange tähele, et see sisaldab praegu järgmisi üksikasju iga makserea jaoks: hankija kontonumber, hankija nimi, pank, protsessikood, kontonumber, deebet, kreedit ja valuuta. Näiteks soovime selle loendi laiendamiseks lisada üksikasju maksekuupäeva kohta.   
6. Sulgege leht.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Rakendage elektroonilise aruandluse vormingule uus Exceli mall
1. Klõpsake valikut Kujundaja.
    * Avage mustandversioon valitud elektroonilise aruandluse vormigu redigeerimiseks.  
2. Klõpsake toimingupaanil nuppu Impordi.
3. Klõpsake käsku Uuenda Excelist.
    * Klõpsake valikut „Uuenda malli” ja seejärel valige fail SampleVendPaymWsReport2.xlsx.  
    * Klõpsake nuppu Värskenda malli ja sirvige, et saada varasem allalaaditud fail SampleVendPaymWsReport2.xlsx.  
4. Klõpsake nuppu OK.
    * Mall SampleVendPaymWsReport2.xlsx on rakendatud. Elektroonilise aruandluse vormingu struktuur sünkroonitakse selle malli sisuga, mille elemendid lisatakse elektroonilise aruandluse vormingule. Kõik olemasolevad elektroonilise aruandluse vormingu elemendid, mis pole malli kaasatud, eemaldatakse vormingu definitsioonist.  
5. Tehke puul valik „Excel".
    * Pange tähele, et väli Mall sisaldab nüüd viidet uuele mallile.   
6. Klõpsake suvandit Manused.
7. Klõpsake valikut Ava.
    * Klõpsake käsku Ava muudetud Exceli malli paigutuse uurimiseks.  
    * Vaadake mall üle. Pange tähele, et see sisaldab nüüd maksekuupäeva rida.   
8. Sulgege leht.
9. Laiendage puul valikut „Excel".
10. Puuvaates laiendage „Excel\PaymLines”.
11. Tehke puul valik „Excel\PaymLines\PaymDate".
    * Pange tähele, et elektroonilise aruandluse vorming sisaldab nüüd veel ühte üksust. Exceli malli on lisatud lahter PaymDate.  
12. Klõpsake vahekaarti Vastendus.
13. Laiendage puus sõlme „model”.
14. Laiendage puus sõlme model\Payments.
15. Valige puul suvand model\Payments\Transaction date(TransactionDate).
16. Klõpsake valikut Seo.
    * Täpsustage, millised andmed on uude lahtrisse lisatud käitusajal.  
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Luba elektroonilise aruandluse muudetud mustandversiooni kasutamiseks maksete töölehe töötlemisel
1. Klõpsake tegumiribal valikut Konfiguratsioonid.
2. Klõpsake valikut Kasutaja parameetrid.
3. Tehke väljal Käivita sätted valik Jah.
4. Klõpsake nuppu OK.
5. Klõpsake nuppu Redigeeri.
6. Tehke väljal Käivita mustand valik Jah.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Kasutage elektroonilise aruandluse muudetud mustandversiooni maksete töölehe töötlemiseks

Vaadake üle loodud tööleht (sh makseridade uus üksikasi – maksekuupäev).  
