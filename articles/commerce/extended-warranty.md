---
title: Laiendatud garantiide loomine ja konfigureerimine
description: See teema hõlmab laiendatud garantiisid ning kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua ja konfigureerida.
author: sijoshi
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 772dc1fdda7c34448ffa946237f717e657df6d83d8fda9336049e79d19ed1af0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745376"
---
# <a name="create-and-configure-extended-warranties"></a>Põhjalikumate garantiide loomine ja konfigureerimine

[!include [banner](includes/banner.md)]

See teema hõlmab laiendatud garantiisid ning kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua ja konfigureerida.

## <a name="overview"></a>Ülevaade

Kliendid valivad toodete (eriti kallimate tarbekaupade, nagu telefonide ja arvutite) ostmisel üha enam laiendatud toe ja teenused. Pakkudes ostmiseks laiendatud garantiisid, saavad jaemüüjad aidata muuta kliente lojaalsemaks. Laiendatud garantiide kaudu antakse klientidele teada, kelle poole nad saavad hoolduse ja toe jaoks pöörduda. Seetõttu võivad nad olla kindlad, et nende probleeme käsitletakse tõhusalt.

Laiendatud garantiisid saab müüa klientidele jaemüügikanalis algse toote ostmise ajal. Neid saab müüa ka piiratud aja jooksul pärast algset ostu.

### <a name="warranty-item-setup"></a>Kaubagarantii seadistamine

Dynamics 365 Commerce pakub võimalust kaubagarantii loomiseks ja sellele atribuutide määramiseks. Need atribuudid hõlmavad seost toote ja kaubagarantii vahel, garantii hinda ning garantii kestust. Kui kaubagarantii on konfigureeritud ja organisatsiooniüksusele kättesaadavaks tehtud, saab jaemüüja garantiisid müüa modernses kassas (MPOS), e-poodides ning teistes jaemüügikanalites.

### <a name="warranty-item-sales"></a>Kaubagarantii müümine

Laiendatud garantiisid müüakse jaemüügikanalis algse toote ostmise ajal. Neid saab müüa ka piiratud aja jooksul pärast algset ostu.

Kui seotud toode lisatakse kliendi ostukorvi, pakutakse müügiesindajatele kassas (POS) laiendatud garantii lisamise võimalust. Seetõttu pakutakse müügiesindajatele müügiprotsessi osana üles- ja ristmüügi võimalust.

Kliendid saavad naasta ka hiljem ja osta laiendatud garantii varem ostetud toote jaoks. Sellisel juhul saab müügiesindaja otsida algse kande üles ja müüa kliendile seotud laiendatud kaubagarantii.

### <a name="warranty-terminology"></a>Garantii terminoloogia

Järgmises tabelis on toodud mõned garantiiga seotud terminid.

| Mõiste | Kirjeldus |
|------------------------------|--------------|
| Laiendatud garantii / garantii | *Laiendatud garantii* viitab teenuseleppele või -lepingule, mis annab klientidele pikendatud garantii. Laiendatud garantii sisaldab kaupade asendamise või parandamise lisateenust laiendatud garantii kehtivusperioodi ajal. |
| Tootjagarantii | *Tootjagarantii* (nimetatakse sageli *piiratud garantiiks*) on garantii, mille kliendid saavad toote ostmisel. Järgmisena on toodud mõned tootjagarantii omadused.<ul><li>Garantii hind sisaldub toote hinnas. Kliendid ei pea tootjagarantii eest lisa maksma.</li><li>Toote kategooriast sõltuvalt kehtib tootjagarantii tavaliselt 30 päeva, kuus kuud või üks aasta. (Suurema osa tarbeelektroonika puhul kehtib garantii üks aasta).</li><li>Garantii hõlmab kõiki defekte, mille on põhjustanud mehaaniline või elektriline rike. Kaitse on piiratud ja see ei hõlma ostetud toote juhuslikke kahjustusi. Kliendid, kes soovivad kaitsta ostetud tooteid igapäevaste kahjustuste eest, peaksid ostma laiendatud garantii. Laiendatud garantiid kestavad toote kategooriast sõltuvalt kaks kuni kümme aastat. Nad hõlmavad ka paremat kaitset ja igapäevaseid äpardusi, nagu mahakukkumist, veekahjustust ja määrdumist.</li></ul> |
| Garantiikaup | *Kaubagarantii* on laiendatud garantii, mida müüakse garantiikõlbliku kauba jaoks. Näitena võib tuua kaheaastase õnnetuskaitseplaani sülearvutite jaoks. |
| Garantiikõlblik kaup | *Garantiikõlblik kaup* on seerianumbriga toode, millele müüakse garantiid. Näiteks on garantiikõlblik kaup sülearvuti, millele müüakse kahe- ja kolmeaastaseid laiendatud garantiisid. |
| Garantiigrupp | *Garantiigrupp* on seos kaubagarantiide ja garantiikõlblike kaupade vahel. Kassa kasutab garantiigruppe, et määrata, milliseid kaubagarantiisid peaks müügiesindajatele lisamiseks pakkuma, kui kliendi ostukorvi lisatakse garantiikõlblik kaup. |
| Garantiipoliitika | *Garantiipoliitika* on üksus, mis luuakse Commerce'is garantiipoliitika müümisel. Garantiipoliitika sisaldab teavet, nagu ostetud kaubagarantii algus- ja lõppkuupäev, tingimused ning garantiikõlbliku toote seerianumber. Garantiipoliitika numbreid saab klientidega jagada, et neil oleks viide ostetud laiendatud garantiile. |

## <a name="create-a-warranty-item"></a>Kaubagarantii loomine

Commerce'is kaubagarantii loomiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Tooted**.
1. Valige uue kaubagarantii loomiseks **Uus**.
1. Valige dialoogiboksi **Uus toode** väljal **Toote tüüp** väärtus **Teenus**.
1. Valige väljal **Toote alamtüüp** väärtus **Toode**.
1. Valige väljal **Toote teenuse tüüp** väärtus **Teenus**.
1. Sisestage toote nimi väljale **Toote nimi**.
1. Valige välja **Jaemüügi kategooria** rippdialoogiboksist väärtus ja klõpsake seejärel **OK**.
1. Sisestage toote number väljale **Toote number**.
1. Valige nupp **OK**.
1. Täitke lehe **Toote üksikasjad** kiirkaardil **Garantii** väljad **Ajaühik** ja **Ajavahemik**.

    | Välja nimi | Väärtus | Kirjeldus |
    |------------|-------|-------------|
    | Ajaühik | **Päev(a)**, **Nädal(at)**, **Kuu(d)** või **Aasta(t)** | See väli määratleb ajaühiku, mida garantii puhul kasutatakse. |
    | Ajavahemik | Positiivne täisarv | See väli määratleb garantii kestuse valitud ajaühikus. |

    Näiteks kaheaastase garantii puhul seadke välja **Ajaühik** väärtuseks **Aasta(t)** ja välja **Ajavahemik** väärtuseks **2**. Teise võimalusena võite seada välja **Ajaühik** väärtuseks **Kuu(d)** ja välja **Ajavahemik** väärtuseks **24**, nagu on näha järgmisel joonisel.

    ![Toote üksikasjade leht kaubagarantii jaoks.](./media/ew-time-properties.png)

1. Kaubagarantii salvestamiseks valige **Salvesta**.
1. Tehke kaubagarantii ettevõttele kättesaadavaks, et seda saaks müüa. Lisateavet leiate teemast [Jaemüügitoodete häälestamine](set-up-retail-products.md).
1. Täitke lehe **Väljastatud toote üksikasjad** kiirkaardil **Garantii** väljad **Hinnavahemiku alus**, **Alampiir** ja **Ülempiir**.

    | Välja nimi | Väärtus | Kirjeldus |
    |------------|-------|-------------|
    | Hinnavahemiku alus | **Puudub**, **Baashind** või **Müügihind** | <ul><li>**Puudub** – hinnavahemiku väärtuseid **Alampiir** ja **Ülempiir** ei rakendata.</li><li>**Baashind** – kõnealune garantii kehtib juhul, kui garantiikõlbliku kauba baashind (see tähendab allahindlusteta hind) jääb garantiikõlbliku kauba hinna põhjal siin määratletud väärtuste **Alampiir** ja **Ülempiir** vahele.</li><li>**Müügihind** – seda väärtust kasutatakse hiljem.</li></ul> |
    | Alampiir, Ülempiir | Positiivne täisarv | Need väljad määratlevad kauba hinna alam- ja ülempiiri ning selle, kuidas asjaomane kaubagarantii garantiikõlbliku kauba puhul rakendub. Piirid võivad põhineda garantiikõlbliku kauba baashinnal (tuntud ka kui tootja soovitatud jaemüügihind \[MSRP\]). Kui välja **Hinnavahemiku alus** väärtuseks on seatud **Baashind**, näidatakse kassas kaubagarantii lisamise võimalust ainult sellise garantiikõlbliku kauba (toote) puhul, mille baashind jääb väärtuste **Alampiir** ja **Ülempiir** vahele. |

    Näiteks on järgmisel joonisel seatud välja **Hinnavahemiku alus** väärtuseks **Baashind**, välja **Alampiir** väärtuseks 500 $ ja välja **Ülempiir** väärtuseks 1000 $.
    
    ![Väljastatud toote üksikasjade leht kaubagarantii jaoks.](./media/ew-release-product-details.png)

1. Määrake kaubagarantii kanalile, kus seda müüakse. Lisateabe saamiseks vt [Sortimentide häälestamine](set-up-assortments.md).

### <a name="example"></a>Näide

Garantiikõlbliku sülearvuti (toote) baashind on 999 $ ja sülearvuti kaubagarantiisid on kaks.

- Garantii\_1 alampiir on 500 $ ja ülempiir 1000 $ ning välja **Hinnavahemiku alus** väärtuseks on seatud **Baashind**.
- Garantii\_2 alampiir on 1001 $ ja ülempiir 2000 $ ning välja **Hinnavahemiku alus** väärtuseks on seatud **Baashind**.

Kui garantiikõlblik sülearvuti lisatakse kliendi ostukorvi, kuvatakse kassas Garantii\_1 lisamise viip, kuna sülearvuti hind jääb Garantii\_1 alam- ja ülempiiri vahele.

> [!NOTE]
> Kui soovite selle näite puhul, et viipa kuvataks garantiikõlbliku kauba hinda arvestamata nii Garantii\_1 kui ka Garantii\_2 puhul, seadke välja **Hinnavahemiku alus** väärtuseks **Puudub**.

## <a name="configure-channel-specific-settings"></a>Kanalipõhiste sätete konfigureerimine

Kanalipõhised sätted võimaldavad teil määrata, kas garantiikõlbliku kauba lisamisel kliendi ostukorvi kuvatakse kassas kaubagarantii lisamise viip.

Commerce'is kanalipõhiste sätete konfigureerimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Garantii \> Garantii sätted**.
1. Valige vahekaardil **Kanalipõhine** oma kanali veerus **Garantii viip** üks järgmistest võimalustest.

    - Märkige see ruut, kui garantiikõlbliku kauba lisamisel ostukorvi peaks kassas ilmuma kaubagarantii viip.
    - Jätke ruut tühjaks, kui garantiikõlbliku kauba lisamisel ostukorvi ei peaks kassas ilmuma kaubagarantii viip.

1. Andmete kanaliga sünkroonimiseks käivitage töö **1070**.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Numbriseeria konfigureerimine garantiipoliitikate jaoks

Igal garantiipoliitikal on kordumatu garantiipoliitika number, mille loob numbriseeria. Numbriseeriate kohta leiate lisateavet teemast [Numbriseeriate ülevaade](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Commerce'is garantiipoliitika jaoks numbriseeria konfigureerimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Garantii \> Garantii sätted**.
1. Valige või sisestage väärtus väljale **Numbriseeria kood**, mis asub vahekaardil **Numbriseeriad** **Garantiipoliitika** viite real.

## <a name="set-up-a-warranty-group"></a>Garantiigrupi seadistamine

Garantiigrupp on seos kaubagarantiide ja garantiikõlblike kaupade vahel. Kassa kasutab garantiigruppe, et määrata, milliseid kaubagarantiisid peaks müügiesindajatele lisamiseks pakkuma, kui kliendi ostukorvi lisatakse garantiikõlblik kaup.

Commerce'is garantiigrupi seadistamiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Garantii \> Garantiigrupid**.
1. Valige uue garantiigrupi loomiseks **Uus**.
1. Sisestage väljale **Nimi** uue grupi nimi.
1. Sisestage grupi kirjeldus kiirkaardi **Üldine** väljale **Kirjeldus**.
1. Valige kiirkaardil **Garantiitooted** suvand **Lisa rida**, et lisada kaubagarantii.
1. Sisestage väljale **Kuvamisjärjestus** kassas garantiigrupi järjestust määrav number. Kassa garantiiviibas kuvatakse kaubagarantiid tõusvas järjestuses.
1. Valige kiirkaardil **Garantiikõlblikud tooted** suvand **Lisa rida**, et lisada garantiikõlblikud tooted.
1. Kui kaubagarantii rakendub kogu garantiikõlblike kaupade (toodete) kategooria puhul, valige see kategooria väljal **Kategooria**. Kui kaubagarantii rakendub konkreetse garantiikõlbliku kauba (toote) puhul, valige see toode väljal **Toode**.
1. Valige kiirkaardil **Rakendatavad kanalid** suvand **Lisa rida**, et lisada kanal, kus soovite kaubagarantiid müüa.
1. Konfiguratsiooni salvestamiseks valige **Salvesta**.
1. Garantiigrupi avaldamiseks valige suvand **Avalda**.
1. Et sünkroonida andmed kanaliga, käivitage töö **1040**.

## <a name="sell-warranty-items-at-the-pos"></a>Kassas kaubagarantiide müümine

Müügiesindajad saavad kliendiostude protsessi ajal kaubagarantiisid müüa kahe kassatoimingu abil.

- **Lisa garantii** – see toiming käivitab viiba, millel kuvatakse ostukorvis valitud garantiikõlbliku kauba puhul rakenduvad garantiid.
- **Olemasolevale kandele garantii lisamine** – see toiming võimaldab müügiesindajatel müüa garantiisid juba müüdud garantiikõlblike kaupade jaoks. Müügiesindajad saavad kande kviitunginumbri sisestamise kaudu otsida üles garantiikõlbliku kauba algse kande.

Järgmisel joonisel on näha kassaterminali lehe näide, millel on kujutatud praegusele garantiikõlbliku kauba ostule kaubagarantii lisamise viip.

![Praegusele ostule kaubagarantii lisamise viiba näide.](./media/ew-sell-warranty.png)

Järgmisel joonisel on näide funktsioonist, mille kaudu saab lisada varem müüdud garantiikõlblikule kaubale kaubagarantii.

![Varem müüdud garantiikõlblikule kaubale kaubagarantii lisamise funktsiooni näide.](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Garantiikannete töötlemine

Kui garantiisid müüakse sularahas, saavad Commerce'i kasutajad pärast kannete sisestamist Commerce'i peakontorisse käitada töö **Garantiikannete töötlemine**, et töödelda garantiikandeid ja luua garantiipoliitikaid.

Commerce'i peakontoris garantiikannete töötlemiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Garantii \> Garantiikannete töötlemine**.
1. Valige väärtus dialoogiboksi **Organisatsioonisõlmede valimine** väljal **Organisatsioonihierarhia**.
1. Valige loendist **Saadaolevad organisatsioonisõlmed** kas üks kauplus või sõlm, kui soovite kaupluste grupi jaoks pakett-töö luua.
1. Valige parem noolenupp, et lisada oma valik loendisse **Valitud organisatsioonisõlmed**.
1. Valige vahekaart **Käivita taustal**.
1. Seadke suvandi **Pakktöötlus** väärtuseks **Jah** ning valige seejärel **Kordumine**.
1. Valige või sisestage kordumise alguskuupäev dialoogiboksi **Kordumise määratlemine** väljale **Alguskuupäev**.
1. Valige või sisestage kordumise algusaeg väljale **Algusaeg**.
1. Järgige üht neist sammudest.

    - Valige suvand **Lõppkuupäev puudub**, kui töö peaks alati korduma.
    - Valige suvand **Lõpeta pärast**, kui töö käitamine peaks lõppema pärast konkreetset käitamiste arvu. Selle suvandi valimisel sisestage käitamiste arv.
    - Valige suvand **Lõpetamiskuupäev**, kui töö käitamine peaks lõppema kindlal kuupäeval. Selle suvandi valimisel valige või sisestage kuupäev.

1. Valige nupp **OK**.
1. Valige nupp **OK**.

## <a name="warranty-policies"></a>Garantiipoliitikad

Laiendatud garantii müümisel luuakse automaatselt garantiipoliitika üksus. Garantiipoliitika numbreid saab klientidega jagada, et neil oleks viide ostetud kaubagarantiile. Garantiipoliitika atribuudid sisaldavad garantii jõustumis- ja aegumiskuupäeva, tingimusi ning selle garantiikõlbliku kauba seerianumbrit, mille juurde garantii müüdi.

> [!NOTE]
> Garantiipoliitika atribuudid luuakse automaatselt garantiipoliitika üksuste loomisel. Praegu ei saa neid käsitsi konfigureerida ega redigeerida.

Järgmises tabelis on toodud garantiipoliitika atribuudid ja nende väärtused. Commerce'i peakontoris on andmebaasi tabeli nimi WARRANTYPOLICY.

| Atribuudi nimi | Väärtus | Kirjeldus |
|---------------|-------|-------------|
| PolicyNumber | Tähemärkide string (kuni 20 tähemärki) | Garantiipoliitika number |
| WarrantiedItemId | Tähemärkide string (kuni 20 tähemärki) | Garantiikõlbliku kauba ID |
| WarrantiedInventoryLotId | Tähemärkide string (kuni 20 tähemärki) | Garantiikõlbliku kauba laopartii ID |
| WarrantiedSerialNumber | Tähemärkide string (kuni 20 tähemärki) | Garantiikõlbliku kauba seerianumber |
| WarrantiedFulfilledDate | Kuupäev | Garantiikõlbliku kauba täitmise kuupäev |
| WarrantyItemId | Tähemärkide string (kuni 20 tähemärki) | Kaubagarantii ID |
| WarrantyInventoryLotId | Tähemärkide string (kuni 20 tähemärki) | Kaubagarantii laopartii ID |
| WarrantySalesDate | Kuupäev | Kaubagarantii müügikuupäev |
| WarrantyEffectiveDate | Kuupäev | Garantiipoliitika jõustumiskuupäev |
| WarrantyExpirationDate | Kuupäev | Garantiipoliitika aegumiskuupäev |
| CustAccount | Tähemärkide string (kuni 20 tähemärki) | Kliendikonto number |
| Olek | **Loodud**, **Tühistatud**, **Jõustunud** või **Aegunud** | Garantiipoliitika olek |
| Märkmed | Tähemärkide string (kuni 255 tähemärki) | Märkused garantiipoliitika kohta, näiteks tingimused |

## <a name="frequently-asked-questions-faq"></a>Korduma kippuvad küsimused (KKK)

**Miks ei kuvata kassas garantiiviipa?**

Veenduge, et kaubagarantii oleks kanalile määratud. Veenduge ka, et garantiigrupp oleks konfigureeritud nii, et see sisaldab kõnealust kanalit.

**Kui ma üritan olemasolevale kandele garantiid lisada ja sisestan klienditellimuse kviitunginumbri, miks ei näe ma ühtegi kanderea kaupa?**

Kviitungid on leitavad vaid siis, kui kviitungite üleslaadimiseks Commerce'i peakontorisse on käivitatud üleslaadimistöö. Üleslaadimistöö käivitamiseks avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**, valige töö **P-0001** ning seejärel käsk **Käivita kohe**.

**Miks rakendatakse garantiifunktsiooni ainult seerianumbriga toodete puhul?**

Garantii on teenus, mis on mõeldud kindla kordumatu toote jaoks. Rakenduses Dynamics 365 on toode kordumatult tuvastatav ainult seerianumbri abil.

## <a name="additional-resources"></a>Lisaressursid

[Jaemüügitoodete häälestamine](set-up-retail-products.md)

[Sortimentide häälestamine](set-up-assortments.md)

[Numbriseeriate ülevaade](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]