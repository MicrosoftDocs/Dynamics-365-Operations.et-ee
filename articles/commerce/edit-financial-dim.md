---
title: Jaemüügikannete finantsdimensioonide redigeerimine
description: Selles artiklis kirjeldatakse, kuidas redigeerida Microsoft Dynamics 365 Commerce'is jaemüügikannete finantsdimensioone.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: b382907cd79a13319601dd694261319875565947
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268390"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Jaemüügikannete finantsdimensioonide redigeerimine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas redigeerida Microsoft Dynamics 365 Commerce'is jaemüügikannete finantsdimensioone.

## <a name="edit-financial-dimensions"></a>Finantsdimensioonide redigeerimine

Commerce'i peakontoris jaemüügikannete finantsdimensioonide redigeerimiseks toimige järgmiselt.

1. Avage leht **Finantsdimensioonide konfiguratsioon rakenduste integreerimiseks**.
1. Valige aktiivne kirje **Vaikedimensioonide integratsioon**.
1. Veenduge, et kõik kiirkaardil **Finantsdimensioonid** olevad dimensioonid, mida soovite Exceli töölehel redigeerida, oleksid loendis **Valitud**. Lisateavet leiate artiklist [Andmeüksused](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. Laadige alla ja avage Exceli fail lehelt **Väljavõtted**, lehelt **Jaemüügikanded** või tööruumi **Kaupluse finantsandmed** paanilt **Kande kinnitamise tõrked**.
1. Kande finantsdimensiooni muutmiseks valige **Kujundus** ja seejärel rea **Kanne (auditeeritav)** kõrval olev pliiatsisümbol.
1. Leidke ja valige väli **FinancialDimensionDisplayValue**, valige Exceli töölehe päiseosas lahter ja seejärel suvand **Lisa silt**.
1. Valige eelmises sammus valitud lahtri all olev lahter, valige **Lisa väärtus** ja seejärel **Värskenda**. Finantsdimensioonid lisatakse Exceli töölehele ning neid saab seejärel redigeerida ja avaldada.
1. Kanderidade dimensioonide muutmiseks valige rida **Müügikanded (auditeeritav)**, valige pliiatsisümbol ning järgige uuesti samme 6 ja 7.
1. Makseridade dimensioonide muutmiseks valige rida **Maksekanded (auditeeritav)**, valige pliiatsisümbol ning järgige uuesti samme 6 ja 7.

## <a name="additional-resources"></a>Lisaressursid

[Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine](edit-cash-trans.md)

[Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine](edit-order-trans.md)

[Exceli töövihiku loomine jaemüügikannete redigeerimiseks](create-excel-edit.md)

[Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
