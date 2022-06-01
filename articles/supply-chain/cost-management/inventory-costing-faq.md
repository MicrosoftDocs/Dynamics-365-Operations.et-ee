---
title: Varude kuluarvestuse KKK
description: See teema vastab mõnele korduma kippuvale küsimusele varude kuluarvestuse kohta Microsoftis Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809302"
---
# <a name="inventory-costing-faq"></a>Varude kuluarvestuse KKK

[!include [banner](../includes/banner.md)]

See teema vastab mõnele korduma kippuvale küsimusele varude kuluarvestuse kohta Microsoftis Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Lao sulgemine, korrigeerimine ja ümberarvutamine

### <a name="is-the-inventory-close-required"></a>Kas lao sulgemine on vajalik?

Kui plaanite kasutada varude arhiveerimise funktsiooni, on vaja lao sulgemist. Kui te ei plaani kasutada varude arhiveerimise funktsiooni, soovitame tungivalt, et käitaksite lao sulgemise, sõltumata kulumudelitest, mida kasutate.

### <a name="how-often-should-the-inventory-close-be-run"></a>Kui sageli tuleks lao sulgemist käitada?

Lao sulgemist tuleb käitada vähemalt üks kord pearaamatu perioodi kohta. Kui teie pearaamatus on näiteks seadistatud kalendrikuul põhinev rahanduskalender, tuleks lao sulgemine käivitada kord kuus.

### <a name="is-the-inventory-recalculation-required"></a>Kas varude ümberarvutamine on vajalik?

Ei, lao ümberarvutamine pole nõutav. Kui kasutate perioodilist kulumudelit, nt FIFO- (esimene sisse, esimesena välja), viimasena sisse, esimesena välja (LIFO) või kaalutud keskmist, peaksite hoolikalt järele mõtlema, kas käivitate lao ümberarvutamise. See võib pakkuda täpsemat kuluarvestust teie valitud heuristilises mudelis.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Kui sageli tuleks lao ümberarvutamine käivitada?

Kui plaanite lao ümberarvutamise käivitada, soovitame seda iga päev pakktöötlusena kasutada. Kui teie organisatsioon ei nõua perioodiliste kuluarvutusmudelite laoväärtuste sagedast aruandlust, võite kaaluda laoarvutuse käivitamist vähem.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Millal tuleks kasutada vaba kaubavaru korrigeerimist lehel Sulgemine ja korrigeerimised?

Vaba kaubavaru korrigeerimist saab käitada alles pärast lao sulgemise lõpetamist. Tavaliselt käitatakse seda kuupäeva pärast viimast sulgemist. Vaba korrigeeringuga saab korrigeerida ainult neid ladusid, mis on alates korrigeerimise käivitamiselt veel vabad.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Millal tuleks kasutada laokande korrigeerimist lehel Sulgemine ja korrigeerimised?

Enne lao sulgemise käivitamist peaksite kasutama laokande korrigeerimist. Tavaliselt kasutatakse seda vale sissetuleku parandamiseks. Te ei saa sisestada laokande korrigeerimist pärast lao sulgemise käivitamist ja kanne on tasakaalustatud.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Kas ostutellimuse tagastusi käsitletakse lao sulgemisel nagu muid väljaminekeid?

Jah. Ostutellimuse sissetulek on väljaminek, mis tasakaalustatakse kaubale valitud heuristilise mudeli sissetulekuga. Kui kasutate perioodilist kulumudelit, saate kasutada märkimist heuristilise kulu alistamiseks.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Mis toimub müügitellimuse tagastusega lao sulgemisel?

Lao sulgemise käivitamisel koheldakse müügitellimuse tagastust sissetulekuna varudesse. Väljaminek tasakaalustatakse laovarudega kaubale valitud heuristilise mudeli alusel.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Millist omahinda kasutatakse müügitellimuse tagastuses?

**Müügitellimusega** seotud tagastuse loomisel kopeeritakse välja Ühiku hind väärtus algsest müügitellimusest ja tagastamise omahinna välja väärtuseks seatakse algse laokande korrigeeritud omahind müügitellimuse real, **mis** tagastatakse. Kui seotud **laokande** väärtuse avatud valik *on seatud väärtusele Jah*, võib lao sulgemine põhjustada algse müügitellimuse väljaminekkulude uuendused. Selles **stsenaariumis** ei värskendata välja Omahinna tagastamine. Kuid kui sisestate tagastustellimuse saatelehe, kontrollib süsteem omahinda ja kasutab värskendatud kulu tagastatud laokandel.

Müügitellimusega seotud standardkuluüksuse tagastamiseks kasutab süsteem standardset kulu alates algse müügitellimuse ajast, isegi kui kauba jaoks on aktiivne uus standardne kulu.

Kui loote tagastuse, mis ei ole seotud müügitellimusega, seatakse välja Tagastamise omahind väärtuseks aktiivne kauba hind, **mis** teil on kaubale saidil, mille jaoks tagastustellimust loote. Kui teil ei ole kauba kuluversioonis aktiivset omahinda, on väärtus 0 (null). Kui jätate väärtuse väärtuseks 0 (null), saate hoiatuse, mis näitab, et tagastatud partii ID või tagastamise omahind on määramata.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Milline on lao sulgemise eeldatav jõudlus?

Paljud tegurid võivad mõjutada lao sulgemise jõudlust. Need tegurid hõlmavad kaupade koguarvu, perioodi kannete koguarvu, teie kasutate laomudeleid ja varude ja laohalduse parameetrites konfigureeritavate partiide abiliste arvu. Võite eeldada, et sulgemisel võib olla vähem kui mõned minutid või rohkem kui mitu tundi. Pole ühtegi konkreetset juhendit aja kohta, mis sulgemisel peaks käivituma. Peaksite määratlema oma mittefunktsioonilised ärinõuded lao sulgemise jõudluseks ja tegema partneriga koostööd, et määrata lao sulgemise protsessi käivitamine. Kui lao sulgemise protsessi jõudlus ootamatult väike, peaksite avama tugipileti.

## <a name="costing-sheet-and-indirect-costs"></a>Kululeht ja kaudsed kulud

### <a name="which-costing-models-support-the-costing-sheet"></a>Millised kulumudelid toetavad kuluarvestuse lehte?

Kuigi kululehte kasutatakse enamasti organisatsioonides, mis kasutavad standardset kuluarvestust, saate seda kasutada mis tahes kulumudeliga, mis on saadaval tarneahela halduses.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Kas ma soovin oma organisatsiooni erinevate osade jaoks mitut kululehte?

Ei. Teil võib olla ainult üks kululeht juriidilise isiku kohta.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Kas ma soovin iga saidi jaoks erinevaid kululehti?

Ei, teil ei saa iga saidi jaoks olla erinev kululeht. Saate igale juriidilisele isikule luua ainult ühe kululehe. Saate siiski konfigureerida kogusõlmed, kulugrupid või kaudse kulu sõlmed saidi kohta. See konfiguratsioon on käsitsi protsess ja teil tuleb säilitada hierarhia ja kauba määrangud kuluarvestuse lehel, kui ilmnevad organisatsioonilised või tööga seotud muudatused. Kui üks kaup on toodetud või ostetud rohkem kui ühel saidil, puudub mehhanism, mis võimaldab teil käsitleda kaupa iga saidi kululehel teisiti. Pange tähele, et kõigil kaudsete kulude koodidel on määr või lisatasu, mis on määratletud teie kuluversioonis. Teie määratletud kulud on alati saidiomased.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Kas ma soovin kuluarvestuse lehe versioone desaktiveerida ja aktiveerida?

Kuigi kuluarvestuse lehe jaoks ei hoita üksikasjalikku versiooniajalugu, saate teha muudatusi kuluarvestuse lehel ning seejärel valmis olemise korral salvestada ja kinnitada. Puudub mehhanism, mis võimaldab teil minna tagasi kuluarvestuse lehe vanemasse versiooni või vaadata kuluarvestuse lehel tehtud muudatusi. Kui te alustate muudatusi ja ei soovi nende kehtima hakkamist, saate lehe sulgeda muudatusi salvestamata ja kinnitamata. Teil palutakse muutustest loobuda.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Kas igale kaubale saab luua kaudseid kulusid?

Kuluarvestuslehel saate luua kaudseid **kulukoode, kus sõlme tüübi** *välja väärtuseks on seatud Lisatasu*, Määr *või* *Väljundi ühik*. Seejärel saate määratleda määra või lisatasu nii, et see oleks kaubakoodile omane. Lisage **kiirkaardil** **Määr** või Lisatasu rida ruudustikku. Seadke väljale **Kehtib väärtus** Tabel *ja* väljale **Seos** määratud kaubakood.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Kas ma saab luua kaudse kulu, mis ei ole seotud konkreetse kaubaga?

Jah. Saate luua kaudse kulu koodi, kus sõlme **tüübi välja väärtuseks** on seatud Väljundüksusel *põhinev*. Seejärel saate seadistada välja Alamtüüp **väärtusele** *Kogus,* *Kaal* või Maht *, et määrata toodetava kauba kogus, kaal või maht.* Kiirkaardil Määr **määratud** määr rakendatakse valitud alamtüübile. Näiteks seate välja **Alamtüüp** väärtuseks *Kogus* **·** *ja Määr väärtuseks 1,00 USD* ning seejärel loote tootmis- või partiitellimuse kogusele 10. Sel juhul lisatakse valmis kaubale lisatav kaudne kulu 10.00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Kas ma saaks kasutada kuluarvestuslehte oma tootmiskulude tükeldamiseks tundide ja materjalide alusel?

Jah. Kululehel **saate** luua kogusõlmi, et eraldada kulud mis tahes valitud grupeerimise alusel. Näiteks saate luua ühe **Kogusõlme** *nimega Tunnid ja* teise nimega *Materjalid*. **Lisage** tundide sõlme all kõik tundidega seotud koodigrupid. **Lisage** sõlm Materjalid iga materjalidega seotud kulugrupp.

## <a name="dimension-groups"></a>Dimensioonigrupid

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Kas ma hallata kulusid partii- või seerianumbri tasemel?

Jah, kui kasutate perioodilist kulumudelit, nagu FIFO, LIFO, LIFO kuupäev, kaalutud keskmine või kaalutud keskmine kuupäev, **·** **·** **saate** lubada suvandi Finantsiline laovaru jälgimisdimensiooni grupi partii- või seerianumbri dimensioonile, et jälgida kulusid üksikasjalikul tasemel.

### <a name="can-i-manage-costs-at-the-location-level"></a>Kas ma saab hallata kulusid asukoha tasemel?

Ei, te ei saa varude dimensiooni grupi **asukohadimensiooni** jaoks **lubada** suvandit Finantsiline laovaru. Kui teie organisatsioon peab jälgima kulusid üksikasjalikumal tasemel, kaaluge, kas saate luua virtuaalseid ladusid **ja** **seejärel** valige laoala dimensiooni jaoks suvand Finantsiline laovaru oma laoala dimensiooni grupis.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Kas lubada laoala dimensiooni grupile suvand Kasuta laohaldusprotsesse?

Kui te arvate, et te soovite ehk kasutada täpsemaid laohalduse funktsioone tulevikus, peaksite lubama suvandi Kasuta **laohaldusprotsesse**. Pärast laoala dimensiooni grupi salvestamist ei saa te enam muuta sätte Kasuta laohaldusprotsesse **selle** jaoks. Kui otsustate hiljem laohaldusprotsesse kasutada, peate looma uue lao, kus see valik on lubatud. Pole automaatset protsessi, mida saate kasutada kõikide varude teisaldamiseks ühest laost teise lattu või seotud konfiguratsioonide kopeerimiseks uude lattu.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Kas lubada laoala dimensioonigrupi puhul kasutada laohaldusprotsesse isegi siis, kui ma ei plaani täpsemat ladustamist kasutada?

Jah, isegi kui te ei plaani täpsemaid laohalduse funktsioone kasutada, **saate laoala dimensioonigrupile** lubada suvandi Kasuta laohaldusprotsesse. Kannete loomiseks ja töötlemiseks peate lõpule viima minimaalse konfiguratsiooni, nt reserveerimise hierarhiad ja ühiku seeriagrupid. Täpsema ladustamise sätteid eiratakse tavaliselt komplekteerimislehtede, saatelehtede ja toote sissetulekute käsitsi töötlemise korral (nt müügitellimuse ja ostutellimuse lehtedel).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Millal peaks laoala või jälgimisdimensiooni grupi jaoks lubama füüsilise lao valiku?

Peate lubama laoala **- ja** jälgimisdimensioonigruppide jaoks suvandi Füüsiline ladu, kui peate hoidma selle dimensiooni põhjal üksikasjalikke laokirjeid. Tavaliselt jälgitakse füüsiliselt ka kõiki aktiivseid dimensioone. Seetõttu jälgib valitud dimensioon lao sissetulekut, väljaminek või liikumist. Kui dimensioon ei ole kohustuslik (nt litsentsiplaat), **·** **saate** lubada lubatud tühja sissetuleku ja määramata väljamineku valikud, et lubada kasutajatel varusid vastu võtta, väljastada või teisaldada isegi siis, kui dimensioon on määramata.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Millal tuleks laoala või jälgimisdimensiooni grupi jaoks lubada finantsiline laovaru?

Peate lubama finantsilise **laoseisu** suvandi ladustamis- ja jälgimisdimensioonigruppidele, kui peate hoidma selle dimensiooni põhjal üksikasjalikke finantskirjeid. **Saidi** dimensioone jälgitakse alati finantsiliselt, samas kui teised dimensioonid on finantsilise jälgimise jaoks valikulised. Kui kasutate perioodilist kulumudelit, nagu FIFO, LIFO või kaalutud keskmist, **näitab** dimensiooni finantsilise lao suvandi lubamine, et teete tasakaalustusi ainult juhul, kui sissetulekul ja väljaminekul on samad dimensiooniväärtused. Näiteks **kui** **lubate** varude dimensiooni jaoks suvandi Finantsladu, on teil igas laos erinevad kulud ning erinevate ladude sissetulekuid ja väljamineki ei saa tasakaalustada.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Kas pärast kannete olemasolu saab toote-, laoala- või jälgimisdimensioonigruppi muuta?

Pärast kauba mudeligrupi loomist saate muuta laovarude plaani sätet dimensioonide kaupa, **ostuhindade** jaoks ja müügihindade jaoks, **·** **kui** kauba mudeligrupi dimensiooni jaoks on valitud märkeruut Aktiivne.**·** Muid muudatusi ei ole lubatud. Näiteks ei saa te lubada ega keelata **suvandeid Aktiivne**, **Tühi väljaminek** lubatud, **Tühi** sissetulek lubatud, **Füüsiline** ladu ja Finantsiline **laovaru**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Kas ma soovin väljastatud toote toote-, laoala- või jälgimisdimensioonigruppi muuta?

Kui toote vaba kaubavaru on 0 (null) **·** *ja* valiku Avatud väärtuse valik on kõigi laokannete puhul seatud väärtusele Ei, saate laoala ja jälgimisdimensioonigruppe muuta vabastatud tootmise lehel. Tootedimensiooni gruppi ei saa pärast kirje loomist muuta.

## <a name="item-model-groups"></a>Kauba mudeligrupid

### <a name="when-should-i-enable-the-stocked-product-option"></a>Millal tuleks lubada ladustatud toote suvand?

Peate lubama ladustatava **toote** suvandi mis tahes kaubale, mida teie laos jälgitakse. Kui see suvand on lubatud, säilitatakse üksikasjalikud laokanded, mis jälgivad kauba sissetulekut ja väljaminek. See valik on tavaliselt lubatud mis tahes materiaalse kauba puhul, mida oma laos hoiate, näiteks. Samuti peaksite lubama selle suvandi, kui plaanite lisada mitte materiaalse kauba, nt teenusekauba oma kooslustele või valemitele. Kui te ei **luba** valikut Ladustatav toode, ei jälgita varude alammoodulis ühtegi laotehingut ja kaupade kulu läheb tavaliselt pearaamatusse. Seda valikut kasutatakse sageli näiteks ostu varude või teenuste puhul, mida ei ole teie kooslustes või valemites kaasatud.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Millal tuleks lubada suvand Sisesta füüsiline ladu?

Suvand **Sisesta füüsilised** varud on tavaliselt lubatud, kui **suvand Ladustav** toode on lubatud. Kui lubate selle suvandi, jälgib süsteem laokandel kauba füüsilist uuendamist. Seda valikut kasutatakse seoses ostureskontro, müügireskontro ja tootmise juhtimise parameetritega, mis määravad, kas füüsiline värskendus peaks looma kande. Tavaliselt lubate selle suvandi, kui soovite pearaamatut alati uuendada, kui lao füüsiliselt uuendate. Kui tarneahela haldus ei ole finantside kirjesüsteem, võiksite selle suvandi keelata.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Millal peaks lubama suvandi Rahaliste varude sisestamine?

Suvand **Sisesta finantsiline** laovaru on tavaliselt lubatud, kui **suvand Ladustav** toode on lubatud. Seda valikut kasutatakse koos parameetritega Ostureskontros, Müügireskontros ja Tootmise juhtimises, mis määravad, et finantsvärskendus peaks looma kande. Tavaliselt lubate selle suvandi, kui soovite pearaamatut uuendada alati, kui lao finantsiliselt uuendate (nt müügitellimuste ja ostutellimuste arveldamine või tootmistellimuse sulgemine). Kui tarneahela haldus ei ole finantside kirjesüsteem, võiksite selle suvandi keelata.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Millal tuleks lubada suvand Sisesta edasilükatud tulu kontole müügi tarnel?

Kasutage suvandit **Edasilükatud tulu kontole sisestamisel müügitarnel**, et näidata, kas soovite müügitellimuse saatelehe sisestamisel pearaamatust tulu ära tunda. Seda valikut kasutatakse tavaliselt siis, kui müügitellimuse saatelehe ja arve vahel on pikk viivitus või kui kõigi selle perioodi müügitellimuste arveldamine ei ole võimalik. Tavaliselt keelate selle suvandi, kui sisestate müügitellimuse arved kohe pärast saatelehe sisestamist. Sel viisil väldite lisa pearaamatu sisestuste genereerimist, mis tühistatakse müügitellimuse arveldamisel kohe.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Millal tuleks lubada toote sissetulekul viitvõlakohustus?

Enamikus organisatsioonides soovite lubada kumuleeritud kohustuse toote sissetulekul kõigi kauba mudeligruppide puhul, sõltumata sellest, **kas teil on** ladustatud toode või mittelaokaupa salvestatud toode. Seda valikut kasutatakse viitvõla sisestamiseks pearaamatusse toote sissetuleku hinna alusel. Kuna tavaliselt on ostutellimuse toote sissetuleku sisestamise ja arve sisestamise vahel viivitus, peab enamik organisatsioone tuvastama bilansilehe kohustuse, et need vastaksid kohalikele määrustele, nt Üldaksessi raamatupidamistavadele (GAAP). Kui tarneahela haldus ei ole finantside kirjesüsteem, võiksite selle suvandi keelata. Kui teie organisatsioon kasutab ostutellimuste hankekategooriaid, saate kontrollida viitvõla nõuet, **lubades suvandi Kogunev ostukulu** **sissetulekul kategooria poliitika reegli jaoks ostupoliitika lehel**.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Kuidas takistada kasutajat ostutellimuse toote sissetuleku sisestamist, kui sissetuleku registreerimist pole veel sisestatud?

Saate takistada kasutajat ostutellimuse toote sissetuleku **sisestamisel**, kui ostutellimuse registreerimist pole veel toimunud, lubades kauba mudeligrupi jaoks suvandi Registreerimisnõuded. Seda valikut kasutatakse tavaliselt organisatsioonides, mis kasutavad kaheastmelise vastuvõtuprotsessi või stsenaariumite puhul, kus peate registreerima partii- või seerianumbri, näiteks kaupade puhul, mida saate. Registreerimisnõude **valik** kehtib kõigile *kauba* lao sissetulekutele, mitte ainult ostutellimustele. Näiteks rakendatakse seda positiivse kogusega laotöölehele ja tootmistellimuse lõpetatuna kinnitatud töölehele.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Kuidas takistada kasutajat ostutellimuse arvet sisestamast, kui toote sissetulekut pole veel sisestatud?

Saate takistada kasutajat ostutellimuse tootearve sisestamisel, kui ostutellimuse toote sissetulekut pole veel **toimunud, lubades kauba** mudeligrupi jaoks valiku Vastuvõtunõuded. Seda valikut kasutatakse tavaliselt organisatsioonides, mis nõuavad pearaamatus viitvõlgade füüsilist tuvastamist. Valik **Vastuvõtunõue** kehtib kauba *kõigile* lao sissetulekutele, mitte ainult ostutellimustele. Näiteks rakendatakse seda positiivse kogusega laotöölehele ja tootmistellimuse lõpetatuna kinnitatud töölehele. Kui teie organisatsioon kasutab ostutellimustel hankekategooriaid, saate kontrollida sissetuleku nõuet, **·** **lubades suvandi Vastuvõtunõuded kategooria poliitika reegli jaoks ostupoliitika lehel.**

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Kuidas vältida kasutajalt müügitellimuse saatelehe sisestamist, kui müügitellimuste komplekteerimislehte pole veel sisestatud?

Saate takistada kasutajat müügitellimuse **saatelehe** või arve sisestamist, kui müügitellimuse komplekteerimislehte pole veel toimunud, lubades kauba mudeligrupile valiku Komplekteerimisnõuded. Seda valikut kasutatakse tavaliselt organisatsioonides, mis sooritavad laos füüsilise komplekteerimise protsessi (nt kasutades komplekteerimiseks lao mobiilset seadet). Valik **Komplekteerimisnõue** kehtib kauba kõigile *väljaminek* väljaminek, mitte ainult müügitellimustele. Näiteks rakendatakse seda laotöölehele, mille kogus on negatiivne, ja tootmistellimuse komplekteerimislehe töölehel.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Kuidas takistada kasutajat müügitellimuse arvet sisestamast, kui müügitellimuse saatelehte pole veel sisestatud?

Saate takistada kasutajat müügitellimuse **arve** sisestamist, kui müügitellimuse saatelehte pole veel toimunud, lubades kauba mudeligrupi jaoks valiku Mahaarvamise nõuded. Seda valikut kasutatakse tavaliselt organisatsioonides, mis sooritavad laos füüsilise pakkimisprotsessi (nt kasutades laohalduse mobiilirakendust pakkimiseks või luues dokumendi, mis kaasatakse saadetavatele kaupadele). Mahaarvamise **vajaduse valik** kehtib kauba kõigile *lao* väljaminek, mitte ainult müügitellimustele. Näiteks rakendatakse seda laotöölehele, mille kogus on negatiivne, ja tootmistellimuse komplekteerimislehe töölehel.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Kas saab vältida registreeritud kaupade müümist?

Kui kaup on teie laos tarneahela halduses registreeritud, on kogus füüsiliselt süsteemis väljastatud. Kui *kaubad*, mis on registreeritud, kuid mida pole veel vastuvõetud, ei tohiks müügitellimustele või tootmistellimustele väljastada, ei tohiks olla saadaval, nt kaaluge äriprotsessi haldamiseks varude olekut, varude blokeerimist, kvaliteettellimusi, vahelaoordereid või reserveeringu funktsioone.

## <a name="production-costing"></a>Tootmise kuluarvutus

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Kas toormaterjalide puhul saab kasutada üht kulumudelit ja erinevat lõpetatud kaupade kulumudelit?

Jah, saate iga kauba puhul kasutada erinevaid kulumudeleid. Tootjatel ei ole vaja kasutada toormaterjalide puhul perioodilist kulumudelit ning pooltoodete ja valmiskaupade standardkulusid.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Kuidas ma juhin üldkulusid masinakuludest?

Selleks, et juhtida üldkulusid oma masinakuludest, peate looma igale masinale ressursse ja ressursigruppe vastavalt ärinõuetele. Iga ressurssi või ressursigruppi saab määrata kulukategooriatele masina kulude juhtimiseks. Iga kulukategooria saab siduda kulugrupiga ja iga kulugruppi saab kasutada kaudsete kulude arvutamise alusena kululehel.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Kuidas ma soovin ära tunda kuluarvestustabelis energiatarbimisega (nt vee, energia või gaasi tarbimine) seotud kulu?

Üldiselt saate ära tunda energiatarbimisega seotud kulusid ühel kahest viisist:

- Looge oma koosluses või valemis rida. Tavaliselt luuakse see rida teenusüksusena ja te saate määrata mõõtühiku, mida te toodetava koguse suhtes tarbite. Sel viisil saab kasutaja tootmisprotsessi käigus tarbida erinevat kogust. Saate kaubad tarbida automaatselt vastavalt väärtusele, mille **valite väljal Uhtmise** põhimõte.
- Looge oma kululehel kaudne kulu. Tavaliselt kasutatakse seda lähenemist, et eraldada oma energiatarbimise kogukulu läbi oma tootmisprotsessi. Saate kasutada kulugruppi ja absorbtsiooni alust, et näiteks oma protsessi materjalidel või tööl põhinevat tarbimist vähendada.

Parim valik tuleks valida vastavalt oma aruandlusele, vastavusseviimisele ja tegevusnõuetele.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Kas ma soovin koosluses või valemis ressursi üksikasju hõivata?

Ressursi üksikasju saab hõivata ainult protsessi operatsioonis. Kuigi saate luua teenusüksuse ressursi esindamiseks ja määrata kulu lõpetatud kauba kulukalkulatsiooni suurendamiseks, ei soovita me tavaliselt seda lähenemist. Soovitame selle asemel luua lihtsa protsessi, kus on üks rida ressursi kulude jälgimiseks, ja konfigureerida operatsioon nii, et see tarbitakse automaatselt kas tootmistellimuse alguses või lõpus.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Kas ma soovin vaadata arvutuse üksikasju, kui kulu sisestatakse käsitsi?

Ei. Kui sisestate hinna käsitsi kauba **hinnalehele**, ei ole **nupud Vaata arvutuse üksikasju** **ja Aruande** arvutamise üksikasju saadaval. **Kui** valite käsitsi sisestatud omahinnale kulugrupi alusel ümberarvestuse kulugrupi järgi, kuvatakse summeeritud rida ja kõik kulud takse ümber lõpetatud kaubale.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Kas süsteem arvutab kulu käsitsi sisestamisel tootmistellimuse hälbeid?

Jah, süsteem arvutab hälbeid, kui sisestate standardkulu käsitsi. Kuid kui sisestate selle arvutamise asemel käsitsi standardkulu, loetakse tootmistellimuse kogu materjali, protsessi ja kaudse kulu tarbimised asenduse hälbeks. Kui on lisahälbeid, nagu lisamaterjalide tarbimine või tööjõud, kirjendatakse need ka tootmiskoosluse hälvetena. Seetõttu soovitame tungivalt, et käivitaksite alati kalkulatsiooni kaupadele, mille kooslus, protsess või kaudsed kulud on olemas.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Kuidas ma saaks hälbeid alltootmise tellimusest üle kanda ematootmistellimusele?

Kui kasutate perioodilist kulumudelit, nagu FIFO, LIFO või kaalutud keskmist, tuvastatakse alamtootmise kulud kaupadele valitud heuristilises mudelis. Kui vajate tegelikku kuluarvestust, kaaluge märkimise põhimõtte kasutamist, et näidata, milline alamtootmine väljastatakse ematootmistellimusele. Teise võimalusena kaaluge näiteks **jälgimisdimensiooni** grupis **partii** **või** seerianumbri dimensiooni jaoks suvandi Finantsiline laovaru kasutamist.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Kuidas tarbimist mõjutab tarbimist tarbimist tarbimist?

Koosluse, valemi või protsessirea uhtmispõhimõte kontrollib kauba või töö tarbimiseks kasutatavat ajastust ja tehnikat. Kui valite *alguse*, tarbitakse kaup või tööjõud tootmistellimuse käivitamisel automaatselt. Kui valite *Lõpeta*, tarbitakse kaup või tööjõud automaatselt, kui teatate tootmistellimuse lõpetamisest. Kui valite *Käsitsi*, peab kasutaja käsitsi materjale komplekt võtma või registreerima aja töös või protsessikaardi töölehel. Kooslustel ja valemitel on ka *asukohas saadaval suvand*. Selle valiku puhul tarbitakse kaubad automaatselt pärast kaupade üle üle lülitumist tootmispinna asukohale.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Kuidas käivitada kuluarvutusi, kui mul on mitmetasemelised kooslusi või valemeid?

Üldiselt soovitame teil alustada kalkulatsiooniks kõige madalamal koosluste või valemite tasemel. Filtrite lihtsustamiseks kuluarvutuste hulgiarvutuste puhul saate kasutada kalkulatsioonigruppe toodete eraldamist hõlbustamiseks. Soovitame käivitada kooslusetasemete *perioodilise* töö uuesti arvutada enne, kui alustate kuluarvutuste hulgiarvutust. Iga organisatsioon peaks arvestama toodete segamisega ja määratlema strateegia, mis vastab teie toote ja koosluse või valemi struktuuri konkreetsetele vajadustele.

## <a name="transfer-order-costing"></a>Üleviimistellimuse kuluarvestus

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Kas on olemas viis eraldada veoraha üleviimistellimuse kulule?

Lisakulude lisamiseks saate üleviimistellimusele tasusid lisada. Lisakulude kood määratleb lisakulu deebeti ja kreediti. Esmalt peate looma lisakulude koodid moodulis **Varud**. Tasu lisamiseks üleviimistellimusele valige tasud **üleviimistellimuse** real, millele soovite tasu lisada.

## <a name="variances"></a>Hälbed

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Kas hälbeid saab saidi või lao alusel erinevalt käsitleda?

Hälbekontosid ei saa saidi alusel konfigureerida. Kui kasutate väljastatud toote puhul standardset kuluarvestust, saate valida põhikonto, mida kasutatakse standardsete omahinna hälbe sisestuste puhul **sisestuslehel**. Saate konfigureerida kontod ühe kauba, kaubagrupi või kõigi kaupade jaoks. Samuti saate konfigureerida ühe kulugrupi, kulugruppide grupi või kõik kulugrupid.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Kas ma soovin valuuta vahetuskursside tulemiks tingitud hälbeid teist tüüpi hälvetest eraldada?

Kui hälve on valuuta vahetuskursi erinevuse tulemus ostutellimuse hinna ja kauba standardkulu vahel, ei ole võimalik vahetuskursi erinevust muudest hälvetest eraldada.

## <a name="reporting"></a>Aruandlus

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Mitu laoväärtuse aruande konfiguratsiooni saab luua ja kasutada?

Puudub piirang laoväärtuse aruande konfiguratsioonide arvuga, mida saate luua. Peaksite hindama oma aruandlusnõudeid ja looma nendele nõuetele vastamiseks vajalik konfiguratsioonide arvu. Aruande või aruande ladustamisvaliku käivitamiseks on vaja vähemalt ühte laoväärtuse aruande konfiguratsiooni.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Kas ma soovin varude väärtuse aruannet kasutada kauba maksumuse analüüsimiseks igas laos?

Jah. Varude väärtuse aruande **konfiguratsioonis** **saate** iga laodimensiooni **jaoks** lubada suvandi Kuva või Kokku. Kuid aruandes kuvatakse väärtused ainult nende dimensioonide puhul, kus laoala **dimensioonigrupi** jaoks on lubatud suvand Finantsiline laovaru. Teiste dimensioonide puhul kuvatakse tühjad veerud. Lisateavet vt laoväärtuse aruande [näidetest ja loogikast](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Kuidas ma saaks vaadata varude kogust konkreetsel kuupäeval koos kaalutud keskmisega?

Saate kasutada varude **aegumisaruannet**, mis sisaldab keskmise **ühiku hinna** veergu, mis näitab lao väärtust konkreetse kuupäeva alusel. Lisateavet vt varude aegumisaruande [näidetest ja loogikast](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Kuidas vaadata, milliseid sissetulekukandeid väljaminev kandega tasakaalustatakse?

Laokande **tasakaalustusi** **·** **·** **·** **saate** vaadata, kui valite laokande või laokande üksikasjade lehe vahekaardil Varud suvandi Tasakaalustused või Kulu sirvija. Kui valite sissetuleku kandega seotud väljaminek vaatamiseks, ei näita kulu sirvija üksikasju. Üksikasjad kuvatakse ainult siis, kui valite väljaminek kande.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Kuidas näitab laoväärtuse aruanne kaupu, mille füüsiline kogus on positiivne ja negatiivne rahaline väärtus?

Laoväärtuse aruanne eraldab füüsilised ja finantssummad ning kogused eraldi veergudesse. Aruandes kuvatavad väärtused on aruande käivitamisel valitud kuupäevavahemikus. Kuvatava summeerimise tase sõltub teie valitud sätetest. Kui kaubal on kandeid, mis on füüsiliselt vastuvõetud ja finantsiliselt väljastatud, summeeritakse kogused ja väärtused iseseisvalt. Kui valisite üksikasjade taseme kuvamise kannetena, näidatakse iga sissetuleku ja väljamineu ridu eraldi ning kuvatakse vastavalt füüsilised ja rahalised kogused ja summad. Lisateavet vt laoväärtuse aruande [näidetest ja loogikast](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Mis on laoala ja jälgimisdimensioonigruppide mõju varude väärtuse aruandes?

Kui lubate **laoala** või jälgimisdimensiooni grupi dimensiooni jaoks suvandi Finantsväärtus, **·** **saate** varude väärtuse aruande konfiguratsioonis dimensiooni jaoks valida suvandi Kuva või Kokku. Kui valite suvandi **Kuva** või **Kokku** dimensioonile, **kus** suvand Rahaline väärtus pole valitud, on aruande väljundis veerg tühi. **·** **·** **Kui** olete laoala või jälgimisdimensiooni grupi dimensiooni jaoks lubanud suvandi Finantsväärtus ja te ei vali varude väärtuse aruande konfiguratsioonis suvandit Kuva või Kokku, võtab süsteem kokku valitud dimensioonide väärtused, kus neid finantsiliselt jälgitakse.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Kas ma saab kuluarvestuseks Power BI manustatud aruandeid kohandada?

Jah, kasutajad, kellel on õiged turvaõigused, saavad uuendada aruande kujunduse lõuendit Power BI mis tahes tarneahela halduse manustatud aruandele. Lisateavet vt manustatud aruannete [kohandamisest analüütilistes tööruumides](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Kus ma saaks hälbe analüüsi väljavõtet vaadata?

Pääsete hälbe analüüsi väljavõttele **\>\> juurde, kui kasutate kuluhalduse päringuid ja aruandeid Laoarvestus –** **analüüsiaruanded või kuluhalduse \>\> päringud ja aruanded Tootmise raamatupidamine – analüüsiaruanded.** Mõlemad valikud avavad sama aruande ja aruandel on sama käitumine.

## <a name="item-prices-and-default-costs"></a>Kauba hinnad ja vaikekulud

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Kas iga tootevariandi puhul saab kulu hallata?

Jah. Saate lubada suvandi **Kasuta omahinda variandi alusel** lehel **·** **Väljastatud** toote kulu kiirkaardi haldamine, et lubada hinnakujundus tootevariandi alusel. (See suvand on saadaval ainult tooteetelgide puhul.) Seejärel saate kauba **hinnalehel** (**·** **mille** saate avada kas kuluversiooni leheküljelt või leheküljelt Väljastatud toode), **·** **valida dimensioonide kuva, et määrata, kas soovite kuvada dimensiooni Konfiguratsioon**, **Suurus**,**·** **Värv või Stiil.** Seadistuse salvestamiseks ja valitud dimensioonide kasutamiseks iga kord, kui avate selle lehe, **lubage suvand Salvesta** seadistus ja seejärel valige **OK**. Saate sisestada dimensioone ainult nende kaupade puhul, mille dimensioonid on tootedimensioonigrupis aktiivsed.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Kas ma soovin iga lao kulu säilitada?

Ei, te ei saa kauba hinda lao järgi säilitada. Saate siiski hallata ostuhindade või müügihindade kaubandusleppeid lao järgi. Kõigepealt valige lehel **Laoala dimensiooni grupp** **dimensiooni jaoks** suvand Ostuhindade jaoks või **Müügihindade jaoks**. Seejärel, kui loote kaubanduslelepingu töölehe ja avate dimensioonide read, valige Varude **kuvamise dimensioonid, et valida, \> milline dimensioon tuleks ruudustikus** kuvada. Seadistuse salvestamiseks ja valitud dimensioonide kasutamiseks iga kord, kui avate selle lehe, **lubage suvand Salvesta** seadistus ja seejärel valige **OK**. Saate sisestada dimensioone ainult nende kaupade puhul, mille dimensioonid on tootedimensioonigrupis aktiivsed.

### <a name="what-are-price-charges"></a>Millised on hinnakulud?

Hinnakulud on viis kauba hinnale või kaubanduslelepingule fikseeritud summa lisamiseks. Kui sisestate summa väljale **Hinnakulud**, saate ka sisestada väärtuse väljale Kulude **kogus**. Hinnakulud amortiseeritakse teie määratud kulude kogusest rohkem. Kui soovite **kauba hinnakulusid kaasata** kauba ühiku hinda, lubage valik Lisa ühiku hinnas. See valik on standardkulu puhul alati lubatud.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Kuidas tuleks konfigureerida hinnad kaupadele, mis on hangitud mitmes valuutas?

Kui sisestate **vaikehinna** **väljale** Ostuhind lehel Väljastatud toode, eeldatakse, et olete selle juriidilise isiku pearaamatu arvestusvaluutas, kus olete. Kui sisestate ostuhinna **kuluversiooni, kus välja Hinna** *tüüp* väärtuseks on seatud Ost, eeldatakse, et hind on teie juriidilise isiku arvestusvaluutas. Kui loote ostutellimuse hankijale, kellel on erinev valuuta, **teisendab süsteem valuuta automaatselt arvestusvaluutast kandevaluutasse, kasutades pearaamatu väljal Arvestusvaluuta** vahetuskursi tüüp määratud kurssi.

Kaubanduslelepingu töölehe loomisel saate määrata valuuta, millega igal real hinda väljendate. Kaubandusleppeid saate luua mitme valuuta, kindlate hankijate ja paljude teiste tegurite kombinatsioonide jaoks. Kui loote ostutellimuse, kus kaubandusle leping on valitud valuuta kohta olemas, kasutab süsteem kaubanduslelepingut, milles on vastav valuuta. Selliste kannete sisestamisel nagu toote sissetulekud või arved teisendatakse summa pearaamatu arvestusvaluutasse pearaamatus määratud arvestusvaluuta vahetuskursi abil.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Kuidas tuleks konfigureerida kulud kaupadele, mis on hangitud mitmes valuutas?

Kulusid ei saa konfigureerida rohkem kui ühes valuutas. Kulud, **mille** määrate kauba hinnale või vaikekuludele, mille sisestate väljale Kulu haldamine kiirkaardis Väljastatud toode, väljendatakse **·** **alati** teie valitud juriidilise isiku pearaamatu arvestusvaluutas.

Kui teie organisatsioon kasutab standardset kuluarvestust, peaksite määratlema kulude määratlemise strateegia mitme valuuta puhul. Samuti peaksite määratlema protsessi kulude regulaarseks uuendamiseks, et aidata vähendada sisestatud hälvete arvu.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Kas müügihindade arvutamiseks saab kasutada lehe Kulugrupp sätet Kasum?

Jah, saate kasutada lehe **Kulugrupp** sätet **Kasum**, et lisada protsent, kui müügihinnad arvutatakse kuluarvutust kasutades. Lisateavet vt koosluse [kalkulatsioonide kohta](bom-calculations.md).

## <a name="marking"></a>Märkimine

### <a name="how-does-marking-affect-periodic-costing-models"></a>Kuidas mõjutab märkimine perioodilisi kulumudeleid?

Kui kasutate perioodilist kulumudelit, nagu FIFO, LIFO või kaalutud keskmist ja olete märkinud sissetulekukande väljaminek kande vastu, eiratakse kauba heuristikmudelit lao sulgemise protsessi ajal. Selle asemel kasutab süsteem sissetuleku tegelikku kulu väljaminek maksumuses.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Mis toimub lao sulgemisel, kui märkimist kasutatakse?

Sissetulekute ja väljaminekde märkimisel tasakaalustab lao sulgemine koos märgitud kanded. Kui märkimist kasutatakse tasakaalustuse loomiseks, **seatakse** tasakaalustuse lehe **välja** Põhimõte väärtuseks *Märkimine*. Kui kanne on märgitud enne selle füüsilist või finantsiliselt värskendamist, kasutab väljaminek jooksva keskmise kulu asemel märgitud sissetuleku kulu. Kui kanded märgitakse pärast finantsi värskendamist, korrigeerib lao sulgemise ja korrigeerimise protsess väljamineu kulu nii, et need vastaksid sissetuleku kulule.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Kas ma soovin kanded käsitsi märkida, kui ma kasutan standardset omahinna või liikuvat keskmist?

Ei, te ei saa käsitsi märkida sissetulekuid ja väljaminek, kui kasutate standardset kuluarvestust või liikuvat keskmist. Kui kanded (nt otsetarned või kontsernisisesed tellimused) märgitakse automaatselt, jääb märkimiskirje alles ja see käitub kui raske reserveering. Kuid kui kasutate standardset kuluarvestust või liikuvat keskmist, ei mõjuta kirjete märkimine kaupade kulu.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Kuidas mõjutab märkimine kasumi- ja kahjumiaruannet?

Kui märgite väljaminek kande sissetuleku vastu, kattub väljaminek valitud sissetulekuga. Kui sisestate väljaminek füüsiliselt ja finantsiliselt, **mõjutab sisestamine müüdud kaupade omahinda,** **tarnitud** ja müüdud kaupade omahinda, lao sisestusreeglites määratud arveldatud kontosid. Kui kanne märgitakse pärast füüsilist või finantsilist värskendamist, loob lao sulgemis *- ja korrigeerimisprotsess korrigeerimise,* **mille vastav kanne kohandab müüdud kaupade omahind, arveldatud konto ja vastaskonto kontole** **, mille määrate kaupade hinnale arveldatud** (ladu).

### <a name="how-does-marking-affect-master-planning"></a>Kuidas märgistus koondplaneerimist mõjutab?

Koondplaneerimise **parameetrite** lehe standardvärskenduse **vahekaart** sisaldab välja nimega Uuenda **märkimine**. Teie valitud varianti kasutatakse siis, kui kinnitate koondplaneerimise loodud plaanitud tellimuse. Valikud on järgmised:

- *Ei* – süsteem ei märgi midagi.
- *Standard* – süsteem märgib sissetulekud väljamineke vastu sidumise alusel. Vajaduse tellimus märgitakse täitmise tellimuse suhtes. Kui täitmisele jääb teatud kogus alles, siis täitmistellimust ei märgita.
- *Laiendatud* – süsteem märgib nii vajaduse tellimusi kui ka täitmistellimusi, sõltumata sellest, kas täitmise tellimusel jääb mõni kogus avatuks.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negatiivne laovaru

### <a name="when-should-i-allow-physical-negative-inventory"></a>Millal tuleks lubada füüsilist negatiivset laovaru?

Üldiselt ei ole soovitatav lubada füüsilist negatiivset laovaru, kuna laos ei saa olla alla 0 (null) materiaalset kaupa. Mõne majandusharu ja äristsenaariumi äriprotsessid võivad siiski piirata operatsioone, mis nõuavad, et laovarud tohiks füüsiliselt negatiivseks minna. Näiteks ei pruugi jaemüüjad soovida kassaaparaati toodud kauba müüki takistada, isegi kui süsteem näitab, et kaupu pole saadaval. Protsessi tootjad pakuvad teist näidet. Nende tootjate puhul võib tarbitav summa ületada valemis soovitatava koguse. Teise võimalusena võib tarbimist täpse asemel hinnata, nii et tarbimine ületab konkreetses asukohas (nt kindlas asukohas) määratud summa.

Võimaluse korral peaksite hindama oma äriprotsessi ja proovima seda parandada, kindlustamaks, et varud ei saa olla negatiivsed. Kui peate lubama negatiivset laovaru, peaks teil olema negatiivne laovaru parandamiseks selge äriprotsess, sest see võib omahinna kulusid negatiivselt mõjutada.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Millal tuleks lubada finantsi negatiivset laovaru?

Üldiselt soovitame enamikele organisatsioonidele lubada finantsi negatiivset laovaru. (Enamasti ei töödelda ostutellimuse arveid enne, kui saate kaubad lähetada.) Peaksite selle suvandi lubama, kui teil on kindlad äriprotsessid, mis nõuavad, et müügihind kajastaks ostutellimuse lõppkulu. Näiteks võib see nõue kehtida vastavalt tellimuse majandusharule või teatud piirkondades, kus see on seadusega dikteeritud.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Mis toimub minu väljaminev kuluga, kui laoseis on negatiivne?

Kui teie kauba ladu on negatiivne ja väljastada rohkem kaupu, kui teil füüsiliselt on, kasutab süsteem vaikimisi kauba hinda jooksva keskmise arvutamiseks, kui kasutate perioodilist kulumudelit, nagu FIFO, LIFO või kaalutud keskmine. Kui kaubale ei ole vaikehinda määratud, väljastab süsteem lao väärtusega 0 (null). Selline käitumine võib põhjustada teie jooksva keskmise või liikuva keskmise tulevased kalkulatsioonid ebatäpseks.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Kas ma ei saa takistada kaupade noppimist, pakkimist või müümist müügitellimustel ja tootmistellimustel, kui vaba kaubavaru on piisavalt?

Jah. Soovitame keelata kauba mudeligrupi **suvandi** Füüsiline negatiivne, et vältida kaupade komplekteeritud, pakitud või müüdud kaupu müügitellimustel ja tootmistellimustel.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Kas ma ei saa kaupade arveldamist müügitellimusel, kui sama kauba kohta pole ostutellimusi arveldatud?

Jah. Kui sama kauba kohta **pole** ostutellimusi arveldatud, on soovitatav keelata kauba mudeligrupi suvand Rahaline negatiivne.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Kuidas mõjutab negatiivne laovaru rahalisi suhteid, nt kogukasumi marginaali?

Kui lubate laovarude negatiivseks muuta, saab laoväärtust teie bilansikontol ning kasumi- ja kahjumiaruandes müüdud kaupade hinda alata, eriti kui teie kaupade puhul vaikehinda ei konfigureerita. Seetõttu saab finantsaruandlust ja suhteid (nt kogukasumi marginaalid) üle jaotada, kuna kulu on vale. Kui kasutate perioodilist kulumudelit, nagu FIFO, LIFO või kaalutud keskmist, saab väljaminekeid korrigeerida, kui käitate lao sulgemise ja korrigeerimisprotsessi pärast negatiivsete laokoguste korrigeerimist. Ent kui kasutate liikuvat keskmist, ei ole võimalik üksikute kannete ümberhindamist.

### <a name="how-should-i-correct-negative-inventory"></a>Kuidas tuleks parandada negatiivset laovaru?

Soovitame teil sageli jälgida ja parandada negatiivset laovaru, kui teie organisatsioon või ärinõuded dikteerivad seda, et võimaldate laovarude negatiivseks muuta. Laoväärtusi saate parandada tsüklilise inventuuri, korrigeeringu sisestamise või liikumise töölehe sisestamisega. Kui peate tuvastama ootamatu kasumi laos konkreetsel pearaamatukontol, peaksite kasutama liikumise töölehte. Muul juhul sisestab süsteem tsüklilise inventuuri või laokorrektsiooni protsessi **kasutamisel** **laokorrektsiooni lao sissetuleku kontole ja tasakaalustab lao väljaminekuga kasumikontod,** mille määrate lao sisestusprofiilil.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Kas ma soovin luua uue kauba, kui minu varud on negatiivsed ja ma kasutan liikuvat keskmist?

Ei. Kui teie organisatsioon võimaldab laovarudel füüsiliselt negatiivseks minna ja te kasutate laomudelina liikuvat keskmist, **kasutab süsteem varude ja laohalduse parameetrite lehel määratud varusid ja laohalduse parameetrites** määratud taavarude kulujärjestust, et määrata, kuidas määratakse kulu teie väljaminek. Üldiselt soovitame teil vältida laovarude füüsilist negatiivset olekut. Lisateavet vt selle teema jaotisest [Negatiivne](#negative-inventory) laovaru.

## <a name="not-stocked-products"></a>Ladustamata tooted

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Kas ma saab sisestada müügitellimuste komplekteerimislehti ladustamata toodetele?

Kui te loob komplekteerimislehe müügitellimusele, mis sisaldab kaupu, mis on kauba mudeligrupis, mida ei ladustata, ei näe te nende mitte ladustatavate kaupade kohta ühtegi rida. Laohalduse mobiilirakendust ei saa kasutada ladustamata kaupade töötlemiseks.

Kui luuakse saateleht müügitellimuse jaoks, mis sisaldab kaupu, mis on kauba mudeligrupis, mida ei ladustata, **määrake väljal Kogus** *väärtuseks* Komplekteeritud kogus ja mitte ladustatud tooted, et kaasata dokumendi loomisesse mitte ladustatud kaubad. Kui valite *suvandi* Kõik, kaasatakse saatelehele ainult ladustatud kaubad.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Kas peaks kasutama ladustamata toodet või kategooriat (müügikategooria või hankekategooria)?

Ladustamata toote ja kategooria vaheline valik sõltub teie konkreetsetest ärinõuetest. Ladustamata tooted pakuvad üldiselt rohkem kontrolli vaikeväärtuste üle, nt ostutellimuste ja müügitellimuste kogused ja hinnad. Seetõttu eelistatakse ladustamata tooteid stsenaariumides, kus sama toodet või teenust ostetakse või müüakse rohkem kui üks kord. Kategooriad on kasulikud stsenaariumide puhul, kus hind, kaubad, kirjeldused jne pole vastavuses kandega. Kategooriaid saab kasutada ka mis tahes tootel, et aidata liigitada müüdava või ostetud toote tüüpi.

## <a name="service-items"></a>Teenusüksused

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Mis vahe on teenusüksusel ja mitte ladustamata tootel?

Teenusüksus on toote tüüp. Kui loote äsja väljastatud toote, saate seada välja **Toote tüüp väärtuseks** Kaup *või* *Teenus*. *Kaup* valitakse tavaliselt selleks, et näidata, et kaup on materiaalne, samas kui *teenus* on tavaliselt valitud näitamaks, et kaup on immateriaalne.

Mis tahes väljastatud toodet, sõltumata sellest, kas tegemist on kauba või teenusetootega, saab ladustada või mitte ladustada. Ladustatud või ladustamata sätet kontrollib väljastatud tootele valitud kauba mudeligrupp. Kui valite kaubagrupi, mis ei ole ladustatud, ei loo süsteem laokandeid seotud müügitellimusele või ostutellimusele.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Kas ma soovin kooslusesse kaasata ka ladustamata kaupu?

Ei, te ei saa kaasata väljastatud **toodet, mis on lingitud kauba mudeligrupiga, kus suvand Ladustamine** on koosluses või valemis keelatud. Pole tähtsust, kas välja Toote **tüüp väärtuseks** on seatud *Kaup* või *Teenus*. Koosluse- või valemiridadele saab kaasata ainult ladustatud kaupu.

## <a name="costing-modelspecific-questions"></a>Kuluarvestuse mudelipõhised küsimused

### <a name="which-costing-model-should-i-use"></a>Millist kulumudelit tuleks kasutada?

Kulumudelid, mille peaksite valima, sõltuvad teie äritegevuse nõuetest. Enne kui valite kulumudeli tarneahela haldamises kasutamiseks, peaksite kinnitama, et mudel on lubatud vastavalt kohalikele eeskirjadele. Soovitame teil kinnitada oma valiku oma regioonis sertifitseeritud raamatupidajaga.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Kas organisatsioonis saab kasutada rohkem kui ühte kulumudelit?

Jah. Tarneahela halduses valitud kauba mudeligruppide või kulumudelite arvu kohta pole piirangut.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Kas iga kauba puhul saab kasutada rohkem kui ühte kulumudelit?

Ei. Saate iga väljastatud toote jaoks valida ainult ühe kulumudeli. Seda käitumist kontrollib kauba mudeligrupp. Kui peate varude väärtuste kohta aruande pidamiseks kasutama rohkem kui ühte kulumudelit, peaksite kaaluma globaalse varude arvestuse lisandmooduli kasutamist.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Millist kulumetoodikat peaks tootmise teostamisel kasutama?

Kulumudelid, mille peaksite valima, sõltuvad teie äritegevuse nõuetest. Kui teie organisatsioon kasutab tootmise käivitamist, puudub mis tahes kulumudeli kasutamise konkreetne eelis või täitja.

### <a name="when-is-fefo-used"></a>Millal kasutatakse FEFO-t?

Esimene aegunud, esimesena välja (FEFO) ei ole kuluarvestuse metodoloogia. Selle asemel on see reserveerimisvõtte tehnika, mida kasutatakse sageli tootmisorganisatsioonides. Saate lubada FEFO reserveerimised kauba mudeligrupile, **lubades FEFO** kuupäevakontrolli suvandi ja valides seejärel väärtuse väljalt **Komplekteeringukriteeriumid**.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Kas ühe kulumudeli valimisel teise peale on jõudluse soodustused?

Üldiselt on kaubale valitud kulumudelil minimaalne mõju süsteemi üldisele jõudlusele. Valitud lao kuluarvestusmudel võib siiski mõjutada lao sulgemise või ümberarvutamise protsessi käivitamiseks kuluarvestusprotsessi aega. Näiteks kui kasutate standardset kulu või liikuvat keskmist, on lao sulgemise protsessil minimaalne mõju süsteemile, sest see ei värskenda iga laokannet ega loo tasakaalustusi. Perioodiline kulumudel nagu FIFO, LIFO või kaalutud keskmine võib siiski suurendada lao sulgemise protsessi lõpetamiseks kuluva aja arvu. Sulgemisprotsess **·** **võib** *olla pikem, kui sisestate suure arvu iteratsioonide maksimumarv kauba välja kohta või väikese arvu väljale Lao sulgemise protsessi lubatud miinimumsumma.*

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Millal tuleks kasutada valikut Fikseeritud jaehind?

Kui valite **kauba mudeligrupi** **lehel** märkeruudu Fikseeritud vastuvõtuhind, kasutab süsteem sissetuleku hinda lao sissetuleku standardkuluna. Kui ostuhinna ja toote jaoks konfigureeritud kauba vaikekuluhinna vahel on erinevus, **·** **sisestatakse erinevus fikseeritud jaehinna kasumile või fikseeritud jaehinna kahjumi** **kontole** ja tasakaalustatakse fikseeritud jaehinna vastaskontole. (Kõik need kontod on määratud väljal **Sisestusleht** .)

**Kui kasutate perioodilist kulumudelit** nagu FIFO, LIFO või kaalutud keskmine, peaksite valima märkeruudu Fikseeritud vastuvõtuhind ning soovite, et pearaamatus jälgitakse ostuhinna hälbeid, kui sissetuleku hind erineb kauba vaikekulust.

### <a name="moving-average"></a>Liikuv keskmine

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Kas liikuv keskmine on sama mis ujuv keskmine?

Mõisteid "keskmine, ujuv keskmine ja jooksev keskmine" kasutatakse sageli sünonüümselt. Nendest tingimustest on liikuv keskmine ainus ametlik kulumudel, mis on saadaval tarneahela halduses. Kuigi jooksev keskmine ei ole ametlik kulumudel, on see tehnika, mida kasutatakse selliste perioodiliste kulumudelite kasutamisel nagu FIFO, LIFO või kaalutud keskmine. Terminit "ujuv keskmine" ei kasutata tarneahela halduses ja sel võivad olla teistes süsteemides erinevad marginaalid.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Kuidas ma soovin arvesse võtta erinevust toote sissetuleku hinna ja arve hinna vahel liikuva keskmise kasutamisel?

Kui kasutate liikuvat keskmist, kasutatakse füüsilist kulu (vastuvõtuhinda) liikuva keskmise arvutamiseks kõigi väljaminekkannete puhul. Kui füüsilise omahinna (vastuvõtuhinna) ja finantskulu (arve hind) vahel on erinevus, **sisestab** süsteem automaatselt erinevuse põhikontole, mis **on** **määratud liikuva keskmise sisestustüübi hinna jaoks vahekaardil Varud vahekaardil Varude sisestusreeglid**.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Kus on pearaamatus esitatud liikuva keskmise hinnaerinevus?

Kui füüsilise värskenduse sisestamise ja sissetuleku finantsilise värskenduse vahel on hinnaerinevus, sisestatakse erinevus põhikontole, **mis** on **·** **määratud** liikuva keskmise sisestustüübi hinnaerinevuse jaoks vahekaardil Varud vahekaardil Varude sisestusreeglid. Lisateavet vt liikuva keskmise [kohta](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Mis toimub liikuva keskmise kasutamisel, kui enne sissetulekut ilmneb väljaminev väljaminev?

Tavaliselt võib enne sissetulekut olla väljaminek, kas seetõttu, et lubate kauba mudeligrupi füüsilist negatiivset laovaru või kuna väljaminek on varundatud. Lisateavet vt selle teema [jaotisest](#negative-inventory) Negatiivne laovaru.

Kui te kandeid varundate, soovitame hoolikalt kaaluda oma äriprotsessi ja operatsioone, et otsustada, kas on olemas võimalus seda stsenaariumi vältida. Kui varundate kande kaubale, mis kasutab liikuvat keskmist, määrab süsteem kandele praeguse liikuva keskmise. Hilisemaid väljaminek ei korrigeerita. Lisateavet liikuv keskmise kohta varundatud kannetega vt liikuvast [keskmisest](moving-average.md).

### <a name="standard-costing"></a>Standardne kuluarvutus

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Mis vahe on standardkulu ja fikseeritud vastuvõtuhinna vahel?

Standardne kuluarvestus nõuab kauba hinna määratlemist ja kulu aktiveerimist kuluversioonis. Seda kulu kasutatakse kõigi sissetulekute ja väljaminekte puhul. Lao sissetulekute hälbeid kirjendatakse pearaamatus, kasutades standardkulu **hälbekontosid, mille määrate vahekaardil Standardne** **kulu vahekaardil Lao sisestusreeglid**.

Kui kasutate aga fikseeritud vastuvõtuhinda, on **·** **vaid sissetulekute kulu fikseeritud ja süsteem kasutab kulu, mille määrate kiirkaardil Kulude haldamine lehel Väljastatud** toode. Erinevused vaikekulu ja ostutellimuse hinna vahel põhjustavad ostuhinna hälbe sisestamise fikseeritud jaehinna kasumi- ja kahjumikontodele. Väljaminek ei kasuta fikseeritud vastuvõtuhinda. Selle asemel hinnatakse väljaminekeid sisestamise ajal jooksva keskmise järgi (v.a juhul, kui kasutate märkimist), ja need hinnatakse ümber heuristilisele mudelile, mille valite lao sulgemisel.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Kas kasutada FEFO reserveeringuid standardse kuluarvestusega?

Jah, saate kasutada FEFO reserveeringuid kauba mudeligrupil, kui valite standardse kuluarvestuse. FEFO reserveeringud kontrollivad reserveerimisloogikat, mida kasutatakse kaupade füüsiliseks käsitsemiseks, samas kui standardne omahinna kuluarvestus kontrollib kauba füüsilist ja finantsilist kulu.

### <a name="can-i-upload-pending-prices"></a>Kas ma saab ootel hindu üles laadida?

Jah, saate ootel hinna üleslaadimiseks kasutada Exceli lisandmoodulit või andmehalduse raamistikku. Soovitame kasutada järgmisi üksusi:

- Ootel kauba hinnad (V2)
- Ootel protsessi kulukategooria ühikuhinnad
- Kuluarvutustabeli sõlme arvutustegurid (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Kui tihti saab kauba standardkulusid uuendada?

Uue standardkulu aktiveerimise sageduse kohta pole piirangut. Kui aktiveerite kaubale uue kulu samal päeval, mil viimane kulu aktiveeriti, kasutab süsteem viimati aktiveeritud kulu uute kannete või uuenduste puhul (nt olemasolevate kannete uuendused).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Kas aktiveeritud kulu saab desaktiveerida või kustutada?

Ei, aktiveeritud kulu ei saa desaktiveerida ega kustutada. Kui te olete kulu valesti aktiveerinud, saate aktiveerida uue õige kuluga kulu.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Kas kalkulatsioonigruppe kasutatakse standardse kuluarvestuse puhul?

Kalkulatsioonigruppe saab kasutada mis tahes kauba puhul, sõltumata valitud kauba mudeligrupist. Kalkulatsioonigruppe kasutatakse kulude ümberarvestuse või kulukalkulatsiooni protsessi ajal, et määrata sätted, mida tuleks kasutada kaupade puhul, mille jaoks kalkulatsiooni käitate. Lisateavet kalkulatsioonigruppide kohta vt koosluse [kalkulatsioonigruppidest](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Millal peaks kasutama planeeritud kuluversiooni?

Kuluversioonide tüüp võib olla Standardne *kulu või* *Planeeritud kulu*. Standardkulu *tüüpi* kasutatakse kulude puhul, mis on süsteemis aktiivsed ja sisestatakse kannetesse. Planeeritud *kulu* tüüpi kasutatakse kulude simulatsioonide käivitamiseks ja see ei mõjuta kannete kulu.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Kas müügikuluna saab ühe üksuse kogukulu teise üksusesse üle kanda?

Puudub automatiseeritud viis kulude kopeerimiseks ühest ettevõttest teise. Lisaks puudub automaatne viis kulude kopeerimiseks ostuhinnast müügihinnale. Kui teie organisatsioon peab täitma ühe neist ülesannetest, kaaluge, kas saate andmehalduse raamistikku kasutada andmete eksportimiseks oma kuluversioonist ja laadida üles teise ettevõttesse, kas omahinnana kuluversioonis või kaubanduslelepinguna. Failide käsitsi manipulatsioon võib olla nõutav.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Milline on parim viis planeeritud kulude kopeerimiseks standardne kuluversioon?

Saate kasutada nuppu **Kopeeri** kuluversioonide **lehel**, et kopeerida kauba hinnad, kulukategooria hinnad või kaudsed kulud ühest kuluversioonist teise.
