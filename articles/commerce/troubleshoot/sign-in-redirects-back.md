---
title: Sisselogimislingi ümbersuunamised tagasi e-äri saidile
description: See teema pakub tõrkeotsingu juhiseid, mis aitavad teil sisselogimise lingil tagasi e-äri saidile ümber suunata, selle asemel et minna sisselogimislehele.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 94afc339bd156d26c5057c1e401d707aa7d517a041493659a40c7b69ad4d377a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715280"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Sisselogimislingi ümbersuunamised tagasi e-äri saidile

[!include [banner](../../includes/banner.md)]

See teema pakub tõrkeotsingu juhiseid, mis aitavad teil sisselogimise lingil tagasi e-äri saidile ümber suunata, selle asemel et minna sisselogimislehele.

## <a name="description"></a>Kirjeldus

Pärast uue Microsoft Azure Active Directory B2C (Azure AD B2C) rentniku konfigureerimist Commerce'i saidi koostajas, kes valisid **sisselogimise** suunatakse kasutajad tagasi, ilma sisselogimislehele minemata.

## <a name="resolution"></a>Eraldusvõime

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Veenduge, et vastuse URL on Azure AD B2C-rakenduses õigesti konfigureeritud

Veenduge, et vastuse URL on Azure AD B2C-rakenduses õigesti konfigureeritud, järgides järgmisi samme.

1. Avage [Azure’i portaalis](https://portal.azure.com/).
1. Valige Azure AD B2C-rakendus, mille lõite oma saidi juurdepääsuks.
1. Valige rakendus, mille lõite Azure AD B2C-seadistuse ajal.
1. **Vastuse URLi** all veenduge, et loend sisaldab kirjeid nii saidi domeeni URL-i kui e-kaubanduse loodud URL-i kohta, nagu näidatud järgmises illustratsioonis.

    ![Azure AD B2C-vastuse URL-i kirjed.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Nii saidi domeeni URL kui ka e-äri loodud URL peavad olema kehtivas URL-vormingus, mis ei sisalda lõpu- või lõpukriipse.

## <a name="additional-resources"></a>Lisaressursid

[Ühendatud rakenduse registreerimine Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[B2C-rentniku häälestus Commerce'is](../set-up-b2c-tenant.md)