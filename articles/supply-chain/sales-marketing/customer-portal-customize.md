---
title: Kliendiportaali kohandamine ja kasutamine
description: See artikkel selgitab, kuidas kohandada kliendiportaali pärast selle lisamist teie süsteemi.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85ec4beda2efe62ff5076a5ed694efbc47c6d87f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878870"
---
# <a name="customize-and-use-the-customer-portal"></a>Kliendiportaali kohandamine ja kasutamine

[!include [banner](../includes/banner.md)]


See artikkel kirjeldab erinevaid lehekülgi, mis on saadaval kliendi portaalis väljast. Selles seletatakse, mida lehed teevad ja kuidas saate neid kohandada.

Kliendiportaal pakub valmiskujul mõningaid veebilehti ja toiminguid. Järgmine saidikaart annab ülevaate nendest veebisaitidest ja toimingutest ning samuti rollidest, mis saavad nimetatud toiminguid teha.

![Kliendiportaali saidikaart.](media/customer-portal-site-map.png "Kliendiportaali saidikaart")

## <a name="typical-customizations"></a>Tavalised kohandused

Järgmised artiklid aitavad teil saada teada portaalide põhitõed Power Apps ja kuidas saate portaale kohandada:

- [Töötada mallidega](/powerapps/maker/portals/work-with-templates) – see artikkel annab ülevaate Power Apps portaalide töö ja portaalide lihtsate kohanduste kohta.
- [Portaali sisu haldamine](/dynamics365/portals/manage-portal-content) – see artikkel selgitab, kuidas saate hallata ja kohandada sisu, mille olete oma portaalis pinnaks.
- [Redigeerimine CSS](/powerapps/maker/portals/edit-css) – see artikkel aitab teil teha keerukamaid portaali kasutajaliidese (UI) kohandusi.
- [Looge oma portaali jaoks kujundus](/dynamics365/portals/create-theme) – see artikkel aitab luua portaali jaoks kasutajaliidese kujunduse.
- [Looge ja mugavam portaali sisu –](/dynamics365/portals/create-expose-portal-content) see artikkel aitab hallata aluseks olevaid andmeid ja tabeleid, mida oma portaalis kasutate.
- [Konfigureerige kontakt portaalis](/powerapps/maker/portals/configure/configure-contacts) kasutamiseks – see artikkel selgitab kasutajarollide loomise ja kohandamise ning turvalisuse ja autentimise tööd portaalides Power Apps.
- [Konfigureerige märkused tabelivormidele ja veebivormidele portaalides](/powerapps/maker/portals/configure-notes) – see artikkel selgitab, kuidas lisada portaali dokumente ja täiendavat talletusruumi.
- [Tõrkekäsitlus portaali veebisaidi puhul](/powerapps/maker/portals/admin/view-portal-error-log) – see artikkel selgitab, kuidas kuvada portaali tõrkelogisid ja salvestada need oma Microsoft Azure bloobi talletuskontole.

## <a name="customize-the-order-creation-process"></a>Tellimuse loomise protsessi kohandamine

Kui kasutaja esitab kliendiportaali kasutades tellimuse, siis sünkroonitakse tellimus automaatselt asjakohase Dynamics 365 Supply Chain Managementi keskkonnaga. Kuna kasutaja on välisklient, on osa nõutavast teabest tema eest tahtlikult peidetud. See teave täidetakse automaatselt vormi esitamisel.

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

    ![Tellimuse teabeleht.](media/customer-portal-order-information.png "Tellimuse teabeleht")

1. Valige **Edasi**.
1. Valige lehel **Kaubad** suvand **Lisa kaup**.

    ![Kaupade leht.](media/customer-portal-items.png "Kaupade leht")

1. Määrake dialoogiboksis **Kauba teave** järgmised väljad.

    - **Toote nimi** – otsige ja valige toode, mida tellimusele lisada.
    - **Kogus** – sisestage valitud toote kogus.
    - **Ühik** – määrake mõõtühik (nt **ea.**, **kg** või **kast**).
    - **Eeldatav netosumma** – väärtus arvutatakse kauba eeldatava hinna ja valitud üksuse koguse korrutisena.

    ![Kauba teabe dialoogiboks.](media/customer-portal-item-information.png "Kauba teabe dialoogiboks")

1. Kauba tellimusele lisamiseks valige **Esita**.
1. Korrake samme 4–6, kuni olete lisanud kõik kaubad, mida soovite tellida.
1. Kui olete kaupade lisamise lõpetanud, klõpsake lehel **Kaubad** nuppu **Edasi**.
1. Lehel **Tellimuse teave** esitatakse tellimuse kokkuvõte. Vaadake üle tellimuse sisu ja tarne üksikasjad. Kui kõik tundub õige, siis valige tellimuse esitamiseks suvand **Esita**.

    ![Täidetud tellimuse teabeleht.](media/customer-portal-order-submit.png "Täidetud tellimuse teabeleht")

### <a name="standard-data-setup"></a>Standardandmete seadistus

Sujuva kasutajakogemuse tagamise otstarbel täidab kliendiportaal mitme nõutava välja väärtused automaatselt. Need väärtused põhinevad tellimust esitava kliendi kontaktikirjes toodud teabel.

Kliendiportaali tellimuste esitamiseks kasutava kliendi iga [kontaktirida](/powerapps/maker/portals/configure/configure-contacts) kohta tuleb täpsustada järgmiste nõutud väljade väärtused. Vastasel juhul ilmnevad tõrked.

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

Kui soovite lehele veerge lisada või neid eemaldada, vt teemat [Kiirloomise vormide loomine või redigeerimine sujuvaks andmesisestuseks](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Kui soovita muuta veergude eelseadistust ning seda, kuidas väärtused lehe salvestamisel seadistatakse, siis tutvuge Power Appsi portaalide dokumentatsioonis järgmise teabega.

- [Välja eeltäitmine](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Määra väärtus salvestamisel](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Avalehe kohandamine

Kõik kliendiportaali juhtelemendid on Power Appsi portaalide sisseehitatud juhtelemendid. Te saate neid kohandada, järgides Power Appsi portaalide dokumentatsiooni jaotist [Lehe koostamine](/powerapps/maker/portals/compose-page).

Ainus kliendiportaali malli kaasatud kohandatud juhtelement on mõeldud avalehel paanide loomiseks.

![Avalehe paanid.](media/customer-portal-home-page-tiles.png "Avalehe paanid")

Paanide muutmiseks toimige järgmiselt.

1. Avage [portaalihalduse rakendus](/powerapps/maker/portals/configure/configure-portal).
1. Valige navigeerimispaanilt vasakult suvand **Lehe mallid**.

    ![Portaalihalduse navigeerimispaan.](media/customer-portal-nav.png "Portaalihalduse navigeerimispaan")

1. Valige lehe mall, mille nimi on **Avaleht**.
1. Valige väljal **Veebimall** link **Avaleht**, et avada selle lehe lähtekood.

    ![Veebimalli väli.](media/customer-portal-web-template.png "Veebimalli väli")

1. Nüüd peaksite nägema kogu avalehe lähtekoodi ja saate seda vajaduse järgi muuta.

## <a name="resources"></a>Ressursid

Lisateavet kliendiportaali seadistamise ja kohandamise kohta leiate järgmistest allikatest.

- [Power Appsi portaalide dokumentatsioon](/powerapps/maker/portals/overview)
- [Topeltkirjutuse dokumentatsioon](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Portaali töötsükkel](/powerapps/maker/portals/admin/portal-lifecycle)
- [Portaali uuendamine](/powerapps/maker/portals/admin/upgrade-portal)
- [Portaali konfiguratsiooni migreerimine](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Lahenduse töötsükli haldus: Dynamics 365 for Customer Engagementi rakendused](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]