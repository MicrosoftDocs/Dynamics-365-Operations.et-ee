---
title: Common Data Service'i virtuaalüksuste konfigureerimine
description: Selles teemas kirjeldatakse virtuaalüksuste konfigureerimist rakenduse Dynamics 365 Human Resources jaoks. Looge ja värskendage olemasolevaid virtuaalüksusi ning analüüsige loodud ja saadaolevaid üksusi.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645597"
---
# <a name="configure-common-data-service-virtual-entities"></a>Common Data Service'i virtuaalüksuste konfigureerimine

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Common Data Service. See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Common Data Service ning Microsoft Power Platform. Virtuaalüksuste andmeid ei talletata teenuses Common Data Service, vaid rakenduse andmebaasis. 

Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Common Data Service, peate tegema üksused teenuses Common Data Service virtuaalüksustena kättesaadavaks. See võimaldab teil teha lahendustes Common Data Service ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources. Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.

## <a name="available-virtual-entities-for-human-resources"></a>Rakenduses Human Resources saadaolevad virtuaalüksused

Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalüksustena teenuses Common Data Service. Need on saadaval ka rakenduses Power Platform. Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Common Data Service. Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.

Saate vaadata keskkonnas lubatud virtuaalüksuste loendit ja alustada üksustega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalüksused**.

![Dynamics 365 HR-i virtuaalüksused Power Appsis](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuaal- ja tavaliste üksuste võrdlus

Rakenduse Human Resources virtuaalüksused pole samad, mis tavalised teenuse Common Data Service üksused, mis on loodud rakenduse Human Resources jaoks. Rakenduse Human Resources tavalised üksused luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Common Data Service. Tavaliste üksuste puhul talletatakse andmed teenuses Common Data Service ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.

> [!NOTE]
> Rakenduse Human Resources jaoks mõeldud teenuse Common Data Service tavaliste üksuste loendi leiate teemast [Common Data Service'i üksused](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Seadistus

Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalüksused.

### <a name="enable-virtual-entities-in-human-resources"></a>Virtuaalüksuste lubamine rakenduses Human Resources

Esmalt peate lubama tööruumi **Funktsioonihaldus** kaudu virtuaalüksused lubama.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige paan **Funktsioonihaldus**.

3. Valige **Virtuaalüksuse tugi rakenduses HR/CDS** ja seejärel valige **Luba**.

Lisateavet eelvaatefunktsioonide lubamise ja keelamise kohta vt jaotisest [Funktsioonide haldus](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Rakenduse registreerimine Microsoft Azure'is

Peate Human Resourcesi eksemplari Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid. Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Avage [Microsoft Azure'i portaal](https://portal.azure.com).

2. Valige Azure'i teenuste loendis **Rakenduste registreerimised**.

3. Valige **Uus registreerimine**.

4. Sisestage väljale **Nimi** rakendust kirjeldav nimi. Näiteks **Dynamics 365 Human Resources'i virtuaalüksused**.

5. Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.

6. Valige suvand **Registreeri**.

7. Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade**, mis sisaldab väärtust **Rakenduse (kliendi) ID**. Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles. Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.

9. Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.

10. Sisestage kirjeldus, valige kestus ja valige **Lisa**.

11. Kirjutage saladuse väärtus üles. Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Kirjutage saladuse väärtus kindlasti praegu üles. Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Dynamics 365 HR Virtual Entity rakenduse installimine

Installige Dynamics 365 HR Virtual Entity rakendus oma Power Appsi keskkonda, et juurutada virtuaalüksuse lahenduse pakett teenuses Common Data Service.

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2. Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.

3. Valige lehe jaotises **Ressursid** suvand **Dynamics 365 rakendused**.

4. Valige tegevus **Installi rakendus**.

5. Valige **Dynamics 365 HR Virtual Entity** ja valige **Edasi**.

6. Vaadake teenusetingimused üle ja märkige, et te nõustute nendega.

7. Valige **Installi**.

Installimine võtab mõne minuti. Kui see on lõpule viidud, jätkake järgmiste sammudega.

![Dynamics 365 HR Virtual Entity rakenduse installimine Power Platformi halduskeskusest](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Virtuaalüksuse andmeallika konfigureerimine 

Järgmine samm on konfigureerida virtuaalüksuse andmeallikas Power Appsi keskkonnas. 

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2. Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.

3. Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.

4. Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.

5. Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.

6. Valige **Tulemid**.

7. Valige kirje **Microsoft HR-i andmeallikas**.

8. Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.

   - **Siht-URL**: teie rakenduse Human Resources nimeruumi URL. Siht-URL-i vorming on:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Näide:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Tõrketeate kuvamise välistamiseks lisage URL-i lõppu märk „**/**“.

   - **Rentniku ID**: Azure Active Directory (Azure AD) rentniku ID.

   - **AAD rakenduse ID**: rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks. Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD rakenduse saladus**: klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks. Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR-i andmeallikas](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Valige **Salvesta ja sule**.

### <a name="grant-app-permissions-in-human-resources"></a>Rakenduse õiguste andmine rakenduses Human Resources

Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.

- Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis
- Dynamics 365 HR Virtual Entity rakendus, mis on installitud Power Appsi keskkonnas 

1. Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.

2. Valige uue rakenduse kirje loomiseks **Uus**.

    - Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.
    - Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.
    - Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.

3. Valige teise rakenduse kirje loomiseks **Uus**.

    - **Kliendi ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Nimi**: Dynamics 365 HR Virtual Entity
    - Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.

## <a name="generate-virtual-entities"></a>Virtuaalüksuste loomine

Kui seadistus on lõpule viidud, saate valida virtuaalüksused, mille soovite luua ja lubada oma Common Data Service'i eksemplaris.

1. Avage rakenduses Human Resources leht **Common Data Service (CDS) integratsioon**.

2. Valige vahekaart **Virtuaalsed üksused**.

> [!NOTE]
> Lüliti **Virtuaalse üksuse lubamine** olekuks seatakse automaatselt **Jah**, kui kogu nõutav seadistus on lõpule viidud. Kui lüliti olekuks on seatud **Ei**, vaadake läbi selle dokumendi eelmiste jaotiste etapid, et kogu eeltingimuste häälestus oleks lõpule viidud.

3. Valige üksus või üksused, mida soovite luua Common Data Service'is.

4. Valige **Loo/värskenda**.

![Common Data Service’i integratsioon](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Üksuse loomise oleku kontrollimine

Virtuaalseid üksusi luuakse Common Data Service'i asünkroonse taustal töötlemise abil. Protsessi uuendusi kuvatakse tegevuskeskuses. Protsessi üksikasju, sh tõrkelogisid, kuvatakse lehel **Protsessi automatiseerimised**.

1. Avage rakenduses Human Resources loendi **Protsessi automatiseerimised** leht.

2. Valige vahekaart **Taustaprotsessid**.

3. Valige **Virtuaalse üksuse pollimise asünkroonse toimingu taustaprotsess**.

4. Valige **Kuva viimased tulemused**.

Liuguripaan kuvab protsessi kõige viimased käivitamise tulemused. Saate kuvada protsessi logi, sh kõiki tagastatud tõrkeid Common Data Service'is.

## <a name="see-also"></a>Vt ka

[Mis on Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Üksuse ülevaade](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Üksuse seoste ülevaade](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Välistest andmeallikatest pärit andmeid sisaldavate virtuaalüksuste loomine ja redigeerimine](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Mis on Power Appsi portaalid?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Rakenduste loomise ülevaade Power Appsis](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]