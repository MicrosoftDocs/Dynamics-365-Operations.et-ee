---
title: Puhkuste ja puudumiste tüüpide konfigureerimine
description: Seadistage puhkuse tüübid, mida töötajad saavad rakenduses Dynamics 365 Human Resources valida.
author: twheeloc
ms.date: 09/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59fe5ece00500f7dafab282c00d572575706f790
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894581"
---
# <a name="configure-leave-and-absence-types"></a>Puhkuste ja puudumiste tüüpide konfigureerimine

> [!Important]
> Selles artiklis märgitud funktsioonid on klientide jaoks praegu saadaval eraldiseisev Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduse Dynamics 365 Human Resources puhkuse tüübid määratlevad puhkuste tüübid, millest töötajal on võimalik teada anda. Saate kohandada puhkuse tüüpe vastavalt teie organisatsiooni vajadustele. Puhkuse tüübid hõlmavad järgmisi.

- Tasustatav puhkus
- Tasustamata puhkus
- Tasustatav puhkus
- Haiguspuhkus
- Meditsiiniline puhkus
- Perekondlik puhkus
- Lühiajaline invaliidsus
- Lähedase kaotuse puhkus

## <a name="add-a-leave-type"></a>Puhkuse tüübi lisamine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste tüübid**.

3. Valige suvand **Uus**.

4. Sisestage puhkuse tüübi nimi suvandis **Tüüp**, valige töövoog suvandist **Töövoo ID** ja sisestage kirjeldus suvandisse **Kirjeldus**.

5. Jaotises **Üldine** valige suvand **Puudub**, **Plaanipärane** või **Plaaniväline** ripploendis **Kategooria**.

6. Valige tulukood ripploendist **Tulukood**.

7. Jaotises **Põhjuse kood nõutav** valige, kas soovite nõuda põhjuse koodi. Kui soovite põhjuse koode nõuda, peate võib-olla need lisama. Jaotises **Põhjuse koodid** valige suvand **Lisa**, valige põhjuse kood ja seejärel valige selle kõrval märkeruut **Lubatud**.

8. Jaotises **Valitud rollide juurdepääsu piiramine** valige, kas soovite juurdepääsu piirata. Seejärel valige turberollid jaotises **Selle puhkuse tüübi turberollid**. Turberollid määratletakse töövoos, mille valisite selles toimingus varem jaotises **Töövoo ID**.

9. Valige jaotises **Kalendri värv**, millist värvi selle puhkusetüübi puhul puhkuste ja puudumiste kalendrites kuvada. 

10. Valige jaotises **Peatamise suhted**, kas soovite, et see puhkusetüüp peataks mõne teise puhkusetüübi või et selle puhkusetüübi peataks mõni teine puhkusetüüp. Kui puhkusetaotlus esitatakse peatava puhkusetüübi kohta, siis luuakse peatatud puhkusetüübi kohta automaatselt puhkuse peatamise kanne. 

10. Valige käsk **Salvesta**.

## <a name="configure-leave-type-rules"></a>Puhkuse tüübi reeglite konfigureerimine

1. Määrake puhkuse tüübi ümardamise suvandid. Valikud hõlmavad suvandeid **Puudub**, **Üles**, **Alla** ja **Lähim**. Saate määrata ka puhkuse tüübi ümardamise täpsuse.

2. Määrake puhkuse tüübiks **Puhkuse parandused**. Kui valite selle valiku, kasutatakse tööpäevale langevate puhkepäevade arvu, et määrata kindlaks, kuidas puhkusetüübi jaoks vaba aega koguda. Näiteks kui jõulupüha langeb esmaspäevale, lahutab rakendus Human Resources lisandumiste töötlemisel puhkuse tüübist ühe päeva.

   Pühad määrate tööajakalendris. Lisateabe saamiseks vaata [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md).
   
 3. Seadistage puhkusetüübi kohta **Ülekantav puhkusetüüp**. Selle valiku korral kantakse ülekantavad saldod üle konkreetsele puhkusetüübile. Samuti tuleb ülekantava puhkuse tüüp lisada puhkuse ja puudumiste plaanile. 
 
4. Määratlege puhkusetüübi kohta **Aegumisreeglid**. Selle valiku konfigureerimisel saate valida päevade või kuude üksuse ja määrata aegumise kestuse. Aegumisreegli jõustumiskuupäeva kasutatakse selleks, et määrata, millal puhkuse aegumist töötlev pakett-töö käivitada, või millisel kuupäeval reegel jõustub. Aegumine ise leiab aset viitvõlaperioodi alguskuupäeval. Kui viitvõlaperioodi alguskuupäev on näiteks 3. august 2021 ja aegumisreegliks seadistati 6 kuud, siis töödeldakse reeglit viitvõlaperioodi alguskuupäeva aegumisvastaskonto alusel, nii et see käivitatakse 3. veebruaril 2022. Kõik aegumiskuupäeval eksisteerivad puhkusesaldod arvatakse puhkusetüübist maha ning need kajastuvad puhkusesaldos.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Konfigureerige puhkuse tüübi jaoks vajalik manus

> [!NOTE]
> **Manus nõutud** välja kasutamiseks peate funktsioonihalduses funktsiooni **Puhkusetaotluste jaoks vajaliku manuse seadistamine** sisse lülitama. Lisateabe jaoks funktsioonide sisselülitamise kohta vaata [Funktsioonide haldamine](hr-admin-manage-features.md).

1. Valige lehel **Puhkus ja puudumine** vahekaart **Lingid** jaotises **Seadistamine** valik **Puhkuse ja puudumise tüübid**.

2. Valige loendist puhkuse ja puudumise tüüp. Seejärel kasutage jaotises **Üldine** välja **Manus nõutud**, et määrata, kas manus tuleb üles laadida, kui töötaja esitab valitud puhkuse tüübile uue puhkuse taotluse. 

Töötajad peavad manuse üles laadima, kui nad esitavad uue puhkusetaotluse, mille puhkusetüübi puhul on väli **Manus kohustuslik** lubatud. Puhkusetaotluse osana üleslaaditud manuse vaatamiseks saavad taotluse kinnitajad kasutada neile määratud tööüksuste valikut **Manused**. Kui puhkuse taotlusele pääseb juurde Microsoft Teams Human Resources rakenduse kaudu, saab suvandit **Kuva üksikasjad** kasutada selle üksikasjade ja manuste vaatamiseks.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Puhkuseühikute (tunnid/päevad) konfigureerimine puhkusetüübi järgi

> [!NOTE]
> Puhkuseühikute kasutamiseks puhkuse tüübi funktsiooni kohta peate Funktsioonihalduses kõigepealt sisse lülitama funktsiooni **Puhkuseühikute konfigureerimine puhkusetüübi kohta**. Lisateabe jaoks funktsioonide sisselülitamise kohta vaata [Funktsioonide haldamine](hr-admin-manage-features.md).

> [!IMPORTANT]
> Vaikimisi kasutavad puhkusetüübid juriidilises isikus puhkuse parameetrite konfiguratsioonist juriidilise isiku tasemel puhkuseühikuid.
> 
> Puhkuse ja puudumise tüübi puhkuseühikut saab muuta ainult siis, kui selle puhkusetüübi puhul ei ole puhkusekandeid.
> 
> Funktsiooni ei saa pärast sisselülitamist välja lülitada.

1. Valige lehel **Puhkus ja puudumine** vahekaart **Lingid** jaotises **Seadistamine** valik **Puhkuse ja puudumise tüübid**.

2. Valige loendist puhkuse ja puudumise tüüp. Seejärel valige jaotises **Üldine** väljal **Ühik** puhkuseühik. Saate valida **Tunnid** või **Päevad**.

3. Valikuline: kui valisite väljal **Ühik** väärtuse **Tunnid**, saate kasutada välja **Luba poole päeva definitsioon**, et määrata, kas töötajad saavad valida esimese poolaasta või teise pool vaba päeva, kui nad taotlevad poole päevast puhkust.

Uue puhkustaotluse esitanud töötajad saavad puhkusetaotluse koostamiseks valida erinevad puhkusetüübid. Kõigil ühe puhkusetaotluse osana valitud puhkusetüüpidel peaks siiski olema sama puhkuseühik. Töötajad saavad iga puhkuse tüübi puhkusühikut vaadata vormil **Taotle puhkust**.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkuste ja puudumiste plaani loomine](hr-leave-and-absence-plans.md)
- [Looge töögraafik](hr-leave-and-absence-working-time-calendar.md)
- [Puhkuse katkestamine](hr-leave-and-absence-suspend-leave.md)
- [Puhkuse ostu- ja- müügitaotluste töövoo loomine](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
