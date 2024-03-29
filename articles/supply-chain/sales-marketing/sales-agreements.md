---
title: Müügilepingute ülevaade
description: Selles artiklis antakse teavet müügilepingute kohta. Müügileping on lepe, mis kohustab klienti aja jooksul kindlates kogustes või kindla summa eest tooteid ostma ja võimaldab seda teha erihinnaga või allahindlustega.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage, SalesAgreementInvoiceJournal, SalesAgreementInvoicePart
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "9554"
- intro-internal
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e84b8be597870deea3beaf1bdc4a98021b7f135
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903836"
---
# <a name="sales-agreements-overview"></a>Müügilepingute ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet müügilepingute kohta. Müügileping on lepe, mis kohustab klienti aja jooksul kindlates kogustes või kindla summa eest tooteid ostma ja võimaldab seda teha erihinnaga või allahindlustega.

Müügileping on leping, mis kohustab kliendi ostma tooteid konkreetses koguses või kindla summa eest teatud aja jooksul, saades selle eest erihindu, eriallahindlusi ja muid eritingimusi, nagu makse- ja tarnetingimused. Müügilepingu hinnad ja allahindlused tühistavad kõik hinnad ja allahindlused, mis on märgitud kõigis olemasolevates kaubanduslepetes.  

Müügilepingu kehtivusperiood määratletakse lepingu väljadega **Jõustumiskuupäev** ja **Aegumiskuupäev**. Kliendi müügitellimus vastab lepingu tingimustele kui tellimuse nõutav lähetuskuupäev on tellimuse kehtivusperioodi piires. Kõik müügilepinguga seotud müügitellimuse read aitavad kaasa selle müügilepingu täitmisele.  

Saate luua müügitellimuse otse müügilepingult, kasutades tegevust **Väljalaskeorder**. Teine võimalus on valida tellimuste tegemisel kehtiva müügilepingu (vt selle artikli jaotist „Müügilepingute rakendamine tellimisprotsessis”).  

> [!NOTE] 
> Varasemates versioonides viidatakse müügilepingutele kui raammüügitellimustele.

## <a name="commitment-types"></a>Kohustuse tüübid
Müügilepingu iga rida väljendab teatud kauba müümise kohustust. Üldiselt on kohustusekategooriaid kaks.

-   **Väärtuse kohustus**– klient nõustub ostma tooteid kindla summa eest.
-   **Koguse kohustus**– klient nõustub ostma kindla koguse tooteid.

Peale selle saab leping kohustada klienti ostma teatud toodet või tootekategoorias olevaid tooteid. Kombineerides neid kaht tegurit (väärtus vs kogus ning konkreetsed tooted vs tootekategooriad), saame nelja tüüpi kohustusi.

-   **Toote koguse kohustus** – klient nõustub ostma kindla koguse tooteid. Read, mis kasutavad seda kohustusetüüpi, määratletakse kaubakoodi ning kokkulepitud koguse ja ühiku järgi. Väli **Summa** pole saadaval.
-   **Toote väärtuse kohustus** – klient nõustub ostma konkreetseid tooteid kindla summa eest. Read, mis kasutavad seda kohustusetüüpi, määratletakse kaubakoodi ja kokkulepitud summa järgi. Väljad **Kogus** ja **Ühik** ei ole saadaval.
-   **Tootekategooria väärtuse kohustus** – klient nõustub ostma tooteid konkreetsest müügikategooriast kindla summa eest. Read, mis kasutavad seda kohustusetüüpi, määratletakse müügikategooriate hierarhiasse kuuluva müügikategooria ja summa järgi. Väljad **Kogus** ja **Ühik** ei ole saadaval.
-   **Väärtuse kohustus** – klient nõustub ostma mis tahes toodet või mis tahes hankekategooriasse kuuluvaid tooteid kindla summa eest. Väljad **Kogus** ja **Ühik** ei ole saadaval.

Sama müügilepingu ridadel võivad olla erinevat tüüpi kohustused.

## <a name="pricing-terms-for-sales-agreements"></a>Müügilepingute hinnakujunduse tingimused
Hinnakujunduse tingimused võivad erineda olenevalt kohustuse tüübist. Müügilepinguga seotud müügitellimusel tühistavad selle müügilepingu hinnakujunduse tingimused kõik muud kaubanduslepete põhjal rakenduvad hinnakujunduse tingimused. Järgmises tabelis kirjeldatakse hinnaga seotud välju, mida iga kohustuse tüüp mõjutab. Suvand Jah näitab, et välja saab tellimusereal värskendada.

| Kohustuse tüüp                   | Ühiku hind | Hinnaühik | Allahindluse protsent | Skonto summa |
|-----------------------------------|------------|------------|------------------|----------------------|
| Toote koguse kohustus       | Jah        | Jah        | Jah              | Jah                  |
| Toote väärtuse kohustus          |            |            | Jah              |                      |
| Tootekategooria väärtuse kohustus |            |            | Jah              |                      |
| Väärtuse kohustus                  |            |            | Jah              |                      |

## <a name="policies-for-sales-agreements"></a>Müügilepingute poliitikad
Järgmised poliitikad mõjutavad müügilepingu kohustuse ja vastava müügitellimuse ridade vahelise seose toimimise viisi.

-   **Maksimum rakendatud** – kõikide tellimuse ridade koondkogus ega koondsumma ei või ületada seotud kohustuses määratud kogust ega summat.
-   **Hind ja allahindlus on fikseeritud** – tellimusereal olev hind ja seotud kohustuses olev hind ei tohi erineda. Kui hinda tellimuse real muudetakse, on seos kohustusega katkestatud. Kui seos on katkenud, ei panusta tellimuse rida kohustuse täitmisse.
-   **Minimaalne väljastussumma** ja **Maksimaalne väljastussumma** – kui summa on määratud, kuvatakse sõnum, kui teete tellimusereal muudatuse, mille tagajärjel erineb tellimuserida seotud kohustusest.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Müügilepingute täitmise arvutused
Lehe **Müügilepingud** kiirkaardi **Rea üksikasjad** vahekaardil **Täitmine** kuvatakse täitmise kogused ja summad.  

Alal **Täitmine** saate vaadata kõigi määratud müügilepingutega seotud tellimuseridade kogukoguseid ja -summasid. Samuti saate vaadata järelejäänud summat või kogust, mida on kohustuse täitmiseks vaja.  

Alal **Leping** saate vaadata määratud müügilepingu koguseid ja summasid. Need kogused ja summad on kohustuslikud kogukogused ja -summad.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Müügilepingute kinnitused ja versiooniajalugu
Müügilepingu kinnitamisel salvestatakse müügilepingu praegune versioon ajalootabelisse. Kui muudate müügilepingut, saate selle uuesti kinnitada, et salvestada ajalukku müügilepingu teine versioon.  

Kui te müügilepingut ei kinnita, saate seda endiselt müügitellimuste loomiseks kasutada. Müügilepingu ajalooteavet siiski ei salvestata.  

Saate kõiki kinnituste parandusi eelvaadata või printida. Seejärel saate parandusi kinnituse saamiseks oma kliendiga jagada.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Müügilepingute kasutamine tellimisprotsessi ajal
Kui te ei väljasta müügitellimusi müügilepingu puhul otse, saate siiski siduda müügilepingu tellimusega tellimuse sisestamise protsessi käigus. Kui loote uue uue müügitellimuse ja valite müügilepingu, rakendatakse selle lepingu tingimused, nagu maksetingimused, tarnetingimused ja tarneaadress, tellimuse päisele ning lepingu ja tellimuse vahel luuakse seos. Seejärel kopeeritakse hinnad ja allahindlused sellest lepingust tellimuseridadele, kus saate valida müügilepingus määratud tooteid ja kategooriaid. Sama müügitellimus võib sisaldada nii ridu, mis ei ole müügilepinguga seotud, kui ka ridu, millel on müügilepingu kohustus.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Müügilepinguga seotud müügitellimuste muutmine
Kui olete loonud (väljastanud) müügilepinguga seotud müügitellimuse, saate mõnd selle müügitellimuse ridade väärtust muuta ainult siis, kui eemaldate lingi seostatud müügitellimuse ridadega. Mõni neist väljadest on toodud allolevas tabelis.

| Väli                                                             | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nõutav lähetuskuupäev                                               | Kui muudate nõutud lähetuskuupäeva kuupäevale, mis on varasem kui müügilepingu real olev väärtus **Jõustumiskuupäev**, peate eemaldama lingi müügilepingu reaga, enne kui saate muudetud lähetuskuupäeva salvestada. Kui muudate nõutud lähetuskuupäeva kuupäevale, mis on hilisem kui müügilepingu real olev väärtus **Aegumiskuupäev**, peate eemaldama lingi müügilepingu reaga, enne kui saate muudetud lähetuskuupäeva salvestada. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNeti summa | Kui muudate mõne selle välja väärtust ja seostatud müügilepingu real on märgitud ruut **Hind ja allahindlus on fikseeritud**, kuvatakse sõnumiviip, milles palutakse teil muudatus salvestada. Klõpsake valikut **Jah**, et eemaldada link müügilepingu reaga ja hind ümber arvutada. Klõpsake valikut **Ei**, et eemaldada link müügilepingu reaga ilma hinda ümber arvutamata.                                                                   |
| Netosumma                                                        | Kui määrate summa, mis ületab summat müügilepingu real, kus märgitud on ruut **Maksimaalne on jõustatud**, kuvatakse sõnumiviip, milles palutakse teil muudetud summa salvestada. Klõpsake valikut **Jah**, et eemaldada link müügilepingu reaga ja hind ümber arvutada. Klõpsake valikut **Ei**, et eemaldada link müügilepingu reaga ilma hinda ümber arvutamata.                                                                 |
| Kogus                                                          | Kui määrate koguse, mis ületab kogust müügilepingu real, kus märgitud on ruut **Maksimaalne on jõustatud**, kuvatakse sõnumiviip, milles palutakse teil muudetud kogus salvestada. Klõpsake valikut **Jah**, et eemaldada link müügilepingu reaga ja hind ümber arvutada. Klõpsake valikut **Ei**, et eemaldada link müügilepingu reaga ilma hinda ümber arvutamata.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Müügilepingu alusel tellitud kauba tagastamine
Kui klient tagastab toote, mis on tellitud müügilepingu alusel, saab Supply Chain Management seotud müügilepingu kohustuse leida ja seda automaatselt värskendada, et kajastada koguse või summa muutust. Algse müügilepinguga lingitud müügitellimuse põhjal tagastustellimust luues loote lingi müügilepingu kohustuse, müügitellimuse rea ja tagastustellimuse arve vahel.  

Kui te ei soovi tagastatud kauba kogust müügilepingu kohustusest lahutada, saate kasutada lehel **Tagastustellimus** juhtnuppu **Eemalda link**, et eemaldada tagastustellimuse ja müügilepingu kohustuse vaheline link. Kui peate lingi hiljem uuesti looma, klõpsake nuppu **Loo link**.  

**Märkus.** Tagastustellimust saab linkida ainult ühe müügilepinguga. Kui klient tagastab mitu toodet, mis on tellitud rohkem kui ühe müügilepingu alusel, peate looma igale tootele uue tagastustellimuse ja lingi vastava müügilepinguga.

## <a name="automatic-search-for-sales-agreements"></a>Müügilepingute automaatne otsimine
Mõnes olukorras, kui müügitellimus luuakse kaudselt, nt kreeditarve või kontsernisiseste müügitellimuste loomisel, saate määrata, kas süsteem otsib rakendatavaid müügilepinguid automaatselt.

## <a name="financial-dimensions-on-sales-agreements"></a>Müügilepingute finantsdimensioonid
Saate kopeerida finantsdimensioonid kas dokumendipäistesse või müügilepingu üksikutele ridadele. Saate mis tahes lepingupäises või lepingureal olevaid dimensioone igal ajal muuta. Sellisel juhul kopeeritakse dimensioonid automaatselt väljastuspäisesse või väljalaskeorderite väljastusreale.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]