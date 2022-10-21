---
title: Arve hõivamise lahenduse täpsemad sätted
description: See artikkel annab teavet arve hõivamise lahenduse täpsemate sätete kohta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690977"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Arve hõivamise lahenduse täpsemad sätted

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel annab teavet arve hõivamise lahenduse täpsemate sätete kohta.

## <a name="create-additional-connections-for-channels"></a>Lisaühenduste loomine kanalite jaoks

Erinevate kanalite sissetulevate arvete jälgimiseks peate looma ühendused meili- või failisalvestustega. Peate alguses ühendused registreerima, et anda juurdepääs lahenduses kasutatavatele automatiseeritud voogudele.

Arvete importimiseks kasutatakse järgmisi ühenduse tüüpe:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Arvete importimise kanal kasutab ühendusi täiendavates konfiguratsioonietappides. Enne kui kasutajad saavad luua kindla ühenduse kanali, **peab** administraatori turberoll olema neile antud ja nad peavad looma ühendused.

Ühenduse loomiseks järgige Microsoft Dataverse neid samme.

1. Minge haldussüsteemi **vaikelahendusse \>**.
2. Valige **uus** ja seejärel ühenduse **viide**.
3. **Sisestage nimi** väljale Kuvatav nimi.
4. Valige **Microsoft Dataverse** ühendus.
5. Kui häälestate ühenduse esmakordselt, valige suvand Uus **ühendus**.
6. Kuvatavas dialoogiboksis looge ühendus ja Dataverse seejärel valige käsk **Loo**.
7. Sisestage Dataverse konto ja parool.
8. Pärast kinnitamise läbimist minge ühenduslehele, valige **värskendamis**, valige konto ja seejärel käsk **Loo**.

Meili- või failisalvestusühenduse loomiseks järgige neid samme.

1. **Valige ühenduse loomise** lehe väljal **Ühenduse tüüp** suvand **Office 365 Outlook**.
2. E-posti ühenduse loomiseks saate valida Outlook.com **ühenduseks** **Office 365 Outlooki**. Faili talletusühenduse jaoks saate valida kas või **OneDrive** **SharePoint**.

Olemasolevate ühenduste ülevaatamiseks minge lahenduseobjektide **ühenduse vaikeviidetesse \>\>.** Kanaleid loov kasutaja peaks lisaks kindlatele meili Dataverse - või failisalvestusühendustele olema vähemalt üks ühendus. Uue kanali looja peaks olema ühenduse omanik.
