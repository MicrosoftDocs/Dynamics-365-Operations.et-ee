---
title: Ladustamisrakenduse installimise ja konfigureerimise ülevaade
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 for Finance and Operations – Ladustamine installimist ja konfigureerimist.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: df0bc9ff2405cc2f370ea777a70e005a1ff338a0
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814946"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Ladustamisrakenduse installimise ja konfigureerimise ülevaade

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Selles teemas kirjeldatakse, kuidas pilvejuurutuse korral konfigureerida ladustamist. Asutusesiseste juurutamiste korral ladustamise konfigureerimise kohta lugege teemat [Kohapealsete juurutuste ladustamine](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Selles teemas kirjeldatakse rakenduse Dynamics 365 for Finance and Operations – Ladustamine installimist ja konfigureerimist.

Rakendus Ladustamine on saadaval Google Play poes ja Windowsi poes. Praeguse Dynamics 365 Supply Chain Managementi puhul pakutakse seda rakendust autonoomse komponendina, mis tähendab isejuurutamist laotoimingute jaoks kasutatavatel seadmetel. Rakenduse kasutamiseks tuleb rakendus igasse seadmesse alla laadida ja konfigureerida see oma Supply Chain Managementi keskkonnaga ühendust looma. See teema kirjeldab, kuidas rakendust oma seadmetesse installida. Samuti kirjeldatakse, kuidas konfigureerida rakendust Supply Chain Managementi keskkonnaga ühendust looma.

## <a name="prerequisites"></a>Eeltingimused
Rakendus on saadaval Androidi ja Windowsi operatsioonisüsteemides. Selle rakenduse kasutamiseks peab teie seadmetesse olema installitud üks järgmistest toetatud operatsioonisüsteemidest. Teil peab olema üks järgmistest toetatud versioonidest. Kasutage järgmises tabelis olevat teavet hindamiseks, kas teie riist- ja tarkvarakeskkond on valmis installimist toetama.

| Platvorm                    | Versioon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (kõik versioonid)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, versioon 1611 <br>- või - <br>Microsoft Dynamics AX-i versioon 7.0/7.0.1 ja Microsoft Dynamics AX-i platvormivärskendus 2 kiirparandusega KB 3210014 |

## <a name="get-the-app"></a>Hangi rakendus
-   Windows (UWP)
     - [Finance and Operations – Ladustamine Windowsi poes](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations – Ladustamine Google Play Store’is](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery on kasutuselt kõrvaldatud, mis tähendab, et rakendust Ladustamine ei saa sealt enam alla laadida.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Veebiteenuse rakenduse loomine Azure Active Directorys
Selleks et rakendus saaks konkreetse Supply Chain Managementi serveriga suhelda, tuleb registreerida veebiteenuse rakendus Azure Active Directorys Supply Chain Managementi rentnikule. Turvalisusega seotud põhjustel on soovitatav luua veebiteenuse rakendus igale kasutatavale seadmele. Veebiteenuse rakenduse loomiseks Azure Active Directorys (Azure AD) tehke järgmist.

1.  Minge brauseris lehele <https://portal.azure.com>.
2.  Sisestage selle kasutaja nimi ja parool, kellel on juurdepääs Azure’i tellimusele.
3.  Klõpsake Azure’i portaalis vasakpoolsel navigeerimispaanil valikut **Azure Active Directory**.

    [![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)

4.  Veenduge, et Active Directory eksemplar on see, mida Supply Chain Management kasutab.
5.  Klõpsake loendis suvandit **Rakenduste registreerimine**. 

    [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)

6.  Klõpsake ülemisel paanil suvandit **Uus registreerimine**. Käivitub **viisard Rakenduse registreerimine**.
7.  Sisestage rakenduse nimi ja valige **Ainult selle organisatsioonikataloogi kontod**. Klõpsake valikut **Registreerimine**.  

    [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)

8.  Avaneb teie uue rakenduse registreerimisaken. 

    [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)

9.  Jätke **rakenduse ID**meelde, te vajate seda hiljem. **Rakenduse ID**-le on hiljem viidatud kui **kliendi ID**.
10. Klõpsake paanil **Haldamine** valikut **Serdid ja saladused**. Klõpsake valikut **Uus kliendi saladus**. 

    [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

11. Looge võti, sisestades jaotises **Paroolid** võtme kirjeldus ja kestus. Klõpsake käsku **Lisa** ja kopeerige võti. Sellele võtmele viidatakse hiljem kui **kliendi saladusele**. 

    [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Supply Chain Managementis kasutajakonto loomine ja konfigureerimine
Selleks et võimaldada Supply Chain Managementil teie Azure AD rakendust kasutada, peate tegema järgmised konfigureerimistoimingud.

1.  Looge laorakenduse kasutaja identimisteabele vastav kasutaja.
    1.  Minge jaotisse **Süsteemihaldus** &gt; **Üldine** &gt; **Kasutajad**.
    2.  Looge uus kasutaja.
    3.  Määrake lao mobiilse seadme kasutaja, nagu on näidatud järgmisel kuvatõmmisel. 
    
        [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Seostage oma Azure Active Directory rakendus laorakenduse kasutajaga.
    1.  Avage Supply Chain Managementis **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
    2.  Looge uus rida.
    3.  Sisestage **Kliendi ID** (mille viimases jaotises hankisite), andke sellele nimi ja valige eelnevalt loodud kasutaja. Soovitame märgistada kõik seadmed, et saaksite sellelt lehelt nende juurdepääsu Supply Chain Managementile hõlpsasti eemaldada, kui need peaksid kaotsi minema. 
    
        [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Rakenduse konfigureerimine
Peate konfigureerima rakenduse seadmel Supply Chain Managementi serveriga Azure AD rakenduse kaudu ühendust looma. Selleks läbige järgmised sammud.

1.  Avage rakenduses **Ühenduse sätted**.
2.  Tühjendage väli **Demorežiim**. <br>

    [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)

3.  Sisestage järgmine teave: 
    + **Azure Active directory kliendi ID** – kliendi ID hangiti sammus 9 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. 
    + **Azure Active directory kliendi saladus** – kliendi saladus hangiti sammus 11 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. 
    + **Azure Active directory ressurss** – Azure AD kausta ressurss kujutab endast Supply Chain Managementi juur-URL-i. 
    
        > [!NOTE]
        > Ärge lõpetage seda välja kaldkriipsuga (/). 

    + **Azure Active directory rentnik** – Azure AD kausta rentnik, mida Supply Chain Managementi serveri puhul kasutatakse: `https://login.windows.net/your-AD-tenant-ID`. Näiteks: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    
        > [!NOTE]
        > Ärge lõpetage seda välja kaldkriipsuga (/). 
    
    + **Ettevõte** – sisestage rakendusse Supply Chain Management juriidiline isik, millega soovite rakenduse ühendada. <br>
    
    [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)

4.  Valige nupp **Tagasi** rakenduse ülemises vasakus nurgas. Rakendus loob nüüd ühenduse teie Supply Chain Managementi serveriga ja kuvatakse laotöötaja sisselogimisekraan.

    [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Teavet rakenduse Ladustamine seadistamise kohta skannima mobiilse seadme kaamera abil vöötkoode, vt teemast [Vöötkoodide skannimine kaameraga rakenduses Dynamics 365 for Finance and Operations – rakendus Ladustamine](scan-bar-codes-using-a-camera.md).

## <a name="remove-access-for-a-device"></a>Seadmelt juurdepääsu äravõtmine
Kaotatud või ohtu sattunud seadme puhul on vaja seadmelt juurdepääs Supply Chain Managementile ära võtta. Järgmised toimingud kirjeldavad juurdepääsu äravõtmise soovituslikku protsessi.

1.  Minge jaotisse **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
2.  Kustutage rida, mis vastab seadmele, millelt soovite juurdepääsu ära võtta. Pidage eemaldatud seadme **kliendi ID** meeles, te vajate seda hiljem.
3.  Logige sisse Azure’i portaali lehel<https://portal.azure.com>.
4.  Klõpsake vasakpoolses menüüs **Active Directory** ikooni ja veenduge, et olete õiges kataloogis.
5.  Klõpsake loendis suvandit **Rakenduste registreerimine** ja seejärel rakendust, mida konfigureerida soovite. Kuvatakse leht **Sätted** konfiguratsiooniteabega.
6.  Veenduge, et rakenduse **kliendi ID** on sama nagu selle jaotise 2. etapis.
7.  Klõpsake ülemisel paanil nuppu **Kustuta**.
8.  Klõpsake kinnitusteates nuppu **Jah**.
