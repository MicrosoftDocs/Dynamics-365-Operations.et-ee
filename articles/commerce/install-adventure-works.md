---
title: Adventure Worksi kujunduse installimine
description: See teema kirjeldab, kuidas installida Adventure Worksi kujundust rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655844"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Worksi kujunduse installimine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas installida Adventure Worksi kujundust rakenduses Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Adventure Works teema ja moodulid on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20. Need on saadaval rakendusest Microsoft AppSource.

## <a name="prerequisites"></a>Eeltingimused

Enne Adventure Worksi kujunduse installimist peab teil olema Dynamics 365 Commerce keskkond (Commerce version 10.0.20 või uuem), mis sisaldab Retail Cloud Scale Unit (RCSU), Commerce online tarkvara arenduskomplekti (SDK) ja Commerce mooduli teeki. Lisateavet Commerce SDK ja moodulteegi installimise kohta vt [SDK- ja mooduliteegi uuendused](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Installimisetapid

### <a name="install-the-adventure-works-theme-in-your-application"></a>Installi oma rakendusse Adventure Worksi teema

Adventure Worksi teemapakett on saadaval feedis **dynamics365-commerce** kui **@msdyn365-commerce-theme/adventureworks-theme-kit**. Kuigi teemapakett Adventure Works on selle voo osa, on see erineva nimeruumi all. Seetõttu peate nimeruumi registrikirjete lisamiseks järgima neid samme.

1. Värskendage **.npmrc** faili, et see sisaldaks järgmist registrikirjet (kui kirjet juba ei kaasata):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Värskendage **.yarnrc** faili, et see sisaldaks järgmist registrikirjet (kui kirjet juba ei kaasata):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Paketi installimiseks kohalikus keskkonnas käivitage käsuviibalt järgmine käsk. See käsk uuendab faili package.json automaatselt nii, et see sisaldaks sõltuvust.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

Failis **package.json** peaksite värskendama kujunduse versiooni konkreetseks versiooniks.

> [!IMPORTANT]
> - Kujunduse versioon peab vastama moodulteegi versioonile, et tagada kõigi funktsioonide eeldatav töö. 
> - Commerce mooduli teek ja SDK minimaalse versiooni peab olema 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Fondifailide lisamine Adventure Worksi kujundusele

Kui Adventure Worksi teema on teie rakendusse installitud, peate lisama sellele vajalikud fondifailid. Selle sammu lõpuleviimiseks kopeerige kõik fondifailid asukohast **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** partnerrakenduse avalikku asukohta **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Seadistage Adventure Works teema ressursid

Järgmiseks sammuks on kujunduse jaoks nõutava vaikeressursi värskendamine. Selle sammu lõpuleviimiseks kopeerige sisu failist global.json asukohas **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** partnerrakenduse global.json faili asukohas **\src\resources\modules**. Kui **\src\resources** sihtkataloogi ei ole olemas, saab selle kopeerida tervikuna lähtekaustast **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** sihtkataloogi **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Tõmba värskendused ja kinnita kujundus

Lisateavet viimase SDK, mooduliteegi ja muude sõltuvuste värskenduste tõmbamise kohta vt [SDK ja moodulteegi värskendused](e-commerce-extensibility/sdk-updates.md#pull-updates) jaotisest "Tõmba värskendused".

Kui viimased sõltuvused on alla tõmmatud, saate käivitada käivituskäsku **yarn start**, et käivitada Node serveri oma arenduskeskkonnas ja katsetada uut Adventure Worksi kujundust. Sirvige rakendust kohalikult, kasutades päringustringi `?theme=adventureworks` parameetrit (nt `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Lisaressursid

[Adventure Works teema](adventure-works-theme.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
