---
title: Kvaliteettellimused
description: See teema kirjeldab, kuidas käsitsi või automaatselt luua kvaliteettellimusi ning kuidas teha nendega toiminguid ja kirjeldada testitulemusi Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c951716a456101ba753e5c567c80deb4ee7e764f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956631"
---
# <a name="quality-orders"></a>Kvaliteettellimused

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas käsitsi või automaatselt luua kvaliteettellimusi ning kuidas teha nendega toiminguid ja kirjeldada testitulemusi Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Automaatselt loodud kvaliteeditellimused

Saate konfigureerida süsteemi nii, et see loob automaatselt kauba valimi reeglitel põhinevad kvaliteettellimused. Lisateavet vt [Kvaliteedijuhtimise kauba valim](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Kvaliteeditellimuste loomine käsitsi

Kvaliteeditellimuse loomiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Valige suvand **Uus**.
1. Valige **Kvaliteeditellimused** dialoogiakna väljal **Viite tüüp** varude viide, millega teie kvaliteettellimus seotud on. Valimiseks saadaolevate viitetüüpide kirjelduse jaoks vaadake jaotist [Kvaliteeditellimuse viitetüübid](#ref-types) selles teemas järgnevalt.

    > [!NOTE]
    > Valitud viitega seotud varud peavad olema saadaval. Kui valitud viitetüübi, koguse ja varude dimensioonide kombinatsiooni jaoks pole varusid saadaval, saate veateate.

1. Järgige üht alltoodud etappidest, lähtudes väärtusest, mille valisite **Viite tüüp** väljal:

    - Kui valite **Varud**, siis pole täiendavat viiteteavet vaja.
    - Kui valisite **Müügid** või **Ostud**, määrake järgmine teave:

        - **Konto valik** – Viide kliendi- või hankijanumbrile.
        - **Viitenumber** – viide müügitellimuse või ostutellimuse numbrile.
        - **Viite partii** – Viide konkreetsele müügitellimuse reale või ostutellimuse reale.

    - Kui valisite väljal **Viitenumber** valiku **Tootmine**, **Garanti** või **Kaastoote tootmine**, viidake tootmistellimusele, partiitellimusele või garantiitellimuse numbrile.
    - Kui valisite **Marsruudi Toiming**, määrake järgmine teave:

        - **Viitenumber** – viide tootmistellimuse või partiitellimuse numbrile.
        - **Toimingu nr** – Viide konkreetsele marsruudi toimingu numbrile.
        - **Toiming** – Viide konkreetsele marsruudi toimingule.
        - **Ressurss** – Viide konkreetsele ressursile, mida tuleb marsruudi toiminguga kasutada.

1. Valige väljal **Testgrupp** see testi grupp, mida peab läbi viima.
1. Sisestage **Kogus** väljale testitavate kaupade kogus.
1. Jaotisesse **Varude dimensioonid** sisestage mis tahes täiendavad varude dimensioonid, mis on valitud kauba puhul nõutavad.
1. Valige nupp **OK**.

Pärast kvaliteettellimuse loomist saate alustada varude üle vaatamist ja testitulemuste kirjendamist. Lisateavet testitulemuste kirjendamise ja kontrollimise kohta vt [Kauba kvaliteedi kontroll](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Kvaliteettellimuse viitetüübid

Kvaliteettellimusi kasutatakse teie laos määratud varude kontrollimise ja katsetulemuste üksikasjade jälgimiseks. Kvaliteettellimus peab sisaldama viidet, mis esindab testitava laovaru allikat. Kvaliteettellimused võivad olla seotud järgmiste viitetüüpidega:

- **Ladu** – See viitetüüp näitab, et vaatate läbi vaba kaubavaru. Seda tüüpi kontrollid on tavaliselt juhuslikud või plaanimata ning neid tehakse juhul, kui laotöötaja tuvastab probleemi.
- **Müük** – See viitetüüp näitab, et vaatate üle konkreetse müügitellimusega seotud varusid. Seda tüüpi kontrollid on tavaliselt seotud kliendi spetsifikatsioonidega või analüüsitunnistuse (COA) loomisega, mis tuleb kliendile saadetise osana esitada. (CoA-d nimetatakse mõnikord ka vastavustunnistuseks \[CoC\].)
- **Müük** – See viitetüüp näitab, et vaatate üle konkreetse ostutellimusega seotud varusid. Seda tüüpi kontrolli kasutatakse sageli sissetulevate kaupade ülevaatamisel enne nende lattu arvele võtmist või tootmisprotsessides kasutamist.
- **Tootmine** – See viitetüüp näitab, et vaatate üle konkreetse tootmistellimusega seotud varusid. Seda tüüpi kontrolli kasutatakse sageli valminud kaupade ülevaatamisel enne nende lattu arvele võtmist.
- **Garantii** – See viitetüüp näitab, et vaatate üle konkreetse garantiitellimusega seotud varusid. Garantiitellimused on eri tüüpi tellimused, mis jälgivad teie varusid eraldatud laos või eraldatud laoalal. Seda tüüpi kontrolli kasutatakse sageli nende kaupade üle kontrollimiseks, mille klient on tagastanud või mis on antud edasiseks analüüsiks garantiisse. Garantiitellimusi saab luua kvaliteettellimustest. Neid saab luua ka teistest allikatest ning seejärel saab kvaliteettellimusi garantiitellimuste abil määrata.
- **Marsruudi toiming** – See viitetüüp näitab, et kontrollite tootetellimuse marsruudi konkreetse etapiga seotud varusid. Seda tüüpi kontrolle kasutatakse tavaliselt toote töötlemisel (WIP) analüüsimiseks enne selle järgmisse tootmisprotsessi etappi liikumist.
- **Kaastoodete tootmine** – See viitetüüp näitab, et vaatate üle varusid, mis on seotud konkreetse tootmistellimusega seotud kaastoodetega. Seda tüüpi kontrolli kasutatakse tavaliselt partiitellimuse kaastoote ülevaatuseks enne kaastoote lisamist varudesse.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Kvaliteettellimuste kuvamine ja loomine süsteemi erinevatest osadest

Kvaliteettellimusi saab luua käsitsi. Teise võimalusena saab neid automaatselt luua teie määratud kvaliteediseoste põhjal. Lisateavet kvaliteettellimuste automaatse loomise ja haldamise kohta vt [Kvaliteediseosed](quality-associations.md).

Saate kasutada kvaliteettellimuse lehte, et luua käsitsi uus kvaliteettellimus või vaadata teise kirjega seotud kvaliteettellimuse olekut. Kvaliteettellimuse lehele pääsemiseks on mitu viisi.

### <a name="from-the-quality-orders-page"></a>Kvaliteettellimuste lehelt

Kvaliteeditellimuste käsitsi loomiseks ja kõigi olemasolevate kvaliteeditellimuste vaatamiseks, minge **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**. Selle teema ülejäänud jaotised annavad lisateavet selle kohta, kuidas töötada lehega **Kvaliteettellimused**.

### <a name="from-sales-orders"></a>Müügitellimustest

Et töötada teie müügitellimustega seotud kvaliteettellimustega, minge **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused** ja järgige seejärel järgmisi samme:

- Avage müügitellimus või valige see ruudustikus. Seejärel, tegevuspaani vahekaardil **Vali ja paki**, **Kvaliteedijuhtimine** grupis, valige **Kvaliteettellimused**, et avada leht **Kvaliteettellimused**. Seal saate vaadata, luua või uuendada müügitellimusega seotud kvaliteettellimusi.
- Avage müügitellimus ja seejärel valige vahekaardil **Päis** kiirkaart **Üldine**. **Kvaliteettellimuse olek** väli näitab kõigi müügitellimusega seotud kvaliteettellimuste üldist olekut.
- Avage müügitellimus ja seejärel valige vahekaardil **Read** kiirkaart **Müügitellimuse read**. **Kvaliteettellimuse olek** veerus kuvatakse müügitellimuse iga rea olek.

### <a name="from-purchase-orders"></a>Ostutellimustest

Et töötada teie ostutellimustega seotud kvaliteettellimustega, minge **Hanked ja allikad \> Ostutellimused \> Kõik ostutellimused** ja järgige seejärel järgmisi samme:

- Avage ostutellimus või valige see ruudustikus. Seejärel, tegevuspaani vahekaardil **Saamine**, **Kvaliteedijuhtimine** grupis, valige **Kvaliteettellimused**, et avada leht **Kvaliteettellimused**. Seal saate vaadata, luua või uuendada ostutellimusega seotud kvaliteettellimusi.
- Avage ostutellimus ja seejärel valige vahekaardil **Päis** kiirkaart **Üldine**. **Kvaliteettellimuse olek** väli näitab kõigi ostutellimusega seotud kvaliteettellimuste üldist olekut.
- Avage ostutellimus ja seejärel valige vahekaardil **Read** kiirkaart **Ostutellimuse read**. **Kvaliteettellimuse olek** veerus kuvatakse ostutellimuse iga rea olek.

### <a name="from-production-orders"></a>Tootmistellimustest

Et töötada teie tootmistellimustega seotud kvaliteettellimustega, minge **Tootmise kontroll \> Tootmistellimused \> Kõik tootmistellimused** ja järgige seejärel järgmisi samme:

- Avage tootmistellimus või valige see ruudustikus. Seejärel, tegevuspaani vahekaardil **Vaade**, **Kvaliteedijuhtimine** grupis, valige **Kvaliteettellimused**, et avada leht **Kvaliteettellimused**. Seal saate vaadata, luua või uuendada tootmistellimusega seotud kvaliteettellimusi.
- Avage tootmistellimus või valige see ruudustikus. Valige lehe **Tootmistellimus** toimingupaani vahekaardi **Tootmisdetailid** grupis **Marsruut**, et avada leht **Tootmismarsruut**. Marsruudi toimingutega seotud kvaliteettellimuste vaatamiseks järgige neid samme:

    - Valige ruudustikust sihtmarsruudi toiming. Seejärel valige tegevuspaanil **Päringud \> Kvaliteettellimused**.
    - Valige väärtus väljal **Toimingu nr** Väli sihtmarsruudi toimingu jaoks, et avada **Tootmismarsruut** üksikasjade leht. Kiirkaardil **Üldine** näitab **Kvaliteettellimuse olek** kvaliteettellimuste olekut, mis on seotud marsruudi toiminguga.

- Avage tootmistellimus ja valige **Üldine** kiirkaart. Väli **Kvaliteettellimuse olek** näitab kõigi tootmistellimusega seotud kvaliteettellimuste üldist olekut.

### <a name="from-quarantine-orders"></a>Garantiitellimustest

Et töötada teie garantiitellimustega seotud kvaliteettellimustega, minge **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Garantiitellimused** ja järgige seejärel järgmisi samme:

- Vaadake üle **Kvaliteettellimuse olek** veeru väärtused. Sel viisil saate teada kõigi nende kvaliteettellimuste üldise oleku, mis on seotud iga garantiitellimusega ruudustikus.
- Valige ruudustikust garantiitellimus, seejärel tegevuspaanil valige **Kvaliteettellimused**, et vaadata, luua ja uuendada garantiitellimusega seotud garantiitellimusi.

## <a name="advanced-actions-for-quality-orders"></a>Kvaliteettellimuste täpsemad tegevused

Saate teha mitmeid tegevusi kvaliteettellimustega, et hallata olekut, luua dokumente ja uurida lisateavet.

### <a name="reopen-a-quality-order"></a>Kvaliteettellimuse uuesti avamine

Vaikimisi ei saa te enam kvaliteettellimust redigeerida ega värskendada, kui see on kontrollitud ja testid on läbitud. Mõnel juhul võib siiski olla vaja kvaliteettellimus pärast selle lõpetamist uuesti avada.

Kvaliteeditellimuse taasavamiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Avage kvaliteettellimus või valige see ruudustikus.
1. Tegevuspaanil valige **Kvaliteettellimuse taasavamine**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Kvaliteettellimuse analüüsitunnistuse loomine

CoA on aruanne, mille on loonud organisatsiooni kvaliteedi tagamise meeskond. See kinnitab, et toode vastab kindlatele määrustele või nõuetele. Teie kliendid või regulatiivsed tegevuskohad teie geopoliitilistes asukohtades võivad nõuda CoAs-sid. Need võivad olla nõutavad ka teie majandusharu ja teie poolt käsitsetavate, ostetavate, toodetavate või müüdavate toodete tüüpide alusel.

Supply Chain Management võimaldab kvaliteettellimusest luua COA. Aruanne sisaldab kvaliteettellimuse mis tahes testide tulemusi, kui **Analüüsiaruande tunnistus** valik on seatud väärtusele *Jah*. Selle valiku saab vaikimisi määrata lehel **Testid** määratletud testi põhjal. Konkreetse kvaliteeditellimuse jaoks saate siiski teatud testide seadistust muuta.

Kvaliteeditellimuse CoA loomiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Valige kvaliteettellimus, mille jaoks soovite CoA luua.
1. Tegevuspaanil valige **Päringud \> Analüüsitunnistus**.
1. **Analüüsitunnistus** lehel tegevuspaanil, valige **Uus**.
1. Valikuline: **Kontakt** väljal valige kontaktisik, kellele tunnistus tuleb saata.
1. Valige tegevuspaanil suvand **Prindi**.
1. Määrake dialoogiboksis **Analüüsitunnistus**, kuidas aruannet printida. Seejärel valige **OK**, et printida aruanne printerisse, ekraanile, faili või e-kirjaga.
1. Sulgege lehed.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Blokeeri varude kvaliteettellimus või eemalda sellelt blokk

Kui kvaliteediseos genereerib automaatselt kvaliteettellimuse, saab kvaliteedi seosele määratud kauba valimi konfigureerida blokeerima kogu varude koguse viitel, mida testitakse. Lisateavet kauba valimite kohta vt [Kvaliteedihalduse kauba valim](quality-item-sampling.md).

Kui te ei kasuta täielikku blokeerimist või kui loote kvaliteettellimuse käsitsi, loob süsteem automaatselt varude blokeerimise kirje kaubakogusele, mida kvaliteettellimusel testitakse. Salvestatud dokumendis, mis on loodud **Varude blokeerimine** lehel, **varude blokeerimise tüüp** väli on seatud *Kvaliteettellimused*.

Varude blokeerimise vaatamiseks ja redigeerimiseks kvaliteettellimuse puhul, mis on valitud lehel **Varude blokeerimine**, valige tegevuspaanil suvand **Päringud \> Varude blokeerimine**. Lisateavet vt teemast [Varude blokeerimine](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Päringud kvaliteettellimuse üksikasjade kohta

Kasutage järgmisi nuppe **Kvaliteettellimused** lehe tegevuspaanil, et vaadata lisateavet kvaliteettellimuse kohta või sellega seoses.

- **Päringud \> Töö üksikasjad** – Avage leht, kus saate vaadata kvaliteettellimusega seotud laotööd.
- **Päringud \> Mittevastavused** – Avage leht, kus saate vaadata kõiki kvaliteettellimusega seotud mittevastavusi.
- **Ladu** – Selle menüü käsud on ühised kõigi laokannete puhul. Nende abil saate vaadata või värskendada üksikasju, näiteks tehinguid, laos olevaid varusid, broneeringuid ja märgistusi.

### <a name="create-cases-related-to-quality-orders"></a>Kvaliteettellimustega seotud juhtumite loomine

Saate luua kvaliteettellimustega seotud juhtumeid. Sel viisil saate jälgida probleemide üksikasju ja töötada lahenduse leidmiseks. Seejärel saate kasutada juhtumihalduse töövoo funktsioone juhtumi suunamiseks eelmääratletud äriprotsessi kaudu, et saada täiendavaid kinnitusi või saada lisateavet konkreetse probleemi kohta. Teadmusartiklite funktsiooni abil saate luua levinud probleemide lahenduste teadmistebaasi.

## <a name="case-management-examples-for-quality-management"></a>Kvaliteedijuhtimise juhtumihalduse näited

### <a name="example-1"></a>Näide 1

e töötate tootmisettevõttes, mis peab järgima rangeid eeskirju, mis on seotud reguleeritud toodete, näiteks toidu tootmisega. Kvaliteeditellimusi kasutatakse esemete kvaliteedi üksikasjade registreerimiseks ja jälgimiseks kogu tootmisprotsessi vältel. Kui kvaliteettellimus nurjub testil, võib seadmetega probleeme olla. Juhtumeid kasutatakse äriprotsessi jälgimiseks ja probleemi edastamiseks õigetele inseneridele, et saaks määrata algpõhjuse. Äriprotsesside hõlpsamaks jälgimiseks peab ettevõte teadmistebaasi levinud probleemidest, mis on seotud kvaliteettellimuste ja seadmetega.

### <a name="example-2"></a>Näide 2

Te töötate turustusettevõttes, mis saadab tooteid, mida saab kohandada erinevate riikide ja piirkondade jaoks. Mõnel kliendil on ranged täpsustused, mida tuleb järgida. Vastasel juhul võivad tekkida tasud ja tagastused või tagasimaksed. Kvaliteettellimuste abil saate jälgida iga testi üksikasju ja klientide nõuetele vastavaid tulemusi. Juhtumeid kasutatakse CoA üksikasjade ülevaatamiseks ja kinnitamiseks, enne kui dokument luuakse ja seotakse koos teiste saadetiste dokumentidega.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise protsessid](quality-management-processes.md)
- [Kvaliteeditest](quality-tests.md)
- [Kvaliteedi testgrupid](quality-test-groups.md)
- [Kvaliteediseosed](quality-associations.md)
- [Kvaliteedijuhtimise protsessid](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
