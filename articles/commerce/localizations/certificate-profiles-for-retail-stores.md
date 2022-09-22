---
title: Kasutaja määratletud serdiprofiilid jaekaupluste jaoks
description: See artikkel annab ülevaate serdiprofiilidest, mis on saadaval Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558433"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Kasutaja määratletud serdiprofiilid jaekaupluste jaoks

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate serdiprofiilidest, mis on saadaval Microsoft Dynamics 365 Commerce. See funktsioon laiendab funktsiooni [Jaemüügikanalite saladuste haldamine](../dev-itpro/manage-secrets.md), lisades kohalike sertide toe.

Kui kassa (POS) töötab ühenduseta režiimis, ei pääse see juurde sertifikaatidele, mis on talletatud võtme Microsoft Azure hoidlasse. Selle asemel tuleks kasutada kohalikku serti. Toetatud on järgmised võimalused.

- Kohalike sertide kasutamine võtme vault-varustsenaariumides
- Kohalike sertide kasutamine võtme hoidlata (näiteks ettevõttesisene install).
- Sertide järkjärguline uuendamine, mille korral kasutab mõni kauplus ja terminal serdi uut versiooni, kuid teised kauplused ja terminalid jätkavad eelmise versiooni kasutamist

Serdiprofiilide funktsioon võimaldab määrata vaikeserdi ja seadistada järjekorra, mille alusel serte samas serdiprofiilis otsitakse. See funktsioon pakub ka sarnaseid seadistusvõimalusi kohalike sertide ja võtmehoidla sertide puhul. Saate seadistada serte ettevõttepõhiselt, kuid iga serdi kordumatut ettevõtteülest identifikaatorit on võimalik kasutada Commerce'i kanalites.

### <a name="scenarios"></a>Stsenaariumid

Serdiprofiilide funktsioon toetab Commerce'i kanalites järgmisi stsenaariume.

- Kasutage võtme vault-varustsenaariumides kohalikku serti. Siin on mõned näited taandeolekusse laskumisest.

    - Võtmehoidla salvestusruum ei ole juurdepääsetav.
    - Serti ei leitud võtmehoidlast.
    - Kassa töötab ühenduseta režiimis.

- Kasutage kohalikke serte, kuid neid ei salvestata võtme hoidlasse (nt valdustes installatsioonis).
- Sertide järkjärguline värskendamine, mille korral kasutatakse serdi uut versiooni ainult kauplustes ja terminalides, kus uus versioon on juba saadaval.
- Sama serdi kasutamine mitmes ettevõttes.

## <a name="set-up-certificate-profiles"></a>Serdiprofiilide seadistamine

Järgmisena selgitatakse, kuidas seadistada serdiprofiile.

### <a name="set-up-key-vault"></a>Seadista võtme vault

Enne võtme vaultis talletatava digitaalsertifikaadi kasutamist tuleb lõpule viia järgmised sammud.

1. Vault-võtme talletuskonto loomine. Soovitame teil juurutada ladustamiskonto samas geograafilises piirkonnas nagu Commerce Scale Unit.
1. Laadige digitaalse sert üles võtme vaultsalvestuskontole.
1. Autoriseerige rakendusobjekti serveri (AOS) rakendus loema turvahoidla võtmekonto saladusi.

Lisateavet selle kohta, kuidas võtmega Vault töötada, vt [Teemat Alustamine Azure’i võtme vault-ga](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Süsteemiparameetrite häälestamine

Enne ärikanalites serdiprofiilide konfigureerimist peate lubama rakendusel Commerce kasutada nii võtme hoidla kui ka serdiprofiili salvestatud serte.

Commerce Headquartersis süsteemiparameetrite häälestamiseks järgige neid samme.

1. Seadke süsteemiparameetrite **lehel** suvandi Kasuta täpsema **serdisalve väärtuseks** **Jah**.
1. Lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Kasutaja määratletud serdiprofiilid jaekaupluste jaoks**.

### <a name="set-up-key-vault-parameters"></a>Võtme hoidla parameetrite seadistamine

Lehel Võtme **hoidla parameetrid** peate võtme hoidla talletusse pääsemiseks määrama järgmised parameetrid:

- **Nimi** ja **kirjeldus** – võtmesalvestuse konto nimi ja kirjeldus.
- **Vault-võtme URL** – vault-mälukonto võtme URL.
- **Vault-võtme klient** – autentimiseks võtmesalvestuskontoga seostatud (Azure Active Directory) rakenduse interaktiivne kliendi-ID Azure AD. Sellel kliendil peab olema juurdepääs salvestuskonto lugemissaladustele.
- **Võtme vault-salavõti** – salavõti, Azure AD mis on seostatud rakendusega, mida kasutatakse autentimiseks võtme hoidlakontos.
- **Nimi**, **kirjeldus** ja **salaviide**– tunnistuse nimi, kirjeldus ja salaviide.

Lisateavet vt Azure’i [võtme vault kliendi häälestamise kohta](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Serdiprofiili konfigureerimine

Rakenduse Commerce headquarters serdiprofiili konfigureerimiseks järgige neid samme.

1. Avage **Süsteemihaldus \> Seadistus \> Serdiprofiilid**.
1. Kirje loomiseks valige toimingupaanilt suvand **Uus**.
1. Sisestage tunnistuse profiili **, nime** ja **kirjelduse** väljadele **väärtused**.

    > [!NOTE]
    > Serdiprofiil on serdi kordumatu identifikaator kõikides ettevõtetes ja Commerce'i komponentides.

1. **Valige kiirkaardil** Juriidilised isikud suvand **Lisa** rea lisamiseks.
1. Valige **juriidilise isiku** all juriidiline isik (ettevõte), kelle jaoks praegust serdiprofiili kasutada tuleb.

    Kui serdiprofiili tuleks kasutada mitme juriidilise isiku puhul, korrake samme 4 ja 5, et lisada rida iga täiendava juriidilise isiku jaoks.

1. Valige **Sätted**, et avada leht **Serdiprofiili sätted**, kus saate sisestada serdiprofiilile ettevõttespetsiifilisi sätteid. Saate määrata, milliseid serte kasutada praeguse serdiprofiili ärikanalites kutsumisel. Lisage nii palju tunnistusi, kui vajate, ja seadke neile prioriteedid. Kui kõrgema prioriteediga sert pole saadaval, kasutatakse prioriteedil põhinevat järgmist serti. Lisateavet vt jaotisest Töövoog [: sertifikaatide otsimine jaotises Äri käitusaeg](#workflow-searching-certificates-in-the-commerce-runtime).

    > [!NOTE]
    > Väli **Prioriteet** seatakse automaatselt. Väärtus **1** tähistab kõrgeimat prioriteeti. Kui lehel **Serdiprofiili sätted** lisatakse uus rida, seatakse selle prioriteediks arv, mis on eelmise rea prioriteedist ühe võrra suurem. Konkreetse rea prioriteedi muutmiseks valige rida ja seejärel valige prioriteedi tõstmiseks **Nihuta üles** või prioriteedi langetamiseks **Nihuta alla**.

1. Kui lisate tunnistuse profiili sätete lehel **uue rea**, seadke järgmised väljad:

    - **Asukoha tüüp** – valige asukoht, kus sert on talletatud. Sellel väljal on kaks võimalikku väärtust: **kohalik sert** ja **võtmehoidla**.
    - **Võtmehoidla sert** – see väli on kohustuslik, kui seate välja **Asukoha tüüp** väärtuseks **Võtmehoidla**. Kasutage seda võtmehoidla serdi saladuse määramiseks.
    - **Kaupluse nimi** – see väli on valikuline ja on saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**. Kasutage seda kaupluse vaikenime määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Kaupluse asukoht** – see väli on valikuline ja on saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**. Kasutage seda kaupluse vaikeasukoha määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.

        > [!NOTE]
        > Kaupluse vaikenimi ja -asukoht lisatakse, et lihtsustada kohalike sertide otsimist lahenduses Commerce Runtime. X509StoreProvideril on loend kaustadest, kus serte talletatakse. Kui kaupluse vaikenimi ja vaikeasukoht on määramata, proovib X509StoreProvider leida sertifikaati selle loendist teistest kaustadest. Lisateavet kaupluse nime ja kaupluse asukoha jaoks saada olemise väärtuste kohta vt [storeName enum](/dotnet/api/system.security.cryptography.x509certificates.storename) ja [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Sõrmejälg** – see väli on kohustuslik ja saadaval ainult siis, kui asukoha **tüübi välja väärtuseks** on seatud **Kohalik sert**. Kasutage seda serdi sõrmejälje määramiseks.

        > [!IMPORTANT]
        > Peate tagama, et kasutajal, kes käitab kohalikku serti kasutama peab (nt Modern POS võrguühenduseta režiimis), on serdi privaatvõtmele vähemalt kirjutuskaitstud juurdepääs.

    - **Kommentaarid** – see väli on valikuline ja võimaldab kasutajatel sisestada märkmeid.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Töövoog: sertide otsimine lahenduses Commerce Runtime

Siin on põhiline töövoog, mida kasutatakse serdi otsimiseks serdiprofiili kutsumise korral Commerce Runtime'is.

1. Süsteem tuvastab, kas serdiprofiilil on praeguse juriidilise isiku jaoks ettevõttespetsiifilisi sätteid.
1. Süsteem püüab leida serti, kasutades lehel **Serdiprofiili sätted** toodud sellise rea väärtusi, mille väli **Prioriteet** väärtuseks on seatud **1**.

    - Kui välja **Asukoha tüüp** väärtuseks on seatud **Võtmehoidla**, kasutatakse välja **Võtmehoidla serdi saladus** väärtust, et otsida serti lehel **Võtmehoidla parameetrid**. Seejärel otsitakse serti võtmehoidla salvestusruumist.
    - Kui välja **Asukoha tüüp** väärtuseks on seatud **Kohalik sert**, otsib X509StoreProvider esiteks serti kaupluse vaikenime ja -asukoha põhjal, kui need parameetrid on määratud. Seejärel otsib see oma kaustaloendi kõigist muudest kaustadest.

1. Kui serti ei leita, korratakse protsessi rea puhul, mille välja **Prioriteet** väärtuseks on seatud **2** jne.

> [!NOTE]
> Kui serdiprofiilil pole praeguse juriidilise isiku jaoks ühtki sätet või kui serdiotsing ebaõnnestub kõikide lehel **Serdiprofiili sätted** toodud ridade puhul, jääb sert leidmata.

### <a name="caching-the-results-of-certificate-searches"></a>Serdiotsingute tulemuste salvestamine vahemällu

Serdiotsingute tulemused salvestatakse vahemällu. Vahemälu vaikeaegumisaeg on üks tund. Seda aega saab aga kohandada ja selle väärtuseks saab seadistada maksimaalselt 24 tundi.

## <a name="gradual-update"></a>Järkjärguline värskendamine

Kui kasutusele võetakse serdi uus versioon, kuid seda ei saa värskendada samal ajal kõikides kauplustes, võimaldab serdiprofiilide funktsioon serti järk-järgult värskendada.

1. Leidke serdiprofiil ja rida, mida tuleks värskendada, ning seejärel valige **Sätted**.
1. Lisage rida ja määrake sätted, mis on seotud serdi uusima versiooniga.
1. Suurendage uue rea välja **Prioriteet** väärtust. Kasutage nuppu **Nihuta üles**, et liigutada rida nii, et see oleks sama serdi eelmise versiooni rea kohal.
> [!NOTE]
> Commerce Runtime'is kutsutakse serdi uut versiooni esimesena. Kui serti ei olda veel kindlas poes või terminalis värskendatud, kutsutakse eelmist versiooni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
