---
title: Töötamine elektrooniliste sõnumite funktsiooniga
description: See artikkel annab teavet selle kohta, kuidas töötada elektrooniliste teadete (EM) funktsiooniga.
author: AdamTrukawka
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 929d3d3aad249007264204a3fd51377c8bb42377
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279268"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Töötamine elektronsõnumite funktsiooniga

[!include [banner](../includes/banner.md)]

Kui töötate sõnumi tasemel, on leht **Elektronsõnumid** (**Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumid**) kasulikum. Kui tegutsete andmete kogumise (sõnumiüksuse) tasemel, on **Elektronsõnumi üksused** lehel (**Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumi üksused**) kõige kasulikum.

## <a name="electronic-messages"></a>Elektronsõnumid

Leht **Elektronsõnumid** võimaldab töötlemist, mis on teie rolli põhjal teile saadaval. Turberollid on seostatud töötlemisega selle töötlemise seadistuses. Iga töötlemise jaoks, mis on teile saadaval, kuvab leht elektronsõnumid ja nendega seotud teabe.

Kiirkaardil **Sõnumid** kuvatakse elektronsõnumid valitud töötlemise jaoks. Olenevalt valitud sõnumi olekust ja eelmääratletud töötlemisest saate käivitada teatud tegevusi, kasutades ruudustiku kohal olevaid nuppe.

- **Uus** – see nupp on seotud tegevustega, mille tüüp on **Loo sõnum**.
- **Kustuta** – see nupp on saadaval, kui valitud sõnumi praeguse oleku jaoks on valitud märkeruut **Luba kustutamine**.
- **Kogu andmeid** – see nupp on seotud tegevustega, mille tüüp on **Kirjete asutamine**.
- **Loo aruanne** – see nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**.
- **Saada aruanne** – see nupp on seotud tegevustega, mille tüüp on **Veebiteenus**.
- **Impordi vastus** – see nupp on seostatud tegevustega, mille tüüp on **Elektroonilise aruandluse importimine**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine sõnumi tasemel**.
- **Sõnumiüksused** – avab lehe **Elektronsõnumi üksused**.

Kiirkaart **Tegevuste logi** kuvab teabe kõigi tegevuste kohta, mis on valitud sõnumi jaoks käivitatud. Kui tegevus põhjustas tõrke, lisatakse teave tõrke kohta ruudustikus seotud reale. Tõrke kohta teabe vaatamiseks valige ruudustikus rida ja seejärel valige lehe ülanurgas nupp **Manus** (kirjaklambrisümbol).

Kiirkaart **Sõnumi lisaväljad** kuvab kõik lisaväljad, mis on sõnumite jaoks määratletud töötlemise seadistuses. See kiirkaart sisaldab lisaks nende lisaväljade väärtusi.

Kiirkaart **Sõnumiüksused** kuvab kõik sõnumiüksused, mis on seotud valitud sõnumiga. Olenevalt valitud sõnumiüksuse olekust saate käivitada teatud tegevusi, kasutades ruudustiku kohal olevaid nuppe.

- **Kustuta** – see nupp on saadaval, kui valitud sõnumiüksuse praeguse oleku jaoks on valitud märkeruut **Luba kustutamine**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine**.
- **Algdokument** – saate avada lehe, millel kuvatakse valitud sõnumiüksuse algdokument.

Kõik sõnumi puhul juba loodud ja vastu võetud aruanded on sellele sõnumile manustatud. Sõnumiga seotud manuste vaatamiseks valige sõnum ja seejärel valige lehe ülanurgas nupp **Manus** (kirjaklambrisümbol).

![Nupp Manus](media/attachment-icon.png)

Lehel **Manused** kuvatakse kõik valitud sõnumiga seotud manused. Faili vaatamiseks valige see vasakul olevast loendist ja seejärel valige toimingupaanil nupp **Ava**.

![Nupp Ava](media/open-button.png)

Saate ka vaadata manuseid, mis on seotud sõnumi puhul varem käivitatud konkreetse tegevusega. **Elektroonilised sõnumid** lehel **Sõnumid** kiirkaardil valige sõnum. **Toimingu** logi kiirkaardil valige toiming ja seejärel valige lehe ülemises parempoolses nurgas nupp **Manus** (paberiklambri sümbol).

Saate käivitada kas kogu töötlemise või ainult kindla tegevuse, valides toimingupaanil nupu **Käivita töötlemine**.

## <a name="electronic-message-items"></a>Elektronsõnumi üksused

Lehel **Elektronsõnumi üksused** on esitatud kõik sõnumiüksused ja iga sõnumiüksuse jaoks käivitatud tegevuste logi. Sellel lehel kuvatakse ka lisaväljad, mis on sõnumiüksuste jaoks määratletud, ja nende lisaväljade väärtused.

Järgmises tabelis kirjeldatakse vahekaardi **Sõnumiüksused**.

<table>
<thead>
<tr>
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Teostamine</td>
<td>Sõnumiüksuse loomiseks kasutatud töötlemise nimi.</td>
</tr>
<tr>
<td>Sõnumiüksus</td>
<td>Sõnumiüksuse ID. ID määratakse automaatselt, võttes aluseks <b>Sõnumiüksus</b> numbriseeria mis on määratletud lehel <b>Pearaamatu parameetrid</b>.</td>
</tr>
<tr>
<td>Sõnumiüksuse kuupäev</td>
<td>Sõnumiüksuse loomise kuupäev.</td>
</tr>
<tr>
<td>Sõnumiüksuse tüüp</td>
<td>Sõnumiüksuse tüüp. Sama töötlemise jaoks saab seadistada mitut tüüpi sõnumiüksusi (nt <b>Sissetulevad arved</b> ja <b>Väljaminevad arved</b>). Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
</tr>
<tr>
<td>Sõnumiüksuse olek</td>
<td><p>Sõnumiüksuse tegelik olek. Saadaolevad olekud on olenevalt sõnumiüksuse tüübist erinevad. Järgmisena on toodud mõned näited.</p>
<ul>
<li><b>Asustatud</b> – kirje lisati sõnumiüksuste tabelisse.</li>
<li><b>Hinnatud</b> – sõnumiüksuse jaoks arvutati lisaatribuudid.</li>
<li><b>Esitatud</b> – sõnumiüksuse lisati aruandele.</li>
<li><b>Välja jäetud</b> – see olek võib olla kasulik, kui peate aruandest enne selle eksportimist mõned sõnumiüksused välja jätma.</li>
</ul>
</td>
</tr>
<tr>
<td>Edastuse kuupäev</td>
<td>Töötlemise jaoks, mis edastab loodud aruande automaatselt väljapoole süsteemi, sõnumiüksuse edastamise kuupäev.</td>
</tr>
<tr>
<td>Dokumendi number</td>
<td>See väli täidetakse kirjete asustamise tegevuse seadistuse alusel automaatselt. Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
</tr>
<tr>
<td>Konto number</td>
<td>Kliendi või hankija kontonumber (või muu välja väärtus, olenevalt väljast, mis on määratletud kirjete asustamise tegevuses). Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
</tr>
<tr>
<td>Sõnum</td>
<td>Sõnumi kood. Kood määratakse automaatselt, võttes aluseks numbriseeria <b>Sõnum</b> mis on määratletud lehel <b>Pearaamatu parameetrid</b>.</td>
</tr>
<tr>
<td>Teate olek</td>
<td>Elektronsõnumi tegelik olek.</td>
</tr>
<tr>
<td>Järgmine tegevus</td>
<td>Järgmised tegevused, mille saab sõnumiüksuse praeguse oleku jaoks käivitada.</td>
</tr>
</tbody>
</table>

Vahekaart **Lisaväljad** kuvab lisaväljad valitud sõnumiüksuse jaoks, ja nende väärtused.

### <a name="run-processing"></a>Töötlemise käivitamine

Valige toimingupaanil **Töötlemise käivitamine**, et käivitada sõnumiüksuste töötlemine. Kindla tegevuse käivitamiseks määrake dialoogiboksis **Töötlemise käivitamine** suvandi **Vali tegevus** sätteks **Jah** ja seejärel valige tegevus. Kogu töötlemise käivitamiseks jätke suvandi **Vali tegevus** sätteks **Ei**.

### <a name="generate-report"></a>Aruande loomine

Valige toimingupaanil **Loo aruanne**. See nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimine**.

### <a name="update-status"></a>Värskenda olekut

Valige toimingupaanil **Värskenda olekut**, et värskendada ühe või mitme sõnumiüksuse olekut. Dialoogiboksis **Värskenda olekut** kasutage kiirkaarti **Kaasatavad kirjed**, et valida värskendatavad sõnumiüksused. Veenduge, et määratleksite valikukriteeriumid õigesti, sest sõnumiüksuse olekud värskendatakse nende kriteeriumide, valitud tegevuse esialgse oleku ja teie määratud väärtuse **Uus olek** järgi. Kui oleku värskendamine on lõpule viidud, on keeruline määratleda, milliseid üksusi just värskendati. Seetõttu on olekuvärskendust raske tagasi võtta.

### <a name="electronic-messages"></a>Elektronsõnumid

Valige toimingupaanil suvand **Elektronsõnumid**, et vaadata üle valitud sõnumiüksusega seotud elektronsõnum.

Saate üle vaadata ka kõik kindla sõnumiüksusega seotud failid. Valige sõnumiüksuse väli **Sõnum** või valige toimingupaanil suvand **Elektronsõnumid**. Seejärel valige lehel **Elektronsõnum** sõnum, mille faile soovite üle vaadata, ja seejärel valige lehe ülanurgas nupp **Manus** (kirjaklambrisümbol).

Lehel **Manused** kuvatakse kõik manused, mis on sõnumiga seotud. Faili vaatamiseks valige see vasakul olevast loendist ja seejärel valige toimingupaanil nupp **Ava**.

### <a name="original-document"></a>Algdokument

Valige toimingupaanil **Algdokument**, et avada valitud sõnumiüksuse algdokument.
