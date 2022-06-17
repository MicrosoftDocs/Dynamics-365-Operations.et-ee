---
title: Partii jälgimisega kaupade täiustatud käsitlemine
description: Selles artiklis kirjeldatakse väljavõtete sisestuse käigus tehtud partii jälgimisega kaupade täiustustatud käsitlemist teenuses Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 736ab8dd21f04d7119cca6d53bfeb5e408b8cbd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881874"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Partii jälgimisega kaupade täiustatud käsitlemine

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse väljavõtete sisestuse käigus tehtud partii jälgimisega kaupade täiustustatud käsitlemist teenuses Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce'i kassas (POS) ei saa partiinumbreid partii jälgimisega kaupade puhul müügi hetkel jäädvustada. Kui müügiandmed sisestatakse Commerce'i peakontoris klienditellimuste või väljavõtete sisestuse käigus, siis eeldab Commerce teatud konfiguratsioonide korral, et partii jälgimisega kaupade jaoks on olemas sobivad partiinumbrid ja neid kasutatakse arveldusprotsessis.

Kui toodete jaoks on saadaval sobivad partiinumbrid, kasutavad nii väljavõtete sisestamise käigus toimuv klienditellimuste arveldamise protsess ja müügitellimuste arveldamise protsess neid partiinumbreid. Kui kehtivad partiinumbrid pole toodete puhul saadaval, ei saa klienditellimuse arveldamisprotsessi sisestada ja müügikoha kasutaja saab tõrketeate. Väljavõtte sisestamine läheb siis tõrkeolekusse, isegi kui negatiivne laovaru on toodete puhul sisse lülitatud.

Commerce'is tehtud täiustused aitavad tagada, et kui partii jälgimisega kaupade jaoks on sisse lülitatud negatiivsed varud, ei blokeerita nende kaupade puhul väljavõtete sisestuse kaudu toimuvat klienditellimuste arveldust ega müügitellimuste arveldust, kui varude väärtus on 0 (null) või partiinumber pole saadaval. Kui partiinumbrid pole saadaval, kasutab see täiustatud funktsioon müügiridade jaoks vaikimisi partii ID.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Määratlege vaikimisi partii ID, mida kasutatakse klienditellimuste jaoks

Klienditellimuste jaoks kasutatava vaikimisi partii ID määratlemiseks järgige allolevaid juhiseid.

1. Valige Commerce'i peakontoris suvandid **Retail ja Commerce \> Peakontori seadistamine \> Parameetrid \> Commerce'i parameetrid**.
1. Sisestage väärtus vahekaardi **Klienditellimused** kiirkaardi **Tellimus** väljale **Vaikimisi partii ID**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Määratlege vaikimisi partii ID, mida kasutatakse müügitellimuse arveldamiseks väljavõtte sisestamise kaudu

Vaikimisi partii ID määratlemiseks, mida kasutatakse müügitellimuse arveldamiseks väljavõtte sisestamise kaudu, järgige allolevaid juhiseid.

1. Valige Commerce'i peakontoris suvandid **Retail ja Commerce \> Peakontori seadistamine \> Parameetrid \> Commerce'i parameetrid**.
1. Sisestage väärtus vahekaardi **Sisestamine** kiirkaardi **Laoseisu uuendamine** väljale **Vaikimisi partii ID**.

> [!NOTE]
> - Vaikimisi partii ID funktsioon on saadaval ainult juhul, kui konkreetse kaupluse lao ja kaupade jaoks on lubatud täpsem laohaldus. Järgmises versioonis toetatakse vaikimisi partii ID funktsiooni ka selliste stsenaariumite puhul, kus täpsem laohaldus poel lubatud.
> - Partii jälgimisega kaupade täiustatud töötlemise tugi väljavõtte sisestamise ajal võeti täpsemat laohaldust mittekasutavates stsenaariumites kasutusele Commerce'i versiooni 10.0.5 väljalaskes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
