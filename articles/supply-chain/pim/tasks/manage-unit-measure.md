---
title: Mõõtühikute haldamine
description: Selles teemas kirjeldatakse, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.
author: t-benebo
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e13897396810507bb4b2cbb415b873eb3dd7f4e8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565515"
---
# <a name="manage-units-of-measure"></a>Mõõtühikute haldamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.

## <a name="open-the-units-page"></a>Avage ühikute leht

Süsteemis saadaolevate mõõtühikute loomiseks ja tööks minge **organisatsioonihalduse \> häälestusüksuste \> ühikute \> üksusesse**.

Selle teema ülejäänud jaotised kirjeldavad, mida saate teha lehel **Ühikud**.

## <a name="create-standard-units-and-conversions"></a>Standardühikute ja teisenduste loomine

Kui teie süsteem ei sisalda juba kõige sagedamini kasutatavaid mõõtühikuid meetermõõdustiku ja/või USA standardsüsteemi (USCS) jaoks, võib ühiku häälestusviisard aidata teil kiiresti baasühikumääratluste ja teisendustega alustada. Viisardi lõpuleviimiseks valige **tegevuspaanil ühiku loomise viisard** ja järgige seejärel ekraanil olevaid juhiseid.

## <a name="create-or-edit-a-unit-of-measure"></a>Mõõtühiku loomine või redigeerimine

Mõõtühiku loomiseks või redigeerimiseks järgige neid samme.

1. Järgige üht neist sammudest.

    - Olemasoleva üksuse redigeerimiseks valige see loendipaanilt.
    - Uue ühiku loomiseks valige toimingupaanilt suvand **Uus**.

1. Määrake uue kirje päises järgmised väljad.

    - **Ühik** – sisestage ID või sümbol, mida kasutada üksusele viitamiseks süsteemikeeles. See ID või sümbol on tavaliselt ühiku tavaühend, nt *ea* igaühe või *cm* sentimeetri kohta.
    - **Kirjeldus** – Sisestage mõõtühikule süsteemikeeles kirjeldav nimi. See nimi on tavaliselt üksuse täielik nimi, nt *Iga* või *Sentimeeter*.

1. Määrake kiirkaardil **Üldine** järgmised väljad.<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Ühiku klass** – valige atribuut, mida ühik mõõtühiku abil (nt pikkus, ala, mass või kogus).
    - **Ühikutesüsteem** – valige mõõtmissüsteem, kuhu ühik kuulub (*meetermõõdustiku ühikud* või *Ameerika Ühendriikide tavamõõdustiku ühikud*).
    - **Baasühik** – määrake see suvand väärtusele *Jah*, et kasutada praegust ühikut ühiku klassis baasühikuna. Sel juhul peate sinult ühiku klassis määrama ainult baasühiku ja iga ühikuklassi lisaühiku vahelise teisendusteguri. Süsteem saab seejärel läbi viia teisendusi kõikide selle ühiku klassi ühikute vahel. Seepärast on teisenduste seadistamine lihtsam.

        Näiteks kui gallon on *mahuühiku* klassi baasühik, peate seadistama teisendustegurid kvartilt gallonile ja pint-st gallonini. Süsteem saab seejärel teisendada ka kvartilt pindiks.

        Teil võib ühiku klassi kohta olla ainult üks baasühik.

    - **Süsteemi ühik** – määrake see suvand väärtusele *Jah*, et kasutada oletatavat ühikut ühiku kõigi täpsustamata mõõdete puhul. Näiteks kui koguse sisestamiseks kasutatav väli ei luba ühikut määrata (kui kasutaja ei vali ühikut), kasutab süsteem ühikut, mis on määratud klassi *Kogus* süsteemiühikuks. Teil võib ühiku klassi kohta olla ainult üks süsteemi ühik.
    - **Kümnendarvuline täpsus** – määrake komakohtade arv, milleni praeguse ühiku jaoks määratud või teisendatud väärtused tuleb ümardada.

1. Valige toimingupaanil nupp **Salvesta**.

## <a name="define-unit-translations"></a>Ühiku teisenduste määratlemine

ID või sümboli tõlgete ja mõõtühiku kirjelduse määratlemiseks järgige neid samme.

1. Looge või valige üksus, mille jaoks tõlkeid luua.
1. Valige toimingupaanil suvand **Ühiku tekstid**.

    Kuvatakse **ühiku tekstid** tekstide leht. Kasutate seda lehekülge, et määrata valitud üksuse ID või sümboli tõlked. Neid tõlkeid saab seejärel kasutada välistes dokumentides kliendi- või hankijaspetsiifilistes keeltes.

1. Valige toimingupaanil nupp **Uus**.
1. Valige **keeleväljal** keel, millesse tuleb ühiku ID või sümbol tõlkida.
1. Sisestage väljale **Tekst** ühiku ID või sümboli tõlge valitud keeles.
1. Valige toimingupaanil nupp **Salvesta**.
1. Sulgege leht.
1. Valige **Toimingupaanil** **Ümberarvestatud ühiku kirjeldused**.

    Kuvatakse lehekülg **Tõlgitud ühiku kirjeldused**. Kasutate seda lehekülge, et määrata valitud üksusele keelepõhiseid kirjeldusi.

1. Valige toimingupaanil nupp **Uus**.
1. Valige **keeleväljal** keel, millesse tuleb ühiku kirjeldus tõlkida.
1. Sisestage väljale **Kirjeldus** ühiku kirjelduse tõlge valitud keeles.
1. Valige toimingupaanil nupp **Salvesta**.
1. Sulgege leht.

## <a name="define-unit-conversion-rules"></a>Ühiku teisendamise reeglite määratlemine

Mõõtühikute vaheliste teisendusreeglite määratlemiseks järgige neid samme.

1. Looge või valige üksus, mille jaoks defineerida teisendusreegleid.
1. Valige toimingupaanilt suvand **Ühiku teisendused**.

    Avaneb leht **Ühiku teisendused**. Seda lehte kasutate, et defineerida reeglid valitud mõõtühiku teisendamiseks muudesse mõõtühikutesse valitud ühiku klassis.

1. Valige üks järgmistest vahekaartidest, sõltuvalt teisendustüübist, mida soovite seadistada:

    - **Standardsed teisendused** – saate seadistada kõigi toodete standardsed teisendusreeglid.
    - **Klassisisesed teisendused** – saate seadistada tootepõhised teisendusreeglid ühikute jaoks samas ühikuklassis.
    - **Klassisisesed teisendused** – saate seadistada tootepõhised teisendusreeglid ühikute jaoks üle ühikuklasside.

1. Järgige üht neist sammudest.

    - Uue teisenduse loomiseks valige tööriistaribalt suvand **Uus**.
    - Olemasoleva teisenduse redigeerimiseks valige teisendus ruudustikus ja seejärel valige tööriistaribal **Redigeeri**.

1. Määrake järgmised väljad kuvatavas ripp-dialoogiboksis.

    - **Toode** – valige konkreetne toode, mille suhtes teisendus kehtib. See väli on saadaval ainult klassisiseste ja klassisiseste teisenduste puhul.
    - **Valemi paigutus** – jätke selle välja väärtuseks *Lihtne*, et määrata lihtne teisendamine, sel on üks tegur. Seadistage see väärtusele *Täpsem*, et seadistada keerukam võrrand. Täpsemate võrrandite vorming erineb olenevalt ühiku klassist.
    - **Vormi ühik** – sellel väljal kuvatakse valitud ühik. Tavaliselt ei tohi te seda väärtust muuta. (Kui muudate väärtust, peate avama väärtuse valitud ühiku **ühikuteisenduste** leht, et pärast salvestamist vaadata oma uut teisendust.)
    - **Ühikuks** – valige ühik, milleks teisendada.
    - **Ümardamine** – valige, kuidas murrud ümardada, võttes aluseks valitud ühiku **kümnendarvuline** täpsusväärtus (*Lähimani* *Üles* või *Alla*).
    - **Teisendusvalem** – kasutage rippmenüü ülemises ülaosas allesolevaid välju kahe ühiku vahelise teisendamise valemi määramiseks. Saadaolevad väljad varieeruvad sõltuvalt valitud ühiku klassist ja valemi kavandist.

1. Valige nupp **OK**.
1. Sulgege leht.

> [!TIP]
> Samuti saate seadistada ühikuteisendused tootevariandi kohta. Lisateavet saate jaotisest [Mõõtühiku teisendus tootevariandi kohta](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
