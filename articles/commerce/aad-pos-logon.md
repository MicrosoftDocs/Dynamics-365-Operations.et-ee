---
title: Luba Azure Active Directory kassa sisselogimise autentimine
description: See teema selgitab, kuidas konfigureerida Microsoft Dynamics 365 Commerce'i kassasse (POS) sisselogimise kogemust nii, et see kasutab Azure Active Directory autentimist.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982736"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Luba Azure Active Directory kassa sisselogimise autentimine
[!include [banner](includes/banner.md)]


Paljud kliendid, kes kasutavad Microsoft Dynamics 365 Commerce'i, kasutavad ka teisi Microsoft pilve teenuseid ja võivad Azure Active Directory kasutada (Azure AD) nende teenuste kasutaja mandaadi haldamiseks. Sel juhul võivad kliendid soovida kasutada sama Azure AD kontot kõigis rakendustes. See teema selgitab, kuidas konfigureerida kaubanduse kassasse (POS) sisselogimise kogemust nii, et see kasutab Azure AD autentimist.

## <a name="configure-azure-ad-authentication"></a>Autentimise Azure AD konfigureerimine

Kaupluse Azure AD jaoks kassa sisselogimise autentimise meetodina kättesaadavaks tegemiseks tuleb teil konfigureerida kaupluse funktsionaalsuse profiili sätted ja rakendada need sätted POS klientidele.

Funktsionaalsuse profiili konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Kassa seadistus** \> **Kassaprofiilid** \> **Funktsiooniprofiilid**.
1. Valige muudetava funktsionaalsuse profiil.
1. Muutke FastTab **funktsioonid** jaotises **POS personali sisselogimine** **väärtuseks sisselogimise autentimise meetodi** väljale **personali ID ja parool** **Azure Active Directory**.

Vaikimisi kasutavad kõik funktsionaalsuse profiilid **töötaja ID-d ja parooli** POS-i autentimise meetodina. Seega, kui soovite kasutada Azure AD , peate muutma **sisselogimise autentimise meetodi** välja väärtust. See muudatus mõjutab kõiki jaekaupluseid, mis on valitud funktsiooniprofiiliga ühendatud.

Sätete rakendamiseks kassa klientidele tehke järgmist.

1. Avage **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Jaotusgraafik**.
1. Käivitage **1070** (**Kanali konfiguratsioon**) jaotusgraafik.

> [!NOTE]
> Azure AD autentimine vajab Interneti-ühendust. See ei tööta, kui kassa töötab ühenduseta režiimis.
> 
> Praegu ei toeta funktsioon **Halduri alistamine** Azure AD-d autentimismeetodina. Operaatori ID-d ja parooli nõutakse ka siis, kui Azure AD on konfigureeritud kassa sisselogimise autentimismeetodina.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Konto Azure AD seostamine töötajaga

Enne kui kaupluse töötaja saab kasutada kontot Azure AD, et sisse logida kassa rakendusse, peab konto Azure AD olema seotud selle töötajaga.

Konto Azure AD seostamiseks töötajaga toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus** \> **Palgalised** \> **Töötajad**.
1. Avage töötaja üksikasjade leht.
1. Valige tegumiriba vahekaardil **Kaubandus** grupis **Välisidentiteet** , valige **Olemasoleva identiteedi seostamine**.
1. Dialoogiaknas **Kasuta olemasolevat välisidentiteeti** valige **Otsi kasutades e-posti**, sisestage Azure AD e-posti aadress ja seejärel valige **Otsing**.
1. Valige saadud konto Azure AD ja seejärel valige **OK**.

Täidetakse väljad **Alias**, **UPN** ja **Väline alamidentifikaator** töötaja üksikasjade lehe vahekaardil **Kaubandus** .

> [!NOTE]
> Pärast töötaja kirje uuendamist, näiteks pärast uue Azure AD konto seostamist, parooli muutmist või töövõtja aadressiraamatu uuendamist, soovitatakse käitada jaotusgraafik **1060** (**Personal**), et sünkroonida uusim personaliteave kanaliga. Nii saab kassarakendus tuua õigeid andmeid kasutaja autentimiseks ja autoriseerimise kontrollimiseks.

## <a name="additional-resources"></a>Lisaressursid

[MPOS-i ja pilve kassa laiendatud sisselogimisfunktsiooni häälestus](extended-logon.md)

[Jaemüügi funktsiooniprofiili loomine](retail-functionality-profile.md)

[ Töötaja konfigureerimine](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
