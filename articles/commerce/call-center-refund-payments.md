---
title: Tagasimaksete töötlemine kõnekeskustes
description: See artikkel selgitab, kuidas makse tagasimakseid luuakse kõnekeskuste kaudu, kui tagastused luuakse või kui tellimused või tellimuse read tühistatakse.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 330674a31dc59e99ffedb82d0896c64214562eb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880110"
---
# <a name="refund-payment-processing-in-call-centers"></a>Tagasimaksete töötlemine kõnekeskustes

See artikkel selgitab, kuidas makse tagasimakseid luuakse kõnekeskuste kaudu, kui tagastused luuakse või kui tellimused või tellimuse read tühistatakse.

Kasutaja, kes loob kliendile tagastustellimuse kõnekeskuse kasutajana Microsoft Dynamics 365 Commerce'i peakontoris, kasutab lehte **Tagastustellimus**, et luua esialgne tagastatud kauba kood (RMA). RMA määratleb tooted, mida klient soovib tagastada või vahetada, ja loob lingitud tagastamise müügitellimuse, mille tellimuse tüüp on **Tagastatud tellimus**. Seda lingitud tagastustellimust kasutatakse tagastatud varude sisestamise ja mis tahes sisestatud kreeditarvete või tagasimaksete jälgimiseks.

Kui kõnekeskuse kanali puhul on suvandi **Tellimuse lõpetamise lubamine** väärtuseks määratud **Jah**, peab RMA loonud kõnekeskuse kasutaja käivitama tellimuse täitmise töötlemisvoo, valides lehel **Tagastustellimus** käsu **Vii lõpule**. Funktsioon **Vii lõpule** kuvab arvutatud tagastuse kokkuvõtte, milles on toodud teave maksmisele kuuluva tagasimakse summa kohta. Peale selle, kui see on õigesti seadistatud, loob see süstemaatiliselt tagastustellimusele vastava tagasimakse rea.

Kõnekeskuse loogika määrab tagasimakse rea makseviisi, mis põhineb algses tellimuses kasutatud makseviisil. Kui loodud tagastustellimus ei ole algse tellimusega lingitud, rakendatakse süsteemiparameetri kohast vaikemakseviisi.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Kuidas määrab kõnekeskus tagastustellimusele rakendatava makseviisi?

Kõnekeskus lähtub tagastustellimusele rakendatava makseviisi määramisel algse tellimuse makseviisist. Allpool on teave selle kohta, kuidas toimib see protsess järgmiste algsete makseviiside korral.

- **Tavaline** (sularaha) või **Tšekk** – kui loodud tagastustellimus viitab algsele tellimusele, mille eest maksmiseks kasutati tavalist (sularaha) või tšekipõhist makseviisi, viitab kõnekeskuse rakendus konfiguratsioonidele lehel **Kõnekeskuse tagasimakseviisid**. See leht võimaldab organisatsioonidel määrata tellimuse vääringu alusel seda, kuidas väljastatakse tagasimakseid klientidele tellimuste eest, mille eest algselt tasumiseks kasutati tavalist või tšekipõhist maksetüüpi. Kõnekeskuse **tagasimakse meetodite** leht võimaldab organisatsioonil valida ka selle, kas kliendile tuleb saata süsteemi loodud tagasimakse kontroll. Nendes stsenaariumides viitab kõnekeskuse loogika tagastustellimuse vääringule ja kasutab seejärel tagastamise müügitellimuse tagasimakse rea loomiseks väljal **Jaemüügi makseviis** toodud väärtust selle vääringu kohta. Hiljem lingitakse vääringuga müügireskontro (AR) kliendi maksetööleht, mis kasutab vastendatud AR-makseviisi.

    Järgmisel joonisel on toodud konfiguratsioon sellise stsenaariumi korral, kus klient tagastab tooted, mis pärinevad USD vääringuga lingitud müügitellimusest, ja mille eest algselt tasumiseks kasutati tavalist või tšekipõhist maksetüüpi. Selles stsenaariumis väljastatakse kliendile tagasimakse süsteemi genereeritud tagasimaksetšeki kaudu. AR-makseviis **REF-CHK** on konfigureeritud tagasimaksetšeki maksetüübina.

    ![Kõnekeskuse tagasimakseviiside konfigureerimine tavaliste ja tšekipõhiste algsete maksete korral.](media/callcenterrefundmethods.png)

    > [!NOTE]
    > Kliendi konto ei ole sularaha- või tšekimaksete tagasimakseviis.

- **Krediitkaart** – kui loodud tagastustellimus viitab algsele tellimusele, mille eest maksmiseks kasutati krediitkaarti, rakendab kõnekeskuse tagasimakseloogika tagastustellimusele sama algse krediitkaardi.
- **Kliendikaart** – kui loodud tagastustellimus viitab algsele tellimusele, mille eest maksmiseks kasutati kliendikaarti, rakendab kõnekeskuse tagasimakseloogika tagasimakse samale algsele kliendikaardile.
- **Kinkekaart** (ettevõttesisene) – kui loodud tagastustellimus viitab algsele tellimusele, mille eest maksmiseks kasutati Dynamics 365 Commerce'i kaudu väljastatud kinkekaarti (ettevõttesisese kinkekaardi funktsionaalsus), rakendab kõnekeskuse tagasimakseloogika tagasimakse samale algsele kinkekaardile.
- **Kinkekaart** (väline) – kui loodud tagastustellimus viitab algsele tellimusele, mille eest maksmiseks kasutati välist kolmanda osapoole kinkekaarti, rakendab kõnekeskuse tagasimakseloogika vaikimisi lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** määratud tagastusmakseviisi.

Kui algse tellimuse maksetüüp on mis tahes põhjusel tundmatu või kui algse tellimuse eest maksmiseks kasutati mitut makseviisi, rakendab kõnekeskuse loogika vaikimisi lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** määratud tagastusmakseviisi.

Järgmisel joonisel on näidatud lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** olev väli **Makseviis**.

![Lehe Kõnekeskuse parameetrid vahekaardil RMA/Tagastus olev väli Makseviis.](media/callcenterrefundparameters.png)

> [!NOTE]
> Ülalpool kirjeldatud tagasimakse töötlemise reeglid kehtivad ka tellimustele või tellimuse ridadele, mille kõnekeskuse kasutaja Commerce'i peakontoris tühistab. Kui tellimuse või kindlate tellimuse ridade tühistamine põhjustab ülemakseid, kasutatakse tagasimakse ridade loomiseks samu reegleid.

Tavaliselt läbib tagastustellimus standardse protsessi, kus vara võetakse vastu (või kantakse maha), tagastustellimuse suhtes sisestatakse saateleht ja seejärel käivitatakse tagastamise müügitellimuse arve sisestamise protsess. Tagastamise müügitellimus lingitakse ja genereeritakse süstemaatiliselt tagastustellimuse loomise protsessi osana. Tüüpilistes stsenaariumides ei väljastata klientidele tagasimakseid enne, kui tagastamise müügitellimus on sisestatud.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Mis juhtub, kui tagastamise müügitellimusele sisestatakse arve?

Järgmiste stsenaariumite abil selgitatakse, mis juhtub, kui tagastamise müügitellimusele sisestatakse arve.

- Kui tagastustellimuse tagasimakse rakendatakse krediitkaardile, käivitub arve sisestamisel täiendav loogika. See loogika käsib maksetöötlejal teha tagasimakse kliendi krediitkaardile. Samuti luuakse ja sisestatakse kliendi kontol süstemaatiliselt ka kliendimakse tagastuskanne. See maksetööleht tasakaalustatakse tagastustellimuse kreeditarve kandega.
- Kui väljastatav tagasimakse rakendatakse tšekipõhisele maksetüübile, luuakse AR-makseviisi kasutav kliendi maksekanne, mis tuleb enne maksekande kliendikontole sisestamist käsitsi sisestada või printida. Tagasimaksetšekki saavad kasutajad töödelda kas Müügireskontro lehe **Kliendimaksete tööleht** või spetsiaalse Jaemüügi ja kaubanduse lehe **Tagasimaksetšeki töötlemine** kaudu.
- Kui väljastatav tagasimakse rakendatakse ettevõttesisesele kinkekaardile või kliendikaardile, luuakse tagastustellimuse arveldamisel tagasimaksekanne ja sisestatakse see kliendikontole. See arveldusetapp lisab ka tagasimakse summa tagasi kliendi ettevõttesiseselt jälgitud kinkekaardi saldole või püsikliendiprogrammi punktisaldole.
- Kui tagastamise müügitellimusega on lingitud funktsiooni **Klient** kasutav makseviis (nt kliendikonto), eiratakse makse töötlemisel krediidilimiidi valideerimisi. Selles kontekstis ei looda ega sisestata maksekannet. Kui tagastustellimusel kasutatakse kliendi maksetüüpi, toimib arve sisestamise protsessi raames loodav kreeditarve kanne kliendi krediidikandena ja näitab tagasimakset kliendi AR-saldole.

## <a name="advance-credit"></a>Eelnev kreedit

Kui kasutaja töötleb tagastustellimusi kõnekeskuse kasutajana kõnekeskuses, kus suvandi **Tellimuse lõpetamise lubamine** väärtuseks on määratud **Jah**, võib ilmneda eelnevalt kirjeldatud tagasimaksete sisestamise protsessi erand, kui tagastustellimust loov kõnekeskuse kasutaja määrab lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** suvandi **Ettemaks** väärtuseks **Jah**. Sel juhul tehakse tagasimakse kohe pärast seda, kui tagastustellimus on lehe **Tagastuse kokkuvõte** funktsiooni **Esita** abil esitatud. Süsteem loob tagastusväärtusele kohe ettemaksu kliendimakse kande, isegi kui tagastamise müügitellimus on veel arveldamata. Seda lähenemist saab kasutada olukorras, kus organisatsioon peab klienditeeninduse probleemide tõttu väljastama klientidele tagasimaksed ette ega nõua tagasimaksete väljastamiseks tagastatava varu kättesaamist.

## <a name="replacement-orders"></a>Asendustellimused

Kui tagastustellimus on väljastatud, saab kliendile uue müügitellimuse loomiseks kasutada funktsiooni **Asendustellimus**. Seda lähenemist saab kasutada vahetuste korral. Funktsioon **Asendustellimus** loob müügitellimuse uuele väljasaadetavale kaubale, kuid lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** olev ristviitelink lingib asendustellimuse, RMA ja tagastatud müügitellimuse.

Asendustellimuse maksete töötlemisel on organisatsioonidel kaks järgmist valikut.

- Teha kliendile tagastustellimuse eest algsel makseviisil põhinev tagasimakse ja koguda seejärel asendustellimuse jaoks eraldi makse. Selle võimaluse kasutamise korral pole lisakonfiguratsiooni vaja.
- Määrake lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** suvandi **Rakenda krediit** väärtuseks **Jah**. Sel juhul rakendatakse kliendi makseviis süstemaatiliselt nii tagastustellimusele kui ka asendustellimusele. See võimalus aitab vältida välise tagasimakse väljastamist. See aitab ka vältida makse töötlemist kandel. See võib olla kasulik olukorras, kus töödeldakse võrdse väärtusega vahetust ja organisatsioon eelistab kasutada asendustellimuse genereeritud arve maksmiseks tagastustellimuse arveldamisel loodud kreeditkannet. Kui suvandi **Rakenda krediit** väärtuseks on määratud **Jah**, peab organisatsioon kreeditarve pärast mõlema finantsdokumendi genereerimist asendustellimuse arvega käsitsi tasakaalustama.

Suvandi **Rakenda krediit** väärtus **Jah** rakendub ainult siis, kui tagastustellimus lingitakse asendustellimusega. Sel juhul määratakse tagastus- ja vahetustellimuse eest süstemaatiliselt tasumiseks kasutatav kliendi makseviis lehe **Kõnekeskuse parameetrid** vahekaardi **RMA/Tagastus** väljaga **Rakenda krediidi makseviis**. Sellel väljal saab valida funktsiooni **Klient** alla kuuluvat maksetüüpi.

> [!NOTE]
> Kui tagastustellimusel puudub lingitud asendustellimus, ei mõjuta suvandi **Rakenda krediit** väärtus **Jah** tagastustellimuse makseloogikat, sest see säte kehtib ainult asendustellimuste korral.

![Lehe Kõnekeskuse parameetrid vahekaardil RMA/Tagastus olev väli Rakenda krediidi makseviis.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Kui asendustellimusi loovad kasutajad kavatsevad kasutada suvandit **Rakenda krediit**, ei tohi nad tagastustellimusel käivitada funktsiooni **Vii lõpule** enne suvandi **Rakenda krediit** määramist väärtusele **Jah**. Pärast funktsiooni **Vii lõpule** käivitamist arvutatakse tagastusmakse ja see rakendatakse tagastamise müügitellimusele. Kui tagasimakse on juba arvutatud ja rakendatud, ei ole võimalik suvandi **Rakenda krediit** väärtuseks **Jah** määramisega käivitada tagasimakse ümberarvutust ja väljal **Rakenda krediidi makseviis** valitud makseviisi ei rakendata. Kui selles kontekstis tuleb kasutada suvandit **Rakenda krediit**, peab kasutaja kustutama asendustellimuse ja RMA ning seejärel alustama uuesti ja looma uue RMA. Sel korral peab kasutaja enne funktsiooni **Vii lõpule** käivitamist tagama, et suvandi **Rakenda krediit** väärtuseks oleks määratud **Jah**.

## <a name="payment-overrides-for-call-center-returns"></a>Kõnekeskuse tagastuste maksete alistamised

Kuigi kõnekeskuse loogika määrab süsteemselt tagasimakse makseviisi viisil, mida kirjeldatakse selles artiklis, võivad kasutajad mõnikord soovida neid makseid alistada. Näiteks võib kasutaja muuta või eemaldada olemasolevaid tagasimakseridu ja rakendada uusi makseridu. Süsteemi arvutatud tagasimakseid saavad muuta ainult kasutajad, kellel on vajalikud alistamisload. Neid õigusi saab konfigureerida Jaemüügi ja kaubanduse lehel **Lubade alistamine**. Tagasimakse alistamiseks peab kasutaja olema lingitud turberolliga, kus lehe **Lubade alistamine** suvandi **Luba alternatiivne makse** väärtuseks on määratud **Jah**.

![Suvand Luba alternatiivne makse lehel Lubade alistamine.](media/overridepermissions.png)

Teise võimalusena saab organisatsioon lehe **Kõnekeskuse parameetrid** vahekaardil **RMA/Tagastus** määrata suvandi **Luba makse alistamine** väärtuseks **Jah**. Sel juhul peab väljal **Turbe alistamise kood** olema valitud turbe alistamise kood. Turbe alistamise kood on tähtnumbriline kood, mis peab olema väliselt hallatav, kuna kasutajad ei saa seda pärast häälestamist Commerce'i peakontoris vaadata. Turbe alistamise koodi peaks organisatsioonis teadma ainult mõni võtmetähtsusega, usaldusväärne inimene. Kui suvandi **Luba makse alistamine** väärtuseks on määratud **Jah**, siis olukorras, kus mõni kasutaja, kellel ei ole vajalikke rollilubasid, proovib muuta tagastustellimuse makseviisi, pakutakse neile võimalust sisestada turbe alistamise kood. Kui nad seda ei tea või kui juht või ülevaataja ei saa seda nende eest lehele sisestada, ei saa nad tagastuse makseviisi alistada.

> [!NOTE]
> Kui turbe alistamise kood on kadunud või unustatud, peab organisatsioon selle lähtestama, määrates lehe **Kõnekeskuse parameetrid** vahekaardi **RMA/Tagastus** väljal **Turbe alistamise kood** uue turbe alistamise koodi.

![Makse alistamise parameetrid lehe Kõnekeskuse parameetrid vahekaardil RMA/Tagastus.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Enne krediitkaardi maksetüüpi kasutavate tagasimaksete tühistamise üritamist peaksid organisatsioonid kontrollima, kas nende krediitkaardiprotsessor lubab linkimata tagastusi. Paljud protsessorid nõuavad tagasimaksete sisestamist algsele kaardile. Kui üritatakse teha tagasimakset kaardile, millel ei ole eelnevaid hõiveid, võib see protsessoris põhjustada sisestamistõrkeid.

## <a name="additional-resources"></a>Lisaressursid

[Makseviisid kõnekeskustes](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]