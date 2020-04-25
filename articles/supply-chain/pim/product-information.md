---
title: Tooteteabe ülevaade
description: Teema annab teavet tooteteabe halduse kohta. Tooteteabe haldus toimib ühiskasutuses toote definitsiooni, kategoriseerimise ja identifikaatoritega kõigi juriidiliste isikute lõikes ja samuti toote konkreetsete konfiguratsioonidega, et sobida äriprotsessidesse.
author: cvocph
manager: tfehr
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14bcce9235a8ce1d8dc0f8c12e53f9006427cee6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208497"
---
# <a name="product-information-overview"></a>Tooteteabe ülevaade

[!include [banner](../includes/banner.md)]

Teema annab teavet tooteteabe halduse kohta. Tooteteabe haldus toimib ühiskasutuses toote definitsiooni, kategoriseerimise ja identifikaatoritega kõigi juriidiliste isikute lõikes ja samuti toote konkreetsete konfiguratsioonidega, et sobida äriprotsessidesse. 

Tooteteave on tarneahela ja kaubandusrakenduste alus kõigi valdkondade lõikes. See viitab protsessidele ja tehnoloogiatele, mis keskenduvad tooteid puudutava teabe tsentraalsele haldamisele (nt tarneahelate lõikes). On väga tähtis, et kasutataks ühiseid tootedefinitsioone, dokumentatsiooni, atribuute ja identifikaatoreid. Mitmesugustes ärilahenduse moodulites on vajalik tootepõhine teave ja konfiguratsioon, et hallata konkreetsete toodete, tooteperede või tootekategooriatega seotud äriprotsesse.

## <a name="product-definition"></a>Tootedefinitsioon

Toodet defineeritakse peamiselt toote numbri, nime ja kirjeldusega. Kuid toote või teenuse kirjeldamiseks on vaja ka muid andmeid.

- Toote tüüp: kaup või teenus
- Toote alamtüüp: eristatavad tooted või tooteetalonid
- Tootevariandi mudeli määratlus:

     - Tootedimensioonid ja dimensioonigrupid
     - Tootenomenklatuur
     - Toote konfiguratsioonimudelid

- Toote seos vähemalt ühe kategooriaga
- Toote definitsioon ja kategooria atribuudid
- Toote pildid
- Manused
- Mõõtühikud ja seotud teisendused
- Kõigi nimede ja kirjelduste tõlked

## <a name="distribution-export-and-import-of-product-data"></a>Toote andmete jaotus, eksport ja import

Tootedefinitsiooni saab luua rakenduses Supply Chain Management. Selle saab importida ka toote töötsükli halduse (PLM), toote andmehalduse (PDM) või toote teabehalduse (PIM) süsteemidest. Kui kasutatakse mitut Supply Chain Managementi eksemplari, siis kasutatakse ühte eksemplari tavaliselt kõigi teiste eksemplaride tooteandmete etalonina. Seda lähenemist toetab suur kogum andmeüksusi, mis võimaldavad tootedefinitsiooni andmete eksportimist ja importimist ühest eksemplarist teise.

Tooteandmete jaotuse toetamiseks paljudesse eksemplaridesse võimaldab Supply Chain Management kasutada teenust Common Data Service. Tootedefinitsioonid saab eksportida Supply Chain Managementi eksemplarist teenusesse Common Data Service. Seejärel saab tootedefinitsioone kasutada teiste ärirakenduste (nt Dynamics 365 Sales) varustamiseks tooteandmetega.

Pange tähele, et dünaamilistes ja kiirelt arenevates organisatsioonides muutuvad tooteteabe andmed iga päev. Seega on täpsete ja aktuaalsete tooteandmete säilitamine iseenesest väga oluline äriprotsess.

## <a name="product-masters-and-product-variants"></a>Tooteetalonid ja tootevariandid

Kiiresti muutuvas maailmas, kus tooteid tuleb kiiresti klientide nõuete järgi kohandada, määravad tootedefinitsioonid eristatavate toodete asemel tootekogumid. Rakenduses nimetatakse selliseid üldisi tooteid *tooteetalonideks*. Tooteetalonidel on definitsioon ja reeglid, mis määravad, kuidas eristatavaid tooteid äriprotsessis kirjeldatakse ja kuidas nad seal käituvad. Nende definitsioonide põhjal saab luua eristatavaid tooteid. Neid eristatavaid tooteid nimetatakse *tootevariantideks*.

Tooteetalon seostatud ärireeglite määramiseks tootedimensiooni grupi ja konfiguratsioonitehnoloogiaga. Tootedimensioonid (värv, suurus, stiil ja konfiguratsioon) on konkreetne atribuutide kogum, mida saab kasutada kogu rakenduses seotud toodete konkreetsete käitumiste määratlemiseks ja jälgimiseks. Need dimensioonid aitavad kasutajatel ka tooteid otsida ja tuvastada.

## <a name="configuration-technologies"></a>Konfiguratsioonitehnoloogiad

Valida saab kolme konfiguratsioonitehnoloogia vahel.

- Eelmääratletud variandid määratletakse eelmääratletud tootedimensioonidega. Variandi definitsioon hõlmab konkreetse kehtiva dimensioonide kombinatsiooni (nt värv, stiil ja suurus) definitsiooni. Iga kombinatsioon annab eristatava tootevariandi.
- Dimensioonipõhist konfiguratsiooni kasutatakse tavaliselt tootmisstsenaariumides ja see võimaldab kasutada koosluste definitsioonis konfiguratsiooni dimensiooni. Pärast konkreetse konfiguratsiooni valimist kasutab süsteem selle konfiguratsiooni puhul kehtivat koosluseridade alamkogumit plaanimiseks ja tootmiseks. Seda mõistet nimetatakse ka *üldiseks koosluseks*, kuna kõigi toote konfiguratsioonide puhul kasutatakse ühte ühist kooslust.
- Piirangupõhine konfiguratsioon kasutab toote konfiguratsioonimudelit kõigi võimalike atribuutide ja komponentide kirjeldamiseks, mis on vajalikud kõigi toote võimalike variantide kirjeldamiseks ühes mudelis. Atribuutide kombinatsioonide piiranguid saab kirjeldada regulaaravaldiste või tabelipõhiste piirangute kaudu. Konfiguratsioonimudelid ja konfiguraatorid muutuvad tooteteabe haldamisel järjest olulisemaks ja neid kasutatakse kõigi valdkondade lõikes.

Kui plaanite Supply Chain Managementi juurutamist, on väga tähtis, et valiksite äriprotsessile õige konfiguratsioonitehnoloogia. Toodet ei saa pärast juurutamist ühest mudelist teiseks teisendada.

## <a name="product-variant-model-definition-workspace"></a>Tootevariandi mudeli definitsiooni tööruum

Tööruum **Tootevariandi mudeli definitsioon** annab ülevaate tooteetalonidest. See kuvab etalonide ja seotud variantide väljastamise oleku konkreetsetele juriidilistele isikutele.

## <a name="released-products"></a>Väljastatud tooted

Konkreetsele juriidilisele isikule väljastatud tooteid nimetatakse *väljastatud toodeteks*. Tooted saab väljastada hulgi ühele juriidilisele isikule või paljudele juriidilistele isikutele korraga. Kuna juriidilise isiku kohta võib olla vaja lisada mitmesuguseid toodete atribuute, siis võimaldab tööruum **Väljastatud toodete haldus** jälgida ja lõpetada igas juriidilises isikus või juriidilise isiku alamorganisatsioonides hiljuti väljastatud tooted.

### <a name="released-product-maintenance-workspace"></a>Väljastatud toodete halduse tööruum

Tööruumi **Väljastatud toodete haldus** saab konfigureerida menüüelemendist **Minu tööruumi konfigureerimine**. Valige kategooriahierarhia ja kategooria, mille järgi tööruumi filtreerides. Asjakohaste toote andmete kohandamiseks tööruumis võite määratleda ka ajapiirid päevades valikutele **Hiljuti väljastatud tooted** ja **Peatatud väljastatud tooted**.

Tööruum koosneb paanide ja kahe loendi kokkuvõttest. Loendis **Avatud juhtumid** on kuvatud toote muutmise juhtumid, millel on valitud toote kategooriahierarhias tooted, mis pole lõpetatud ja suletud. Loendis **Hiljuti väljastatud** on näha tooted, mis on väljastatud tööruumi konfiguratsioonis määratud ajapiirides. Iga loendiüksuse puhul käivitatakse valideerimine ja kuvatakse valideerimise olek. See olek võib näidata, et juriidilise isiku vajalikke konfigureerimisi pole lõpule viidud. Loendist pääsete otse juurde lehtedele **Väljastatud toote üksikasjad**, **Tooteatribuudi haldus**, **Tootekategooria haldus**, **Tellimuse vaikesätted** ja **Teksti tõlked**, et viia lõpule toote vajalik konfigureerimine.

### <a name="manually-creating-a-new-released-product"></a>Uue väljastatud toote käsitsi loomine

Saate luua väljastatud toote käsitsi ühes tsüklis, olenevalt organisatsiooni äriprotsessidest ja reeglitest selle kohta, kas seda funktsiooni tuleks kasutada. See funktsioon loob uue toote ja vabastab selle automaatselt praegusele juriidilisele isikule. Uue toote loomiseks klõpsake nuppu **Väljastatud tooted** tööruumis **Väljastatud toote haldus** või loendilehel **Väljastatud toode**.
