---
title: Sisuedastusvõrgu (CDN) toe lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001618"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Sisuedastusvõrgu (CDN) toe lisamine


[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).

## <a name="overview"></a>Ülevaade

Rakenduses Dynamics 365 Commerce e-kaubanduse keskkonda seadistades saate konfigureerida selle töötama koos oma CDN-i teenusega. 

Teie kohandatud domeeni saab lubada e-kaubanduse keskkonna ettevalmistamisprotsessi käigus. Teise võimalusena saate kasutada teenusetaotlust, et seadistada see pärast ettevalmistusprotsessi lõpetamist. E-kaubanduse keskkonna ettevalmistamisprotsess loob hostinime, mis on keskkonnaga seotud. Sellel hostinimel on järgmine vorming, kus *e-kaubanduse-rentniku-nimi* on teie keskkonna nimi:

&lt;e-kaubanduse-rentniku-nimi&gt;.commerce.dynamics.com

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
1. Konfigureerige lõppserveri kaust.
1. Seadistage marsruudivalik ja vahemällu salvestamine.

### <a name="add-a-front-end-host"></a>Eesserveri hosti lisamine

Kasutada võib mis tahes CDN-i teenust, kuid näiteks selles teemas kasutatakse Azure’i sisenemispunkti teenust. 

Teavet Azure’i sisenemispunkti teenuse seadistamise kohta vaadake teemast [Lühijuhend: suure saadavusega globaalse veebirakenduse jaoks sisenemispunkti loomine](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Azure’i sisenemispunkti teenuses lõppserveri kausta konfigureerimine

Azure’i sisenemispunkti teenuses lõppserveri kausta konfigureerimiseks järgige järgmisi etappe.

1. Lisage lõppserveri kaustale kohandatud hostiks **&lt;ecom-rentniku-nimi&gt;.commerce.dynamics.com**, millel on tühi lõppserveri hosti päis.
1. Suvandis **Seisundiuuringud** väljal **Tee** sisestage **/keepalive**.
1. Väljale **Intervallid (sekundid)** sisestage **255**.
1. Suvandis **Koormusetasandus** säilitage vaikeväärtused.

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa lõppserveri kaust**.

![Tagaserveri dialoogiakna lisamine](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Azure’i sisenemispunkti teenuse reeglite seadistamine

Azure’i sisenemispunkti teenuse marsruudivaliku reegli seadistamiseks toimige järgmiselt.

1. Lisage marsruudivaliku reegel.
1. Väljale **Nimi** sisestage suvand **vaikimisi**.
1. Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.
1. Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.
1. Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\***.
1. Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.
1. Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.
1. Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**. 
1. Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.
1. Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.

Azure’i sisenemispunkti teenuse vahemällu salvestamise reegli seadistamiseks toimige järgmiselt.

1. Lisage vahemällu salvestamise reegel.
1. Väljale **Nimi** sisestage suvand **staatika**.
1. Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.
1. Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.
1. Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\_msdyn365/\_scnr/\***.
1. Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.
1. Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.
1. Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.
1. Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.
1. Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.
1. Väljal **Päringustringi vahemällu salvestamise käitumine** valige suvand **Salvesta vahemällu kõik ainulaadsed URL-id**.
1. Väljagrupis **Dünaamiline tihendamine** valige suvand **Luba**.

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa reegel**.

![Reegli dialoogiakna lisamine](./media/CDN_CachingRule.png)

Pärast selle algse konfiguratsiooni juurutamist peate lisama Azure’i sisenemispunkti teenuse konfiguratsioonile oma kohandatud domeeni. Kohandatud domeeni lisamiseks (nt `www.fabrikam.com`) peate konfigureerima domeeni kanoonilise nime (CNAME).

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Konfiguratsioon CNAME**.

![Dialoogiaken Konfiguratsioon CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> Kui domeen, mida kasutate, on juba aktiivne ja avaldatud, võtke ühendust toega, et lubada see domeen Azure’i sisenemispunkti teenusega testi seadistamiseks.

Saate kasutada Azure’i sisenemispunkti teenust serdi haldamiseks või saate kasutada oma kohandatud domeeni serti.

Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Kohandatud domeeni HTTPS**.

![Dialoogiaken Kohandatud domeeni HTTPS](./media/Custom_Domain_HTTPS.png)

Teie CDN peaks nüüd olema õigesti konfigureeritud, et seda saaks teie Commerce’i saidiga kasutada.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
