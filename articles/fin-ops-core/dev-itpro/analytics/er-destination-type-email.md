---
title: ER-i sihtkoha tüübi e-post
description: Selles teemas selgitatakse, kuidas konfigureerida meilisihtkohta iga elektroonilise aruandluse (ER) vormingu komponendi FOLDER või FILE jaoks.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4ee1ae4d8a106e467640a8cbcf5986e770395431
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343856"
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

## <a name="enable-an-email-destination"></a>Meili sihtkoha lubamine

Ühe või mitme väljundfaili saatmiseks meiliga järgige neid samme.

1. Vormingu komponentide rühmitamiseks lehel **Elektroonilise aruandluse sihtkoht** kiirkaardil **Faili sihtkoht** valige ruudustikus komponendid või komponentide grupp.
2. Valige **Sätted** ja seejärel dialoogiboksi **Sihtkoha sätted** vahekaardil **E-kiri** määrake suvandi **Lubatud** väärtuseks **Jah**.

[![Meili sihtkoha jaoks suvandi Lubatud määramine väärtusele Jah.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>Meili sihtkoha konfigureerimine

### <a name="email-content"></a>Meili sisu

Saate redigeerida meilisõnumi teemat ja keha.

Sisestage **teema** väljale e-kirja teema tekst, mis peaks ilmuma käitusajal loodud elektroonilise teate teemaväljal. Sisestage **keha** väljale e-kirja keha tekst, mis peaks ilmuma käitusajal loodud elektroonilise teate kehaväljal. Saate seadistada e-kirja teema ja kehateksti jaoks püsiteksti või kasutada ER [valemeid](er-formula-language.md) e-kirjade teksti dünaamiliseks loomiseks käitusajal. Konfigureeritud valem peab tagastama v''rtuse [Stringi](er-formula-supported-data-types-primitive.md#string) tüübi.

Teie meili kehatekst on koostatud TEKSTI või HTML vormingus, sõltuvalt meili kliendist. Võite kasutada mis tahes paigutust, laadi ja kaubamärki, mida HTML ja tekstisisene kaskaadlaadistik (CSS) võimaldavad.

> [!NOTE]
> Meilikliendid kehtestavad paigutuse ja stiili piiranguid, mis võivad nõuda sõnumi sisus kasutatava HTML-i ja CSS-i korrigeerimist. Soovitame teil tutvuda HTML-i loomise heade tavadega, mida kõige populaarsemad meilikliendid toetavad.
>
> Kasutage õiget kodeeringut, et juurutada tagasipöördumine, sõltuvalt keha vormindusest. Lisateabeks vaata definitsiooni [Strringi](er-formula-supported-data-types-primitive.md#string) andmetüübist.

### <a name="email-addresses"></a>Meiliaadressid

Seal saate konfigureerida e-kirja saatja ja e-kirja adressaadid. Vaikimisi saadetakse meil praeguse kasutaja nimel. Teise e -posti saatja määramiseks peate konfigureerima välja **Saatja**.

> [!NOTE]
> Kui meili sihtkoht on konfigureeritud, on väli **Saatja** nähtav ainult kasutajatele, kellel on `ERFormatDestinationSenderEmailConfigure` turbeõigus, **Konfigureerige saatja meiliaadress ER-vormingu sihtkohtade** jaoks.
>
> Kui e-posti sihtkohta pakutakse muutmiseks aadressil [käitamine](electronic-reporting-destinations.md#security-considerations) on väli **Saatja** nähtav ainult kasutajatele, kellel on turbeõigus `ERFormatDestinationSenderEmailMaintain`, **Säilita saatja e-posti aadress ER-vormingus sihtkoha jaoks**.
>
> Kui väli **Saatja** on konfigureeritud kasutama muud e-posti aadressi kui praegune kasutaja, peab luba **Saada kui** või **Saada nimel** luba olema õigesti [seadistatud](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group?view=o365-worldwide) täiendavalt. Vastasel juhul ilmneb käitusajal järgmine erand: "Ei saa saata e-kirja aadressil \<from email account\> kontolt \<current user account\>, palun kontrollige luba "Saada kui aadressil \<from email account\>."

Saate konfigureerida välja **Alates** tagastama rohkem kui ühte meiliaadressi. Sel juhul kasutatakse saatja e-posti aadressina loendi esimest aadressi.

Meilisõnumi adressaatide määramiseks peate konfigureerima väljad **Adressaat** ja **Koopia** (valikuline).

Elektroonilise aruandluse meiliaadresside konfigureerimiseks on kaks võimalust. Konfiguratsiooni saab lõpule viia samamoodi, nagu prindihalduse funktsioon seda lõpule viib, või saate meiliaadressi lahendada, kasutades viitena ER konfiguratsioonile valemi kaudu.

## <a name="email-address-types"></a>Meiliaadressi tüübid

Kui valite suvandi **Redigeeri** välja **Saatja**, **Saaja** või **Koopia** juurdes dialoogiboksis **Sihtkoha sätted**, kuvatakse dialoogiboks **E-kirja saatja**, **E-kirja saaja** või **E-kirja koopia**. Seal saate konfigureerida e-kirja saatja ja e-kirja adressaadid. Valige käsk **Lisa** ja seejärel valige kasutatava meiliaadressi tüüp. Praegu toetatakse kahte tüüpi: **Prindihalduse meiliaadress** ja **Konfigureerimismeil**.

[![Meiliaadressi tüübi valimine.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Prindihalduse meiliaadress

Kui valite meiliaadressi tüübiks **Prindihalduse meiliaadress**, saate sisestada dialoogiboksi **E-kirja saatja**, **E-kirja saaja** või **E-kirja koopia** dialoogiboksi, seadistades järgmised väljad:

- Valige väljal **Meilisõnumi allikas** suvand **Puudub**.
- Sisestage parandatud meiliaadressid väljale **Täiendavad meiliaadressid, eraldatud semikooloniga**.

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
- Juriidiline isik

Näiteks meili sihtkoha konfigureerimiseks ER-i vormingus, mida kasutatakse hankija maksete töötlemiseks, valige roll **Hankija**.

Pärast soovitud rolli valimist valige nupp **Seo** (keti sümbol) välja **Meili allika konto** kõrval, et avada leht [Valemi kujundaja](general-electronic-reporting-formula-designer.md). Seejärel saate kasutada seda lehekülge, et konfigureerida käitusajal tagastatav valem, osapoole konto number, mis määratakse töödeldud dokumendist konfigureeritud rollile meili sihtkohta.

> [!NOTE]
> Valemid on ER-i konfiguratsiooni põhised.

Sisestage lehe **Valemi kujundaja** väljale **Valem** dokumendile vastav toetatud rolli viide. Selle asemel, et tippida paanile **Andmeallikas** viide, leidke ja valige andmeallika sõlm, mis tähistab konfigureeritud rolli kontot, ja valige seejärel valemi värskendamiseks suvand **Lisa andmeallikas**. Näiteks kui konfigureerite meili sihtkoha **ISO 20022 krediidi edastamise** konfiguratsioonile, mida kasutatakse hankija maksete töötlemiseks, on hankija kontot esindav sõlm `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Meili allika konto konfigureerimine.](./media/er_destinations-emaildefineaddresssource.gif)

Kui konfigureeritud rolli kontonumbrid on kordumatud kogu Microsoft Dynamics 365 Finance’i eksemplari jaoks, võib välja **Meili allika ettevõte** dialoogiboks **Meili saaja** jääda tühjaks.

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

### <a name="configuration-email"></a>Konfigureerimismeil

Valige meiliaadressi tüübiks **Konfiguratsiooni meil**, kui teie kasutataval konfiguratsioonil on andmeallikate sõlm, mis annab tulemuseks ühe meiliaadressi või mitu meiliaadressi, mis on eraldatud semikoolonitega (;). Saate kasutada valemi kujundajas [andmeallikaid](general-electronic-reporting.md#FormatComponentOutbound) ja [funktsioone](er-formula-language.md#Functions), et hankida õigesti vormindatud meiliaadress või õigesti vormindatud meiliaadressid, mis on semikoolonitega eraldatud. Näiteks, kui kasutate konfiguratsiooni **ISO 20022 kreediti edastamine**, siis sõlm, mis tähistab hankija esmast meiliaadressi hankija kontaktandmetest, kuhu kaaskiri tuleb saata, on `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Meiliaadressi allika konfigureerimine.](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Vormingu komponentide rühmitamine

Vormingu komponentide rühmitamiseks lehel **Elektroonilise aruandluse sihtkoht** kiirkaardil **Faili sihtkoht** valige ruudustikus komponendid ja seejärel valige **Rühmita**.

**Meil** on ainus eelnevalt konfigureeritud sihtkoht, mis on valitud komponentide puhul veel saadaval. Ühtegi teist eelnevalt konfigureeritud sihtkohta pole saadaval, kuna neid ei toetata komponentide grupi jaoks. Nendest muudatustest teavitatakse teid vastavalt vajadusele.

Eelnevalt lisatud kirjet peetakse loodava grupi päiseks. Selle päise kirje sisaldab grupi meili sihtkoha sätteid. Teised kirjed on grupi liikmed, kes kasutavad grupi päise kirje meili sihtkoha sätteid.

Vormingu komponentide rühmitamise tühistamiseks valige kiirkaart **Faili sihtkoht**, mis kuulub gruppi, ja seejärel valige käsk **Tühista rühmitamine**.

- Kui valite päise kirje, tühistatakse kogu grupi rühmitamine.
- Kui valite liikme kirje ja see on grupi viimase liikme kirje, tühistatakse kogu gruppi rühmitamine.
- Kui valite liikme kirje, mis ei ole grupi viimase liikme kirje, siis see kirje jäetakse praegusest grupist välja.

Järgmisel joonisel on kujutatud ER-i vormingu struktuur, mis on konfigureeritud tootma tihendatud väljamineva faili, mis sisaldab märgukirja märget ja vastavaid kliendi arveid PDF-vormingus.

[![Väljaminevaid dokumente genereeriva ER-i vormingu struktuur.](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Järgmisel joonisel on kujutatud selles teemas kirjeldatud protsessi üksikute komponentide grupeerimiseks ja uue grupi sihtkoha **Meil** lubamiseks, et märgukirja teade saadetakse koos vastava kliendi arvetega meili manustena.

[![Üksikute komponentide grupeerimine ja meili sihtkoha lubamine.](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Valemikoostaja elektroonilises aruandluses (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
