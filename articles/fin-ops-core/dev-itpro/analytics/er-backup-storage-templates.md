---
title: ER-mallide varukoopia salvestamine
description: See artikkel selgitab, kuidas kasutada mallide taastamiseks elektroonilise aruandluse (ER) varundussalvestust.
author: NickSelin
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 635e7152bece91d5dee47f82cef7052730eb0c82
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108948"
---
# <a name="backup-storage-of-er-templates"></a>ER-mallide varukoopia salvestamine

[!include [banner](../includes/banner.md)]

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md) võimaldab ärikasutajatel konfigureerida väljuvate dokumentide vorminguid erinevate riikide ja regioonide õigusnõuete järgi. Konfigureeritud ER-vormingud saavad kasutada eelmääratletud malle, et luua väljaminevaid dokumente erinevates vormingutes, näiteks Microsoft Exceli töövihikud, Microsoft Wordi dokumendid või PDF-dokumendid. Mallid on täidetud andmetega, mida genereeritud dokumentide konfigureeritud andmevoog nõuab.

Kõiki vorminguid saab avaldada ER-lahenduse osana. Iga ER-i lahendust saab eksportida ühest finantside ja toimingute eksemplarist ning importida teise eksemplari.

ER-raamistik kasutab dokumendihalduse [konfigureerimise toiminguid](../../fin-ops/organization-administration/configure-document-management.md), et säilitada nõutavad mallid praeguse finantside ja toimingute eksemplari jaoks. Sõltuvalt ER-raamistiku sätetest saab valida Microsoft Azure Bloobi salvestamise või Microsoft SharePoint kausta, mis on mallide füüsilise esmase salvestamise vaikeasukoht. (Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).) DocuValue tabel sisaldab iga malli kohta eraldi kirjet. Igas kirjes talletab väli **AccessInformation** konfigureeritud salvestuskohas asuva mallifaili tee.

Kui haldate finants- ja operatsioonide eksemplare, võite otsustada praeguse eksemplari teise asukohta üle siirdada. Näiteks võite oma tootmiseksemplari migreerida uude liivakastikeskkonda. Kui konfigureerisite ER-raamistiku talletama malle Bloobi salvestamises, viitab DocuValue tabel uues liivakastikeskkonnas Bloobi salvestamise eksemplarile tootmiskeskkonnas. Sellele eksemplarile ei pääse aga juurde liivakastikeskkonnast, sest migreerimisprotsess ei toeta artefaktide migreerimist Bloobi salvestamises. Seetõttu, kui proovite käitada ER-vormingut, mis kasutab malli äridokumentide loomiseks, ilmneb erand ja teid teavitatakse puuduvast mallist. Juhendate ka ER-puhastustööriista kasutamist malli sisaldava ER-vormingu konfiguratsiooni kustutamiseks ja uuesti importimiseks. Kuna teil võib olla mitu ER-vormingu konfiguratsiooni, võib see protsess olla aeganõudev.

ER-mallide varundusfunktsioon aitab teil malle luua nii, et need oleksid alati äridokumentide loomiseks saadaval.

> [!NOTE]
> Seda funktsiooni saab kasutada ainult siis, kui on märgitud, et ER-mallide füüsiline talletuskoht on valitud.

## <a name="automated-recovery-and-notification"></a>Automaatne taaste ja teavitamine

Selle funktsiooni puhul salvestatakse kõik praeguse keskkonna uue ER-vormingu konfiguratsiooni mallid automaatselt mallide varukoopia salvestuskohta (ERDocuDatabaseStorage andmebaasitabel), kui ilmnevad järgmised sündmused:

- Impordite uue ER-vormingu konfiguratsiooni, mis sisaldab malli.
- Saate lõpule viia malli sisaldava ER-vormingu konfiguratsiooni mustandversiooni.

Mallide varukoopiad migreeritakse rakenduse andmebaasi osana uude finantside ja toimingute eksemplari.

Kui väljaminevate dokumentide genereerimiseks on nõutav ER-vormingu mall, mis töötleb näiteks hankijamakseid, sealhulgas maksenõustamis- ja kontrolliaruannete genereerimist, kuid vajalikku malli ei leita primaarses talletuskohas, ilmnevad järgmised sündmused.

- Kui mall on saadaval varunduse talletamise asukohas, võetakse see automaatselt varunduse asukohast, taastatakse esmasesse salvestamise asukohta ja kasutatakse praeguse käivitamise puhul.
- Iga kasutaja, kellele on määratud **Elektroonilise aruandluse arendaja** või **Süsteemiadministraatori** roll, teavitatakse puuduva malli probleemist tegevuskeskuse kaudu. Kuvatav teade sõltub parameetri **Katkestatud mallide automaatse taastamise protseduur partiis** väärtusest.

    - Kui see teade on **Välja lüitatud**, soovitab teade käivitada pakktöötlusprotsessi, et lahendada sarnased probleemid automaatselt teiste ER-vormingus Teade sisaldab linki, mida saate kasutada pakktöötluse käivitamiseks.
    - Kui selle parameetri väärtuseks on **Sees**, teavitab teade teid puuduvast mallist ja sellest, et uus masstöötlusprotsess **Taasta katkenud mallid sisemise andmebaasi varukoopiast** on automaatselt ajastatud. See pakktöötlus parandab automaatselt teiste mallide sarnaseid probleeme.

Parameetri **Katkestatud mallide automaatse taastamise protseduur partiis** seadmiseks tehke järgmist.

1. Avage finantside ja toimingute puhul organisatsiooni **halduse \> elektroonilise aruandluse \> konfiguratsioonide leht**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Määrake dialoogiboksis **Kasutaja parameetrid** vajalik väärtus parameetrile **Katkestatud mallide automaatse taastamise protseduur partiis**.

> [!NOTE]
> See parameeter on määratletud rakenduse kasutaja ja logitud ettevõtte spetsiifilise parameetrina.

![ER-i konfiguratsiooni leht.](./media/GER-BackupTemplates-1.png)

Järgmisel joonisel on kujutatud teate näidet, mis kuvatakse siis, kui parameeter **Katkestatud mallide automaatse taastamise protseduur partiis** on **Sees**.

![Hankija maksetööleht.](./media/GER-BackupTemplates-2.png)

Järgmisel joonisel on näha pakktöötlust **Katkenud mallide taastamine andmebaasi sisemise varunduse abil** lehel **Pakett-töö**.

![Pakett-töö leht.](./media/GER-BackupTemplates-3.png)

Lõpetatud **Taasta katkenud mallid sisemisest andmebaasi varundusest** pakktöötlusprotsess sisaldab teavet mallide kohta, mis on taastatud varukoopia talletuskohast esmase talletuskohani.

![Pakett-töö ajaloo leht.](./media/GER-BackupTemplates-4.png)

Vaikimisi on sisse lud ER-vorminguga konfiguratsioonides sisalduvatest mallidest automaatselt varukoopiate loomise protsess. Mallidest varukoopiate tegemise lõpetamiseks seadke **Peata mallidest varukoopiate tegemine** valikuks **Jah** vahekaardil **Manused** lehel **Elektroonilise aruandluse parameetrid**. Selle lehe saate avada tööruumist **Elektrooniline aruandlus**.

Kui määrate suvandi **Peata mallidest varukoopiate tegemine** väärtuseks **Jah** ja te ei soovi säilitada varem mallidest tehtud varukoopiaid, valige **Puhasta varunduse salvestusruum** lehel **Elektroonilise aruandluse parameetrid**.

Kui uuendasite oma keskkonda finantside ja toimingute versiooniks 10.0.5 (oktoober 2019) ja soovite migreerida uude keskkonda, mis sisaldab käivitada ER-vormingu konfiguratsioone, **·** **valige** enne migreerimist elektroonilise aruandluse parameetrite lehel varusalvestuse täitmine. See nupp käivitab kõigi saadaolevate mallide varukoopiate tegemise, nii et neid saab talletada mallide ER-varunduse talletuskohas.

![Elektroonilise aruandluse parameetrite leht.](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Käsitsi taastamine

Avage **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Katkenud mallide taastamine**, et käivitada käsitsi ER-mallide taasteprotsess varunduse talletuskohast esmasesse talletuskohta. Enne protsessi käivitamist saate lehel **Katkenud mallide taastamine** täpsustada, kas soovite, et protsess teostataks interaktiivselt või et selleks kavandataks partiiprotsess.

## <a name="supported-deployments"></a>Toetatud juurutused

Finantside ja toimingute versioonis 10.0.5 on ER-mallide funktsiooni varundussalvestus saadaval ainult pilve juurutamistes.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
