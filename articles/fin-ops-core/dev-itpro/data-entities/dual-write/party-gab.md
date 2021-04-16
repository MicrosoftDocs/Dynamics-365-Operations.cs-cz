---
title: Strana a globální adresář
description: Toto téma popisuje funkci strany a globálního adresáře duálního zápisu.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750781"
---
# <a name="party-and-global-address-book"></a>Strana a globální adresář

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Strana a globální adresář jsou pojmy aplikací Finance and Operations. Stranou může být osoba nebo organizace. Je vhodné globálně ukládat a spravovat vlastnosti **strany**, například jméno, jazyk, kontakty a adresy. Když se hodnota vlastnosti změní na jednom místě, projeví se to na všech místech, kde je **Strana** zapojena.

## <a name="party"></a>Strana

*Strana* je osoba nebo organizace zapojená do podnikání. Pomocí konceptu strany může osoba nebo organizace hrát v podniku více než jednu roli (pracovník, zákazník, dodavatel nebo kontakt). Role je založena na kontextu a účelu. Zde je několik příkladů pro dvě fiktivní společnosti Contoso a Fabrikam.

+ **Pracovník**: Zaměstnanec. Například zaměstnanec společnosti Contoso.
+ **Dodavatel**: Dodavatelská organizace nebo jediný majitel, který dodává zboží či služby nějakému podniku. Například pokud společnost Fabrikam prodává zásoby společnosti Contoso, pak je Fabrikam v roli dodavatele.
+ **Kontakt**: Osoba, kterou je třeba kontaktovat. Například pokud společnost Contoso nakupuje zásoby od společnosti Fabrikam, zaměstnanec společnosti Contoso by se spojil s kontaktem ve společnosti Fabrikam.
+ **Zákazník**: Zákazník je osoba nebo společnost, která nakupuje věci od společnosti. Například pokud společnost Contoso nakupuje zásoby od společnosti Fabrikam, pak je společnost Contoso zákazníkem společnosti Fabrikam.

Model strany se často používá k reprezentaci středních až složitých vztahů mezi organizacemi a lidmi, zvláště když strana hraje více než jednu roli. Několik běžných příkladů:

+ Strana může být zákazníkem i dodavatelem. Například v Severní Americe společnost Fabrikam prodává elektrické dráty společnosti Contoso a nakupuje sestavené reproduktory od společnosti Contoso. V Evropě Fabrikam prodává díly společnosti Contoso, ale nic od společnosti Contoso nekupuje.
+ Strana může být zaměstnancem i zákazníkem. Například zaměstnanec společnosti Contoso nakupuje elektroniku od společnosti Contoso pro osobní použití.
+ Mezi člověkem a organizací může existovat vztah N:N. Například společnost Fabrikam dodává servisní specialisty a zaměstnává koordinátora umístění. Koordinátor přiděluje servisní specialisty k pracovním požadavkům od několika zákazníků společnosti Fabrikam. Contoso je jedním ze zákaznických účtů. Když společnost Contoso potřebuje odborníka, kontaktuje společnost Contoso koordinátora, který pak žádost zprostředkuje. Koordinátor vyřizuje požadavky pro všechny zákazníky a vytváří vztah typu N:N.

Následující obrázek ukazuje datový model pro stranu:

![Datový model pro stranu](media/party-gab-image1.png)

> [!Tip]
> Když se pokoušíte vytvořit nový záznam účtu, použijte pole „Strana“ k vyhledání záznamu podle názvu. V případě, že záznam najdete, stačí záznam vybrat. Systém automaticky vyplní všechna data ze strany. Nemusíte ručně zadávat všechna požadovaná pole. Toto chování najdete na integrovaných formulářích účtu, kontaktu a dodavatele.

Duální zápis nepodporuje všechny role stran aplikací Finance and Operations. Úplný seznam rolí stran najdete v části [Přehled globálního adresáře](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globální adresář

Globální adresář je adresář poštovních a elektronických adres organizací a jednotlivců účastnících se podnikání.

Globální adresář ukládá a zpracovává tolik poštovních adres a elektronických adres, kolik je potřeba. Předpokládejme například, že společnost Fabrikam má čerpací stanice na 50 místech. Každé místo má jinou poštovní adresu, e-mail a telefonní číslo. Všechny nákupy jsou účtovány na hlavní čerpací stanici, ale nákupy jsou dodávány přímo na konkrétní čerpací stanici, která o nákup požádala. Globální adresář ukládá hlavní čerpací stanici jako fakturační adresu a každou čerpací stanici jako dodací adresu společnosti Fabrikam. Adresy lze uložit jednou a podle potřeby je načítat pro nabídky a objednávky.

Osoba nebo organizace může hrát více než jednu roli na základě obchodního kontextu. Pokud tak učiní, jejich poštovní a elektronické adresy mohou být stejné. V takovém případě by se změna adresy v jedné roli měla objevit ve druhé roli a naopak. Globální adresář ukládá a zpracovává adresy globálně.

![Datový model pro globální adresář](media/party-gab-image2.png)

## <a name="contacts"></a>Kontakty

V aplikacích pro zapojení zákazníků je *Kontakt* osobou. Nicméně tabulka **Kontakt** byla přetížena, aby představovala osobu, uživatele portálu, zákazníka B2C nebo dodavatele. Reprezentace je implicitní a bez prozkoumání souvisejících transakcí nerozeznáte rozdíl. Tabulka **Kontakt** byla omezena na relaci 1: 1 s tabulkou **Účet**. Jako součást modelu strany a globálního adresáře přináší duální zápis explicitní vlastnosti pro klasifikaci, a duální zápis umožňuje vztahy N: N mezi osobou **Kontakt** a organizací (entitou účtu nebo entitou dodavatele).

Existují dva typy řádků **Kontakt**:

+ Prokládaný kontakt – řádek kontaktu s povinnou hodnotou v poli **Společnost**.
+ Neprokládaný kontakt – řádek kontaktu s prázdným polem **Společnost**.

Tabulka **Kontakt** může ukládat tyto typy řádků:

Typ řádku | popis
---|---
Osoba, která je zákazníkem, například prodejní kontakt nebo zákazník B2C. | Záznam prokládaného kontaktu, kde pole **Společnost** není prázdné a pole **Je zákazník** je nastaveno na **Ano**.
Osoba, která je dodavatelem, například jediný vlastník, jako je dodavatel. | Záznam prokládaného kontaktu, kde pole **Společnost** není prázdné a pole **Je dodavatel** je nastaveno na **Ano**.
Osoba,, která je zákazníkem i dodavatelem. | Záznam prokládaného kontaktu, kde pole **Společnost** není prázdné, pole **Je zákazník** je nastaveno na **Ano** a pole **Je dodavatel** je nastaveno na **Ano**. Osoba může být jak výrobcem jednoho produktu, tak spotřebitelem jiného produktu. Tuto relaci podporují jak aplikace Finance and Operations, tak duální zápis.
Osoba, která je kontaktní osobou pro organizaci, ale není zákazníkem ani prodejcem. | Záznam neprokládaného kontaktu, kde pole **Společnost** je prázdné, pole **Je zákazník** je nastaveno na **Ne** a pole **Je dodavatel** je nastaveno na **Ne**.

## <a name="contact-for-party"></a>Kontakt pro stranu

**Kontakt pro stranu** ukládá a zpracovává vztahy N: N mezi řádky tabulky **Účet** a řádky tabulky **Kontakt**. Prokládané řádky tabulky **Kontakt** můžete odfiltrovat od neprokládaných řádků a přidružit pouze neprokládané řádky **Kontakt** k řádkům tabulek **Účet** nebo **Dodavatel**.

Například Natasha Jones a Miguel Reyes jsou veterináři, kteří se starají o farmy ve svých oblastech. Natasha obsluhuje oblast Seattle a Miguel obsluhuje oblast Kent. V aplikaci pro interakci se zákazníky jsou farmy vyjádřeny jako zákazníci a veterináři jsou kontaktní osoby. Jediný záznam **Kontakt** pro Natašu je spojen se všemi farmami, na kterých Nataša pracuje. Obdobně je jediný záznam **Kontakt** pro Miguela spojen se všemi farmami, na kterých Miguel pracuje.

Tyto relace jsou uloženy v tabulce **Kontakt pro stranu**. Informace najdete v integrovaných formulářích:

+ Když jste ve formuláři **Účet**, najdete v něm kartu s názvem **Přidružené kontakty**. Tato karta slouží k přidružení jednoho nebo více kontaktů k řádku tabulky **Účet**. V tomto formuláři přiřazujete kontaktní osobu pro organizaci. Po přiřazení kontaktů si můžete vybrat jeden z nich jako primární kontakt pro daný účet. Ve formuláři **Rychlé vytvoření** můžete vybrat pouze kontaktní osobu. Chování je stejné, když používáte formulář **Dodavatel** a typ záznamu je **Organizace**.
+ Když jste ve formuláři **Kontakt** a řádkem je zákazník nebo prodejce nebo oba dva (prokládaný kontakt), najdete zde kartu s názvem **Přidružené kontakty**. Tato karta slouží k přidružení jednoho nebo více kontaktů. V tomto formuláři přiřazujete kontaktní osobu pro zákazníka nebo dodavatele B2C. Po přiřazení kontaktů si můžete vybrat jeden z nich jako primární kontakt. Ve formuláři **Rychlé vytvoření** můžete vybrat pouze kontaktní osobu.
+ Když jste ve formuláři **Kontakt** a řádkem je kontaktní osoba (neprokládaný kontakt), najdete zde kartu s názvem **Přidružené organizace**. Tato karta slouží k přidružení jednoho nebo více zákazníků či dodavatelů. V tomto formuláři přiřazujete zákazníka nebo dodavatele k základní kontaktní osobě. Zákazníkem nebo prodejcem může být organizace, osoba nebo obojí. Ze čtyř polí můžete vybrat pouze jednu hodnotu současně.

    ![Karta Přidružené organizace](media/party-gab-image3.png)

    + Když zvolíte **ID strany**, poté je základní kontakt přiřazen všem rolím vybrané strany.
    + Když zvolíte **Přidružený kontakt**, pak vybíráte prokládaný kontakt typu osoba.
    + Když zvolíte **Přidružený účet** nebo **Dodavatel**, pak vybíráte organizaci.

    Bez ohledu na váš výběr je přidružení vytvořeno na úrovni strany a je použitelné na všechny role strany a je uloženo v entitě „Kontakt pro stranu“.

> [!Note]
> Zobrazovaný název pro tabulku **Kontakt pro stranu** v aplikaci pro zapojení zákazníků je **Kontakt pro zákazníka/dodavatele**.

Když otevřete řádek **Kontakt**, kde pole **Je zákazník** má hodnotu **Ne** a pole **Je dodavatel** hodnotu **Ne**, uvidíte kartu **Přidružené organizace**. Tato karta slouží k přidružení jedné nebo více organizací zákazníků nebo dodavatelů ke kontaktu.

Když otevřete řádek **Kontakt**, kde pole **Je zákazník** má hodnotu **Ano**, nebo kde pole **Je dodavatel** má hodnotu **Ano**, uvidíte kartu **Přidružené kontakty**. Tato karta slouží k přidružení jednoho nebo více kontaktů.

## <a name="postal-address"></a>Poštovní adresa

Do formulářů **Účet**, **Kontakt** a **Dodavatel** byla přidána nová karta s názvem **Adresy**. Kartu **Adresy** podporující N adres pomocí mřížky vidíte na tomto obrázku:

![Mřížka pro poštovní adresu](media/party-gab-image4.png)

+ Sloupec **Role poštovní adresy** uvádí účel adresy.
+ Sloupec **Je primární** uvádí primární adresu.
+ Sloupec **Číslo adresy** uvádí pořadí adresy.
+ Tlačítko **+ Nová adresa** umožňuje vytvořit novou adresu. Můžete vytvořit tolik adres, kolik chcete.

Pole **Adresa 1** a **Adresa 2** na kartě **Souhrn** formuláře **Účet** odpovídají adresám **Dodávka** a **Faktura**.

![Karta Souhrn pro poštovní adresu](media/party-gab-image5.png)

Pole **Adresa 1**, **Adresa 2** a **Adresa 3** na kartě **Souhrn** formuláře **Kontakt** odpovídají adresám **Podnik**, **Dodávka** a **Faktura**.

## <a name="electronic-address"></a>Elektronická adresa

Do formulářů **Účet**, **Kontakt** a **Dodavatel** byla přidána nová karta s názvem **Elektronické adresy**. Kartu **Adresy** podporující N adres pomocí mřížky vidíte na tomto obrázku:

![Mřížka pro elektronickou adresu](media/party-gab-image6.png)

+ Ve sloupci **Typ** je uveden typ adresy.
+ Sloupec **Je primární** uvádí primární adresu.
+ Sloupec **Účel** uvádí účel elektronické adresy.
+ Tlačítko **+ Nová elektronická adresa** umožňuje vytvořit novou adresu. Můžete vytvořit tolik adres, kolik chcete.

Elektronické adresy jsou k dispozici pouze v této mřížce. V budoucích verzích budou všechna pole elektronické a poštovní adresy odstraněna z jiných karet, například karet **Souhrn** a **Detaily**.

## <a name="setup-instructions"></a>Pokyny pro nastavení

Pokud jste stávajícím zákazníkem s duálním zápisem, jsou vyžadovány následující pokyny k nastavení. Jinak můžete tuto část přeskočit.

1. Ukončete následující mapování, protože již nejsou nutná. Místo toho spusťte mapování Kontakty V2 (msdyn_contactforparties).

    + Kontakty CDS V2 a Kontakty (týká se zákaznických kontaktů)
    + Kontakty CDS V2 a Kontakty (týká se dodavatelských kontaktů)

2. Následující mapování entit jsou aktualizována pro funkčnost strany, takže na tato mapování musí být použita nejnovější verze.

Zobrazit na mapě | Aktualizujte na tuto verzi | Změny
---|---|---
Zákazníci V3 (accounts) | 1.0.0.5 |Odebráno číslo strany a další pole týkající se strany, jako je jméno, osobní detaily, pole poštovní adresy, pole elektronické kontaktní adresy atd.
Zákazníci V3 (contacts) | 1.0.0.5 | Odebráno číslo strany a další pole týkající se strany, jako je jméno, osobní detaily, pole poštovní adresy, pole elektronické kontaktní adresy atd.
Dodavatelé V2 (msdyn_vendors) | 1.0.0.6 | Odebráno číslo strany a další pole týkající se strany, jako je jméno, osobní detaily, pole poštovní adresy, pole elektronické kontaktní adresy atd.
Záhlaví prodejní nabídky CDS (quotes) | 1.0.0.6 | Nahrazuje kontaktní osobu referencí ContactforParty.
Záhlaví prodejní faktury V2 (invoices) | 1.0.0.4 | Nahrazuje kontaktní osobu referencí ContactforParty.
Záhlaví prodejní objednávky (salesorders) | 1.0.0.5 | Nahrazuje kontaktní osobu referencí ContactforParty.
Kontakty V2 (msdyn_contactforparties) | 1.0.0.2 | Toto je nová mapa. Pokud máte předchozí verzi řešení strany, nezapomeňte aktualizovat tuto mapu na nejnovější verzi, jak je uvedeno.
Umístění poštovní adresy strany CDS (msdyn_partypostaladdresses) | 1.0.0.1  | Toto je nová mapa přidaná jako součást předchozího vydání preview strany.
Historie poštovních adres CDS V2 (msdyn_postaladdresses) | | Toto je nová mapa přidaná jako součást předchozího vydání preview strany.
Umístění poštovní adresy strany CDS (msdyn_postaladdresscollections) | | Toto je nová mapa přidaná jako součást předchozího vydání preview strany.
Kontakty strany V3 (msdyn_partyelectronicaddresses) | | Toto je nová mapa přidaná jako součást tohoto vydání.

## <a name="templates"></a>Šablony

Kolekce mapování tabulek pracují společně pro interakci strany a globálního adresáře, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Aplikace Customer Engagement     | popis
----------------------------|-----------------------------|------------
[Tituly kontaktní osoby](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Zákazníci V3](mapping-reference.md#101) | účty |
[Zákazníci V3](mapping-reference.md#116) | kontakty |
[Strany CDS](mapping-reference.md#220) | msdyn_parties |
[Místa poštovní adresy strany CDS](mapping-reference.md#233) | msdyn_partypostaladdresses |
[Historie poštovní adresy CDS V2](mapping-reference.md#235) | msdyn_postaladdresses |
[Místa poštovní adresy CDS](mapping-reference.md#234) | msdyn_postaladdresscollections |
[Záhlaví prodejní nabídky CDS](mapping-reference.md#215) | nabídky |
[Záhlaví prodejní objednávky CDS](mapping-reference.md#217) | salesorders |
[Zdvořilostní zakončení](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Kontakty V2](mapping-reference.md#221) | msdyn_contactforparties |
[Role v rozhodovacím procesu](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Pracovní funkce zaměstnání](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Úrovně věrnosti](mapping-reference.md#226) | msdyn_loyaltylevels |
[Kontakty strany V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Typy osobní charakteristiky](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Záhlaví prodejní faktury V2](mapping-reference.md#118) | faktury |
[Oslovení](mapping-reference.md#228) | msdyn_salutations |
[Dodavatelé V2](mapping-reference.md#202) | msdyn_vendors |

Další informace viz [Odkaz na mapování duálního zápisu ](mapping-reference.md).
