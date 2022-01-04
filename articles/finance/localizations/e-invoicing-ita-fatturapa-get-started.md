---
title: Itaalia FatturaPA otseintegratsiooni seadistamine SDI-ga
description: See teema annab teavet, mis aitab teil alustada Itaalia elektroonilise arveldusega ja seadistada Itaalia FatturaPA otsese integreerimise vahetussüsteemiga (SDI).
author: abaryshnikov
ms.date: 12/14/2021
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 0ccc9f04e42e748b4531622a1c90559d4ca17196
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922461"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Itaalia FatturaPA otseintegratsiooni seadistamine SDI-ga

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Itaalia elektroonilise arvelduse lisandmoodul ei pruugi praegu toetada kõiki elektrooniliste arvete jaoks saadaolevaid funktsioone rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management.

See teema annab teavet, mis aitab teil alustada Itaalia elektroonilise arveldusega finants- ja tarneahela halduses. See juhib teid läbi konfiguratsioonietappide, mis sõltuvad riigist/regioonist regulatiivsetes konfiguratsiooniteenustes (RCS). Need sammud täiendavad etappe, mida kirjeldatakse jaotises [Alusta elektroonilise arveldusega](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Eeltingimused

Enne selle teema sammude sooritamist peavad olema täidetud järgmised eeltingimused:

- Täitke jaotises Elektroonilise [arveldamise alustamine toodud sammud](e-invoicing-get-started.md).
- Importige **Itaalia FatturaPA (IT)** elektroonilise arveldamise funktsioon globaalsest hoidlast RCS-i. Lisateavet vt eelnevalt mainitud "Elektroonilise arveldamisega alustamine" jaotisest Elektroonilise arveldamise funktsiooni importimine Microsofti [konfiguratsioonipakkujast](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
- Lisage nõutavatest sertidest linke teenuse keskkonda. Nõutavad tunnistused hõlmavad digitaalallkirja serti, sertifikaadi asutusele (CA) serti ja klientide sertifikaati. Lisateavet vt teemast "Elektroonilise arveldusteenuse haldamisega alustamine" digitaalse serdi [saladuse](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) loomine.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Riigile omane konfiguratsioon Itaalia FatturaPA (IT) elektroonilise arveldamise funktsioonile

Enne rakenduse häälestuse juurutamist ühendatud finantside või tarneahela halduse rakendusele viige lõpule järgmised protseduurid.

See jaotis täiendab teema "Alusta elektroonilise arveldamisega alustamine" rakenduse häälestuse [riigiomast](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) konfiguratsiooni.

### <a name="create-a-new-feature"></a>Uue funktsiooni loomine

1. Logige teenusesse RCS sisse.
2. Elektroonilise aruandluse **tööruumi** jaotises **Konfiguratsiooni** pakkujad märkige oma ettevõtte konfiguratsioonipakkuja aktiivseks.
3. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
4. Elektroonilise **arveldamise funktsioonide lehel** valige suvand Lisa olemasoleva **funktsiooni** \> **põhjal**.
5. Microsofti **konfiguratsioonipakkujas** valige alusfunktsiooniks Itaalia **FatturaPA (IT) ja sisestage nimi ja** seejärel valige suvand Loo **funktsioon**.

### <a name="set-up-application-specific-parameters"></a>Seadistage rakenduspõhised parameetrid

1. Elektroonilise **arveldamise funktsioonide** lehel valige redigeeritav funktsioon.
2. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
3. Valige **vahekaardil** Konfiguratsioonid konfiguratsioon ja seejärel **rakendusespetsiifilised** parameetrid.
4. Veenduge, et sektsioonis Otsingud **oleks** märgitud **ruutNimenimekiri Tagasipööratud tasu** alamkategooriate loend.
5. Jaotises **Tingimused** valige **Lisa**.
6. Lisage igale süsteemis määratletud alamkategooriale kindlad tingimused ja seejärel salvestage oma muudatused.

    > [!NOTE]
    > Veerus Nimi saate valida konkreetse väärtuse asemel väärtuse Tühi või Mitte tühi \*\* \*\* kohatäitja.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigureerige müügivõimaluste töötlemine ekspordiks

1. Elektroonilise **arveldamise funktsioonide** lehel valige redigeeritav funktsioon.
2. Vahekaardil **Seadistused** valige **Müügiarved ja** seejärel käsk **Redigeeri**.
3. Läbige **toimingud** jaotises Müügivõimaluste töötlemine ja seadke kõik nõutavad väljad.

    - Dokumendi **allkirjastamise tegevuse** jaoks määrake väljal Serdi nimi **digitaalallkirja** sert.
    - Tegevuse **esitamiseks** seadistage **URL-i aadressi** ja **sertide** väljad. Välja Sertifikaadid väärtus on tunnistuste kett, millest millest esimene on juur-CA-tunnistus **·** (caentrate.cer) ja teine, millest on klientide sertifikaat.

4. Valige **Kinnita**, et veenduda, et kõik nõutud väljad on seatud.
5. Salvestage muudatused ja sulgege leht.
6. Vahekaardil **Seadistused** valige **Projektiarved ja** seejärel käsk **Redigeeri**.
7. Korrake projekti arvete puhul samme 3 kuni 5.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigureeri müügivõimaluste töötlemine importimiseks

1. Elektroonilise **arveldamise funktsioonide** lehel valige redigeeritav funktsioon.
2. Vahekaardil **Seadistused** valige käsk Impordi **arved ja seejärel käsk** **Redigeeri**.
3. Sisestage **jaotise** Andmekanal vahekaardi **Parameetrid** väljale **Andmekanal** stringi väärtus.
4. Seadke **vahekaardil** Kohaldatavusreeglid häälestuse väljad. Saate kasutada kanali **vaikeklauslit, kui määrate eelmises sammus andmekanali välja jaoks seatud väärtuse** **väärtuse väljale** **Väärtus**.

    ![Kohaldatavusreeglite seadistamine;](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Valige **Kinnita**, et veenduda, et kõik nõutud väljad on seatud.

### <a name="deploy-the-feature"></a>Funktsiooni juurutamine

1. Viige funktsioon lõpule, avaldage ja juurutage see teenuse keskkonnas. Lisateavet vt jaotisest "Elektroonilise arveldamisega alustamine" jaotisest "Elektroonilise arveldamisega alustamine" teenuse [keskkonda](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) juurutamine.
2. Juurutage funktsioon ühendatud rakendusse. Lisateabe saamiseks vt "Elektroonilise arveldamise funktsiooni juurutamine" teema "Elektroonilise arveldamisega alustamine" jaotisesse Ühendatud [rakendus](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).

### <a name="set-up-finance"></a>Seadista finantsid

1. Logige sisse oma finantskeskkonda.
2. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**.
3. Valige **globaalsed** \> **avatud** \> **hoidlad**.
4. Saate valida ja **importida kliendiarve** kontekstimudeli **ja hankijaarve impordi (IT)** konfiguratsioonid.
5. Avage **Organisatsiooni haldus** \> **Seadistus** \> **Elektroonilise dokumendi parameetrid**.
6. Vahekaardil **Funktsioonid** leidke ja valige Itaalia elektroonilise arve funktsioon ning märkige **ruut** **Luba**.
7. Kontrollige elektroonilise dokumendi vahekaardil, et kliendi arve töölehe ja projektiarve väljad on seadistatud vastavalt **rakenduse** **·** **häälestuse** [konfigureerimise](e-invoicing-get-started.md#configure-the-application-setup) teabele.

### <a name="set-up-vendor-invoice-import"></a>Saate häälestada hankijaarve importi. 

1. Märkige jaotises Konfiguratsiooni **pakkujad** finantside **elektroonilise aruandluse tööruumis oma ettevõtte** konfiguratsioonipakkuja aktiivseks.
2. Valige **Aruandluse konfiguratsioonid**.
3. Valige **kliendiarve kontekstimudel** ja seejärel valige käsk Loo **konfiguratsioon**.
4. Valige **tuletatud nimest: kliendiarve kontekst, Microsoft** tuletatud konfiguratsiooni loomiseks.
5. Valige **mustandversioonis** **kujundaja**.
6. Valige **andmemudeli** puus suvand **Vastenda mudel** andmeallikale.
7. Valige **definitsioonipuus** **DataChannel** ja seejärel käsk **Kujundaja**.
8. Andmeallikate **puus** laiendage **\$ kontekstikanali \_** ümbrist.
9. Valige **väljal** Väärtus suvand **Redigeeri**. 
10. Sisestage andmekanali nimi. Nime maksimumpikkus on 10 märki. See peaks vastama RCS-i elektroonilise arveldamise funktsiooni andmekanali parameetri **väärtusele**.
11. Salvestage muudatused ja minge siis **aruandluskonfiguratsioonide** \> **konfiguratsiooniversiooni**.
12. Valige **jaotise** Kanalid vahekaardil **Väliskanalid** suvand **Lisa**.
13. Sisestage **väljale** Kanal **\$ kontekstikanali** väärtus.
14. Sisestage väärtused **väljadele** Kirjeldus ja **Ettevõte**.
15. Valige **dokumendi** kontekstiväljal uus konfiguratsioon, mille tuletate **kliendiarve kontekstimudelist.** Vastendamise kirjeldus peaks olema **andmekanali kontekst**.
16. Valige vahekaardil **Impordi** allikad **suvand Lisa ja seadke seejärel järgmised** väärtused:

    - **Nimi:** OutputFile
    - **Andmeüksuse nimi:** hankija arve päis **(andmeüksus:** VendorInvoiceHeaderEntity)
    - **Mudeli vastendamine:** hankija arve import (IT)

> [!NOTE]
> Kui olete importinud hankijaarved erinevatest allikatest, saate luua mitmeid väliskanaleid ja mitmeid tuletatud konfiguratsioone, kus on erinevad **\$ Kontekstikanali** väärtused. Näiteks võite soovida importida hankijaarveid erinevatele juriidilistele isikutele.

## <a name="proxy-server-setup"></a>Puhverserveri seadistus

See jaotis annab teavet, mis aitab teil seadistada ja konfigureerida puhvriteenust andmevahetuse jaoks Exchange süsteemi (SDI) ja elektroonilise arveldusteenuse vahel.

### <a name="create-an-app-registration"></a>Rakenduse registreerimise loomine

1. Kasutage järgmist Windows PowerShelli skripti, et luua ise allkirjastatud sert teenuseteenuse (S2S) autentimiseks.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Salvestage .PFX-i sertifikaadifail võtme hoidlasse ja seejärel kustutage kohalik koopia.
3. Administraatorina [Azure'i portaali](https://portal.azure.com) sisselogimine.
4. Looge rakenduse registreerimine SDI puhvriteenusele.

    1. Avage **rakenduse** registreerimised, looge registreerimine ja seadke selle jaoks järgmised väärtused:

        - **Nimi:** SDI puhvri klient
        - **Toetatud** kontotüübid: ainult selle organisatsioonikausta kontod (üks rentnik)

    2. Valige **Register ja seejärel äsja loodud rakenduse** registreerimine.
    3. Minge **API lubadesse** ja valige hüvitise administraatori **luba**.
    4. Avage **tunnistused ja** saladused, valige **käsk Laadi** sert üles ja laadige S2S-autentimiseks üles cer-tunnistuse fail.
    5. Minge **Ettevõtte** rakendustesse ja valige rakendus, mille lõite.
    6. Salvestage **rakenduse ID** (kliendi ID) ja **rakenduse objekti ID** väärtused.
    7. Arveldusteenuse meeskond peab andma rakendusele teenusele juurdepääsu. Saatke järgmiste parameetrite <D365EInvoiceSupport@microsoft.com> väärtused:

        - AAD rentniku ID
        - LCS-i keskkonna ID
        - Rakenduse ID
        - Objekti ID

5. RCS-is lisage rakendus oma teenusekeskkonna rakenduseloendisse.

    1. Minge **globaliseerimisfunktsiooni** \> **·** \> **keskkondades elektroonilise** \> **arveldamise teenuse keskkonda** ja valige oma keskkond.
    2. Lisage **jaotises** Avaldused rida ruudustikku ning sisestage rakenduse nimi ja objekti ID.

        ![Rakenduse lisamine teenuse keskkonda.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Valige **salvestamine** ja seejärel **avalda**.

### <a name="create-an-azure-virtual-machine"></a>Looge Azure'i virtuaalmasin

1. Minge [Azure'i](https://portal.azure.com) portaali **virtuaalmasinasse** ja valige käsk Loo **uus**.
2. Vahekaardil **Põhied valige** oma kordustellimus ja ressursigrupp. Väärtused peaksid olema tellimus ja ressursigrupp, kus asuvad teie võtme vault ja bloobi talletus.
3. Valige piirkond. See väärtus peaks olema piirkond, kus teie finantskeskkond juurutatakse.
4. Lisage administraatori kasutajanimi ja parool ning salvestage need võtmehoidlasse.
5. Valige väljal **Vali sissetulevad** pordid **HTTPS (443) ja** **RPD (3389).**

    > [!NOTE]
    > Kui süsteem läheb tootmisse, on **soovitatav keelata RDP-port (3389).** Saate selle uuesti lubada, kui teil tuleb tõrkeotsingu eesmärgil luua ühendus virtuaalmasinaga (VM).

    ![Vahekaardi Basics väljade seadmine Azure VM loomiseks.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Vahekaardil **Kettad** kiirkaardil **Täpsem** märkige ruut Kasuta **hallatud** diskleid. Jäta **elimeral operatsioonisüsteemi ketta** märkeruut tühjaks.

    ![Vahekaardil Disks väljade seadmine Azure VM loomiseks.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Valige **vahekaardi Lisa** ja avaliku IP välja all suvand **Loo** **uus**.

    ![VahekaardiArvuti väljade seadmine Azure VM loomiseks.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Valige **SKU** väljagrupis Avaliku **IP-aadressi** loomise dialoogiaknas suvand **Standardne**. Valige **väljagrupil** Määramine suvand **Staatiline**.

    ![Avaliku IP-aadressi loomine.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Vahekaardil **Haldus** tühjendage automaatse sulgemise keelamiseks märkeruut **Automaatne** sulgemine.
10. Seadke külalis **operatsioonisüsteemi värskenduste** välja **väärtuseks Käsitsi** ja seejärel määrake kõik muud poliitikad.
11. Vaadake üle ja looge VM.
12. Uues VM-s minge **määratud** \> **ID-sse** ja seadke **olekussuvand** **olekusse** Sees.
13. Anna VM-juurdepääs võtme hoidlale.

    1. Võtme hoidlas minge pääsu **juhtelemendi (IAM)** \> **rollimäärangutele.**
    2. Valige **käsk Lisa** rollimäärang ja seadke seejärel järgmised väljad.

        1. Määrake **rolli** väljal võtmehoidla **saladuste** kasutaja.
        2. Määrake **väljal Määrake juurdepääs** väljale **Virtuaalne** masin.
        3. Määrake **kordustellimus** väljal Kordustellimus.
        4. Määrake väljal **Vali** oma VM.

    3. Avage **juurdepääsupoliitikad**.
    4. Valige **suvand Lisa** juurdepääsupoliitika ja seadke seejärel järgmised väljad:

        1. Valige **subjektiväli** väljal Valitud VM.
        2. Valige jaotises **Sert** suvand **Loend ja** Too **õigused**.

14. [Azure'i](https://portal.azure.com) portaalis minge avalikele IP-aadressidele ja valige **VM**-is loodud IP-aadress.
15. Minge **konfiguratsiooni** ja määrake nimi Domain Name System (DNS).

### <a name="prepare-the-proxy-service-environment"></a>Puhvriteenuse keskkonna ettevalmistamine

Järgige neid samme arvutis, kus puhvriteenus on majutatud.

1. Looge ühendus VM-ga kaugtöölauaühenduse abil.
2. Avage kohaliku arvuti serdi sissetõmme. Lisateavet vt jaotisest Kuidas [kuvada tunnistusi KKC sissetõmme](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in) abil.
3. Importige **tootmise sert caentrate.cer ja** **caEntratetest.cer** usaldusväärsete [juursertifikaatide sertifitseerimisasutuste kauplusesse testimiseks.](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores) **(CAEntratetest.cer** on juur-CA-sert, mille andis asutus.)
4. Avage juhtpaneelil Windowsi funktsioonide sisse- või väljalülitamine või minge serverihalduri rollide ja funktsioonide lisamiseks serveri operatsioonisüsteemi (OS) ning lülitage sisse **teenuse Internet Information Services** **·** \> **·** (IIS) funktsioonid.

    - Veebihalduse tööriistad
        - IIS-i halduse koncole
    - Ülemaailmne veebiteenused
        - Rakenduse arendusfunktsioonid
            - .NET Extensibility 4.7 (või 4.8)
            - ASP
            - ASP.NET 4.7 (või 4.8)
            - CGI
            - ISAPI laiendused
            - ISAPI filtrid
        - Tavalised HTTP-funktsioonid
            - Vaikedokument
            - Sirvimiskaust
            - HTTP tõrked
            - Staatiline sisu
        - Tervise- ja diagnostika
            - HTTP logimine
            - Jälgimine
        - Jõudlusfunktsioonid
            - Staatiline sisu tihendamine
        - Turvalisus
            - Filtreerimise taotlus

    ![IIS-i funktsioonide sissel lülitamine.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>SDI puhvriteenuse häälestamine IIS-s

1. Elutsükli Microsoft Dynamics teenustes (LCS) minge ühiskasutuses varateeki ja **valige** varatüübiks andmepakett.
2. Otsige **üles elektroonilise arveldamise teenuse Sdi puhver** ja laadige see VM-i alla.
3. Konfigureerige teenus.

    1. Eemaldage elektroonilise **arveldusteenuse Sdi puhvri** arhiivikaust, mille alla laadisite.
    2. Avage **kaustas \\ src FattureService** fail **appsettings.json** ja seadke järgmised parameetrid:

        - **KeyVaultUri:** määrake võtmehoidla aadress, mis talletab arveldusteenuse kliendisertifikaadi.
        - **RentnikId**: määrake kliendi rentniku globaalselt kordumatu ID (GUID).
        - **EnvironmentId**: määrake LCS-keskkonna ID.
        - **ClientId**: määrake vaheteenuste rakenduse registreerimise rakenduse ID kliendi rentnikus.
        - **ClientCertificateName** – määrake võtme hoidlas S2S-serdi nimi.
        - **SecurityServiceClientOptions.Endpoint** – määrake turbeteenuse URL.
        - **SecurityServiceClientOptions.Resource** – määratlege ulatus, mille jaoks luba saada.
        - **InvoicingServiceClientOptions.Endpoint** – määrake arveldusteenuse lõpp-punkt. See väärtus peab olema sama lõpp-punkt, mida kasutatakse RCS-i ja finantside jaoks.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – määrake teenusekeskkonna nimi. See väärtus peaks olema teie finantskeskkonna nimi.
        - **NotificationsFolder:** määrake kaust, kuhu sissetulevate teatiste failid salvestada.

    3. Otsige **failist web.config** üles järgmine rida ja lisage puhverserveri serdi sõrmejälg.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Kui süsteem läheb tootmisele, saate muuta mõningaid väärtusi failis web.config, et vähendada kogutava logiteabe summat ja salvestada kettaruumi. Sõlmes **\<system.diagnostics\>\<source\>** muutke switchValue väärtus **väärtuseks** **Kriitiline,Tõrge.** Lisateavet vt [MS-i teenuse jälgimise vaaturist.](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe)

4. Saate avada IIS-i halduri. Vasakul puus jääge juursõlme. Paremal valige **serverisertifikaadid.**

    ![Teenusesertifikaatide valimine IIS-i halduris.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Avage menüü ja valige **käsk** Impordi.
6. Dialoogiboksis Sertifikaadi importimine väljal Certificate file (.pfx) määrake puhverserveri **serdi** **·** .PFX-faili tee.

    ![Puhvriteenuse serdifaili määramine.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Valige ja hoidke all (või paremklõpsake) **Saite ja valige seejärel käsk Lisa** **veebisait**.
8. Dialoogiakna **Veebisaidi lisamine väljale Saidi nimi** **sisestage** saidi nimi.
9. Väljal **Füüsiline tee** osutage **kaustale src \\ FattureService.**
10. Valige **sidumistüübi** väljal **https**.
11. Määrake **väljal Hosti** nimi hostinimi.
12. Jätke **IP-aadress** ja **pordiväljad** vaikeväärtustele.
13. Veenduge, et **ruut Nõua serveri** nimenimetust oleks tühjendatud, sest SDI ei toeta seda tehnoloogia.
14. Valige **SSL**-serdi väljal teie imporditud puhverserveri sert.
15. Määrake väljal Rakendusekaust saidikaust ja märkige saidi **nimi** (nt **SdiAppPool).**

    ![Veebisaidi lisamine.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Pärast veebisaidi loomise lõpetamist avage SSL-i sätete **menüü**.

    ![SSL-i sätete menüü avamine.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Märkige ruut **Nõua** SSL-i ja seejärel valige **kliendi** sertide väljagrupis suvand **Nõua**.

    ![SSL-i sätete konfigureerimine.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Avage **kausta sirvimine** ja valige **Luba**.
19. Minge mis tahes veebibrauseris faili **serverDNS/TrasmissioneFatture.svc.** Ilmub standardne teenuse lehekülg.

    ![Teenuse kontrollimine brauseris.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Looge logide ja failide salvestamiseks järgmised kaustad:

    - **C: \\ Logid \\** – kaupluse logifailid siin. Neid faile saab vaadata MS Service [Trace](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) Viewer.
    - **C: \\ failid \\** – salvestage kõik vastusefailid siia.

21. Failide exploreris andke võrguteenustele **ja** **IIS AppPool \\ SdiAppPooli** (või **IIS AppPool \\ DefaultAppPool,** **·** **kui** kasutate vaikekausta) juurdepääs logide ja failide kaustadele.

    1. Valige ja hoidke all (või paremklõpsake) ühte kaustast ja valige seejärel **atribuudid**.
    2. Valige **dialoogiboksi** Atribuudid vahekaardil **Turvalisus suvand** **Redigeeri**.
    3. Lisage kasutajad, kui neid loendis pole.
    4. Korrake teise kausta jaoks samme 1 kuni 3.

    ![Teenuse kasutajale õiguste lisamine.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Privaatsusavaldus 

Itaalia elektroonilise **arve funktsiooni lubamine võib nõuda piiratud andmete** saatmist. Need andmed hõlmavad organisatsiooni maksuregistreerimise ID-d. Administraator saab lubada ja keelata Itaalia elektroonilise arve funktsiooni. Funktsiooni keelamiseks järgige neid samme.

1. Avage **Organisatsiooni haldus** \> **Seadistus** \> **Elektroonilise dokumendi parameetrid**.
2. Valige **vahekaardil** Funktsioonid read, mis sisaldavad Itaalia elektroonilise arve **funktsiooni**, ja seejärel valige suvand Keela **kohe**.

Andmed, mis imporditakse nendest välissüsteemidest sellesse Dynamics 365 võrguteenusse, kuuluvad meie [privaatsusavaldusele](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet vt jaotisest "Privaatsusteatis" riigi-/regioonispetsiifilises funktsioonidokumentatsioonis.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Elektroonilise arveldusega alustamine](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
