---
ms.openlocfilehash: 22911afd3a3da0ce3bcaeb7e42ab0096c868be547d559f14a91e09d6e6e12c08
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777060"
---
Kui kopeerite andmebaasi ühest keskkonnast teise, peate enne kopeeritud andmebaasi täielikku töölehakkamist käivitama keskkonna uuesti ettevalmistamise tööriista, et kõik kaubanduse komponendid oleks ajakohased.

> [!IMPORTANT]
> Soovitame teil käivitada see protseduur, ükskõik kas kasutate kaubanduse komponente või mitte, kuna kaubandus on olemas kõigis keskkondades. 

Enne jätkamist peate veenduma, et järgmised tingimused on täidetud.
1. Kui lähete üle 2017. aasta versioonile (teise nimega 7.2) 7.2.11792.56024, rakendage sihtkeskkonnas järgmised rakenduse X++ kiirparandused, enne kui käivitate selles keskkonnas andmete versioonitäienduse. Need hoiavad andmete versioonitäienduse ajal ära mitmesuguste tõrgete tekkimise.

    - KB 4036156 – Retaili vaheversiooni täiendus – „Variandi numbriseeriat pole määratud.“ See paranduspakett sisaldab ka värskendusi KB 4035399 ja KB 4035751. Võtke arvesse, et selle paketi kasutamiseks peab teil olema vähemalt platvormivärskendus 9. Kui te pole kindel, installige uusimad binaarfailid.
    
2. Kui täiendate versiooni Microsoft Dynamics AX 2012, installige enne andmete versioonitäienduse käivitamist sihtkeskkonnas järgmised rakenduse X++ parandused:
    - KB 4033183 – Dynamics AX 2012 R2 või Dynamics AX 2012 R3 Pre-CU8 mitte-Retaili versioonitäiendus nurjub, kuna dbo.RETAILTILLLAYOUTZONE objekti ei leitud.
    - KB 4040692 – Dynamics AX 2012 R3 üleminek versioonile Microsoft Dynamics 365 for Operations 7.2 nurjub RetailSalesLine'i topeltindeksiga SalesLineIdx-is.
    - KB 4035490 – jõudlusprobleem GeneralJournalAccountEntry välja MainAccount versioonitäiendusskriptiga.


Järgige keskkonna uuesti ettevalmistamise tööriista käivitamiseks neid juhiseid.

1. Valige ühiste vahendite teegis **Tarkvara juurutatav pakett**.
2. Laadige alla keskkonna uuesti ettevalmistamise tööriist.
3. Valige oma projekti ühiste vahendite teegis **Tarkvara juurutatav pakett**.
4. Valige uue paketi loomiseks **Uus**.
5. Sisestage paketi nimi ja kirjeldus. Paketi nimeks võite määrata **Keskkonna uuesti ettevalmistamise tööriist**.
6. Laadige üles varem alla laaditud pakett.
7. Tehke oma sihtkeskkonna lehel **Keskkonna üksikasjad** valik **Halda** > **Rakenda värskendused**.
8. Valige keskkonna uuesti ettevalmistamise tööriist, mille varem üles laadisite, ja siis valige paketi rakendamiseks **Rakenda**.
9. Jälgige paketi juurutamise edenemist. 

Lisateavet juurutatava paketi rakendamise kohta leiate teemast [Juurutatava paketi rakendamine](../deployment/create-apply-deployable-package.md). Lisateavet juurutatava paketi käsitsi rakendamise kohta leiate teemast [Juurutatava paketi installimine](../deployment/install-deployable-package.md).
