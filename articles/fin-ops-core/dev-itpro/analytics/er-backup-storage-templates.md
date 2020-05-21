---
title: ER-mallide varukoopia salvestamine
description: Selles teemas selgitatakse, kuidas kasutada elektroonilise aruandluse (ER) varundusmälu mallide taastamiseks.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2e399290153c2c63ac1c02f0f9cdb956ff5031e5
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321662"
---
# <a name="backup-storage-of-er-templates"></a>ER-mallide varukoopia salvestamine

[!include [banner](../includes/banner.md)]

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md) võimaldab ärikasutajatel konfigureerida väljuvate dokumentide vorminguid erinevate riikide ja regioonide õigusnõuete järgi. Konfigureeritud ER-vormingud saavad kasutada eelmääratletud malle, et luua väljaminevaid dokumente erinevates vormingutes, näiteks Microsoft Exceli töövihikud, Microsoft Wordi dokumendid või PDF-dokumendid. Mallid on täidetud andmetega, mida genereeritud dokumentide konfigureeritud andmevoog nõuab.

Kõiki vorminguid saab avaldada ER-lahenduse osana. Iga ER-i lahendust saab eksportida ühest Finance and Operations-i eksemplarist ning importida teise eksemplari.

ER-i raamistik kasutab [dokumendihalduse konfigureerimist](../../fin-ops/organization-administration/configure-document-management.md), et säilitada praeguse Finance and Operations-i eksemplari jaoks nõutavad mallid. Sõltuvalt ER-raamistiku sätetest saab valida Microsoft Azure Bloobi salvestamise või Microsoft SharePoint kausta, mis on mallide füüsilise esmase salvestamise vaikeasukoht. (Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).) DocuValue tabel sisaldab iga malli kohta eraldi kirjet. Igas kirjes talletab väli **AccessInformation** konfigureeritud salvestuskohas asuva mallifaili tee.

Kui haldate oma Finance and Operations-i eksemplare, võite valida praeguse eksemplari siirdamise teise asukohta. Näiteks võite oma tootmiseksemplari migreerida uude liivakastikeskkonda. Kui konfigureerisite ER-raamistiku talletama malle Bloobi salvestamises, viitab DocuValue tabel uues liivakastikeskkonnas Bloobi salvestamise eksemplarile tootmiskeskkonnas. Sellele eksemplarile ei pääse aga juurde liivakastikeskkonnast, sest migreerimisprotsess ei toeta artefaktide migreerimist Bloobi salvestamises. Seetõttu, kui proovite käitada ER-vormingut, mis kasutab malli äridokumentide loomiseks, ilmneb erand ja teid teavitatakse puuduvast mallist. Juhendate ka ER-puhastustööriista kasutamist malli sisaldava ER-vormingu konfiguratsiooni kustutamiseks ja uuesti importimiseks. Kuna teil võib olla mitu ER-vormingu konfiguratsiooni, võib see protsess olla aeganõudev.

ER-mallide varundusfunktsioon aitab teil malle luua nii, et need oleksid alati äridokumentide loomiseks saadaval.

> [!NOTE]
> Seda funktsiooni saab kasutada ainult siis, kui on märgitud, et ER-mallide füüsiline talletuskoht on valitud.

## <a name="automated-recovery-and-notification"></a>Automaatne taaste ja teavitamine

Selle funktsiooni puhul salvestatakse kõik praeguse keskkonna uue ER-vormingu konfiguratsiooni mallid automaatselt mallide varukoopia salvestuskohta (ERDocuDatabaseStorage andmebaasitabel), kui ilmnevad järgmised sündmused:

- Impordite uue ER-vormingu konfiguratsiooni, mis sisaldab malli.
- Saate lõpule viia malli sisaldava ER-vormingu konfiguratsiooni mustandversiooni.

Mallide varukoopiad migreeritakse osana rakenduse andmebaasist uude Finance and Operations-i eksemplari.

Kui väljaminevate dokumentide genereerimiseks on nõutav ER-vormingu mall, mis töötleb näiteks hankijamakseid, sealhulgas maksenõustamis- ja kontrolliaruannete genereerimist, kuid vajalikku malli ei leita primaarses talletuskohas, ilmnevad järgmised sündmused.

- Kui mall on saadaval varunduse talletamise asukohas, võetakse see automaatselt varunduse asukohast, taastatakse esmasesse salvestamise asukohta ja kasutatakse praeguse käivitamise puhul.
- Iga kasutaja, kellele on määratud **Elektroonilise aruandluse arendaja** või **Süsteemiadministraatori** roll, teavitatakse puuduva malli probleemist tegevuskeskuse kaudu. Kuvatav teade sõltub parameetri **Katkestatud mallide automaatse taastamise protseduur partiis** väärtusest.

    - Kui see teade on **Välja lüitatud**, soovitab teade käivitada pakktöötlusprotsessi, et lahendada sarnased probleemid automaatselt teiste ER-vormingus Teade sisaldab linki, mida saate kasutada pakktöötluse käivitamiseks.
    - Kui selle parameetri väärtuseks on **Sees**, teavitab teade teid puuduvast mallist ja sellest, et uus masstöötlusprotsess  **Taasta katkenud mallid sisemise andmebaasi varukoopiast** on automaatselt ajastatud. See pakktöötlus parandab automaatselt teiste mallide sarnaseid probleeme.

Parameetri **Katkestatud mallide automaatse taastamise protseduur partiis** seadmiseks toimige järgmiselt. 

1. Avage rakenduses Finance and Operations **Organisatsiooni haldus \> Elektrooniline aruandlus \> Konfiguratsioonide leht**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Määrake dialoogiboksis **Kasutaja parameetrid** vajalik väärtus parameetrile **Katkestatud mallide automaatse taastamise protseduur partiis**.

> [!NOTE]
> See parameeter on määratletud rakenduse kasutaja ja logitud ettevõtte spetsiifilise parameetrina.

![ER-seadete leht](./media/GER-BackupTemplates-1.png)

Järgmisel joonisel on kujutatud teate näidet, mis kuvatakse siis, kui parameeter **Katkestatud mallide automaatse taastamise protseduur partiis** on **Sees**.

![Hankija maksetööleht](./media/GER-BackupTemplates-2.png)

Järgmisel joonisel on näha pakktöötlust **Katkenud mallide taastamine andmebaasi sisemise varunduse abil** lehel **Pakett-töö**.

![Pakett-töö leht](./media/GER-BackupTemplates-3.png)

Lõpetatud **Taasta katkenud mallid sisemisest andmebaasi varundusest** pakktöötlusprotsess sisaldab teavet mallide kohta, mis on taastatud varukoopia talletuskohast esmase talletuskohani.

![Pakett-töö ajaloo leht](./media/GER-BackupTemplates-4.png)

Vaikimisi on sisse lud ER-vorminguga konfiguratsioonides sisalduvatest mallidest automaatselt varukoopiate loomise protsess. Mallidest varukoopiate tegemise lõpetamiseks seadke **Peata mallidest varukoopiate tegemine** valikuks **Jah** vahekaardil **Manused** lehel **Elektroonilise aruandluse parameetrid**. Selle lehe saate avada tööruumist **Elektrooniline aruandlus**.

Kui määrate suvandi **Peata mallidest varukoopiate tegemine** väärtuseks **Jah** ja te ei soovi säilitada varem mallidest tehtud varukoopiaid, valige **Puhasta varunduse salvestusruum** lehel **Elektroonilise aruandluse parameetrid**.

Kui täiendasite oma keskkonna Finance and Operations-i versioonile 10.0.5 (oktoober 2019) ja soovite siirduda uude keskkonda, mis sisaldab käitatavaid ER-vormingu konfiguratsioone, valige enne migreerimist **Täida varundusmälu** lehel **Elektroonilise aruandluse parameetrid**. See nupp käivitab kõigi saadaolevate mallide varukoopiate tegemise, nii et neid saab talletada mallide ER-varunduse talletuskohas.

![Elektroonilise aruandluse parameetrite leht](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Käsitsi taastamine

Avage **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Katkenud mallide taastamine**, et käivitada käsitsi ER-mallide taasteprotsess varunduse talletuskohast esmasesse talletuskohta. Enne protsessi käivitamist saate lehel **Katkenud mallide taastamine** täpsustada, kas soovite, et protsess teostataks interaktiivselt või et selleks kavandataks partiiprotsess.

## <a name="supported-deployments"></a>Toetatud juurutused

Finance and Operations-i versioonis 10.0.5 on ER-mallide varundusmälu funktsioon saadaval ainult pilvejuurutustes.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md)
