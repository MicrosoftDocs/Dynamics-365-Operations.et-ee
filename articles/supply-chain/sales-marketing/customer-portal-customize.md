---
title: Kliendiportaali kohandamine ja kasutamine
description: Selles teemas selgitatakse, kuidas kohandada kliendiportaali pärast teie süsteemi lisamist.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e491100bc24718b8e5bc0f62de241835787f7ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980852"
---
# <a name="customize-and-use-the-customer-portal"></a>Kliendiportaali kohandamine ja kasutamine

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse erinevaid lehti, mis on valmiskujul kliendiportaalis saadaval. Selles seletatakse, mida lehed teevad ja kuidas saate neid kohandada.

Kliendiportaal pakub valmiskujul mõningaid veebilehti ja toiminguid. Järgmine saidikaart annab ülevaate nendest veebisaitidest ja toimingutest ning samuti rollidest, mis saavad nimetatud toiminguid teha.

![Kliendiportaali saidikaart](media/customer-portal-site-map.png "Kliendiportaali saidikaart")

## <a name="typical-customizations"></a>Tavalised kohandused

Järgmised teemad aitavad teil õppida Power Appsi portaalide põhitõdesid ning portaalide kohandamise viise.

- [Töö mallidega](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – selles teemas antakse üldine ülevaade sellest, kuidas Power Appsi portaalid toimivad ja kuidas saate teha portaalides lihtsamaid kohandusi.
- [Portaali sisu haldamine](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – selles teemas selgitatakse, kuidas saate hallata ja kohandada sisu, mida oma portaalis kasutate.
- [CSS-i redigeerimine](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – see teema aitab teil teha oma portaali kasutajaliidese keerukamaid kohandusi.
- [Portaali jaoks teema loomine](https://docs.microsoft.com/dynamics365/portals/create-theme) – selles teemas aidatakse teil luua oma portaali kasutajaliidese teema.
- [Portaali sisu lihtne loomine ja esitamine](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – selles teemas aidatakse teil hallata alusandmeid ja -tabeleid, mida oma portaalis kasutate.
- [Kontakti konfigureerimine portaalis kasutamiseks](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – selles teemas selgitatakse, kuidas luua ja kohandada kasutajarolle ning kuidas toimivad Power Appsi portaalide turve ja autentimine.
- [Teadete konfigureerimine portaalide tabeli- ja veebivormide jaoks](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – selles teemas selgitatakse, kuidas lisada portaali dokumente ja täiendavat mäluruumi.
- [Portaali veebisaidi tõrketöötlus](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – selles teemas selgitatakse, kuidas kuvada portaali tõrkelogisid ja salvestada neid oma Microsoft Azure'i bloobimälu kontol.

## <a name="customize-the-order-creation-process"></a>Tellimuse loomise protsessi kohandamine

Kui kasutaja esitab kliendiportaali kasutades tellimuse, siis sünkroonitakse tellimus automaatselt asjakohase Dynamics 365 Supply Chain Managementi keskkonnaga. Kuna kasutaja on välisklient, siis on osa nõutavast teabest tema eest tahtlikult peidetud. See teave täidetakse automaatselt vormi esitamisel.

Selles jaotises näidatakse, kuidas peaksite seadistama kontakte, et vältida tõrkeid. See selgitab automaatselt määratud väljasid ning seda, kuidas saate vajadusel nende väljade väärtusi muuta.

### <a name="the-out-of-box-order-creation-process"></a>Valmiskujul tellimuse loomise protsess

Siit leiate standardetapid tellimuse esitamiseks kliendiportaali kaudu.

1. Valige avalehel viisardi **Tellimuse loomine** avamiseks paan **Tellimuse loomine**.
1. Seadistage lehel **Tellimuse teave** järgmised väljad.

    - **Nõutav sissetulekukuupäev** – täpsustage tarnekuupäev.
    - **Tarneaadress** – sisestage aadress, kuhu tellimus tuleks tarnida.
    - **Ettevõte** – valige kliendi ettevõtte nimi. See väli määratakse mitteadministraatorist kasutajate jaoks automaatselt.
    - **Ostutellimuse number** – sisestage tellimuse ostutellimuse number. See väli ei ole kohustuslik.
    - **Tarni riiki/piirkonda** – sisestage riik või piirkond, kuhu kaubad tarnitakse. See väli määratakse mitteadministraatorist kasutajate jaoks automaatselt.

    ![Tellimuse teabeleht](media/customer-portal-order-information.png "Tellimuse teabeleht")

1. Valige **Edasi**.
1. Valige lehel **Kaubad** suvand **Lisa kaup**.

    ![Kaupade leht](media/customer-portal-items.png "Kaupade leht")

1. Määrake dialoogiboksis **Kauba teave** järgmised väljad.

    - **Toote nimi** – otsige ja valige toode, mida tellimusele lisada.
    - **Kogus** – sisestage valitud toote kogus.
    - **Ühik** – määrake mõõtühik (nt **ea.**, **kg** või **kast**).
    - **Eeldatav netosumma** – väärtus arvutatakse kauba eeldatava hinna ja valitud üksuse koguse korrutisena.

    ![Kauba teabe dialoogiboks](media/customer-portal-item-information.png "Kauba teabe dialoogiboks")

1. Kauba tellimusele lisamiseks valige **Esita**.
1. Korrake samme 4–6, kuni olete lisanud kõik kaubad, mida soovite tellida.
1. Kui olete kaupade lisamise lõpetanud, klõpsake lehel **Kaubad** nuppu **Edasi**.
1. Lehel **Tellimuse teave** esitatakse tellimuse kokkuvõte. Vaadake üle tellimuse sisu ja tarne üksikasjad. Kui kõik tundub õige, siis valige tellimuse esitamiseks suvand **Esita**.

    ![Tellimuse teabeleht](media/customer-portal-order-submit.png "Tellimuse teabeleht")

### <a name="standard-data-setup"></a>Standardandmete seadistus

Sujuva kasutajakogemuse tagamise otstarbel täidab kliendiportaal mitme nõutava välja väärtused automaatselt. Need väärtused põhinevad tellimust esitava kliendi kontaktikirjes toodud teabel.

Kliendiportaali tellimuste esitamiseks kasutava kliendi iga [kontaktirida](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) kohta tuleb täpsustada järgmiste nõutud väljade väärtused. Vastasel juhul ilmnevad tõrked.

- **Ettevõte** – juriidiline isik, kellele tellimus kuulub
- **Potentsiaalne klient** – tellimusega seotud kliendikonto
- **Hinnakiri** – kliendi jaoks kohandatud hinnakiri
- **Valuuta** – hinna valuuta
- **Tarni riiki/piirkonda** – riik või piirkond, kuhu kaubad tarnitakse

Müügitellimuse tabeli jaoks on automaatselt täidetud järgmised väljad.

- **Keel** – tellimuse keel (väärtus võetakse vaikimisi kontaktikirjest).
- **Tarni riiki/piirkonda** – riik või piirkond, kuhu kaubad tarnitakse (väärtus võetakse vaikimisi kontaktikirjest).
- **Kontaktisik** – kasutaja, kelle poole pöörduda tellimuse kohta käiva teabe puhul (väärtus võetakse vaikimisi kontaktikirjest).
- **Ettevõte** – juriidiline isik, kellele tellimus kuulub (väärtus võetakse vaikimisi kontaktikirjest).
- **Potentsiaalne klient** – tellimusega seotud kliendikonto (väärtus võetakse vaikimisi kontaktikirjest).
- **Arve klient** – tellimuse arvelduskonto (vaikeväärtus on kontaktikirjes toodud potentsiaalne klient).
- **Müügitellimuse nimi** – müügitellimuse nimi (vaikeväärtus on **müügitellimus**).
- **Valuuta** – hinna valuuta (väärtus võetakse vaikimisi kontaktikirjest).
- **Hinnakiri** – kliendi jaoks kohandatud hinnakiri (väärtus võetakse vaikimisi kontaktikirjest).
- **Tarneaadressi kirjeldus** – müügitellimuse tarneaadress (vaikeväärtus on **tarneaadressi kirjeldus**).

### <a name="modify-the-order-creation-process"></a>Tellimuse loomise protsessi muutmine

Te saate vabalt muuta kliendiportaali välimust ja kasutajaliidest, kui te ei muuda tellimuse loomise põhiprotsessi. Kui soovite muuta tellimuse loomise protsessi, siis tuleb meeles pidada mõned asjad.

Ärge eemaldage Microsoft Dataverse’is müügitellimuse tabelist järgmisi veerge, kuna need on vajalikud müügitellimuse loomisel topeltkirjutuse jaoks.

- **Ettevõte** – juriidiline isik, kellele tellimus kuulub
- **Nimi** – müügitellimuse nimi
- **Valuuta** – hinna valuuta
- **Hinnakiri** – kliendi jaoks kohandatud hinnakiri
- **Tarni riiki/piirkonda** – riik või piirkond, kuhu kaubad tarnitakse
- **Potentsiaalne klient** – tellimusega seotud kliendikonto
- **Keel** – tellimuse keel (tavaliselt on see potentsiaalse kliendi keel).
- **Tarneaadressi kirjeldus** – müügitellimuse tarneaadress

Kaupade puhul on järgmised veerud kohustuslikud.

- **Toode** – tellitav toode
- **Kogus** – valitud toote kogus
- **Ühik** – mõõtühik (nt **ea.**, **kg** või **kast**)
- **Tarni riiki/piirkonda** – tarneriik või -piirkond
- **Tarneaadressi kirjeldus** – tellimuse tarneaadress

Peate veenduma, et kliendiportaal esitaks kuidagi kõigi nende veergude väärtused.

Kui soovite lehele veerge lisada või neid eemaldada, vt teemat [Kiirloomise vormide loomine või redigeerimine sujuvaks andmesisestuseks](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Kui soovita muuta veergude eelseadistust ning seda, kuidas väärtused lehe salvestamisel seadistatakse, siis tutvuge Power Appsi portaalide dokumentatsioonis järgmise teabega.

- [Välja eeltäitmine](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Määra väärtus salvestamisel](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Avalehe kohandamine

Kõik kliendiportaali juhtelemendid on Power Appsi portaalide sisseehitatud juhtelemendid. Te saate neid kohandada, järgides Power Appsi portaalide dokumentatsiooni jaotist [Lehe koostamine](https://docs.microsoft.com/powerapps/maker/portals/compose-page).

Ainus kliendiportaali malli kaasatud kohandatud juhtelement on mõeldud avalehel paanide loomiseks.

![Avalehe paanid](media/customer-portal-home-page-tiles.png "Avalehe paanid")

Paanide muutmiseks toimige järgmiselt.

1. Avage [portaalihalduse rakendus](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).
1. Valige navigeerimispaanilt vasakult suvand **Lehe mallid**.

    ![Portaalihalduse navigeerimispaan](media/customer-portal-nav.png "Portaalihalduse navigeerimispaan")

1. Valige lehe mall, mille nimi on **Avaleht**.
1. Valige väljal **Veebimall** link **Avaleht**, et avada selle lehe lähtekood.

    ![Veebimalli väli](media/customer-portal-web-template.png "Veebimalli väli")

1. Nüüd peaksite nägema kogu avalehe lähtekoodi ja saate seda vajaduse järgi muuta.

## <a name="resources"></a>Ressursid

Lisateavet kliendiportaali seadistamise ja kohandamise kohta leiate järgmistest allikatest.

- [Power Appsi portaalide dokumentatsioon](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Topeltkirjutuse dokumentatsioon](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Portaali töötsükkel](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Portaali uuendamine](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portaali konfiguratsiooni migreerimine](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Lahenduse töötsükli haldus: Dynamics 365 for Customer Engagementi rakendused](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]