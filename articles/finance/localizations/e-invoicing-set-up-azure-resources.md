---
title: Häälestage Azure'i ressursid elektrooniliseks arveldamiseks
description: Selles teemas antakse ülevaade protsessist ressursside seadistamiseks Microsoft Azure elektroonilise arvelduse jaoks.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb1fcddce1054aebf9ef70ba69eb7aca98093cbe
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371888"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Häälestage Azure'i ressursid elektrooniliseks arveldamiseks

[!include [banner](../includes/banner.md)]

Elektroonilise arvelduse ressursside Microsoft Azure seadistamise protsessil on kolm sammu. Esimesed kaks etappi "Azure'i võtme vault loomine Azure'i portaalis" ja "Azure'i ladustamiskonto loomine Azure'i portaalis" on kohustuslikud. Kolmas etapp "Ühenduse konfigureerimine SharePoint " on valikuline.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Looge Azure'i võtme vault Azure'i portaalis

Looge oma Azure'i kordustellimuses võtme võti. Soovitame luua elektrooniliseks arveldamiseks eraldi võtme hoidla ning et te ei kombineeriks saladusi muude rakendustega. Looge nii palju saladusi ja serte, kui vajate oma elektrooniliste dokumentide stsenaariumite puhul. Peate looma vähemalt ühe saladuse, et salvestada järgmises sammus teie looge Azure'i ladustamiskonto saS-i jagatud pääsu allkiri.

Teavet selle sammu lõpuleviimise kohta vt Azure'i [võtme vaulti loomine Azure'i portaalis](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure'i ladustamiskonto loomine Azure'i portaalis

Teie omate kõiki elektroonilisi dokumente ja faile, mille on loonud elektroonilise arvelduse teenus või sisestage teenus. Need dokumendid ja failid salvestatakse Azure'i kordustellimuses lootatavale Azure'i ladustamiskontole. Teenus pääseb teie ladustamiskontole juurde, kasutades SAS-i luba, mis võetakse teie võtme vault-saladustest.

Teavet selle sammu lõpuleviimise kohta vt Azure'i [ladustamiskonto loomine Azure'i portaalis](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>SharePoint Ühenduse konfigureerimine

Mõne stsenaariumi korral võib juhtuda, et peate salvestama elektrooniliste failide kausta ja SharePoint need alla laadima SharePoint. Kindlustamaks, et elektroonilise arveldamise teenusel on juurdepääs teie kaustadele SharePoint, konfigureerige juurdepääs.SharePoint

Teavet selle toimingu lõpuleviimise kohta vt ühenduse [SharePoint konfigureerimine](e-invoicing-create-sharepoint-connection.md).
