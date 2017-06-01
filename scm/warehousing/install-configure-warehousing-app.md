---
title: Microsoft Dynamics 365 for Operationsi rakenduse Ladustamine installimine ja konfigureerimine
description: Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 for Operationsi rakendust Ladustamine.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Operationsi rakenduse Ladustamine installimine ja konfigureerimine

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 for Operationsi rakendust Ladustamine.

Dynamics 365 for Operations – Ladustamine on Google Play Store’is ja Windowsi poes saadaolev rakendus. Praeguse Microsoft Dynamics 365 for Operationsi puhul pakutakse seda rakendust autonoomse komponendina, mis tähendab isejuurutamist laotoimingute jaoks kasutatavatel seadmetel. Rakenduse kasutamiseks Dynamics 365 for Operationsi keskkonnas tuleb rakendus igasse seadmesse alla laadida ja konfigureerida see oma Dynamics 365 for Operationsi keskkonnaga ühendust looma. See teema kirjeldab, kuidas rakendust oma seadmetesse installida. Samuti kirjeldatakse, kuidas konfigureerida rakendust Dynamics 365 for Operationsi keskkonnaga ühendust looma.

## <a name="prerequisites"></a>Eeltingimused
Rakendus on saadaval Androidi ja Windowsi operatsioonisüsteemides. Selle rakenduse kasutamiseks peab teie seadmetesse olema installitud üks järgmistest toetatud operatsioonisüsteemidest. Samuti peab teil olema üks järgmistest Dynamics 365 for Operationsi toetatud versioonidest. Kasutage järgmises tabelis olevat teavet hindamiseks, kas teie riist- ja tarkvarakeskkond on valmis installimist toetama.

| Platvorm                    | Versioon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (kõik versioonid)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operationsi versioon 1611 -või- Microsoft Dynamics AX-i versioon 7.0/7.0.1 ja Microsoft Dynamics AX-i platvormi värskendus 2 kiirparandusega KB 3210014 |

## <a name="get-the-app"></a>Hangi rakendus
-   Windows (UWP) - [Dynamics 365 for Operations - Ladustamine Windowsi poes](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing Google Play Store’is](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Veebiteenuse rakenduse loomine Active Directorys
Et rakendus saaks konkreetse Dynamics 365 for Operationsi serveriga suhelda, tuleb registreerida veebiteenuse rakendus Azure Active Directorys Dynamics 365 for Operationsi rentnikule. Turvalisusega seotud põhjustel on soovitatav luua veebiteenuse rakendus igale kasutatavale seadmele. Veebiteenuse taotluse loomiseks Azure Active Directorys (Azure AD) tehke järgmist.

1.  Minge brauseris lehele <https://manage.windowsazure.com>.
2.  Sisestage selle kasutaja nimi ja parool, kellel on juurdepääs Azure’i tellimusele.
3.  Klõpsake Azure’i portaalis vasakpoolsel navigeerimispaanil valikut **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Valige ruudustikust Active Directory eksemplar, mida Dynamics 365 for Operations kasutab.
5.  Klõpsake ülemisel tööriistaribal valikut **Rakendused**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klõpsake alumisel paanil valikut **Lisa**. Käivitub viisard **Rakenduse lisamine**.
7.  Sisestage rakendusele nimi ja valige **Veebirakendus ja/või veebi API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Sisestage sisselogimise URL, mis on teie rentnikus olev rakendus, Operationsi juur-URL. Sisselogimise URL-i ei kasutata praegu aktiivselt rakenduse autentimisel, kuid see on kohustuslik väli. Sisestage sama URL rakenduse ID URI väljale. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Minge vahekaardile **Konfigureeri**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Kerige alla, kuni näete jaotist **Teiste rakenduste load**. Klõpsake nuppu **Lisa rakendus**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Valige loendist **Microsoft Dynamics ERP**. Klõpsake nuppu **Lõpeta kontrollimine** lehe paremas nurgas. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Märkige loendis **Õiguste delegeerimine** lõik ruudud. Klõpsake käsku **Salvesta**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Märkige üles järgmine teave.
    -   **Kliendi ID** – Lehel üles kerides kuvatakse teile **Kliendi ID**.
    -   **Võti** – looge jaotises **Võtmed** võti, valides kestuse, ja kopeerige võti. Sellele võtmele viidatakse hiljem kui **kliendi saladusele**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Microsoft Dynamics 365 for Operationsis kasutajakonto loomine ja konfigureerimine
Et võimaldada Dynamics 365 for Operationsil oma Azure AD rakendust kasutada, peate tegema järgmised konfigureerimistoimingud.

1.  Microsoft Dynamics 365 for Operationsi rentnikule uue Azure Active Directory kasutajakonto loomine. Selle kasutajakonto eesmärk on pääseda juurde konkreetsele kohandatud teenusele laorakenduses, mille Dynamics 365 for Operationsi server avab. Pärast selle toimingu tegemist on teil WMDP kasutaja identimisteave, mis koosneb WMDP meiliaadressist ja WMDP paroolist. Põhitoimingud kasutajate lisamiseks Azure AD-sse ja Dynamics 365 for Operationsisse leiate järgmisest õpikust: [Microsoft Dynamics 365 for Operationsi tellimuse registreerimine](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Looge laorakenduse kasutaja identimisteabele vastav Dynamics 365 for Operationsi kasutaja.
    1.  Avage rakenduses Dynamics 365 for Operations **Süsteemihaldus** &gt; **Üldine** &gt; **Kasutajad**.
    2.  Looge uus kasutaja.
    3.  Määrake lao mobiilse seadme kasutaja, nagu on näidatud järgmisel kuvatõmmisel. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Seostage oma Azure Active Directory rakendus laorakenduse kasutajaga.
    1.  Avage rakenduses Dynamics 365 for Operations **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
    2.  Looge uus rida.
    3.  Sisestage **Kliendi ID** (mille viimases jaotises hankisite), andke sellele nimi ja valige eelnevalt loodud kasutaja. Soovitame märgistada kõik seadmed, et saaksite sellelt lehele nende juurdepääsu Dynamics 365 for Operationsile hõlpsasti eemaldada, kui need peaksid kaotsi minema. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Rakenduse konfigureerimine
Peate konfigureerima rakenduse seadmel Dynamics 365 for Operationsi serveriga Azure AD rakenduse kaudu ühendust looma. Selleks läbige järgmised sammud.

1.  Avage rakenduses **Ühenduse sätted**.
2.  Tühjendage väli **Demorežiim**. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Sisestage järgmised andmed: - **Azure Active Directory kliendi ID** - kliendi ID hangiti sammus 13 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. - **Azure Active Directory kliendi saladus** - kliendi saladus hangiti sammus 13 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. - **Azure Active directory ressurss** - Azure AD kausta ressurss kujutab endast Dynamics 365 for Operationsi juur-URL-i. **Märkus**. Ärge lõpetage seda välja kaldkriipsuga (/). - **Azure Active Directory rentnik** - Azure AD kausta rentnik, mida Dynamics 365 for Operationsi serveri puhul kasutatakse: https://login.windows.net/&lt;your-AD-tenant-ID&gt;. Näide: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Märkus**. Ärge lõpetage seda välja kaldkriipsuga (/). - **Ettevõte** - sisestage rakendusse Dynamics 365 for Operations juriidiline isik, millega soovite rakenduse ühendada. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valige nupp **Tagasi** rakenduse ülemises vasakus nurgas. Rakendus loob nüüd ühenduse teie Dynamics 365 for Operationsi serveriga ja kuvatakse laotöötaja sisselogimisekraan. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Seadmelt juurdepääsu äravõtmine
Kaotatud või ohtu sattunud seadme puhul on vaja seadmelt juurdepääs Dynamics 365 for Operationsile ära võtta. Järgmised toimingud kirjeldavad juurdepääsu äravõtmise soovituslikku protsessi.

1.  Avage rakenduses Dynamics 365 for Operations **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
2.  Kustutage rida, mis vastab seadmele, millelt soovite juurdepääsu ära võtta. Märkige üles eemaldatud seadme puhul kasutatud **kliendi ID**.
3.  Logige sisse Azure’i tavaportaali lehel <https://manage.windowsazure.com>.
4.  Klõpsake **Active Directory** ikooni vasakus menüüs ja seejärel soovitud kausta.
5.  Klõpsake ülemises menüüs valikut **Rakendused** ja seejärel rakendust, mida konfigureerida soovite. Avaneb leht **Kiirjuhend**, kus on ühekordse sisselogimise teave ja muu teave konfigureerimise kohta.
6.  Klõpsake vahekaarti **Konfigureeri**, kerige alla ja veenduge, et rakenduse **kliendi ID** oleks sama, mis selle jaotise 2. toimingus.
7.  Klõpsake käsuribal nuppu **Kustuta**.
8.  Klõpsake kinnitusteates nuppu **Jah**.





