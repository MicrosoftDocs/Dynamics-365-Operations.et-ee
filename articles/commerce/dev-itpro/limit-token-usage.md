---
title: Piira makse loa kasutust
description: See artikkel kirjeldab funktsiooni, mis piirab makselubade kasutamist Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709370"
---
# <a name="limit-payment-token-usage"></a>Piira makse loa kasutust

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See artikkel kirjeldab funktsiooni, mis piirab makselubade kasutamist Microsoft Dynamics 365 Commerce. Loa kasutamine on piiratud müügitellimuse ulatusega või kui kliendi nõustumine on antud, salvestatakse failis kaardina.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Luba | Dynamics 365 süsteemis viidatud XML-suur bloobi rakendus, mis talletab makseviited kande eesmärkidel. |
| Fail kaardiga | Salvestatud kaardiviite tõend, mis on kokku lepitud tulevaseks kasutamiseks Dynamics 365 süsteemis või makselüüsis ja mis on omane kliendi kontole. |

Makse loa kasutuse limiidid kehtivad mis tahes keskkonnas, mis kasutab makselüüsiteenust, kus kasutatakse korduvaid lubasid. [Puhvrist Dynamics 365 Payment Connector for Puhvri](adyen-connector.md) kasutab korduvaid makselubasid järgmiste tellimistoimingute sooritamiseks, nt autoriseerimise korrigeerimine ja uuesti autoriseerimine.

Et aidata kontrollida, kuidas neid korduvaid makselubasid kogu süsteemis kasutatakse, **piirab makse loa** kasutamise piiramine tellimuse konteksti funktsiooniga korduva loa kasutamist süsteemis müügitellimuse ulatusele. Kui see on lubatud, muudab funktsioon Commerce headquartersi kasutajaliidest, värskendades makse sisestuslehti ja piirates võimalust valida möödunud kliendimakse viiteid uutes kandeeksemplarides kasutamiseks.

See funktsioon aitab vastata kasutusreeglitele mõne makse väljastaja puhul, nt Visa. Visa põhireeglites [ja Visa toote](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) ja teenuse reeglites määrab Visa, et maksetõendeid tuleb piirata kande ulatusega, välja arvatud juhul, kui kaardi kasutaja nõustub teisiti.

Makse **loa kasutamise piiramine tellimuse kontekstifunktsiooniga** on asjakohane ainult siis, kui kasutate makselüüsiteenust, mis kasutab korduvate maksete loa viiteid.

## <a name="enable-the-feature"></a>Funktsiooni lubamine

Makse loa **kasutamise piiramiseks tellimuse konteksti funktsiooni lubamiseks minge rakenduse Commerce headquarters teie keskkonnas tööruumide funktsioonihaldusesse,** **\>** **leidke ja valige suvand Piira makse loa kasutust, et tellida konteksti loendis ja seejärel valige Luba** kohe.**·**

## <a name="limit-payment-token-usage"></a>Piira makse loa kasutust

Kui see funktsioon on lubatud, uuendavad makseviisi hõivamiseks kasutatavad Commerce headquartersi lehed viisi, kuidas need viidete kliendi makseviisidele, mis on kliendi jaoks failis. Uuendus mõjutab peamiselt kahte toiminguvaldkonda:

- Kliendikaardi sisestamise kuidas failis kliendi nimel sisestatakse
- Kuidas talletatakse kliendiga seotud makseteavet tulevaste müügitellimuste maksekirjete jaoks

Kui klienditehingud ärikanalite suhtes salvestatakse makse üksikasjad müügitellimuse kontekstiga. Müügitellimuse kontekst piirab makseluba nii, et seda ei kasutata makseviinana makselehe kliendikirje suhtes uute või redigeeritud müügitellimuste maksete jaoks Commerce Headquartersis.

### <a name="payment-form-changes"></a>Maksevormi muudatused

Kui kõnekeskus või rakendus Commerce Headquarters kasutaja võtab kliendilt müügitellimuse eest makse, esitatakse maksemeetodi valiku üksikasjad makselehel. Kui makse **loa** kasutamise piiramine tellimuse konteksti funktsiooniga on lubatud, kui kasutaja valib makselehel plussmärgi (**+**), siis kuvatakse ainult "kaart failis". Muudatused nõuavad, et kõnekeskus või commerce headquartersi kasutaja **sisestaks** kõik makse üksikasjad, mis klient esitas, kui need täitsid uue müügitellimuse kande kohta kliendi makseteabe sisestamise lehele.

Välja Number väärtuste loend **sisaldab** ainult kaardiviiteid, mis on seotud kliendiga, kellel on fail kaardiga. See filtreerib välja kõik möödunud makseviited, mis pole müügitellimuse jaoks ulatusega seotud.

Plussmärk (**+**) **väljal** Number jääb kättesaadavaks ja seda saab kasutada makseteabe sisestamiseks, mille klient esitas kandele, mis on seostatud töödeldav müügitellimusega.

### <a name="how-cards-on-file-work"></a>Kuidas kaardid failis töötavad

Kui makse **loa** kasutamise piiramine tellimuse konteksti funktsiooniga on lubatud, on failis kaart korduv makseluba, mis salvestatakse kliendi kirje suhtes ja ei ole piiratud müügitellimuse ulatusega. Failikaart võimaldab uuele müügitellimuse makselehel olevale makselehel olevale Commerce Headquartersi kasutajatele kiirviite. See loa viide kehtib ainult Dynamics 365 keskkonna puhul. Makselüüsiteenust iFrame kasutavad võrgukanalid, mis laseb kasutajatel maksemoodulis tulevikus kasutamiseks makseviisi salvestada, talletab makselüüs need viited turvaliselt eraldi viitena failis Dynamics 365-kaardile.

Näiteks kui Dynamics 365 Commerce Puhvrit Payment Connectorit kasutatakse võrgukanalis, iFrame siis maksemoodulisse krediitkaarditeabe sisestavad kliendid näevad järgmise autenditud võrguostu puhul ainult lüüsiteenuse salvestatud kaardiviiteid. Nad ei näe Dynamics 365 keskkonnas talletatud kaarti failis maksemooduli suvandina iFrame. Samamoodi, kui ostjad esitavad tellimuse kõnekeskuse kaudu, ei esitata nende võrgusalvestatud kaardi viiteid kõnekeskuse kasutajale valikutena. Kõnekeskuse kasutaja näeb tulevaste tellimuste salvestamiseks Dynamics 365 süsteemist pärit failiviidetes ainult eelmisi kaartisid (nagu klient on kokku leppinud).

Rakenduse Commerce headquarters kasutajad saavad kliendi puhul kaarti failina salvestada, valides rakenduse Jaemüügi- **ja Ärikliendid \>** ning valides kliendi kontokirje. Jaotises Kliendi **\> häälestud** saavad kasutajad, kellel on luba makselehti töödelda, kasutada krediitkaardi sisestamise lehte, et sisestada maksekaart, **mida** talletatakse tulevaste kannete faili. See toiming aitab säästa aega tulevaste müügitellimuse maksete töötlemisel kliendile. Kõnekeskuse ja Commerce headquartersi kasutajad peaksid sisestama kaardi failikaardi üksikasjadesse ainult juhul, kui klient nõustub tulevikus kaardiviidet kasutama.

Kui **soovite kasutada märkeruutu Salvesta** edaspidiseks kasutamiseks, võimaldab rakendus Commerce Headquarters makselehtede allosas kasutajad kaarti edaspidiseks kasutamiseks salvestada. Seda märkeruutu tuleks kasutada ainult juhul, kui klient nõustub failis kaarti tulevaste kannete puhul kasutama. Saate kuvada või **piirata** **·** **·** **märkeruutu Salvesta tulevikuks, kasutades commerce headquartersi kõnekeskuse parameetrite lehe vahekaardil Makse suvandit Luba kliendikaart failil.** Kui see valik on seatud valikule **Jah**, saavad commerce headquartersi kasutajad, kellel on **makselehtede** töötlemise luba, salvestada failile kaardi, kasutades märkeruutu Tulevikuks salvestamine. Kui suvandi väärtuseks on määratud **Ei**, ei ole märkeruut saadaval Commerce Headquartersi kasutajatele, kellel on makselehtede töötlemise luba. Suvandit **Luba** kliendikaart failis saab kasutada, kui teie ettevõte soovib piirata korduvate lubade kasutamist Commerce Headquartersis, kuid ei soovi veel failis kaardi salvestamist ilma protseduurita, mis tagab kliendi eelneva loa andmise.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Äri peakontori lehed, kus kehtivad korduvate loa piirangud.

Loa piirangu ulatuse määramise funktsioon mõjutab järgmisi alasid Commerce Headquartersis, kui see funktsioon on lubatud:

- Kliendi makseteave müügitellimuse **maksetes Sisestage \>\> kliendimakse**
- Järjepidevad tellimused
- Osamaksed
- Müügireskontro krediitkaardimaksed

### <a name="manage-payment-tokens-archiving-or-removal"></a>Hallake makselubasid (arhiveerimine või eemaldamine)

Makselubasid **·**, mis loodi enne seda, kui makse loa kasutamise piiramine tellimuse kontekstifunktsiooni lipuga oli lubatud (või kui funktsioon keelati) jäävad süsteemis "valimata" ja sellele saab viidata Commerce headquartersi makselehe valikuloendites. Neid lubasid saab commerce headquartersis regulaarselt eemaldada kahel viisil:

- Kasutage krediitkaardikande **andmete arhiivi lehte**, et seadistada töö, mis maksmislubasid regulaarselt uuendab või arhiivib. Kui seadistate suvandi **Kustuta andmed arhiveerimiseta** **valikule Jah**, kustutatakse need sõned, **mis vastavad sättele Minimaalne kande vanus (** päevades). Lisateavet vt krediitkaardikande [andmete arhiivist](archive-cc-data.md).
- Kasutage uut krediitkaardi **lubade** lehte (**\>\>\>** Müügireskontro päringud ja aruanded Likvideeri krediitkaardi tõend), mis võimaldab teil käitada või seadistada pakett-töö, mis kustutab makselubasid. Saate määrata järgmised parameetrid.

    - Minimaalne **loa vanus päevades peab** olema 90 või enam päeva.
    - Taustal **käitatud sätteid saab** kasutada kordumise või teatiste **sätete** määratlemiseks **·**.
    - Pakett-tööde grupi saab määrata konkreetse grupi ülesande käitamiseks.
    - Kui suvandi **Privaatne** väärtus on **Jah**, saab seda käitada ainult töö loonud kasutaja.
    - Väärtuse Jah säte **kriitilise** töö **suvandile** tagab, et süsteem jälgib aktiivselt töö olekut.

Kustutatud lubasid ei saa tuua. Seadistage **välja Minimaalne loa vanus** päevades vahemikku, mis sobib kõige pikema kande tööeaga teie keskkonnas (autoriseerimisest hõivamiseks või tagasimakseks).

## <a name="additional-resources"></a>Lisaressursid

[Maksete KKK](payments-retail.md)

[Maksmismoodul](../add-checkout-module.md)

[Maksemoodul](../payment-module.md)
