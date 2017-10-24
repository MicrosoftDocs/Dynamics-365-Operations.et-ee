---
title: Microsoft Dynamics 365 for Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine
description: Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 for Finance and Operationsi moodulit Ladustamine.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 31e77b27d4bf95c997817b3a053b33119562adf8
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 for Finance and Operationsi moodulit Ladustamine.

Finance and Operations – Ladustamine on Google Play Store’is ja Windowsi poes saadaolev rakendus. Praeguse Finance and Operationsi puhul pakutakse seda rakendust autonoomse komponendina, mis tähendab isejuurutamist laotoimingute jaoks kasutatavatel seadmetel. Rakenduse kasutamiseks Finance and Operationsi keskkonnas tuleb rakendus igasse seadmesse alla laadida ja konfigureerida see oma Finance and Operationsi keskkonnaga ühendust looma. See teema kirjeldab, kuidas rakendust oma seadmetesse installida. Samuti kirjeldatakse, kuidas konfigureerida rakendust Finance and Operationsi keskkonnaga ühendust looma.

## <a name="prerequisites"></a>Eeltingimused
Rakendus on saadaval Androidi ja Windowsi operatsioonisüsteemides. Selle rakenduse kasutamiseks peab teie seadmetesse olema installitud üks järgmistest toetatud operatsioonisüsteemidest. Samuti peab teil olema üks järgmistest Finance and Operationsi toetatud versioonidest. Kasutage järgmises tabelis olevat teavet hindamiseks, kas teie riist- ja tarkvarakeskkond on valmis installimist toetama.

| Platvorm                    | Versioon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (kõik versioonid)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operationsi versioon 1611 <br>-või- <br>Microsoft Dynamics Dynamics AX-i versioon 7.0/7.0.1 ja Microsoft Dynamics AX-i platvormiuuendus 2 kiirparandusega KB 3210014 |

## <a name="get-the-app"></a>Hangi rakendus
-   Windows (UWP): [Finance and Operations – Ladustamine Windowsi poes](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations – Ladustamine Google Play Store’is](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations – Ladustamine Zebra App Gallerys](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Veebiteenuse rakenduse loomine Active Directorys
Et rakendus saaks konkreetse Finance and Operationsi serveriga suhelda, tuleb registreerida veebiteenuse rakendus Azure Active Directorys Finance and Operationsi rentnikule. Turvalisusega seotud põhjustel on soovitatav luua veebiteenuse rakendus igale kasutatavale seadmele. Veebiteenuse taotluse loomiseks Azure Active Directorys (Azure AD) tehke järgmist.

1.  Minge brauseris lehele <https://manage.windowsazure.com>.
2.  Sisestage selle kasutaja nimi ja parool, kellel on juurdepääs Azure’i tellimusele.
3.  Klõpsake Azure’i portaalis vasakpoolsel navigeerimispaanil valikut **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Valige tabelist Active Directory eksemplar, mida Finance and Operations kasutab.
5.  Klõpsake ülemisel tööriistaribal valikut **Rakendused**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klõpsake alumisel paanil valikut **Lisa**. Käivitub viisard **Rakenduse lisamine**.
7.  Sisestage rakendusele nimi ja valige **Veebirakendus ja/või veebi API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Sisestage sisselogimise URL, mis on teie veebirakenduse URL. See URL on sama, mis teie juurutuse URL, kuid lõppu on lisatud oauth. Sisestage rakenduse ID URI, see väärtus on kohustuslik, kuid pole autentimiseks vajalik. Veenduge, et see rakenduse ID URI oleks URI mudel, nt https://contosooperations/wmapp, kuna teie juurutuse URL-i kasutamine võib põhjustada sisselogimisprobleeme teistes AAD rakendustes (nt Exceli lisandmoodul). [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  Minge vahekaardile **Konfigureeri**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Kerige alla, kuni näete jaotist **Teiste rakenduste load**. Klõpsake nuppu **Lisa rakendus**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Valige loendist **Microsoft Dynamics ERP**. Klõpsake nuppu **Lõpeta kontrollimine** lehe paremas nurgas. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Märkige loendis **Õiguste delegeerimine** lõik ruudud. Klõpsake käsku **Salvesta**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Märkige üles järgmine teave.
    -   **Kliendi ID** – Lehel üles kerides kuvatakse teile **Kliendi ID**.
    -   **Võti** – looge jaotises **Võtmed** võti, valides kestuse, ja kopeerige võti. Sellele võtmele viidatakse hiljem kui **kliendi saladusele**.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operationsis kasutajakonto loomine ja konfigureerimine
Et võimaldada Finance and Operationsil oma Azure AD rakendust kasutada, peate tegema järgmised konfigureerimistoimingud.

1.  Finance and Operationsi rentnikule uue Azure Active Directory kasutajakonto loomine. Selle kasutajakonto eesmärk on pääseda juurde konkreetsele kohandatud teenusele laorakenduses, mille Finance and Operationsi server avab. Pärast selle toimingu tegemist on teil WMDP kasutaja identimisteave, mis koosneb WMDP meiliaadressist ja WMDP paroolist. Põhitoimingud kasutajate lisamiseks Azure AD-sse ja Finance and Operationsisse leiate järgmisest õpikust: [Finance and Operationsi tellimuse registreerimine](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Looge laorakenduse kasutaja identimisteabele vastav Finance and Operationsi kasutaja.
    1.  Avage Finance and Operationsis **Süsteemihaldus** &gt; **Üldine** &gt; **Kasutajad**.
    2.  Looge uus kasutaja.
    3.  Määrake lao mobiilse seadme kasutaja, nagu on näidatud järgmisel kuvatõmmisel. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Seostage oma Azure Active Directory rakendus laorakenduse kasutajaga.
    1.  Avage rakenduses Finance and Operations **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
    2.  Looge uus rida.
    3.  Sisestage **Kliendi ID** (mille viimases jaotises hankisite), andke sellele nimi ja valige eelnevalt loodud kasutaja. Soovitame märgistada kõik seadmed, et saaksite sellelt lehelt nende juurdepääsu Finance and Operationsile hõlpsasti eemaldada, kui need peaksid kaotsi minema. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Rakenduse konfigureerimine
Peate konfigureerima rakenduse seadmel Finance and Operationsi serveriga Azure AD rakenduse kaudu ühendust looma. Selleks läbige järgmised sammud.

1.  Avage rakenduses **Ühenduse sätted**.
2.  Tühjendage väli **Demorežiim**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Sisestage järgmine teave: 
    + **Azure Active Directory kliendi ID** – kliendi ID hangiti sammus 13 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. 
    + **Azure Active Directory kliendi saladus** – kliendi saladus hangiti sammus 13 jaotises „Veebiteenuse rakenduse loomine Active Directorys”. 
    + **Azure Active Directory ressurss** – Azure AD kausta ressurss kujutab endast Finance and Operationsi juur-URL-i. **Märkus**. Ärge lõpetage seda välja kaldkriipsuga (/). 
    + **Azure Active Directory rentnik** - Azure AD kausta rentnik, mida Finance and Operationsi serveri puhul kasutatakse: https://login.windows.net/your-AD-tenant-ID. Näide: https://login.windows.net/contosooperations.onmicrosoft.com.
    <br>**Märkus**. Ärge lõpetage seda välja kaldkriipsuga (/). 
    + **Ettevõte** – sisestage rakendusse Finance and Operations juriidiline isik, millega soovite rakenduse ühendada. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valige nupp **Tagasi** rakenduse ülemises vasakus nurgas. Rakendus loob nüüd ühenduse teie Finance and Operationsi serveriga ja kuvatakse laotöötaja sisselogimisekraan. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Seadmelt juurdepääsu äravõtmine
Kaotatud või ohtu sattunud seadme puhul on vaja seadmelt juurdepääs Finance and Operationsile ära võtta. Järgmised toimingud kirjeldavad juurdepääsu äravõtmise soovituslikku protsessi.

1.  Avage rakenduses Finance and Operations **Süsteemihaldus** &gt; **Seadistus** &gt; **Azure Active Directory rakendused**.
2.  Kustutage rida, mis vastab seadmele, millelt soovite juurdepääsu ära võtta. Märkige üles eemaldatud seadme puhul kasutatud **kliendi ID**.
3.  Logige sisse Azure’i tavaportaali lehel <https://manage.windowsazure.com>.
4.  Klõpsake **Active Directory** ikooni vasakus menüüs ja seejärel soovitud kausta.
5.  Klõpsake ülemises menüüs valikut **Rakendused** ja seejärel rakendust, mida konfigureerida soovite. Avaneb leht **Kiirjuhend**, kus on ühekordse sisselogimise teave ja muu teave konfigureerimise kohta.
6.  Klõpsake vahekaarti **Konfigureeri**, kerige alla ja veenduge, et rakenduse **kliendi ID** oleks sama, mis selle jaotise 2. toimingus.
7.  Klõpsake käsuribal nuppu **Kustuta**.
8.  Klõpsake kinnitusteates nuppu **Jah**.





