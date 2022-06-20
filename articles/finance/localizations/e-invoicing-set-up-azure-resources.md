---
title: Azure'i ressursside häälestamine elektroonilise arvelduse jaoks
description: See artikkel annab ülevaate protsessist ressursside seadistamiseks Microsoft Azure elektroonilise arvelduse jaoks.
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
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907725"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Azure'i ressursside häälestamine elektroonilise arvelduse jaoks

[!include [banner](../includes/banner.md)]

Elektroonilise arvelduse ressursside Microsoft Azure seadistamise protsessil on kolm sammu. Esimesed kaks etappi "Azure'i võtme vault loomine Azure'i portaalis" ja "Azure'i ladustamiskonto loomine Azure'i portaalis" on kohustuslikud. Kolmas etapp "Ühenduse konfigureerimine SharePoint " on valikuline.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Looge Azure'i võtme vault Azure'i portaalis

Looge oma Azure'i kordustellimuses võtme võti. Soovitame luua elektrooniliseks arveldamiseks eraldi võtme hoidla ning et te ei kombineeriks saladusi muude rakendustega. Looge nii palju saladusi ja serte, kui vajate oma elektrooniliste dokumentide stsenaariumite puhul. Peate looma vähemalt ühe saladuse, et salvestada järgmises sammus teie looge Azure'i ladustamiskonto saS-i jagatud pääsu allkiri.

Teavet selle sammu lõpuleviimise kohta vt Azure'i [võtme vaulti loomine Azure'i portaalis](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure'i salvestusruumi konto loomine Azure'i portaalis

Teie omate kõiki elektroonilisi dokumente ja faile, mille on loonud elektroonilise arvelduse teenus või sisestage teenus. Need dokumendid ja failid salvestatakse Azure'i kordustellimuses lootatavale Azure'i ladustamiskontole. Teenus pääseb teie ladustamiskontole juurde, kasutades SAS-i luba, mis võetakse teie võtme vault-saladustest.

Teavet selle sammu lõpuleviimise kohta vt Azure'i [ladustamiskonto loomine Azure'i portaalis](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>SharePointi ühenduse konfigureerimine

Mõne stsenaariumi korral võib juhtuda, et peate salvestama elektrooniliste failide kausta ja SharePoint need alla laadima SharePoint. Kindlustamaks, et elektroonilise arveldamise teenusel on juurdepääs teie kaustadele SharePoint, konfigureerige juurdepääs.SharePoint

Teavet selle toimingu lõpuleviimise kohta vt ühenduse [SharePoint konfigureerimine](e-invoicing-create-sharepoint-connection.md).
