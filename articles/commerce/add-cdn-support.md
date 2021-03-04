---
title: Sisuedastusvõrgu (CDN) toe lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0e888fca4a5401f1df6e61b10358489846ad4b0e
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517204"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Sisuedastusvõrgu (CDN) toe lisamine


[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).

## <a name="overview"></a>Ülevaade

Kui seadistate e-kaubanduse keskkonda rakenduses Dynamics 365 Commerce, siis saate konfigureerida selle töötama koos oma CDN-i teenusega. 

Teie kohandatud domeeni saab lubada e-kaubanduse keskkonna ettevalmistamisprotsessi käigus. Teise võimalusena saate kasutada teenusetaotlust, et seadistada see pärast ettevalmistusprotsessi lõpetamist. E-kaubanduse keskkonna ettevalmistamisprotsess loob keskkonnaga seotud hostinime. Sellel hostinimel on järgmine vorming, kus \<*e-commerce-tenant-name*\> on teie keskkonna nimi.

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Ettevalmistusprotsessi käigus loodud hostinimi või lõpp-punkt toetab turvasoklite kihi (SSL) serti ainult \*.commerce.dynamics.com-i jaoks. See ei toeta kohandatud domeenide SSL-i. Seega peate kohandatud domeenide SSL-i määrama oma CDN-is ja edastama liikluse CDN-ist kaubanduse loodud hostinimele või lõpp-punktile. 

Lisaks teenindatakse lõpp-punktist Commerce’i *staatika* (JavaScripti või kaskaadlaadistiku \[CSS\] faile), mille Commerce genereeris (\*.commerce.dynamics.com). Staatika saab vahemällu salvestada ainult siis, kui Commerce’i genereeritud hostinimi või lõpp-punkt lisatakse on CDN-i taha.

## <a name="set-up-ssl"></a>SSL-i seadistamine

SSL-i seadistamise ja staatika vahemällu salvestamise tagamiseks peate konfigureerima oma CDN-i nii, et see on seostatud teie keskkonna jaoks loodud Commerce’i nimega. Staatika jaoks peate salvestama vahemällu ka järgmise mustri: 

/\_msdyn365/\_scnr/\*

Pärast antud kohandatud domeeniga Commerce’i keskkonna ettevalmistamist või pärast oma keskkonnale teenusetaotlust kasutades kohandatud domeeni sisestamist, suunake oma kohandatud domeen Commerce’i loodud hostinimele või lõpp-punktile.

Nagu eelnevalt mainitud, toetab loodud hostinimi või lõpp-punkt SSL-i serti ainult \*.commerce.dynamics.com-i jaoks. See ei toeta kohandatud domeenide SSL-i.

## <a name="cdn-services"></a>CDN-teenused

Commerce’i keskkonnaga saab kasutada mis tahes CDN-i teenust. Järgmisena on toodud kaks näidet.

- **Microsoft Azure’i sisenemispunkti teenus** – Azure’i CDN-i lahendus. Lisateavet Azure’i sisenemispunkti teenuse kohta vt [Azure’i sisenemispunkti teenuse dokumentatsioon](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai dünaamiline saidi kiirendi** – lisateavet vaadake teemast [Dünaamiline saidi kiirendi](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN häälestus

CDN-i seadistamise protsess koosneb järgnevatest üldistest etappidest.

1. Lisage eesserveri host.
1. Konfigureerige tagaserverite kaust.
1. Seadistage marsruudivalik ja vahemällu salvestamine.

### <a name="add-a-front-end-host"></a>Eesserveri hosti lisamine

Kasutada võib mis tahes CDN-i teenust, kuid näiteks selles teemas kasutatakse Azure’i sisenemispunkti teenust. 

Teavet Azure’i sisenemispunkti teenuse seadistamise kohta vaadake teemast [Lühijuhend: suure saadavusega globaalse veebirakenduse jaoks sisenemispunkti loomine](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Azure’i sisenemispunkti teenuses tagaserverite kausta konfigureerimine

Azure’i sisenemispunkti teenuses tagaserverite kausta konfigureerimiseks järgige järgmisi etappe.

1. Lisage tagaserverite kaustale kohandatud hostiks **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**, millel on tühi tagaserveri hosti päis.
1. Suvandis **Koormusetasandus** säilitage vaikeväärtused.

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiboks **Lisa tagaserver**, millesse on sisestatud tagaserveri hosti nimi.

![Tagaserveri dialoogiakna lisamine](./media/CDN_BackendPool.png)

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiboks **Lisa tagaserverite kaust** koos koormuse tasakaalustamise vaikeväärtustega.

![Jätkuv tagaserveri dialoogiboksi lisamine](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Azure’i sisenemispunkti teenuse reeglite seadistamine

Azure’i sisenemispunkti teenuse marsruudivaliku reegli seadistamiseks toimige järgmiselt.

1. Lisage marsruudivaliku reegel.
1. Väljale **Nimi** sisestage suvand **vaikimisi**.
1. Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.
1. Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.
1. Jaotises **Vastavusse viidavad mustrid** sisestage ülemisele väljale **/\** _.
1. Jaotises _**Protsessi üksikasjad** määrake suvandi **Protsessi tüüp** väärtuseks **Edasi**.
1. Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.
1. Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**. 
1. Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.
1. Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.

Azure’i sisenemispunkti teenuse vahemällu salvestamise reegli seadistamiseks toimige järgmiselt.

1. Lisage vahemällu salvestamise reegel.
1. Väljale **Nimi** sisestage suvand **staatika**.
1. Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.
1. Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.
1. Jaotises **Vastavusse viidavad mustrid** sisestage ülemisele väljale **/\_msdyn365/\_scnr/\** _.
1. Jaotises _**Protsessi üksikasjad** määrake suvandi **Protsessi tüüp** väärtuseks **Edasi**.
1. Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.
1. Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.
1. Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.
1. Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.
1. Väljal **Päringustringi vahemällu salvestamise käitumine** valige suvand **Salvesta vahemällu kõik ainulaadsed URL-id**.
1. Väljagrupis **Dünaamiline tihendamine** valige suvand **Luba**.

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa reegel**.

![Reegli dialoogiakna lisamine](./media/CDN_CachingRule.png)

> [!WARNING]
> Kui domeen, mida te kasutama hakkate, on juba aktiivne ja kasutusvalmis, looge teenuse [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) paanil **Tugi** tugiteenusepilet, et saada järgmiste sammude jaoks abi. Lisateavet leiate teemast [Finance and Operationsi rakenduste või teenuse Lifecycle Services (LCS) tugi](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Kui teie domeen on uus ja ei ole olemasolev kasutatav domeen, saate lisada oma kohandatud domeeni Azure'i sisenemispunkti teenuse konfiguratsiooni. See võimaldab suunata veebiliiklust teie saidile Azure'i sisenemispunkti teenuse kaudu. Kohandatud domeeni lisamiseks (nt `www.fabrikam.com`) peate konfigureerima domeeni kanoonilise nime (CNAME).

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Konfiguratsioon CNAME**.

![Dialoogiaken Konfiguratsioon CNAME](./media/CNAME_Configuration.png)

Saate kasutada Azure’i sisenemispunkti teenust serdi haldamiseks või saate kasutada oma kohandatud domeeni serti.

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Kohandatud domeeni HTTPS**.

![Dialoogiaken Kohandatud domeeni HTTPS](./media/Custom_Domain_HTTPS.png)

Üksikasjalikku teavet kohandatud domeeni lisamise kohta oma Azure'i sisenemispunkti leiate teemast [Kohandatud domeeni lisamine sisenemispunkti](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).

Teie CDN peaks nüüd olema õigesti konfigureeritud, et seda saaks teie Commerce’i saidiga kasutada.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]