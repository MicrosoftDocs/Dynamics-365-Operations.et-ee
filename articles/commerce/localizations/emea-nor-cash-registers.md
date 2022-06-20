---
title: Kassaaparaadi funktsioonid Norra jaoks
description: See artikkel annab ülevaate kassaraamatu funktsioonidest, mis on Norrale Microsoft Dynamics 365 Commerce saadaval ja annab juhised funktsioonide seadistamiseks.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 778a947f03866518219e9c0fa44660d66f19f53a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906695"
---
# <a name="cash-register-functionality-for-norway"></a>Kassaaparaadi funktsioonid Norra jaoks

[!include[banner](../includes/banner.md)]

See artikkel annab ülevaate kassaraamatu funktsioonidest, mis on Saadaval Norras Dynamics 365 Commerce. Samuti annab see juhised funktsioonide seadistamiseks. Funktsioon koosneb järgmistest osadest:

- Kõigi riikide või regioonide klientidele saadaolevad tavalise müügikoha (POS) funktsioonid. Näited hõlmavad valikut, mis laseb teil takistada kviitungi koopia prindimist rohkem kui üks kord.
- Norrale omased funktsioonid, nt müügikannete digitaalallkirjad.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Norra kassaregistri funktsioonide ülevaade

### <a name="common-pos-features"></a>Ühise kassa funktsioonid

Lisateavet müügikoha funktsioonide kohta, mis on saadaval klientidele kõikides riikides või regioonides, vt spikriressursse [Dynamics 365 Retail](../index.md).

Järgmisi müügikoha lokaliseerimise funktsioone, mis on eelnevalt rakendatud ja mis on tehtud klientidele kõikides riikides või regioonides kättesaadavaks, saab nüüd kasutada konkreetselt Norra puhul:

- **Prindib kviitungi tekstiväljad suurema fondisuuruses.** Kviitungi vormingu **kujundajas** saate kasutada fondi suuruse parameetrit, et määrata, kas kviitungi vormingus väljal tuleb kasutada suurt fondi suurust. (Suur fondi suurus on tavalisest fondi suurusest umbes kahekordne.) Näiteks saate seda parameetrit kasutada näidiku Kopeeri printimiseks kviitungi koopiale suurte märkidega.
- **Registreerige kviitungi koopiate printimine kassa auditi sündmustelogis.** Saate kasutada kassa funktsiooniprofiilis **parameetrit** Audit, et lubada kviitungite koopiate printimise ja teiste kassa auditi sündmuste registreerimist. Auditi sündmused registreeritakse kanali andmebaasis ja Peakontoris. Auditi sündmusi saate vaadata lehel **Auditi sündmused**.
- **Takistage kviitungi koopiat rohkem kui üks kord printimist.** Kui kassa **funktsiooniprofiili** auditi parameeter on lubatud, **kontrollib luba kviitungi koopiate** kassa loa printimine, kas kviitungite koopiaid saab printida. Samuti on olemas valik, mis laseb teil takistada kviitungi koopia prindimist rohkem kui üks kord.

Lisaks rakendati Norra jaoks järgmine müügikoha funktsioon, kuid see tehti kättesaadavaks klientidele kõikides riikides või regioonides:

- **Registreerige täiendavad sündmused kassa auditi sündmustelogisse.** Kui kassa **funktsiooniprofiilis** on auditi parameeter lubatud, registreeritakse kassa auditi sündmuste logis järgmised sündmused:

    - Hinnakontrollid
    - Maksu alistamine
    - Rea koguste parandused
    - Kannete tühjendamine kanali andmebaasist

### <a name="norway-specific-pos-features"></a>Norrale omased müügikoha funktsioonid

Järgmised Norrale omased müügikoha funktsioonid on lubatud, kui **kassa funktsiooniprofiili ISO-koodi** parameetri väärtuseks on seatud **Ei**.

#### <a name="digital-signing-of-sales-transactions"></a>Müügikannete digitaalne allkirjastamine

Iga müügikanne on digitaalselt allkirjastatud. Allkiri luuakse ja salvestatakse müügikoha kande töölehele samal ajal, kui kanne on lõpetatud. Allkiri on saadaval ka töölehel, mis eksporditakse auditeerimiseks.

Allkirjastatakse ainult sularahamüügi kanded. Siin on mõned näited kannetest, mis on allkirjastamisprotsessist välja jäetud:

- Ettemaksed (kliendikonto deposiit)
- Ettemaksed müügitellimuste jaoks (kliendi tellimuse deposiit)
- Kinkekaardi väljaandmine
- Mittemüügikanded (float-kirje, maksevahendi eemaldamine, muu)

Allkirjastatud andmed on tekstistring, mis koosneb järgmistest andmeväljadest. Andmeväljad eraldatakse semikoolonitega.

1. Sama kassa eelmine allkiri (esimese kande \[**puhul kasutatakse nulli 0**\] .)
2. Kande kuupäev
3. Kande aeg
4. Järjestikuse allkirjastatud kande number
5. Kandesumma, sh maks
6. Kandesumma ilma maksuta

Digitaalsel allkirjastamise protsessil kasutatakse RSA 1024-bitiset võtit, mis omab SHA-1 RSA-SHA1-1024. Commerce Scale Uniti installitud serti kasutatakse allkirjastamiseks. Serdi kordumatu ID (tunnistus) registreeritakse koos allkirjaga.

Allkiri talletatakse koos kandeandmetega kaupluse andmebaasis ja peakontori (HQ) andmebaasis. Kande allkirja ja selle loomiseks kasutatud kande andmete saate vaadata **kaupluse** **kannete lehe finantskannete kiirkaardil.**

#### <a name="receipts"></a>Kviitungid

Norra sissetulekud võivad hõlmata täiendavat teavet, mis rakendati kohandatud väljade abil:

- **Kviitungi** pealkiri – kviitungi vormingu kavandile saate lisada välja, et tuvastada kviitungi tüüp. Näiteks sisaldab müügikviitung teksti "Müügi sissetulek".
- **Allkirjastatud kande seerianumber** – allkirjastatud kande järjenumber võib ilmuda kviitungil, et seostada prinditud kviitung andmebaasis digitaalallkirjaga.
- **Sissetuleku kogusummad** – kohandatud väljad sissetuleku kogusummade jaoks välistavad kande kogusummadest müügiväliseid summasid. Mittemüügisummad sisaldavad summasid järgmistele toimingutele:

    - Ettemaksed (kliendikonto deposiit)
    - Ettemaksed müügitellimuste jaoks (kliendi tellimuse deposiit)
    - Kinkekaardi väljaandmine
    - Kinkekaardile vahendite lisamine

#### <a name="x-and-z-reports"></a>X- ja Z-aruanded

X- ja Z-aruannetes kaasatud teave põhineb Norra nõuetel. Näiteks hõlmab sularaha **müügi kogusumma ainult sularahakannete** summasid ning välistada kinkekaarditoimingute ja ettemaksete väljaminek. Sularahamüükide kogusumma loetletakse ka kaubagrupi ja makseviisi järgi. Lisaks säilitatakse ja prinditakse **kumulatiivsed müügi** **kogusummad** ja tagastuste kogusummad.

#### <a name="saf-t-cash-register-audit-file"></a>SAF-T kassaregistri auditifail

Saate eksportida müügikoha kande töölehe eelmääratletud standardse auditifaili - maksu (SAF-T) kassaregistri vormingus. Auditifail sisaldab teavet organisatsiooni kohta, asjakohaseid koondandmeid (nt kaubagruppe, kaupu ja maksukoode), sularaha müügikande andmeid koos nende kannete allkirjadega, müügiväliste sündmuste andmeid ja lõppkuupäeva aruande andmeid.

Auditifaili saab eksportida järgmiste stsenaariumide jaoks:

- Kaupluse kohta
- Kõik kauplused
- Terminali kohta
- Kõik terminalid

Te saate saata aruande ka ühest juriidilisest isikust teise juriidilise isiku nimel. Sellisel juhul peate käitama ekspordi tootmisüksusest ja määrama aruande saatjaks juriidilise isiku.

SAF-T kassaregistri vorming rakendatakse Peakontoris elektroonilise aruandluse [abil](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Norra äri seadistamine

Selles jaotises kirjeldatakse Norrale omased ja soovitatavad sätteid. Lisateavet vt spikri ressurssidest [Dynamics 365 Retail](../index.md).

Norrale omase funktsionaalsuse kasutamiseks peate lõpule täitma need ülesanded:

- Seadke väli **Riik/regioon** **väärtusele NOR** (Norra) juriidilise isiku esmases aadressis.
- **Seadke ISO-koodi** väljale **NO** (Norra) iga Norras paikneva kaupluse kassa funktsiooniprofiilis.

Peate määrama ka Järgmised sätted Norra jaoks.

### <a name="set-up-the-legal-entity"></a>Juriidilise isiku häälestamine

Veenduge, et juriidilise isiku nimi on määratud. See nimi prinditakse X- ja Z-aruannetele.

Lisaks määrake pangakonto **teabe kiirkaardil** väljal **Protsessikood** organisatsiooni kood.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Saate häälestada km-i Norra nõuete kohta.


Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate häälestama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksude seadistamis- ja kasutus kohta vt käibemaksu [ülevaatest](../../finance/general-ledger/indirect-taxes-overview.md).

Peate määrama ka käibemaksugrupid ja lubama Suvandi **Hinnad sisaldavad** käibemaksu valikut kauplustele, mis asuvad Norras.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide häälestus

Peate lubama auditi ja seadistama kviitungite nummerdamise.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Kassa lubade gruppide ja kaupluse töötajate individuaalsete õiguste sätete värskendamine

Seadke luba **kviitungi koopia printimise** õigusele sobiv väärtus.

- **Luba alati** – operaator saab mitu korda kviitungi koopiat printida.
- **Lubatakse ainult** üks kord – operaator saab kviitungi koopiat ainult ühe korra printida.
- **Lubatakse ainult üks kord ja ainult siis, kui HQ DB** on saadaval – operaator saab printida kviitungi koopia ainult üks kord ning ainult siis, kui HQ Commerce Data Exchange andmebaas on saadaval järgmise kaudu: Real-time Service, nii et süsteem saab kontrollida, et kviitungi koopiaid pole eelnevalt üheski kaupluses prinditud.
- **Mitte** kunagi – operaator ei saa kviitungi koopiat printida.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Lisage keele **teksti lehel** kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange tähele **, et tabelis kuvatavad** keele **-,** **teksti-ID**- ja tekstiväärtused on vaid näited. Saate neid vastavalt oma nõuetele muuta.

| Keele ID | Tekst                   | Teksti ID |
|-------------|------------------------|---------|
| et       | Kviitungi pealkiri          | 900011  |
| et       | On kinkekaart           | 900012  |
| et       | Kokku (müük)          | 900013  |
| et       | Kogumaks (müük)      | 900014  |
| et       | Kokku koos maksuga (müük) | 900015  |
| et       | Maksusumma (müük)     | 900016  |
| et       | Sularahakande ID    | 900017  |

**Lisage kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange tähele **, et pealdise teksti ID** väärtused peavad vastama **teksti ID** väärtustele, mille määrate **keele teksti** lehel.

| Nimi                            | Tüüp    | Pealdise teksti ID |
|---------------------------------|---------|-----------------|
| Kviitungi kviitung                    | Sissetulek | 900011          |
| IsGiftCard                      | Sissetulek | 900012          |
| SalesTotalExt                   | Sissetulek | 900013          |
| TaxTotalExt                     | Sissetulek | 900014          |
| KokkuWithTaxExt                 | Sissetulek | 900015          |
| AmountPerTaxExt                 | Sissetulek | 900016          |
| KassatransactionSequentialNumber | Sissetulek | 900017          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud ülaltoodud tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke kõigi nõutud kviitungi vormingute puhul välja **Prindikäitumine väärtus** väärtuseks **Prindi alati** kviitungi vormingu jaoks.

Lisage kviitungi vormingu kujundajasse järgmised kohandatud väljad asjakohastele kviitungi jaotistele. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

1. Päis:

    - **Kviitungi** pealkiri – see väli tuvastab kviitungi tüübi.
    - **Sularahakande ID** – see väli prindib allkirjastatud sularahakande seerianumbri.

2. Read:

    - **On kinkekaart** – see väli märgib kviitungi rea seoses väljasta kinkekaardiga või lisa kinkekaardi toiminguga.

3. Jalus:

    - **Kokku (müük)** – see väli prindib sissetuleku sularahamüügi kogusumma. Summa ei sisalda maksu. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
    - **Maksu kogusumma (müük)** – see väli prindib sissetuleku käibemaksu kogusumma sularahamüügi puhul. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
    - **Kogusumma koos maksuga (müük)** – see väli prindib sissetuleku sularahamüügi kogusumma. Summa sisaldab maksu. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
    - **Maksusumma (müük)** – selle välja abil prinditakse iga maksukoodi kohta kassakäibmaksu summa. Ettemaksed ja kinkekaarditoimingud on välja jäetud.

Lisateavet kviitungi vormingutega töötades vt Kviitungi vormingute [häälestamine ja kujundamine](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>SAF-T kassaraamatu ekspordivormingu konfigureerimine

SAF-T kassaregistri konfiguratsioon on allalaadimiseks saadaval elutsükli Microsoft Dynamics teenustest (LCS). Lisateavet vt impordi elektrooniliste aruandluskonfiguratsioonide [kohta](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Peate alla laadima järgmised konfiguratsioonid:

- **Jaemüügikanali andmed.version.1** – andmemudeli konfiguratsioon.
- **DMM jaemüügikanali andmed.version.1.14** – andmemudeli vastendamise konfiguratsioon.
- **EI SAF T Cash Register.version.1.20** – vormingu konfiguratsioon.

Pärast **konfiguratsioonide** **·** **importimist äriparameetrite lehel, vahekaardil Elektroonilised dokumendid, valige SAF-T** sularaharegistri ekspordivormingu väljal imporditud vormingu konfiguratsiooni nimi.

Samuti peate vastendama nõutavad koondandmed eelmääratletud SAF-T standardkoodidega. Lisateavet vt Norra maksuhalduse esitatud SAF-T kassaraamatu dokumentatsioonist. Vastenduse loomiseks peate määrama uue **SAF-T kassaraamatu koodi** välja järgmistel lehekülgedel:

- Kaubagrupid
- Makseviisid
- Käibemaksukoodid

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

Norrale omase funktsionaalsuse lubamiseks peate konfigureerima kanali komponendid. Lisateavet vt juurutamise [juhistest](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
