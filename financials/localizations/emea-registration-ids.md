---
title: Registreerimise ID-d
description: See teema pakub teavet ja kasutamise registreerimise ID-d.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Registreerimise ID-d

See teema pakub teavet ja kasutamise registreerimise ID-d.

Paljud riigid ja piirkonnad on erinevad ja nõuetega, numbrite või ID-d. See teema annab ülevaate seadete ja toetatud registreerimise tüüpide isikuandmete isikutele erinevates Euroopa riikides/piirkondades. Kõikides riikides/regioonides on toetada erinevaid riigi funktsioone, mis on seotud erinevate liidumaade poolt numbrite puhul. Numbrite näiteks, isikukood (SSN), maksu ID-kood (TIN) ja Euroopa maksukohustuslased (EL KMKR). See funktsioon pakub ühtset raamistikku kõikide riikide kõikides piirkondades, võttes arvesse riigi nõudeid Euroopa riikides. Järgmistes punktides kirjeldatakse üldise teabevahetust, mida kasutatakse loomiseks ja töötlemise registreerimise ID-d.

## <a name="registration-type-creation"></a>Registreerimise tüübi loomine
Enne registreerimise ID sisestamist peate seadistama registreerimise tüüpide registreerimisnumbrid, mis kumbki lepinguosaline on erinevat tüüpi. Mine **organisatsiooni haldamine**&gt;**globaalse**&gt;**registreerimise tüüpide**&gt;**registreerimise tüüpide** luua ja hallata hankijate, klientide, töötajate ja juriidiliste isikute eri riigis registreerimise tüüpide lehte.

|Väli                 |Kirjeldus      |
|------------------------------|----------------------------|                                                                           
| Nimi                | Registreerimise tüübi nimi. |                                                                           
| Kirjeldus         | Registreerimise tüübi kirjeldus. |
| Riik/regioon      | Riigi/regiooni kordumatu kood.|
| Maksuhaldur       | Maksuhaldur, mis on seotud registreerimise tüüp.|
| Kitsendatud       | Selline piirang rakendab maksu registreerimine liigile: ükski isik, organisatsioon.|
| Vorming              | Registreerimise tüübi kinnitamise vormi.|
| Saab uuendada      | Määratletakse kui registreerimistüübi registreerimisnumber saab uuendada pärast seda, kui see on sisestatud.|
| Kordumatu              | Määratleb registreerimistüübi registreerimisnumber on unikaalne. |
| Riigi puhul esmane | Kui pool on seotud üks või rohkem aadresse eelkõige riigi ja registreerimise ID kehtib kõik need aadressid, peavad määrama ühe aadressi riigi primaarseks. Primaarseks saab registreeruda ainult üks nimi. Määratletakse kui registreerimisnumber kantakse ainult puhul esmase aadressi riigi. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Registreerimise tüübi määrata registreerimise kategooria
Registreerimine on riigi registreerimise ID heaks kasutades eelkõige riigi maksu-, tolli- ja muudel eesmärkidel. Selle kategooria määratletakse kinnitusreeglite eriti registreerimise ID (sealhulgas kontrolljärk jne) ja kaasatuse registreerimise erinevaid aruandeid. Lehel **organisatsiooni haldamine**&gt;**globaalse**&gt;**registreerimise tüüpide**&gt;**registreerimine kategooriate** toetatud registreerimise kategooria konkreetses riigis registreerimise tüübi määramiseks.

| Väli            | Kirjeldus|
|-----------------------|----------------|
| Registreerimise tüüp     | Registreerimise tüüp eelkõige riigi.|
| Kitsendatud         | Selline piirang kehtib maksu registreerimise tüüp: ükski isik, organisatsioon.|
| Registreerimiskategooria | Unikaalne registreerimise kood heaks, kasutades. Täielik tugi programmis AX7.1 on kategooriate alla. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Sisestage registreerimise ID-d globaalse aadressiloendi raamatu tarbeks
Globaalse aadressiraamatu (GAB) Microsoft Dynamics 365 operatsioonide sisaldab konsolideeritud aadressiteavet klientide, hankijate, kontaktid, ärisuhete ja juriidilised isikud. Lisateabe saamiseks vaadake teemat [globaalse aadressiloendi raamatust ülevaate](/dynamics365/operations/organization-administration/overview-global-address-book). Pool kirjed salvestatakse globaalse võib sisaldada ühe või mitme aadressi kirje. Neid aadresse kasutatakse erinevatel eesmärkidel, näiteks arvete või tarnimise jaoks. Saate seadistada aadressi teave klientide, hankijate, töötajate ja juriidiliste isikute registreerimise ID-d. Osapool (juriidiline isik, hankija, klient, töötaja) salvestada soovite sisestada registri-ID ja seejärel klõpsake nuppu Otsi **registreerimise ID-d** vormidel seotud isik, juriidiline isik, hankija, klient, töötaja avamiseks ning **aadresside haldamine** lehel. Kohta ning **maksu registreerimine** vahekaardil, klõpsake **lisa**, ja sisestage järgmine teave registreerimise ID-d.

|Väli                |Kirjeldus                                                |
|---------------------|-----------------------------------------------------------|
| Registreerimise tüüp   | Registreerimise tüüp valitud riigi/regiooni.     |
| Registreerimiskood | Partei registreerimise ID-d.                                |
| Kirjeldus         | Kirjeldus registreerimisnumber.               |
| Lõik             | Lisateavet registreerimisnumber. |
| Väljaandev asutus      | Registreerimisnumber väljastanud asutus.        |
| Väljastamise kuupäev         | Väljaantud kuupäeva registreerimisnumbri.              |
| Jõustunud           | Jõustumiskuupäev registreerimisnumber.           |
| Aegumine          | Registreerimisnumber aegumiskuupäeva.          |

> [!NOTE]
> Käibemaksukohuslase kood õigussubjekt, hankija, klient saab valida registreerimine maksu ID-d km ID seotud ja poole kanda.

## <a name="search-for-records-by-registration-id"></a>Otsi kirjeid registreerimise ID järgi
Otsi Partei kirjed registreerimise ID on saadaval vormidel seotud isik, juriidiline isik, hankija, klient ja töötaja. Klõpsake **registreerimise ID otsingut** avamiseks ning **registreerimise ID otsingu kriteeriumid** lehel. Saate määrata otsingukriteeriumid ja klõpsake **leida**. Süsteem kuvab valitud kirjed alates globaalse ja seotud osapoole kirje kohta.

## <a name="supported-registration-categories"></a>Toetatud registreerimise kategooriad
Järgmises tabelis on loetletud toetatud registreerimise tüüpide Dynamics 365 toiminguteks. Kui olete tuttav Microsoft Dynamics AX 2012 väljad registreerimise ID-d, see tabel ka kaardid nende väljade Dynamics 365 toimingute registreerimise puhul.

| Toimingute registreerimine kategooria Dynamics 365         |Riik/regioon  | Dynamics AX 2012 mõiste/välja|
|---------------------------------------------------------------|---------------------|---------------------------------|
| KM-i ID                                                        | Kõikides riikides Euroopa Liidu (EL)|  Maksukohuslase kood (seadusandlikud tüüp AX2012 R3 maksu-ID)|
| Ettevõtte ID (COID)                                          | Belgia Tšehhi Eesti Ungari Läti Leedu Poola Šveits | Ettevõtte number (EnterpriseNumber) registreerimisnumber (RegNum\_W) registreerimisnumber (RegNum\_W) registreerimisnumber (RegNum\_W) registreerimisnumber (RegNum\_W) ettevõtte kood (EnterpriseCode) registreerimisnumber (RegNum\_W) UID (seadusandlikud tüüp UID AX2012 R3) |
| Haru ID                                                     | Belgia            | Pangakontori numbri (BranchNumber)|
| Spisová značka (registreerimisnumber, väljaandev asutus, lõik) | Tšehhi Vabariik     | Vahetükk number (CommercialRegisterInsetNumber) hoitakse kaubanduslikul registreerida äriregistri (CommercialRegisterSection) (CommercialRegister) sektsioon|
| Tollikliendi ID                                           | Soome | Tolli kliendinumber (CustomsCustomerNumber\_ühendus)|
| INN                                                           | Venemaa Föderatsioon| INN (seadusandlikud tüüp INN AX2012 R3)|
| RRC                                                           | Venemaa Föderatsioon| RRC (seadusandlikud tüüp RRC AX2012 R3)|
| KATEGOORIAD OKDP                                                          | Venemaa Föderatsioon| Kategooriad OKDP (seadusandlik tüüp kategooriad OKDP AX2012 R3)|
| OKPO                                                          | Venemaa Föderatsioon| OKPO (seadusandlikud tüüp OKPO AX2012 R3)|
| RCOAD                                                         | Venemaa Föderatsioon| RCOAD (seadusandlik tüüp RCOAD AX2012 R3)|
| OGRN                                                          | Venemaa Föderatsioon| OGRN (seadusandlik tüüp OGRN AX2012 R3) |
| SNILS                                                         | Venemaa Föderatsioon| SNILS (seadusandlik tüüp SNILS AX2012 R3)|
| CIFTS                                                         | Venemaa Föderatsioon| CIFTS (seadusandlik tüüp CIFTS AX2012 R3)|

Rohkem infot registreerimise ID-d töötlemiseks, sealhulgas nõutavad eeldused, vt järgmine ülesanne salvestisi KMKR elutsükli teenused (LCS):

-   KM ID seadistamine
-   Müüja KMKR registreerimine
-    Osapoole otsing KM ID abil



