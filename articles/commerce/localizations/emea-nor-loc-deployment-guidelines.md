---
title: Norra kassaregistrite juurutuse juhised (pärand)
description: See artikkel on juurutuse juhend, mis näitab, kuidas lubada Microsoft Dynamics 365 Commerce Lokaliseerimine Norras.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: fb597add48ac3508a88142e63d80f405b6b5f8b4
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346041"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Norra kassaregistrite juurutuse juhised (pärand)

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Fiskaalintegratsiooni näidisfunktsioon ei kasuta fiskaalintegratsiooni [raamistikku](./fiscal-integration-for-retail-channel.md) ja seda ei parandata hilisemate värskenduste puhul. Kasutage hoopis fiskaalintegratsiooni [raamistikul põhinevat funktsiooni](./emea-nor-fi-deployment.md).

See artikkel on juurutuse juhend, mis näitab, kuidas lubada Microsoft Dynamics 365 Commerce Lokaliseerimine Norras. Lokaliseerimine koosneb Commerce’i komponentide mitmest laiendist. Näiteks lubavad laiendid printida kviitungitele kohandatud välju, registreerida täiendavaid auditi sündmusi, müügikandeid ja maksekandeid kassas (POS), digitaalselt müügikandeid allkirjastada ja printida X- ja Z-aruanded kohalikes vormingutes. Lisateavet Norra lokaliseerimise kohta vt Norra kassaraamatu [funktsioonist](./emea-nor-cash-registers.md).

See näidis on osa jaemüügi tarkvara arenduskomplektist (SDK). Lisateavet SDK kohta vt jaemüügi tarkvara [arenduskomplekti (SDK) arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md).

See näidis koosneb Commerce Runtime’i (CRT), jaemüügiserveri ja kassa laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja koosnema projektidest CRT, jaemüügiserverist ja kassaprojektidest. Soovitame kasutada jaemüügi SDK-d, et teha selles artiklis kirjeldatud muudatused. Soovitame kasutada ka allikakontrollisüsteemi, nt Microsoft Visual Studio Online (VSO), kus ühtegi faili pole veel muudetud.

> [!NOTE]
> Rakendusel Commerce 10.0.8 ja eespool nimetatakse jaemüügiserverit Commerce Scale Unitiks. Kuna see artikkel kehtib rakenduse mitme varasema versiooni kohta, kasutatakse *jaemüügiserverit* kogu artikli jooksul.
>
> Mõned selle artikli protseduuride sammud erinevad üksteisest sõltuvalt kasutatavast äriversioonist. Lisateavet vt jaotisest Mis [on uut või muutunud Dynamics 365 Retail](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Serdiprofiilide kasutamine ärikanalites

Commerce’i versioonides 10.0.15 ja uuemates versioonides saate kasutada kasutaja määratud serdiprofiile jaekaupluste funktsiooni jaoks, [mis](./certificate-profiles-for-retail-stores.md) toetab tõrke üleminekut võrguühenduseta, kui võtme vault või commerce headquarters pole saadaval. See funktsioon laiendab jaemüügikanalite [funktsiooni salateene haldamine](../dev-itpro/manage-secrets.md).

Selle funktsiooni rakendamiseks laiendis CRT järgige neid samme.

1. Looge uus laiendusprojekt CRT (C# klassi teegi projekti tüüp). Kasutage jaemüügi tarkvara arenduskomplekti (SDK) näidismalle (RetailSDK\SampleExtensions\CommerceRuntime).

2. Lisage kohandatud ohjur certificateSignatureServiceRequest projektile SequentialSignatureRegister.

3. Salakutse lugemiseks, kasutades `GetUserDefinedSecretCertificateServiceRequest` konstruktorit parameetriga profileId. See käivitab funktsiooni, mis töötab serdiprofiilide sätetega. Sätete põhjal tuuakse sert kas Azure’i võtme hoidlast või kohaliku arvuti mäluseadmest.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Serdi toomisel jätkake andmete allkirjastamist.

5. Saate koostada CRT laiendusprojekti.

6. Kopeerige väljaminekuklassiteek ja kleepige see käsitsi testimiseks rakendusse ...\RetailServer\webroot\bin\Ext.

7. Failis CommerceRuntime.Ext.config värskendage laiendi koosseisu jaotist kohandatud teegiteabega.

## <a name="development-environment"></a>Arenduskeskkond

Viige need protseduurid lõpule arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="the-crt-extension-components"></a>Laienduse CRT komponendid

Laienduskomponendid CRT kaasatakse näidiste CRT hulka. Järgmiste protseduuride lõpule viimiseks avage CRT lahendus **CommerceRuntimeSamples.sln** jaotises **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>ReceiptsNorway komponent

1. Leidke projekt **Runtime.Extensions.ReceiptsNorway** ja koostage see.
2. Leidke kaustast Extensions.ReceiptsNorway **bin\\ Debug\\** contoso.Commerce.Runtime.ReceiptsNorway.dll **assemblerfail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ microsoft\\ Internet Information Services (IIS) jaemüügiserveri asukoha bin ext** kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt komponent

1. Leidke projekt **Runtime.Extensions.SalesPaymentTransExt** ja koostage see.
2. Leidke kaustast Extensions.SalesPaymentTransExt **bin\\ Debug\\** Contoso.Commerce.Runtime.SalesPaymentTransExt.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway komponent

1. Leidke projekt **Runtime.Extensions.XZReportsNorway** ja koostage see.
2. Leidke kaustast Extensions.XZReportsNorway **bin\\ Debug\\** Contoso.Commerce.Runtime.XZReportsNorway.dll **assemblerfail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

# <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEventi näidiskomponent

1. Otsige üles **projekt Runtime.Extensions.RegisterAuditEventSample** ja koostage see.
2. Leidke kaustast Extensions.RegisterAuditEventSample **bin\\ Debug\\** contoso.Commerce.Runtime.RegisterAuditEventSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature’i näidiskomponent

1. Leidke projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Muutke faili **App.config**, määrates sõrmejälje, kaupluse asukoha ja kaupluse nime serdi jaoks, mida tuleks kasutada müügikannete allkirjastamiseks.
3. Koostage projekt.
4. Leidke kaustast **Extensions.SalesTransactionSignatureSample\\ bin\\ Debug** järgmised failid:

    - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll **assemblerifail**
    - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config **konfiguratsioonifail**

5. Kopeerige failid laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

6. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

7. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

# <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEventi näidiskomponent

1. Otsige üles **projekt Runtime.Extensions.RegisterAuditEventSample** ja koostage see.
2. Leidke kaustast Extensions.RegisterAuditEventSample **bin\\ Debug\\** contoso.Commerce.Runtime.RegisterAuditEventSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature’i näidiskomponent

1. Leidke projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Muutke faili **App.config**, määrates sõrmejälje, kaupluse asukoha ja kaupluse nime serdi jaoks, mida tuleks kasutada müügikannete allkirjastamiseks.
3. Koostage projekt.
4. Leidke kaustast **Extensions.SalesTransactionSignatureSample\\ bin\\ Debug** järgmised failid:

    - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll **assemblerifail**
    - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config **konfiguratsioonifail**

5. Kopeerige failid laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

6. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

7. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messagesi komponent

1. Leidke runtime.Extensions.SalesTransactionSignatureSample.Messages **project**.
2. Leidke kaustast Extensions.SalesTransactionSignatureSample.Messages **bin\\ Silumine\\** contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll **assemblerfail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

# <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEventi näidiskomponent

1. Otsige üles **projekt Runtime.Extensions.RegisterAuditEventSample** ja koostage see.
2. Leidke kaustast Extensions.RegisterAuditEventSample **bin\\ Debug\\** contoso.Commerce.Runtime.RegisterAuditEventSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature’i näidiskomponent

1. Leidke projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Muutke faili **App.config**, määrates sõrmejälje, kaupluse asukoha ja kaupluse nime serdi jaoks, mida tuleks kasutada müügikannete allkirjastamiseks.
3. Koostage projekt.
4. Leidke kaustast **Extensions.SalesTransactionSignatureSample\\ bin\\ Debug** järgmised failid:

    - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll **assemblerifail**
    - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config **konfiguratsioonifail**

5. Kopeerige failid laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

6. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

7. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponent SequentialSignatureRegister.Contracts

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Leidke kaustast Extensions.SequentialSignatureRegister.Contracts **bin\\ Silumine\\** contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

# <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEventi näidiskomponent

1. Otsige üles **projekt Runtime.Extensions.RegisterAuditEventSample** ja koostage see.
2. Leidke kaustast Extensions.RegisterAuditEventSample **bin\\ Debug\\** contoso.Commerce.Runtime.RegisterAuditEventSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregister-component"></a>Komponent SequentialSignatureRegister

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Muutke faili **App.config**, määrates sõrmejälje, kaupluse asukoha ja kaupluse nime serdi jaoks, mida tuleks kasutada müügikannete allkirjastamiseks.
3. Koostage projekt.
4. Leidke kaustast **Extensions.SequentialSignatureRegister\\ bin\\ Debug** järgmised failid:

    - Contoso.Commerce.Runtime.SequentialSignatureRegister.dll-i **assemblerifail**
    - **Konfiguratsioonifail Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopeerige failid laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

6. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

7. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway komponent

1. Leidke projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Leidke kaustast Extensions.SalesTransactionSignatureNorway **bin\\ Debug\\** contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponent SequentialSignatureRegister.Contracts

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Leidke kaustast Extensions.SequentialSignatureRegister.Contracts **bin\\ Silumine\\** contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponent

1. Leidke projekt **Runtime.Extensions.SalesPaymentTransExtNorway** ja koostage see.
2. Leidke kaustast Extensions.SalesPaymentTransExtNorway **bin\\ Debug\\** contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

# <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway komponent

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

2. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregister-component"></a>Komponent SequentialSignatureRegister

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Muutke faili **App.config**, määrates sõrmejälje, kaupluse asukoha ja kaupluse nime serdi jaoks, mida tuleks kasutada müügikannete allkirjastamiseks.
3. Koostage projekt.
4. Leidke kaustast **Extensions.SequentialSignatureRegister\\ bin\\ Debug** järgmised failid:

    - Contoso.Commerce.Runtime.SequentialSignatureRegister.dll-i **assemblerifail**
    - **Konfiguratsioonifail Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopeerige failid laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

6. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

7. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway komponent

1. Leidke projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Leidke kaustast Extensions.SalesTransactionSignatureNorway **bin\\ Debug\\** contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponent SequentialSignatureRegister.Contracts

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Leidke kaustast Extensions.SequentialSignatureRegister.Contracts **bin\\ Silumine\\** contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponent

1. Leidke projekt **Runtime.Extensions.SalesPaymentTransExtNorway** ja koostage see.
2. Leidke kaustast Extensions.SalesPaymentTransExtNorway **bin\\ Debug\\** contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

# <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway komponent

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

2. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregister-component"></a>Komponent SequentialSignatureRegister

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Muutke faili **App.config**, määrates sõrmejälje, kaupluse asukoha ja kaupluse nime serdi jaoks, mida tuleks kasutada müügikannete allkirjastamiseks.
3. Koostage projekt.
4. Leidke kaustast **Extensions.SequentialSignatureRegister\\ bin\\ Debug** järgmised failid:

    - Contoso.Commerce.Runtime.SequentialSignatureRegister.dll-i **assemblerifail**
    - **Konfiguratsioonifail Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopeerige failid laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

6. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

7. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway komponent

1. Leidke projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Leidke kaustast Extensions.SalesTransactionSignatureNorway **bin\\ Debug\\** contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponent SequentialSignatureRegister.Contracts

1. Leidke projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Leidke kaustast Extensions.SequentialSignatureRegister.Contracts **bin\\ Silumine\\** contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponent

1. Leidke projekt **Runtime.Extensions.SalesPaymentTransExtNorway** ja koostage see.
2. Leidke kaustast Extensions.SalesPaymentTransExtNorway **bin\\ Debug\\** contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Jaemüügiserver:** kopeerige assembler **\\ IIS-i\\** jaemüügiserveri saidi asukoha bin-ext kausta.
    - **Kohalik CRT modern POS-is:** kopeerige assembler **\\ kohaliku kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Jaemüügiserver:** faili nimi on **commerceruntime.ext.config** **\\ ja see on IIS-i jaemüügiserveri saidi asukoha bin ext-kaustas.**
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Ärge **redigeerige** faile commerceruntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

---

### <a name="the-retail-server-extension-components"></a>Jaemüügiserveri laienduse komponendid

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature jaemüügiserveri näidiskomponent

1. **Leidke kaustas RetailSDK\\ SampleExtensions\\ RetailServer\\ RetailServer.Extensions.SalesTransactionSignatureSample projekt RetailServer.Extensions.SalesTransactionSignatureSample** **ja** koostage see.
2. Leidke kaustast RetailServer **Extensions.SalesTransactionSignatureSample\\ bin\\ Debug\\** kaust Contoso.RetailServer.SalesTransactionSignatureSample.dll **.**
3. Kopeerige assemblerifail jaemüügiserveri laienduste kausta.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    See kaust on **\\ IIS-i** jaemüügiserveri asukoha bin-kaust.

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    See kaust on **\\ IIS-i** jaemüügiserveri asukoha bin-kaust.

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    Kaust on IIS-i **\\\\ jaemüügiserveri** asukoha bin-ext-kaust.

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    Kaust on IIS-i **\\\\ jaemüügiserveri** asukoha bin-ext-kaust.

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    Kaust on IIS-i **\\\\ jaemüügiserveri** asukoha bin-ext-kaust.

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    Kaust on IIS-i **\\\\ jaemüügiserveri** asukoha bin-ext-kaust.

    ---

4. Otsige jaemüügiserveri konfiguratsioonifail. Faili nimi on **web.config** ja see on IIS-i jaemüügiserveri saidi asukoha juurkaustas.
5. Registreerige jaemüügiserveri laiendused **konfiguratsioonifaili laiendi sektsioonis extensionComposition**.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Saate registreerida jaemüügiserveri laienduste sõltuvused.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4/)

    1. Leidke kaustast **CommerceRuntime\\ Extensions.SalesTransactionSignatureSample\\ bin\\ Silumine** järgmised failid:

        - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll **assemblerifail**
        - Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config **konfiguratsioonifail**

    2. Kopeerige failid IIS-i **\\** jaemüügiserveri asukoha bin-kausta.
    3. Registreeri laiendi CRT konfiguratsioonifaili muudatus.CRT Selle faili nimi on **commerceruntime.ext.config** **ja** see on IIS-i jaemüügiserveri saidi asukoha bin-kaustas.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later/)

    1. Leidke kaustas CommerceRuntime Extensions.SalesTransactionSignatureSample.Messages bin Debug **\\ kaust Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll assemblerifail\\.\\** **·**
    2. Kopeerige fail IIS-i **\\** jaemüügiserveri saidi asukoha bin-kausta.
    3. Registreeri laiendi CRT konfiguratsioonifaili muudatus.CRT Selle faili nimi on **commerceruntime.ext.config** **ja** see on IIS-i jaemüügiserveri saidi asukoha bin-kaustas.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Toimingud pole nõutavad.

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    > [!NOTE]
    > Toimingud pole nõutavad.

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    > [!NOTE]
    > Toimingud pole nõutavad.

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    > [!NOTE]
    > Toimingud pole nõutavad.

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS-i laienduse komponendid

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Võrguühenduseta režiimi puhvrikoodi juurutamine

See osa on võrdne jaemüügiserveri kontrolleriga, CRT kuid see laiendab kohalikku versiooni, mida kasutatakse siis, kui klientrakendus ei ole ühendatud.

1. Kohandamisfailis **muutke** **jaotist @(RetailServerLibraryPathForProxyGeneration),** et see kasutaks puhverserveri loomiseks uut jaemüügiserveri assemblerit.
2. Juurutage järgmised liidesemeetodid **klassis StoreOperationsManager**. Lisage esimese iteratsiooni jaoks järgmine kood:

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    ---

3. Puhvrikoodi uuesti loomiseks looge **käsurealt** **kaust Puhvrid, kasutades käsku msbuild /t:Rebuild**.
4. Lahenda projekti **sõltuvus Proxies.RetailProxy**:

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    Avatud RetailSDK Proxies **RetailProxy\\ Proxies.RetailProxy.csproj, lisage lahendusele projekt RetailSDK\\ SampleExtensions\\ CommerceRuntime** Extensions.SalesTransactionSignatureSample **CommerceRuntime.Extensions.SalesTransactionSignatureSample \\\\ projekt ja lisage projekti viide projektile RetailTransactionSignatureSample\\\\**.**·** **·**

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    Avatud RetailSDK Proxies **RetailProxy\\ Proxies.RetailProxy.csproj. Lisage retailSDK\\ SampleExtensions\\ CommerceRuntime** Extensions.SalesTransactionSignatureSample.Messages CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages **\\ project lahendusele ja lisage projekti viide projektile RetailProxy\\\\, et viidata SalesTransactionSignatureSample.Messages\\.** **·** **·**

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    ---

5. Liidese meetodite korrigeerimine **klassis StoreOperationsManager**:

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    > [!NOTE]
    > See etapp ei kehti sellele versioonile.

    ---

6. Värskendage **faili dllhost.exe.config** nii, et kliendi maakler laadib uue RetailProxy assembleri.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Jaemüügi puhvri laienduse komponent (jaemüügi 7.3.1 ja uuem)

Täitke järgmine protseduur ainult juhul, kui kasutate jaemüügi 7.3.1 ja uuemat versiooni.

1. **Leidke kaustas RetailSDK\\ SampleExtensions\\ RetailProxy.Extensions.SalesTransactionSignatureSample\\ projekt RetailServer.Extensions.SalesTransactionSignatureSample** **ja** koostage see.
2. Leidke kaustas RetailProxy RetailProxy.Extensions.SalesTransactionSignatureSample bin Debug **\\ assemblerifail Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample\\\\.** **·**
3. Kopeerige assemblerifailid kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.
4. Registreerige jaemüügi puhvri muudatus laiendi konfiguratsioonifailis. Faili nimi on **RetailProxy.MPOSOffline.ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Tänapäevase kassa laienduse komponendid

1. Avage lahendus retailSdk **\\ POS\\ ModernPOS.sln-sln** ja veenduge, et seda saab kompileerida tõrgeteta. Lisaks veenduge, et saate Microsoft’ilt Modern POS-i käivitada Visual Studio, kasutades käsku **Käivita**.

    > [!NOTE]
    > Tänapäevane kassa ei tohi olla kohandatud. Peate kasutajakonto juhtelemendi (UAC) lubama ja vastavalt vajadusele desinstallima modern POS-i varem installitud eksemplarid.

2. Kaasa järgmised olemasolevad lähtekoodi kaustad pos.Extensions **projekti.**

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Lubage laienduste kompileerimine failis **tsconfig.json**, eemaldades välistamisloendist järgmised kaustad.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Lubage laienduste laadimine laiendustes.json **·**, lisades sobivasse kohta järgmised read.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Lisateavet ja näidiseid, mis näitavad lähtekoodi kaustade kaasamist ja laiendite laadimist, leiate readme.md **müügikoha laienduste projekti juhistest**.

5. Saate lahenduse uuesti luua.
6. Käivitage Modern POS siluris ja katsege funktsioone.

### <a name="cloud-pos-extension-components"></a>Pilve kassa laienduse komponendid

1. Avage lahendus retailSdk **\\ POS\\ CloudPOS.sln-s ja** veenduge, et seda saab kompileerida tõrgeteta.
2. Kaasa järgmised olemasolevad lähtekoodi kaustad **pos.Extensions projekti.**

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Lubage laienduste kompileerimine failis **tsconfig.json**, eemaldades välistamisloendist järgmised kaustad.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Lubage laienduste laadimine laiendustes.json **·**, lisades sobivasse kohta järgmised read.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Lisateavet ja näidiseid, mis näitavad lähtekoodi kaustade kaasamist ja laiendite laadimist, leiate readme.md **müügikoha laienduste projekti juhistest**.

5. Saate lahenduse uuesti luua.
6. Käivitage lahendus, kasutades käsku **Käivita** ja järgides Jaemüügi SDK kasutusjuhend.
7. Saate funktsiooni testida.

### <a name="set-up-required-parameters-in-headquarters"></a>Häälestage peakontoris nõutavad parameetrid.

Lisateavet vt Norra kassaraamatu [funktsioonidest](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Tootmiskeskkond

Järgige neid samme Commerce’i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Viige lõpule selles artiklis varasemas [pilve kassa laienduse](#cloud-pos-extension-components)[komponentide või Modern POS-i](#modern-pos-extension-components) laienduskomponentide jaotises toodud sammud.
2. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets\\ all järgmised** muudatused:

    1. **Lisage konfiguratsioonifailides commerceruntime.ext.config** **ja CommerceRuntime.MPOSOffline.Ext.config** koostise jaotisele **järgmised** read:

        # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Commerce puhvri kohandamise lubamine:

        # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

        Konfiguratsioonifailis **dllhost.exe.config** lisage konfiguratsioonijaotise **alamjaotisesse appSettings** järgmised **read**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

        Konfiguratsioonifailis **dllhost.exe.config** lisage konfiguratsioonijaotise **alamjaotisesse appSettings** järgmised **read**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

        Konfiguratsioonifailis **RetailProxy.MPOSOffline.ext.config** lisage koostise jaotisesse järgmised **read**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

        Konfiguratsioonifailis **RetailProxy.MPOSOffline.ext.config** lisage koostise jaotisesse järgmised **read**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

        Konfiguratsioonifailis **RetailProxy.MPOSOffline.ext.config** lisage koostise jaotisesse järgmised **read**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

        Konfiguratsioonifailis **RetailProxy.MPOSOffline.ext.config** lisage koostise jaotisesse järgmised **read**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Tehke kohanduspaketi kohandamise **konfiguratsioonifailis** järgmised muudatused.

    1. Luba jaemüügi puhvri kohandamine.

        # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

        Lisage järgmised read jaotisesse **&lt; ItemGroup Condition="@(RetailServerLibraryPathForProxyGeneration)" == ""&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

        Lisage järgmised read jaotisesse **&lt; ItemGroup Condition="@(RetailServerLibraryPathForProxyGeneration)" == ""&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

        Lisage jaotisesse **ItemGroup järgmised read**, et kaasata jaemüügi puhvri laiendus juurutatavatesse pakettidesse:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

        Lisage jaotisesse **ItemGroup järgmised read**, et kaasata jaemüügi puhvri laiendus juurutatavatesse pakettidesse:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

        Lisage jaotisesse **ItemGroup järgmised read**, et kaasata jaemüügi puhvri laiendus juurutatavatesse pakettidesse:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

        Lisage jaotisesse **ItemGroup järgmised read**, et kaasata jaemüügi puhvri laiendus juurutatavatesse pakettidesse:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Lisage jaotisesse **ItemGroup järgmised read**, et kaasata CRT laiendused juurutatavatesse pakettidesse:

        # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Lisage jaotisesse **ItemGroup järgmised read**, et kaasata jaemüügiserveri laiend juurutatavatesse pakettidesse:

        # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Muutke järgmisi faile, et kaasata Norra ressursifailid juurutatavatesse pakettidesse:
    - Paketid\_ SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Pakendid\RetailServer\Sdk.RetailServerSetup.proj
  
  - **Faili Sdk.ModernPos.Shared.csproj** jaoks 
    - Lisa rida jaotisse **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Määrake <File_name> ressursifaili nimi. Sama kehtib teiste alltoodud näidete kohta.
 
    - Lisa rida jaotisesse **Sihtkoha nimi = "CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - **Faili Sdk.RetailServerSetup.proj** jaoks 
    - Lisa rida jaotisse **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Lisa rida jaotisesse **Sihtkoha nimi = "CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Muutke serdi konfiguratsioonifaili, määrates müügikannete allkirjastamiseks kasutatava serdi sõrmejälje, kaupluse asukoha ja kaupluse nime. Seejärel kopeerige konfiguratsioonifail kausta **Viited**.

    # <a name="application-update-4"></a>[Rakenduse värskendus 4](#tab/app-update-4)

    Faili nimi on **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** **ja see on jaotises CommerceRuntime\\ Extensions.SalesTransactionSignatureSample\\ bin\\ Debug**.

    # <a name="application-update-5-and-later"></a>[Rakenduse värskendus 5 ja uuem](#tab/app-update-5-and-later)

    Faili nimi on **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** **ja see on jaotises CommerceRuntime\\ Extensions.SalesTransactionSignatureSample\\ bin\\ Debug**.

    # <a name="retail-731"></a>[Jaemüügi 7.3.1](#tab/retail-7-3-1)

    Faili nimi on **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** **ja see on jaotises CommerceRuntime\\ Extensions.SalesTransactionSignatureSample\\ bin\\ Debug**.

    # <a name="retail-732-and-later"></a>[Jaemüügi 7.3.2 ja uuemad](#tab/retail-7-3-2)

    Faili nimi on **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** ja **see on jaotises Extensions.SequentialSignatureRegister\\ bin\\ Debug**.

    # <a name="retail-735-and-later"></a>[Jaemüügi 7.3.5 ja uuemad](#tab/retail-7-3-5)

    Faili nimi on **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** ja **see on jaotises Extensions.SequentialSignatureRegister\\ bin\\ Debug**.

    # <a name="retail-811-and-later"></a>[Jaemüügi 8.1.1 ja uuem](#tab/retail-8-1-1)

    Faili nimi on **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** ja **see on jaotises Extensions.SequentialSignatureRegister\\ bin\\ Debug**.

    ---

6. Jaemüügiserveri konfiguratsioonifaili värskendamine. Failis **RetailSDK\\ Packages\\ RetailServer\\ Code\\ web.config** lisage **laiendicomposition** sektsiooni järgmised read.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Juurutatavate **pakendite loomiseks käivitage msbuild** kogu Retail SDK jaoks.
8. Rakendage paketid elutsükli Microsoft Dynamics teenuste (LCS) kaudu või käsitsi. Lisateavet vt teemast Juurutatavate [pakendite loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Digitaalallkirja lubamine Modern POS-i võrguühenduseta režiimis

Modern POS-i võrguühenduseta režiimis digitaalallkirja lubamiseks peate järgima neid samme pärast Modern POS-i aktiveerimist uues seadmes.

1. Logige teenusesse POS sisse.
2. Andmebaasi ühenduse **oleku lehel** veenduge, et ühenduseta andmebaas on täielikult sünkroonitud. Kui välja Ootel allalaadimised **väärtus** on **0** (null), siis on andmebaas täielikult sünkroonitud.
3. Logige müügikohast välja.
4. Oodake, kuni võrguühenduseta andmebaas täielikult sünkroonitakse.
5. Logige teenusesse POS sisse.
6. Andmebaasi ühenduse **oleku lehel** veenduge, et ühenduseta andmebaas on täielikult sünkroonitud. Kui ootel kannete väärtus **võrguühenduseta andmebaasi väljal** on **0** (null), siis on andmebaas täielikult sünkroonitud.
7. Modern POS-i taaskäivitamine.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
