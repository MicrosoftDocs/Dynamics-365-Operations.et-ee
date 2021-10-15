---
title: Integratsiooni konfigureerimine Dayforce’iga
description: See teema kirjeldab vajalikke konfigureerimisetappe, mida on vaja Microsoft Dynamics 365 Human Resources ja Ceridian Dayforce'i vaheliseks integreerimiseks.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f92850a741f2a0d4d1c2636cbbdf21fe95f307df
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559457"
---
# <a name="configure-integration-with-dayforce"></a>Integratsiooni konfigureerimine Dayforce’iga

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduste Microsoft Dynamics 365 Human Resources ja Ceridian Dayforce vaheline integratsioon sõltub mitmest konfiguratsioonietapist, mida kirjeldatakse selles teemas. Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Human Resources kui ka Dayforce.

Kui te kasutate palgatöötluste tegemiseks teenust, nagu Dayforce, siis peate rakenduses Human Resources integratsiooni lubama. Integratsiooni jaoks on rakendusest Human Resources vaja teatud andmeid. Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Human Resources konfigureeritud viisil, mis lubab integratsiooni. Integratsioon kasutab järgmisi üldisi andmekategooriaid.

- Inimressursside andmed
- Hüvituse andmed
- Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid
- Töötaja andmed

See teema kirjeldab samme, mida peate järgima integratsiooni lubamiseks ja selgitab andmetüüpe ja konfiguratsiooni üksikasju, mida integratsioon nõuab.

## <a name="enable-the-integration"></a>Integratsiooni lubamine

Dayforce’iga ühendamiseks peate rakenduses Human Resources sisse lülitama integratsiooni ja sisestama konfigureerimisteabe. Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 Finance, siis peate seadistama Microsoft Azure’i salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance.

Integratsiooni sisselülitamiseks rakenduses Human Resources järgige neid samme.

1. Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.
2. Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.
3. Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.
4. Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.

Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus. Vajaduse korral saate seda sagedust muuta.

Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.

- [Azure’i salvestuskontod](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Azure’i salvestusruumi ühendusstringide konfigureerimine](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Tehnilised üksikasjad, kui palga integratsioon on lubatud

Palga integreerimise sisselülitamisel on kaks peamist mõju.

- Luuakse andmete ekspordi projekt nimega "Palga integreerimise eksport". See projekt sisaldab palga integreerimise jaoks nõutavaid üksusi ja välju. Projekti uurimiseks avage **Süsteemihaldus**, valige paan **Andmehaldus** ja avage projektiloendist andmete projekt.
- See pakett-töö käivitab andmete eksportimise projekti, krüptib tulemuste andmete paketi ja edastab andmete paketi faili SFTP-lõpp-punktile, mis on konfigureeritud kuval **integratsiooni konfiguratsioon**.

> [!NOTE]
> SFTP-lõpp-punkti edastatud andmete pakett krüptitakse, kasutades võtit, mis on paketile kordumatu. Võti on Azure võtmehoidlas, mis on kättesaadav ainult Ceridianile. Andmebaasi sisu ei saa dekrüptida ja uurida. Kui teil on vaja uurida andmepaketi sisu, peate eksportima projekti "Palga integreerimise eksport" käsitsi, selle alla laadima ja seejärel avama. Käsitsi eksportimine ei rakenda krüptimist ega edasta paketti.

## <a name="configure-your-data"></a>Andmete konfigureerimine 

Palgaarvestuse töötlemiseks peate konfigureerima personaliandmeid rakenduses Human Resources. Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta. Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.

### <a name="human-resource-data"></a>Personaliandmed

#### <a name="benefits"></a>Soodustused 

Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.

Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.

##### <a name="benefit-plans"></a>Soodustusplaanid

- Plaan (kohustuslik)
- Tüüp (kohustuslik)
- Palga mõju (kohustuslik)
- Võlgnevuste sissenõudmine
- Mahaarvamismeetod
- Mahaarvamise prioriteet
- Perioodi piiramine
- Piirsumma

##### <a name="benefits"></a>Soodustused

- Plaan (kohustuslik)
- Tüüp (kohustuslik)
- Suvand (kohustuslik)
- Soodustuse ID (kohustuslik)
- Sagedus
- Alus
- Summa või määr
- Tulukood

##### <a name="supported-frequencies"></a>Toetatud sagedused 

- Iga nädal
- Kahe nädala tagant
- Iga poole kuu tagant
- Kord kuus

##### <a name="supported-bases"></a>Toetatud alused 

- Fikseeritud summa
- Tulu protsent
- Produktiivsed tunnid

Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.

| Valik rakenduses Human Resources        | Tulemus rakenduses Dayforce                            |
|----------------------------|-----------------------------------------------|
| Puudub                       | Mahaarvamist ei looda.                      |
| Ainult mahaarvamine             | Luuakse töövõtja mahaarvamine.             |
| Ainult lisamine          | Luuakse tööandja mahaarvamine.             |
| Mahaarvamine ja lisamine | Luuakse töövõtja ja tööandja mahaarvamised. |

Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest teemadest.

- [Töötaja soodustuste programmi pakkumine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Uue soodustuse loomine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Soodustuskõlblikkuse reeglite ja poliitikate määratlemine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Töötajate soodustuste registreerimine ja eemaldamine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Hüvitus 

Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks. Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu. Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.

Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks. Nõutavad on põhipalgaplaanid ja palgamäära teisendamised. Töövõtjad peavad olema seotud põhipalgaplaaniga.

Lisateavet hüvitusplaanide kohta vaadake järgmistest teemadest.

- [Põhipalga plaanide loomine](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Ergutussüsteemi plaanide loomine](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Palga/hüvituse struktuuri ja plaanide arendamine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Hüvitusprotsess](/dynamics365/unified-operations/talent/process-compensation)
- [Hüvitusprotsessi määratlemine ja tulemuste arvutamine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Töötaja liitmine põhipalga plaaniga](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Töötaja liitmine tulemustasu plaaniga](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Tööd 

Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum. Lisateavet vt järgmistest teemadest:

- [Töö komponentide seadistamine](/dynamics365/unified-operations/talent/create-job)
- [Uute tööde määratlemine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Ametikohad

Ametikoht on töökoha üksik eksemplar. Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti. Ametikoht kuulub osakonna alla. Iga ametikohaga saab seostada vaid ühte töötajat.

Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.

- Ametikoht (kohustuslik)
- Kirjeldus (kohustuslik)
- Töö (kohustuslik)
- Osakond (kohustuslik)
- Ametikoha tüüp (kohustuslik)
- Täistööaja vaste
- Iga-aastased regulaarsed tunnid (kohustuslik)
- Maksja juriidiline isik (kohustuslik)
- Palgatsükkel (kohustuslik)
- Vaike-finantsdimensioonid – kulukeskus (kohustuslik)
- Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood

Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.

Lisateavet vt järgmistest teemadest:

- [Tööjõu korraldamine osakondade, tööde ja ametikohtade abil](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Ametikohtade seadistamine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Osakonnad

Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala. Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid. Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks. Osakonnad võivad vastutada kasumi ja kahjumi eest.

Lisateavet vt järgmistest teemadest:

- [Osakonna loomine ja selle seostamine osakonnahierarhiaga](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Uute osakondade määratlemine](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Palgatsüklid ja makseperioodid

Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse. Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval. Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu. Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.

Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid. Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel. Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.

Dayforce kasutab järgmist teavet.

- Palgatsükkel (kohustuslik)
- Palgatsükli sagedus (kohustuslik)
- Perioodi alguskuupäev (esimene makseperiood on kohustuslik)
- Makse vaikekuupäev (esimene makseperiood on kohustuslik)

See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga. Enne integreerimist peab olema loodud vähemalt üks makseperiood. Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Human Resources määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.

#### <a name="earning-codes"></a>Tulukoodid

Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad. Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.

Dayforce kasutab järgmist teavet.

- Tulukood (kohustuslik)
- Kirjeldus
- Mõõtühik
- Produktiivne

### <a name="worker-data"></a>Töötaja andmed

Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks. Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.

Töötajate kohta saate hallata järgmist teavet.

- **Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.
- **Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.
- **Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.
- **Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.

Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.

#### <a name="general-information"></a>Üldteave

- Töötaja number (kohustuslik)
- Eesnimi (kohustuslik)
- Perekonnanimi (kohustuslik)
- Teine eesnimi
- Staaž kuupäeval
- Tuntud kui

#### <a name="personal-information"></a>Isikuandmed

- Perekonnaseis (kohustuslik)
- Sünnikuupäev (kohustuslik)
- Sugu (kohustuslik)
- Puudega isik
- Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)

#### <a name="address-information"></a>Aadressiteave

- Tänava nimi ja hoone number (kohustuslik)
- Riik/regioon (kohustuslik)
- Sihtnumber (kohustuslik)
- Tänava number (kohustuslik) (ainult Mehhiko puhul)
- Hoone tähis (ainult Mehhiko puhul)
- Linn (kohustuslik)
- Osariik (kohustuslik)
- Maakond (kohustuslik)

#### <a name="contact-information"></a>Kontaktteave 

- Tänava nimi ja hoone number (kohustuslik)
- Kontaktnumber (kohustuslik)
- Sisetelefon

#### <a name="payroll-information-and-earning-codes"></a>Palgateave ja tulukoodid

Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid. Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.

##### <a name="earning-codes"></a>Tulukoodid

- Ametikoht (kohustuslik)
- Tulukood (kohustuslik)
- Maksesagedus (kohustuslik)
- Summa (kohustuslik)

##### <a name="payroll-information"></a>Palgateave

- Makseviis
- Majanduspiirkond (kohustuslik)
- Töövõtja soodustuste ID
- Riiklik isikukood (kohustuslik)
- Sõjaväeteenistuse number
- Vahetuse ID (kohustuslik)
- Maksukood (kohustuslik)
- Ühingu ID (kohustuslik)
- Tööpäeva ID (kohustuslik)
- Tööloa number

> [!NOTE]
> Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**. Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.

#### <a name="employment-details"></a>Töösuhte üksikasjad

Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud. Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.

- Töösuhte alguskuupäev (kohustuslik)
- Töösuhte lõppkuupäev
- Alguskuupäev
- Korrigeeritud alguskuupäev
- Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)
- Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)

Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.

| Inimressursid                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Kõige värskem palkamise kuupäev | Praeguse lõpetamata töösuhte ajalookirje alguskuupäev                                 |
| Lõpetamiskuupäev      | Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev                                 |
| Alguskuupäev            | Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev |
| Palkamise algne kuupäev    | Varaseima töösuhte ajalookirje alguskuupäev                                               |

#### <a name="compensation"></a>Hüvitus

Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan. See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.

- Kehtivuse algus (kohustuslik)
- Aegumiskuupäev
- Palgamäär (kohustuslik)
- Palgamäära teisendamised (kohustuslik)
- Aastane vaste (kohustuslik)
- Tunnine vaste (kohustuslik)

Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana. Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.

Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.

#### <a name="identification-numbers"></a>ID-numbrid

##### <a name="social-security-identifier"></a>Isiku identifikaator 

Igal töövõtjal peab olema üks peamine identifikaator. Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi. Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.

- Peamine isikukood (kohustuslik)
- ID tüüp = SSN
- Väljastamise kuupäev
- Aegumiskuupäev

Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit. Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.

#### <a name="bank-accounts-and-disbursements"></a>Pangakontod ja väljamaksed

Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.

| Inimressursid                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Pangakonto number (kohustuslik) |                                                                                                             |
| SWIFT-kood (kohustuslik)          | Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.                                                             |
| Filiaali kood (kohustuslik)       |                                                                                                             |
| Pangakonto tüüp (kohustuslik)   | Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos. Toetatud väärtused on **Jooksevkonto** ja **Palgakonto** |

> [!NOTE]
> Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga. Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.

#### <a name="address-information"></a>Aadressiteave

Igal töövõtjal peab olema üks peamine asukoht. Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.

- Peamine elukoht (kohustuslik)
- Riik/regioon (kohustuslik)
- Sihtnumber (kohustuslik)
- Tänava nimi (kohustuslik)
- Tänava number (kohustuslik)
- Hoone tähis
- Linn (kohustuslik)
- Osariik (kohustuslik)
- Maakond (kohustuslik)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas

Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.

- Ametikohtadele tuleb määrata osakonnad.
- Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.

> [!NOTE] 
> Saate rakenduse Human Resources konfigureerida nõudma osakonna määratlemist ametikohtade poolt. Selleks valige **Inimressursside ühised ametikohad > Ametikohad > Nõua ametikohtade puhul osakondi**. Soovitame selle sätte integreerimiseks jõustada.

### <a name="job-types"></a>Töötüübid

Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks. Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas. Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk. Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.

Järgmised töötüübid ja kirjeldused on kohustuslikud.

| Töö tüüp   | Kirjeldus |
|------------|-------------|
| Tunnimäär     | Tunnimäär      |
| Põhipalk   | Põhipalk    |

### <a name="position-types"></a>Ametikoha tüübid 

Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud. Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.

Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.

| Ametikoha tüüp   | Kirjeldus        |
|-----------------|--------------------|
| Täistööaeg       | Täistööajaga töövõtja |
| Osaline tööaeg       | Osalise tööajaga töövõtja |

### <a name="reason-codes"></a>Põhjuse koodid

Põhjusekoodid annavad teavet töövõtja oleku kohta. Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.

Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.

| Põhjusekood    | Kirjeldus      | Rakendatavad stsenaariumid |
|----------------|------------------|----------------------|
| RESIGNATION    | Lahkumine      | Töötajaga lepingu lõpetamine     |
| TERMINATION    | Lõpetamine      | Töötajaga lepingu lõpetamine     |
| RETIREMENT     | Pensionile jäämine       | Töötajaga lepingu lõpetamine     |
| OTHER          | Muud põhjused    | Töötajaga lepingu lõpetamine     |
| DEATH          | Surm            | Töötajaga lepingu lõpetamine     |
| LEAVEOFABSENCE | Puhkus | Töötajaga lepingu lõpetamine     |
| CONTRACTEND    | Lepingu lõpetamine  | Töötajaga lepingu lõpetamine     |
| SALARYCHANGE   | Palga muutus | Hüvitus         |

### <a name="marital-status"></a>Perekonnaseis

Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.

Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.

| Inimressursid                 | Dayforce             |
|------------------------|----------------------|
| Abielus                | Abielus              |
| Üksik                 | Üksik               |
| Lesk                | Lesk              |
| Lahutatud               | Lahutatud             |
| Registreeritud partnerlus | Mitteabieluline kooselu |
| None                   | None                 |
| Kooselu             | Kooselu           |

### <a name="gender"></a>Sugu

Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.

Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.

| Inimressursid       | Dayforce        |
|--------------|-----------------|
| Mees         | Mees            |
| Naissoost       | Naissoost          |
| Mittespetsiifiline | *Ei toetata* |

### <a name="earning-codes"></a>Tulukoodid

Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad. Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime. Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.

#### <a name="supported-frequencies"></a>Toetatud sagedused

- Kõik
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Aadressid

Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad. Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.

| Inimressursid          | Dayforce              |
|-----------------|-----------------------|
| Riik/regioon  | Riigi kood          |
| Sihtnumber | Sihtnumber           |
| Osariik           | Osariigi kood            |
| Linn            | Linn                  |
| Maakond          | Maakond (haldusüksus) |
| Tänav          | Aadressirida 1        |

### <a name="tax-regions"></a>Maksuregioonid

Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks. Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena. Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga. 

- Maksuregioon (kohustuslik)
- Riik/regioon (kohustuslik)
- Osariik (kohustuslik)
- Maakond 
- Linn (kohustuslik)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Andmete konfigureerimine palgaandmete loomiseks Mehhikos

Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.

- Ametikohtadele tuleb määrata osakonnad.
- Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.

### <a name="job-types"></a>Töötüübid

Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks. Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid. Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk. Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.

Järgmised töötüübid ja kirjeldused on kohustuslikud.

| Töö tüüp   | Kirjeldus |
|------------|-------------|
| Tunnimäär     | MX tunnimäär   |
| Põhipalk   | MX põhipalk |

### <a name="position-types"></a>Positsioonitüübid 

Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud. Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.

Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.

| Ametikoha tüüp   | Kirjeldus        |
|-----------------|--------------------|
| Täistööaeg       | Täistööajaga töövõtja |
| Osaline tööaeg       | Osalise tööajaga töövõtja |

### <a name="reason-codes"></a>Põhjuse koodid

Põhjusekoodid annavad teavet töövõtja oleku kohta. Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.

Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.

| Põhjusekood            | Kirjeldus                    | Rakendatavad stsenaariumid |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Lahkumine enne esimest palgamakset | Töötajaga lepingu lõpetamine     |
| RESIGNATION            | Lahkumine                    | Töötajaga lepingu lõpetamine     |
| PENSION                | Pension                        | Töötajaga lepingu lõpetamine     |
| TERMINATION            | Lõpetamine                    | Töötajaga lepingu lõpetamine     |
| RETIREMENT             | Pensionile jäämine                     | Töötajaga lepingu lõpetamine     |
| ABSENTEE               | Puuduja                       | Töötajaga lepingu lõpetamine     |
| OTHER                  | Muud põhjused                  | Töötajaga lepingu lõpetamine     |
| CLOSURE                | Ettevõte suletud               | Töötajaga lepingu lõpetamine     |
| DEATH                  | Surm                          | Töötajaga lepingu lõpetamine     |
| LEAVEOFABSENCE         | Puhkus               | Töötajaga lepingu lõpetamine     |
| CONTRACTEND            | Lepingu lõpetamine                | Töötajaga lepingu lõpetamine     |
| SALARYCHANGE           | Palga muutus               | Hüvitus         |

### <a name="terms-of-employment"></a>Töösuhte tingimused

Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks. Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.

Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.

| Töösuhte tingimused   | Kirjeldus |
|-----------------------|-------------|
| Tavaline               | Tavaline     |
| Otse                | Otse      |
| Praktika            | Praktika  |
| Alaline             | Alaline   |

### <a name="marital-status"></a>Perekonnaseis

Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.

Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.

| Inimressursid                 | Dayforce                  |
|------------------------|---------------------------|
| Abielus                | Abielus                   |
| Üksik                 | Üksik                    |
| Lesk                | Lesk                   |
| Lahutatud               | Lahutatud                  |
| Registreeritud partnerlus | Mitteabieluline kooselu      |
| None                   | *Pole Mehhikos toetatud* |
| Kooselu             | *Pole Mehhikos toetatud* |

### <a name="gender"></a>Sugu

Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.

Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.

| Inimressursid       | Dayforce                  |
|--------------|---------------------------|
| Mees         | Mees                      |
| Naissoost       | Naissoost                    |
| Mittespetsiifiline | *Pole Mehhikos toetatud* |

### <a name="payment-method"></a>Makseviis

Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse. Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.

Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.

| Inimressursid             | Dayforce                  |
|--------------------|---------------------------|
| Sularaha               | Sularaha                      |
| Elektrooniline makse | Ülekanne                  |
| Kontrolli              | Tšekk                    |
| Pangaveksel         | *Pole Mehhikos toetatud* |
| Muud              | *Pole Mehhikos toetatud* |

### <a name="bank-account-type"></a>Pangakonto tüüp

Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele. Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena. Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.

| Inimressursid            | Dayforce                  |
|-------------------|---------------------------|
| Jooksevkonto  | Jooksevkonto           |
| Palgakonto   | Palgakonto            |
| Hoiukonto   | *Pole Mehhikos toetatud* |
| BankGiroti konto | *Pole Mehhikos toetatud* |
| PlusGiroti konto | *Pole Mehhikos toetatud* |

### <a name="earning-codes"></a>Tulukoodid

Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad. Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime. Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.

#### <a name="supported-frequencies"></a>Toetatud sagedused

- Kõik
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Aadressid

Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad. Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.

| Inimressursid              | Dayforce              |
|---------------------|-----------------------|
| Riik/regioon      | Riigi kood          |
| Sihtnumber     | Sihtnumber           |
| Osariik               | Osariigi kood            |
| Linn                | Linn                  |
| Maakond              | Maakond (haldusüksus) |
| Tänav              | Aadressirida 1        |
| Majanumber       | Aadressirida 2        |
| Hoone tähis | Aadressirida 5        |

### <a name="passport-number"></a>Passi number

Töötajad saavad deklareerida passi teavet. See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.

- Identifitseerimistüüp = pass
- Väljastamise kuupäev
- Aegumiskuupäev

Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit. Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje. Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
