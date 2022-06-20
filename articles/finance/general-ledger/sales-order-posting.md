---
title: Müügitellimuse sisestamine
description: See artikkel annab teavet lao sisestusreeglite lehe vahekaardi Müügitellimus kohta.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886309"
---
# <a name="sales-order-posting"></a>Müügitellimuse sisestamine

Lao **sisestusreeglite** lehe **müügitellimuse vahekaarti** kasutatakse müügitellimuste pearaamatusse sisestamise järjestuse juhtimiseks. Müügitellimuse pearaamatusse sisestatakse kaks peamist tegevust: 

- Saateleht
- Arve

Et müügitellimuse puhul sisestada füüsiline kanne (saateleht) pearaamatusse, peavad olema täidetud järgmised tingimused:

- Varude ja **laohalduse parameetrite lehel** peab ruut **Sisesta saateleht** pearaamatusse olema märgitud.
- **Müügitellimuse real valitud kauba** mudeligrupi lehel peab olema märgitud **ruut** Sisesta füüsiline ladu pearaamatusse.
- Lao sisestusreeglite **lehel** peab põhikontod olema määratud järgmistele sisestustüüpidele:
  - Tarnitud ühikute kulu
  - Tarnitud tuletusreegel

Finantskande (arve) sisestamiseks müügitellimuse pearaamatusse peavad olema täidetud järgmised tingimused:

- **Müügitellimuse real valitud kauba** mudeligrupi lehel peab olema märgitud **ruut** Sisesta finantsiline laovaru pearaamatusse.
- Lao sisestusreeglite lehel tuleb määrata **põhikontod** järgmiste sisestustüüpide jaoks:
  - Arveldatud ühikute kulu
  - Arveldatud tuletusreegel
  - Tulu
  - Allahindlus\*

> [!NOTE]
> Allahindluse konto on valikuline. Paljud raamatupidamisstandardid (nt GAAP ja IFRS) nõuavad, et allahindlused vähendavad müügitulu ja seetõttu ei kasutata neid kontosid paljudes stsenaariumides. Kui kohalikud reeglid seda lubavad, kasutage eraldi põhikontot allahindlusega müügihinna osa sisestamiseks.

Edasilükatud (hinnangulise) tulu väärtuse sisestamiseks pearaamatusse müügitellimuse saatelehe loomisel peavad järgmised tingimused olema täidetud:

- **Müügitellimuse real valitud kauba** mudeligrupi lehel peab olema märgitud **ruut** Sisesta füüsiline ladu pearaamatusse.
- Kauba mudeligrupi **lehel** peab märkeruut **Sisesta edasilükatud tulu kontole müügitarnel** olema valitud.
- **Varude ja laohalduse parameetrite lehel** peab ruut **Sisesta saateleht** pearaamatusse olema märgitud.
- **Varude ja laohalduse parameetrite lehel** peab ruut **Sisesta füüsiline** käibemaks olema märgitud.
- Müügireskontro **parameetrite** lehel peab **ruut Sisesta saateleht** pearaamatusse olema märgitud.
- Lao sisestusreeglite **lehel** peab põhikontod olema määratud järgmistele sisestustüüpidele:
  - Viivitusega tulu tarnimisel
  - Viivitusega tulu vastaskonto tarnimisel
  - Viivitusega käibemaks tarnimisel

> [!NOTE]
> Üldiselt soovitame teil lubada suvandid Sisesta füüsiline **ladu ja** **Sisesta saateleht pearaamatusse**. Nende valikute lubamine võib aidata kiirendada kuu lõpu sulgemistoiminguid, kuna viitvõlgu ei ole vaja käsitsi arvutada ega sisestada. Peale selle peegeldavad finantsaruanded automaatselt edasilükatud summasid ilma käsitsi sekkumiseta.

> [!IMPORTANT]
> Müügitarne **viittulukontole sisestamise valikut** ei kasutata tulu tuvastamisel. Lisateavet tulu tuvastamise kohta vt tulu tuvastamise [ülevaadet](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Sisestusprofiili näidiskonfiguratsioon 

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid koos näidis põhikontode ja kirjeldustega:
 
- Kliiringukonto **veerg** näitab, et sisestamistüüp on kliiringukonto. Kontole sisestatud summa tühistatakse hilisema kande sisestamisel automaatselt. 
- Veerg **P/F näitab** füüsilise sisestamise **P-d** ja finantsilist **sisestamist** F. 
- Veerg **Järgi** näitab, kas kindla sisestustüübi põhikonto on tavaliselt sama mis mõni muu sisestamistüüp. Veeru väärtus näitab tavaliselt kasutatavat sisestustüüpi.

> [!NOTE]
> Need põhikontod ja põhikonto nimed on ainult soovitused. Soovitame teil teha koostööd raamatupidajaga, et määratleda ärivajaduste jaoks parim konfiguratsioon.


| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Tarnitud ühikute kulu | 140100</br>140101 | Materjalide laoseis</br>Saadetud, arveldamata materjalid | Vara | Krediit | Jah | P | Arveldatud ühikute kulu | Kasutatakse müügitellimuse saatelehe sisestamisel. Konto vastaskonto on müüdud ja tarnitud kaupade omahind. Selle konto summa tühistatakse müügitellimuse arve sisestamisel. Võib-olla soovite kasutada kontot Saadetud, kuid arveldamata materjalid, et tähistada füüsilist laovaru ja reserveerida materjali laokonto finantsiliseks uuendamiseks. |
| Tarnitud tuletusreegel | 500150 | Viivitusega COGS | Kulu | Deebet | Jah | P  | Kasutatakse müügitellimuse saatelehe sisestamisel. Kontole vastaskonto on tarnitud ühikute omahind. Selle konto summa tühistatakse müügitellimuse arve sisestamisel. |
| Arveldatud ühikute kulu | 140100 | Materjalide laoseis | Vara | Krediit | Nr | R | Tarnitud ühikute kulu | Kasutatakse müügitellimuse arve sisestamisel. Selle konto vastaskonto on müüdud ja arveldatud kaupade omahind. See konto tähistab teie bilansikonto varusid. |
| Arveldatud tuletusreegel | 500100 | COGS-materjalid | Kulu | Deebet | Nr | R  | Kasutatakse müügitellimuse arve sisestamisel. Selle konto vastaskonto on arveldatud ühikute omahind. See konto tähistab teie P L-lause COGS-i&amp;. |
| Tulu (müügitellimuse tulu*) | 400100 | Tulumaterjalid | Tulu | Krediit | Nr | R   | Kasutatakse müügitellimuse arve sisestamisel. Selle konto vastaskonto on sisestusreeglites **Müügireskontro summakonto** (Kliendi saldo*·). |
| Komisjonitasu (Müük, Komisjonitasu*) | 602150 | Komisjonitasu | Kulu | Deebet | Nr | R  | Kasutatakse siis, kui komisjonitasu on lubatud ja arvutatud müügi jaoks ja sisestatud müügitellimuse arve protsessi käigus. Selle konto vastaskontoks on tasumisele kuuluv komisjonitasu. |
| Komisjonitasu vastaskonto (Müük, Komisjonitasu vastaskonto*) | 201110 | Maksmisele kuuluv komisjonitasu | Kohustus | Krediit | Jah | R | Kasutatakse siis, kui komisjonitasu on lubatud ja arvutatud müügi jaoks ja sisestatud müügitellimuse arve protsessi käigus. Selle konto vastaskonto on komisjonitasu kulu. |
| Edasilükatud tulu tarnimisel (Müük – saatelehe tulu*) | 401400 | Tekkepõhised müügid | Tulu | Krediit | Jah | P  | Kasutatakse siis, kui tarne viittulu on lubatud ja sisestatakse müügitellimuse saatelehe töötlemise ajal. Selle konto vastaskonto on edasilükatud tulu vastaskonto. Selle konto summad tühistatakse müügitellimuse arve sisestamisel automaatselt. |
| Edasilükatud tulu vastaskonto tarnimisel (Müük – saatelehe tulu vastaskonto)* | 130400 | Müügireskontro – arveldamata | Vara | Deebet | Jah | P  | Kasutatakse siis, kui tarne viittulu on lubatud ja müügitellimuse saatelehe töötlemise käigus postitab. Selle konto vastaskonto on tarnimisel edasilükatud tulu. Selle konto summad tühistatakse müügitellimuse arve sisestamisel automaatselt. |
| Edasilükatud käibemaks tarnimisel (müük, saatelehe maks*) | 250500 | Viitmaks | Kohustus | Krediit | Jah | P  | Kasutatakse siis, kui tarne viittulu on lubatud ja sisesta füüsiline käibemaks lubatud. Maksusumma sisestatakse müügitellimuse saatelehe töötlemise ajal. |

\* Selles tabelis sulgudes kuvatud väärtused **tähistavad** väärtust, mida kasutatakse kandekannete lehe väljal **Sisestustüüp**. Sisestustüüpi saate **vaadata** vahekaardi **Üldine** lehel Kande **kanded**.

## <a name="sales-category-posting"></a>Müügikategooria sisestamine

Kõigi kaupade, kaubagrupi või üksiku kauba lao sisestamise seadistamise alternatiivina saate seadistada kategooriaid ja kontrollida pearaamatu sisestamist müügikategooriate kaupa. Lisateavet kategooriahierarhia [seadistamise](/supply-chain/pim/tasks/create-hierarchy-product-classification.md)[ja toodetele kategooriate määramise kohta leiate teemast Tooteklassifikatsiooni hierarhia loomine ja Toote klassifitseerimine kategooriahierarhiate abil.](/supply-chain/pim/tasks/classify-product-category-hierarchies.md)

Pärast kategooriahierarhia loomiset peate määrama hierarhia ühele või mitmele tüübile. Müügitellimustes kategooriahierarhia kasutamiseks tuleb kategooria määrata müügikategooria hierarhia tüübile. Lisateabe saamiseks minge kategooriahierarhiate [kohta](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Loo tulu sisestamine müügikategooriate alusel

Müügikategoorial põhinevale müügitellimusele pearaamatu sisestuste määramiseks järgige neid samme:

1. Avage **Varude haldus** > **Seadistus** > **Sisestus** > **Sisestus**.
2. Valige vahekaart **Müük**.
3. Valige konfigureerimist vajava sisestamistüübi raadionupp (nt **Tulu**).
4. Valige suvand **Uus**.
5. **Väljal Kaubakood** valige **kategooria**.
6. Kasutage välja **Kategooriaseost**, et valida sisestusreegli kategooria.
7. **Valige väljal Konto** kood suvand Tabel **, Grupp** **või** **Kõik**. Näiteks sisestusreeglite rakendamiseks kõikidele klientidele valige suvand **Kõik**.
   - Kui valisite **6**. sammus tabeli, valige **sisestusreeglile** konkreetne hankijakood väljal **Konto** seos.
   - Kui valisite **6**. etapis grupi, **valige sisestusreegli** jaoks hankijagrupp väljal **Konto** seos.
   - Kui valisite **sammus** 6 väärtuse **Kõik, jääb** kontoseose väli tühjaks.

8. Valitud sisestustüübiga konkreetse maksugrupi seostamiseks valige **käibemaksugrupp**. Kui see väli jääb tühjaks, siis rakendub sisestamistüüp kõigile olemasolevatele maksugruppidele. Maksugruppidele määratud sisestamist rakendatakse ainult müügi ja ostu puhul tehtud kannetele.

9. Väljal Põhikonto **määrake** kontonumber, mille jaoks kontotüüp sisestada. Valige üks kontoplaanis olev konto number.
