---
title: Luba koondandmete otsing maksuarvestuse konfiguratsiooni jaoks
description: See artikkel selgitab, kuidas seadistada ja lubada maksu arvutamise koondandmete otsingufunktsioone.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181120"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Luba koondandmete otsing maksuarvestuse konfiguratsiooni jaoks 

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada ja lubada maksu arvutamise koondandmete otsingufunktsioone. Ripploendit saab kasutada maksuarvutuse **konfiguratsioonis** selliste väljade väärtused nagu Juriidiline isik, **Hankija konto**, **Kaubakood** ja **Tarne tähtaeg**. Need väärtused tulevad ühendatud Microsoft Dynamics 365 finantskeskkonnast andmeallika Microsoft Dataverse abil.

> [!NOTE] 
> Maksu arvutamise koondandmete otsingu funktsioon on valikuline funktsioon. Kui keelate maksuteenuse andmeallikate **Dataverse tugifunktsiooni regulatiivses konfiguratsiooniteenuses** (RCS), võite järgmised sammud vahele jätta. Sel juhul ei ole aga ripploend maksuarvestuse konfiguratsioonis saadaval.

Maksuarvestuse funktsiooniversiooni konfiguratsiooni ripploendi lubamiseks viige lõpule järgmised sammud.

1. [Lubage Microsoft Power Platform integreerimine ja avage Dataverse keskkond.](#enable)
2. [Installige finantsid ja toimingute virtuaalüksused.](#install)
3. [Registreerige Azure Active Directory (Azure AD) avaldus.](#register)
4. [Andke rakenduse õigused finantside ja toimingute rakendustes.](#grant)
5. [Konfigureerige virtuaalüksuse andmeallikas.](#configure)
6. [Lubage Dataverse virtuaalsed üksused.](#virtual)
7. [Seadistage ühendatud rakendus maksu arvutamiseks.](#set-up)
8. [Importige ja seadistage mudeli Dataverse vastendamise konfiguratsioon.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a> Luba Microsoft Power Platform integreerimine ja ava Dataverse keskkond

Finantside ja toimingute rakenduste Microsoft Power Platform integreerimist saab lubada, Microsoft Dynamics kui loote elutsükli teenustes (LCS) uue finantside ja toimingute rakenduste keskkonna. Lisateavet vt teemast [Microsoft Power Platform ingegratsioon - lisandmooduli ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kui olete lõpetanud, kuvatakse keskkonna Microsoft Power Platform nimi integratsiooni **Power Platform jaotises**.

1. LCS-i finants- ja tegevuskeskkonnas **Power Platform** **leiate** integratsioonijaost üles ja tehke märkust lingitud keskkonna nime väärtuse kohta.

    [![Keskkonna nime väärtus](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. [Power Platform Halduskeskuse vahekaardil](https://admin.powerplatform.microsoft.com/environments) Keskkonnad **valige keskkond**, mis vastab keskkonna nime väärtusele, **mille** kohta olete märkuse teinud.
3. **Lehel Üksikasjad** leiate keskkonna **URL-i** Dataverse väärtuse. Tehke sellest väärtusest märkus, sest teil on seda vaja sammus [7. Seadistage ühendatud rakendus maksu arvutamiseks](#set-up).
4. Valides väärtuse Keskkonna URL, Dataverse veenduge, et saate brauseris **keskkonna avada**.

    [![Dataverse keskkonnaleht.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Hoidke keskkond Dataverse brauseris avatuna. Seda vajate sammus [5. Konfigureerige virtuaalüksuse andmeallikas](#configure).

Lisateavet vt Luba [Microsoft Power Platform integreerimine](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a> Finantside ja toimingute virtuaalüksuste installimine

Finantside Dataverse ja toimingute virtuaalüksuste lahendus tuleb installida virtuaalüksuse Microsoft AppSource lahendusest.

1. Leidke AppSource finantside ja [toimingute virtuaalne üksus](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Valige **hangi see kohe**.
3. **Väljale Keskkonna valimine sisestage** keskkonna nime **väärtus**, mille olete varemmärkuse teinud.
4. Märkige ruudud ja seejärel valige käsk **Installi**.

Kui installimine on lõpule viidud, leiate finantside ja toimingute virtuaalüksuse rakenduse **halduskeskusest**, [Power Platform](https://admin.powerplatform.microsoft.com/)**ressursside** Dynamics 365 rakenduste all.\>**·**

Lisateavet vt virtuaalüksuse [lahenduse saamine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Azure AD Avalduse registreerimine

Peate registreerima rakenduse Azure AD finantside ja toimingute rakendustega samal rentnikul, et neid saaks kutsuda Dataverse.

1. [Avage Azure'i](https://portal.azure.com) portaalis rakenduse **Azure Active Directory\> registreerimised**.
2. Valige **uus** registreerimine ja sisestage järgmine teave:

    - **Nimi** : sisestage kordumatu nimi.
    - **Konto tüüp** – sisestage mis **tahes Azure AD kaust** (üksik rentnik või mitme rentnik).
    - **Ümbersuunamise URI** – jätke see väli tühjaks.

3. Valige suvand **Registreeri**.
4. Märkige välja **Rakenduse (klient) ID** väärtus üles, seda läheb hiljem vaja.

    [![Azure AD Rakenduse (kliendi) ID väärtus.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Saate luua rakenduse sümmeetrilise võtme.
6. Uues rakenduses valige tunnistused **ja saladused**.
7. Valige **Uus kliendi saladus**.
8. Sisestage kirjeldus, valige aegumiskuupäev ja seejärel valige **salvestamine**. Luuakse ja näidatakse võtit. Saate väärtuse hilisemaks kasutamiseks kopeerida.

Lisateavet vt teemast Rakenduse [Azure AD registreerimine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a> Rakenduse õiguste andmine finantside ja toimingute rakendustes

Dataverse rakendusse Azure AD, mille lõite finantside ja toimingute rakenduste kutsumiseks. Seetõttu peavad finantside ja toimingute rakendused rakendust usaldama ning olema seostatud sobiva õigusega kasutajakontoga. Finantside ja toimingute rakendustes peate looma spetsiaalse teenuse kasutaja, tal on õigused **ainult** virtuaalüksuse funktsioonidele. Sellel teenuse kasutajal ei tohi olla muid õigusi. Pärast selle sammu lõpule viimist saab iga rakendus, mis on loodud rakenduse saladus, Azure AD kutsuda finantside ja toimingute rakenduste keskkonda ning pääseda juurde virtuaalüksuse funktsioonidele.

1. Minge oma keskkonnas Süsteemihalduse **kasutajate** \> **·** \> **süsteemi**.
2. Valige **uue** kasutaja lisamiseks uus ja sisestage järgmine teave:

    - **Kasutaja ID** – sisestage **dataverseintegration või** muu väärtus.
    - **Kasutajanimi** : sisestage **dataverse integratsioon** või muu väärtus.
    - **Pakkuja**: seadke see väli nonAAD-le **·**.
    - **E-kiri** : sisestage **andmetepöördumine** või muu väärtus. (Väärtus ei pea olema kehtiv meiliaadress.)

3. Määrake kasutajale **CDS-i virtuaalüksuse** rakenduse turberoll.
4. Eemaldage kõik teised rollid, k.a **süsteemi kasutaja**.
5. Minge registreerimiseks **süsteemihalduse** \> **·** \> **Azure Active Directory seadistuse** rakendustesse.Dataverse 
6. Lisage rida ja seejärel sisestage **väljale Kliendi ID rakenduse (kliendi) ID** **väärtus,** mille olete varemmärkuse teinud.
7. Väljale **Nimi** sisestage nimi. Näiteks sisestage integratsioon **Dataverse**.
8. Sisestage **väljale Kasutaja ID varem loodud kasutaja ID**.

Lisateavet vt Rakenduse õiguste andmine [finantside ja toimingute rakendustes](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Virtuaalüksuse andmeallika konfigureerimine

Ühenduse loomiseks Dataverse peate sisestama finantside ja toimingute rakenduse eksemplari.

1. Keskkond Dataverse peab teie brauseris siiski olema avatud sammust [1. Lubage Microsoft Power Platform integreerimine ja avage Dataverse keskkond](#enable). Valige sätete nupp (käigu sümbol) ülemisel paremal ja seejärel valige Täpsemad **sätted**.

    [![Täpsemate sätete avamine Dataverse keskkonnas.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. **Valige rippmenüü** sätted suvand **Haldus**.

    [![Administratsioon.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Valige **virtuaalüksuse andmeallikad**.

    [![Virtuaalüksuse andmeallikad.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Valige andmeallikas nimega Finantsid **ja Toimingud**.

    [![Finantside ja toimingute andmeallikas.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Sisestage varasemate sammude põhjal järgmine teave:

    - **Siht-URL** – sisestage URL, kuhu pääsete juurde finantside ja toimingute rakendustele.
    - **OAuthi URL** – sisestage `https://login.windows.net/`.
    - **Rentniku ID** – määrake oma rentnik. See väärtus võib olla teie ettevõtte meiliaadressi domeeninimi (nt contoso.com).
    - **AAD rakenduse ID** – sisestage rakenduse **(kliendi) ID väärtus**, mis loodi varem.
    - **AAD rakenduse saladus** – sisestage varem loodud saladus.
    - **AAD ressurss** – sisestage **00000015-0000-0000-c000-000000000000**. See väärtus on rakendus Azure AD, mis esindab finantside ja toimingute rakendusi. See peaks alati olema sama väärtus.

6. Salvestage muudatused.
7. Sulgege leht, et naasta **administreerimislehele**, kus alustate sammu [6. Lubage Dataverse virtuaalsed üksused](#virtual).

    [![Üksuse sulgemine redigeerimiseks.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Lisateavet vt virtuaalüksuse [andmeallika konfigureerimine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a> Luba Dataverse virtuaalsed üksused

Finantside ja toimingute rakenduste virtuaalüksuste **nähtavus** peab olema seatud väärtusele Jah, enne kui maksuarvestuse konfiguratsioon neid tarbib.

> [!NOTE]
> Võite selle sammu vahele jätta, lubades maksuarvestusega seotud virtuaalsed üksused ühe klõpsuga [sammus 8. Seadistage ühendatud rakendus maksu arvutamiseks](#import). Soovitame siiski käsitsi lubada vähemalt ühe virtuaalse üksuse, näitamaks, et finantside ja toimingute rakenduste vaheline seos Dataverse on hästi loodud.

1. Valige oma Dataverse keskkonnas lehe Administreerimine **ülemises** parempoolses nurgas filtrinupp (lehtri sümbol).

    [![Filtri nupp.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Valige akna **Täpsem otsing väljal** Otsi, **suvand** Saadaolevad finantside ja toimingute **üksused**.
3. Lisage järgmine reegel: Nimi **·** – Sisaldab **·** – **CompanyInfoEntity**. Seejärel valige **tulemused**.

    [![Täpsema otsimisaken.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Valige **otsingutulemustes CompanyInfoEntity**, märkige ruut **Nähtav** ja seejärel valige **salvestamine**.

    [![Üksuse nähtavuse seadmine.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Korrake eelnevaid samme järgmiste üksuste puhul, millele on viidatud maksuarvestuse konfiguratsioonis:

    - EttevõteInfoÜksus
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogistikaAadressRiikRegioonTõlgeÜksus
    - LogistikaAadressOsariikÜksus
    - OstaHankedTasuCDSÜksus
    - MüükTasuCDSÜksus
    - TaxGroupEntity
    - MaksKaupGruppPäisÜksus
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Üksuse esimesed 5000 Dataverse kirjet saab tuua ja teha kättesaadavaks maksuarvutuse konfiguratsiooni ripploendis.

Lisateavet vt [Microsoft Dataverse virtuaalsete olemite lubamine](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a> Ühendatud maksuarvutuse rakenduse häälestamine

1. RCS-is avage funktsioonihalduse **tööruum** ja lubage järgmised funktsioonid:

    - elektroonilise aruandluse Dataverse andmeallikate tugi
    - Maksuteenuse Dataverse'i andmeallikate tugi
    - Globaliseerimisfunktsioonid

2. Minge elektroonilise **aruandluse** jaotisse ja seejärel valige jaotises **Seotud lingid** suvand **Ühendatud rakendused**.

    [![Ühendatud avaldused.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. Kirje **lisamiseks** valige väärtus Uus ja sisestage järgmine teave.

    - **Nimi** - sisesta nimi.
    - **Tüüp** : vali **Dataverse**.
    - **Rakendus** : sisestage Dataverse oma keskkonna **URL-i** väärtus, mille tegite [sammus 1 märkuse. Lubage Microsoft Power Platform integreerimine ja avage keskkond Dataverse](#enable).
    - **Rentnik** – sisestage oma rentnik.
    - **Kohandatud URL** – sisestage oma Dataverse URL ja lisage **sellele /api/data/v9.1**.

4. Valige **kontrolli ühendust** ja seejärel kuvatavas dialoogiboksis valige Klõpsake siin, **et luua ühendus valitud kaugrakendusega**.

    [![Ühenduse kontrollimine.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. Veenduge, et saate "Edu". Teade, mis näitab, et ühendus on edukalt loodud.

    [![Eduteade.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a> Mudeli vastendamise konfiguratsiooni importimine Dataverse ja häälestamine

Microsoft pakub vaikemudeli vastendamise konfiguratsioone üksuste jaoks, mis on finantside ja toimingute rakendustest maksuarvutusse.

1. Minge RCS-i elektroonilisse **aruandlusse**.
2. Microsofti pakkuja **paani** jaotises Konfiguratsioonipakkujad **valige** hoidlad **·**.

    [![Hoidlates.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Valige globaalse **konfiguratsiooni hoidla** kirje ja seejärel valige **Avatud**.
4. Maksuandmete **mudeli maksuarvutuse** \> **andmemudeli all** valige mudeli vastendamise **Dataverse** konfiguratsioon.
5. Valige kiirkaardil **Versioonid** versioon, mis vastab teie finantside ja toimingute rakenduste versioonile, ja seejärel valige suvand **Impordi**.

    [![Mudeli vastendamise Dataverse konfiguratsiooni importimine](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Mudeli **Dataverse vastendamise** konfiguratsioon kehtib ainult selle suurima imporditud versiooni puhul. Seetõttu ei tohiks importida mudeli **Dataverse** vastendamise konfiguratsiooni versiooni, mis on kõrgem kui maksuarvutuse konfiguratsiooni versioon, mida plaanite juurutada. Näiteks kui plaanite rakendada maksuarvestuse 40.50.225 versiooni, peaksite importima ainult mudeli vastendamise konfiguratsiooni versiooni 40.50.13 **Dataverse**. Te ei tohiks importida versiooni 40.54.14. Vastasel juhul on konfiguratsioonis andmemudeli lahknevus.

6. Minge tagasi elektroonilise aruandluse **juurde** ja valige maksukonfiguratsioonide **paan**.
7. Valige imporditud mudelivastenduse **Dataverse** konfiguratsioon ja seejärel käsk **Redigeeri**.
8. Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.
9. Valige **väljal Ühendatud** rakendus ühendatud rakendus, mille seadistate sammus [7. Seadistage ühendatud rakendus maksu arvutamiseks](#set-up).
10. Seadistage virtuaalse **tabeli nähtavuse valik** Jah **,** et seada kõik maksuarvestusega seotud virtuaalsed üksused nähtavaks.

Olete nüüd lõpule viinud koondandmete otsingufunktsiooni seadistuse. Dynamics 365 Finance'i **väljade,** **nagu juriidiline isik,** **hankija konto, kaubakood ja tarne tähtaeg,** **ripploend lubatakse nüüd maksuarvestuse funktsiooni versiooni seadistuses.** **·**

[![Juriidilise isiku ripploend.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
