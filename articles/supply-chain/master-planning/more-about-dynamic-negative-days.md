---
title: Negatiivsed päevad ja dünaamilised negatiivsed päevad
description: Selles teemas antakse ülevaade negatiivsetest päevadest ja dünaamilistest negatiivsetest päevadest ning kuidas neid oma ettevõtte abistamiseks kasutada.
author: t-benebo
manager: tfehr
ms.date: 06/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e64a4bd9e65b62bb782785a363aa2eee5264e3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426233"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negatiivsed päevad ja dünaamilised negatiivsed päevad

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade negatiivsetest päevadest ja dünaamilistest negatiivsetest päevadest ning kuidas neid oma ettevõtte abistamiseks kasutada. *Negatiivsete päevade ajapiir* tähistab päevade arvu, mida olete valmis ootama, enne kui tellite negatiivse kaubavaru korral uue täienduse.

Selles teemas on järgmine teave.

- Kuidas plaanitud tellimusi luuakse?
- Negatiivsete päevade ajapiiri ja kauba täitmisaja vaheline korrelatsioon
- Kuidas dünaamiliste negatiivsete päevade ajapiiri arvutatakse ja kuidas arvutamisel võetakse arvesse kauba täitmisaega.
- Kuidas tõlgendada [soovitusi materiaalsete nõuete plaanimise käitusaja parandamiseks (koondplaneerimine)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx), mis on negatiivsete päevadega seotud.

Selles teemas kasutatakse teabe mõistmise hõlbustamiseks kolme oletuslikku stsenaariumit. Erinevus stsenaariumite vahel on nõudluse saamise hetk – enne, selle ajal või pärast kauba täitmisaja perioodi lõppu.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>1. stsenaarium: saate nõudluse enne kauba täitmisaja perioodi

Võite saada nõudluse kas kauba täitmisajal suhteliselt varakult või vahetult enne täitmisaja perioodi algust. Siin on selle stsenaariumi kohta näide.

- Demotoote kaubal on kuuepäevane ostu täitmisaeg.
- Päeval null (1. jaanuar) on demotoote kaubavarude tase 0 (null).
- Päeval null (1. jaanuar) saate müügitellimuse kogusele 10 demotoodet.
- Seitsmendal päeval (7. jaanuar) on olemasolev ostutellimus kogusele 10 demotoodet.

Järgmisel joonisel on selle stsenaariumi graafiline vaade.

![1. stsenaariumi graafiline vaade](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Juhtum A: negatiivseid päevi on vähem kui kauba täitmisaeg.

Kui määrate negatiivsed päevad arvule, mis on väiksem kui kauba täitmisaeg, otsib MRP demotoote sissetulekuid negatiivsete päevade ajapiiris. Kuna see ühtegi sissetulekut ei leia, loob MRP uue plaanitud ostutellimuse. Selle plaanitud tellimus hilineb koheselt kuus päeva (täitmisaeg). Seega saabub see 7. jaanuaril. Olemasolevale ostutellimusele saabub tegevussoovitus **Tühista**, kuna uue plaanitud ostutellimuse loomine on muutnud selle üleliigseks.

Järgmisel joonisel on selle juhtumi kuvatõmmis.

![1. stsenaariumi juhtumi A kuvatõmmis](./media/negative-days-2.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![1. stsenaariumi juhtumi A graafiline vaade](./media/negative-days-3.png)

Kui kaalute MRP jõudluse ja plaani närvilisust, siis see juhtum hästi ei toimi. MRP peab looma uue plaanitud tellimuse ning arvutama viivitused ja tegevused. Need ülesanded on aeganõudvad. See juhtum lisab teie plaani veel kaks kannet. Teisest küljest hilineb müügitellimus ainult kuus päeva, mitte seitse päeva.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Juhtum B: negatiivseid päevi on rohkem kui kauba täitmisaeg.

MRP jõudluse parandamiseks saate määrata negatiivsed päevad arvule, mis on suurem kui kauba täitmisaeg. Kuna selle stsenaariumi puhul ei saa kaupa täitmisaja sees hankida, saate otsida sissetulekuid seni, kuni see otsing on mõistlik. Kuigi MRP töötamise aeg on lühem, peaksite olema tellimuste täiendavate hilinemiste osas tähelepanelik.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Juhtum C: kauba täitmisaja automaatne korreleerimine negatiivsete päevade ajapiirile

Kasutage kauba täitmisaja automaatseks negatiivsete päevade ajapiirile korreleerimiseks dünaamilisi negatiivseid päevi. Dünaamiliste negatiivsete päevade kasutamiseks avage **Koondplaneerimine \> Häälestus \> Koondplaneerimise parametrid** ja seejärel määrake vahekaardil **Üldine** jaotises **Laovarud** suvand **Kasuta dünaamilisi negatiivseid päevi** valikule **Jah**. MRP otsib seejärel sissetulekuid dünaamiliste negatiivsete päevade ajapiiri sees. See ajapiir arvutatakse järgmist valemit kasutades.

Dünaamiliste negatiivsete päevade ajapiir = ostu täitmisaeg + negatiivse päeva ajapiir + (praegune kuupäev – nõudekuupäev)

(Kui demotoote vaikimisi kasutatava tellimuse tüüp on **Tootmine** või **Ülekanne**, on ajapiir **varude** ajapiir.)

Kui kasutatakse dünaamilisi negatiivseid päevi, on MRP sissetulekute otsimise ajapiir nüüd 6 + 2 + 0 = 8 päeva. MRP leiab olemasoleva ostutellimuse ja seob müügitellimuse sellega. Uusi plaanitud tellimusi ei looda. Seetõttu on MRP töötamise aeg lühem. Järgmisel joonisel on näha demotoote netonõuded.

![1. stsenaariumi juhtumi C netonõuded](./media/negative-days-4.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![1. stsenaariumi juhtumi C graafiline vaade](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Juhtum D: ainult dünaamiliste negatiivsete päevade kasutamine

Kui määrate negatiivsed päevad väärtusele **0** (null) ja kasutate ainult dünaamiliste negatiivsete päevade ajapiiri, on dünaamiliste negatiivsete päevade ajapiir 6 + 0 + 0 = 6 päeva. Sellisel juhul on tulemus sama, mis selle stsenaariumi juhtumi A puhul. MRP peab looma uue plaanitud tellimuse ning arvutama viivitused ja tegevused. Need ülesanded on aeganõudvad ja võivad olla ka heidutavad. Teil on veel töödelda kaks kannet. Kuna nõudlust ei saa kauba õigeaeseks saabumiseks täita, lisab see plaanile tarbetuid komplikatsioone.

Järgmisel joonisel on selle juhtumi kuvatõmmis.

![1. stsenaariumi juhtumi D kuvatõmmis](./media/negative-days-6.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![1. stsenaariumi juhtumi D graafiline vaade](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Juhtum E: mõlema negatiivse päeva kasutamine, mis on suurem kui kauba täitmisaeg ja dünaamiliste negatiivsete päevade ajapiir.

Kui määrate negatiivsed päevad väärtusele, mis on suurem kui kauba täitmisaeg, ja kui kasutate ka dünaamiliste negatiivsete päevade ajapiiri, on dünaamiliste negatiivsete päevade ajapiir 6 + 6 + 0 = 12 päeva. See lähenemine võib luua väga pika ajapiiri, mille seast MRP peab tulemusi otsima. Teavet selle kohta, kuidas juhtum E on seotud olukorraga, kus määrate negatiivsed päevad pikale ajapiirile, vt selle teema jaotist [Lõppsõna](#conclusion).

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>2. stsenaarium: saate nõudluse kauba täitmisaja perioodi jooksul

Võite saada nõudluse millalgi kauba täitmisajal. Siin on selle stsenaariumi kohta näide.

- Demotoote kaubal on kuuepäevane ostu täitmisaeg. 
- Päeval null (1. jaanuar) on demotoote kaubavarude tase 0 (null).
- Neljandal päeval (5. jaanuar), mis on kauba täitmisaja sees, saate müügitellimuse kogusele 10 demotoodet.
- Seitsmendal päeval (8. jaanuar) on ostutellimus kogusele 10 demotoodet.

Järgmisel joonisel on selle stsenaariumi graafiline vaade.

![1. stsenaariumi graafiline vaade](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Juhtum A: negatiivseid päevi on vähem kui kauba täitmisaeg.

Kui määrate negatiivsed päevad arvule, mis on väiksem kui kauba täitmisaeg, otsib MRP demotoote sissetulekuid negatiivsete päevade ajapiiris. Kuna see ühtegi sissetulekut ei leia, loob MRP uue plaanitud ostutellimuse, mis kasutab tellimuse kuupäevana praegust kuupäeva. Selle plaanitud tellimus hilineb koheselt kuus päeva (täitmisaeg). Seega saabub see 7. jaanuaril. Olemasolevale ostutellimusele saabub tegevussoovitus **Tühista**, kuna uue plaanitud ostutellimuse loomine on muutnud selle üleliigseks.

Järgmisel joonisel on selle juhtumi kuvatõmmis.

![2. stsenaariumi juhtumi A kuvatõmmis](./media/negative-days-9.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![2. stsenaariumi juhtumi A graafiline vaade](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Juhtum B: negatiivseid päevi on rohkem kui kauba täitmisaeg.

See juhtum sarnaneb 1. stsenaariumi juhtumile B. Kui määrate negatiivsed päevad väärtusele, mis on suurem kui kauba täitmisaeg, te uut plaanitud tellimust ei saa. Müügitellimus on seotud olemasoleva ostutellimusega.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Juhtum C: kauba täitmisaja automaatne korreleerimine negatiivsete päevade ajapiirile

See juhtum meenutab 1. stsenaariumi juhtumit C, kuna dünaamilised negatiivsed päevad töötavad sama hästi kui selle juhtumi korral. Dünaamiliste negatiivsete päevade ajapiir on nüüd 6 + 2 – 4 = 4 päeva. Kui kasutate seda lähenemist, otsib MRP olemasoleva ostutellimuse ja seob müügitellimuse sellega. Kuna uusi plaanitud tellimusi ei looda, on MRP töötamise aeg lühem.

Järgmisel joonisel on selle juhtumi kuvatõmmis.

![2. stsenaariumi juhtumi C kuvatõmmis](./media/negative-days-11.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![2. stsenaariumi juhtumi C graafiline vaade](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Juhtum D: ainult dünaamiliste negatiivsete päevade kasutamine

Kui määrate negatiivsed päevad väärtusele **0** (null) ja kasutate ainult dünaamiliste negatiivsete päevade ajapiiri, on dünaamiliste negatiivsete päevade ajapiir nüüd 6 + 0 – 4 = 2 päeva. Sellisel juhul on tulemus sama, mis selle stsenaariumi juhtumi A puhul. Toimuva graafiliseks vaateks vaadake selle stsenaariumi juhtumit A.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Juhtum E: mõlema negatiivse päeva kasutamine, mis on suurem kui kauba täitmisaeg ja dünaamiliste negatiivsete päevade ajapiir.

Kui määrate negatiivsed päevad väärtusele, mis on suurem kui kauba täitmisaeg, ja kui kasutate ka dünaamiliste negatiivsete päevade ajapiiri, on dünaamiliste negatiivsete päevade ajapiir 6 + 6 – 4 = 8 päeva. See lähenemine võib luua väga pika ajapiiri, mille seast MRP peab tulemusi otsima. Teavet selle kohta, kuidas juhtum E on seotud olukorraga, kus määrate negatiivsed päevad pikale ajapiirile, vt selle teema jaotist [Lõppsõna](#conclusion).

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>3. stsenaarium: saate nõudluse pärast kauba täitmisaja perioodi

Võite saada nõudluse pärast kauba täitmisaja perioodi. Siin on selle stsenaariumi kohta näide.

- Demotoote kaubal on kuuepäevane ostu täitmisaeg.
- Päeval null (1. jaanuar) on demotoote kaubavarud 0 (null).
- Seitsmendal päeval (8. jaanuar), mis on kauba täitmisajast väljaspool, saate müügitellimuse kogusele 10 demotoodet.
- 10. päeval (11. jaanuar) on ostutellimus kogusele 10 demotoodet.

Järgmisel joonisel on selle stsenaariumi graafiline vaade.

![3. stsenaariumi graafiline vaade](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Juhtum A: negatiivseid päevi on vähem kui kauba täitmisaeg.

Kui määrate negatiivsed päevad väärtusele, mis on väiksem kui kauba täitmisaeg, vaatab MRP müügitellimuse vajaduse kuupäevast kaks päeva edasi. Kuna see midagi ei leia, loob MRP 2. jaanuaril plaanitud ostutellimuse. See plaanitud ostutellimus saadetakse müügitellimuse nõudluse täitmiseks täpselt õigeks ajaks. Olemasolev ostutellimus saab tegevussoovituse **Tühista**, kuna see pole vajalik.

Järgmisel joonisel on selle juhtumi kuvatõmmis.

![3. stsenaariumi juhtumi A kuvatõmmis](./media/negative-days-14.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![3. stsenaariumi juhtumi A graafiline vaade](./media/negative-days-15.png)

> [!NOTE]
> Eelmisel kuvatõmmisel on ostutellimuse vajaduse kuupäev 12. jaanuar. Kuna see kuvatõmmis tehti 2015. aastal, kui 11. jaanuar oli pühapäev, liigutas MRP vajaduse kuupäeva järgmisele tööpäevale, mis oli esmaspäev, 12. jaanuar. Sellegipoolest on ostutellimuse tarnekuupäev 11. jaanuar.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Juhtum B: negatiivseid päevi on rohkem kui kauba täitmisaeg.

Kui määrate negatiivsed päevad väärtusele, mis on suurem kui kauba täitmisaeg, te uut plaanitud tellimust ei saa. Müügitellimus seotakse olemasoleva ostutellimusega. Seetõttu ostutellimus hilineb. Kui loote plaanitud tellimuse, saate müügitellimuse õigeaegselt lähetada.

Järgmisel joonisel on selle juhtumi kuvatõmmis.

![3. stsenaariumi juhtumi B kuvatõmmis](./media/negative-days-16.png)

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![3. stsenaariumi juhtumi B graafiline vaade](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Juhtum C: kauba täitmisaja automaatne korreleerimine negatiivsete päevade ajapiirile

See juhtum meenutab 1. stsenaariumi juhtumit C, kuna dünaamilised negatiivsed päevad töötavad sama hästi või isegi paremini kui selle stsenaariumi juhtumi B korral.

Dünaamiliste negatiivsete päevade ajapiir on nüüd 6 + 2 – 7 = 1 päev. Kuid sellisel juhul arvestab süsteem endiselt negatiivsete päevade täitmisajaga (2), kuna MRP võtab arvesse maksimaalse väärtuse negatiivsete päevade täitmisaja ja dünaamiliste negatiivsete päevade täitmisaja vahel. Seetõttu on selle juhtumi tulemus sama, mis selle stsenaariumi juhtumi A puhul.

Järgmisel joonisel on selles juhtumis toimuva graafiline vaade.

![3. stsenaariumi juhtumi C graafiline vaade](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Juhtum D: ainult dünaamiliste negatiivsete päevade kasutamine

Kui määrate negatiivsed päevad väärtusele **0** (null) ja kasutate ainult dünaamiliste negatiivsete päevade ajapiiri, on dünaamiliste negatiivsete päevade ajapiir nüüd 6 + 0 – 7 = –1 päev. Sellisel juhul arvestab süsteem endiselt negatiivsete päevade täitmisajaga (2). Seetõttu on selle juhtumi tulemus sama, mis selle stsenaariumi juhtumi A puhul, ja sellel on kõik samad puudused. Toimuva graafiliseks vaateks vaadake 2. stsenaariumi juhtumit A.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Juhtum E: mõlema negatiivse päeva kasutamine, mis on suurem kui kauba täitmisaeg ja dünaamiliste negatiivsete päevade ajapiir.

See juhtum on sama, mis 1. ja 2. stsenaariumi juhtum E. Sellel on põhimõtteliselt samad eelised ja puudused.

## <a name="conclusion"></a>Lõppsõna

Nagu selle teema kolm stsenaariumit näitava, on hea mõte seada negatiivsed päevad väärtusele, mis on suurem kui laovarude grupi kaupade täitmisaeg. Samuti on hea mõte kasutada ainult dünaamilisi negatiivseid päevi ja määrata negatiivsed päevad päevade arvule, kaua olete negatiivse laovaru korral nõus enne uue täiendamise tellimist ootama (teisisõnu päevade arv, kaua olete nõus nõudlust veel edasi lükkama). Lisaks peaks samas laovarude grupis olevatel kaupadel olema sarnased täitmisajad.

Kui määrate negatiivsed päevad väärtusele **0** (null) ja dünaamilisi negatiivseid päevi ei kasuta, loob MRP nõudluse täitmiseks alati uue plaanitud tellimuse. Sellises olukorras on oluline, et töötate tegevussoovitustega veendumaks, et te kaubavarusid ei kuhjaks.

Võite soovida seada negatiivsed päevad pikale ajapiirile ja seejärel töötada tegevussoovitustega. See lähenemisviis annab häid planeerimistulemusi, kuid see on ka veidi aeglasem. Seda võib olla ka raskem analüüsida, kuna peate analüüsima ja rakendama tegevussoovitusi. Siin on näide.

- Demotoote kaubal on kuuepäevane ostu täitmisaeg.
- Päeval null (1. jaanuar) on demotoote kaubavarud 0 (null).
- Päeval null (1. jaanuar) saate müügitellimuse kogusele 10 demotoodet.
- 10. päeval (10. jaanuar) saate müügitellimuse kogusele 10 demotoodet.
- 12. päeval (12. jaanuar) on ostutellimus kogusele 10 demotoodet.
- Negatiivsed päevad on määratud väärtusele **20**, mis on palju pikem kui kauba täitmisaeg.

Järgmisel joonisel on toimuva graafiline vaade.

![Näite graafiline ülevaade](./media/negative-days-19.png)

MRP annab järgmised tulemused.

![Tulemused](./media/negative-days-20.png)

Eelmisel kuvatõmmisel on müügitellimuse vajaduse kuupäev 10. jaanuari asemel 9. jaanuaril. Kuna see kuvatõmmis tehti 2015. aastal, kui 10. jaanuar oli laupäev, peaks vajaduse kuupäev olema eelmine tööpev, mis oli reede, 9. jaanuar.

MRP loob plaanitud ostutellimuse, et täita esimese müügitellimuse nõudlus, kuid see soovitab ka plaanitud tellimuse tühistada, kuna saate olemasoleva ostutellimuse ette võtta ja kogust suurendada.

Tulemused ei ole valed, kuid MRP toimimise aeg võib olla pikem, kuna MRP peab looma kõik hilinemised ja soovitused. Lisaks võib plaanija vajada MRP tulemuste mõistmiseks rohkem aega. Mis kõige olulisem, selle juhtumi puhul on oluline, et plaanija mõistaks ja kasutaks tegevussoovitusi.

Kui vähendate negatiivsed päevad arvule, mis on kauba täitmisajale lähemal, ja kasutate dünaamilisi negatiivseid päevi, annab MRP järgmised tulemused.

![Tulemused](./media/negative-days-21.png)

MRP loob plaanitud tellimuse, mis on esimese müügitellimusega seotud. Seejärel seotakse teine müügitellimus oodatult negatiivsete päevade seadistuse põhjal olemasoleva müügitellimusega. Selle planeerimise tulemus on samuti õige ja MRP töötamise aeg võib olla lühem. Sellisel juhul pole oluline mõista ja teada, kuidas tegevussoovitustega töötada.

Teie ettevõtte jaoks õigete väärtuste sisestamise tagamiseks peate mõtlema nii funktsioonidele kui ka MRP töötamise ajale. Seetõttu võib optimaalsete väärtuste määramiseks olla vaja veidi proovida.

## <a name="see-also"></a>Vt ka

Täiendavat arutelu vt algsest ajaveebipostitusest [(Dünaamiliste) negatiivsete päevade lisateave](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/).
