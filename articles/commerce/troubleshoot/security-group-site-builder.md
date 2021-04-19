---
title: Ärisaidi koostaja turbegruppi ei saa algse juurutamise ajal konfigureerida
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui Microsoft Azure Active Directory (Azure AD) ärisaidi koostaja turvagruppi ei kuvata suvandina, kui loote Lifecycle Services (LCS) e-äri komponente uue e-äri rentniku algsel Microsoft Dynamics juurutamisel.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801503"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Ärisaidi koostaja turbegruppi ei saa algse juurutamise ajal konfigureerida

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui Microsoft Azure Active Directory (Azure AD) ärisaidi koostaja turvagruppi ei kuvata suvandina, kui loote Lifecycle Services (LCS) e-äri komponente uue e-äri rentniku algsel Microsoft Dynamics juurutamisel.

## <a name="description"></a>Kirjeldus

Kui loote e-äri komponendid osana uue e-äri rentniku, sealhulgas Commerce'i saidikonstruktori komponenti juurutamisprotsessist, ei kuvata turbegruppi dialoogiboksi Azure AD suvandina.

## <a name="resolution"></a>Eraldusvõime

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>E-kaubanduse saidi ettevalmistamine õiges rentnikus kasutajaga

1. Avage [Azure’i portaalis](https://portal.azure.com/).
1. Rentniku all, kelle jaoks teie e-äri saidi LCS-projekt oli ette antud, järgige juhiseid jaotises [Põhigrupi loomine ja liikmete lisamine Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Minge [LCS](https://lcs.dynamics.com/) ja logige sisse kontoga, mis jagab äsja loodud turvagrupiga Azure AD sama rentnikku. Kontol peab olema turvagrupi Azure AD vaatamiseks juurdepääs.
1. E-äri saidi konfigureerimiseks viige lõpule seadistuse sammud. Kui te e-äri komponente ette kasutate, peaks turvagrupp olema dialoogiaknas valikuna.

> [!NOTE]
> Kindlustamaks, et dialoogiboksi väli täidetakse turvagruppide loendiga, peate valima **Enter** pärast loodud turvagrupi nime Azure AD turvagruppi sisestamist. Otsingutulemustes loetletakse Azure AD kõik turvagrupid, mis algavad otsingutekstiga ja neile on kasutajal juurdepääs. Pikema otsingutulemuse võimaldamiseks saate kasutada lühemat otsingusõna.

## <a name="additional-resources"></a>Lisaressursid

[Looge põhigrupp ja lisage liikmeid, kasutades Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Uue e-kaubanduse rentniku juurutamine](../deploy-ecommerce-site.md)
