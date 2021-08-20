---
title: Tasude automaatne eraldamine
description: Microsoft Dynamics 365 Supply Chain Managementi tasude funktsiooni abil saate automaatselt eraldada tasusid ostutellimustele või müügitellimustele.
author: dasani-madipalli
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 04e17947073fca63ab68f0b5d0d72eb8366a1600117f61851179e8b0ed2c8184
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753935"
---
# <a name="automatic-allocation-of-charges"></a>Tasude automaatne eraldamine

[!include [banner](../includes/banner.md)]

Sõltuvalt kliendist, kellega töötate, või müüdavast kaubast, võite soovida rakendada kindlaid lisatasusid. Microsoft Dynamics 365 Supply Chain Managementi *tasude* funktsiooni abil saate automaatselt eraldada tasusid ostutellimustele või müügitellimustele.

Automaatsed tasud või autom. tasud, rakendatakse automaatselt, kui loote müügitellimuse või ostutellimuse. Automaatsed tasud saate määratleda kindlate hankijate, klientide hankija- või kaubagruppide kohta. Saate määratleda ka automaatsed tasud, mis kehtivad kõigi hankijate, klientide või kaupade puhul.

## <a name="set-up-charges-codes"></a>Tasukoodide häälestus

Tasude eraldamiseks peate esmalt määratlema tasukoodid.

1. Järgige üht neist sammudest.

    - Ostutellimuste puhul avage **Ostureskontro \> Tasude seadistamine \> Tasukood**.
    - Müügitellimuste puhul avage **Müügireskontro \> Tasude seadistamine \> Tasukood**.

1. Tasukoodi loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake uue kirje päises järgmised väljad.

    - **Tasukood** – sisestage tasukood.
    - **Kirjeldus** – sisestage tasude kirjeldus.
    - **Kauba käibemaksugrupp** – valige kauba käibemaksugrupp (kui see on olemas).
    - **Proportsionaalne jaotumine** – määrake suvandi väärtuseks *Jah*, kui soovite tasusid proportsionaalselt jaotada. See suvand on saadaval ainult müügitellimuste puhul.
    - **Maksimaalne summa** – sisestage maksimaalne summa, mis selle tasukoodi puhul lubatud on. Seda välja kasutatakse hankija arvete tasude kontrollimiseks. See on saadaval ainult ostutellimustele.

        > [!NOTE]
        > Ostutellimuste tasude kinnitamise funktsiooni sisselülitamiseks avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**. Määrake kiirkaardi **Arve kinnitamine** jaotises **Arve kinnitamine** suvandi **Luba arvete võrdlemise kinnitamine** väärtuseks *Jah*.

1. Kiirkaart **Sisestamine** sisaldab jaotiseid **Deebet** ja **Krediit**. Määrake järgmised väljad, sõltuvalt pearaamatust, kuhu soovite tasud sisestada.

    - **Tüüp** – valige konto tüüp, kuhu sisestate (*Pearaamat*, *Klient* või *Kaup*).
    - **Sisestamine** – valige loodavate sisestuste tüüp (nt *Peatöövõtja tasu* või *Kliendi tasakaalustamine*).
    - **Konto** – valige konto, mille eest tasu sisestate.

1. Valige toimingupaanil nupp **Salvesta**.

## <a name="create-charge-groups"></a>Tasugruppide loomine

Tasugrupid eraldavad kindlaid klientide või hankijate grupi tasusid automaatselt. Järgmised alamjaotised kirjeldavad, kuidas luua ja määrata neid tasugruppe.

### <a name="charge-groups-for-purchase-orders"></a>Ostutellimuste tasugrupid

Ostutellimuste jaoks tasugruppide loomiseks toimige järgmiselt.

1. Avage **Ostureskontro \> Tasude seadistus \> Hankija tasugrupp**.
1. Valige toimingupaanil **Uus**, et lisada rida jaotise ruudustikku ja seejärel määrake järgmised väljad.

    - **Tasugrupp** – sisestage tasugrupi nimi.
    - **Kirjeldus** – sisestage tasugrupi kirjeldus.

1. Valige toimingupaanil nupp **Salvesta**.
1. Avage **Ostureskontro \> Hankijad \> Kõik hankijad** ja avage olemasolev hankija või looge uus hankija.
1. Määrake kiirkaardi **Ostutellimuse vaikeväärtused** jaotise **Ostutellimus** väljale **Tasugrupp** äsja loodud tasugrupp.

### <a name="charge-groups-for-sales-orders"></a>Müügitellimuste tasugrupid

Müügitellimuste jaoks tasugruppide loomiseks toimige järgmiselt.

1. Minge jaotisse **Müügireskontro \> Tasude seadistus \> Kliendi tasugrupid**.
1. Valige toimingupaanil **Uus**, et lisada rida jaotise ruudustikku ja seejärel määrake järgmised väljad.

    - **Tasugrupp** – sisestage tasugrupi nimi.
    - **Kirjeldus** – sisestage tasugrupi kirjeldus.

1. Valige toimingupaanil nupp **Salvesta**.
1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid** ja avage olemasolev klient või looge uus klient.
1. Määrake kiirkaardi **Ostutellimuse vaikeväärtused** jaotise **Müügitellimus** väljale **Tasugrupp** äsja loodud tasugrupp.

## <a name="define-auto-charges"></a>Automaatsete tasude määratlemine

Pärast tasukoodide seadistamist tehke automaatsete tasude määratlemiseks järgmist.

1. Järgige üht neist sammudest.

    - Ostutellimuste puhul avage **Hanked \> Seadistus \> Tasud \> Automaatsed tasud**.
    - Müügitellimuste puhul avage **Müügireskontro \> Seadistus \> Tasude seadistamine \> Automaatsed tasud**.

1. Valige loendipaani väljal **Tase** tase, mille puhul rakendub teie automaatne tasu.

    - *Peamine* – tasud rakendatakse tellimuse päisele.
    - *Rida* – tasud rakendatakse tellimuse ridadele.

1. Valige olemasolev automaatne tasu selle redigeerimiseks või valige **Uus** uue automaatse tasu määratlemiseks.
1. Valige loendist **Konto kood** üks järgmistest väärtustest, et määrata mõjutatud kontode ulatus.

    - *Tabel* – tasud määratakse kindlale kliendile või hankijale.
    - *Grupp* – tasud määratakse lisatasude grupile.
    - *Kõik* – tasud määratakse kõigile klientidele või hankijatele.

1. Valige väljal **Kliendi seos** või **Hankija seos** kindel klient või hankija, kui tegite väljal **Konto kood** valiku *Tabel*. Kui tegite väljal **Konto kood** valiku *Grupp*, valige kliendi või hankija tasugrupp.
1. Valige väljal **Kauba kood** üks järgmistest väärtustest, et määrata mõjutatud kaupade ulatus. Kauba koodi saate valida ainult siis, kui määratlete automaatsed tasud reatasemel.

    - *Tabel* – tasud määratakse kindlale kaubale.
    - *Grupp* – tasud määratakse kauba tasugrupile.
    - *Kõik* – tasud määratakse kõigile kaupadele.

1. Valige väljal **Kauba seos** kindel kaup, kui tegite väljal **Kauba kood** valiku *Tabel*. Kui tegite väljal **Kauba kood** valiku *Grupp*, valige kauba tasugrupp.
1. **Ainult müügitellimuste puhul:** valige väljal **Tarneviisi kood** üks järgmistest väärtustest, et määrata tarneviiside ulatus, mis on mõjutatud.

    - *Tabel* – tasud määratakse konkreetsele tarneviisile.
    - *Grupp* – tasud määratakse konkreetsele tarnegrupile.
    - *Kõik* – tasud määratakse kõigile tarneviisidele.

1. **Ainult müügitellimuste puhul** valige väljal **Tarneviisi seos** kindel tarneviis, kui tegite väljal **Tarneviisi kood** valiku *Tabel*. Kui tegite väljal **Tarneviisi kood** valiku *Grupp*, valige tarneviisi grupp.
1. Määratlege kiirkaardil **Read** tasud ja tasumäärad, mida kasutatakse praeguse automaatse tasu rakendamisel. Saate kasutada selle kiirkaardi tööriistariba nii paljude ridade lisamiseks, kui vajate. Määrake igale reale järgmised väljad.

    - **Valuuta** – valige valuuta, mida tuleks kasutada tasu arvutamiseks.
    - **Tasukood** – valige tasukood.
    - **Kategooria** – valige üks järgmistest väärtustest.

        - *Fikseeritud*– tasu sisestatakse reale fikseeritud summana. Fikseeritud tasusid saab kasutada tellimuse päises ja tellimuse ridadel olevate tasude puhul.
        - *Tk* – tasu põhineb ühikul. Neid tasusid saab kasutada ainult tellimuse ridadel. Need kuvatakse tellimuse kogusumma arvutamisel.
        - *Protsent* – tasu sisestatakse reale protsendina. Tasude protsente saab kasutada tellimuse päises ja tellimuse ridadel olevate tasude puhul.
        - *Kontsernisisene protsent* – tasu sisestatakse kontsernisiseste tellimuste real protsendina. Kontsernisisest protsenti saab kasutada ainult tellimuse ridadel.
        - *Väline* – tasu arvutatakse muu osapoole teenuse alusel, mis on seotud ühe või mitme kättetoimetajaga.

    - **Tasu väärtus** – sisestage tasu väärtus, mis põhineb teie valitud kategoorial.
    - **Tasu valuutakood** – määrake tasule valuuta, kui soovite kasutada väljal **Valuuta** määratletud valuutast erinevat valuutat. Saate kasutada teist valuutat juhul, kui valitud tasukoodile on väljal **Deebeti tüüp** või **Krediidi tüüp** määratud *Pearaamatukonto* või *Kaup*.
    - **Alates summast** – määrake algsumma, millele automaatne tasu rakendada. Summa tähendab selles kontekstis tellimuse kogusummat.
    - **Kuni summani** – määrake lõppsumma, millele automaatne tasu rakendada. Summa tähendab selles kontekstis tellimuse kogusummat.
    - **Käibemaksugrupp** – määrake käibemaksugrupp.
    - **Sait** ja **Ladu** – määrake sait ja ladu, kui tasud tuleb rakendada ainult konkreetsele saidile ja laole.
    - **Säilita** – märkige see ruut tasukannete säilitamiseks pärast arve esitamise lõpule viimist, et tasu rakendataks iga kord, kui valitud kliendikontole uue arve loote.

1. **Ainult müügitellimuste puhul:** kui soovite arvutada mitmetasandilisi tasusid, tutvuge teemaga [Müügitellimuste mitmetasandilised tasud](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders).

## <a name="allocate-charges-from-the-header-to-a-line"></a>Tasude eraldamine päisest reale

Järgmises protseduuris näidatakse kuidas eraldada päisetaseme tasusid reale. Enne selle protseduuri alustamist peaks teil juba olema *fikseeritud summa* tüübiga päisetaseme tasu ja tellimus, mille puhul seda tasu rakendatakse. Lisaks peab tellimus juba sisaldama vähemalt ühte reaüksust.

1. Avage ostutellimus või tasutellimus.
1. Järgige toimingupaanil ühte järgmistest etappidest.

    - Ostutellimuste puhul: valige vahekaardil **Ost** grupis **Tasud** suvand **Tasude eraldamine**.
    - Müügitellimuste puhul: valige vahekaardil **Müük** grupis **Tasud** suvand **Tasude eraldamine**.

1. Määrake dialoogiboksis **Tasude määramine tellimuseridadele** järgmised väljad.

    - **Tasude eraldamine** – valige üks järgmistest väärtustest, et määrata, kuidas tuleks tasusid eraldada.

        - *Netosumma* – eraldage tasud vastavalt iga rea summale kogu netosumma suhtes.
        - *Kogus* – eraldage tasud vastavalt iga rea ühikute arvule, mis on seotud ühikute koguarvuga.
        - *Rea kohta* – eraldage tasud võrdselt ridade koguarvu vahel.

    - **Tasude eraldamine ridadele** – valige väärtus, et määrata, kas tasud tuleks eraldada kõikidele ridadele, ainult positiivsetele ridadele või ainult negatiivsetele ridadele.
    - **Eralda kõik** – märkige see ruut, et eraldada tasud ostutellimuse ridadele ka juhul, kui tasukoodil on muu deebettüüp kui *Kaup*.
    - **Vastuvõetud** – märkige see ruut, et eraldada tasud ainult saadud tellimuse ridadele.
    - **Ladustatud** – märkige see ruut, et eraldada tasud ainult inverteeritud tellimuse ridadele.
    - **Suvandite kuvamine ja kindlate ridade tühjendamine** – märkige see ruut, et välistada sellest eraldamisest konkreetsed read. Kui märgite selle ruudu, siis avaneb ruudustik **Eraldamisest välja arvatud ridade valimine**. See ruudustik sisaldab ainult sätetega **Rea tasude eraldamine** ja **Ladustatud** määratletud kriteeriumidele vastavaid ridu. Näiteks kui teete väljal **Rea tasude eraldamine** valiku *Positiivsed read* ja märgite ruudu **Ladustatud**, kuvatakse ruudustikus ainult need read, mis on positiivsed ja inventeeritud. Lisaks filtreerib ruudustik automaatselt kõik read, millel on kogu kogus juba vastu võetud. Kui ruudustik on avatud, tühjendage märkeruut **Kaasa** iga rea puhul, mis tuleks eraldamisel välistada. 

        > [!IMPORTANT]
        > Kui töötate ruudustikuga **Eraldamisest välja arvatud ridade valimine**, jätke kindlasti ruudustik senikaua avatuks, kuni valite **Eralda**. Kui sulgete ruudustiku enne valiku **Eralda** tegemist, lähevad teie ruudustiku sätted kaotsi. Seega tasud eraldatakse vastavalt eelnevalt määratletud kriteeriumitele.

1. Valige **Eralda**, et rakendada oma sätted ja sulgeda päringu dialoogiboks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]