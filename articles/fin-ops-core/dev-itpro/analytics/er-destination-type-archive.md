---
title: ER-i sihtkoha tüübi arhiveerimine
description: See artikkel annab teavet arhiivi sihtkoha konfigureerimise kohta iga elektroonilise aruandluse (ER) vormingus KAUSTA või FAILI komponendi jaoks.
author: kfend
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: d907bf391c0629d62da489cea90a05eabaf69ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285451"
---
# <a name="archive-er-destination-type"></a>ER-i sihtkoha tüübi arhiveerimine

[!include [banner](../includes/banner.md)]

Saate konfigureerida arhiivi sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga **kausta** või **faili** komponendi jaoks. Sihtkoha sätte põhjal talletatakse loodud dokument ER tööde loendi kirje manusena. Tulemuste vaatamiseks avage jaotis **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse tööd**.

Selle valiku abil saab saata loodud dokumendi Microsoft SharePointi kausta või Microsoft Azure’i salvestusruumi. Määrake valiku **Lubatud** väärtuseks **Jah** väljundi saatmiseks valitud dokumenditüübiga määratletud sihtkohta. Valida saab ainult neid dokumenditüüpe, millel grupiks on määratud **Fail**. Dokumendi [tüübid](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) saate määratleda jaotistes **Organisatsiooni haldus**\> **Dokumendihaldus**\> **Dokumenditüübid**. ER-i sihtkohtade konfiguratsioon on sama, mis dokumendihaldussüsteemi konfiguratsioon.

[![Dokumenditüüpide lehed.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Asukoht määrab, kuhu fail salvestatakse. Kui sihtkoht **Arhiiv** on lubatud, saab konfiguratsiooni käivitamise tulemused salvestada tööarhiivi. Tulemusi saate vaadata jaotises **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse arhiivitud tööd**.

> [!NOTE]
> Tööarhiivi jaoks saate dokumenditüübi valida, liikudes jaotisesse **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse parameetrid**. Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Faili saab salvestada selleks mõeldud SharePointi kausta. SharePointi vaikeserveri määratlemiseks avage **Organisatsiooni haldus**\> **Dokumendihaldus**\> **Dokumendihalduse parameetrid**. Vahekaardil **SharePoint** konfigureerige SharePointi kaust. Seejärel saate valida selle kausta, kuhu ER väljund salvestatakse. Selle dokumenditüübi **SharePoint** i asukoht peab olema valitud.

[![SharePoint`i kausta valimine.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure’i salvestusruum

Kui dokumenditüübi asukohaks on määratud **Azure'i salvestusruum**, saate faili salvestada Azure’i salvestusruumi.

> [!NOTE] 
> ER-i raamistik salvestab failid püsivalt Azure’i bloobimällu, erinevalt andmehaldusraamistikule, mis rakendab seitsmepäevast dokumentide säilituspoliitikat dokumentidele, mis tuleb töödelda. Lisateabe saamiseks vt teemat [Olekusõnumi olekute läheduses](../data-entities/recurring-integrations.md#api-for-getting-message-status)ja [Oleku kontrollimise API](../data-entities/data-management-api.md#status-check-api). ER-ga seotud failid talletatakse Azure’i bloobimälus vastavate tabeli kirjete manustena nii kaua kui vajalik. Aure’i bloobimälust kustutatakse üks fail koos rakenduse tabeli kirjega, millele see fail oli manustatud.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Dokumendihalduse konfigureerimine](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
