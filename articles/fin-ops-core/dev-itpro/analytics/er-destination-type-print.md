---
title: ER-i sihtkoha tüübi printer
description: See artikkel selgitab, kuidas konfigureerida printeri sihtkohta elektroonilise aruandluse (ER) vormingus iga KAUSTA või FAILI komponendi jaoks.
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 826455d0901a45ef26755fd323ee2a2737b5eec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845566"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Printeri sihtkoht

[!include [banner](../includes/banner.md)]

Saate loodud dokumendi otse printimiseks otse võrguprinterisse saata.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist peate installima ja konfigureerima dokumendi marsruudi agendi ning seejärel registreerima võrgu printerid. Lisateavet saate teemast [Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Printeri sihtkoha kättesaadavaks tegemine

Et teha printeri **sihtkoht** praeguses Microsoft Dynamics 365 Finance eksemplaris kättesaadavaks, **minge** Funktsioonihalduse tööruumi ja lülitage järgmised funktsioonid sisse selles järjekorras:

1. Teisenda elektroonilise aruandluse väljaminevad dokumendid Microsoft Office'i vormingutest PDF-iks
2. Dokumendi marsruudivaliku agent väljaminevate dokumentide elektroonilise aruandluse sihtkohana

[![ER printeri sihtkoha funktsiooni sisselülitamine funktsioonide halduses.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Kohaldatavus

#### <a name="pdf-printing"></a>PDF-printimine

Rakenduse Finance versioonides enne versiooni 10.0.18 saab printerit konfigureerida ainult failikomponentide jaoks, **mida** kasutatakse väljundi loomiseks prinditavas PDF-vormingus (**PDF-liitumine** **või PDF-failivormingu** elemendid) Microsoft Office Excel või Wordi vormingus (**Exceli failivormingu** element). Kui väljund luuakse PDF-vormingus, saadetakse see printerisse. Kui väljund luuakse Office'i vormingus Exceli **failivormingu** elemendi abil, teisendatakse see automaatselt PDF-vormingusse ja saadetakse seejärel printerisse.

Versiooni 10.0.18 **·** **puhul saate siiski konfigureerida failivormingu tavaelemendile** printeri sihtkoha. Seda vorminguelementi kasutatakse enamasti väljundi loomiseks kas TXT- või XML-vormingus. Saate konfigureerida ER-vormingu, **·** **mis** sisaldab tavalise failivormingu elementi juurvormingu elemendina ja binaarsisu vormingu elementi selle all ainsa pesastatud elemendina. Sellisel juhul loob üldine failivormingu **element** väljundi vormingus, **mis on määratud kahendsisu vormingu elemendi jaoks konfigureeritud** sidumisega. Näiteks saate konfigureerida selle [sidumise](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format)[nii](../../fin-ops/organization-administration/configure-document-management.md), et see täidaks selle elemendi dokumendihalduse manuse sisuga PDF- või Office'i (Excel või Word) vormingus. Saate printida väljundi konfigureeritud printerisihtkoha **abil**. 

> [!NOTE]
> Kui valite **\\** **tavalise** faili vormingu elemendi sihtkoha konfigureerimiseks, pole võimalik tagada kujundusaja jooksul, kas valitud element annab väljundi PDF-vormingus või väljundi, mida saab teisendada PDF-vormingusse. Seetõttu saate järgmise hoiatusteate: "Palun veenduge, et valitud vormingukomponendi loodud väljundi saab teisendada PDF-iks. Vastasel juhul eemaldage märge suvandilt Teisenda PDF-vormingusse." Käitusaja probleemide vältimiseks peate käitusaja probleemide vältimiseks tegemata PDF-vormingus või pdf-vormingus teisendatava väljundi printimiseks käitusajal. Kui eeldate saada toodangut Office'i (Exceli või Wordi) vormingus, peab **olema valitud suvand Teisenda PDF-ina**.
>
> Versioonis 10.0.26 **ja uuemas versioonis peate konfigureeritud** **printeri sihtparameetri jaoks valima PDF-i.** **·** **·**

#### <a name="zpl-printing"></a>ZPL-i printimine

Versioonis 10.0.26 ja uuemas versioonis saate konfigureerida tavalise faili vormingu elemendi printeri sihtkoha, **·** **\\** **valides dokumendi protsessitüübi parameetrile ZPL.** **·** Sel juhul **ignoreeritakse suvandit Teisenda PDF-ina** käitusajal ja TXT või XML-i väljund saadetakse otse valitud printerisse, kasutades Dokumendi protsessiagendi (DRA [)](install-document-routing-agent.md) ZPL-lepingut. Kasutage seda funktsiooni ER-vormingu jaoks, mis tähistab erinevate siltide printimiseks ZPL II sildipaigutust.

[![Dokumendi protsessitüübi parameetri seadistamine dialoogiboksis Sihtkoha sätted.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Lisateavet selle funktsiooni kohta vt Teemast Uue [ER-lahenduse loomine ZPL-siltide printimiseks](er-design-zpl-labels.md).

### <a name="limitations"></a>Kitsendused

**Printeri** sihtkohta rakendatakse ainult pilve juurutamiseks.

### <a name="use-the-printer-destination"></a>Printimise sihtkoha kasutamine

1. Seadke **Lubatud** suvand väärtusele **Jah**, et saata loodud dokument printerisse.
2. Valige väljal **Printeri nimi** vajalik võrguprinter.
3. Seadke suvand **Kas soovite salvestada printimise arhiivi?** väärtusele **Jah**, et salvestada loodud väljund printimise arhiivi, nii et see on edasiseks printimiseks saadaval. Arhiveeritud väljundi juurde pääsemiseks hiljem avage **Organisatsiooni haldus** \> **Päringud ja aruanded** \> **Aruannete arhiiv**.

[![Printimise sihtkoha kasutamine.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Suvand **Teisendamine PDF-iks** ei pea **Printeri** sihtkoha konfigureerimisel olema sisse lülitatud. PDF-i teisendamine printimiseks toimub isegi siis, kui suvand on välja lülitatud.

Kindla [lehe paigutuse](electronic-reporting-destinations.md#SelectPdfPageOrientation) kasutamiseks väljamineva Exceli vormingus dokumendi printimiseks, peate sisse lülitama suvandi **Teisenda PDF-iks**. Kui määrate suvandi **Teisenda PDF-iks** väärtuseks **Jah**, on saadaval väli **Lehe paigutus**. Väljal **Lehe paigutus** saate valida lehe paigutuse.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
