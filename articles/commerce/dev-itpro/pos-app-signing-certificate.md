---
title: Allkirjasta MPOS.appx-fail koodi allkirjastamistunnistusega
description: See artikkel selgitab, kuidas MPOS-i koodi allkirjastamise serdiga allkirjastada.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 4cbdfcb5229be2f04531031c80f41f672b2a4747
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169095"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Allkirjasta MPOS.appx-fail koodi allkirjastamistunnistusega

[!include [banner](../includes/banner.md)]

Modern POS-i (MPOS) installimiseks peate MPOS-rakenduse allkirjastama usaldusväärse pakkuja koodi allkirjastamise serdiga ja installima sama serdi kõigile masinatele, kus MPOS on praeguse kasutaja usaldusväärse juurkausta alla installitud.

MPOS-rakenduse serdiga allkirjastamiseks **kasutage üht järgmistest suvanditest retail SDK\\Build tool\\Customization.settings** failis:

- Lisage koostamisetappide secure faili ülesande Azure DevOps osa ja laadige sert üles faili ülesande turvamiseks. Kasutage turvalise faili ülesande väljunditee muutujat parameetrina failis Customization.settings.

    > [!NOTE]
    > Secure Filei ülesanne ei toeta parooliga kaitstud serti. Enne selle ülesande üleslaadimist peate parooli eemaldama. Kuna sert on turvalisse failisüsteemi ülesandesse Azure'is üles laaditud, saate parooli eemaldada ainult selle sammu jaoks. Siiski peaksite käsitlema parooli eemaldamist oma turvaeksepertidega, et määratleda, kas see on teie projekti puhul õige toiming. Ärge eemaldage muude stsenaariumite serdi parooli.
- Kasutage failisüsteemis serti. Selleks laadige alla või looge sert ning paigutage see failisüsteemi, kus kooste töötab. Microsofti majutatud agendil või koostekasutajal peab olema juurdepääs sellele teele ja failile.
- Serdi otsimiseks kaupluses kasutage sõrmejälge ja logige sisse selle serdiga.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Turvalise faili ülesande kasutamine Universal Windowsi platvormi rakenduse allkirjastamiseks

> [!NOTE]
> Serdi salvestamiseks saate kasutada ka Azure Key Vault'i ja kasutada Azure'i märgi tööriista Modern POS-i .appx-faili ja iseteeninduse installijate allkirjastamiseks. Müügivõimaluste näidisskriptide ja lisateabe saamiseks vt [müügivõimaluste häälestamist Azure DevOps jaemüügi iseteeninduspakettide loomiseks](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Turvalise faili ülesande kasutamine on Soovitatav lähenemine Universal Windowsi platvormi (UWP) rakenduse allkirjastamisele. Lisateavet paketi allkirjastamise kohta vt "Paketi allkirjastamise [konfigureerimine"](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). See protsess kuvatakse järgmisel pildil.

![MPOS-rakenduse allkirjastamisvoog.](media/POSSigningFlow.png)

> [!NOTE]
> Praegu toetab OOB pakend ainult .appx-faili allkirjastamist, sellele protsessile ei ole allakirjutatud muud iseteenindussüsteemi installijad, nagu MPRAKENDUSEd,MERAU ja HWS. Peate selle allkirjastama käsitsi SignTooli või muude allkirjastamistööriistade abil. .appx-faili allkirjastamiseks kasutatav sert tuleb installida masinasse, kuhu on installitud Modern POS.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Serdi konfigureerimise sammud Azure Pipelines'i logimiseks

### <a name="certificate-in-the-file-systemsecure-location"></a>Failisüsteemi/turvalise asukoha sert

Laadige alla [toiming DownloadFile](/visualstudio/msbuild/downloadfile-task) ja lisage see koostamisprotsessi esimese sammuna. Turvalise faili ülesande kasutamise eeliseks on see, et fail krüptitakse ja paigutatakse kettale koostamis käigus hoolimata sellest, kas koostamisvõimaluste loomine õnnestus, nurjub või kui see tühistatakse. Fail kustutatakse allalaadimise asukohast pärast seda, kui koostamisprotsess on lõpetatud.

1. Laadige alla ja lisage Secure File toiming esimese sammuna Azure'i build müügivõimalustes. Võite secure file task alla laadida downloadFile'ist [...](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
1. Laadige sert üles turvafaili ülesandele ja määrake jaotises Väljundmuutujad viite nimi, nagu järgmisel pildil näha.
    > [!div class="mx-imgBorder"]
    > ![Turvaline failiülesanne.](media/SecureFile.png)
1. Looge uus muutuja Azure Pipelines'is, valides **vahekaardil** **Muutujad valiku Uus** muutuja.
1. Sisestage muutujale väärtusväljal nimi, näiteks **MySigningCert**.
1. Salvestab muutuja.
1. Avage **RetailSDK\\BuildToolsi** fail **Customization.settings** ja uuendage **ModernPOSPackageCertificateKeyFile** konveieris loodud muutuja nimega (etapp 3). Näide:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Kui sert ei ole parooliga kaitstud, on see samm kohustuslik. Kui sert on parooliga kaitstud, jätkake järgmiste sammudega.
    
1. Kui soovite selle serdiga allkirjastamisel Ajatempli MPOS .appx faili, **avage retail SDK\\ Build tööriist\\ Customization.settings** **fail ja värskendage ModernPOSPackageCertificateTimestamp** muutujat ajatempli pakkujaga (näiteks`http://timestamp.digicert.com`).
1. Konveieri vahekaardil Muutujad **lisage** uus turvateksti muutuja. Seadke nimi mySigningCert.secretiks **ja** määrake serdi parooli väärtus. Saate valida muutuja turvamiseks luku ikooni.
1. Lisage Powershelli **skripti ülesanne** konveierile (pärast turvalise faili allalaadimist ja enne etapi koostet). Sisestage **kuvatav** nimi ja määrake tüüp **tekstisiseseks**. Kopeerige ja kleepige järgmine skripti jaotisse.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Avage **RetailSDK\\BuildToolsi** fail **Customization.settings** ja uuendage **ModernPOSPackageCertificateThumbprint** serdi sõrmejälje väärtusega.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Üksikasju serdi jaoks sõrmejälje saamiseks vaadake serdi [sõrmejälje toomiseks](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Laadige alla või looge sert MPOS-rakenduse käsitsi allkirjastamiseks, kasutades msbuild-i SDK-s

Kui allalaaditud või loodud serti kasutatakse MPOS-rakenduse allkirjastamiseks, **siis värskendage ModernPOSPackageCertificateKeyFile** sõlme **BuildTools Customization.settings\\ failis**, et osutada PFX-faili asukohale (**$(SdkReferencesPath)\\ appxsignkey.pfx**). Näide:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

Sellisel juhul on sertifikaadifaili nimi **appxsignkey.pfx**, mis asub **kaustas Retail SDK\\Reference**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Kasutage MPOS-rakenduse allkirjastamiseks sõrmejälge

Kui kasutate MPOS-rakenduse allkirjastamiseks sõrmejälge, installige sert kohalikult. Uuendage sõrmejälje väärtust **ModernPOSPackageCertificateThumbprint** sõlmes **BuildTools\\ Customization.settings** failis.

See valik töötab, kui koostamiskasutaja on kohalik kasutaja. Kui aga kasutate Azure DevOps järgu loomiseks agendiid, ei pruugi agendil olla allkirjastamiseks serdi kasutamiseks juurdepääsuluba sertimispoele või ei installita koostemasinat. Sel juhul on lahenduseks muuta järgu kasutaja kohalikuks kasutajaks ja installida sert kasti. Kuid see valik ei tööta, kui teil ei ole väljale administraatori juurdepääsu.

> [!NOTE]
> Kui rakenduse allkirjastamiseks kasutatakse .PFX-faili või secure-faili ülesande valikut, **jätke modernPOSPackageCertificateThumbprinti** sõlm **Customization.settings tühjaks**. Kui kasutatakse sõrmejälje valikut, jätke **ModernPOSPackageCertificateKeyFile tühjaks**. Kui mõlemat väärtust uuendatakse, siis kooste nurjub.

### <a name="certification-renewal"></a>Sertifikaadi uuendamine

### <a name="renew-a-certificate-from-trusted-ca"></a>Usaldusväärselt CA-lt serdi pikendamine

Sertifikaadi uuendamise protsessis võtke ühendust oma sertifitseerimisasutusega (CA). Usaldusväärse serdi jaoks ei ole MPOS-i poole jaoks vaja ühtki tegevust.

### <a name="renew-a-self-signed-certificate"></a>Ise allkirjastatud serdi pikendamine

Ärge kasutage tootmiseks Retail SDK-s saadaolevat näidissertifikaati. Seda saab kasutada ainult arenduse eesmärkidel. Contoso näidis serti ei saa uuendada ja jaemüügi SDK versioonis 10.0.16 kaasatud näidissertifikaat aegub 31. detsembril 2020. Kui seda serti või enda allkirjastatud serti kasutatakse kohandatud Modern POS-i allkirjastamiseks, on suur võimalus, et Modern POS ei tööta pärast seda kuupäeva õigesti.
 
### <a name="impact"></a>Mõju
 
Kui see on teie jaoks tõene, tuleb teil lahendada probleem, et installer ei saa enam käitada pärast 31. detsembrit 2020. Sõltuvalt ettevõtte kasutatavast IT-poliitikast ei pruugi Modern POS enam funktsioneerib olla. On kriitiline, et testite seda, muutes kuupäeva ajutiselt tulevaseks kuupäevaks, et määratleda mõju teie organisatsioonile.
 
### <a name="steps-to-determine-the-issue"></a>Probleemi määratlemise etapid
 
1.  Kasutage Windowsi sätteid, et muuta arvutikella kuupäevaks ja kellaajaks aastal 2021.
2.  Veenduge, et Modern POS-i saab avada, sisse logida ja kande saab lõpule viia.
3.  Kontrollige, kas Modern POS-i iseteeninduse installerit on võimalik käitada ja kui jah, siis on installimine edukalt lõpetatud.
4.  Tagastage Windowsi kella sätted õigele kuupäevale ja kellaajale.
 
Kui te saate kõik need sammud ilma väljaminekuta lõpetada, saate töötada praeguse tunnistusega pärast 31. detsembrit 2020.  
 
### <a name="steps-going-forward"></a>Etapid edasi 

Eelnevalt kasutatud tunnistuse uuendamine on väga soovitatav. Soovitame tungivalt teil saada uus sert. Selleks peate tegema ühe järgmistest toimingutest:
 
- **Eelistatud** - hankige usaldusväärselt serdiasutuselt koodi allkirjastamistunnistus.

- **Pole eelistatud** - looge kasutamiseks enesega allkirjastatud koodi allkirjastamise sert. Seda kasutatakse tavaliselt ainult arenduseesmärkidel domeenis ja see ei ole tootmiseks soovitatav. 

- **Saadaval ajutise lahendusena** – kasutage uuendatud Contoso koodi allkirjastamise serti. Seda kasutatakse tavaliselt testimisotstarbel, seega pole soovitatav seda tootmisse juurutada.
 
Seejärel looge uus kohandatud Modern POS-i pakett, mis on allkirjastatud selle sertifikaadiga, mis on saadud ühest ülalnimetatud toimingutest. Sõltuvalt tunnistusest tuleb järgida ühte järgmistest sammudest:
 
- Uue, usaldusväärse serdi (või uue ise allkirjastatud serdi) kasutamisel tuleb teil installida igasse seadmesse uus sert. Pärast peate tegema vastloodud Modern POS-i paketi (installer), desinstallima olemasoleva rakenduse ja seejärel installima uue Modern POS-i paketi uuesti. Peate tegema Modern POS-i seadme aktiveerimise igas seadmes.

- Kui kasutate uuendatud Contoso serti, peate uue serdi installima igale seadmele ja installima Modern POS-i paketi (installer). Teilt ei nõuta desinstallimist, kuid peate seadme uuesti installima. Pange tähele, et Modern POS-i aktiveerimist ei nõuta. See suvand on ajutine lahendus. Kasutage seda valikut ainult uuestiaktiveerimise vältimiseks ja probleemi lahendamiseks enne uue usaldusväärse serdi saamist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
