---
title: Dataverse'i virtuaalsete tabelite konfigureerimine
description: See teema näitab, kuidas konfigureerida, luua, uuendada olemasolevaid virtuaaltabeleid ning analüüsida loodud ja saadaolevaid tabeleid Dynamics 365 Human Resources jaoks.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e26a2fb65564cb4a1d2f9ba4b0d621177207545
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414660"
---
# <a name="configure-dataverse-virtual-tables"></a>Dataverse'i virtuaalsete tabelite konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Microsoft Dataverse. See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Dataverse ning Microsoft Power Platform. Virtuaalsete tabelite andmeid ei talletata teenuses Dataverse, vaid rakenduse andmebaasis.

Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Dataverse, peate tegema tabelid teenuses Dataverse virtuaalüksustena kättesaadavaks. See võimaldab teil teha lahendustes Dataverse ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources. Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.

> [!NOTE]
> Human Resourcesi olemid vastavad Dataverse'i tabelitele. Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Rakenduses Human Resources saadaolevad virtuaalsed tabelid

Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalsete tabelitena teenuses Dataverse. Need on saadaval ka rakenduses Power Platform. Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Dataverse. Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.

Saate vaadata keskkonnas lubatud virtuaalsete tabelite loendit ja alustada tabelitega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalsed tabelid**.

![Dynamics 365 HR-i virtuaalsed tabelid Power Apps`is.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuaalsed tabelid vs. ematabelid

Rakenduse Human Resources virtuaalsed tabelid pole samad, mis teenuse Dataverse ematabelid, mis on loodud rakenduse Human Resources jaoks. 

Rakenduse Human Resources ematabelid luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Dataverse. Ematabelite puhul talletatakse andmed teenuses Dataverse ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.

> [!NOTE]
> Rakenduse Human Resources jaoks mõeldud teenuse Dataverse ematabelite loendi leiate teemast [Dataverse'i tabelid](./hr-developer-entities.md).

## <a name="setup"></a>Seadistus

Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalsed tabelid.

### <a name="enable-virtual-tables-in-human-resources"></a>Virtuaalsete tabelite lubamine rakenduses Human Resources

Esmalt peate lubama tööruumi **Funktsioonihaldus** kaudu virtuaalsed tabelid lubama.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige paan **Funktsioonihaldus**.

3. Valige **Virtuaalsete tabelite tugi HR-le rakenduses Dataverse** ja seejärel valige **Luba**.

Lisateavet eelvaatefunktsioonide lubamise ja keelamise kohta vt jaotisest [Funktsioonide haldus](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Rakenduse registreerimine Microsoft Azure'is

Peate Human Resourcesi eksemplari Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid. Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](/azure/active-directory/develop/quickstart-register-app).

1. Avage [Microsoft Azure'i portaal](https://portal.azure.com).

2. Valige Azure'i teenuste loendis **Rakenduste registreerimised**.

3. Valige **Uus registreerimine**.

4. Sisestage väljale **Nimi** rakendust kirjeldav nimi. Näiteks **Dynamics 365 Human Resources'i virtuaalsed tabelid**.

5. Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.

6. Valige suvand **Registreeri**.

7. Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade**, mis sisaldab väärtust **Rakenduse (kliendi) ID**. Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles. Te sisestate selle teabe [virtuaalsete tabelite andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.

9. Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.

10. Sisestage kirjeldus, valige kestus ja valige **Lisa**.

11. Saate salvestada saladuse väärtuse tabeli atribuudist **Väärtus**. Te sisestate selle teabe [virtuaalsete tabelite andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Kirjutage saladuse väärtus kindlasti praegu üles. Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Dynamics 365 HR Virtuaalsete tabelite rakenduse installimine

Installige Dynamics 365 HR Virtuaalse tabeli rakendus oma Power Appsi keskkonda, et juurutada virtuaalse tabeli lahenduse pakett teenuses Dataverse.

1. Avage rakenduses Human Resources leht **Microsoft Dataverse integratsioon**.

2. Valige vahekaart **Virtuaalsed tabelid**.

3. Valige suvand **Installi virtuaaltabeli rakendus**.

### <a name="configure-the-virtual-table-data-source"></a>Virtuaalse tabeli andmeallika konfigureerimine

Järgmine samm on konfigureerida virtuaalse tabeli andmeallikas Power Appsi keskkonnas.

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2. Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.

3. Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.

4. Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.

5. Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.

   > [!NOTE]
   > Eelmise häälestussammu virtuaaltabeli rakenduse installimine võib võtta mitu minutit. Kui **Finance and Operations virtuaalse andmeallika konfiguratsioonid** ei ole loendis saadaval, oodake minut ja värskendage siis loendit.

6. Valige **Tulemid**.

7. Valige kirje **Microsoft HR-i andmeallikas**.

8. Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.

   - **Siht-URL**: teie rakenduse Human Resources nimeruumi URL. Siht-URL-i vorming on:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Näide:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Tõrketeate kuvamise välistamiseks lisage URL-i lõppu märk „**/**“.

     >[!NOTE]
     >Siht-URL määrab inimressursside keskkonna, milleni virtuaalsed tabelid andmete eest liidavad. Kui loote uuenduskeskkonna, luues tootmiskeskkonnast koopia, uuendage see väärtus oma uue sisendkausta keskkonna nimeruumi URL-iks. See tagab, et virtuaalsed tabelid on ühendatud liivakasti keskkonna andmetega, selle asemel, et osutada tootmiskeskkonnale.

   - **Rentniku ID**: Azure Active Directory (Azure AD) rentniku ID.

   - **AAD rakenduse ID**: rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks. Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD rakenduse saladus**: klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks. Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft`i HR-i andmeallikas.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Valige **Salvesta ja sule**.

### <a name="grant-app-permissions-in-human-resources"></a>Rakenduse õiguste andmine rakenduses Human Resources

Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.

- Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis
- Dynamics 365 HR Virtuaalse tabeli rakendus, mis on installitud Power Appsi keskkonnas 

1. Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.

2. Valige uue rakenduse kirje loomiseks **Uus**.

    - Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.
    - Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.
    - Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.

3. Valige teise rakenduse kirje loomiseks **Uus**.

    - **Kliendi ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Nimi**: Dynamics 365 HR Virtuaalne tabel
    - Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.

## <a name="generate-virtual-tables"></a>Virtuaalsete tabelite loomine

Kui seadistus on lõpule viidud, saate valida virtuaalsed tabelid, mille soovite luua ja lubada oma Dataverse'i eksemplaris.

1. Avage rakenduses Human Resources leht **Microsoft Dataverse integratsioon**.

2. Valige vahekaart **Virtuaalsed tabelid**.

> [!NOTE]
> Lüliti **Virtuaalse tabelite lubamine** olekuks seatakse automaatselt **Jah**, kui kogu nõutav seadistus on lõpule viidud. Kui lüliti olekuks on seatud **Ei**, vaadake läbi selle dokumendi eelmiste jaotiste etapid, et kogu eeltingimuste häälestus oleks lõpule viidud.

3. Valige tabel või tabelid, mida soovite luua Dataverse'is.

4. Valige **Loo/värskenda**.

![Dataverse’i integratsioon.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Tabeli loomise oleku kontrollimine

Virtuaalseid tabeleid luuakse Dataverse'i asünkroonse taustal töötlemise abil. Protsessi uuendusi kuvatakse tegevuskeskuses. Protsessi üksikasju, sh tõrkelogisid, kuvatakse lehel **Protsessi automatiseerimised**.

1. Avage rakenduses Human Resources loendi **Protsessi automatiseerimised** leht.

2. Valige vahekaart **Taustaprotsessid**.

3. Valige **Virtuaalse tabeli pollimise asünkroonse toimingu taustaprotsess**.

4. Valige **Kuva viimased tulemused**.

Liuguripaan kuvab protsessi kõige viimased käivitamise tulemused. Saate kuvada protsessi logi, sh kõiki tagastatud tõrkeid Dataverse'is.

## <a name="see-also"></a>Vt ka

[Mis on Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabelid rakenduses Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Tabelite seoste ülevaade](/powerapps/maker/common-data-service/relationships-overview)<br>
[Välistest andmeallikatest pärit andmeid sisaldavate virtuaalsete tabelite loomine ja redigeerimine](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Mis on Power Appsi portaalid?](/powerapps/maker/portals/overview)<br>
[Rakenduste loomise ülevaade Power Appsis](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
