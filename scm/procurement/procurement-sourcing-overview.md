---
title: "Hangete ülevaade"
description: "See artikkel annab ülevaate hankemooduli funktsioonidest."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3669de6314e65c78ce5d401dae2e7481ec38b68
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="procurement-and-sourcing-overview"></a>Hangete ülevaade

[!include[banner](../includes/banner.md)]


See artikkel annab ülevaate hankemooduli funktsioonidest.

Hanked katavad kõiki etappe alates toote ja teenuste vajaduse tuvastamisest kuni toote hankimiseni, kviitungi, arveldamise ja hankijatega makse töötlemiseni. Hanke protsesse saab konfigureerida kindlatele ärivajadustele, määratledes ostupoliitikad ja töövood.

## <a name="identifying-a-need-for-product-and-services"></a>Toote ja teenuste vajaduse tuvastamine
Vajadus toodete või teenuste järele võib tekkida *taotlusest*, näiteks kui töötaja taotleb toodet. *Tootekataloogid *saab seadistada juhtima saadaolevate toodete valikut, mille seast valida, või saab taotleda tooteid, mis ei ole veel kataloogis saadaval, võimaldades ostuosakonnal kaaluda, kuidas toodet tarnida.  

Suvandit *Kulutuse piirmäärad *saab kasutada taotluse kulutuste piiramiseks ja *ostutöövoog *lisab enne tellimuse tegemist kinnituse nõude suvandi. Vajaduse korral saab määrata ka eelarvefondi eraldamise.  
  
Hankeosakond tuvastab nõutavate toodete ja teenuste tarnijad ning see võib hõlmata seda, et mitmele potentsiaalsele tarnijale saaadetakse *pakkumiskutse*. Taotletud toote spetsifikatsioone saab ühiskasutada ja potentsiaalsed hankijad saavad neid vaadata, et näha, kas nad saavad neile vastava toote hankida. Hankijad tagastavad oma pakkumised, mille hankeosakond siis üle vaatab, enne kui valitakse tarnija, kellelt nad soovivad hankida.  

Ostutellimused sisaldavad võimalust saata välja *ostupäring *hankijale alternatiivina põhjalikumale pakkumikutsele. Ostupäringut saab kasutada selliste tingimuste loomiseks nagu hinnad, allahindlused ja tellimuse tarnekuupäev. Kui hankijad on seadistatud kasutama portaali **Hankija**, siis on ostupäringu funktsioon keelatud. Selle asemel ühiskasutatakse tellimust portaalis**Hankija** ja kui saadetakse *kinnituse taotlus*, saab hankija tellimuse otse kinnitada.  

*Hankija katalooge *saab kasutada kogumaks teavet tootesortimendi kohta, mida hankijad tarnida saavad. Hankijad saavad avaldada oma kataloogi, et oleks lihtsam kataloogi ajakohasena hoida. Võimalik n manustada tootele * kinnitatud hankijate loend* ja see aitab juhtida hankija valikut, kui uued ostutellimused avatakse, ning vältida soovimatute hankijate kasutamist.

## <a name="procurement"></a>Hange
*Ostutellimusi *saab luua mitmel eri moel, k.a järgmiselt.

-   Koondplaneerimise tulemusena, mis on tuvastanud ostu taotleva nõude. See protsess loob plaanitud ostutellimused ja kui need vabastatakse, luuakse ostutellimused.
-   Ostutaotluste töötlemise kaudu, mis lõppeb hankega.
-   Ostulepingute töötlemise kaudu, kus ostutellimused luuakse lepingutest vabastattud tellimustena. Seda kasutatakse tavaliselt siis, kui ostulepinguid kasutatakse raamtellimuste tähistamiseks.
-   Käsitsi, kui loodud ostutellimus ei põhine muul dokumendil.

Ostutellimused, mis on konfigureeritud *ostu kinnitustöövooga*, vajavad enne kinnitatuna salvestamist kinnitamist ja seda nõutakse, enne kui tellimust saab edasi töödelda.  

Ostutellimused *kinnitatakse* näitamaks, et hankijaga on loodud leping. Ostutellimus edeneb seejärel järk-järgult läbi erinevate olekute, kuni arveldatakse või tühistatakse lõpuks.  

Ostutellimuse loomisel on paljud väljad eelnevalt täidetud väärtustega, mis on lehel **Hankijad** salvestatud vaiketeave hankija kohta. See tähendab, et peate täitma ostutellimusel piiratud koguses välju, ehkki teil on võimalus vaikeväärtused alistada.

### <a name="prices-and-discounts"></a>Hinnad ja allahindlused

Hinnad ja allahindlused sisaldavad teavet hindade, allahindluste ja nende pakutavate tagasimaksete tingimuste kohta. Hindu ja allahindlusi saab esitada *kaubanduslike* *lepingutena*. Kaubanduslikud lepingud esindavad hankija hinnaloendeid hindade või allahindlustega ja neil on kindel kuupäevade määrang, millal leping kehtib. Hinnad ja allahindlused on läbiräägitavad ja esitatavad *ostulepingute *kaudu tingimustega, nagu kohustused osta teatud koguses või rahasummas eeltingimusena läbirääkimis tingimustes. *Tagasimakseleppeid *saab luua hankijatega, kui kindlate toodete või tootegruppide hankimine võib käivitada hankija tagasimakse olenevalt ostu summast ja kogusest.

### <a name="delivery-options"></a>Tarnevalikud

Ostutellimusega seotud tarneprotsesside puhul on erinevad võimalused. Tellitud tooted saab jaotada *tarnegraafikutesse*, kus saab tellitud koguse osadele plaanida erinevad tarnekuupäevad. Tarne võib sisaldada ka ostutellimuses algatatud *otsetarnet*, mis automatiseerib saatelehe loomise müügitellimuses samal ajal kui ostutellimuses salvestatakse toote kviitung. Ostutellimused võivad olla ka *kontsernisisese tellimuse *ahela osad, mida nimetatakse ka kontsernisisesteks ostutellimusteks, kus tooteid tellitakse sobivast kontsernisisesest müügitellimusest. Selles olukorras on mõned etapid kahes seotud kontsernisiseses tellimuses automatiseeritud.

### <a name="supplementary-items"></a>Lisakaubad

Tooted saab seadistada sisaldama *lisakaupu*. See on selleks, et esitada tooteid, mis on seotud tellitava tootega. Lisatooted võivad olla nüutavad või valikulised. Mõnel juhul võidakse lisada lisakaupu tasuta toodetena, mis lisatakse muudele ostetud toodetele.

### <a name="purchase-order-charges"></a>Ostutellimuse tasud

Ostutellimusele saab määrata tasusid. See võib juhtuda automaatselt automaatsete tasude seadistamise kaudu või tasude käsitsi lisamise kaudu. Tasusid saab tellimusele määrata päise tasemel või tellimuse rea tasemel. Tasude arvestamist saab seadistada erinevatel viisidel. Näiteks saate seadistada tasu arvestamise toote kuluna. Kui seda teete, tuleb tasud määrata tellimuse rea tasemel, enne kui tellimuse aaab kinnitada. On võimalus, mis aitab tasusid tellimuse päisest ridadele eraldada.

## <a name="product-receipt-and-invoicing"></a>Toote sissetulek ja arveldamine
Füüsilisi tooteid sisaldavad ostutellimused vajavad tavaliselt laos *saabumise registreerimist* ja pärast seda registreeritakse tellimusele *toote sissetulek*. Taotlusi täitvate toodetega ostutellimused võib konfigureerida nii, et tooteid taotlenud töötaja peab lisama ka *vastuvõtmise kinnituse*.  

Mõned ostutellimused sisaldavad tooteid, mis on teenused või muud mittefüüsilised tooted, kus lao kviitungit ei ole vaja. Tooteid saab luua teenustena või selliste tellimuste puhul saab kasutada otse ostutellimusel *hankekategooriaid*. Nende tellimuste puhul jäetakse toote sissetuleku arveldamine mõnikord vahele ja tellimus arveldatakse otse või tehakse toote sissetuleku registreerimine teise võimalusena ostutellimuses ilma igasuguse eelneva saabumise registreerimiseta.  

Toodete sissetulek võib kaasa tuua automaatse tarbimise kindlal eesmärgil. See hõlmab kaudset tarbimist otsetarnega, projekti tarbimist või toote arveldamist põhivarana.  

Kui hankijalt saabuvad* hankija arved*, võidakse need esmalt salvestada ostutellimusest sõltumatusse *arveregistrisse *ja hiljem kinnitatakse need ostutellimuses kirjena. Hankija arve salvestamine ostutellimusega hõlmab toote sissetuleku vastendamist arvega.  

*Arvestuse jaotuse* saab määrata ostutellimuses kirjeldamaks, kuidas tuleks pearaamatus arveldada, ja samuti saab määratleda, kuidas eelarvefondi eraldus saadakse, kui see lisatakse teie konfiguratsiooni.  

Arveldatud ostutellimused salvestavad ostureskontros kohustuse hankija kontole, kust saab *h*a*nkija makset *töödelda.

## <a name="vendor-performance"></a>Hankija jõudlus
Ostmise jõudlust ja ülevaatust toetatakse *hanke ja ostureskontro aruannete* kaudu, mis hõlmavad kulutuse analüüsi ja hankija jõudluse analüüsi.




