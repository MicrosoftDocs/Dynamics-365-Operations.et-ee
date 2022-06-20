---
title: Kuluarvutusparameetri väärtuste häälestus
description: Mooduli Väljalaadimiskulu häälestamisel saate määratleda mitu ühiste väärtuste kogumit, mis on saadaval rakenduse muudes osades kindlat tüüpi kuluarvutusparameetrite väärtuste valimisel. See artikkel selgitab, kuidas neid väärtuskomplekte seadistada.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ca3633cd8a3fb053bda597b968003685aa2326ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852327"
---
# <a name="costing-parameter-values-setup"></a>Kuluarvutusparameetri väärtuste häälestus

[!include [banner](../../includes/banner.md)]

Mooduli **Väljalaadimiskulu** häälestamisel saate väärtuse kohta määratleda mitu ühiste väärtuste ja seostuvate sätete komplekti. Need väärtused on siis saadaval, kui valite rakenduse muudes osades kindlat tüüpi kuluarvutusparameetrite väärtused. See artikkel selgitab, kuidas neid väärtuskomplekte seadistada.

## <a name="set-up-cost-type-codes"></a>Kulutüübi koodide häälestamine

Kulutüübi koodid määravad kulu tüübi, mis tekib kauba väljalaadimisel lattu, või teekonna väljalaadimiskulud. Kuigi need suurendavad tavaliselt kaupade väärtust, saab neid kasutada ka summade lisamiseks pearaamatusse. Pearaamatu korrigeerimisi kasutatakse siis, kui kulu koguneb aja jooksul või teekondade jada jooksul ning tasaarvestatakse ühe kandega.

> [!NOTE]
> Kui kulutüübi tabelit kasutavad mitu juriidilist isikut ühiselt, peab ka kontoplaan olema juriidiliste isikute jaoks ühiskasutatav. Vastasel juhul ei tööta sisestuskanded õigesti.

Kulutüübi koodide häälestamiseks valige **Väljalaadimiskulu \> Kuluarvutuse häälestamine \> Kulutüübi koodid**. Toimingupaani nuppude abil saate luua uusi kulutüübi koode, redigeerida olemasolevaid koode või kustutada valitud kulutüübi.

Järgmises tabelis kirjeldatakse igas kulutüübi koodi jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kulutüübi kood | Sisestage kulutüübi koodi nimi. |
| Kirjeldus | Sisestage kulutüübi koodi kirjeldus. |
| Kasuta saatmiskurssi | Seadke selle suvandi väärtuseks *Jah*, kui nende kulude väärtuse arvutamiseks tuleb kasutada teekonna vahetuskurssi (mõnikord nimetatakse seda halduskursiks). Sel juhul kasutatakse välisvaluutaarvete vahetamiseks standardse vaike- või hetkekursi asemel saatmiskurssi. |
| Aruandluskategooria | Selle välja abil luuakse kulutüübi aruandluskategooria. Aruandeid saab printida kas aruandluskategooriate või kulutüüpide kaupa. |
| Deebeti tüüp | Saate valida, kas kulutüüp peaks debiteerima kaupa, pearaamatukontot või hankijat. |
| Deebeti sisestamine | Kui välja **Deebeti tüüp** väärtuseks on seatud *Pearaamatukonto*, valige sisestamise kirjeldus. |
| Deebetkonto | Kui välja **Deebeti tüüp** väärtuseks on seatud *Pearaamatukonto*, valige kasutatav pearaamatukonto. |
| Kreediti tüüp | Saate valida, kas see kulutüüp peaks krediteerima kaupa, pearaamatukontot või hankijat. |
| Kreediti sisestamine | Kui välja **Kreediti tüüp** väärtuseks on seatud *Pearaamatukonto*, valige sisestamise kirjeldus. |
| Kreeditkonto | Kui välja **Kreediti tüüp** väärtuseks on seatud *Pearaamatukonto*, valige kasutatav pearaamatukonto. |
| Kliiringukonto | Valige kulutüübi jaoks kliiringukonto. Vastavusseviimise tagamiseks soovitame määrata iga kulutüübi kohta eraldi kliiringukonto. |
| Standardomahinna sisestustüüp | Kui kasutate standardset kuluarvutust, valige sisestamise kirjeldus. |
| Standardomahinna hälbe konto | <p>Kui kasutate standardset kuluarvutust, kasutatakse siin määratud kontot mis tahes hälbe sisestamiseks. See konto kasutab lehel **Kaubahinnad** esitatud väljalaadimiskulude jaotust. See jaotus luuakse perioodilise protseduuri abil hindade uuendamiseks.</p><p>Näiteks kauba standardomahind on 15,00 $, FOB on 13,00 $ ja vedu on 2,00 $. Laovaru eest arve saamisel võetakse kaup vastu hinnaga 15,00 $, kuid kauba puhul kehtib 2,00 $ standardne hinnahälve, sest tegelik FOB on 13,00 $. See hälve sisestatakse kauba sisestusprofiilis häälestatud standardhinna hälbekontole. Kuna hinnanguline veokulu on 2,00 $, pole laoarve sisestamisel mingit hälvet. Veoarve laekumisel on veokulu ühiku kohta siiski 2,50 $. Seetõttu sisestatakse määratud kulusse 0,50 $ hälve. |
| Libiseva keskmise hälbe konto | <p>Kui kasutate libiseva keskmisega kuluarvutust, kasutatakse siin määratud kontot mis tahes hälbe sisestamiseks.</p><p>Näiteks on hinnanguline veokulu 2,00 $. Veoarve laekumisel on veokulu ühiku kohta siiski 2,50 $. Seetõttu tuleb sisestada 0,50 $ hälve.</p><p>Kui lehel **Väljalaadimiskulu parameetrid** on suvandi **Sisesta korrigeerimised hälbena** väärtuseks seatud *Jah*, sisestatakse kõik hinnanguliste ja tegelike saatmiskulude vahelised hälbed siin määratud libiseva keskmise hälbe kontole. Kui suvandi **Sisesta korrigeerimised hälbena** väärtuseks on seatud *Ei*, kasutatakse standardfunktsiooni ja hälvet rakendatakse sõltuvalt vabast kaubavarust kas varudele või siin määratud libiseva keskmise hälbe kontole.</p> |
| Tasu juurdekasvukonto | Valige konto, mida kasutatakse ostuarve sisestamisel kuluhinnangute kogumiseks. Seda välja kasutatakse ainult siis, kui lehel **Väljalaadimiskulu parameetrid** on vahekaardi **Üldine** kiirkaardil **Kuluarvutus** suvandi **Kasuta kulutüübi viitvõlgade kontot** väärtuseks seatud *Jah*. |
| Tasukonto | Saate valida konto, mida kasutatakse tarnija arveldatud sissetulevate transpordikulude kajastamiseks. Summa lisatakse deebetina. Vastaskonto on varude variatsiooni konto. Seda sisestamist kasutatakse ainult siis, kui lehel **Ostureskontro parameetrid** on suvandi **Sisesta pearaamatu tasukontole** väärtuseks on seatud *Jah*. |
| Hälbekonto | Konto, mida kasutatakse ostuarve sisestamisel kulu viitvõlgade tasakaalustamiseks. Seda välja kasutatakse ainult siis, kui lehel **Väljalaadimiskulu parameetrid** on vahekaardi **Üldine** kiirkaardil **Kuluarvutus** suvandi **Kasuta kulutüübi viitvõlgade kontot** väärtuseks seatud *Jah*. |

## <a name="vendor-cost-type-groups"></a>Hankija kulutüübigrupid

Hankija kulutüüpide grupid aitavad määratleda, kuidas *automaatse kulu* tasud leitakse ja rakendatakse teekonnale. Sarnaste impordikuludega hankijad on omavahel lingitud. Näiteks maksavad kõik arenevate turgude hankijad sama tollimaksuprotsenti sama tüüpi toodete eest, mis ostetakse väljakujunenud turult.

Hankija kulutüüpide gruppe saate hallata, valides **Väljalaadimiskulu \> Kuluarvutuse häälestus \> Hankija kulutüüpide grupid**. Lehel **Hankija kulutüüpide grupid** on ruudustik, kus on loetletud kõik olemasolevad hankija kulutüüpide grupid. Toimingupaani nuppude abil saate ruudustiku ridu lisada, eemaldada ja redigeerida.

Järgmises tabelis kirjeldatakse ruudustiku igal real saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Hankija kulutüübigrupid | Sisestage hankija kulutüüpide grupi kordumatu nimi (nt *Arenevad turud*). |
| Kirjeldus | Sisestage hankija kulutüüpide grupi kirjeldus. See kirjeldus võib sisaldada üksikasju hankija grupiga seotud tasu taseme või tüübi kohta. |

## <a name="item-cost-type-groups"></a>Kauba kulutüübigrupid

Kauba kulutüüpide grupid aitavad määratleda, kuidas *automaatse kulu* tasud leitakse ja rakendatakse teekonnale. Sarnased kaubad on omavahel lingitud. Näiteks võivad kõik kaubad, mille tollimaksumäär on 5 protsenti, kuuluda kindlasse kulutüübi gruppi.

Kauba kulutüüpide gruppe saate hallata, valides **Väljalaadimiskulu \> Kuluarvutuse häälestus \> Kauba kulutüüpide grupid**. Lehel **Kauba kulutüüpide grupid** on ruudustik, kus on loetletud kõik olemasolevad kauba kulutüüpide grupid. Toimingupaani nuppude abil saate ruudustiku ridu lisada, eemaldada ja redigeerida.

Järgmises tabelis kirjeldatakse ruudustiku igal real saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kauba kulutüübigrupid | Sisestage kauba kulutüüpide grupi kordumatu nimi (nt *Tollimaks 5%*). |
| Kirjeldus | Sisestage kauba kulutüüpide grupi kirjeldus. See kirjeldus võib sisaldada üksikasju kaubagrupiga seotud tasu taseme või tüübi kohta. |

> [!NOTE]
> Kauba kulutüüp lingitakse kaubaga lehe **Väljastatud toode** kiirkaardi **Ost** välja **Kulutüübi grupp** kaudu.

## <a name="transfer-order-cost-type-groups"></a>Üleviimistellimuse kulutüübi grupid

Üleviimistellimuse kulutüüpide grupid aitavad määratleda, kuidas *automaatse kulu* tasud leitakse. Sarnased kaubad on omavahel lingitud. Näiteks võivad kõik kaubad, mille tollimaksumäär on 7 protsenti, kuuluda kindlasse kulutüübi gruppi.

Üleviimistellimuse kulutüüpide gruppe saate hallata, valides **Väljalaadimiskulu \> Kuluarvutuse häälestus \> Üleviimistellimuse kulutüüpide grupid**. Lehel **Üleviimistellimuse kulutüüpide grupid** on ruudustik, kus on loetletud kõik olemasolevad üleviimistellimuse kulutüüpide grupid. Toimingupaani nuppude abil saate ruudustiku ridu lisada, eemaldada ja redigeerida.

Järgmises tabelis kirjeldatakse ruudustiku igal real saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Üleviimistellimuse kulutüübi grupid | Sisestage üleviimistellimuse kulutüüpide grupi kordumatu nimi (nt *Tollimaks 7%*). |
| Kirjeldus | Sisestage üleviimistellimuse kulutüüpide grupi kirjeldus. See kirjeldus võib sisaldada üksikasju üleviimistellimuse kulutüübi grupiga seotud tasu taseme või tüübi kohta. |

> [!NOTE]
> Üleviimistellimuse kulutüüp lingitakse kaubaga lehe **Väljastatud toode** kiirkaardi **Ost** välja **Üleviimistellimuse kulu grupp** kaudu.

## <a name="cost-templates"></a>Kulumallid

Kulumallide abil saate seada vaikeväärtused sätetele, mida kuluhinnangut saavad kasutajad ei pruugi teada. Kulumallid aitavad vähendada hindamisprotsessi keerukust, minimeerides valikud, mille kasutajad peavad täpse prognoosi saamiseks määrama.

Kulumallide kasutamiseks valige **Väljalaadimiskulu \> Kuluarvutuse häälestamine \> Kulumallid**. Lehel **Kulumallid** on vasakpoolsel loendipaanil kuvatud kõik praegused kulumallid. Toimingupaani nuppude abil saate malle lisada, eemaldada ja redigeerida.

Järgmises tabelis kirjeldatakse iga malli jaoks saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Kulumall | Sisestage kulumalli kordumatu nimi. Nimi kirjeldab tavaliselt malli tegurit või kulu kordajat. |
| Kirjeldus | Sisestage kulumalli kirjeldus. |
| Saatmisettevõte | Saate valida kulumalliga seostatava saatmisettevõtte hankijakonto. |
| Tarneviis | Saate valida tarneviisi, mida kulumall peaks kauba eeldatava omahinna arvutamisel kasutama. See väli aitab määratleda kuluhinnangus kaupadega seostatud automaatsed kulud. |
| Saatmiskonteineri tüüp | Saate valida kulumalliga seostatava saatmiskonteineri tüübi. See väli aitab määratleda kuluhinnangus kaupadega seostatud automaatsed kulud. |
| Tollimaakler | Saate valida kulumalliga seostatava tollimaakleri (hankija). See väli aitab määratleda kuluhinnanguga seostatud automaatsed kulud. |
| Tegur | Saate sisestada kaupade lõplikule kuluhinnangule rakendatava teguri. Näiteks arvutatud kuluhinnangule 10 protsendi lisamiseks sisestage *1,10*. |

## <a name="volumetric-divisors"></a>Mahupõhised jagajad

Mahukaalu arvutamiseks kasutatakse mahulisi jagajaid. Iga saatmis-/kaubaveoettevõte koostab oma mahujagajad. Lisaks varieeruvad ettevõtte jagajad tavaliselt sõltuvalt tarneviisist. Näiteks õhu- ja meretranspordil on sageli väga erinevad jagajad. Ettevõte võib sõltuvalt saatmiskohast muuta oma reeglid ka keerulisemaks. Süsteem kasutab järgmist valemit mahulise kaalu leidmiseks: mahuline kaal = mahu ÷ MahulineDivisor.

Näiteks õhu kaudu saadetava paki maht on 3 kuupmeetrit (m³). Ettevõte võtab tasu mahukaalu järgi ja rakendab mahulist jagajat 6. See jagaja jagatakse mahuga mahulise kaalu määratlemiseks. Seega on selle näite mahuline kaal 3 kg÷ 6 = 0,5 kilogramm (kg).

Mahuliste jagajate häälestamiseks valige **Väljalaadimiskulu \> Kuluarvutuse häälestamine \> Mahulised jagajad**. Lehel **Mahulised jagajad** on ruudustik, kus on loetletud kõik olemasolevad mahulised jagajad. Toimingupaani nuppude abil saate ruudustiku ridu lisada, eemaldada ja redigeerida.

Järgmises tabelis kirjeldatakse ruudustiku igal real saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Saatmisettevõte | Saate valida mahulise jagaja seostatud saatmisettevõtte hankija konto. |
| Kulutüübi kood | Saate valida mahulise jagajaga seostatud kulutüübi koodi. Sellel väljal saate paigutada kulutüüpe aruandlusvahemikesse. Aruandeid saab printida kas aruandluskategooriate või kulutüüpide kaupa. |
| Lähtesadam | Saate valida lähtesadama, millele mahuline jagaja rakendub. |
| Mahupõhine jagaja | Saate sisestada reale rakendatava mahulise jagaja väärtuse. Iga paki maht jagatakse sellele väljale salvestatud väärtusega, et määrata pakendi mahuline kaal. |

> [!NOTE]
> Süsteem kasutab maksimaalset väärtust tegeliku kaalu **ja mahulise** **kaalu vahel**.
