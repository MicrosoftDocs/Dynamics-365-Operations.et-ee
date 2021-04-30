---
title: Hübriidreaalsusjuhendite kasutamise võimaldamine tootmistöötajatele
description: Selles teemas selgitatakse, kuidas integreerida rakenduse Microsoft Dynamics 365 Supply Chain Management tootmishalduse moodul rakendusega Dynamics 365 Guides.
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 15595c46f9d6ff91f6fd618859e9f059ae88bd78
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910085"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Hübriidreaalsusjuhendite kasutamise võimaldamine tootmistöötajatele

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tootmistöötajad saavad kasu asjakohastest juhistest, mida pakutakse nende töö kontekstis õigel ajal. *Juhised* rakenduvad mitmes töövaldkonnas, sealhulgas koostamine, hooldus, toimingud, sertifitseerimine ja ohutus. Kõigi nende põhiärifunktsioonide puhul võivad aktiivsed koolitusjuhised aidata töötajatel rohkem ja paremini töötada.

## <a name="introduction"></a>Sissejuhatus

Juhiseid saate pakkuda eri viisidel. Üks kohe kasutamiseks valmis tõhus süsteem kasutab rakendust [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Rakendus Dynamics 365 Guides võib aidata teie töötajaid praktilise õppe kaudu. Saate määratleda standarditud protsesse koos etapiviisiliste juhistega, mis juhatavad teie töötajaid vajalike tööriistade ja osade juurde ning näitavad neile, kuidas tööriistu reaalses tööolukorras kasutada.

Saate lisada juhendeid tootmise juhtimise eri aspektidele, sealhulgas järgmistele.

- [Ressursid](#resources)
- [Ressursigrupid](#resource-groups)
- [Väljastatud tooted](#released-products)
- [Valemid](#formulas)
- [Valemiversioonid](#formula-versions)
- [Kooslused (BOM-id)](#bom)
- [Koosluse versioonid](#bom-versions)
- [Protsessid](#routes)
- [Protsessi versioonid](#route-versions)
- [Protsessi toiminguseosed](#route-operation-relations)

> [!NOTE]
> Saate lisada rakenduse Guides ka varahaldusesse. Selle võimaluse kohta leiate lisateavet teemast [Rakenduse Dynamics 365 Supply Chain Management (varahaldus) integreerimine rakendusega Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

Kui esmatasanditöötaja valib rakenduse Supply Chain Management kaudu tootmisjaoskonnas töö, näeb ta töö kaardil [asjaomaseid juhendeid](#logic). Kui töötaja valib kindla juhendi, kuvatakse ekraanil selle juhendi QR-kood. Seejärel kasutab töötaja QR-koodi skannimiseks oma HoloLensi, mis käivitab rakenduse Guides ja kuvab vajalikud juhised.

Järgmistes alajaotistes on kirjeldatud mõnda valitud stsenaariumi, mille puhul võivad kõikide valdkondade ettevõtted ise näha, kui kasulik on rakenduse Guides kasutamine tootmisjuhiste pakkumiseks.

### <a name="assembly"></a>Assembler

![Rakenduse Guides kasutamine koostamisülesannetes](media/instruction-guides-hero-assembly.png "Rakenduse Guides kasutamine hooldusülesannetes")

Koostamistoimingute juhised näitavad töötajatele vajalikke tööriistu ja osasid ning kuidas neid reaalses tööolukorras kasutada.

Tootmisjuhid saavad luua ja määrata juhendeid näiteks [tootmisprotsesside](routes-operations.md), [toiminguseoste](routes-operations.md#operation-relations) või [koosluste](bill-of-material-bom.md) jaoks. Töötajad leiavad asjakohased juhised tootmisjaoskonnas asjaomase toimingu kallal töötades.

### <a name="service"></a>Teenus

![Rakenduse Guides kasutamine hooldusülesannetes](media/instruction-guides-hero-service.png "Rakenduse Guides kasutamine hooldusülesannetes")

Varustage tehnikud töökohas juhistega, et lisakülastusi poleks vaja plaanida.

Hooldusjuhid saavad määrata juhendeid näiteks konkreetsetele [toodetele](../../commerce/product.md), mis pakuvad kvaliteedi hindamise toimingute üksikasju.

### <a name="quality"></a>Kvaliteet

![Rakenduse Guides kasutamine kvaliteedi tagamise ülesannetes](media/instruction-guides-hero-quality.png "Rakenduse Guides kasutamine kvaliteedi tagamise ülesannetes")

Looge uusi protsesse ja tagage suurem järjepidevus, muutes töötajate teadmised korduvalt kasutatavaks tööriistaks.

Kvaliteedi tagamise juhid saavad määrata juhendeid näiteks konkreetsetele [toodetele](../../commerce/product.md), mis pakuvad kvaliteedi hindamise toimingute üksikasju.

### <a name="certifications"></a>Serdid

![Rakenduse Guides kasutamine sertifitseerimisega seotud ülesannetes](media/instruction-guides-hero-certification.png "Rakenduse Guides kasutamine sertifitseerimisega seotud ülesannetes")

Veenduge, et iga töötaja vastaks standarditele, tehes kiiresti kindlaks, kes vajab abi ja kus.

### <a name="safety"></a>Ohutus

![Rakenduse Guides kasutamine tööohutusjuhistes](media/instruction-guides-hero-safety.png "Rakenduse Guides kasutamine tööohutusjuhistes")

Looge juhised, mis näitavad ohtlikke olukordi virtuaalselt, enne kui neid päriselt tehakse. Hübriidreaalsust kasutades saavad töötajad kogeda ohtlikke olukordi virtuaalselt.

Tootmisjuhid võivad pakkuda spetsiaalseid käitlemisjuhiseid ohtlike materjalide käitlemiseks või delikaatset käitlemist vajavate olukordade jaoks, määrates juhised [toodetele](../../commerce/product.md), [protsessidele](routes-operations.md) ja [toimingutele](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Juhiste ja rakenduse Guides kasutamise alustamine

Tootmisprotsessides juhiste lubamiseks pakub rakendus Supply Chain Management integratsiooni rakendusega Dynamics 365 Guides, mis on kasutamiseks valmis. Hübriidreaalsusjuhendite loomiseks, haldamiseks ja määramiseks tootmisvaradele ning tööle on vajalik litsentsitud ja installitud rakenduse Guides eksemplar.

### <a name="prerequisites"></a>Eeltingimused

Selle funktsiooni kasutamiseks peab teie süsteem sisaldama järgmist.

- Dynamics 365 Supply Chain Managementi versioon 10.0.15 või uuem
- [Topeltkirjutamine](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md) Supply Chain Managementi rakenduste jaoks.
- [Rakenduse Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versioon 400.0.1.48 või uuem

### <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Et muuta funktsioon oma süsteemis kättesaadavaks, peate lubama selle konfiguratsioonivõtmed. Peate seda tegema ainult üks kord. Selleks peab administraator tegema järgmist.

1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Laiendage jaotis **Hübriidreaalsus** ja valige seejärel märkeruut **Hübriidreaalsusjuhend**.
1. Laiendage jaotis **Tootmishaldus** ja valige seejärel märkeruut **Tootmisjuhised**.
1. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Rakenduse Guides kujunduse konfigureerimine tootmisjaoskonnas

Et konfigureerida, kuidas rakendust Guides tootmisjaoskonnas kuvatakse, avage **Hübriidreaalsus \> Dynamics 365 Guides \> Rakenduse Guides integratsiooni konfigureerimine**.

![Rakenduse Guides integratsiooni konfigureerimine tootmise jaoks](media/instruction-guides-configure-integration.png "Rakenduse Guides integratsiooni konfigureerimine tootmise jaoks")

Seadistage järgmised väljad.

- **Microsoft Dataverse'i URL** – saate määrata Microsoft Dataverse'i keskkonna URL-i , kus rakenduse Guides loote. Vorming on „contoso.crm4.dynamics.com“, kus URL-i esimene osa on tavaliselt nime saanud teie organisatsiooni järgi (nt „contoso.“), teine osa on omane teie keskkonna andmepiirkonnale (nt „crm4.“) ja viimane osa on domeen (nt „dynamics.com“). Üks viis õige URL-i leidmiseks on avada [home.dynamics.com](https://home.dynamics.com/) ja seejärel avada rakendus Guides. Kui Guides avaneb, näete URL-i brauseri aadressiribal (võtke aluseks ainult põhi-URL, mis peaks meenutama eelmist näidet). Seda väärtust kasutatakse juhendite aadresside koostamiseks ja kodeeritakse QR-koodidesse.
- **QR-koodi suurus** – määrake renderdatava QR-koodi suurus. Soovitame valida suuruse, mis täidab enamiku teie ekraanist, kuid mitte rohkem. Tavaliselt on *15* hea väärtus.
- **QR-koodi veaparanduse tase** – seadke QR-koodi teralisus. Suurem teralisus võib aidata suurendada koodi usaldusväärsust, kuid teie **QR-koodi suurus** peab olema piisavalt suur, et toetada teie valitud veataseme põhjal vajalikku üksikasjalikkust.

> [!TIP]
> - QR-koodide, mis on teie kuva jaoks liiga suured, renderdamine ja siis teie kuvaga kohandamine võtab veidi kauem aega. Need ei paku eeliseid.
> - QR-koodid, mis on liiga väikesed, võivad vähendada mõnes keskkonnas HoloLensi võimet koodi korralikult lugeda.
> - Soovitame teil testida sätteid igas seadmes, milles kuvatakse QR-koodid HoloLensi jaoks. Valige sätted, mis tagavad teie tootmisjaoskonnas piisava loetavuse.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Kõigi määratud juhendite ülevaate hankimine

Kasutage lehte **Kõik juhendid**, et näha kõigi teie organisatsioonis saadaolevate juhendite loendit ning kõiki määramisi teie tootmisprotsessidele ja ressurssidele. Selle avamiseks avage **Hübriidreaalsus \> Juhendid \> Kõik juhendid**. Üleval olevas loendis kuvatakse kõik saadaolevad juhendid ja saate seda välja kasutada loendi filtreerimiseks. All olevas loendis kuvatakse kõik juhendite määramised ning tööriistariba nende haldamiseks.

![Juhendite haldamine](media/instruction-guides-allguides.png "Juhendite haldamine")

Järgmised jaotised kirjeldavad objektide tüüpe, millele saate juhendeid määrata. Iga määratud juhend sisaldab juhiseid, mis seotakse automaatselt asjaomaste tootmistöödega ja mis on saadaval tootmisjaoskonnas.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Juhendi seostamine ressursiga

Lisage [ressursile](operations-resources.md) juhend, et pakkuda seda asjakohaste tootmistööde kontekstis.

### <a name="typical-scenario-using-resources"></a>Tüüpiline stsenaarium ressursside kasutamisel

Näiteks saate lisada üldiste masinaohutus- või käsitsemisjuhistega juhendi ressursile, mille tüüp on masin. Seejärel on juhend saadaval iga töö puhul, mida masinaga tehakse.

### <a name="add-a-guide-to-a-resource"></a>Juhendi lisamine ressursile

Juhendi lisamiseks ressursile tehke järgmist.

1. Valige **Tootmise juhtimine \> Seadistus \> Ressursid \> Ressursid**.
1. Valige loendipaanist ressurss, millele soovite juhendit määrata.
1. Laiendage kiirkaart **Seotud juhendid**.
1. Valige suvand **Lisa** tööribast **Seotud juhendid**. Ruudustikku lisatakse uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata. Kui teil on palju juhendeid, saate loendit filtreerida, et leida otsitav.
    ![Juhendite haldamine](media/instruction-guides-allguides.png "Juhendite haldamine")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Juhendi seostamine ressursirühmaga

Saate lisada juhendi [ressursirühmadele](tasks/define-discrete-manufacturing-resource-group.md), kui kasutate neid masinate, tootmisridade või töörakkude rühmade haldamiseks.

### <a name="typical-scenarios-using-resource-groups"></a>Tavalised stsenaariumid ressursirühmade kasutamisel

**Näide 1:** olete määratlenud ressursirühma mitme samast mudelist masina jaoks. Selle asemel, et määrata selle masinamudeli käsitsemise juhiseid sisaldav juhend igale asjaomasele ressursile, võiksite selle asemel määrata juhendi seda masinamudelit kajastava ressursirühma jaoks.

**Näide 2:** olete määratlenud ressursirühma töörakule, mis sisaldab eri masinaid, ja teil on juhend, mis pakub üldisi juhiseid tööraku haldamiseks. Juhend kehtib mis tahes tootmistegevuse puhul selles töörakus.

### <a name="add-a-guide-to-a-resource-group"></a>Juhendi lisamine ressursirühmale

Juhendi lisamiseks ressursirühmale tehke järgmist.

1. Valige **Tootmise juhtimine \> Seadistus \> Ressursid \> Ressursirühmad**.
1. Valige loendipaanist ressursirühma, millele soovite juhendit määrata.
1. Laiendage kiirkaart **Seotud juhendid**.
1. Valige suvand **Lisa** tööribast **Seotud juhendid**. Ruudustikku lisatakse uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata. Kui teil on palju juhendeid, saate loendit filtreerida, et leida otsitav.
    ![Juhendi lisamine ressursirühmale](media/instruction-guides-resourcegroup.png "Juhendi lisamine ressursirühmale")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Juhendi seostamine väljastatud tootega

Saate lisada juhendi igale [väljastatud tootele](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Tüüpiline stsenaarium väljastatud toodete kasutamisel

Tootepõhised juhendid pakuvad tootmisjaoskonna töötajatele juhiseid selle kohta, kuidas toimida iga kindla väljastatud toote või kauba korral ja neid käsitseda.

### <a name="add-a-guide-to-a-released-product"></a>Juhendi lisamine väljastatud tootele

Juhendi lisamiseks väljastatud tootele tehke järgmist.

1. Avage **Tootmisteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage toode, millele soovite juhendit määrata.
1. Valige toimingupaanil vahekaart **Projekteerimine** ning valige rühmas **Kuvamine** suvand **Seotud juhendid**.
1. Teie valitud toote jaoks avaneb leht **Seotud juhendid**.
1. Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida. 
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine väljastatud tootele](media/instruction-guides-ReleasedProduct-AddGuides.png "Juhendi lisamine väljastatud tootele")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Juhendi seostamine valemiga

Saate lisada juhendi igale [valemile](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Tüüpiline stsenaarium valemite kasutamisel
  
Valemipõhised juhendid pakuvad tootmisjaoskonna töötajatele käsitsemisjuhiseid valemi või retsepti kontekstis. Juhendeid saab määrata ka valemi versioonidele.

> [!NOTE]
> Saate lisada valemipõhiste tootmisprotsesside puhul kehtivad juhised protsessile, protsessi versioonile või protsessi toiminguseostele.  

> Juhendeid ei saa praegu siduda üksikute valemiridadega.

### <a name="add-a-guide-to-a-formula"></a>Juhendi lisamine valemile

Juhendi lisamiseks valemile tehke järgmist.

1. Avage **Tootmisteabe haldus \> Kooslused ja valemid \> Valemid**.
1. Avage valem, millele soovite juhendit määrata.
1. Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.
1. Laiendage kiirkaart **Seotud juhendid**.
1. Valige suvand **Lisa** tööribast **Seotud juhendid**. Ruudustikku lisatakse uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine valemile](media/instruction-guides-Formula.png "Juhendi lisamine valemile")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Juhendi seostamine valemi versiooniga

Saate lisada juhendi igale [valemi versioonile](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Tüüpiline stsenaarium valemi versioonide kasutamisel

Valemi ühele versioonile lisatud juhendid annavad tootmisjaoskonna töötajatele juhiseid, mis sisaldavad valemiretsepti selle versiooni tootmise üksikasju.

> [!TIP]
> Saate lisada selle valemi versiooni põhiste tootmisprotsesside puhul kehtivad juhised protsessile, protsessi versioonile või protsessi toiminguseostele.  

> [!NOTE]
> Juhendeid ei saa praegu siduda üksikute valemiridadega.

### <a name="add-a-guide-to-a-formula-version"></a>Juhendi lisamine valemi versioonile

Juhendi lisamiseks valemi versioonile tehke järgmist.

1. Avage **Tootmisteabe haldus \> Kooslused ja valemid \> Valemid**.
1. Avage valem, mis sisaldab versiooni, millele soovite juhendit määrata.
1. Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.
1. Valige kiirkaardil **Valemi versioonid** versioon, millele soovite juhendit määrata.
1. Valige tööriistaribal **Valemi versioonid** suvand **Seotud juhendid**.
    ![Valitud valemi versiooniga seotud juhendite avamine](media/instruction-guides-FormulaVersion.png "Valitud valemi versiooniga seotud juhendite avamine")
1. Teie valitud valemi versiooni jaoks avaneb leht **Seotud juhendid**.
1. Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida. 
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine valemi versioonile](media/instruction-guides-FormulaVersionAddGuide.png "Juhendi lisamine valemi versioonile")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Juhendi seostamine kooslusega

Saate lisata juhendi mis tahes [kooslusele](bill-of-material-bom.md) (BOM).

### <a name="typical-scenario-using-bills-of-materials"></a>Tüüpiline stsenaarium koosluste kasutamisel

Kooslusele lisatud juhendid pakuvad tootmisjaoskonna töötajatele juhiseid, mis selgitavad, kuidas koosluses sisalduvat materjali ette valmistada ja käsitseda. Juhendeid saab määrata ka koosluse versioonidele.

> [!NOTE]
> Juhendeid ei saa praegu siduda üksikute koosluseridadega.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Juhendi lisamine kooslusele

Juhendi lisamiseks kooslusele tehke järgmist.

1. Minge jaotisse **Tootmisteabe haldus \> Kooslused ja valemid \> Kooslused**.
1. Avage kooslus, millele soovite juhendit määrata.
1. Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.
1. Laiendage kiirkaart **Seotud juhendid**.
1. Valige suvand **Lisa** tööribast **Seotud juhendid**. Ruudustikku lisatakse uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine kooslusele](media/instruction-guides-BOM.png "Juhendi lisamine kooslusele")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Juhendi seostamine koosluse versiooniga

Saate lisata juhendi mis tahes [koosluse versioonile](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Tüüpiline stsenaarium koosluse versioonide kasutamisel

Üksikule koosluse versioonile lisatud juhendid pakuvad tootmisjaoskonna töötajatele juhiseid, mis selgitavad, kuidas valmistada ette ja käsitseda materjali, mis on pärit koosluse versioonist, mis erineb üldisest kooslusest või selle teistest versioonidest.

> [!NOTE]
> Juhendeid ei saa praegu siduda üksikute koosluseridadega.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Juhendi lisamine koosluse versioonile

Juhendi lisamiseks koosluse versioonile tehke järgmist.

1. Minge jaotisse **Tootmisteabe haldus \> Kooslused ja valemid \> Kooslused**.
1. Avage kooslus, mis sisaldab versiooni, millele soovite juhendit määrata.
1. Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.
1. Valige kiirkaardil **Koosluse versioonid** versioon, millele soovite juhendit määrata.
1. Valige tööriistaribal **Koosluse versioonid** suvand **Seotud juhendid**.
    ![Valitud koosluse versiooniga seotud juhendite avamine](media/instruction-guides-BOMVersion.png "Valitud koosluse versiooniga seotud juhendite avamine")
1. Teie valitud koosluse versiooni jaoks avaneb leht **Seotud juhendid**.
1. Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine koosluse versioonile](media/instruction-guides-BOMVersionAddGuide.png "Juhendi lisamine koosluse versioonile")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Juhendi seostamine protsessiga

Saate lisada juhendi igale [protsessile](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Tüüpiline stsenaarium protsesside kasutamisel

Protsesse kasutatakse tavaliselt selleks, et määrata, kuidas kindlat väljastatavat toodet toodetakse koosluse või koosluse versiooni põhjal ning koos ressursside või ressursirühmadega.

Määrake protsessile juhend, et pakkuda etapiviisilisi juhiseid asjaomase tootmisprotsessi kohta.

### <a name="add-a-guide-to-a-route"></a>Juhendi lisamine protsessile

Juhendi lisamiseks protsessile tehke järgmist.

1. Avage **Tootmise juhtimine \> Kõik protsessid**.
1. Avage protsess, millele soovite juhendit määrata.
1. Laiendage kiirkaart **Seotud juhendid**.
1. Valige suvand **Lisa** tööribast **Seotud juhendid**. Ruudustikku lisatakse uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine protsessile](media/instruction-guides-Route.png "Juhendi lisamine protsessile")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Juhendi seostamine protsessi versiooniga

Saate lisada juhendi igale [protsessi versioonile](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Tüüpiline stsenaarium protsessi versioonide kasutamisel

Protsesside versioone kasutatakse tavaliselt olemasoleva protsessi põhjal tootmisprotsesside variantide täpsustamiseks. Saate määrata igale protsessi versioonile erinevad juhendid.

### <a name="add-a-guide-to-a-route-version"></a>Juhendi lisamine protsessi versioonile

Juhendi lisamiseks protsessi versioonile tehke järgmist.

1. Avage **Tootmise juhtimine \> Kõik protsessid**.
1. Avage protsess, millele soovite juhendit määrata.
1. Valige kiirkaardil **Versioonid** versioon, millele soovite juhendit määrata.
1. Valige tööriistaribal **Versioonid** suvand **Seotud juhendid**.
    ![Valitud protsessi versiooniga seotud juhendite avamine](media/instruction-guides-RouteVersion.png "Valitud protsessi versiooniga seotud juhendite avamine")
1. Teie valitud koosluse versiooni jaoks avaneb leht **Seotud juhendid**.
1. Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida.
1. Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.
    ![Juhendi lisamine protsessi versioonile](media/instruction-guides-RouteVersionAddGuide.png "Juhendi lisamine protsessi versioonile")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Juhendi seostamine protsessi toiminguseosega

Saate lisada juhendi igale [protsessi toiminguseosele](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Tüüpiline stsenaarium protsessi toiminguseoste kasutamisel

Toiminguseosed on kõige kindlam viis tooteprotsessile ja sellega seotud toimingutele juhiste lisamiseks. Saate määrata juhiseid igale protsessi toimingule ja määrata eri juhised igat tüüpi seosekontekstile, mis on protsessi puhul täpsustatud, nt kindlate kaupade, konfiguratsioonide ja muu jaoks. Samuti saate määrata, milliste toimingu etappide puhul juhend kehtib (nt seadistus, järjekord, töötlemine või transport).

> [!NOTE]
> Kui määrate juhendid protsessi mitme toiminguseose jaoks, kuvatakse tootmisjaoskonnas loodud töö puhul nende juhendite hulgast ainult kõige täpsema seose juhendit.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Juhendi lisamine protsessi toiminguseosele

Juhendi lisamiseks protsessi toiminguseosele tehke järgmist.

1. Avage **Tootmise juhtimine \> Kõik protsessid**.
1. Avage protsess, millele soovite juhendit määrata.
1. Valige toimingupaanil vahekaart **Protsess** ning valige rühmas **Haldamine** suvand **Protsessi üksikasjad**.
1. Teie valitud protsessi jaoks avaneb leht **Protsessi üksikasjad**.
1. Valige ülemises ruudustikus toiming, millele soovite juhiseid pakkuda.
1. Valige alumises ruudustikus konkreetne seos (või üldine seos **Kõik**).
    ![Toimingu ja seejärel seose valimine](media/instruction-guides-RouteOperationRelation.png "Toimingu ja seejärel seose valimine")
1. Avage alumise ruudustiku kohal olev vahekaart **Seotud juhendid**.  ![Seotud juhendite vahekaart](media/instruction-guides-RouteOperationRelation-AddGuide.png "Seotud juhendite vahekaart")
1. Valige alumise ruudustiku ülaosas olevalt tööriistaribalt suvand **Lisa**, et lisada ruudustikku uus rida.
1. Uue rea puhul kasutage veerus **Nimi** olevat ripploendit, et valida juhend, mida soovite määrata. Märkige ülejäänud reas märkeruut iga konteksti puhul, kus valitud juhend peaks saadaval olema.

> [!NOTE]
> Igale toimingu etapile saate lisada ühe või mitu juhendit.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Juhendite valimine tootmisjaoskonna käivitusliidesest

Kui töötaja avab tootmisjaoskonna käivitusliidesest tööde loendi, otsib rakendus Supply Chain Management üles asjaomased juhendid kuvatud tööde jaoks. Kasutage nuppu **Juhendid**, et vaadata asjakohaseid juhendeid.

![Nupp „Juhendid” tootmisjaoskonna käivitusliideses](media/instruction-guides-Shopfloor1.png "Nupp „Juhendid” tootmisjaoskonna käivitusliideses")

Seejärel pange ette HoloLens ning avage asjakohane juhend, vaadates QR-koodi ja aktiveerides asjakohase juhendi.

![QR-kood juhendite avamiseks HoloLensi abil](media/instruction-guides-Shopfloor2.png "QR-kood juhendite avamiseks HoloLensi abil")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Juhendite valimise loogika lahendamine

Saate lisada juhendeid järgmistele tootmisandmetele.

- [Ressursid](#resources)
- [Ressursigrupid](#resource-groups)
- [Väljastatud tooted](#released-products)
- [Valemid](#formulas)
- [Valemiversioonid](#formula-versions)
- [Kooslused (BOM-id)](#bom)
- [Koosluse versioonid](#bom-versions)
- [Marsruudid](#routes)
- [Protsessi versioonid](#route-versions)
- [Protsessi toiminguseosed](#route-operation-relations)

Kui rakendus Supply Chain Management loob tootmisjaoskonna jaoks töid, kogub see kokku asjakohased juhendid nendest allikatest. Pidage meeles järgmiseid olulisi reegleid.

- Kui lisate koosluse versiooni või valemi versiooni protsessile või tootmistellimusele, kuvatakse töö juures kõik selle versiooniga seotud juhendid ning samuti selle versiooni peakoosluse või -valemiga seotud juhendid.
- Kui lisate protsessi versiooni tootmistellimusele, kuvatakse töö juures kõik selle versiooniga seotud juhendid ning samuti selle versiooni peaprotsessiga seotud juhendid.
- Kui määratlete mitu protsessi toiminguseost, mis sisaldavad seost *Kõik*, ja määrate neile juhendid, kuvatakse töö juures ainult kõige täpsema seose juhendid.  

![Asjakohaste juhendite lahendamise diagramm](media/instruction-guides-Resolve.png "Asjakohaste juhendite lahendamise diagramm")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]