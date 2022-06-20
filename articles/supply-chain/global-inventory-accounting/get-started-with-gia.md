---
title: Global Inventory Accounting kasutamise alustamine
description: See artikkel kirjeldab, kuidas käivitada globaalse varude raamatupidamisega.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 493e0be8ab56abc2a3253876107b7f4fefabf4ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891085"
---
# <a name="get-started-with-global-inventory-accounting"></a>Global Inventory Accounting kasutamise alustamine

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Global Inventory Accounting võimaldab teil teha mitut laoarvestust teie seadistatud Global Inventory Accounting pearaamatutes. Te seostate iga Global Inventory Accounting pearaamatu *reegliga*. Reegel on järgmist tüüpi raamatupidamispoliitikate kogumik.

- Kuluobjekt
- Sisendi mõõtmise alus
- Kuluvoo eeldus
- Kuluelement

> [!NOTE]
> Isegi kui olete Global Inventory Accounting laoarvestuse sisse lülitanud, saate jätkuvalt samamoodi Microsoft Dynamics 365 Supply Chain Managementis laoarvestust teha.

Global Inventory Accounting on lisandmoodul. Selle funktsioonide kättesaadavaks tegemiseks peate selle installima teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu. Saate valida, kas hinnata seda testimiskeskkonnas enne selle sisselülitamist töökeskkondades.

Global Inventory Accounting laoarvestus ei toeta praegu kõiki Supply Chain Management integreeritud kuluhalduse funktsioone. Seega on oluline, et hindaksite, kas hetkel saadaolev funktsioonide komplekt vastab teie nõuetele.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a> Kuidas saada globaalse varude raamatupidamise lisandmoodulit

> [!IMPORTANT]
> Global Inventory Accounting laoarvestuse kasutamiseks peab teil olema LCS-iga lubatud kõrge saadavuskeskkond (mitte OneBoxi keskkond). Lisaks peate käitama Supply Chain Management versiooni 10.0.19 või uuema.

### <a name="supply-chain-management-version-10019-to-10026"></a>Tarneahela halduse versioon 10.0.19 kuni 10.0.26

Tarneahela haldusversiooni 10.0.19 versioonini 10.0.26 [globaalse varude raamatupidamise installimiseks alustage lisandmooduli installimisest](#install). Seejärel saatke oma LCS-i keskkonna ID ja ettevõtte nimi meiliga globaalse laoarvestuse [töörühmale](mailto:GlobalInvAccount@microsoft.com). Meeskond saadab järeltegevuse meili, mis sisaldab teie globaalse varude arvestuse teenuse lõpp-punktid.

### <a name="supply-chain-management-version-10027-and-later"></a>Tarneahela halduse versioon 10.0.27 ja uuem

Tarneahela halduse versiooni 10.0.27 ja uuema versiooni installimiseks installige [vaid lisandmoodul](#install). Tarneahela halduse nendes versioonides seadistatakse globaalse varude raamatupidamise teenuse lõpp-punktid automaatselt, nii et te ei pea neid käsitsi leidma. Kui lisandmooduli seadistamisel ilmneb probleeme, võtke ühendust globaalse laoarvestuse [töörühmaga](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Litsentsimine

Global Inventory Accounting laoarvestus litsentsitakse koos standardsete laoarvestuse funktsioonidega, mis on saadaval teenuse Supply Chain Management jaoks. Te ei pea Global Inventory Accounting kasutamiseks ostma täiendavat litsentsi.

## <a name="prerequisites"></a>Eeltingimused

### <a name="set-up-microsoft-power-platform-integration"></a>Saate häälestada Microsoft Power Platformi integratsiooni.

Enne lisandfunktsiooni lubamist tuleb teil need sammud Microsoft Power Platform järgmiste sammudega integreerida.

1. Avage LCS-i keskkond, kuhu soovite teenuse lisada.
1. Avage **Kõik üksikasjad**.
1. Valige **Power Platform`i integratsioon** jaotises nupp **Seadistused**.
1. Märkige ruut **Power Platform platvormi keskkonna seadistus** dialoogiboksis ja valige seejärel **Seadistamine**. Tavaliselt võtab seadistus aega 60 kuni 90 minutit.
1. Pärast Microsoft Power Platform keskkonna seadistuse lõpuleviimist kuvatakse lehel teie keskkonna nimi. Lisaks kuvatakse jaotises **Power Platform integratsioon** lause "Power Platform keskkonna seadistus on lõpule viidud." Global Inventory Accounting laoarvestus ei nõua topeltkirjutuse rakendust.

Lisateavet vt teemast [Luba peale keskkonna juurutamist](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

### <a name="set-up-dataverse"></a>Üksuse Dataverse häälestus

Enne Dataverse seadistamist järgmiste sammude abil lisage oma rentnikule Global Inventory Accounting laoarvestuse põhimõtted.

1. Installige Azure AD Windows PowerShell Module v2, nagu on kirjeldatud [Instalige Azure Active Directory PowerShell Graph'ile](/powershell/azure/active-directory/install-adv2).
1. Käivitage järgmine PowerShell käsk.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Järgmisena looge rakenduse kasutajad Global Inventory Accounting laoarvestuse jaoks Dataverse'is järgmiste sammude abil.

1. Avage oma Dataverse keskkonna URL.
1. Minge **Lisaseaded \> Süsteem \> Turvalisus \> Kasutajad** ja looge rakenduse kasutaja. Kasutage **Vaade** välja, et muuta lehe vaade *Rakenduse kasutajad*.
1. Valige suvand **Uus**.
1. Määrake välja **Rakenduse ID** väärtuseks *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Valige **Määra roll** ja seejärel valige *Süsteemiadministraator*. Kui rolli nimi on Kasutaja *Common Data Service, valige* ka see.
1. Korrake eelnevaid samme, kuid seadistage **Rakenduse ID** välja väärtuseks *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Lisateavet leiate teemast [Rakenduse kasutaja loomine](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Kui teie Dataverse installi vaikekeel ei ole inglise keel, järgige neid samme.

1. Avage **Täpsemad seadistused \>Administreerimine \> Keeled**.
1. Valige *Inglise keel* (*LanguageCode=1033*) ja valige **Rakenda**.

## <a name="install-the-add-in"></a><a name="install"></a>Lisandmooduli installimine

Järgige neid samme lisandmooduli installimiseks Global Inventory Accounting laoarvestuse kasutamiseks.

1. Logige teenusesse [LCS](https://lcs.dynamics.com/Logon/Index) sisse.
1. Avage LCS-i keskkond, kuhu soovite teenuse lisada.
1. Avage **Kõik üksikasjad**.
1. Avage **Power Platform integratsioon** ja valige **Seadistamine**.
1. Märkige ruut **Power Platform platvormi keskkonna seadistus** dialoogiboksis ja valige seejärel **Seadistamine**. Tavaliselt võtab seadistus aega 60 kuni 90 minutit.
1. Kui Microsoft Power Platform keskkonna häälestamine on lõpule viidud, valige kiirkaardil **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
1. Valige **Globaalne laoarvestus**.
1. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.
1. Valige **Installi**.
1. Peaksite nägema kiirkaardil **Keskkonna lisandmoodulid**, et Global Inventory Accounting installitakse. Mõne minuti pärast peaks olek *Installimine* muutuma olekuks *Installitud*. (Selle muudatuse nägemiseks võib olla vaja lehte värskendada.) Pärast seda on Global Inventory Accounting kasutamiseks valmis.

## <a name="set-up-the-integration"></a>Integratsiooni seadistamine

Järgige neid samme Global Inventory Accounting ja Supply Chain Management vahelise integreerimise häälestamiseks.

1. Logige sisse rakendusse Supply Chain Management.
1. Avage **Süsteemihaldus \> Funktsioonihaldus**.
1. Valige **Otsi värskendusi**.
1. Vahekaardil Kõik **otsige** funktsiooni nimega (Eelvaade *) globaalset varude arvestust*.
1. Valige **Luba kohe**.
1. Minge **Globaalne laoarvestus \> Seadistamine \>Globaalse laoarvestuse parameetrid \> Integratsiooniparameetrid**.
1. Sõltuvalt sellest, millist tarneahela haldamise versiooni te käitate, tehke üks järgmistest sammudest:
    - **Tarneahela halduse versioon 10.0.19 versioonile 10.0.26**: **·** **sisestage** andmeteenuse lõpp-punkti ja globaalse varude raamatupidamise lõpp-punkti väljadel URL-id, mis saadeti teile globaalse laoarvestuse töörühma kaudu meiliga (vt [ka globaalse varude arvestuse lisandmooduli saamine).](#sign-up)
    - **Tarneahela halduse versioon 10.0.27** ja uuem: lõpp-punktid ei pea sisestama, seega võite selle sammu vahele jätta.

Global Inventory Accounting laoarvestus on nüüd kasutamiseks valmis.
