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
ms.openlocfilehash: 463a66002ec7a6536c9ff829f9ea2c3734138eae
ms.sourcegitcommit: 6221a25f81aa83ab335de7cb6b6c3014dbec0116
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177144"
---
# <a name="get-started-with-global-inventory-accounting"></a>Global Inventory Accounting kasutamise alustamine

[!include [banner](../includes/banner.md)]

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

## <a name="install-or-update-the-add-in-and-solution"></a><a name="install"></a> Lisandmooduli ja lahenduse installimine või värskendamine

Kasutage järgmist protseduuri globaalse laoarvestuse lisandmooduli ja lahenduse installimiseks või värskendamiseks. Protseduuri osa, mida järgida, sõltub sellest, kas installite esmakordselt või peate olemasoleva installi lahendust värskendama.

- Kui te pole kunagi lisandmoodulit installinud, järgige nii lisandmooduli kui ka lahenduse installimiseks täielikku protseduuri.
- Kui kasutate juba globaalset varude arvestust [Power Platform](https://admin.powerplatform.microsoft.com), kuid peate lahenduse halduskeskuses värskendama, siis tehke ainult sammu 6 ja jätke kõik muud sammud vahele.

Lisandmooduli ja lahenduse installimiseks või värskendamiseks:

1. Logige teenusesse [LCS](https://lcs.dynamics.com/Logon/Index) sisse.
1. Avage LCS-i keskkond, kuhu soovite teenuse lisada.
1. Avage **Kõik üksikasjad**.
1. Minge integratsiooni **Power Platform ja** valige **seadistus**.
1. Märkige ruut **Power Platform platvormi keskkonna seadistus** dialoogiboksis ja valige seejärel **Seadistamine**. Tavaliselt võtab seadistus aega 60 kuni 90 minutit.
1. Pärast keskkonna Microsoft Power Platform seadistuse lõpule viimist logige [Power Platform](https://admin.powerplatform.microsoft.com) halduskeskusesse sisse ja seejärel installige või värskendage globaalse laoarvestuse lahendus järgmiste sammude abil.
   1. Valige keskkond, kuhu soovite lahenduse installida või värskendada.
   1. Valige **Dynamics 365 rakendused**.
   1. Valige **installirakendus**.
   1. Valige **Dynamics 365 globaalne laoarvestus**.
   1. Valige **installimiseks** edasi.
1. Kui lahendus on täielikult installitud, minge tagasi LCS-i keskkonda. Valige kiirkaardil **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
1. Valige **Globaalne laoarvestus**.
1. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.
1. Valige **Installi**.
1. Peaksite nägema kiirkaardil **Keskkonna lisandmoodulid**, et Global Inventory Accounting installitakse. Mõne minuti pärast peaks olek *Installimine* muutuma olekuks *Installitud*. (Selle muudatuse nägemiseks võib olla vaja lehte värskendada.) Pärast seda on Global Inventory Accounting kasutamiseks valmis.

Kui teie installi vaikekeel ei Dataverse ole inglise keel, järgige neid samme.

1. Avage **Täpsemad seadistused \>Administreerimine \> Keeled**.
1. Valige *Inglise keel* (*LanguageCode=1033*) ja valige **Rakenda**.

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
