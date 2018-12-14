---
title: Microsoft Dynamics 365 for Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine
description: Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 for Finance and Operationsi moodulit Ladustamine.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 0967b10c2037c24c044f38c49b1b998f6771c66b
ms.openlocfilehash: a1f3cb65e370154e8f3f94780ffb5cab223c85f8
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Selles teemas kirjeldatakse, kuidas pilvejuurutuse korral konfigureerida ladustamist. Asutusesiseste juurutamiste korral ladustamise konfigureerimise kohta lugege teemat [Kohapealsete juurutuste ladustamine](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 for Finance and Operationsi moodulit Ladustamine.

Finance and Operations – Ladustamine on Google Play Store’is ja Windowsi poes saadaolev rakendus. Praeguse Finance and Operationsi puhul pakutakse seda rakendust autonoomse komponendina, mis tähendab isejuurutamist laotoimingute jaoks kasutatavatel seadmetel. Rakenduse kasutamiseks Finance and Operationsi keskkonnas tuleb rakendus igasse seadmesse alla laadida ja konfigureerida see oma Finance and Operationsi keskkonnaga ühendust looma. See teema kirjeldab, kuidas rakendust oma seadmetesse installida. Samuti kirjeldatakse, kuidas konfigureerida rakendust Finance and Operationsi keskkonnaga ühendust looma.

## <a name="prerequisites"></a>Eeltingimused
Rakendus on saadaval Androidi ja Windowsi operatsioonisüsteemides. Selle rakenduse kasutamiseks peab teie seadmetesse olema installitud üks järgmistest toetatud operatsioonisüsteemidest. Samuti peab teil olema üks järgmistest Finance and Operationsi toetatud versioonidest. Kasutage järgmises tabelis olevat teavet hindamiseks, kas teie riist- ja tarkvarakeskkond on valmis installimist toetama.

| Platvorm                    | Versioon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (kõik versioonid)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, versioon 1611 <br>- või - <br>Microsoft Dynamics AX-i versioon 7.0/7.0.1 ja Microsoft Dynamics AX-i platvormiuuendus 2 kiirparandusega KB 3210014 |

## <a name="get-the-app"></a>Hangi rakendus
-   Windows (UWP)
     - [Finance and Operations – Ladustamine Windowsi poes](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations – Ladustamine Google Play Store’is](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations – Ladustamine Zebra App Gallerys](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Veebiteenuse rakenduse loomine Azure Active Directorys
Selleks et rakendus saaks konkreetse Finance and Operationsi serveriga suhelda, tuleb registreerida veebiteenuse rakendus Azure Active Directorys Finance and Operationsi rentnikule. Turvalisusega seotud põhjustel on soovitatav luua veebiteenuse rakendus igale kasutatavale seadmele. Veebiteenuse taotluse loomiseks Azure Active Directorys (Azure AD) tehke järgmist.

1.  Minge brauseris lehele <https://portal.azure.com>.
2.  Sisestage selle kasutaja nimi ja parool, kellel on juurdepääs Azure’i tellimusele.
3.  Klõpsake Azure’i portaalis vasakpoolsel navigeerimispaanil valikut **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Veenduge, et Active Directory eksemplar on see, mida Finance and Operations kasutab.
5.  Klõpsake loendis suvandit **Rakenduste registreerimine**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Klõpsake ülemisel paanil suvandit **Uue rakenduse registreerimine**. Käivitub viisard **Rakenduse lisamine**.
7.  Sisestage rakendusele nimi ja tehke valik **Veebirakendus / veebi API**. Sisestage sisselogimise URL, mis on teie veebirakenduse URL. See URL on sama, mis teie juurutuse URL, kuid lõppu on lisatud oauth. Klõpsake käsku **Loo**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Valige loendist uus rakendus. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Jätke **rakenduse ID**meelde, te vajate seda hiljem. **Rakenduse ID**-le on hiljem viidatud kui **kliendi ID**.
10. Klõpsake jaotises **Sätete paan** suvandit **Võtmed**. Looge võti, sisestades jaotises **Paroolid** võtme kirjeldus ja kestus. 
11. Klõpsake käsku **Salvesta** ja kopeerige võti. Sellele võtmele viidatakse hiljem kui **kliendi saladusele**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operationsis kasutajakonto loomine ja konfigureerimine
Et võimaldada Finance and Operationsil oma Azure AD rakendust kasutada, peate tegema järgmised konfigureerimistoimingud.

1.  Looge laorakenduse kasutaja identimisteabele vastav Finance and Operationsi kasutaja.
    1.  Avage Finance and Operationsis **Süsteemihaldus** &gt; **Üldine** &gt; **Kasutajad**.
    2.  Looge uus kasutaja.
    3.  Määrake lao mobiilse seadme kasutaja, nagu on näidatud järgmisel kuvatõmmisel. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Seostage oma Azure Active Directory rakendus laorakenduse kasutajaga.
    1.  Avage rakenduses Finance and Operations **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
    2.  Looge uus rida.
    3.  Sisestage **Kliendi ID** (mille viimases jaotises hankisite), andke sellele nimi ja valige eelnevalt loodud kasutaja. Soovitame märgistada kõik seadmed, et saaksite sellelt lehelt nende juurdepääsu Finance and Operationsile hõlpsasti eemaldada, kui need peaksid kaotsi minema. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Rakenduse konfigureerimine
Peate konfigureerima rakenduse seadmel Finance and Operationsi serveriga Azure AD rakenduse kaudu ühendust looma. Selleks läbige järgmised sammud.

1.  Avage rakenduses **Ühenduse sätted**.
2.  Tühjendage väli **Demorežiim**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Sisestage järgmine teave: 
    + **Azure Active Directory kliendi ID** – kliendi ID hangiti sammus 9 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. 
    + **Azure Active Directory kliendi saladus** – kliendi saladus hangiti sammus 11 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. 
    + **Azure Active Directory ressurss** – Azure AD kausta ressurss kujutab endast Finance and Operationsi juur-URL-i. **Märkus**. Ärge lõpetage seda välja kaldkriipsuga (/). 
    + **Azure Active Directory rentnik** - Azure AD kausta rentnik, mida Finance and Operationsi serveri puhul kasutatakse: `https://login.windows.net/your-AD-tenant-ID`. Näide: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Märkus**. Ärge lõpetage seda välja kaldkriipsuga (/). 
    + **Ettevõte** – sisestage rakendusse Finance and Operations juriidiline isik, millega soovite rakenduse ühendada. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valige nupp **Tagasi** rakenduse ülemises vasakus nurgas. Rakendus loob nüüd ühenduse teie Finance and Operationsi serveriga ja kuvatakse laotöötaja sisselogimisekraan. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Lisateavet selle kohta, kuidas seadistada rakendust Dynamics 365 for Finance and Operations – Ladustamine vöötkoodide skannimiseks mobiilse seadme kaameraga, vt teemast [Vöötkoodide skannimine kaameraga Microsoft Dynamics 365 for Finance and Operationsi moodulis Ladustamine](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Seadmelt juurdepääsu äravõtmine
Kaotatud või ohtu sattunud seadme puhul on vaja seadmelt juurdepääs Finance and Operationsile ära võtta. Järgmised toimingud kirjeldavad juurdepääsu äravõtmise soovituslikku protsessi.

1.  Avage rakenduses Finance and Operations **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
2.  Kustutage rida, mis vastab seadmele, millelt soovite juurdepääsu ära võtta. Pidage eemaldatud seadme **kliendi ID** meeles, te vajate seda hiljem.
3.  Logige sisse Azure’i portaali lehel<https://portal.azure.com>.
4.  Klõpsake vasakpoolses menüüs **Active Directory** ikooni ja veenduge, et olete õiges kataloogis.
5.  Klõpsake loendis suvandit **Rakenduste registreerimine** ja seejärel rakendust, mida konfigureerida soovite. Kuvatakse leht **Sätted** konfiguratsiooniteabega.
6.  Veenduge, et rakenduse **kliendi ID** on sama nagu selle jaotise 2. etapis.
7.  Klõpsake ülemisel paanil nuppu **Kustuta**.
8.  Klõpsake kinnitusteates nuppu **Jah**.

