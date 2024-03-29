---
title: Allettevõte andmete eksportimine faili
description: See artikkel selgitab, kuidas valmistada ette andmete eksportimist versioonist Microsoft Dynamics 365 Finance ja seejärel importida see konsolideeritud juriidilisele isikule.
author: jinniew
ms.date: 11/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 30d69f9a2813621df410a29568644f264392fb49
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779957"
---
# <a name="export-subsidiary-data-to-files"></a>Allettevõte andmete eksportimine faili

[!include [banner](../includes/banner.md)]

Kasutage lehte **Eksport** (**Süsteemihaldus \> Tööruumid \> Import/Eksport**), et valmistada allandmete eksportimiseks failidesse, mida saab seejärel importida konsolideeritud juriidilisse isikusse. Lisateavet importimise ja eksportimise kohta leiate jaotisest [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Juriidilise isiku loomine konsolideerimisprotsessiks. Lisateavet juriidiliste isikute loomise kohta leiate jaotisest [Juriidilise isiku loomine](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Lisateavet leiate jaotisest [Juriidilise isiku ettevalmistamine konsolideerimisprotsessis kasutamiseks](prepare-company-for-consolidation.md) ja [Allettevõtte juriidilise isiku seadistamine konsolideerimiseks](set-up-subsidiary-company-for-consolidation.md). 

2. Avage **Konsolideerimised \> Ekspordi ettevõtte saldod**. Määratlege lehe **Ekspordi ettevõtte saldod** vahekaardil **Kriteeriumid** konsolideerimise üksikasjad, seadistades järgmised väljad.

    | Field                             | Kirjeldus |
    |-----------------------------------|-------|
    | **Põhikonto**                      | Määrake konsolideeridavad kontod. Kõikide kontode kaasamiseks jätke see väli tühjaks. |
    | **Konsolideerimiskonto kasutamine**         | Kui olete konsolideerimiskontod määranud, määrake selle valiku väärtuseks **Jah**. |
    | **Vali konsolideerimiskonto asukohast** | Valige kas **Põhikonto** või **Konsolideerimiskontode grupp**. |
    | **Konsolideerimiskonto grupp**       | Valige konsolideerimiskontode grupp valitud konsolideerimiskontole. |
    | **Konsolideerimisperiood**              | Määratlege konsolideerimise kuupäevad "alates" ja "kuni". |
    | **Tegelike summade kaasamine**            | Tegelike summade kaasamist seadistage see suvand väärtusele **Jah**. |
    | **Eelarvesummade kaasamine**            | Eelarvesummade konsolideerimisse kaasamiseks seadistage see suvand väärtusele **Jah**. |
    | **Eelarvemudelid**                     | Määrake kaasatav eelarvemudel. |

3. Vahekaardil **Finantsdimensioonid** määratlege konsolideerimise üksikasjad.

    - Määratlege finantsdimensiooni teave, mis tuleks kanda tütarettevõtte kontode kannetest üle konsolideeritud juriidilise üksuse kannetesse.
    - Valige finantsdimensioonid loendist.
    - Tuvastage iga konsolideeritud finantsdimensiooni jaoks õige spetsifikatsioon. Saadaval on valikud **Dimensioon**, **Grupi dimensioon**, **Ettevõtte kontod** ja **Konto**.

        > [!NOTE]
        > Suvand **Grupidimensiooni** võimaldab teil määratleda dimensiooniväärtuse, mida konsolideeritavate ettevõtete grupp kasutab.

    - Määrake segmendijärjestus, milles konsolideerida.

4. Järgige vahekaardil **Juriidilised isikud** näid samme, et määratleda juriidiline isik, keda ekspordite.

    1. Valige suvand **Uus**.
    2. Sisestage juriidiline isik väljale **Algne juriidiline isik**.

        Kui samad kriteeriumid kehtivad mitmetele tütarettevõtetele, mis on samas andmebaasis, saate nende tütarettevõtete andmed ühe toiminguga eraldi ekspordifailidesse üle kanda.

        1. Looge rida iga tütarettevõttest juriidilisele isiku jaoks, kelle kontod eksporditakse failidesse. Need failid imporditakse hiljem konsolideeritud juriidilisele isikule.
        2. Sisestage iga allettevõtte jaoks allettevõtte nimi ja ekspordifaili nimi, mis luuakse eksporditöö jooksul.

    3. Valige väljal **Teisenduserinevuste kontotüüp** suvand **Kasum ja kahjum** või **Bilanss**.
    4. Sisestage faili nimi loodava ekspordifaili jaoks.

5. Ekspordi käivitamiseks valige **OK**.

Kui eksport on lõpetatud, saate sõnumi, mis loetleb kirjete arvu, mis igasse faili salvestati. Seejärel saate importida failid konsolideeritud juriidilisele isikule.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
