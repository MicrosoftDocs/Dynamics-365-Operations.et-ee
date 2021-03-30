---
title: Kasutaja määratletud serdiprofiilid jaekaupluste jaoks
description: Selles teemas antakse ülevaade selle kohta, kuidas serte kauplustes kasutatakse.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 03fe3d7fb64b2e9d0a06dc56654933f0c672782a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225741"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Kasutaja määratletud serdiprofiilid jaekaupluste jaoks

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Ülevaade

Selles teemas antakse ülevaade rakenduses Microsoft Dynamics 365 Commerce saadaolevatest serdiprofiilidest. See funktsioon laiendab funktsiooni [Jaemüügikanalite saladuste haldamine](../dev-itpro/manage-secrets.md), lisades kohalike sertide toe.

Kui kassa (POS) töötab ühenduseta režiimis, ei pääse see juurde võtmehoidlas talletatud sertidele. Selle asemel tuleks kasutada kohalikku serti. Toetatud on järgmised võimalused.

- Kohalike sertide kasutamine võtmehoidla taandeolekusse laskumise korral
- Kohalike sertide kasutamine võtmehoidlata (nt kohapealse installimise korral)
- Sertide järkjärguline uuendamine, mille korral kasutab mõni kauplus ja terminal serdi uut versiooni, kuid teised kauplused ja terminalid jätkavad eelmise versiooni kasutamist

Serdiprofiilide funktsioon võimaldab määrata vaikeserdi ja seadistada järjekorra, mille alusel serte samas serdiprofiilis otsitakse. See funktsioon pakub ka sarnaseid seadistusvõimalusi kohalike sertide ja võtmehoidla sertide puhul. Saate seadistada serte ettevõttepõhiselt, kuid iga serdi kordumatut ettevõtteülest identifikaatorit on võimalik kasutada Commerce'i kanalites.

### <a name="scenarios"></a>Stsenaariumid

Serdiprofiilide funktsioon toetab Commerce'i kanalites järgmisi stsenaariume.

- Kohaliku serdi kasutamine võtmehoidla taandeolekusse laskumise korral. Siin on mõned näited taandeolekusse laskumisest.

    - Võtmehoidla salvestusruum ei ole juurdepääsetav.
    - Serti ei leitud võtmehoidlast.
    - Kassa töötab ühenduseta režiimis.

- Kohalike sertide kasutamine, ilma et neid võtmehoidlas talletataks (nt kohapealse installimise korral).
- Sertide järkjärguline värskendamine, mille korral kasutatakse serdi uut versiooni ainult kauplustes ja terminalides, kus uus versioon on juba saadaval.
- Sama serdi kasutamine mitmes ettevõttes.

## <a name="set-up-certificate-profiles"></a>Serdiprofiilide seadistamine

Järgmisena selgitatakse, kuidas seadistada serdiprofiile. Enne kui kasutate Commerce'i kanalites serdiprofiile, järgige sätete konfigureerimiseks järgmisi samme.

1. Lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Kasutaja määratletud serdiprofiilid jaekaupluste jaoks**.
2. Avage **Süsteemihaldus \> Seadistus \> Serdiprofiilid**.
3. Looge kirje ja määratlege selle jaoks väljad **Serdiprofiil**, **Nimi** ja **Kirjeldus**.

    > [!NOTE]
    > Serdiprofiil on serdi kordumatu identifikaator kõikides ettevõtetes ja Commerce'i komponentides.

3. Lisage rida vahekaardil **Juriidilised isikud** ja valige juriidiline isik (ettevõte), mille jaoks praegust serdiprofiili tuleks kasutada. Kui serdiprofiili tuleks kasutada mitme juriidilise isiku puhul, korrake seda sammu iga täiendava juriidilise isiku jaoks rea lisamiseks.
4. Valige **Sätted**, et avada leht **Serdiprofiili sätted**, kus saate sisestada serdiprofiilile ettevõttespetsiifilisi sätteid.

### <a name="certificate-profile-settings"></a>Serdiprofiili sätted

Kui valite serdiprofiili ridade puhul suvandi **Sätted**, avaneb leht **Serdiprofiili sätted**. See leht võimaldab teil määrata, milliseid serte saab kasutada, kui praegust serdiprofiili Commerce'i kanalites kutsutakse. Samuti saate määrata, millises järjekorras tuleks serte otsida.

> [!NOTE]
> Väli **Prioriteet** seatakse automaatselt. Väärtus **1** tähistab kõrgeimat prioriteeti. Kui lehel **Serdiprofiili sätted** lisatakse uus rida, seatakse selle prioriteediks arv, mis on eelmise rea prioriteedist ühe võrra suurem. Konkreetse rea prioriteedi muutmiseks valige rida ja seejärel valige prioriteedi tõstmiseks **Nihuta üles** või prioriteedi langetamiseks **Nihuta alla**.

Uue rea lisamisel lehel **Serdiprofiili sätted** seadke järgmiste väljade väärtused.

- **Asukoha tüüp** – valige asukoht, kus sert on talletatud. Sellel väljal on kaks võimalikku väärtust: **kohalik sert** ja **võtmehoidla**.
- **Võtmehoidla sert** – see väli on kohustuslik, kui seate välja **Asukoha tüüp** väärtuseks **Võtmehoidla**. Kasutage seda võtmehoidla serdi saladuse määramiseks.

    > [!NOTE]
    > Enne võtmehoidla serdi kasutamist serdiprofiilides laadige sert üles võtmehoidla salvestusruumi ja järgige juhiseid, mis on toodud teemas [Azure'i võtmehoidla klientrakenduse seadistamine](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Kaupluse nimi** – see väli on valikuline ja on saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**. Kasutage seda kaupluse vaikenime määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
- **Kaupluse asukoht** – see väli on valikuline ja on saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**. Kasutage seda kaupluse vaikeasukoha määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.

    > [!NOTE]
    > Kaupluse vaikenimi ja -asukoht lisatakse, et lihtsustada kohalike sertide otsimist lahenduses Commerce Runtime. X509StoreProvideril on loend kaustadest, kus serte talletatakse. Kui kaupluse vaikenimi ja -asukoht on määramata, üritab X509StoreProvider leida serti oma loendi teistest kaustadest.

- **Sõrmejälg** – see väli on kohustuslik ja saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**. Kasutage seda serdi sõrmejälje määramiseks.
- **Kommentaarid** – see väli on valikuline ja võimaldab kasutajatel sisestada märkmeid.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Töövoog: sertide otsimine lahenduses Commerce Runtime

Siin on põhiline töövoog, mida kasutatakse serdi otsimiseks serdiprofiili kutsumise korral Commerce Runtime'is.

1. Süsteem tuvastab, kas serdiprofiilil on praeguse juriidilise isiku jaoks ettevõttespetsiifilisi sätteid.
1. Süsteem püüab leida serti, kasutades lehel **Serdiprofiili sätted** toodud sellise rea väärtusi, mille väli **Prioriteet** väärtuseks on seatud **1**.

    - Kui välja **Asukoha tüüp** väärtuseks on seatud **Võtmehoidla**, kasutatakse välja **Võtmehoidla serdi saladus** väärtust, et otsida serti lehel **Võtmehoidla parameetrid**. Seejärel otsitakse serti võtmehoidla salvestusruumist.
    - Kui välja **Asukoha tüüp** väärtuseks on seatud **Kohalik sert**, otsib X509StoreProvider esiteks serti kaupluse vaikenime ja -asukoha põhjal, kui need parameetrid on määratud. Seejärel otsib see oma kaustaloendi kõigist muudest kaustadest.

1. Kui serti ei leita, korratakse protsessi rea puhul, mille välja **Prioriteet** väärtuseks on seatud **2** jne.

> [!NOTE]
> Kui serdiprofiilil pole praeguse juriidilise isiku jaoks ühtki sätet või kui serdiotsing ebaõnnestub kõikide lehel **Serdiprofiili sätted** toodud ridade puhul, jääb sert leidmata.

#### <a name="caching-the-results-of-certificate-searches"></a>Serdiotsingute tulemuste salvestamine vahemällu

Serdiotsingute tulemused salvestatakse vahemällu. Vahemälu vaikeaegumisaeg on üks tund. Seda aega saab aga kohandada ja selle väärtuseks saab seadistada maksimaalselt 24 tundi.

### <a name="gradual-update"></a>Järkjärguline värskendamine

Kui kasutusele võetakse serdi uus versioon, kuid seda ei saa värskendada samal ajal kõikides kauplustes, võimaldab serdiprofiilide funktsioon serti järk-järgult värskendada.

1. Leidke serdiprofiil ja rida, mida tuleks värskendada, ning seejärel valige **Sätted**.
1. Lisage rida ja määrake sätted, mis on seotud serdi uusima versiooniga.
1. Suurendage uue rea välja **Prioriteet** väärtust. Kasutage nuppu **Nihuta üles**, et liigutada rida nii, et see oleks sama serdi eelmise versiooni rea kohal.

> [!NOTE]
> Commerce Runtime'is kutsutakse serdi uut versiooni esimesena. Kui serti ei olda veel kindlas poes või terminalis värskendatud, kutsutakse eelmist versiooni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]