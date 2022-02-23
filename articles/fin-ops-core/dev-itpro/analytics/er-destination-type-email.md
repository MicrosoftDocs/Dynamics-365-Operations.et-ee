---
title: ER-i sihtkoha tüübi e-post
description: Sellest teemast selgitatakse, kuidas konfigureerida meili sihtkoht iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.
author: NickSelin
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c6242ecb44a206aacc0e1b1b3c4f588eadd18882
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690122"
---
# <a name="email-er-destination-type"></a>ER-i sihtkoha tüübi e-post

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) vormingu käivitamisel saab luua ühe või mitu väljaminevat dokumenti. Vormingu **Kaust** või **Fail** komponente kasutatakse ER-i vormingutes, et määrata väljamineva dokumendi struktuur. Saate konfigureerida meili sihtkoha seda tüüpi komponentidele, et saata väljaminevaid dokumente meili manustena.

Saate konfigureerida meili sihtkoha iga ER-i vormingu komponendi **Kaust** või **Fail** jaoks. Sel juhul **saadetakse iga väljaminev dokument eraldi**. Selle sihtkoha sätte põhjal tarnitakse loodud dokument meili manusena. 

> [!NOTE]
> Kui dokumenti ei looda, kuna avaldis **Lubatud** asjaomase komponendi **Fail** jaoks on konfigureeritud tagastama loogikaväärtuse **Vale**, ühtegi meili ei saadeta, isegi kui meili sihtkoht on konfigureeritud ja komponendi jaoks lubatud.

Samuti saate [rühmitada](#grouping) mitu komponenti **Kaust** või **Fail** kokku ja seejärel konfigureerida meili sihtkoht kõigi grupi komponentide jaoks. Sel juhul saadetakse kõik väljaminevad dokumendid, mis kuuluvad gruppi kuuluvatele komponentidele, **ühe meili mitme manusena**. Selle sihtkoha sätte põhjal tarnitakse iga loodud dokument ühe meili manusena.

> [!NOTE]
> Kui vähemalt üks dokument luuakse komponentide rühmas komponendi **Fail** poolt, saadetakse meil. Kui rühmitatud komponentide poolt dokumenti ei looda, kuna avaldis **Lubatud** iga komponendi **Fail** jaoks on konfigureeritud tagastama loogikaväärtuse **Vale**, ühtegi meili ei saadeta, isegi kui meili sihtkoht on konfigureeritud ja selle komponentide rühma jaoks lubatud.
>
> **Meil** on ainus sihtkoht, mida saab konfigureerida komponentide grupi jaoks. Meili sihtkoha sättel põhineva dokumendi grupile kohaletoimetamiseks lisage veel üks sihtkoha kirje, valige soovitud komponent ja seejärel konfigureerige selle kirje teine sihtkoht.

Ühe ER-i vormingu konfiguratsiooni jaoks saab konfigureerida mitu komponentide gruppi. Sel viisil saate konfigureerida meili sihtkoha iga komponentide grupi ja meili sihtkoha iga komponendi jaoks.

## <a name="configure-an-email-destination"></a>Meili sihtkoha konfigureerimine

Väljundfaili või mitme väljundfaili meili teel saatmiseks valige lehe **Elektroonilise aruandluse sihtkoht** kiirkaardil **Faili sihtkoht** ruudustiku komponent või komponentide grupp ja seejärel valige **Sätted**. Kuvatava dialoogiboksi **Sihtkoha sätted** vahekaardil **Meil** määrake suvandi **Lubatud** väärtuseks **Jah**. Seejärel saate määrata meili adressaadid ning redigeerida meilisõnumi teemat ja kehateksti. Saate kas seadistada meilide teema ja kehateksti jaoks püsiteksti või kasutada meilitekstide loomiseks elektroonilise aruandluse [valemeid](er-formula-language.md), et dünaamiliselt luua meilitekste.

Elektroonilise aruandluse meiliaadresside konfigureerimiseks on kaks võimalust. Konfiguratsiooni saab lõpule viia samamoodi, nagu prindihalduse funktsioon seda lõpule viib, või saate meiliaadressi lahendada, kasutades viitena ER konfiguratsioonile valemi kaudu.

[![Meili sihtkoha jaoks suvandi Lubatud määramine väärtusele Jah](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Meiliaadressi tüübid

Kui valite suvandi **Redigeeri** välja **Saaja** või **Koopia** juurdes dialoogiboksis **Sihtkoha sätted**, kuvatakse dialoogiboks **Meili saaja**. Valige käsk **Lisa** ja seejärel valige kasutatava meiliaadressi tüüp. Praegu toetatakse kahte tüüpi: **Prindihalduse meiliaadress** ja **Konfigureerimismeil**.

[![Meiliaadressi tüübi valimine](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Prindihalduse meiliaadress

Kui valite meiliaadressi tüübiks **Prindihalduse meiliaadress**, saate sisestada dialoogiboksi **Meili adressaat** parandatud meiliaadressid, seadistades järgmised väljad.

- Valige väljal **Meilisõnumi allikas** suvand **Puudub**.
- Sisestage parandatud meiliaadressid väljale **Täiendavad meiliaadressid, eraldatud semikooloniga**.

![Parandatud meiliaadressi konfigureerimine](./media/er_destinations-emailfixedaddress.png)

Teise võimalusena saate hankida meiliaadresse selle osapoole kontaktandmetest, kelle jaoks väljamineva dokumendi loote. Parandamata meiliaadresside kasutamiseks väljal **Meili allikas** valige faili sihtkoha jaoks osapoole [roll](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles). Toetatud on järgmised rollid.

- Klient
- Tarnija
- Potentsiaalne klient
- Kontakt
- Konkurent
- Töötaja
- Kandidaat
- Potentsiaalne hankija
- Keelatud hankija

Näiteks meili sihtkoha konfigureerimiseks ER-i vormingus, mida kasutatakse hankija maksete töötlemiseks, valige roll **Hankija**.

Pärast soovitud rolli valimist valige nupp **Seo** (keti sümbol) välja **Meili allika konto** kõrval, et avada leht [Valemi kujundaja](general-electronic-reporting-formula-designer.md). Seejärel saate kasutada seda lehekülge, et konfigureerida käitusajal tagastatav valem, osapoole konto number, mis määratakse töödeldud dokumendist konfigureeritud rollile meili sihtkohta.

> [!NOTE]
> Valemid on ER-i konfiguratsiooni põhised.

Sisestage lehe **Valemi kujundaja** väljale **Valem** dokumendile vastav toetatud rolli viide. Selle asemel, et tippida paanile **Andmeallikas** viide, leidke ja valige andmeallika sõlm, mis tähistab konfigureeritud rolli kontot, ja valige seejärel valemi värskendamiseks suvand **Lisa andmeallikas**. Näiteks kui konfigureerite meili sihtkoha **ISO 20022 krediidi edastamise** konfiguratsioonile, mida kasutatakse hankija maksete töötlemiseks, on hankija kontot esindav sõlm `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Meili allika konto konfigureerimine](./media/er_destinations-emaildefineaddresssource.gif)

Kui konfigureeritud rolli kontonumbrid on kordumatud kogu Microsoft Dynamics 365 Finance’i eksemplari jaoks, võib välja **Meili allika ettevõte** dialoogiboks **Meili saaja** jääda tühjaks.

![Tühi meili allika välja ettevõte](./media/er_destinations-emaildefineaddresssourceformula.png)

Teise võimalusena võib teil olla olukord, kus erinevates ettevõtetes on registreeritud [globaalse aadressiraamatu](../../fin-ops/organization-administration/overview-global-address-book.md) erinevad osapooled ([juriidilised isikud](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) nii, et nad kõik kasutavad konfigureeritud rolli täitmiseks sama kontonumbrit. Sel juhul ei ole konfigureeritud rolli kontonumbrid kogu rakenduse Finance eksemplari jaoks kordumatud. Seetõttu ei saa te osapoole selgeks valimiseks määrata ainult kontonumbri. Samuti peate määrama ettevõtte, kus osapool on konfigureeritud rolli täitmiseks registreerinud. Valige nupp **Seo** (keti sümbol) välja **Meili allika ettevõte** kõrval dialoogiboksis **Meili saaja**, et avada leht [Valemi disainija](general-electronic-reporting-formula-designer.md). Seejärel saate kasutada lehekülge, et konfigureerida valemi, mis tagastab käitusajal ettevõtte koodi, mille ulatuses tuleb leida soovitud allikas.

> [!TIP]
> Kui peate kasutama ER-i vormingu käitamiseks ettevõtte koodi, kuid ER-i vorming ei anna ühtegi andmeallikat, millest ettevõtte koodi saab hankida, konfigureerige valem `GetCurrentCompany()`, kasutades sisseehitatud ER-i funktsiooni [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Valemid on ER-i konfiguratsiooni põhised.

Käitusajal kasutatava meiliaadressi tüübi määramiseks valige dialoogiboksis **Meili saaja** suvand **Redigeeri** välja **Saaja** kõrval, et avada rippmenüüga dialoogiboks **Meiliaadressi määramine**. Seejärel määrake järgmised väljad.

- Valige väljal **Eesmärk** soovitud eesmärgid. Kasutatakse ainult valitud eesmärkidega meiliaadresse tuvastatud osapoole kontaktidelt.
- Määrake suvandi **Esmane kontakt** väärtuseks **Jah**, et kasutada tuvastatud osapoole esmase meiliaadressina konfigureeritud meiliaadressi.

> [!NOTE]
> Kui eesmärgid on väljal **Eesmärk** valitud ja suvand **Peamine kontakt** on samal ajal määratud valikule **Jah**, kasutatakse käitusajal kõike meile, kus vähemalt üks konfiguratsioon vastab kriteeriumile.

![Meili allika atribuutide konto konfigureerimine](./media/er_destinations-emaildefineaddresssourceattributes.png)

### <a name="configuration-email"></a>Konfigureerimismeil

Valige meiliaadressi tüübiks **Konfiguratsiooni meil**, kui teie kasutataval konfiguratsioonil on andmeallikate sõlm, mis annab tulemuseks ühe meiliaadressi või mitu meiliaadressi, mis on eraldatud semikoolonitega (;). Saate kasutada valemi kujundajas [andmeallikaid](general-electronic-reporting.md#FormatComponentOutbound) ja [funktsioone](er-formula-language.md#functions), et hankida õigesti vormindatud meiliaadress või õigesti vormindatud meiliaadressid, mis on semikoolonitega eraldatud. Näiteks, kui kasutate konfiguratsiooni **ISO 20022 kreediti edastamine**, siis sõlm, mis tähistab hankija esmast meiliaadressi hankija kontaktandmetest, kuhu kaaskiri tuleb saata, on `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Meiliaadressi allika konfigureerimine](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Vormingu komponentide rühmitamine

Vormingu komponentide rühmitamiseks lehel **Elektroonilise aruandluse sihtkoht** kiirkaardil **Faili sihtkoht** valige ruudustikus komponendid ja seejärel valige **Rühmita**.

**Meil** on ainus eelnevalt konfigureeritud sihtkoht, mis on valitud komponentide puhul veel saadaval. Ühtegi teist eelnevalt konfigureeritud sihtkohta pole saadaval, kuna neid ei toetata komponentide grupi jaoks. Nendest muudatustest teavitatakse teid vastavalt vajadusele.

Eelnevalt lisatud kirjet peetakse loodava grupi päiseks. Selle päise kirje sisaldab grupi meili sihtkoha sätteid. Teised kirjed on grupi liikmed, kes kasutavad grupi päise kirje meili sihtkoha sätteid.

Vormingu komponentide rühmitamise tühistamiseks valige kiirkaart **Faili sihtkoht**, mis kuulub gruppi, ja seejärel valige käsk **Tühista rühmitamine**.

- Kui valite päise kirje, tühistatakse kogu grupi rühmitamine.
- Kui valite liikme kirje ja see on grupi viimase liikme kirje, tühistatakse kogu gruppi rühmitamine.
- Kui valite liikme kirje, mis ei ole grupi viimase liikme kirje, siis see kirje jäetakse praegusest grupist välja.

Järgmisel joonisel on kujutatud ER-i vormingu struktuur, mis on konfigureeritud tootma tihendatud väljamineva faili, mis sisaldab märgukirja märget ja vastavaid kliendi arveid PDF-vormingus.

[![Väljaminevaid dokumente genereeriva ER-i vormingu struktuur](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Järgmisel joonisel on kujutatud selles teemas kirjeldatud protsessi üksikute komponentide grupeerimiseks ja uue grupi sihtkoha **Meil** lubamiseks, et märgukirja teade saadetakse koos vastava kliendi arvetega meili manustena.

[![Üksikute komponentide grupeerimine ja meili sihtkoha lubamine](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Valemikoostaja elektroonilises aruandluses (ER)](general-electronic-reporting-formula-designer.md)
