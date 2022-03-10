---
title: Transiidis olevate kaupade töötlemine
description: Selles teemas kirjeldatakse, kuidas töötada transiidis olevate kaupade tellimustega. Kui tellimus või teekond on häälestatud kasutama transiidis olevate kaupade töötlemist, saab kaupu arveldada juba enne seda, kui need on tarbimiseks laos vastu võetud.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e85e3ba92b61e0208e1cf95d3f361d38772d83cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571037"
---
# <a name="goods-in-transit-processing"></a>Transiidis olevate kaupade töötlemine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas töötada transiidis olevate kaupade tellimustega. Seda tüüpi tellimust kasutatab ainult moodul **Väljalaadimiskulu**. Kui tellimus või teekond on häälestatud kasutama transiidis olevate kaupade töötlemist, ei pea te kaupade arveldamiseks ootama, kuni need on laos vastu võetud. Kaubad arveldatakse selle asemel kohe, kui nad hankija laost või lähtesadamast lahkuvad, finantskulud tuvastatakse teekonna alguses. See funktsioon võimaldab teil varude kuuluvuse õigesti endale võtta, kuna kaubad muutuvad sageli teie organisatsiooni omandiks juba lähtesadamast väljumisel.

Transiidis olevate kaupade tellimuste kasutamisel võetakse finantsiliselt värskendatud kaubad vastu vahelaos, mida nimetatakse transiidis olevateks kaupade laoks. Kaubad jäävad seejärel sellesse lattu seniks, kuni need saab lõppsihtlaos (st ostureal määratletud laos) vastu võtta. Neid ei saa käsitsi eemaldada.

Seni, kuni kaubad on transiidis, pole need varudes saadaval ja neid ei saa tarnimiseks varudest komplekteerida. Siiski saate transiidis olevate kaupade varusid vaadata. Samuti saate neid kaupu kasutada koondplaneerimisel. Sel juhul kasutage ostutellimuse real kinnitatud tarnekuupäeva eeldatava kuupäevana, mil varud on tarbimiseks saadaval.

Järgmistes jaotistes kirjeldatakse seadistust, mis on transiidis olevate kaupade mõisteid ja funktsioone kasutades varude ja teekondade töötlemiseks vajalik.

## <a name="terms-of-delivery"></a>Tarnetingimused

Mooduli **Väljalaadimiskulu** lubamise korral täiendatakse standardsete *tarnetingimuste* üksust transiidis olevate kaupade funktsiooni toetamiseks.

Kui rakendatava tarnetingimuste kirje korral on sätte **Transiidis olevate kaupade haldus** väärtuseks määratud *Jah*, paigutatakse kaubad transiidis olevate kaupade lattu. See toiming käivitatakse ainult juhul, kui varude sissetulekut ei töödelda enne arve töötlemist. Kui tellimuse tarnetingimustes on määratud transiidis olevate kaupade kasutamine, ei saa kasutajad enam ostutellimuse jaoks tootesissetulekut sisestada. Kui nad seda siiski teha proovivad, ilmneb tõrge. Tõrketeade annab teada, et jätkamiseks tuleb kasutada transiidis olevate kaupade funktsiooni.

Transiidis olevate kaupade tarnetingimuste teabega töötamiseks valige **Hanked \> Seadistamine \> Jaotus \> Tarnetingimused**. Järgmises tabelis kirjeldatakse välju, mille moodul **Väljalaadimiskulu** lisab transiidis olevate kaupade funktsiooni toetamiseks lehele **Tarnetingimused**. Mõlemad väljad asuvad kiirkaardil **Üldine**. Lisateavet selle lehe teiste väljade kohta leiate teemast [Tarnetingimused (vorm)](/dynamicsax-2012//terms-of-delivery-form).

| Field | Kirjeldus |
|---|---|
| Saatmissadam on kohustuslik | Kui lähtesadam on tarnetingimuste rakendumisel kohustuslik, määrake selle sätte väärtuseks *Jah*. |
| Transiidis olevad kaubad: haldus | Transiidis olevate kaupade funktsiooni kasutamiseks tarnetingimuste rakendumisel määrake selle sätte väärtuseks *Jah*. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Transiidis olevate ja alatarnitud kaupade laod

Mooduli **Väljalaadimiskulu** lubamise korral täiustatakse *ladude* standardüksust ostutellimuste arveldamise lubamiseks, kui kaubad on transiidis olevate kaupade laos.

Väljalaadimiskulu moodul lisab kaks uut laotüüpi: *transiidis olevad kaubad* ja *alatarne*. Mõlemat tüüpi ladusid saab määrata vaikelaoks. Transiidis olevate kaupade tellimuste töötlemiseks tuleb lehel **Laod** konfigureerida nii transiidis olevate kaupade ladu kui ka alatarne ladu. Seejärel tuleb iga väljalaadimiskulu ja transiidis olevate kaupade korral kasutatava vaikelao jaoks valida kumbagi tüüpi saadaolevate ladude hulgast nii transiidis olevate kaupade ladu kui ka alatarne ladu.

*Transiidis olevate kaupade* laotüüp seostatakse teie transiidis olevate kaupade laoga ja seda ladu kasutatakse transiidis olevate kaupade tellimustesse kaasatud kaupade töötlemiseks enne nende vastuvõtmist lõppsihtlaos. Üldiselt piisab iga koha jaoks ühest transiidis olevate kaupade laost, kui koht ja ladu on ainsad varude haldamiseks kasutatavad varude dimensioonid. Kui kasutatakse ka asukoha varude dimensiooni, peab transiidis olevate kaupade ladu olema seadistatud iga koha ja lao kombinatsiooni jaoks, et määrata saaks ka vaikeasukoha.

Ladude transiidis olevate kaupade sätetega töötamiseks valige **Varude haldus \> Seadistamine \> Laovarude jaotamine \> Laod**. Järgmises tabelis kirjeldatakse välju, mille moodul **Väljalaadimiskulu** lisab transiidis olevate kaupade funktsiooni toetamiseks lehele **Laod**. Mõlemad väljad kuvatakse kiirkaardil **Üldine**. Lehe teiste väljade kohta leiate lisateavet teemast [Laod (vorm)](/dynamicsax-2012//warehouses-form).

| Field | Kirjeldus |
|---|---|
| Transiidis olevad kaubad: ladu | Määratlege pealaoga seotud transiidis olevate kaupade ladu. |
| Alatarne ladu | Määratlege pealaoga seotud alatarneladu. |

## <a name="posting-rules-for-landed-cost"></a>Väljalaadimiskulu sisestusreeglid

Väljalaadimiskulu lisab kaks uut sisestusreeglit, mida saate konfigureerida. Neid sisestusreegleid kasutatakse ostutellimuste otseste arvesummade finantsiliseks sisestamiseks, et tuvastada kaupade kuuluvus lähtepunktist lahkumisel. See protsess asendab *vastu võetud, ent arveldamata kaupade* mõiste, sest kaubad arveldatakse enne nende vastuvõtmist. <!-- KFM: Add a link to the related scenario when available. -->

Sisestusreeglitega töötamiseks valige **Varude haldus \> Seadistamine \> Sisestamine \> Sisestamine**. Vahekaardil **Ostutellimus** on saadaval järgmised uued sisestusreeglid:

- **Väljalaadimiskulu, transiidis olevad kaubad** – määrake transiidis olevate kaupade halduse sisestusreeglid.
- **Väljalaadimiskulu, kulutasu tekkepõhine arvestus** – määrake kulukonto tekkepõhise arvestuse sisestusreeglid.

## <a name="goods-in-transit-orders"></a>Transiidis olevad kaupade tellimused

Transiidis olevate kaupade tellimusi saate vaadata ja hallata otse moodulis **Väljalaadimiskulu**. Transiidis olevate kaupade tellimusi saate töödelda otse lehel **Transiidis olevate kaupade tellimused**. Teise võimalusena võite valida transiidis olevate kaupade tellimustega seostatud teekonna ja töödelda terve teekonna, saatmiskonteineri või foolio. Teekonna arveldamisel ja transiidis olevate kaupade tellimuste loomisel luuakse uus transiidis olevate kaupade tellimus iga varude ja varude dimensioonide kombinatsiooni jaoks, mis on ostutellimuse reaga seostatud.

Transiidis olevate kaupade haldamiseks kasutab väljalaadimiskulu moodul kaheastmelist protseduuri.

1. Kaup on vastu võetud, kui laovaru arve on töödeldud ja selle olekuks on määratud *Transiidis*.
1. Transiidis olevate kaupade tellimus töödeldakse lehel **Transiidis olevad kaubad: tellimused** ja seejärel võetakse see vastu ostutellimusel määratud laos. Uueks olekuks määratakse siis *Vastu võetud*.

Transiidis olevate kaupade tellimustega töötamiseks valige **Väljalaadimiskulu \> Perioodilised ülesanded \> Transiidis olevad kaubad: tellimused**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Laovaru vastuvõtmine transiidis olevate kaupade laost

Transiidis olevate kaupade tellimusest saab sõltuvalt teie süsteemi seadistusest kaupu vastu võtta mitmel viisil.

### <a name="in-transit-receiving"></a>Transiitvastuvõtt

Transiitvastuvõttu saate teha järgmiste lehtede kaudu.

- Valige rida lehel **Transiidis olevad kaubad: tellimused** ja seejärel valige toimingupaanil **Võta vastu**.
- Valige või avage lehel **Kõik teekonnad** soovitud teekond. Seejärel valige toimingupaani vahekaardi **Haldamine** jaotises **Transiidis olevad kaubad** käsk **Võta transiidis olevad kaubad vastu**.
- Valige või avage lehel **Kõik saatmiskonteinerid** soovitud konteiner. Seejärel valige toimingupaani vahekaardi **Haldamine** jaotises **Transiidis olevad kaubad** käsk **Võta transiidis olevad kaubad vastu**.
- Valige või avage lehel **Kõik fooliod** soovitud foolio. Seejärel valige toimingupaani vahekaardi **Haldamine** jaotises **Transiidis olevad kaubad** käsk **Võta transiidis olevad kaubad vastu**.

> [!NOTE]
> Transiitvastuvõttu kasutatakse tavaliselt olukordades, kus asukohtade ning partii- ja seerianumbrite jälgimist ei kasutata.

### <a name="arrival-journal"></a>Saabumise tööleht

Kaupu saate vastu võtta ka saabumistöölehe loomisega. Saabumistöölehe saate luua otse teekonna lehe kaudu. Teie organisatsioonis kehtestatud head tavad määravad, kas saabumistöölehte kasutatakse kaupade vastuvõtuks.

1. Avage teekond, konteiner või foolio.
1. Valige toimingupaani vahekaardi **Haldamine** jaotises **Funktsioonid** käsk **Loo saabumistööleht**.
1. Dialoogiboksis **Saabumistöölehe loomine** määrake järgmised väärtused.

    - **Lähtesta kogus** – koguse määramiseks transiidi kogusest määrake selle sätte väärtuseks *Jah*. Kui selle sätte väärtus on *Ei*, ei määrata transiidis olevate kaupade ridadelt vaikekogust.
    - **Loo transiidis olevatest kaupadest** – määrake selle sätte väärtuseks *Jah*, et võtta kogused valitud teekonna, konteineri või foolio valitud transiidiridadelt.
    - **Loo tellimuse ridadelt** – määrake selle sätte väärtuseks *Jah*, et määrata saabumistöölehe vaikekogus ostutellimuse ridadelt. Saabumistöölehe vaikekoguse saab sel viisil määrata ainult siis, kui ostutellimuse rea kogus ühtib transiidis olevate kaupade tellimuse kogusega.

1. Töödelge saabumistööleht vastavalt teemas [Kauba sissetulekute registreerimine kauba saabumise töölehel](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal) kirjeldatud juhistele.

> [!NOTE]
> Saabumistöölehte kasutatakse enamasti olukordades, kus kasutatakse asukohtade ning partii- ja seerianumbrite jälgimist, kuid mitte laohaldust.
>
> Vastuvõtu vaikeasukohti ei tohiks tellimuse ridadel määrata, kui saabumise töölehel määratakse ladustamise asukoht.

## <a name="warehouse-management"></a>Laohaldus

Kui lubate mooduli **Väljalaadimiskulu**, muudetakse mitut mooduli **Laohaldus** lehte nii, et tellimuste töötlemist (eelkõige transiidis olevate kaupade töötlemist) saab teha mooduli **Väljalaadimiskulu** kaudu. Selles jaotises antakse ülevaade väljadest ja protsessidest, mis lisatakse moodulisse **Laohaldus**.

### <a name="mobile-device-menu-items"></a>Mobiilse seadme menüü-üksused

Kaupu saab mobiilse seadme kaudu vastu võtta eeldusel, et mobiilse seadme menüü ja moodul **Laohaldus** on seadistatud kaupu vastu võtma transiidis olevate kaupade tellimusest. Selles jaotises kirjeldatakse transiidis olevate kaupade vastuvõtmisega seotud seadistust.

Mobiilsete seadmete seadistamiseks transiidis olevate kaupade töötlemiseks valige **Laohaldus \> Seadistamine \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.

Väljalaadimiskulu moodul lisab transiidis olevate kaupade töötlemise toetamiseks mobiilse seadme menüükäskude hulka järgmised töö loomise protsessid.

- Transiidis olevad kaubad: kauba sissetulek
- Transiidis olevad kaubad: kauba vastuvõtt ja ladustamine

Nende protsesside konfigureerimissätted sarnanevad [ostutellimuse vastuvõtu ja ladustamise töö loomise protsesside](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work) sätetega. Protsess *Transiidis olevad kaubad: kauba vastuvõtt ja ladustamine* lisab ka järgmise välja.

- **Luba saatmiskonteineri lõpetamine** – kui selle sätte väärtuseks on määratud *Jah*, kuvab lao mobiilirakendus Warehouse Management ladustamistöö lõpuleviimisel lisasuvandi nimega **Saatmiskonteiner on valmis**. Selle suvandi valimise korral palutakse töötajal kinnitada, et konteiner on lõpule viidud. Sel hetkel töödeldakse kõik puudulikud vastuvõtmised alakandena.

### <a name="location-directives"></a>Asukohakorraldus

Väljalaadimiskulu lisab lehele *Asukohakorraldus* uue töökäsutüübi nimega **Transiidis olevad kaubad**. See töökäsutüüp tuleb konfigureerida sarnaselt [ostutellimuse töökäsutüüpidega](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Töömallid

See jaotis kirjeldab funktsioone, mida **väljaminev kulu** moodul lisab töömallidele.

#### <a name="goods-in-transit-work-order-type"></a>Transporditöö tellimuse tüüp

Väljalaadimiskulu lisab lehele *Töömallid* uue töökäsutüübi nimega **Transiidis olevad kaubad**. See töökäsutüüp tuleb konfigureerida sarnaselt [ostutellimuse töömallidega](/dynamicsax-2012/appuser-itpro/create-a-work-template).

#### <a name="work-header-breaks"></a>Tööpäise jaotused

Töömalle, mille töötellimuse tüüp on *Transiidis kaubad*, saab konfigureerida tööpäiste tükeldamiseks. Lehel **Töömallid** tehke üht järgmistest.

- Seadke malli vahekaardil **Üldine** tööpäise maksimumid. Need maksimumid töötavad samal viisil, nagu need töötavad ostutellimuse töömallide puhul. (Lisateavet vt [ostutellimuse töömallid](/dynamicsax-2012/appuser-itpro/create-a-work-template).)
- Kasutage nuppu **Tööpäise piirid**, et määrata, millal süsteem peaks looma uusi tööpäiseid sõltuvalt sorteeritavatest väljadest. Näiteks, et luua tööpäis igale konteineri ID-le, valige toimingupaanil **Redigeeri päringut** ja siis lisage väli **Konteineri ID** päringuredaktoris vahekaardile **Sortimine**. Välju, mis on lisatud **Sortimise** vahekaardile, saab valida *grupeerimisväljadena*. Grupeerimisväljade määramiseks valige toimingupaanil **Tööpäise piirid** ja seejärel valige märkige iga välja puhul, mida soovite kasutada grupeerimisväljana, märkeruut veerus **Grupeeri selle välja järgi**.

Väljaminev kulu [loob ülekande](over-under-transactions.md), kui registreeritud kogus ületab algse tellimuse koguse. Kui tööpäis on lõpule viidud, värskendab süsteem peamise tellimiskoguse varude tehingute olekut. Siiski värskendab see esmalt ülekandega seotud kogust pärast põhiosa täielikku ostmist.

Kui tühistate juba registreeritud ülekande tööpäise, vähendatakse ülekande summat esmalt tühistatud koguse võrra. Pärast ülekandetehingu vähendamist koguseks 0 (null) eemaldatakse kirje ja lisakogused registreeritakse põhilise tellimiskoguse suhtes.
